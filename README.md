# Comments Manager Frontend

A modern, responsive web application for managing comments with full CRUD (Create, Read, Update, Delete) operations. Built with vanilla HTML, CSS, and JavaScript with a beautiful gradient-based design.

## 🌟 Features

- **Add Comments**: Create new comments with task ID and content
- **View Comments**: Display all comments or retrieve a specific comment by ID
- **Edit Comments**: Inline editing with cancel functionality
- **Delete Comments**: Remove comments with confirmation dialog
- **Real-time Updates**: Automatic refresh after operations
- **Responsive Design**: Works seamlessly on desktop and mobile devices
- **Modern UI**: Beautiful gradient design with smooth animations

## 🚀 Getting Started

### Prerequisites

- A web browser (Chrome, Firefox, Safari, Edge)
- A local web server (optional, but recommended)
- Backend API server running on `http://localhost:1234`

### Installation

1. Clone or download this repository
2. Navigate to the project directory
3. Open `index.html` in your web browser, or serve it using a local web server

### Using a Local Server (Recommended)

For better development experience and to avoid CORS issues:

```bash
# Using Python 3
python -m http.server 8000

# Using Node.js (if you have http-server installed)
npx http-server

# Using PHP
php -S localhost:8000
```

Then open `http://localhost:8000` in your browser.

## 🔧 API Configuration

The application expects a REST API server running on `http://localhost:1234` with the following endpoints:

- `GET /api/comments/` - Retrieve all comments
- `GET /api/comments/{id}` - Retrieve a specific comment
- `POST /api/comments/` - Create a new comment
- `PUT /api/comments/{id}` - Update an existing comment
- `DELETE /api/comments/{id}` - Delete a comment

### API Request/Response Format

**Create/Update Comment Request:**
```json
{
  "task_id": 1,
  "content": "This is a comment"
}
```

**Comment Response:**
```json
{
  "id": 1,
  "task_id": 1,
  "content": "This is a comment"
}
```

## 📱 Usage

### Adding a Comment
1. Fill in the "Task ID" field with a numeric value
2. Enter your comment content (max 200 characters)
3. Click "Add Comment"

### Viewing Comments
- All comments are automatically loaded when the page opens
- Click "Refresh" to reload all comments
- Enter a specific comment ID in the "Get Single Comment" section to view one comment

### Editing a Comment
1. Click the "Edit" button on any comment card
2. The form will populate with the existing values
3. Make your changes and click "Update Comment"
4. Click "Cancel" to abort the edit operation

### Deleting a Comment
1. Click the "Delete" button on any comment card
2. Confirm the deletion in the popup dialog

## 🎨 Design Features

- **Gradient Background**: Beautiful purple-to-blue gradient
- **Glass Morphism**: Semi-transparent containers with backdrop blur
- **Smooth Animations**: Hover effects and transitions
- **Responsive Layout**: Adapts to different screen sizes
- **Color-coded Elements**: Different colors for IDs, task references, and actions

## 📁 Project Structure

```
frontend/
├── index.html          # Main HTML file with embedded JavaScript
├── styles.css          # CSS styles and responsive design
└── README.md          # This documentation file
```

## 🔄 Status Messages

The application provides real-time feedback through status messages:

- ✅ **Success**: Green messages for successful operations
- ❌ **Error**: Red messages for failed operations or validation errors
- ⏳ **Loading**: Displayed while fetching data

## 🌐 Browser Compatibility

- Chrome 60+
- Firefox 55+
- Safari 12+
- Edge 79+

## 🛠️ Customization

### Changing API Endpoint

Update the `API_BASE` constant in the JavaScript section of `index.html`:

```javascript
const API_BASE = 'https://your-api-domain.com/api/comments';
```

### Styling Modifications

All styles are contained in `styles.css`. Key customization areas:

- **Colors**: Modify the gradient values in the CSS custom properties
- **Layout**: Adjust container max-width and padding values
- **Typography**: Change font families and sizes
- **Animations**: Modify transition durations and hover effects

## 🚨 Error Handling

The application handles common error scenarios:

- Network connectivity issues
- API server unavailability
- Invalid comment IDs (404 errors)
- Form validation errors
- Confirmation dialogs for destructive actions

## 📝 Notes

- Comment content is limited to 200 characters
- All operations require a valid API connection
- The application automatically scrolls to the form when editing
- Delete operations require user confirmation

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
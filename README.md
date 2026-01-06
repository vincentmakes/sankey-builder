# Sankey Diagram Editor

A modern, browser-based WYSIWYG editor for creating and editing Sankey diagrams. Built as a single HTML file with no external dependencies (except Google Fonts and Material Icons).

![Sankey Diagram Editor Screenshot](screenshot.png)

## Features

### Diagram Editing
- **Visual WYSIWYG editing** - Click flows to edit colors and values directly on the diagram
- **Drag-and-drop nodes** - Reposition nodes vertically by dragging
- **Right-click context menu** - Add or remove flows from nodes
- **Real-time updates** - Changes reflect immediately in the diagram

### Flow Management
- **Individual flow colors** - Each flow can have its own color (no forced inheritance)
- **Quick color picker** - Click any flow to access a color palette
- **Editable data table** - Modify source, target, value, and color for each flow
- **Add/delete flows** - From the sidebar or directly on the diagram

### Display Options
- **Show/hide node values** - Toggle value display next to node names
- **Show/hide flow values** - Display values on flow paths
- **Tooltips** - Hover over flows and nodes for detailed information
- **Customizable background** - Choose from preset colors with optional dot pattern

### Import/Export
- **JSON import/export** - Save and load diagram data
- **SVG export** - Export high-quality vector graphics with embedded styles
- **Persistent state** - All settings and positions are preserved in exports

### UI Features
- **Resizable sidebar** - Drag to adjust panel width
- **Tabbed interface** - Organized Flows, Nodes, and Settings panels
- **Zoom controls** - Zoom in/out and reset view
- **Responsive design** - Works on desktop and tablet

## Usage

### Quick Start
1. Open `sankey-editor.html` in any modern browser
2. The editor loads with sample data showing an energy flow diagram
3. Click flows to edit colors/values, drag nodes to reposition

### Adding Flows
- Click the **+ Add Flow** button in the Flows tab
- Or click any node to add a flow from that node
- Or right-click a node for more options

### Editing Flows
- **Click a flow** in the diagram → popup appears with value and color options
- **Edit in table** → modify source, target, value directly in the Flows tab
- **Delete** → click the trash icon in the table or use the popup delete option

### Keyboard Shortcuts
- Flows and nodes can be edited via the sidebar tables
- Use Tab to navigate between input fields

## File Structure

```
sankey-editor.html    # Complete application (single file)
README.md             # This file
screenshot.png        # Screenshot for documentation
```

## Technical Details

### Built With
- Pure HTML, CSS, and JavaScript (no build step required)
- SVG for diagram rendering
- CSS custom properties for theming
- Google Fonts (Inter) and Material Icons

### Browser Support
- Chrome (recommended)
- Firefox
- Safari
- Edge

### Data Format
The JSON export/import format:
```json
{
  "flows": [
    { "source": "Node A", "target": "Node B", "value": 100, "color": "#002EFF" }
  ],
  "nodePositions": {
    "Node A": { "y": 50 }
  },
  "settings": {
    "nodeWidth": 20,
    "nodePadding": 40,
    "width": 900,
    "height": 500,
    "backgroundColor": "#FFFFFF",
    "showDotPattern": false,
    "showFlowValues": false,
    "showNodeValues": true
  }
}
```

## Customization

### Colors
The editor includes a curated color palette. To customize:
1. Find the `sulzerColors` object in the JavaScript
2. Modify or add color categories and values

### Default Data
Edit the `diagramData` object to change the initial diagram shown on load.

### Styling
CSS custom properties at the top of the file control:
- `--color-*` - Color palette
- `--space-*` - Spacing scale
- `--radius-*` - Border radii
- `--shadow-*` - Box shadows

## License

MIT License - feel free to use, modify, and distribute.

## Author

**Vincent Verdet**

## Acknowledgments

- Inspired by [SankeyMatic](https://sankeymatic.com/) and Google Charts Sankey
- Uses [Inter](https://fonts.google.com/specimen/Inter) typeface
- Icons from [Material Icons](https://fonts.google.com/icons)

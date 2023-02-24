## class `QGoodWindow` 

`
class QGoodWindow
  : public QMainWindow
`

**QGoodWindow** class contains the public API's to control the behavior of the customized window.

### Members

#### `public  explicit QGoodWindow(QWidget * parent, const QColor & clear_color)` 

Constructor of *QGoodWindow*.

On Windows creates the native window, turns the `QMainWindow` as a native widget, creates the shadow, initialize default values and calls the `QMainWindow` parent constructor.

On Linux creates the frame less `QMainWindow`, use the shadow only to create resize borders, and the real shadow is draw by current Linux window manager.

On macOS creates a `QMainWindow` with full access to the title bar, and hide native minimize, zoom and close buttons.

#### `public  ~QGoodWindow()` 

Destructor of *QGoodWindow*.

#### `public WId winId() const` 

Returns the window id of the *QGoodWindow*.

#### `public void setWindowFlags(Qt::WindowFlags type)` 

*QGoodWindow* handles flags internally, use this function only when *QGoodWindow* is not enabled.

#### `public Qt::WindowFlags windowFlags() const` 

Returns the window flags of the *QGoodWindow*.

#### `{signal} public void captionButtonStateChanged(const QGoodWindow::CaptionButtonState & state)` 

On handled caption buttons, this SIGNAL report the state of these buttons.

#### `{signal} public void systemThemeChanged()` 

Notify that the system has changed between light and dark mode.

#### `{slot} public void setTitleBarHeight(int height)` 

Call setMargins() but only changes title bar height.

#### `{slot} public void setIconWidth(int width)` 

Call setMargins() but only changes icon width.

#### `{slot} public void setLeftMargin(int width)` 

Call setMargins() but only changes left margin.

#### `{slot} public void setRightMargin(int width)` 

Call setMargins() but only changes right margin.

#### `{slot} public int titleBarHeight() const` 

On Windows, Linux and macOS, returns the actual title bar height, on other OSes returns 0.

#### `{slot} public int iconWidth() const` 

On Windows, Linux and macOS, return the actual icon width, on other OSes returns 0.

#### `{slot} public int leftMargin() const` 

On Windows, Linux and macOS, returns the left margin of the customized title bar, on other OSes returns 0.

#### `{slot} public int rightMargin() const` 

On Windows, Linux and macOS, returns the right margin of the customized title bar, on other OSes returns 0.

#### `{slot} public void setMargins(int title_bar_height, int icon_width, int left, int right)` 

Set the tile bar height, icon width, left and right margins of the customized title bar. Note: Any call to setMargins() clear the left and right masks and the title bar caption buttons masks.

#### `{slot} public void setLeftMask(const QRegion & mask)` 

Set the mask for the left margin of the customized title bar.

#### `{slot} public void setRightMask(const QRegion & mask)` 

Set the mask for the right margin of the customized title bar.

#### `{slot} public void setCenterMask(const QRegion & mask)` 

Set the mask for the center of the customized title bar.

#### `{slot} public void setTitleBarMask(const QRegion & mask)` 

Set the mask for the customized title bar, used in combination with others masks.

#### `{slot} public void setCaptionButtonsHandled(bool handled, const Qt::Corner & corner)` 

Set if the caption buttons should be handled by *QGoodWindow* and on which *corner*, valid only top left and top right corners.

#### `{slot} public void setMinimizeMask(const QRegion & mask)` 

Set the location and shape of handled minimize button, relative to handled corner.

#### `{slot} public void setMaximizeMask(const QRegion & mask)` 

Set the location and shape of handled maximize button, relative to handled corner.

#### `{slot} public void setCloseMask(const QRegion & mask)` 

Set the location and shape of handled close button, relative to handled corner.

#### `{slot} public QRegion leftMask() const` 

Get the mask for the left margin of the customized title bar.

#### `{slot} public QRegion rightMask() const` 

Get the mask for the right margin of the customized title bar.

#### `{slot} public QRegion centerMask() const` 

Get the mask for the center of the customized title bar.

#### `{slot} public QRegion titleBarMask() const` 

Get the mask for the customized title bar.

#### `{slot} public QRegion minimizeMask() const` 

Get the location and shape of handled minimize button, relative to handled corner.

#### `{slot} public QRegion maximizeMask() const` 

Get the location and shape of handled maximize button, relative to handled corner.

#### `{slot} public QRegion closeMask() const` 

Get the location and shape of handled close button, relative to handled corner.

#### `{slot} public QSize leftMaskSize() const` 

Get the size that should be the size of the mask on the left margin of the customized title bar.

#### `{slot} public QSize rightMaskSize() const` 

Get the size that should be the size of the mask on the right margin of the customized title bar.

#### `{slot} public QRect leftCaptionButtonsRect() const` 

If caption buttons are handled on left corner, their buttons masks should be in the bounds of this rect.

#### `{slot} public QRect rightCaptionButtonsRect() const` 

If caption buttons are handled on right corner, their buttons masks should be in the bounds of this rect.

#### `{slot} public void setFixedSize(int w, int h)` 

Set fixed size for *QGoodWindow* to width *w* and height *h*.

#### `{slot} public void setFixedSize(const QSize & size)` 

Set fixed size for *QGoodWindow* to *size*.

#### `{slot} public void setMinimumSize(const QSize & size)` 

Set minimum size for *QGoodWindow* to *size*.

#### `{slot} public void setMaximumSize(const QSize & size)` 

Set maximum size for *QGoodWindow* to *size*.

#### `{slot} public void setMinimumWidth(int w)` 

Set minimum width for *QGoodWindow* to *w*.

#### `{slot} public void setMinimumHeight(int h)` 

Set minimum height for *QGoodWindow* to *h*.

#### `{slot} public void setMaximumWidth(int w)` 

Set maximum width for *QGoodWindow* to *w*.

#### `{slot} public void setMaximumHeight(int h)` 

Set maximum height for *QGoodWindow* to *h*.

#### `{slot} public QSize minimumSize() const` 

Returns the *QGoodWindow* minimum size.

#### `{slot} public QSize maximumSize() const` 

Returns the *QGoodWindow* maximum size.

#### `{slot} public int minimumWidth() const` 

Returns minimum width for *QGoodWindow*

#### `{slot} public int minimumHeight() const` 

Returns minimum height for *QGoodWindow*

#### `{slot} public int maximumWidth() const` 

Returns maximum width for *QGoodWindow*

#### `{slot} public int maximumHeight() const` 

Returns maximum height for *QGoodWindow*

#### `{slot} public QRect normalGeometry() const` 

Returns the geometry for *QGoodWindow* when it's state is no state.

#### `{slot} public QRect frameGeometry() const` 

Returns the geometry for *QGoodWindow* including extended frame and excluding shadow.

#### `{slot} public QRect geometry() const` 

Returns the client area geometry.

#### `{slot} public QRect rect() const` 

Returns the client area size, position is always `QPoint(0, 0)`.

#### `{slot} public QPoint pos() const` 

Position of the window on screen.

#### `{slot} public QSize size() const` 

Size of the window on screen.

#### `{slot} public QSize sizeHint() const` 

Size hint of the window.

#### `{slot} public QSize minimumSizeHint() const` 

Minimum size hint of the window.

#### `{slot} public int x() const` 

X position of the window on screen.

#### `{slot} public int y() const` 

Y position of the window on screen.

#### `{slot} public int width() const` 

Width of the window.

#### `{slot} public int height() const` 

Height of the window.

#### `{slot} public void move(int x, int y)` 

Move the window to *x* - *y* coordinates.

#### `{slot} public void move(const QPoint & pos)` 

Move the window to *pos*.

#### `{slot} public void resize(int width, int height)` 

Resize the window to *width* - *height* size.

#### `{slot} public void resize(const QSize & size)` 

Resize the window to *size*.

#### `{slot} public void setGeometry(int x, int y, int w, int h)` 

Set geometry to pos *x* - *y*, width *w* and height *h*.

#### `{slot} public void setGeometry(const QRect & rect)` 

Set geometry to *rect*.

#### `{slot} public void activateWindow()` 

Activates the *QGoodWindow*.

#### `{slot} public void show()` 

Shows the *QGoodWindow*.

#### `{slot} public void showNormal()` 

Shows or restore the *QGoodWindow*.

#### `{slot} public void showMaximized()` 

Shows or maximize the *QGoodWindow*.

#### `{slot} public void showMinimized()` 

Minimize the *QGoodWindow*.

#### `{slot} public void showFullScreen()` 

Turns the *QGoodWindow* into full screen mode. Including the title bar.

#### `{slot} public void hide()` 

Hide the *QGoodWindow*.

#### `{slot} public void close()` 

Close the *QGoodWindow*.

#### `{slot} public bool isVisible() const` 

Returns if the *QGoodWindow* is visible or not.

#### `{slot} public bool isEnabled() const` 

Returns if the *QGoodWindow* is enabled or not.

#### `{slot} public bool isActiveWindow() const` 

Returns if the *QGoodWindow* is the foreground window or not.

#### `{slot} public bool isMaximized() const` 

Returns if the *QGoodWindow* is maximized or not.

#### `{slot} public bool isMinimized() const` 

Returns if the *QGoodWindow* is minimized or not.

#### `{slot} public bool isFullScreen() const` 

Returns if the *QGoodWindow* is in full screen mode or not.

#### `{slot} public Qt::WindowStates windowState() const` 

Returns the *QGoodWindow* state.

#### `{slot} public void setWindowState(Qt::WindowStates state)` 

Sets the state of the *QGoodWindow* to *state*.

#### `{slot} public QWindow * windowHandle() const` 

Returns the window handle of the *QGoodWindow*.

#### `{slot} public qreal windowOpacity() const` 

Returns the opacity of the *QGoodWindow*.

#### `{slot} public void setWindowOpacity(qreal level)` 

Sets the opacity of the *QGoodWindow* to *level*. Where 0.0 is fully transparent and 1.0 fully opaque.

#### `{slot} public QString windowTitle() const` 

Returns the title of the *QGoodWindow*.

#### `{slot} public void setWindowTitle(const QString & title)` 

Sets the title of the *QGoodWindow* to *title*.

#### `{slot} public QIcon windowIcon() const` 

Returns the icon of the *QGoodWindow*.

#### `{slot} public void setWindowIcon(const QIcon & icon)` 

Sets the icon of the *QGoodWindow* to *icon*.

#### `{slot} public QByteArray saveGeometry() const` 

Returns a copy of the window state to restore it later.

#### `{slot} public bool restoreGeometry(const QByteArray & geometry)` 

Restore window to previous state *geometry*.

#### `enum CaptionButtonState` 

 Values                         | Descriptions                                
--------------------------------|---------------------------------------------
MinimizeHoverEnter            | Minimize button hover enter.
MinimizeHoverLeave            | Minimize button hover leave.
MinimizePress            | Minimize button press.
MinimizeRelease            | Minimize button release.
MinimizeClicked            | Minimize button clicked.
MaximizeHoverEnter            | Maximize or restore button hover enter.
MaximizeHoverLeave            | Maximize or restore button hover leave.
MaximizePress            | Maximize or restore button press.
MaximizeRelease            | Maximize or restore button release.
MaximizeClicked            | Maximize or restore button clicked.
CloseHoverEnter            | Close button hover enter.
CloseHoverLeave            | Close button hover leave.
ClosePress            | Close button press.
CloseRelease            | Close button release.
CloseClicked            | Close button clicked.

Enum that contains caption buttons states when it's states are handled by *QGoodWindow*.

#### `public static void setup()` 

Call this function to setup *QApplication* for *QGoodWindow* usage.

#### `public static bool isSystemThemeDark()` 

Returns if the current system theme is dark or not.

#### `public static bool shouldBordersBeDrawnBySystem()` 

Returns true if system draw borders and false if your app should do it.

#### `public static int execDialog(QDialog * dialog, QGoodWindow * child_gw, QGoodWindow * parent_gw)` 

Show modal frame less *QDialog*, inside window *child_gw*, with parent *parent_gw*.

#### `public static void setAppDarkTheme()` 

Set the app theme to the dark theme.

#### `public static void setAppLightTheme()` 

Set the app theme to the light theme.

#### `public static QGoodStateHolder * qGoodStateHolderInstance()` 

Get the global state holder.

Generated by [Moxygen](https://github.com/sourcey/moxygen)
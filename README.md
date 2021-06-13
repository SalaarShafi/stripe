Check it out here: https://stripe-salaarshafi.netlify.app/

This is a project in which you can hover your cursor on the navbar elements and it will automatically show you the sub elements and the desired links that interests you. When the screen width is less than a certain threshold, a bars icon button is visible on the top right corner of the screen which you can click to see the same elements mentioned above without causing clutter on a small screen.

The navbar elements have on them the onMouseOver attribute which when the cursor hovers over them, run the openSubmenu function and passes in the text content of these elements to the function. Also using getBoundingRect function the coordinates for where to display the submenu are also ascertained and then passed in to the openSubmenu function. It also sets the isSubmenuOpen state to true. The openSubmenu function is brought into the navbar elements file using useContext from the context file. The isSubmenuOpen state is set to true and the location state is passed in to the submenu function file using useContext and it uses a ternary operator to determine whether the isSubmenuOpen state is true or not. If so it returns the required class in the className attribute of the jsx component which shows the submenu component. This submenu component uses the page state and obtains the sublinks so that they can be displayed, and does just that.

But the location of each submenu for each navbar element is set by using the location state and setting the inline styling of the submenu components to the obtained positions by using useRef on the submenu.

Whenever the mouse goes over the hero element the isSubmenuOpen state is set to false not showing the submenu anymore. On the nav element it first checks if the classlist does not contain the 'link-btn' class and then it's onMouseOver attribute also runs a function which stops displaying the submenu.

The sidebar functionality has already been previously described in the sidebar-modal project so you can refer to that description.

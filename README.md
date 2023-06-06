## HTML STRUCTURE
A parent DIV is created that holds a child DIV which holds all images, and two sibling BUTTONS for navigation. The BUTTONS are absolutely positioned within the parent DIV uusing CSS.

## SCRIPT
This is where the magic happens.
First, all images with class 'slide' is gotten. This helps to get the total number of images on which the slide effect will be applied.
Next, we loop over every image, setting the translation on the X-axis using the translateX() CSS function. The slideIndex variable is multiplied by 100% to determine the amount of translation.
Next, we create a previoseSlide function which checks if the index of the current image is greater than zero, indicating that it is not the first image. If true, the slideIndex var is decremented, moving it to the previous slide. If the check is false, it means that the current slide is the first slide. In this case, it sets the slideIndex to the index of the last slide, looping back to the last slide.
Next, a nextSlide function is created which effectivelu does the opposite of the previoseSlide function. A check if done to ensure that the current slide is greater than the total unmber of slides. This ensures that the current slide is not the last slide in the slider. If this is false, it means the current slide is the last. In this case, it sets the slideIndex to 0, looping back to the first slide.
At the end of both previousSlide and nextSlide, the showSlide function is called to display the updated slide based on the new slideIndex
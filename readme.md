# Grocery Store Inventory Project

- [Grocery Store Inventory Project](#grocery-store-inventory-project)
  - [Scraping notes](#scraping-notes)
  - [YOLO fine-tuning](#yolo-fine-tuning)
    - [Using openCV image tools](#using-opencv-image-tools)
    - [Using synthetic data creation](#using-synthetic-data-creation)

## Scraping notes

- Check each site's robots.txt file, and sitemap if possible
  - Loblaws:
    - [robots.txt](https://www.loblaws.ca/robots.txt)
    - [sitemap](https://www.loblaws.ca/sitemap.xml)
  
## YOLO fine-tuning

### Using openCV image tools

- Try using OpenCV to (slowly) "find" cereal boxes within videos, extract bounding boxes, and auto-tuning YOLOv8 based on this.  Methods include:
  - ORB
  - SIFT
  - SURF
- ORB is preferred for this class, since it is open-source.  Example videos:
  - [Feature Matching (Brute-Force)](https://www.youtube.com/watch?v=NhuE9P5gDJg)
    - Includes code
  - [ORB Real Time Best Choice Detector](https://www.youtube.com/watch?v=NhuE9P5gDJg)
    - No description, but shows good results
  
### Using synthetic data creation

- Use video frames and create a process to overlay target images.  May need some warping transformations etc., or some other techniques to put them in "realistic" places
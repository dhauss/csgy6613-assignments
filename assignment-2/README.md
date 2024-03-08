# Assignment 2: Video Search

Date of submission: 3/8/2024

## Instructions on how to run the code:

This code will most easily be run in Google Colab. I've included a requirements.txt file to run it locally, but to run in Colab I included all necessary library installations and dependencies in the first two cells. If running locally, be aware that some functionality is Colab specific: there is a patch for cv2.imshow() as well as matlib's Rectangle function. To use these locally simply replace the patches with the original functions, but be sure to add a string for imshow()'s first argument (the patch does not accept a title argument). I also use Colab's secrets storage, if running locally, these will have to be replaced with the secrets for a local pgvector DB. Lastly, I use Colab functions to mount the Notebook to my drive and download the trained autoencoder models, but these lines of code can simply be commented out when running locally as long as the file paths are corrected.

As far as file structure, I wrote all code in a single notebook (assignment_2.pynb) assuming that would make grading a bit simpler. Let me know if that assumption isn't true and I'll make A3 cleaner/more modular. You'll also find the requirements.txt file, this README, and two separate autoencoder models.

The autoencoder model that I used in the assignment_2 notebook is "autoencoder_model.keras". I also included autoencoder_model_full_mscoco.keras, which was trained on the full MS COCO dataset in the hopes of creating a model with greater bias, but ultimately did not perform as well as the autoencoder_model.keras model, which was trained on cropped object images of classes that had been detected in the first stage of this assignment. Testing with both models led me to believe my autoencoder model requires a higher level of complexity to improve its performance with images found on the internet

## Supabase Postgres DB

As I was running my code in Colab, I opted to use a Supabase Postgres DB with pgvector functionality. I interact with the Supabase client through psycopg instead of Supabase's custom API, so that the code should run as expected by simply updating the DB secrets for any Postgres instance (local or external) as long as it is compatible with pgvector.


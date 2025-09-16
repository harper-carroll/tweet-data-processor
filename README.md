# Tweet Processing for Fine-Tuning

To process your own tweets and create a training and validation set, please follow these steps:

1. **Add your tweets:**
   Place your `tweets.js` file in this directory. You can obtain this file by requesting your Twitter/X archive (Settings > search "archive").

2. **Process your tweets:**
   Run the `process_tweets.py` script. This script will read the `tweets.js` file and create `data.jsonl`.

   When you run the script, you will be prompted to enter your name or identifier (for example, `Harper Carroll AI`). This will be used in the prompt, e.g., `Write a tweet in the style of Harper Carroll AI`.

   ```bash
   python process_tweets.py
   ```

   or

   ```bash
   python3 process_tweets.py
   ```

3. **Split the dataset:**
   Run the `split_dataset.py` script. This will take the `data.jsonl` file and split it into `train.jsonl` and `val.jsonl` files, which can be used for model training.

   ```bash
   python split_dataset.py
   ```

   or

   ```bash
   python3 split_dataset.py
   ```

After following these steps, you will have your own `train.jsonl` and `val.jsonl` files ready for use.

4. **Analyze tweet lengths (optional):**
   The `analyze_tweet_lengths.py` script can be used to help you get a distribution of your tweet lengths. This can be useful for setting a `max_length` value for some fine-tuning jobs.

   ```bash
   python analyze_tweet_lengths.py
   ```

   or

   ```bash
   python3 analyze_tweet_lengths.py
   ```

   Note: This is not required for all fine-tuning services. For example, Nebius handles this for you.

5. **Fine-tune your model!**
[Go to the Nebius AI Studio](https://nebius.com/services/studio-inference-service?utm_medium=cpc&utm_source=yoloco&utm_campaign=harpercarrollai) (who sponsored this content) and watch the [Reel](https://www.instagram.com/p/DLXm1YIRts9/) for instructions! Let me know if you have any questions!

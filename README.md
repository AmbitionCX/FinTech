
# Fudan University Fintech and Data Intelligence Laboratory
- 复旦大学金融科技与数据智能实验室

### Instructions with Docker
1. Install Docker on your computer.
2. Run `./.docker/run.sh`.
3. Wait for Docker to build a sandbox with all the languages and packages the template needs. Should take ~2 min the first time and be almost instant on subsequent runs.
4. Wait for Docker to start the preview. You should shortly get a `localhost` link that you can open in your browser to see your site preview.
5. When you make a change to a file in your repo folder, your preview should refresh/update automatically, except for changes to `_config.yaml` which require you to manually refresh.
6. When you make a change to your sources or metasources, the cite process should automatically re-run, and when finished be reflected in your preview via the same behavior as above.
### Non-Docker instructions
- Build site:
  1. Install Ruby v3.3.4 (Recommand using [rvm](https://github.com/rvm/rvm)).
  2. Install Bundler by running `gem install bundler`.
  3. Install needed Ruby packages by running `bundle install`.
  4. Re-run the previous command if you ever add new plugins.
  5. Start the site by running bundle exec `jekyll serve --open-url --livereload --trace`.
  6. Re-run the previous command if you make changes to _config.yaml.

- Run cite process:
  1. Install Python 3 (with PIP).
  2. Install virtual environment for Python `pip install virtualenv`.
  3. Create and enter the virtual environment `virtualenv fintech && source fintech/bin/activate`.
  4. Install needed Python packages by running `python -m pip install --upgrade --requirement ./_cite/requirements.txt`.
  5. Generate citations by running `python ./_cite/cite.py`.
  6. Re-run the previous command when you make changes to your input sources and metasources.

  ![on-push](../../actions/workflows/on-push.yaml/badge.svg)
  ![on-pull-request](../../actions/workflows/on-pull-request.yaml/badge.svg)
  ![on-schedule](../../actions/workflows/on-schedule.yaml/badge.svg)

  Visit **[fintech.fduvis.net](https://fintech.fduvis.net)** 🚀

  _Built with [Lab Website Template](https://greene-lab.gitbook.io/lab-website-template-docs)_

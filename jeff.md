notes to myself

this is primarily used to give me a simplified rails ruby environment for rever
there is so much going on in the at codebase, so I want something to compare it to.

steps to get running
keep as few dependencies as possible

ensure you can connect to database with expected credentials
PGPASSWORD=password psql --host=db --username=postgres --port=5432

bin/rake db:drop db:create

# to startup rails
bin/rails s -b 0.0.0.0


look in test/README.md for how to dump the database
to connect
docker exec -it sustainable-rails-docker-db-1 bash
psql -U postgres

bin/rake db:create

psql -U postgres -h db rever_development < rever_development-mdb-2023-01-16.sql

unzip suppport/geolite2-City.mmdb
move to /

rails s -b 0.0.0.0

bin/rake db:migrate

npm install

su rever
./node_modules/bower/bin/bower install


TRY
precompile assets
bundle exec rake assets:precompile
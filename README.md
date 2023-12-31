  <h1>Invitation API Documentation</h1>

 <h2>Setup project</h2>

<ul>
  <li>git clone https://github.com/hels-wrk/invitation-rest-api-test-project.git</li>
  <li>cd invitation-rest-api-test-project</li>
  <li>docker-compose build</li>
  <li>docker-compose up -d</li>
  <li>docker-compose exec php composer install</li>
  <li>docker-compose exec php bin/console doctrine:migrations:migrate</li>
  <li>docker-compose exec php ./vendor/bin/phpunit</li>
</ul>


  <h2>Sending an Invitation</h2>

  <p><strong>Endpoint:</strong></p>
  <pre><code>POST /send-invitation</code></pre>

  <p><strong>Request Body:</strong></p>
  <pre><code>{
  "sender": "user1",
  "invited": "user2"
}</code></pre>

  <h2>Canceling an Invitation</h2>

  <p><strong>Endpoint:</strong></p>
  <pre><code>POST /cancel-invitation/{id}</code></pre>

  <h2>Accepting an Invitation</h2>

  <p><strong>Endpoint:</strong></p>
  <pre><code>POST /accept-invitation/{id}</code></pre>

  <h2>Declining an Invitation</h2>

  <p><strong>Endpoint:</strong></p>
  <pre><code>POST /decline-invitation/{id}</code></pre>

  <p>These endpoints allow you to perform various actions related to invitations, including sending, canceling, accepting, and declining them. Replace <code>{id}</code> in the endpoints with the actual ID of the invitation you want to target.</p>

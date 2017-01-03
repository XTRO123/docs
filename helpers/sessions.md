The session is a static class, this means it can be used in any controller without needing to be instantiated, the class has an init method if session_start() has not been set then it starts it. This call is in place in (Core/Config.php) so it can already be used with no setup required.

The advantages of using a session class is all sessions are prefixed using the constant setup in the root index.php file, this avoid sessions clashing with other applications on the same domain.

<b>Usage</b>

Setting a session, call Session then ::set pass in the session name followed by its value

```php
\Helpers\Session::set('username', 'Dave');
```

To retrieve an existing session use the get method:

```php
\Helpers\Session::get('username');
```

Pull an existing session key and remove it, use the pull method:

```php
\Helpers\Session::pull('username');
```

use id to return the session id:

```php
\Helpers\Session::id();
```

Destroy a session key  by calling:

```php
\Helpers\Session::destroy('mykey');
```

To look inside the sessions array, call the display method:

```php
print_r(\Helpers\Session::display());
```

# ctrl_cmd_save

ctrl(Windows) or Cmd(Mac) + s 이벤트

```javascript
   useEffect(() => {
    const saveEvent = e => {
      if ((window.navigator.platform.match('Mac') ? e.metaKey : e.ctrlKey) && e.keyCode === 83) {
        e.preventDefault();
        // onSubmit();
      }
    };
    document.addEventListener('keydown', saveEvent, false);
    return () => {
      document.removeEventListener('keydown', saveEvent);
    };
  }, [data, onSubmit]);
```

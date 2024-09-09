Toast Notification System
This project implements a toast notification system using custom toast.css and toast.js files. It allows you to display error and success messages through a clean and user-friendly toast notification UI.
    
    <link rel="stylesheet" href="https://ankitnishad6313.github.io/toast-notification/toast.css" />
    <script src="https://ankitnishad6313.github.io/toast-notification/toast.js"></script>

    
    @if ($errors->any())
        @foreach ($errors->all() as $error)
            <script>
                triggerAlert('{{ $error }}', 'error')
            </script>
        @endforeach
    @endif
    @if (session('success'))
        <script>
            triggerAlert("{{ session('success') }}", 'success')
        </script>
    @endif

    @if (session('error'))
        <script>
            triggerAlert("{{ session('error') }}", 'error')
        </script>
    @endif

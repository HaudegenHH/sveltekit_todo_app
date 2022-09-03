<script>
    import TodoItem from "../lib/todo-item.svelte";

    const title = "Todos"
</script>

<style>
    .todos {
        width: 100%;
        max-width: 40rem;
        margin: 4rem auto 0 auto;
    }

    .new-todo-form {
        margin: 0 0 0.5rem 0;
    }

    .new-todo-form input {
        font-size: 28px;
        width: 100%;
        padding: 0.5em 1em 0.3em 1em;
        box-sizing: border-box;
        border-radius: 8px;
        text-align: center;
        background-color: rgba(255, 255, 255, 0.05);        
    }

    .todos :global(input) {
        border: 1px solid transparent;
    }
    .todos :global(input:focus-visible) {
        box-shadow: inset 1px 1px 6px rgba(0, 0, 0, 0.1);
        border: 1px solid #ff3e00 !important;
        outline: none;
    }



</style>

<svelte:head>
    <title>{title}</title>
</svelte:head>

<div class="todos">
    <h1>{title}</h1>

    <form action="" method="" class="new-todo-form">
        <input type="text" name="text" aria-label="add a todo" placeholder="+ Type to add a Todo">
    </form>
    
    <TodoItem />    
</div>

    

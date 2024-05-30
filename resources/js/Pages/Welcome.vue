<script setup>
import { Link } from "@inertiajs/vue3";

defineProps({
    data: Object,
});
</script>

<template>
    <div class="flex flex-col gap-4">
        <Link :href="`${route('profile.issue')}?case=1`" :only="['data']">
            Case 1
        </Link>
        <Link :href="`${route('profile.issue')}?case=2`" :only="['data']">
            Case 2
        </Link>
        <Link :href="`${route('profile.issue')}?case=3`" :only="['data']">
            Case 3
        </Link>
        <Link :href="`${route('profile.issue')}?case=4`" :only="['data']">
            Case 4
        </Link>
    </div>

    <div>
        <div>From props</div>
        <pre>{{ data }}</pre>
    </div>
    <div>
        <div>From global</div>
        <pre>{{ $page.props.data }}</pre>
    </div>
</template>

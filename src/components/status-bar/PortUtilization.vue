<template>
    <div>
        <span class="message">{{ $t("statusbar_port_utilization") }}</span>
        <ReadingStat message="statusbar_usage_download" :value="usageDown" unit="%" />
        <ReadingStat message="statusbar_usage_upload" :value="usageUp" unit="%" />
    </div>
</template>

<script>
import ReadingStat from "./ReadingStat.vue";

export default {
    components: {
        ReadingStat,
    },
    props: {
        usageDown: {
            type: Number,
            default: 0,
        },
        usageUp: {
            type: Number,
            default: 0,
        },
    },
};
</script>

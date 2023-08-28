<script setup lang="ts">
import type { TabsPaneContext } from 'element-plus'
defineOptions({
  name: 'IndexPage',
})
const name = ref('')

const router = useRouter()
const activeName = ref('first')
const handleClick = (tab: TabsPaneContext, event: Event) => {
  console.log(tab, event)
}

</script>
<style scpoed>
.avatar-name {
  width: calc(100% -150px)
}

.demo-tabs{
  .el-tabs__nav-scroll{
    width: 50%;
    margin: 0 auto;
  }
}
</style>
<template>
  <header>
    <div w-full flex px-5 max-w-screen-lg mx-auto h-full m="y-10" >
    <div>
      <img w-150px h-150px rounded-50 src="../assest/image/avatar.jpeg" alt="" srcset="">
    </div>
    <div ml-10 flex-1>
      <div flex flex-justify-between flex-items-center>
        <h1 text-10 font-bold>Kingyp1</h1>
        <div ml-0 sm:ml-8 space-x-3 sm:space-x-4 flex items-center sm:static absolute right-0>
          <!-- <div>
            <button i-carbon:sight></button>
          </div>
          <div>
            <button i-ic:baseline-search></button>
          </div>
          <button btn flex>
            <span i-carbon:user-follow></span>
            <span ml-2>关注</span>
          </button> -->
          <span mr-10 color="#9E9E9E">艳平 Kingyp1</span>
          <TheFooter/>
        </div>
      </div>
      <div mt text-left>
        <span>YANPING</span>
      </div>
      <div mt text-left>
        <a i-carbon-logo-github icon-btn rel="noreferrer" href="https://github.com/kingyp1" target="_blank"
          title="GitHub" />
      </div>
    </div>
  </div>
  </header>
  <div>
    <el-tabs v-model="activeName" class="demo-tabs" @tab-click="handleClick">
    <el-tab-pane label="主页" name="first">
      <First />
    </el-tab-pane>
    <!-- <el-tab-pane label="归档" name="second">
      <second />
    </el-tab-pane>
    <el-tab-pane label="Links" name="third">Role</el-tab-pane>
    <el-tab-pane label="Sponsors" name="fourth">Task</el-tab-pane> -->
  </el-tabs>
  </div>
</template>

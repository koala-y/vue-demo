<style scoped>
  .layout{
    border: 1px solid #d7dde4;
    background: #f5f7f9;
    position: relative;
    border-radius: 4px;
    overflow: hidden;
  }
  .layout-logo{
    width: 100px;
    height: 30px;
    background: #5b6270;
    border-radius: 3px;
    float: left;
    position: relative;
    top: 15px;
    left: 20px;
  }
  .layout-nav{
    width: 420px;
    margin: 0 auto;
    margin-right: 20px;
  }
</style>
<template>
  <div>
    <div>
      <Dropdown>
        <a href="javascript:void(0)">
          下拉菜单
          <Icon type="ios-arrow-down"></Icon>
        </a>
        <DropdownMenu slot="list">
          <DropdownItem>驴打滚</DropdownItem>
          <DropdownItem>炸酱面</DropdownItem>
          <DropdownItem disabled>豆汁儿</DropdownItem>
          <DropdownItem>冰糖葫芦</DropdownItem>
          <DropdownItem divided>北京烤鸭</DropdownItem>
        </DropdownMenu>
      </Dropdown>
      <Dropdown style="margin-left: 20px">
        <Button type="primary">
          下拉菜单
          <Icon type="ios-arrow-down"></Icon>
        </Button>
        <DropdownMenu slot="list">
          <DropdownItem>驴打滚</DropdownItem>
          <DropdownItem>炸酱面</DropdownItem>
          <DropdownItem disabled>豆汁儿</DropdownItem>
          <DropdownItem>冰糖葫芦</DropdownItem>
          <DropdownItem divided>北京烤鸭</DropdownItem>
        </DropdownMenu>
      </Dropdown>
    </div>
    <div class="layout">
      <Alert>An info prompt</Alert>
      <Alert type="success">A success prompt</Alert>
      <Alert type="warning">A warning prompt</Alert>
      <Alert type="error">An error prompt</Alert>
      <Layout>
        <Header>
          <Menu mode="horizontal" theme="dark" active-name="1">
            <div class="layout-logo"></div>
            <div class="layout-nav">
              <MenuItem name="1">
                <Icon type="ios-navigate"></Icon>
                Item 1
              </MenuItem>
              <MenuItem name="2">
                <Icon type="ios-keypad"></Icon>
                Item 2
              </MenuItem>
              <MenuItem name="3">
                <Icon type="ios-analytics"></Icon>
                Item 3
              </MenuItem>
              <MenuItem name="4">
                <Icon type="ios-paper"></Icon>
                Item 4
              </MenuItem>
            </div>
          </Menu>
        </Header>
        <Layout>
          <Sider hide-trigger :style="{background: '#fff'}">
            <Menu active-name="1-2" theme="light" width="auto" :open-names="['1']">
              <Submenu name="1">
                <template slot="title">
                  <Icon type="ios-navigate"></Icon>
                  Item 1
                </template>
                <MenuItem name="1-1">Option 1</MenuItem>
                <MenuItem name="1-2">Option 2</MenuItem>
                <MenuItem name="1-3">Option 3</MenuItem>
              </Submenu>
              <Submenu name="2">
                <template slot="title">
                  <Icon type="ios-keypad"></Icon>
                  Item 2
                </template>
                <MenuItem name="2-1">Option 1</MenuItem>
                <MenuItem name="2-2">Option 2</MenuItem>
              </Submenu>
              <Submenu name="3">
                <template slot="title">
                  <Icon type="ios-analytics"></Icon>
                  Item 3
                </template>
                <MenuItem name="3-1">Option 1</MenuItem>
                <MenuItem name="3-2">Option 2</MenuItem>
              </Submenu>
            </Menu>
          </Sider>
          <Layout :style="{padding: '0 24px 24px'}">
            <Breadcrumb :style="{margin: '24px 0'}">
              <BreadcrumbItem>Home</BreadcrumbItem>
              <BreadcrumbItem>Components</BreadcrumbItem>
              <BreadcrumbItem>Layout</BreadcrumbItem>
            </Breadcrumb>
            <Content :style="{padding: '24px', minHeight: '280px', background: '#fff'}">
              Content
            </Content>
          </Layout>
        </Layout>
      </Layout>
    </div>
    <div>
      <Row>
        <Col span="12">
          <DatePicker type="date" placeholder="Select date" style="width: 200px"></DatePicker>
        </Col>
      </Row>
    </div>
  </div>
</template>

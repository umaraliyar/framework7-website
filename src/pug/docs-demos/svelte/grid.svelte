<App>
  <View main>
    <Page class="grid-demo">
      <Navbar title="Grid / Layout"></Navbar>
      <Block>
        <p>Columns within a row are automatically set to have equal width. Otherwise you can define your column with pourcentage of screen you want.</p>
      </Block>
      <BlockTitle>Columns with gap</BlockTitle>
      <Block>
        <Row>
          <Col>50% (.col)</Col>
          <Col>50% (.col)</Col>
        </Row>
        <Row>
          <Col>25% (.col)</Col>
          <Col>25% (.col)</Col>
          <Col>25% (.col)</Col>
          <Col>25% (.col)</Col>
        </Row>
        <Row>
          <Col>33% (.col)</Col>
          <Col>33% (.col)</Col>
          <Col>33% (.col)</Col>
        </Row>
        <Row>
          <Col>20% (.col)</Col>
          <Col>20% (.col)</Col>
          <Col>20% (.col)</Col>
          <Col>20% (.col)</Col>
          <Col>20% (.col)</Col>
        </Row>
        <Row>
          <Col width="33">33% (.col-33)</Col>
          <Col width="66">66% (.col-66)</Col>
        </Row>
        <Row>
          <Col width="25">25% (.col-25)</Col>
          <Col width="25">25% (.col-25)</Col>
          <Col width="50">50% (.col-50)</Col>
        </Row>
        <Row>
          <Col width="75">75% (.col-75)</Col>
          <Col width="25">25% (.col-25)</Col>
        </Row>
        <Row>
          <Col width="80">80% (.col-80)</Col>
          <Col width="20">20% (.col-20)</Col>
        </Row>
      </Block>
      <BlockTitle>No gap between columns</BlockTitle>
      <Block>
        <Row noGap>
          <Col>50% (.col)</Col>
          <Col>50% (.col)</Col>
        </Row>
        <Row noGap>
          <Col>25% (.col)</Col>
          <Col>25% (.col)</Col>
          <Col>25% (.col)</Col>
          <Col>25% (.col)</Col>
        </Row>
        <Row noGap>
          <Col>33% (.col)</Col>
          <Col>33% (.col)</Col>
          <Col>33% (.col)</Col>
        </Row>
        <Row noGap>
          <Col>20% (.col)</Col>
          <Col>20% (.col)</Col>
          <Col>20% (.col)</Col>
          <Col>20% (.col)</Col>
          <Col>20% (.col)</Col>
        </Row>
        <Row noGap>
          <Col width="33">33% (.col-33)</Col>
          <Col width="66">66% (.col-66)</Col>
        </Row>
        <Row noGap>
          <Col width="25">25% (.col-25)</Col>
          <Col width="25">25% (.col-25)</Col>
          <Col width="50">50% (.col-50)</Col>
        </Row>
        <Row noGap>
          <Col width="75">75% (.col-75)</Col>
          <Col width="25">25% (.col-25)</Col>
        </Row>
        <Row noGap>
          <Col width="80">80% (.col-80)</Col>
          <Col width="20">20% (.col-20)</Col>
        </Row>
      </Block>

      <BlockTitle>Nested</BlockTitle>
      <Block>
        <Row>
          <Col>50% (.col)
            <Row>
              <Col>50% (.col)</Col>
              <Col>50% (.col)</Col>
            </Row>
          </Col>
          <Col>50% (.col)
            <Row>
              <Col width="33">33% (.col-33)</Col>
              <Col width="66">66% (.col-66)</Col>
            </Row>
          </Col>
        </Row>
      </Block>

      <BlockTitle>Responsive Grid</BlockTitle>
      <Block>
        <p>Grid cells have different size on Phone/Tablet</p>
        <Row>
          <Col width="100" medium="50">.col-100.tablet-50</Col>
          <Col width="100" medium="50">.col-100.tablet-50</Col>
        </Row>
        <Row>
          <Col width="50" medium="25">.col-50.tablet-25</Col>
          <Col width="50" medium="25">.col-50.tablet-25</Col>
          <Col width="50" medium="25">.col-50.tablet-25</Col>
          <Col width="50" medium="25">.col-50.tablet-25</Col>
        </Row>
        <Row>
          <Col width="100" medium="40">.col-100.tablet-40</Col>
          <Col width="50" medium="60">.col-50.tablet-60</Col>
          <Col width="50" medium="66">.col-50.tablet-66</Col>
          <Col width="100" medium="33">.col-100.tablet-33</Col>
        </Row>
      </Block>

      <BlockTitle>Resizable Cols</BlockTitle>
      <Block class="grid-resizable-demo">
        <Row>
          <Col resizable style="min-width: 20px">1</Col>
          <Col resizable style="min-width: 20px">2</Col>
          <Col resizable style="min-width: 20px">3</Col>
        </Row>
      </Block>

      <BlockTitle>Resizable Fixed Col</BlockTitle>
      <BlockHeader>2nd column has fixed size</BlockHeader>
      <Block class="grid-resizable-demo">
        <Row>
          <Col resizable style="min-width: 20px">1</Col>
          <Col resizable resizableFixed style="min-width: 20px">2</Col>
          <Col resizable style="min-width: 20px">3</Col>
        </Row>
      </Block>

      <BlockTitle>Resizable Grid</BlockTitle>
      <Block class="grid-resizable-demo">
        <Row class="align-items-stretch" style="height: 300px">
          <Col resizable class="demo-col-center-content" style="min-width: 50px">Left</Col>
          <Col resizable class="display-flex flex-direction-column" style="padding: 0px; border: none; min-width: 50px; background-color: transparent">
            <Row resizable style="height: 50%; min-height: 50px">
              <Col class="demo-col-center-content" style="height: 100%">Center Top</Col>
            </Row>
            <Row resizable style="height: 50%; min-height: 50px">
              <Col class="demo-col-center-content" style="height: 100%">Center Bottom</Col>
            </Row>
          </Col>
          <Col resizable class="demo-col-center-content" style="min-width: 50px">Right</Col>
        </Row>
      </Block>
    </Page>
  </View>
</App>
<style>
  :global(.grid-demo div[class*="col"]) {
    background: #fff;
    text-align: center;
    color: #000;
    border: 1px solid #ddd;
    padding: 5px;
    margin-bottom: 15px;
    font-size: 12px;
  }
  :global(.grid-resizable-demo) {
    --f7-grid-row-gap: 16px;
  }
  :global(.grid-resizable-demo div[class*="col"]) {
    margin-bottom: 0;
  }
  :global(.grid-resizable-demo .demo-col-center-content) {
    display: flex;
    align-items: center;
    justify-content: center;
  }
</style>
<script>
  import {App, View, Page, Navbar, Block, BlockTitle, Row, Col, BlockHeader} from 'framework7-svelte';
</script>

<script lang="ts">
    import 'bootstrap/dist/css/bootstrap.min.css';
    import {
        Button, 
        Modal,
        ModalBody,
        ModalFooter,
        ModalHeader,
        Container,
        Row,
        Col,
        Image,
        Figure,
        Input,
        InputGroup,
        InputGroupText
    } from 'sveltestrap';
    let open = false;
    const togglelogin = () => (open= !open) ;
</script>

<style>
    :global(body){
        background-color: #949494;
    }
    img{
        width: 30%;
        height: 30%;
    }
    figure.logo{
        display: block;
        margin-left: auto;
        margin-right: auto;
        width: 50%;
        text-align: center;
    }
    .logo_title{
        display: block;
        font-family: Krungthep;
        font-size: 72px;
    }

</style>

<div class="Login_btn">
<Container fluid>
    <Row>
        <Col class="text-end">
        <Button color="warning" on:click={togglelogin}>Login</Button> 
        <Modal isOpen={open} backdrop={false} {togglelogin}>
            <ModalHeader {togglelogin}>Login</ModalHeader>
            <ModalBody>Insert Input Field</ModalBody>
            <ModalFooter>
                <Button color="warning" on:click={togglelogin}>Submit</Button>
                <Button color="secondary" on:click={togglelogin}>Cancel</Button>
            </ModalFooter>
        </Modal>
    </Col>
    </Row>
</Container>
</div>

<div class="logo">
<Container>
    <Row>
        <Col class="text-center">
            <figure class="logo">
                <img src="/pngwin-modified.png" alt="pngwin logo">
                <figcaption class="logo_title">PNG.WIN</figcaption>
            </figure>
        </Col>
    </Row>
</Container>
</div>
<div class="searchbar">
    <Container>
        <Row>
                <div class="col-9 mx-auto my-2 text-center">
                    <InputGroup>
                    <Input placeholder="Search"></Input>
                </InputGroup>
                </div>
        </Row>
    </Container>
</div>
<div class="buttons">
<Container>
    <Row>
        <div class="gap-5 col-6 mx-auto text-center">
            <Button color="warning">Home</Button>
            <Button color="warning" >Collections</Button>
            <Button color="warning">Random</Button>
        </div>
    </Row>
</Container>

<Container>
    <Row>
        <div class="gap-5 col-6 mx-auto my-2 text-center">
            <Button color="warning">Help</Button>
            <Button color="warning" >Settings</Button>
        </div>
    </Row>
</Container>
</div>

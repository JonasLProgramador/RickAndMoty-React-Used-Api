<!DOCTYPE html>
<body>
    <div class="container">
        <h1>RickAndMorty-React-Used-Api</h1>
        <img src="https://github.com/JonasLProgramador/RickAndMoty-React-Used-Api/assets/172916273/4cf8032e-06dd-4957-abae-524017c763d9">
        <p>Este projeto consiste em uma aplicação React que consome a API do <a href="https://rickandmortyapi.com/" target="_blank">Rick and Morty</a>, exibindo informações sobre personagens em forma de cards na tela. O principal objetivo é consolidar o conhecimento em React, incluindo o uso de hooks, manipulação de estados e integração com APIs externas.</p>
        <h2>Sumário</h2>
        <ul>
            <li><a href="#visao-geral">Visão Geral</a></li>
            <li><a href="#estrutura-do-projeto">Estrutura do Projeto</a></li>
            <li><a href="#componentes-principais">Componentes Principais</a></li>
            <li><a href="#execucao-do-projeto">Execução do Projeto</a></li>
            <li><a href="#dependencias">Dependências</a></li>
            <li><a href="#licenca">Licença</a></li>
        </ul>
        <h2 id="visao-geral">Visão Geral</h2>
        <p>A aplicação permite que o usuário clique em um botão para buscar informações de personagens aleatórios da série "Rick and Morty". Esses personagens são então exibidos em forma de cards. Há também a possibilidade de apagar os personagens exibidos através de um botão específico.</p>
        <h2 id="estrutura-do-projeto">Estrutura do Projeto</h2>
        <p>A estrutura principal do projeto é organizada da seguinte forma:</p>
        <pre><code>
/
│
├── /public
│   └── index.html
│
├── /src
│   ├── /components
│   │   ├── Button.jsx
│   │   ├── Card.jsx
│   │   └── Button.css
│   │   └── Card.css
│   │
│   ├── App.jsx
│   ├── index.js
│   ├── index.css
│   └── App.css
│
└── package.json
        </code></pre>
        <h2 id="componentes-principais">Componentes Principais</h2>
        <h3 id="card">Card</h3>
        <p>O componente <code>Card</code> é responsável por exibir as informações de cada personagem, como nome, status, espécie, gênero e imagem.</p>
        <pre><code>
import { oneOfType } from 'prop-types'
import PropTypes from 'prop-types'
import './Card.css'

export const Card = ({ id, name, status, species, gender, image }) => {
    return (
        &lt;ul className='lista'&gt;
            &lt;li className='item'&gt;
                &lt;div key={id} className="card"&gt;
                    &lt;h1&gt;{name}&lt;/h1&gt;
                    &lt;p&gt;Status: {status}&lt;/p&gt;
                    &lt;p&gt;Espécie: {species}&lt;/p&gt;
                    &lt;p&gt;Gênero: {gender}&lt;/p&gt;
                    &lt;img src={image} className="img" alt={name} /&gt;
                &lt;/div&gt;
            &lt;/li&gt;
        &lt;/ul&gt;
    )
}
Card.propTypes = {
    id: oneOfType([PropTypes.string, PropTypes.number]).isRequired,
    name: PropTypes.string.isRequired,
    status: PropTypes.string.isRequired,
    species: PropTypes.string.isRequired,
    gender: PropTypes.string.isRequired,
    image: PropTypes.string.isRequired
}
        </code></pre>
        <h3 id="button">Button</h3>
        <p>O componente <code>Button</code> é um botão genérico que dispara funções específicas ao ser clicado, como buscar novos personagens ou apagar os existentes.</p>
        <p><strong>Nota:</strong> O código do componente <code>Button</code> não foi fornecido, mas pode ser semelhante ao seguinte:</p>
        <pre><code>
import PropTypes from 'prop-types';
import './Button.css';

const Button = ({ handleFunction, title, color }) => {
    return (
        &lt;button 
            onClick={handleFunction} 
            className={`button ${color}`}&gt;
            {title}
        &lt;/button&gt;
    );
}
Button.propTypes = {
    handleFunction: PropTypes.func.isRequired,
    title: PropTypes.string.isRequired,
    color: PropTypes.string.isRequired
}
export default Button;
        </code></pre>
        <h2 id="execucao-do-projeto">Execução do Projeto</h2>
        <p>Para executar o projeto localmente, siga as etapas abaixo:</p>
        <ol>
            <li>Clone este repositório:</li>
            <pre><code>git clone https://github.com/seu-usuario/RickAndMorty-React-Used-Api.git</code></pre>
            <li>Navegue até o diretório do projeto:</li>
            <pre><code>cd RickAndMorty-React-Used-Api</code></pre>
            <li>Instale as dependências:</li>
            <pre><code>npm install</code></pre>
            <li>Inicie a aplicação:</li>
            <pre><code>npm start</code></pre>
        </ol>
        <p>A aplicação estará disponível em <code>http://localhost:3000</code>.</p>
        <h2 id="dependencias">Dependências</h2>
        <p>As principais dependências deste projeto são:</p>
        <ul>
            <li><a href="https://reactjs.org/" target="_blank">React</a></li>
            <li><a href="https://www.npmjs.com/package/prop-types" target="_blank">PropTypes</a></li>
        </ul>
        <p>Você pode encontrar a lista completa de dependências no arquivo <code>package.json</code>.</p>
        <h2 id="licenca">Licença</h2>
        <p>Este projeto é licenciado sob a Licença MIT. Consulte o arquivo <a href="LICENSE">LICENSE</a> para obter mais detalhes.</p>
        <p>Sinta-se à vontade para contribuir com melhorias ou abrir issues para reportar problemas. Aproveite a exploração da API do Rick and Morty com esta aplicação React!</p>
    </div>
</body>
</html>

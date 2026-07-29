.. raw:: html

    <div style="height: 0; visibility: hidden;">

Stpr
====

.. raw:: html

    </div>

    <div class="main-content">
        <div class="main-section two-col fill-v">
            <div class="left">
                <div class="above">A structured concurrency library for Python</div>
                <h1>Concurrency <br/>made <em>easy.</em></h1>
                <p>
                    Stpr lets you write concurrent pipelines with simple constructs -
                    no callbacks, no thread juggling, no asyncio boilerplate.
                </p>
                <div class="btns">
                    <a href="https://stprlib.net/docs/index.html" class="btn-fill">Get started</a>
                    <a href="https://github.com/FarStruct/stpr" class="btn-line">GitHub</a>
                </div>
                <div class="pip">
                    <span class="pip-tag">install</span>
                    <span class="pip-val">pip install stpr</span>
                    <button class="pip-copy" onclick="navigator.clipboard.writeText('pip install stpr');this.innerHTML='✓';setTimeout(()=>this.innerHTML='⎘',1500)" title="Copy">⎘</button>
                </div>
            </div>
            <div class="right">
                <div class="example">
                    <div class="example-canvas">
                        <div id="example-code" class="code">

    <pre><span class="ck">import</span> <span class="ct">stpr</span>

    <span class="cm"># Two code blocks run concurrently</span>
    <span class="ck">with</span> parallel:
    <div class="hlbg hl1">    <span class="ck">with</span> seq:              <span class="cm"># block A</span>
            <span class="cf">validate</span>(data)
            <span class="cf">transform</span>(data)
            <span class="cf">store</span>(data)</div><div class="hlbg hl2">    <span class="ck">with</span> seq:              <span class="cm"># block B</span>
            <span class="cf">fetch_meta</span>()
            <span class="ck">with</span> parallel:     <span class="cm"># nested parallelism</span>
                <span class="cf">index</span>()
                <span class="cf">notify</span>()
            <span class="cf">audit_log</span>()</div></pre>
                        </div>
                        <hr/>
                        <div id="dag" class="dag">
                            <img src="_static/ex-graph.svg"/>
                        </div>
                    </div>
                </div><!-- example -->
            </div>
        </div>

        <div class="main-section one-col shaded-section">
            <div class="above">Features</div>
            <h2>The right tools for writing concurrent programs</h2>

            <p class="half">A concise API that gives you composable concurrency primitives.</p>
            <div class="m-two-col">
                <div class="cell">
                    <p class="cell-title">Composition</p>
                    <div class="rule"></div>
                    <h3>Code structure is execution structure</h3>
                    <p>Nesting <code>parallel</code> inside <code>seq</code> inside <code>parallel</code> works
                    exactly as it reads. The execution graph is derived directly from the code structure.</p>
                </div>
                <div class="cell">
                    <p class="cell-title">Easy Migration</p>
                    <div class="rule"></div>
                    <h3>Decorator-based adoption</h3>
                    <p>Add <code>@stpr.fn</code> to any existing function to make it asynchronous and enable
                    all Stpr features. No need to change the function body. Stpr will use the existing synchronous
                    functions and switch to using <code>await</code> automatically when they are made async.</p>
                </div>
                <div class="cell">
                    <p class="cell-title">Performance</p>
                    <div class="rule"></div>
                    <h3>Scalable async I/O</h3>
                    <p>Thousands of concurrent network calls, file reads, and DB queries on a single
                    thread using asyncio event loops without the complexity of asyncio.</p>
                </div>
                <div class="cell">
                    <p class="cell-title">Safety</p>
                    <div class="rule"></div>
                    <h3>Structured error handling</h3>
                    <p>Concurrent primitives use structure exception handling semantics in which
                    errors propagate cleanly through context manager scopes.</p>
                </div>
            </div>
        </div>

        <div class="main-section two-col">
            <div class="left">
                <div class="above">Installation</div>
                <h2>Up and running in seconds</h2>
                <p>
                    Requires Python 3.8 or later. Minimal external dependencies.
                </p>
                <a href="https://stprlib.net/install.html" class="install-link">
                    Full install guide &rarr;
                </a>
            </div>
            <div class="right">
                <div class="install">
                    <div class="install-section">
                        <h3>PyPI — recommended</h3>
                        <div class="code">
                            <span class="pt">$ </span><span class="cmd">pip</span> install stpr
                        </div>
                    </div>
                    <div class="install-section">
                        <h3>From source</h3>
                        <div class="code">
                            <span class="pt">$ </span><span class="cmd">git</span> clone https://github.com/hategan/stpr<br>
                            <span class="pt">$ </span><span class="cmd">pip</span> install -e ./stpr
                        </div>
                    </div>
                    <div class="install-section">
                        <h3>Verify</h3>
                        <div class="code"><span class="pt">$ </span>python -c <span class="cs">'import stpr; print(stpr.__version__)'</span></div>
                    </div>
                  </div>
            </div>
        </div>

        <div class="footer">
            <h2>Build faster pipelines</h2>
            <p>Open souurce. Built for Python developers.</p>
            <div class="footer-buttons">
                <a href="https://stprlib.net/docs/index.html" class="btn-white">Read the documentation</a>
                <a href="https://github.com/FarStruct/stpr" class="btn-glass"><img src="_static/github-mark.png" height="18px"></img>View on GitHub</a>
            </div>
        </div>
    </div>

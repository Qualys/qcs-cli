THIS TOOL IS PROVIDED TO YOU "AS IS." TO THE EXTENT PERMITTED BY LAW, QUALYS HEREBY DISCLAIMS ALL WARRANTIES AND LIABILITY FOR THE PROVISION OR USE OF THIS TOOL. 
IN NO EVENT SHALL THESE TOOLS BE DEEMED TO BE CLOUD SERVICES AS PROVIDED BY QUALYS


<h1> Qualys Container Security - CLI </h1>

<h2>Overview</h2>

<p><code>qcs-cli</code> is a command-line interface (CLI) tool designed to interact with Qualys components. It allows users to check the status of components, export logs, and run the tool in both interactive and non-interactive modes. The tool is intended to simplify operations and provide easy access to essential Qualys components from the command line.</p>

<h2>Installation</h2>

<p>To install <code>qcs-cli</code>, download the latest release from the official repository, and place the executable in a directory included in your system's PATH.</p>

<h2>Usage</h2>

<p>The <code>qcs-cli</code> tool provides several commands to interact with Qualys components. Below is a summary of the available commands and their usage:</p>

<h3>Basic Usage</h3>

<pre><code>qcs-cli [command] [flags]</code></pre>

<h3>Available Commands</h3>
<ul>
  <li><strong>export-logs</strong>: Exports logs for the Qualys components.</li>
  <li><strong>help</strong>: Provides help information about any command.</li>
  <li><strong>status</strong>: Checks the status of Qualys components.</li>
</ul>

<h3>Global Flags</h3>
<ul>
  <li><code>-d, --debug</code>: Enable debug logs for the CLI tool.</li>
  <li><code>-h, --help</code>: Display help information for <code>qcs-cli</code>.</li>
  <li><code>-i, --interactive</code>: Run the CLI tool in interactive mode.</li>
  <li><code>--kubeconfig string</code>: Specify the path to the kubeconfig file to use for CLI requests.</li>
  <li><code>-o, --output-dir string</code>: Specify the directory path to store the output of the CLI tool. The default is <code>/tmp/output</code>.</li>
  <li><code>-v, --version</code>: Display the version of <code>qcs-cli</code>.</li>
</ul>

<h3>Command-Specific Help</h3>

<p>For more detailed information on any command, use:</p>

<pre><code>qcs-cli [command] --help</code></pre>

<h2>Examples</h2>

<h3>Check Status of Qualys Sensors</h3>

<pre><code>qcs-cli status sensors [flags]</code></pre>

<h3>Check Status of specific Qualys Sensors</h3>

<pre><code>qcs-cli status sensors --sensors qcs-sensor,cluster-sensor</code></pre>

<h3>Export Logs for Qualys Sensors and copy the logs to a specific directory</h3>

<pre><code>qcs-cli --output-dir /path/to/save/logs export-logs sensors </code></pre>

<h3>Export Logs for Qualys Sensors from specific node</h3>

<pre><code>qcs-cli export-logs sensors --nodes &lt;node-name &gt;  </code></pre>

<h3>Run in Interactive Mode</h3>

<pre><code>qcs-cli --interactive status sensors</code></pre>

<h2>Custom Configuration</h2>

<h3>Kubeconfig File</h3>

<p>You can specify a custom kubeconfig file using the <code>--kubeconfig</code> flag:</p>

<pre><code>qcs-cli status sensors --kubeconfig /path/to/kubeconfig</code></pre>

<h2>Debugging</h2>

<p>To enable debug logs, use the <code>--debug</code> flag:</p>

<pre><code>qcs-cli --debug [command] [subcommand] [flags]</code></pre>



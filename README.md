# LiteDemo
A very simple project to show off <b>Globalyzer Lite</b> and with <b>LRM</b>
On the Dashboard, it will show up as <code>Lingoport.LRMandLite</code>, using this kind of script:

<pre>
<code>
# Get the code using LRM's config_vcs.properties (so files can be pushed back)
cd $JENKINS_HOME
. $LRM_HOME/bin/init_vars.sh
. $LRM_HOME/bin/vcs/$VCS_TYPE/checkout_project.sh

# Run Lite and Generate Reports
java -jar $LITE_HOME/globalyzer-lite.jar $WORKSPACE/ProjectDefinition.xml

# Run the LRM Reports
. $LRM_HOME/bin/generate_lrm_reports.sh

# Update the Dashboard
. $LRM_HOME/bin/update_dashboard.sh

# Pseudo-localize the resource bundles
. $LRM_HOME/bin/pseudo_localize.sh
</code>
</pre>



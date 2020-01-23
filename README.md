

this is an unstructured [Anthos Config
Management](https://cloud.google.com/anthos/config-management/) repository. the
config which is to be sync'ed is located in the [config-root](config-root)
directory here and when used in this mode, the ACM sync'ed does the equivalent
of `kubectl apply -R -f config-root/` to apply the config (plus important things
like sequencing to avoid issues of ordering).


Adjacent to it is an example [ConfigManagement
resource](config-management.yaml) with parameters to point to the correct
directory and also the flag to enable the unstructured mode. This mode is in
contrast to the default mode of [ACM
Repos](https://cloud.google.com/anthos-config-management/docs/concepts/repo)
which has a dedicated directory for cluster scoped resources and a namespaces
directory which enables push down inheritance of resource in intermediate,
non-leaf directories.




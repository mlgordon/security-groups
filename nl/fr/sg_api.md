---



copyright:
  years: 2017
lastupdated: "2017-08-10"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Référence d'API du groupe de sécurité
{: #api-reference} 

L'interface de programmation SoftLayer&reg; permet aux développeurs et aux administrateurs système d'interagir directement avec le système backend de SoftLayer.
{:shortdesc}

L'interface de programmation SoftLayer (SLAPI) offre un grand nombre de fonctionnalités du portail client, ce qui signifie généralement que si une interaction est disponible dans le portail client, elle peut également être exécutée dans l'interface. Puisque vous pouvez interagir à l'aide d'un programme avec toutes les portions de l'environnement SoftLayer au sein de l'API, vous pouvez utiliser l'API pour automatiser les tâches. Vous pouvez, par exemple, utiliser l'API *SoftLayer_Virtual_Guest/createObject* pour déployer une instance de serveur virtuel avec un groupe de sécurité activé.

L'interface de programmation SoftLayer est un système à appel de procédure distante. Chaque appel implique l'envoi de données vers un noeud final d'API et la réception de données structurées en retour. Le format utilisé pour l'envoi et la réception de données à l'aide de SLAPI dépend de l'implémentation que vous avez choisie. 

Pour plus d'informations sur l'API SoftLayer, le serveur virtuel et les API de groupe de sécurité, voir les ressources suivantes dans le réseau de développement SoftLayer :
* [SoftLayer API Overview ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://sldn.softlayer.com/article/softlayer-api-overview){: new_window} 
* [Getting Started with the SoftLayer API ![External link icon](../../icons/launch-glyph.svg "External link icon")](http://sldn.softlayer.com/article/getting-started){: new_window}
* [*SoftLayer_Virtual_Guest/createObject* API ![External link icon](../../icons/launch-glyph.svg "External link icon")](http://sldn.softlayer.com/reference/services/SoftLayer_Virtual_Guest/createObject){: new_window}
* [*SoftLayer_Network_SecurityGroup* API ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://sldn.softlayer.com/reference/services/SoftLayer_Network_SecurityGroup){: new_window}
* [*SoftLayer_Virtual_Guest_Network_Component* API ![External link icon](../../icons/launch-glyph.svg "External link icon")](http://sldn.softlayer.com/reference/services/SoftLayer_Virtual_Guest_Network_Component){: new_window}

Vous pouvez aussi utiliser le client Python de l'API SoftLayer pour interagir avec les groupes de sécurité. Pour en savoir plus à ce sujet, reportez-vous aux liens suivants :
* [SoftLayer API Python Client: Working with Virtual Servers ![External link icon](../../icons/launch-glyph.svg "External link icon")](http://softlayer-python.readthedocs.io/en/latest/cli/vs.html){: new_window}
* [Python examples for softlayer_network_securitygroup ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://softlayer.github.io/classes/softlayer_network_securitygroup/){: new_window}

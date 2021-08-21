---
description: Die IUpdate-Schnittstelle definiert die folgenden Eigenschaften.
ms.assetid: d87544f1-a107-440f-8ce0-77d9f2d90578
title: IUpdate-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b93db8e7d8d6786e3f3f827d9eb2e9f97c43aae4781edf0a05fcf6d03e8fb1f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859860"
---
# <a name="iupdate-properties"></a>IUpdate-Eigenschaften

Die [**IUpdate-Schnittstelle**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate) definiert die folgenden Eigenschaften.



| Eigenschaft                                                                           | BESCHREIBUNG                                                                                                                                                                         |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutoSelectOnWebSites**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_autoselectonwebsites)                       | Ruft einen booleschen Wert ab, der angibt, ob das Update so gekennzeichnet ist, dass es von Windows Update automatisch ausgewählt wird.                                                                   |
| [**BundledUpdates**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_bundledupdates)                                   | Ruft eine Schnittstelle ab, die Informationen über die sortierte Liste der gebündelten Updates für das Update enthält.                                                                           |
| [**CanRequireSource**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_canrequiresource)                               | Ruft einen booleschen Wert ab, der angibt, ob das Quellmedium des Updates für die Installation oder Deinstallation erforderlich ist.                                                          |
| [**Kategorien**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_categories)                                           | Ruft eine Schnittstelle ab, die eine Auflistung von Kategorien enthält, zu denen das Update gehört.                                                                                             |
| [**Stichtag**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_deadline)                                               | Ruft das Datum ab, an dem das Update installiert werden muss.                                                                                                                                |
| [**DeltaCompressedContentAvailable**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_deltacompressedcontentavailable) | Ruft einen booleschen Wert ab, der angibt, ob deltakomprimierte Inhalte auf einem Server für das Update verfügbar sind.                                                                       |
| [**DeltaCompressedContentPreferred**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_deltacompressedcontentpreferred) | Ruft einen booleschen Wert ab, der angibt, ob deltakomprimierte Inhalte während des Herunterladens und Installierens oder Deinstallierens des Updates bevorzugt werden sollen, wenn deltakomprimierte Inhalte verfügbar sind. |
| [**DeploymentAction**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_deploymentaction)                               | Ruft die Aktion ab, für die das Update bereitgestellt wird.                                                                                                                                   |
| [**Beschreibung**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_description)                                         | Ruft die lokalisierte Beschreibung des Updates ab.                                                                                                                                       |
| [**DownloadContents**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_downloadcontents)                               | Ruft Dateiinformationen zum Downloadinhalt des Updates ab.                                                                                                                    |
| [**DownloadPriority**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_downloadpriority)                               | Ruft die vorgeschlagene Downloadpriorität des Updates ab.                                                                                                                                 |
| [**EulaAccepted**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_eulaaccepted)                                       | Ruft einen booleschen Wert ab, der angibt, ob die Microsoft-Software-Lizenzbedingungen, die dem Update zugeordnet sind, für den Computer akzeptiert werden.                                 |
| [**EulaText**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_eulatext)                                               | Ruft den vollständig lokalisierten Text der Microsoft-Software-Lizenzbedingungen ab, die dem Update zugeordnet sind.                                                                           |
| [**HandlerID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_handlerid)                                             | Ruft den Installationshandler des Updates ab.                                                                                                                                             |
| [**Identity**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_identity)                                               | Ruft eine Schnittstelle ab, die den eindeutigen Bezeichner des Updates enthält.                                                                                                                |
| [**Image**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_image)                                                     | Ruft eine Schnittstelle ab, die Informationen zu einem Bild enthält, das dem Update zugeordnet ist.                                                                                      |
| [**InstallationBehavior**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_installationbehavior)                       | Ruft eine Schnittstelle ab, die die Installationsoptionen des Updates enthält.                                                                                                             |
| [**IsBeta**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_isbeta)                                                   | Ruft einen booleschen Wert ab, der angibt, ob es sich bei dem Update um ein Beta-Release handelt.                                                                                                           |
| [**IsDownloaded**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_isdownloaded)                                       | Ruft einen booleschen Wert ab, der angibt, ob der gesamte Updateinhalt auf dem Computer zwischengespeichert wird.                                                                                       |
| [**IsHidden**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden)                                               | Ruft einen booleschen Wert ab, der angibt, ob ein Update von einem Benutzer ausgeblendet wird.                                                                                                          |
| [**IsInstalled**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_isinstalled)                                         | Ruft einen booleschen Wert ab, der angibt, ob das Update auf einem Computer installiert ist, wenn die Suche ausgeführt wird.                                                                     |
| [**IsKategorieory**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ismandatory)                                         | Ruft einen booleschen Wert ab, der angibt, ob die Installation des Updates obligatorisch ist.                                                                                            |
| [**IsUninstallable**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_isuninstallable)                                 | Ruft einen booleschen Wert ab, der angibt, ob ein Benutzer das Update von einem Computer deinstallieren kann.                                                                                        |
| [**KBArticleIDs**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_kbarticleids)                                       | Ruft eine Auflistung Microsoft Knowledge Base Artikel-IDs ab, die dem Update zugeordnet sind.                                                                                      |
| [**Sprachen**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_languages)                                              | Ruft eine Schnittstelle ab, die die vom Update unterstützten Sprachen enthält.                                                                                                     |
| [**LastDeploymentChangeTime**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_lastdeploymentchangetime)               | Ruft das Datum der letzten Veröffentlichung des Updates in koordinierte Weltzeit Datum und Uhrzeit (UTC) auf dem Server ab, der das Update bereitstellt.                                               |
| [**MaxDownloadSize**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_maxdownloadsize)                                 | Ruft die maximale Downloadgröße des Updates ab.                                                                                                                                       |
| [**MinDownloadSize**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_mindownloadsize)                                 | Ruft die minimale Downloadgröße des Updates ab.                                                                                                                                       |
| [**MoreInfoUrls**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_moreinfourls)                                       | Ruft eine Auflistung sprachspezifischer Zeichenfolgen ab, die die Links zu weiteren Informationen zum Update angeben.                                                                    |
| [**MsrcSeverity**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_msrcseverity)                                       | Ruft den Microsoft Security Response Center Schweregrad des Updates ab.                                                                                                          |
| [**RecommendedCPUSpeed**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_recommendedcpuspeed)                         | Ruft die empfohlene CPU-Geschwindigkeit für die Installation des Updates in Megahertz (MHz) ab.                                                                                                      |
| [**RecommendedHardDiskSpace**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_recommendedharddiskspace)               | Ruft den empfohlenen freien Speicherplatz ab, der auf der Festplatte verfügbar sein sollte, bevor Sie das Update installieren. Der freie Speicherplatz wird in Megabyte (MB) angegeben.                             |
| [**RecommendedMemory**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_recommendedmemory)                             | Ruft die empfohlene größe des physischen Arbeitsspeichers ab, die auf Ihrem Computer verfügbar sein sollte, bevor Sie das Update installieren. Die Größe des physischen Arbeitsspeichers wird in Megabyte (MB) angegeben.         |
| [**Releasenotes**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_releasenotes)                                       | Ruft die lokalisierten Versionshinweise für das Update ab.                                                                                                                                    |
| [**SecurityBulletinIDs**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_securitybulletinids)                         | Ruft eine Auflistung von Zeichenfolgenwerten ab, die die dem Update zugeordneten Sicherheitsbulletin-IDs enthalten.                                                                      |
| [**SupersededUpdateIDs**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_supersededupdateids)                         | Ruft eine Auflistung von Updatebezeichnern ab. Diese Auflistung von Bezeichnern gibt die Updates an, die durch das Update ersetzt werden.                                                    |
| [**Supporturl**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_supporturl)                                           | Ruft einen Link zu den sprachspezifischen Unterstützungsinformationen für das Update ab.                                                                                                       |
| [**Titel**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_title)                                                     | Ruft den lokalisierten Titel des Updates ab.                                                                                                                                             |
| [**type**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_type)                                                       | Ruft den Updatetyp ab.                                                                                                                                                        |
| [**DeinstallationBehavior**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_uninstallationbehavior)                   | Ruft eine Schnittstelle ab, die die Deinstallationsoptionen für das Update enthält.                                                                                                          |
| [**DeinstallationNotes**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_uninstallationnotes)                         | Ruft die Deinstallationshinweise für das Update ab.                                                                                                                                       |
| [**DeinstallationSchritte**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_uninstallationsteps)                         | Ruft eine Schnittstelle ab, die die Deinstallationsschritte für das Update enthält.                                                                                                            |



 

 

 




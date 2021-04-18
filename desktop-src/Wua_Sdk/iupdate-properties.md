---
description: Die iupdate-Schnittstelle definiert die folgenden Eigenschaften.
ms.assetid: d87544f1-a107-440f-8ce0-77d9f2d90578
title: Iupdate-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7df3f67f95936ea54dd09131e605da9e439caa43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526693"
---
# <a name="iupdate-properties"></a>Iupdate-Eigenschaften

Die [**iupdate**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate) -Schnittstelle definiert die folgenden Eigenschaften.



| Eigenschaft                                                                           | BESCHREIBUNG                                                                                                                                                                         |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Autoselectonwebsites**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_autoselectonwebsites)                       | Ruft einen booleschen Wert ab, der angibt, ob das Update so gekennzeichnet ist, dass es automatisch von Windows Update ausgewählt wird.                                                                   |
| [**Bundledupdates**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_bundledupdates)                                   | Ruft eine Schnittstelle ab, die Informationen über die geordnete Liste der gebündelten Updates für das Update enthält.                                                                           |
| [**Canrequirements-Quelle**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_canrequiresource)                               | Ruft einen booleschen Wert ab, der angibt, ob das Quell Medium des Updates für die Installation oder die Installation erforderlich ist.                                                          |
| [**Kategorien**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_categories)                                           | Ruft eine Schnittstelle ab, die eine Auflistung von Kategorien enthält, zu denen das Update gehört.                                                                                             |
| [**Stichtag**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_deadline)                                               | Ruft das Datum ab, an dem das Update installiert werden muss.                                                                                                                                |
| [**Delta-dcontentavailable**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_deltacompressedcontentavailable) | Ruft einen booleschen Wert ab, der angibt, ob Delta komprimierter Inhalt auf einem Server für das Update verfügbar ist.                                                                       |
| [**Delta-dcontentpreferred**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_deltacompressedcontentpreferred) | Ruft einen booleschen Wert ab, der angibt, ob Delta komprimierter Inhalt beim Herunterladen und installieren oder Deinstallieren des Updates bevorzugt werden soll, wenn Delta komprimierter Inhalt verfügbar ist. |
| [**Deploymentaction**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_deploymentaction)                               | Ruft die Aktion ab, für die das Update bereitgestellt wird.                                                                                                                                   |
| [**Beschreibung**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_description)                                         | Ruft die lokalisierte Beschreibung des Updates ab.                                                                                                                                       |
| [**Download Content**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_downloadcontents)                               | Ruft Dateiinformationen über den Download Inhalt des Updates ab.                                                                                                                    |
| [**Download Priorität**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_downloadpriority)                               | Ruft die empfohlene Download Priorität des Updates ab.                                                                                                                                 |
| [**Eulaaccepted**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_eulaaccepted)                                       | Ruft einen booleschen Wert ab, der angibt, ob die Microsoft-Software-Lizenzbedingungen, die dem Update zugeordnet sind, für den Computer akzeptiert werden.                                 |
| [**Eulatext**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_eulatext)                                               | Ruft den vollständig lokalisierten Text der Microsoft-Software-Lizenzbedingungen ab, die dem Update zugeordnet sind.                                                                           |
| [**Handlerid**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_handlerid)                                             | Ruft den Installations Handler für das Update ab.                                                                                                                                             |
| [**Identity**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_identity)                                               | Ruft eine Schnittstelle ab, die den eindeutigen Bezeichner des Updates enthält.                                                                                                                |
| [**Image**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_image)                                                     | Ruft eine Schnittstelle ab, die Informationen zu einem Bild enthält, das mit dem Update verknüpft ist.                                                                                      |
| [**Installationbehavior**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_installationbehavior)                       | Ruft eine Schnittstelle ab, die die Installationsoptionen für das Update enthält.                                                                                                             |
| [**Isbeta**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_isbeta)                                                   | Ruft einen booleschen Wert ab, der angibt, ob das Update eine Beta Version ist.                                                                                                           |
| [**Isdownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_isdownloaded)                                       | Ruft einen booleschen Wert ab, der angibt, ob der gesamte Update Inhalt auf dem Computer zwischengespeichert wird.                                                                                       |
| [**IsHidden**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden)                                               | Ruft einen booleschen Wert ab, der angibt, ob ein Update von einem Benutzer ausgeblendet wird.                                                                                                          |
| [**IsInstalled**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_isinstalled)                                         | Ruft einen booleschen Wert ab, der angibt, ob das Update auf einem Computer installiert wird, wenn die Suche durchgeführt wird.                                                                     |
| [**IsMandatory**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ismandatory)                                         | Ruft einen booleschen Wert ab, der angibt, ob die Installation des Updates obligatorisch ist.                                                                                            |
| [**Isuninstalable**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_isuninstallable)                                 | Ruft einen booleschen Wert ab, der angibt, ob ein Benutzer das Update von einem Computer deinstallieren kann.                                                                                        |
| [**KBArticleIDs**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_kbarticleids)                                       | Ruft eine Auflistung der Microsoft Knowledge Base-Artikel-IDs ab, die mit dem Update verknüpft sind.                                                                                      |
| [**Sprachen**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_languages)                                              | Ruft eine Schnittstelle ab, die die Sprachen enthält, die vom Update unterstützt werden.                                                                                                     |
| [**Lastdeploymentchangetime**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_lastdeploymentchangetime)               | Ruft das Datum und die Uhrzeit der letzten Veröffentlichung auf dem Server, auf dem das Update bereitgestellt wird, in koordinierter Weltzeit (UTC) ab.                                               |
| [**MaxDownloadSize**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_maxdownloadsize)                                 | Ruft die maximale Downloadgröße des Updates ab.                                                                                                                                       |
| [**Mindownloadsize**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_mindownloadsize)                                 | Ruft die minimale Downloadgröße des Updates ab.                                                                                                                                       |
| [**Morum fourls**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_moreinfourls)                                       | Ruft eine Auflistung von sprachspezifischen Zeichen folgen ab, die die Links zu weiteren Informationen über das Update angeben.                                                                    |
| [**Msrcschwere Grad**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_msrcseverity)                                       | Ruft den Schweregrad des Updates des Microsoft Security Response Centers ab.                                                                                                          |
| [**Empfehlungs Geschwindigkeit**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_recommendedcpuspeed)                         | Ruft die empfohlene CPU-Geschwindigkeit in Megahertz (MHz) ab, die zur Installation des Updates verwendet wird.                                                                                                      |
| [**Empfehlungs Bereich**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_recommendedharddiskspace)               | Ruft den empfohlenen freien Speicherplatz ab, der auf der Festplatte verfügbar sein sollte, bevor Sie das Update installieren. Der freie Speicherplatz wird in Megabyte (MB) angegeben.                             |
| [**Empfehlungs Speicher**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_recommendedmemory)                             | Ruft die empfohlene Größe des physischen Speichers ab, die auf Ihrem Computer verfügbar sein sollte, bevor Sie das Update installieren. Die Größe des physischen Speichers ist in Megabyte (MB) angegeben.         |
| [**Releasenotes**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_releasenotes)                                       | Ruft die lokalisierten Versions Hinweise für das Update ab.                                                                                                                                    |
| [**Securitybulletinids**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_securitybulletinids)                         | Ruft eine Auflistung von Zeichen folgen Werten ab, die die Sicherheitsbulletin-IDs enthalten, die mit dem Update verknüpft sind.                                                                      |
| [**Ablösen von abdedupdateids**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_supersededupdateids)                         | Ruft eine Auflistung von Update bezeichatoren ab. Diese Auflistung von Bezeichner gibt die Updates an, die durch das Update abgelöst werden.                                                    |
| [**SupportUrl**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_supporturl)                                           | Ruft einen Hyperlink zu den sprachspezifischen Unterstützungs Informationen für das Update ab.                                                                                                       |
| [**Titel**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_title)                                                     | Ruft den lokalisierten Titel des Updates ab.                                                                                                                                             |
| [**type**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_type)                                                       | Ruft den Typ des Updates ab.                                                                                                                                                        |
| [**Uninstallationbehavior**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_uninstallationbehavior)                   | Ruft eine Schnittstelle ab, die die uninstallationsoptionen für das Update enthält.                                                                                                          |
| [**Uninstallationnotes**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_uninstallationnotes)                         | Ruft die uninstallationshinweise für das Update ab.                                                                                                                                       |
| [**Uninstallationsteps**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_uninstallationsteps)                         | Ruft eine Schnittstelle ab, die die uninstallations Schritte für das Update enthält.                                                                                                            |



 

 

 




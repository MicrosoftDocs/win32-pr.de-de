---
description: Die vorgeschlagenen Aktions Sequenzen für eine grundlegende InstallExecuteSequence-Tabelle in einer Windows Installer-Datenbank.
ms.assetid: 7f337f37-1528-4b7e-a628-f9d235510a6f
title: Empfohlene InstallExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c25f2db56ef3ad7296bddf4088ad32191f57df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530374"
---
# <a name="suggested-installexecutesequence"></a>Empfohlene InstallExecuteSequence



| Aktion                                                          | Bedingung                          | Sequenz |
|-----------------------------------------------------------------|------------------------------------|----------|
| [LaunchConditions](launchconditions-action.md)                 |                                    | 100      |
| [AppSearch](appsearch-action.md)                               |                                    | 400      |
| [Ccpsearch](ccpsearch-action.md)                               | Nicht [ **installiert**](installed.md) | 500      |
| [RMCCPSEARCH](rmccpsearch-action.md)                           | Nicht [ **installiert**](installed.md) | 600      |
| [ValidateProductID](validateproductid-action.md)               |                                    | 700      |
| [Costinitialize](costinitialize-action.md)                     |                                    | 800      |
| [Datei Kosten](filecost-action.md)                                 |                                    | 900      |
| [Costfinalize](costfinalize-action.md)                         |                                    | 1000     |
| ["Btodbcfolders"](setodbcfolders-action.md)                     |                                    | 1100     |
| [InstallValidate](installvalidate-action.md)                   |                                    | 1400     |
| [Installinitialisieren](installinitialize-action.md)               |                                    | 1500     |
| [Zuordnung von "Zuweisung"](allocateregistryspace-action.md)       | Nicht [ **installiert**](installed.md) | 1550     |
| [ProcessComponents](processcomponents-action.md)               |                                    | 1600     |
| [Unpublishcomponents](unpublishcomponents-action.md)           |                                    | 1.700     |
| [Nicht publishfeatures](unpublishfeatures-action.md)               |                                    | 1800     |
| [Stop Services](stopservices-action.md)                         | [**VersionNT**](versionnt.md)     | 1.900     |
| [Delta Service Services](deleteservices-action.md)                     | [**VersionNT**](versionnt.md)     | 2000     |
| [Unregistercomplus](unregistercomplus-action.md)               |                                    | 2100     |
| [Selfunregmodules](selfunregmodules-action.md)                 |                                    | 2200     |
| [Unregistertypelibraries](unregistertypelibraries-action.md)   |                                    | 2300     |
| [Removeodbc](removeodbc-action.md)                             |                                    | 2400     |
| [Unregisterfonts](unregisterfonts-action.md)                   |                                    | 2500     |
| [Removeregistryvalues](removeregistryvalues-action.md)         |                                    | 2600     |
| [Unregisterclassinfo](unregisterclassinfo-action.md)           |                                    | 2700     |
| [Unregisterextensioninfo](unregisterextensioninfo-action.md)   |                                    | 2800     |
| [Unregisterprogidinfo](unregisterprogidinfo-action.md)         |                                    | 2900     |
| [Unregistermimeinfo](unregistermimeinfo-action.md)             |                                    | 3000     |
| [RemoveIniValues](removeinivalues-action.md)                   |                                    | 3100     |
| [Removeshortcuts](removeshortcuts-action.md)                   |                                    | 3200     |
| [Removeumgebfäden](removeenvironmentstrings-action.md) |                                    | 3300     |
| [RemoveDuplicateFiles](removeduplicatefiles-action.md)         |                                    | 3400     |
| [RemoveFiles](removefiles-action.md)                           |                                    | 3500     |
| [RemoveFolders](removefolders-action.md)                       |                                    | 3600     |
| ["Kreatefolders"](createfolders-action.md)                       |                                    | 3700     |
| ["Muvefiles"](movefiles-action.md)                               |                                    | 3800     |
| [InstallFiles](installfiles-action.md)                         |                                    | 4000     |
| [Patchdateien](patchfiles-action.md)                             |                                    | 4090     |
| [Duplicatefiles](duplicatefiles-action.md)                     |                                    | 4210     |
| [BindImage](bindimage-action.md)                               |                                    | 4300     |
| ["Kreateshortcuts"](createshortcuts-action.md)                   |                                    | 4500     |
| [RegisterClassInfo](registerclassinfo-action.md)               |                                    | 4600     |
| [RegisterExtensionInfo](registerextensioninfo-action.md)       |                                    | 4700     |
| [Registerprogidinfo](registerprogidinfo-action.md)             |                                    | 4800     |
| [Registermimeinfo](registermimeinfo-action.md)                 |                                    | 4900     |
| ["Schreibegistryvalues"](writeregistryvalues-action.md)           |                                    | 5.000     |
| ["Write"-Werte](writeinivalues-action.md)                     |                                    | 5100     |
| [Write-Umgebungs Zeichenfolgen](writeenvironmentstrings-action.md)   |                                    | 5200     |
| [Register Fonts](registerfonts-action.md)                       |                                    | 5300     |
| [Installodbc](installodbc-action.md)                           |                                    | 5400     |
| [Registertypelibraries](registertypelibraries-action.md)       |                                    | 5500     |
| [SelfRegModules](selfregmodules-action.md)                     |                                    | 5600     |
| [Registercomplus](registercomplus-action.md)                   |                                    | 5.700     |
| [Installdienste](installservices-action.md)                   | [**VersionNT**](versionnt.md)     | 5800     |
| [Startdienste](startservices-action.md)                       | [**VersionNT**](versionnt.md)     | 5900     |
| [Register User](registeruser-action.md)                         |                                    | 6000     |
| [Register Product](registerproduct-action.md)                   |                                    | 6100     |
| [PublishComponents](publishcomponents-action.md)               |                                    | 6200     |
| [Publishfeatures](publishfeatures-action.md)                   |                                    | 6300     |
| [Publishproduct](publishproduct-action.md)                     |                                    | 6400     |
| [InstallFinalize wurde](installfinalize-action.md)                   |                                    | 6600     |



 

 

 




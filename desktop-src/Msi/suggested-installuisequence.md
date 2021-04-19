---
description: Die vorgeschlagenen Aktions Sequenzen für eine grundlegende instaluisequence-Tabelle in einer Windows Installer-Datenbank.
ms.assetid: f1ddad1e-c075-4054-aa24-f1acdc72da96
title: Vorgeschlagene InstallUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1accfc889d51cb75b3928df60931c848b30bcad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348068"
---
# <a name="suggested-installuisequence"></a>Vorgeschlagene InstallUISequence



| Aktion                                          | Bedingung                                                                                                  | Sequenz |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------|----------|
| Fatalerrordlg                                   |                                                                                                            | -3       |
| Userexitdlg                                     |                                                                                                            | -2       |
| Exitdlg                                         |                                                                                                            | -1       |
| [LaunchConditions](launchconditions-action.md) |                                                                                                            | 100      |
| Preparedlg                                      |                                                                                                            | 140      |
| [AppSearch](appsearch-action.md)               |                                                                                                            | 400      |
| [Ccpsearch](ccpsearch-action.md)               | Nicht [ **installiert**](installed.md)                                                                         | 500      |
| [RMCCPSEARCH](rmccpsearch-action.md)           | Nicht [ **installiert**](installed.md)                                                                         | 600      |
| [Costinitialize](costinitialize-action.md)     |                                                                                                            | 800      |
| [Datei Kosten](filecost-action.md)                 |                                                                                                            | 900      |
| [Costfinalize](costfinalize-action.md)         |                                                                                                            | 1000     |
| Welcomedlg                                      | Nicht [ **installiert**](installed.md)                                                                         | 1230     |
| Resumedlg                                       | [**Installiert**](installed.md) Und ( [**fort**](resume.md) setzen oder [**vorab ausgewählt**](preselected.md))       | 1240     |
| Maintenancewelcomedlg                           | [**Installiert**](installed.md) Und nicht [**fortsetzen und nicht**](resume.md) [**vorab ausgewählt**](preselected.md) | 1250     |
| ProgressDlg                                     |                                                                                                            | 1280     |
| [ExecuteAction](executeaction-action.md)       |                                                                                                            | 1300     |



 

 

 




---
description: Die vorgeschlagenen Aktions Sequenzen für eine grundlegende AdminUISequence-Tabelle in einer Windows Installer-Datenbank.
ms.assetid: a5371133-7d55-4041-8e1f-ecc8245c8d3a
title: Vorgeschlagene AdminUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af34c0662d19070b1d97b88e8942b2276cc64a97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755400"
---
# <a name="suggested-adminuisequence"></a>Vorgeschlagene AdminUISequence



| Aktion                                      | Bedingung | Sequenz |
|---------------------------------------------|-----------|----------|
| Fatalerrordlg                               |           | -3       |
| Userexitdlg                                 |           | -2       |
| Exitdlg                                     |           | -1       |
| Preparedlg                                  |           | 140      |
| [Costinitialize](costinitialize-action.md) |           | 800      |
| [Datei Kosten](filecost-action.md)             |           | 900      |
| [Costfinalize](costfinalize-action.md)     |           | 1000     |
| Adminwelcomedlg                             |           | 1230     |
| ProgressDlg                                 |           | 1280     |
| [ExecuteAction](executeaction-action.md)   |           | 1300     |



 

 

 




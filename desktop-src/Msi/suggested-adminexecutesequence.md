---
description: Die vorgeschlagenen Aktions Sequenzen für eine grundlegende AdminExecuteSequence-Tabelle in einer Windows Installer-Datenbank.
ms.assetid: c54181d3-a16a-4007-a9ac-03ace98b637e
title: Vorgeschlagene AdminExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ead890630b397062c6b8e645385b2810fa39d95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527026"
---
# <a name="suggested-adminexecutesequence"></a>Vorgeschlagene AdminExecuteSequence



| Aktion                                                | Bedingung | Sequenz |
|-------------------------------------------------------|-----------|----------|
| [Costinitialize](costinitialize-action.md)           |           | 800      |
| [Datei Kosten](filecost-action.md)                       |           | 900      |
| [Costfinalize](costfinalize-action.md)               |           | 1000     |
| [InstallValidate](installvalidate-action.md)         |           | 1400     |
| [Installinitialisieren](installinitialize-action.md)     |           | 1500     |
| [Installadminpackage](installadminpackage-action.md) |           | 3900     |
| [InstallFiles](installfiles-action.md)               |           | 4000     |
| [InstallFinalize wurde](installfinalize-action.md)         |           | 6600     |



 

 

 




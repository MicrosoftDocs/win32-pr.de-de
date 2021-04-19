---
description: Die vorgeschlagenen Aktions Sequenzen für eine einfache AdvtExecuteSequence-Tabelle in einer Windows Installer-Datenbank.
ms.assetid: 42a55f8f-582a-499b-8a6b-c893da62a4d4
title: Vorgeschlagene AdvtExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a672579a174a0cc242ac503225d81976de60d9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355078"
---
# <a name="suggested-advtexecutesequence"></a>Vorgeschlagene AdvtExecuteSequence



| Aktion                                                    | Bedingung | Sequenz |
|-----------------------------------------------------------|-----------|----------|
| [Costinitialize](costinitialize-action.md)               |           | 800      |
| [Costfinalize](costfinalize-action.md)                   |           | 1000     |
| [InstallValidate](installvalidate-action.md)             |           | 1400     |
| [Installinitialisieren](installinitialize-action.md)         |           | 1500     |
| ["Kreateshortcuts"](createshortcuts-action.md)             |           | 4500     |
| [RegisterClassInfo](registerclassinfo-action.md)         |           | 4600     |
| [RegisterExtensionInfo](registerextensioninfo-action.md) |           | 4700     |
| [Registerprogidinfo](registerprogidinfo-action.md)       |           | 4800     |
| [Registermimeinfo](registermimeinfo-action.md)           |           | 4900     |
| [PublishComponents](publishcomponents-action.md)         |           | 6200     |
| [Publishfeatures](publishfeatures-action.md)             |           | 6300     |
| [Publishproduct](publishproduct-action.md)               |           | 6400     |
| [InstallFinalize wurde](installfinalize-action.md)             |           | 6600     |



 

 

 




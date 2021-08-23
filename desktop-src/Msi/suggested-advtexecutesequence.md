---
description: Die vorgeschlagenen Aktionssequenzen für eine einfache AdvtExecuteSequence-Tabelle in Windows Installer-Datenbank.
ms.assetid: 42a55f8f-582a-499b-8a6b-c893da62a4d4
title: Vorgeschlagene AdvtExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62e61768565b48395ed0046c353b51cf1fe4c7470125e61a92f0328a5edfb882
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627150"
---
# <a name="suggested-advtexecutesequence"></a>Vorgeschlagene AdvtExecuteSequence



| Aktion                                                    | Bedingung | Sequenz |
|-----------------------------------------------------------|-----------|----------|
| [CostInitialize](costinitialize-action.md)               |           | 800      |
| [CostFinalize](costfinalize-action.md)                   |           | 1000     |
| [InstallValidate](installvalidate-action.md)             |           | 1400     |
| [InstallInitialize](installinitialize-action.md)         |           | 1500     |
| [CreateShortcuts](createshortcuts-action.md)             |           | 4500     |
| [RegisterClassInfo](registerclassinfo-action.md)         |           | 4600     |
| [RegisterExtensionInfo](registerextensioninfo-action.md) |           | 4700     |
| [RegisterProgIdInfo](registerprogidinfo-action.md)       |           | 4800     |
| [RegisterMIMEInfo](registermimeinfo-action.md)           |           | 4900     |
| [PublishComponents](publishcomponents-action.md)         |           | 6200     |
| [PublishFeatures](publishfeatures-action.md)             |           | 6300     |
| [PublishProduct](publishproduct-action.md)               |           | 6400     |
| [InstallFinalize](installfinalize-action.md)             |           | 6600     |



 

 

 




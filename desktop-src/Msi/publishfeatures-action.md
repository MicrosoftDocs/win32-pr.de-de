---
description: Die publishfeatures-Aktion schreibt den Status jeder Funktion in die Systemregistrierung.
ms.assetid: 8205e865-e625-43b9-8ce9-cff8026b2717
title: Publishfeatures-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f5356ef89aa2651c470917a9b8d81b79ee83d01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106351666"
---
# <a name="publishfeatures-action"></a>Publishfeatures-Aktion

Die publishfeatures-Aktion schreibt den Status jeder Funktion in die Systemregistrierung. Der Funktionsstatus kann entweder nicht vorhanden, angekündigt oder installiert sein. Die publishfeatures-Aktion schreibt auch die featurekomponentenzuordnung für jede installierte Funktion in die Systemregistrierung.

Mit der publishfeatures-Aktion werden die [FeatureComponents-Tabelle](featurecomponents-table.md),- [Funktions Tabelle](feature-table.md)und- [Komponenten Tabelle](component-table.md)abgefragt.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die publishfeatures-Aktion muss vor [publishproduct](publishproduct-action.md)erfolgen.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen



| Feld | Beschreibung der Aktions Daten        |
|-------|-----------------------------------|
| \[1\] | Bezeichner der angekündigten Funktion. |



 

## <a name="remarks"></a>Bemerkungen

Die publishfeatures-Aktion veröffentlicht die Komposition aller Features, die für die Ankündigung oder Installation ausgewählt wurden.

 

 




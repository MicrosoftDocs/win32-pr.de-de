---
description: Die Aktion UnpublishComponents verwaltet die Nichtvertierung von Komponenten, die in der PublishComponent-Tabelle aufgeführt sind.
ms.assetid: 3e50f668-6d08-405e-a5a4-f422041ef0b1
title: Aktion "Nicht veröffentlichenKomponenten"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1feaca4449ffa344eeda828334f879ebc12905406446dd14623e3b9c4474c6b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810260"
---
# <a name="unpublishcomponents-action"></a>Aktion "Nicht veröffentlichenKomponenten"

Die Aktion UnpublishComponents verwaltet die Nichtvertierung von Komponenten, die in der PublishComponent-Tabelle aufgeführt sind. Dies sind Komponenten, die von anderen Produkten möglicherweise fehlerhaft sind. Diese Aktion entfernt Informationen zu veröffentlichten Komponenten aus der [PublishComponent-Tabelle,](publishcomponent-table.md) für die das entsprechende Feature derzeit für die Deinstallation ausgewählt ist.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Es gibt keine Sequenzeinschränkungen.

## <a name="actiondata-messages"></a>ActionData-Meldungen



| Feld | Beschreibung der Aktionsdaten                                   |
|-------|--------------------------------------------------------------|
| \[1\] | GUID, die die Komponenten-ID eines angekündigten Features darstellt. |
| \[2\] | Qualifizierer der Komponenten-ID.                               |



 


---
description: ICE08 überprüft, ob die Komponenten Tabelle doppelte GUIDs enthält. Jede Komponente muss eine eindeutige GUID aufweisen. Wenn die Komponenten Tabelle nicht vorhanden ist, wird keine Validierung durchgeführt.
ms.assetid: c8ff53f3-6587-479d-afb8-b09d0df3b673
title: ICE08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 051f32aa983fdae39fc3717d3c9036b542f14369
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349502"
---
# <a name="ice08"></a>ICE08

ICE08 überprüft, ob die [Komponenten Tabelle](component-table.md) doppelte [GUIDs](guid.md)enthält. Jede Komponente muss eine eindeutige GUID aufweisen. Wenn die Komponenten Tabelle nicht vorhanden ist, wird keine Validierung durchgeführt.

## <a name="result"></a>Ergebnis

ICE08 gibt eine Fehlermeldung aus, wenn mindestens zwei Einträge in der ComponentID-Spalte der Komponenten Tabelle dieselbe GUID enthalten.

## <a name="example"></a>Beispiel

Im folgenden Beispiel würde ICE08 eine Meldung veröffentlichen, die besagt, dass die Komponenten rot und grün doppelte GUIDs aufweisen.

[Komponenten Tabelle](component-table.md) (partiell)



| Komponente | ComponentID                            |
|-----------|----------------------------------------|
| Red       | {0000000A-0003-0000-0000-624474736554} |
| Blau      | {0000000A-0003-0000-0000-624474736354} |
| Grün     | {0000000A-0003-0000-0000-624474736554} |



 

Um diesen Fehler zu beheben, ändern Sie eine der doppelten GUIDs.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 




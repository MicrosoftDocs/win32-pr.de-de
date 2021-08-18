---
description: ICE08 überprüft, ob die Component-Tabelle keine doppelten GUIDs enthält. Jede Komponente muss über eine eindeutige GUID verfügen. Es wird keine Überprüfung durchgeführt, wenn die Component-Tabelle nicht vorhanden ist.
ms.assetid: c8ff53f3-6587-479d-afb8-b09d0df3b673
title: ICE08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6075b7c895242fe5cfa7608a414643a9e3491787fc59037f8761fa66b18354
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745320"
---
# <a name="ice08"></a>ICE08

ICE08 überprüft, ob die [Component-Tabelle](component-table.md) keine doppelten [GUIDs enthält.](guid.md) Jede Komponente muss über eine eindeutige GUID verfügen. Es wird keine Überprüfung durchgeführt, wenn die Component-Tabelle nicht vorhanden ist.

## <a name="result"></a>Ergebnis

ICE08 gibt eine Fehlermeldung aus, wenn mindestens zwei Einträge in der ComponentId-Spalte der Component-Tabelle dieselbe GUID enthalten.

## <a name="example"></a>Beispiel

Im folgenden Beispiel würde ICE08 eine Meldung veröffentlichen, die besagt, dass die Komponenten Rot und Grün doppelte GUIDs haben.

[Komponententabelle](component-table.md) (partiell)



| Komponente | Componentid                            |
|-----------|----------------------------------------|
| Red       | {0000000A-0003-0000-0000-624474736554} |
| Blau      | {0000000A-0003-0000-0000-624474736354} |
| Grün     | {0000000A-0003-0000-0000-624474736554} |



 

Um diesen Fehler zu beheben, ändern Sie eine der doppelten GUIDs.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 




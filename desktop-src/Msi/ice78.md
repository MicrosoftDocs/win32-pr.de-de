---
description: ICE78 überprüft, ob die AdvtUISequence-Tabelle entweder nicht vorhanden oder leer ist. Dies ist erforderlich, da während der Werbung keine Benutzeroberfläche zulässig ist.
ms.assetid: 8ed1c68f-331d-42f9-80df-bdcb42962482
title: ICE78
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d39061872b716c9cc05e983d72615bf287683fd9c316df5661c3085e545169f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119638120"
---
# <a name="ice78"></a>ICE78

ICE78 überprüft, ob die [AdvtUISequence-Tabelle](advtuisequence-table.md) entweder nicht vorhanden oder leer ist. Dies ist erforderlich, da während der Werbung keine Benutzeroberfläche zulässig ist.

## <a name="result"></a>Ergebnis

ICE78 gibt einen Fehler aus, wenn die AdvtUISequence-Tabelle vorhanden und nicht leer ist.

## <a name="example"></a>Beispiel

ICE78 meldet den folgenden Fehler für das Beispiel:

Aktion "Action1" in der AdvtUISequence-Tabelle gefunden. Während der Werbung ist keine Benutzeroberfläche zulässig. Daher muss die AdvtUISequence-Tabelle leer sein oder nicht vorhanden sein.

[AdvtUISequence-Tabelle](advtuisequence-table.md)(partiell)



| Aktion  | Bedingung | Sequenz |
|---------|-----------|----------|
| Action1 | TRUE      | 1        |



 

Um den Fehler zu beheben, entfernen Sie entweder "Action1" aus der Tabelle, oder entfernen Sie die Tabelle.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 




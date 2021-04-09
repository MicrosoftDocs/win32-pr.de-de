---
description: ICE78 überprüft, ob die Tabelle advtuisequence entweder nicht vorhanden oder leer ist. Dies ist erforderlich, da während der Werbung keine Benutzeroberfläche zulässig ist.
ms.assetid: 8ed1c68f-331d-42f9-80df-bdcb42962482
title: ICE78
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8993a0a03b0f70bf2d99511782bc9b7d259d4c9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129968"
---
# <a name="ice78"></a>ICE78

ICE78 überprüft, ob die [Tabelle advtuisequence](advtuisequence-table.md) entweder nicht vorhanden oder leer ist. Dies ist erforderlich, da während der Werbung keine Benutzeroberfläche zulässig ist.

## <a name="result"></a>Ergebnis

ICE78 gibt einen Fehler aus, wenn die advtuisequence-Tabelle vorhanden und nicht leer ist.

## <a name="example"></a>Beispiel

ICE78 meldet den folgenden Fehler für das Beispiel:

Die Aktion ' Action1 ' wurde in der advtuisequence-Tabelle gefunden. Während der Werbung ist keine Benutzeroberfläche zulässig. Daher muss die advtuisequence-Tabelle leer sein oder nicht vorhanden sein.

[Advtuisequence-Tabelle](advtuisequence-table.md)(partiell)



| Aktion  | Bedingung | Sequenz |
|---------|-----------|----------|
| Action1 | TRUE      | 1        |



 

Um den Fehler zu beheben, entfernen Sie entweder "Action1" aus der Tabelle, oder entfernen Sie die Tabelle.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 




---
title: DEFAULTACTION (Eigenschaft)
description: Die DEFAULTACTION-Eigenschaft eines Objekts beschreibt die primäre Manipulations Methode des Objekts aus der Sicht des Benutzers. Die DEFAULTACTION-Eigenschaft eines Objekts sollte ein Verb oder ein kurzes Verb-Ausdruck sein.
ms.assetid: 8242c0af-b42e-44a4-8807-d6740fa1a24a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73dc032037c331a2022f227cb8e8547dd8bce9d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309464"
---
# <a name="defaultaction-property"></a>DEFAULTACTION (Eigenschaft)

Die **DEFAULTACTION** -Eigenschaft eines Objekts beschreibt die primäre Manipulations Methode des Objekts aus der Sicht des Benutzers. Die **DEFAULTACTION** -Eigenschaft eines Objekts sollte ein Verb oder ein kurzes Verb-Ausdruck sein.

Die **DEFAULTACTION** -Eigenschaft wird durch Aufrufen von " [**IAccessible:: get \_ accdefaultaction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)" abgerufen.

Um die Standardaktion eines Objekts auszuführen, wird " [**IAccessible:: accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)" aufgerufen.

Nicht alle Objekte haben Standard Aktionen, und einige Objekte verfügen über eine Standardaktion, die sich auf Ihre [**Wert**](value-property.md) Eigenschaft bezieht, z. b. in den folgenden Beispielen:

-   Ein ausgewähltes Kontrollkästchen hat die Standardaktion "uncheck" und den Wert "aktiviert".
-   Ein gelöschtes Kontrollkästchen hat die Standardaktion "Check" und den Wert "deaktiviert".
-   Eine Schaltfläche mit der Bezeichnung "Print" hat die Standardaktion "Press" ohne Wert.
-   Ein statisches Text Steuerelement oder ein Bearbeitungs Steuerelement, das "Printer" anzeigt, hat keine Standardaktion, hat jedoch den Wert "Printer".

 

 





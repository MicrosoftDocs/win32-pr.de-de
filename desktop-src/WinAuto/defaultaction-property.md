---
title: DefaultAction-Eigenschaft
description: Die DefaultAction-Eigenschaft eines Objekts beschreibt die primäre Manipulationsmethode des Objekts aus sicht des Benutzers. Die DefaultAction-Eigenschaft eines Objekts sollte ein Verb oder ein kurzer Verbbegriff sein.
ms.assetid: 8242c0af-b42e-44a4-8807-d6740fa1a24a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd5aa70e0c6c633aa5b0ca3fe5c40049dbeb8cf2496c7785eea513821e1d5ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118325754"
---
# <a name="defaultaction-property"></a>DefaultAction-Eigenschaft

Die **DefaultAction-Eigenschaft eines** Objekts beschreibt die primäre Manipulationsmethode des Objekts aus sicht des Benutzers. Die **DefaultAction-Eigenschaft eines** Objekts sollte ein Verb oder ein kurzer Verbbegriff sein.

Die **DefaultAction-Eigenschaft** wird durch Aufrufen von [**IAccessible::get \_ accDefaultAction abgerufen.**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)

Um die Standardaktion eines Objekts durchzuführen, rufen Clients [**IAccessible::accDoDefaultAction auf.**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)

Nicht alle Objekte verfügen über Standardaktionen, und einige Objekte verfügen über eine Standardaktion, die mit ihrer [**Value-Eigenschaft**](value-property.md) verknüpft ist, wie in den folgenden Beispielen gezeigt:

-   Ein ausgewähltes Kontrollkästchen verfügt über die Standardaktion "Deaktivieren" und den Wert "Aktiviert".
-   Ein deaktiviertes Kontrollkästchen verfügt über die Standardaktion "Check" und den Wert "Unchecked".
-   Eine Schaltfläche mit der Bezeichnung "Drucken" hat die Standardaktion "Drücken" ohne Wert.
-   Ein statisches Textsteuerfeld oder ein Bearbeitungssteuerfeld, das "Printer" (Drucker) zeigt, hat keine Standardaktion, aber den Wert "Printer".

 

 





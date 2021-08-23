---
description: ICE15 überprüft, ob Inhaltstyp- und Erweiterungsverweise in den MIME- und Erweiterungstabellen reziprok sind. Die MIME-Tabelle muss auf einen Inhaltstyp auf eine Erweiterung verweisen, auf die die Erweiterungstabelle zurück auf denselben Inhaltstyp verweist.
ms.assetid: 8a38c8d2-324d-4de9-932b-d188ff5ccbaf
title: ICE15
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ce1e5e54dedd2663a9f849abee43e244c73d7aa5835426be05d4e0163f599ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529310"
---
# <a name="ice15"></a>ICE15

ICE15 überprüft, ob Inhaltstyp- und Erweiterungsverweise in den [MIME-](mime-table.md) und [Erweiterungstabellen](extension-table.md) reziprok sind. Die MIME-Tabelle muss auf einen Inhaltstyp auf eine Erweiterung verweisen, auf die die Erweiterungstabelle zurück auf denselben Inhaltstyp verweist.

Mehrere Erweiterungen können auf denselben MIME-Typ verweisen, solange der MIME-Typ auf eine der Erweiterungen verweist. Mehrere MIME-Typen können auf dieselbe Erweiterung verweisen, solange die Erweiterung auf einen der MIME-Typen verweist.

Beachten Sie, dass die MIME-Spalte in der Extension-Tabelle nicht auf NULL festgelegt werden kann, wenn eine MIME auf eine Erweiterung \_ verweist.

## <a name="result"></a>Ergebnis

ICE15 gibt einen Fehler aus, wenn der Inhaltstyp und die Erweiterungsverweise nicht reziprok sind.

## <a name="example"></a>Beispiel

ICE15 sendet zwei Fehlermeldungen für das gezeigte Beispiel:

-   Der Inhaltstyp test/x-flaps in der MIME-Tabelle verweist auf die Erweiterung tst, aber die Erweiterung tst in der Erweiterungstabelle verweist auf flaps/x-flaps. Dies ist nicht reziprok.
-   Der Inhaltstyp flaps/x-flaps verweist auf die Erweiterung flp, aber diese Erweiterung weist in der MIME-Spalte der Extension-Tabelle einen NULL-Eintrag \_ auf.

[MIME-Tabelle](mime-table.md) (partiell)



| ContentType   | Erweiterung\_ |
|---------------|-------------|
| test/x-test   | Tst         |
| flaps/x-flaps | Flp         |



 

[Erweiterungstabelle](extension-table.md) (teilweise)



| Erweiterung | Mime\_        |
|-----------|---------------|
| Tst       | flaps/x-flaps |
| Flp       | Null          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 




---
title: Verfügbar machen von Owner-Drawn Kombinations Feld Elementen
description: Anwendungsentwickler müssen IAccessible nicht implementieren, um die Elemente in einem von einem Besitzer gezeichneten Kombinations Feld mit dem Stil CBS hasstrings verfügbar zu machen, \_ da Microsoft Active Accessibility die Elemente in Kombinations Feldern mit diesem Stil verfügbar macht.
ms.assetid: 9ff14b2f-ae09-4839-b281-fba46addaf5f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 364dccaf21927e2d0092fc744d501f47830c6eeb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338081"
---
# <a name="exposing-owner-drawn-combo-box-items"></a>Verfügbar machen von Owner-Drawn Kombinations Feld Elementen

Anwendungsentwickler müssen [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nicht implementieren, um die Elemente in einem von einem Besitzer gezeichneten Kombinations Feld mit dem Stil **CBS \_ hasstrings** verfügbar zu machen, da Microsoft Active Accessibility die Elemente in Kombinations Feldern mit diesem Stil verfügbar macht. Die Elemente in einem vom Besitzer gezeichneten Kombinations Feld mit dem Format **CBS \_ hasstrings** werden als Text angezeigt. Dieser Stil wird jedoch auch mit vom Besitzer gezeichneten Kombinations Feldern verwendet, in denen kein Text angezeigt wird, sodass die Kombinations Feld Elemente von Microsoft Active Accessibility verfügbar gemacht werden.

Damit Microsoft Active Accessibility, die Elemente in einem von einem Besitzer gezeichneten Kombinations Feld verfügbar zu machen, das keinen Text anzeigt:

-   Verwenden Sie beim Erstellen des Kombinations Felds den Stil **CBS \_ hasstrings** .
-   Erstellen Sie eine texentsprechung, die jedes Element im Kombinations Feld benennt oder beschreibt.
-   Wenn Sie dem vom Besitzer gezeichneten Kombinations Feld Elemente hinzufügen, verwenden \_ Sie die CB AddString-Nachricht, um den Text hinzuzufügen, den Microsoft Active Accessibility verfügbar machen soll. Dieser Text wird nicht angezeigt und darf daher nicht Teil der vom Besitzer gezeichneten Daten sein. Fügen Sie die von einem Besitzer gezeichneten Elementdaten mithilfe der CB-Nachricht "-" \_ .

Beachten Sie bei Verwendung der obigen Methode Folgendes:

-   Bei Verwendung des **CBS- \_ Sortier** Stils wird das Kombinations Feld mit den angegebenen Zeichen folgen und nicht mit der [WM \_ compareitem](../controls/wm-compareitem.md) -Rückruf Prozedur sortiert.
-   Verwenden Sie mit den vom Besitzer gezeichneten Variablen Kombinations Feldern, die mit der Formatvorlage CBS-Besitzer erstellt wurden, eine globale Variable oder einen anderen Mechanismus, um nachzuverfolgen, wann der **ItemData** -Member der **\_** [measureitemstruct](/windows/win32/api/winuser/ns-winuser-measureitemstruct) gültig ist. Die globale Variable ist erforderlich, da das System die [WM- \_ Datei "MeasureItem](../controls/wm-measureitem.md) " sendet, sobald die Zeichenfolge hinzugefügt wird, aber bevor die Elementdaten angefügt werden. an diesem Punkt ist der **ItemData** -Member ungültig.
-   Um die Zeichenfolge für ein Element in einem Kombinations Feld mit dem **CBS \_ hasstrings** -Stil zu ändern, löschen Sie das Element mit der [CB \_ deletestring](../controls/cb-deletestring.md) -Nachricht, und fügen Sie die neue Zeichenfolge mit der [CB \_ AddString](../controls/cb-addstring.md) -Nachricht hinzu.

 

 
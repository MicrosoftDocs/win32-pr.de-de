---
title: Verfügbar machen von Owner-Drawn Listenfeld Elementen
description: Anwendungsentwickler müssen IAccessible nicht implementieren, um die Elemente in einem von einem Besitzer gezeichneten Listenfeld mit dem Format lbs hasstrings verfügbar zu machen, \_ da Microsoft Active Accessibility die Elemente in Listenfeldern in diesem Stil verfügbar macht.
ms.assetid: d54ce297-ce8a-46c0-a86d-4acffa1eda27
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fbb72285f55796a285cd6e1a8838a629218659b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390778"
---
# <a name="exposing-owner-drawn-list-box-items"></a>Verfügbar machen von Owner-Drawn Listenfeld Elementen

Anwendungsentwickler müssen [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nicht implementieren, um die Elemente in einem von einem Besitzer gezeichneten Listenfeld mit dem Format **lbs \_ hasstrings** verfügbar zu machen, da Microsoft Active Accessibility die Elemente in Listenfeldern in diesem Stil verfügbar macht. Die Elemente in einem vom Besitzer gezeichneten Listenfeld mit dem **lbs \_ hasstrings** -Stil werden als Text angezeigt. Dieser Stil wird jedoch auch mit vom Besitzer gezeichneten Listenfeldern verwendet, in denen kein Text angezeigt wird, sodass die Listenfeld Elemente von Microsoft Active Accessibility verfügbar gemacht werden.

Damit Microsoft Active Accessibility, die Elemente in einem von einem Besitzer gezeichneten Listenfeld verfügbar zu machen, das keinen Text anzeigt:

-   Verwenden Sie den **lbs \_ hasstrings** -Stil, wenn Sie das Listenfeld erstellen.
-   Erstellen Sie eine texentsprechung, die jedes Element im Listenfeld benennt oder beschreibt.
-   Verwenden Sie beim Hinzufügen von Elementen zum Listenfeld "Besitzer gezeichnet" die [lb- \_ AddString](../controls/lb-addstring.md) -Nachricht, um den Text hinzuzufügen, den Microsoft Active Accessibility verfügbar machen soll. Dieser Text wird nicht angezeigt und ist daher nicht Teil der vom Besitzer gezeichneten Daten. Fügen Sie die vom Besitzer gezeichneten Elementdaten mithilfe der " [lb \_ ](../controls/lb-setitemdata.md) -Nachricht"-Nachricht hinzu.

Beachten Sie bei Verwendung der obigen Methode Folgendes:

-   Wenn Sie den **lbs- \_ Sortier** Stil verwenden, wird das Listenfeld mit den angegebenen Zeichen folgen und nicht mit der [WM \_ compareitem](../controls/wm-compareitem.md) -Rückruf Prozedur sortiert.
-   Mit vom Besitzer gezeichneten Variablen Listenfeldern, die mit der Style lbs-Besitzer Zeichenfolge erstellt wurden, verwenden Sie eine globale Variable oder einen anderen Mechanismus, um nachzuverfolgen, wann der **ItemData-Member** der [measureitemstruct](/windows/win32/api/winuser/ns-winuser-measureitemstruct) gültig ist. **\_** Die globale Variable wird benötigt, da das System die [WM- \_ MeasureItem](../controls/wm-measureitem.md) -Nachricht sendet, sobald die Zeichenfolge hinzugefügt wird, aber bevor die Elementdaten angefügt werden. an diesem Punkt ist der **ItemData** -Member ungültig.
-   Um die Zeichenfolge für ein Element in einem Listenfeld mit dem **lbs \_ hasstrings** -Stil zu ändern, löschen Sie das Element mit der [lb- \_ deletestring](../controls/lb-deletestring.md) -Nachricht, und fügen Sie die neue Zeichenfolge mit der LB \_ AddString-Nachricht hinzu.

 

 
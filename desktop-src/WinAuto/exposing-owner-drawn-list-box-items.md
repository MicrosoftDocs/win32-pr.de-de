---
title: Verfügbarmachen von Owner-Drawn Listenfeldelementen
description: Anwendungsentwickler müssen IAccessible nicht implementieren, um die Elemente in einem vom Besitzer gezeichneten Listenfeld mit dem Stil LBS HASSTRINGS verfügbar zu machen, \_ da Microsoft Active Accessibility die Elemente in Listenfeldern mit diesem Stil verfügbar macht.
ms.assetid: d54ce297-ce8a-46c0-a86d-4acffa1eda27
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fed68477680376373da6c16f59b3fb556b6a435f15f04daae8f3f1262829dc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115273"
---
# <a name="exposing-owner-drawn-list-box-items"></a>Verfügbarmachen von Owner-Drawn Listenfeldelementen

Anwendungsentwickler müssen [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nicht implementieren, um die Elemente in einem vom Besitzer gezeichneten Listenfeld mit dem Stil **LBS \_ HASSTRINGS** verfügbar zu machen, da Microsoft Active Accessibility die Elemente in Listenfeldern mit diesem Stil verfügbar macht. Die Elemente in einem vom Besitzer gezeichneten Listenfeld mit dem **LBS \_ HASSTRINGS-Format** werden als Text angezeigt. Dieser Stil wird jedoch auch mit vom Besitzer gezeichneten Listenfeldern verwendet, die keinen Text anzeigen, sodass die Listenfeldelemente von Microsoft Active Accessibility verfügbar gemacht werden.

So ermöglichen Microsoft Active Accessibility, die Elemente in einem vom Besitzer gezeichneten Listenfeld verfügbar zu machen, das keinen Text anzeigt:

-   Verwenden Sie beim Erstellen des Listenfelds den **\_ LBS HASSTRINGS-Stil.**
-   Erstellen Sie eine Textentsprechung, die jedes Element im Listenfeld benennt oder beschreibt.
-   Verwenden Sie beim Hinzufügen von Elementen zum vom Besitzer gezeichneten Listenfeld die [LB \_ ADDSTRING-Nachricht,](../controls/lb-addstring.md) um den Text hinzuzufügen, den Microsoft Active Accessibility verfügbar machen soll. Dieser Text wird nicht angezeigt, sodass er nicht Teil der vom Besitzer gezeichneten Daten ist. Fügen Sie die vom Besitzer gezeichneten Elementdaten mithilfe der [LB \_ SETITEMDATA-Nachricht](../controls/lb-setitemdata.md) hinzu.

Beachten Sie bei Verwendung der obigen Methode Folgendes:

-   Wenn Sie den **LBS \_ SORT-Stil** verwenden, wird das Listenfeld anhand der angegebenen Zeichenfolgen und nicht mit der [WM \_ COMPAREITEM-Rückrufprozedur](../controls/wm-compareitem.md) sortiert.
-   Verwenden Sie bei Listenfeldern mit besitzergezeichneten Variablen, die mit dem Stil **LBS \_ OWNERDRAWVARIABLE** erstellt wurden, eine globale Variable oder einen anderen Mechanismus, um nachzuverfolgen, wann das **itemData-Element** von [MEASUREITEMSTRUCT](/windows/win32/api/winuser/ns-winuser-measureitemstruct) gültig ist. Die globale Variable ist erforderlich, da das System die [WM \_ MEASUREITEM-Nachricht](../controls/wm-measureitem.md) sendet, sobald die Zeichenfolge hinzugefügt wird, aber bevor die Elementdaten angefügt werden. An diesem Punkt ist das **elementData-Element** ungültig.
-   Um die Zeichenfolge für ein Element in einem Listenfeld mit dem **LBS \_ HASSTRINGS-Format** zu ändern, löschen Sie das Element mit der [LB \_ DELETESTRING-Nachricht,](../controls/lb-deletestring.md) und fügen Sie die neue Zeichenfolge mit der LB \_ ADDSTRING-Nachricht hinzu.

 

 
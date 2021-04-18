---
title: Erhalten eines barrierefreien Objekt Schnittstellen Zeigers
description: Microsoft Active Accessibility-Client Anwendungen rufen Schnittstellen Zeiger auf barrierefreie Objekte ab, indem Sie eine der folgenden Funktionen verwenden.
ms.assetid: b82467f0-0d46-482a-8f6d-ad64f236601e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45d4006bf073075f2aa47a9911565213050e3d11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106337247"
---
# <a name="getting-an-accessible-object-interface-pointer"></a>Erhalten eines barrierefreien Objekt Schnittstellen Zeigers

Microsoft Active Accessibility-Client Anwendungen rufen Schnittstellen Zeiger auf barrierefreie Objekte ab, indem Sie eine der folgenden Funktionen verwenden.

**Accessibleobjectfromevent**

Viele Clients suchen Informationen zu bestimmten zugänglichen Objekten, die Ereignisse generieren. Da es sich bei der [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle um das "Gateway" für barrierefreie Objekte handelt, müssen Clients eine einfache Möglichkeit aufweisen, um [WinEvents](winevents-overview.md) die **IAccessible** -Schnittstelle des Objekts zuzuordnen, das die Ereignisse erzeugt. Microsoft Active Accessibility stellt die [**accessibleobjectfromevent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) -Funktion speziell für diesen Zweck bereit.

> [!Note]  
> Clients mit [in-context-Hookfunktionen](in-context-hook-functions.md) müssen die [IsWindow](/windows/win32/api/winuser/nf-winuser-iswindow) -Funktion vor dem Aufruf von [**accessibleobjectfromevent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)aufrufen.

 

Die [**accessibleobjectfromevent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) -Funktion akzeptiert einen Großteil der Informationen, die die [*Hook-Funktion*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) eines Clients empfängt. Wenn eine clienthookfunktion eine Ereignis Benachrichtigung empfängt, übergibt Sie die entsprechenden Parameter aus den Ereignissen an **accessibleobjectfromevent**.

Die-Funktion ruft entweder die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle des Benutzeroberflächen Elements ab, das das Ereignis generiert hat, oder die-Schnittstelle des übergeordneten Objekts des Elements. Wenn der Schnittstellen Zeiger des übergeordneten Objekts zurückgegeben wird, ruft der Client die Eigenschaften und Methoden des übergeordneten Objekts auf, um Informationen über das untergeordnete Element abzurufen, das das Ereignis generiert hat.

**Accessibleobjectfrompoint**

Um die Adresse der [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle eines Objekts an einem angegebenen Punkt auf dem Bildschirm abzurufen, verwenden die Clients die [**accessibleobjectfrompoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) -Funktion.

**Accessibleobjectfromwindow**

Um die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle eines Objekts von einem Fenster Handle abzurufen, verwenden Clients die [**accessibleobjectfromwindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) -Funktion.

Es ist möglich, dass Server jedes Mal, wenn die Funktion [**accessibleobjectfromevent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent), [**accessibleobjectfrompoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)oder [**accessibleobjectfromwindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) aufgerufen wird, unterschiedliche Schnittstellen Zeiger für dasselbe Benutzeroberflächen Element zurückgeben. Um zu ermitteln, ob zwei Zeiger auf dasselbe Benutzeroberflächen Element verweisen, müssen Client Entwickler [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften des Objekts und nicht Zeiger vergleichen.

 

 
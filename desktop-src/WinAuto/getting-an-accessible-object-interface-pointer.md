---
title: Abrufen eines Barrierefreien Objektschnittstellenzeigers
description: Microsoft Active Accessibility Clientanwendungen mithilfe einer der folgenden Funktionen Schnittstellenzeker auf barrierefreie Objekte abrufen.
ms.assetid: b82467f0-0d46-482a-8f6d-ad64f236601e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28ea0d7936671a68c140c6d22fdc3afdad0db0899c9c2cbc51637dcf36d9ad55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994200"
---
# <a name="getting-an-accessible-object-interface-pointer"></a>Abrufen eines Barrierefreien Objektschnittstellenzeigers

Microsoft Active Accessibility Clientanwendungen mithilfe einer der folgenden Funktionen Schnittstellenzeker auf barrierefreie Objekte abrufen.

**AccessibleObjectFromEvent**

Viele Clients suchen Informationen zu bestimmten barrierefreien Objekten, die Ereignisse generieren. Da die IAccessible-Schnittstelle das "Gateway" für barrierefreie Objekte ist, müssen Clients eine einfache Möglichkeit haben, [WinEvents](winevents-overview.md) der [**IAccessible-Schnittstelle**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) des Objekts zu zuordnen, das die Ereignisse generiert.  Microsoft Active Accessibility stellt die [**AccessibleObjectFromEvent-Funktion**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) speziell für diesen Zweck zur Verfügung.

> [!Note]  
> Clients mit [kontextspezifischen Hookfunktionen](in-context-hook-functions.md) müssen die [IsWindow-Funktion aufrufen,](/windows/win32/api/winuser/nf-winuser-iswindow) bevor [**AccessibleObjectFromEvent aufgerufen wird.**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)

 

Die [**AccessibleObjectFromEvent-Funktion**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) akzeptiert einen Großen Teil der Informationen, die die Hookfunktion eines [*Clients*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) empfängt. Wenn eine Clienthookfunktion eine Ereignisbenachrichtigung empfängt, übergibt sie die entsprechenden Parameter von Ereignissen an **AccessibleObjectFromEvent.**

Die Funktion ruft entweder die [**IAccessible-Schnittstelle**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) des Benutzeroberflächenelements ab, das das Ereignis generiert hat, oder die Schnittstelle des übergeordneten Objekts des Elements. Wenn der Schnittstellenzeiger des übergeordneten Objekts zurückgegeben wird, ruft der Client die Eigenschaften und Methoden des übergeordneten Objekts auf, um Informationen über das untergeordnete Element zu erhalten, das das Ereignis generiert hat.

**AccessibleObjectFromPoint**

Um die Adresse der [**IAccessible-Schnittstelle**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) eines Objekts an einem angegebenen Punkt auf dem Bildschirm abzurufen, verwenden Clients die [**AccessibleObjectFromPoint-Funktion.**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)

**AccessibleObjectFromWindow**

Um die [**IAccessible-Schnittstelle**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) eines Objekts aus einem Fensterhand handle abzurufen, verwenden Clients die [**AccessibleObjectFromWindow-Funktion.**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)

Es ist möglich, dass Server bei jedem Aufrufen der [**AccessibleObjectFromEvent-,**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) [**AccessibleObjectFromPoint-**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)oder [**AccessibleObjectFromWindow-Funktion**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) unterschiedliche Schnittstellenze0er für dasselbe Benutzeroberflächenelement zurückgeben. Um zu bestimmen, ob zwei Zeiger auf dasselbe Benutzeroberflächenelement verweisen, müssen Cliententwickler [**IAccessible-Eigenschaften**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) des Objekts vergleichen, nicht Zeiger.

 

 
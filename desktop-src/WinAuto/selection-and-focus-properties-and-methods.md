---
title: Auswahl- und Fokuseigenschaften und -methoden
description: Wie viele Elemente in Anwendungen, die unter Microsoft Windows betriebssystemen ausgeführt werden, wählen barrierefreie Objekte den Tastaturfokus aus und erhalten diesen. Mit diesen Attributen können Benutzer mit Anwendungselementen interagieren, Werte ändern und anderweitig bearbeiten.
ms.assetid: 8170fe19-f157-4d7d-8eec-d384e51f1560
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bf5c5bc4a60e664c124e7181f998d9e0a7af6ab82ef9b2d4f030f7541d530ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117745229"
---
# <a name="selection-and-focus-properties-and-methods"></a>Auswahl- und Fokuseigenschaften und -methoden

Wie viele Elemente in Anwendungen, die unter Microsoft Windows-Betriebssystemen ausgeführt werden, wählen barrierefreie Objekte *den* Tastaturfokus aus und *erhalten diesen.* Mit diesen Attributen können Benutzer mit Anwendungselementen interagieren, Werte ändern und anderweitig bearbeiten.

Es gibt einige wichtige Unterschiede zwischen der Objektauswahl und dem Objektfokus:

-   Ein fokussiertes Objekt ist das einzige Objekt im gesamten Betriebssystem, das Tastatureingaben empfängt. Das Objekt mit dem Tastaturfokus ist entweder das aktive Fenster oder ein untergeordnetes Objekt des aktiven Fensters.
-   Ein ausgewähltes Objekt ist für die Teilnahme an einem Gruppenvorgang markiert.

Beispielsweise kann ein Benutzer mehrere Elemente in einem Listenansicht-Steuerelement auswählen, aber der Fokus wird nur einem Objekt im System gleichzeitig erteilt. Beachten Sie, dass fokussierte Elemente aus einer Auswahl von Elementen sind.

Clients bestimmen, ob ein bestimmtes barrierefreies Objekt oder untergeordnetes Element den Fokus besitzt, indem [**sie IAccessible::get \_ accFocus aufrufen.**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus) Clients bestimmen durch Aufrufen von [**IAccessible::get \_ accSelection,**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)ob ein Objekt ausgewählt ist oder welche elemente in einem barrierefreien Objekt ausgewählt sind. Für Objekte wie Listenansichtssteuerelemente, in denen mehr als ein untergeordnetes Element ausgewählt ist, muss das übergeordnete Objekt die [IEnumVARIANT-Schnittstelle](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) unterstützen, mit der Clients die ausgewählten untergeordneten Elemente auflisten können.

## <a name="events-triggered-in-menus"></a>In Menüs ausgelöste Ereignisse

Microsoft Active Accessibility werden Standardmenüs verfügbar, die mit den Microsoft Win32-Menü-APIs und Ressourcendateien erstellt wurden. Um mit Standardmenüs konsistent zu sein, lösen Server mit benutzerdefinierten Menüs [**EVENT \_ OBJECT \_ FOCUS**](event-constants.md)und nicht [**EVENT OBJECT \_ \_ SELECTION**](event-constants.md)aus, wenn ein Benutzer ein Menüelement hervor hebt.

> [!Note]  
> Microsoft Active Accessibility unterstützt nicht die Auswahl des Texts, der in Bearbeitungs- und Rich Edit-Steuerelementen enthalten ist, da der Text als einzelne Zeichenfolge in der [**Value-Eigenschaft**](value-property.md) für diese Steuerelemente verfügbar gemacht wird.

 

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Auswählen von untergeordneten Objekten](selecting-child-objects.md)

 

 
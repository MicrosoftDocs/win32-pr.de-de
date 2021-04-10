---
title: Auswahl-und Fokus Eigenschaften und-Methoden
description: Wie viele Elemente in Anwendungen, die unter Microsoft Windows-Betriebssystemen ausgeführt werden, können barrierefreie Objekte den Tastaturfokus auswählen und erhalten. Diese Attribute ermöglichen es Benutzern, mit Anwendungs Elementen zu interagieren, Werte zu ändern und Sie anderweitig zu bearbeiten.
ms.assetid: 8170fe19-f157-4d7d-8eec-d384e51f1560
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bbb5eee361707ec4876245eef5b0eb352f8dfd6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728432"
---
# <a name="selection-and-focus-properties-and-methods"></a>Auswahl-und Fokus Eigenschaften und-Methoden

Wie viele Elemente in Anwendungen, die unter Microsoft Windows-Betriebssystemen ausgeführt werden, können barrierefreie Objekte den Tastatur *Fokus* *auswählen* und erhalten. Diese Attribute ermöglichen es Benutzern, mit Anwendungs Elementen zu interagieren, Werte zu ändern und Sie anderweitig zu bearbeiten.

Es gibt einige wichtige Unterschiede zwischen der Objektauswahl und dem Objekt Fokus:

-   Ein Objekt mit Fokus ist das einzige Objekt im gesamten Betriebssystem, das Tastatureingaben empfängt. Das Objekt mit dem Tastaturfokus ist entweder das aktive Fenster oder ein untergeordnetes Objekt des aktiven Fensters.
-   Ein ausgewähltes Objekt ist so gekennzeichnet, dass es an einer Art von Gruppen Vorgang beteiligt ist.

Beispielsweise kann ein Benutzer mehrere Elemente in einem Listenansicht-Steuerelement auswählen, aber der Fokus wird nur jeweils einem Objekt im System zugewiesen. Beachten Sie, dass fokussierte Elemente aus einer Auswahl von Elementen stammen.

Clients bestimmen, ob ein bestimmtes Barrierefreies Objekt oder ein bestimmtes untergeordnetes Element den Fokus besitzt, indem [**IAccessible:: get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)aufgerufen wird. Clients bestimmen, ob ein Objekt ausgewählt ist oder welche untergeordneten Elemente in einem zugänglichen Objekt ausgewählt werden, indem Sie [**IAccessible:: get \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)aufrufen. Für Objekte, wie z. b. Listenansicht-Steuerelemente, in denen mehrere untergeordnete Elemente ausgewählt sind, muss das übergeordnete Objekt die [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle unterstützen, sodass Clients die ausgewählten untergeordneten Elemente aufzählen können.

## <a name="events-triggered-in-menus"></a>Ausgelöste Ereignisse in Menüs

Microsoft Active Accessibility macht Standardmenüs verfügbar, die mit den Microsoft Win32-Menü-APIs und Ressourcen Dateien erstellt wurden. Um mit Standardmenüs konsistent zu sein, werden Server mit benutzerdefinierten Menüs [**Ereignis \_ Objekt \_ Fokus**](event-constants.md)und nicht [**Ereignis \_ Objekt \_ Auswahl**](event-constants.md), wenn ein Benutzer ein Menü Element hervorhebt.

> [!Note]  
> Microsoft Active Accessibility unterstützt nicht die Auswahl des Texts, der in Edit-und Rich Edit-Steuerelementen enthalten ist, da der Text als eine einzelne Zeichenfolge in der [**value**](value-property.md) -Eigenschaft für diese Steuerelemente verfügbar gemacht wird.

 

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Auswählen von untergeordneten Objekten](selecting-child-objects.md)

 

 
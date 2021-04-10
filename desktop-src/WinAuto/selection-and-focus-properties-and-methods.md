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
# <a name="selection-and-focus-properties-and-methods"></a><span data-ttu-id="bc286-104">Auswahl-und Fokus Eigenschaften und-Methoden</span><span class="sxs-lookup"><span data-stu-id="bc286-104">Selection and Focus Properties and Methods</span></span>

<span data-ttu-id="bc286-105">Wie viele Elemente in Anwendungen, die unter Microsoft Windows-Betriebssystemen ausgeführt werden, können barrierefreie Objekte den Tastatur *Fokus* *auswählen* und erhalten.</span><span class="sxs-lookup"><span data-stu-id="bc286-105">Like many elements in applications running on Microsoft Windows operating systems, accessible objects *select* and receive keyboard *focus*.</span></span> <span data-ttu-id="bc286-106">Diese Attribute ermöglichen es Benutzern, mit Anwendungs Elementen zu interagieren, Werte zu ändern und Sie anderweitig zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="bc286-106">These attributes enable users to interact with application elements, change values, and otherwise manipulate them.</span></span>

<span data-ttu-id="bc286-107">Es gibt einige wichtige Unterschiede zwischen der Objektauswahl und dem Objekt Fokus:</span><span class="sxs-lookup"><span data-stu-id="bc286-107">There are some key differences between object selection and object focus:</span></span>

-   <span data-ttu-id="bc286-108">Ein Objekt mit Fokus ist das einzige Objekt im gesamten Betriebssystem, das Tastatureingaben empfängt.</span><span class="sxs-lookup"><span data-stu-id="bc286-108">A focused object is the one object in the entire operating system that receives keyboard input.</span></span> <span data-ttu-id="bc286-109">Das Objekt mit dem Tastaturfokus ist entweder das aktive Fenster oder ein untergeordnetes Objekt des aktiven Fensters.</span><span class="sxs-lookup"><span data-stu-id="bc286-109">The object with the keyboard focus is either the active window or a child object of the active window.</span></span>
-   <span data-ttu-id="bc286-110">Ein ausgewähltes Objekt ist so gekennzeichnet, dass es an einer Art von Gruppen Vorgang beteiligt ist.</span><span class="sxs-lookup"><span data-stu-id="bc286-110">A selected object is marked to participate in some type of group operation.</span></span>

<span data-ttu-id="bc286-111">Beispielsweise kann ein Benutzer mehrere Elemente in einem Listenansicht-Steuerelement auswählen, aber der Fokus wird nur jeweils einem Objekt im System zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="bc286-111">For example, a user can select several items in a list-view control, but the focus is given only to one object in the system at a time.</span></span> <span data-ttu-id="bc286-112">Beachten Sie, dass fokussierte Elemente aus einer Auswahl von Elementen stammen.</span><span class="sxs-lookup"><span data-stu-id="bc286-112">Note that focused items are from a selection of items.</span></span>

<span data-ttu-id="bc286-113">Clients bestimmen, ob ein bestimmtes Barrierefreies Objekt oder ein bestimmtes untergeordnetes Element den Fokus besitzt, indem [**IAccessible:: get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="bc286-113">Clients determine whether a particular accessible object or child element has the focus by calling [**IAccessible::get\_accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus).</span></span> <span data-ttu-id="bc286-114">Clients bestimmen, ob ein Objekt ausgewählt ist oder welche untergeordneten Elemente in einem zugänglichen Objekt ausgewählt werden, indem Sie [**IAccessible:: get \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="bc286-114">Clients determine whether an object is selected, or which children within an accessible object are selected, by calling [**IAccessible::get\_accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection).</span></span> <span data-ttu-id="bc286-115">Für Objekte, wie z. b. Listenansicht-Steuerelemente, in denen mehrere untergeordnete Elemente ausgewählt sind, muss das übergeordnete Objekt die [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle unterstützen, sodass Clients die ausgewählten untergeordneten Elemente aufzählen können.</span><span class="sxs-lookup"><span data-stu-id="bc286-115">For objects such as list-view controls in which more than one child is selected, the parent object must support the [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface, which allows clients to enumerate the selected children.</span></span>

## <a name="events-triggered-in-menus"></a><span data-ttu-id="bc286-116">Ausgelöste Ereignisse in Menüs</span><span class="sxs-lookup"><span data-stu-id="bc286-116">Events Triggered in Menus</span></span>

<span data-ttu-id="bc286-117">Microsoft Active Accessibility macht Standardmenüs verfügbar, die mit den Microsoft Win32-Menü-APIs und Ressourcen Dateien erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="bc286-117">Microsoft Active Accessibility exposes standard menus created with the Microsoft Win32 menu APIs and resource files.</span></span> <span data-ttu-id="bc286-118">Um mit Standardmenüs konsistent zu sein, werden Server mit benutzerdefinierten Menüs [**Ereignis \_ Objekt \_ Fokus**](event-constants.md)und nicht [**Ereignis \_ Objekt \_ Auswahl**](event-constants.md), wenn ein Benutzer ein Menü Element hervorhebt.</span><span class="sxs-lookup"><span data-stu-id="bc286-118">To be consistent with standard menus, servers with custom menus trigger [**EVENT\_OBJECT\_FOCUS**](event-constants.md), not [**EVENT\_OBJECT\_SELECTION**](event-constants.md), when a user highlights a menu item.</span></span>

> [!Note]  
> <span data-ttu-id="bc286-119">Microsoft Active Accessibility unterstützt nicht die Auswahl des Texts, der in Edit-und Rich Edit-Steuerelementen enthalten ist, da der Text als eine einzelne Zeichenfolge in der [**value**](value-property.md) -Eigenschaft für diese Steuerelemente verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="bc286-119">Microsoft Active Accessibility does not support the selection of the text contained in edit and rich edit controls because the text is exposed as a single string in the [**Value**](value-property.md) property for these controls.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="bc286-120">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="bc286-120">In this section</span></span>

-   [<span data-ttu-id="bc286-121">Auswählen von untergeordneten Objekten</span><span class="sxs-lookup"><span data-stu-id="bc286-121">Selecting Child Objects</span></span>](selecting-child-objects.md)

 

 
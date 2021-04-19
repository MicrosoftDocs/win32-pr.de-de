---
title: Einfache Elemente
description: Ein einfaches Element ist ein Benutzeroberflächen Element, das ein IAccessible-Objekt mit anderen Elementen gemeinsam nutzt und darauf basiert, dass dieses Objekt (in der Regel sein übergeordnetes Objekt) seine Eigenschaften verfügbar macht.
ms.assetid: 3f6bd992-4e0a-4dba-b6e9-e70dca77c880
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8f8cb00b19719a4a8779a61f37b079633ada40c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342084"
---
# <a name="simple-elements"></a><span data-ttu-id="1d9f4-103">Einfache Elemente</span><span class="sxs-lookup"><span data-stu-id="1d9f4-103">Simple Elements</span></span>

<span data-ttu-id="1d9f4-104">Ein *einfaches Element* ist ein Benutzeroberflächen Element, das ein [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Objekt mit anderen Elementen gemeinsam nutzt und darauf basiert, dass dieses Objekt (in der Regel sein übergeordnetes Objekt) seine **Eigenschaften verfügbar macht** .</span><span class="sxs-lookup"><span data-stu-id="1d9f4-104">A *simple element* is a UI element that shares an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object with other elements and relies on that **IAccessible** object (typically its parent) to expose its properties.</span></span> <span data-ttu-id="1d9f4-105">Um die Elemente zu unterscheiden, die ein **IAccessible** -Objekt gemeinsam nutzen, weist der Server jedem einfachen Element einen eindeutigen, positiven untergeordneten Bezeichner zu.</span><span class="sxs-lookup"><span data-stu-id="1d9f4-105">To differentiate between the elements sharing an **IAccessible** object, the server assigns a unique, positive child identifier to each simple element.</span></span> <span data-ttu-id="1d9f4-106">Diese Zuweisung erfolgt auf der Basis einer Schnittstelle pro Instanz, sodass die IDs innerhalb dieses Kontexts eindeutig sein müssen.</span><span class="sxs-lookup"><span data-stu-id="1d9f4-106">This assignment is done on a per-instance-of-interface basis, so the IDs must be unique within that context.</span></span> <span data-ttu-id="1d9f4-107">Viele Implementierungen weisen diese IDs sequenziell zu, beginnend mit 1.</span><span class="sxs-lookup"><span data-stu-id="1d9f4-107">Many implementations assign these IDs sequentially, beginning with 1.</span></span> <span data-ttu-id="1d9f4-108">Mit diesem Schema können einfache Elemente keine eigenen Elemente besitzen.</span><span class="sxs-lookup"><span data-stu-id="1d9f4-108">This scheme does not allow simple elements to have children of their own.</span></span> <span data-ttu-id="1d9f4-109">Einfache Elemente werden *auch als unter* geordnete Elemente bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="1d9f4-109">Simple elements are also known as *children*.</span></span>

<span data-ttu-id="1d9f4-110">Für ein einfaches Element, das eindeutig identifiziert und verfügbar gemacht werden muss, [**ist ein einfaches**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Element erforderlich</span><span class="sxs-lookup"><span data-stu-id="1d9f4-110">To be uniquely identified and exposed, a simple element requires an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object and child ID.</span></span> <span data-ttu-id="1d9f4-111">Daher müssen die Clients bei der Kommunikation mit einem Objekt, das nicht **zugänglich** ist, die entsprechende untergeordnete ID angeben.</span><span class="sxs-lookup"><span data-stu-id="1d9f4-111">Therefore, when communicating with an **IAccessible** object, the clients must supply the appropriate child ID.</span></span> <span data-ttu-id="1d9f4-112">Ein spezieller Bezeichner, " **childID \_ Self**", kann verwendet werden, um auf das barrierefreie Objekt selbst zu verweisen, statt eines seiner untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="1d9f4-112">A special identifier, **CHILDID\_SELF**, can be used to refer to the accessible object itself, instead of one of its children.</span></span>

<span data-ttu-id="1d9f4-113">Das [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Objekt, das von einfachen Elementen gemeinsam genutzt wird, entspricht häufig einem gemeinsamen übergeordneten Objekt in der Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="1d9f4-113">The [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object shared among simple elements often corresponds to a common parent object in the user interface.</span></span> <span data-ttu-id="1d9f4-114">So machen z. b. System Listenfelder ein Barrierefreies Objekt für das allgemeine Listenfeld und einfache Elemente für jedes Listenfeld Element verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1d9f4-114">For example, system list boxes expose an accessible object for the overall list box and simple elements for each list box item.</span></span> <span data-ttu-id="1d9f4-115">In diesem Fall ist das **IAccessible** -Objekt für das Listenfeld auch das übergeordnete Element oder der Container der Listenelemente.</span><span class="sxs-lookup"><span data-stu-id="1d9f4-115">In this case, the **IAccessible** object for the list box is also the parent or container of the list items.</span></span>

<span data-ttu-id="1d9f4-116">Weitere Informationen zu zugänglichen Objekten finden Sie unter [barrierefreie Objekte](accessible-objects.md).</span><span class="sxs-lookup"><span data-stu-id="1d9f4-116">For more information about accessible objects, see [Accessible Objects](accessible-objects.md).</span></span>

 

 





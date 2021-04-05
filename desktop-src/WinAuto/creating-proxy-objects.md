---
title: Erstellen von Proxy Objekten
description: Zusätzlich zum Entwerfen von Klassen, die Eigenschaften und Methoden von IAccessible implementieren, müssen Server Entwickler möglicherweise auch Proxy Objekte entwerfen, die die Lebensdauer von zugänglichen Objekten überwachen.
ms.assetid: d140206a-9918-438b-96bd-df141da2f04b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e005af4f02430376bc013a45c68cdecef8c0feba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708555"
---
# <a name="creating-proxy-objects"></a><span data-ttu-id="fb74c-103">Erstellen von Proxy Objekten</span><span class="sxs-lookup"><span data-stu-id="fb74c-103">Creating Proxy Objects</span></span>

<span data-ttu-id="fb74c-104">Zusätzlich zum Entwerfen von Klassen, die Eigenschaften und Methoden von [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementieren, müssen Server Entwickler möglicherweise auch *Proxy* Objekte entwerfen, die die Lebensdauer von zugänglichen Objekten überwachen.</span><span class="sxs-lookup"><span data-stu-id="fb74c-104">In addition to designing classes that implement [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods, server developers may also need to design *proxy* objects that monitor the life span of accessible objects.</span></span> <span data-ttu-id="fb74c-105">Wenn ein Barrierefreies Objekt in einer Anwendung für den gesamten Zeitpunkt verfügbar ist, an dem die Anwendung ausgeführt wird, müssen Sie kein Proxy Objekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="fb74c-105">If an accessible object in an application is available the entire time the application is running, then you do not need to create a proxy object.</span></span> <span data-ttu-id="fb74c-106">Wenn es möglich ist, das barrierefreie Objekt zu zerstören, während die Anwendung ausgeführt wird, müssen Sie ein Proxy Objekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="fb74c-106">If it is possible to destroy the accessible object while the application is running, then you must create a proxy object.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="fb74c-107">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="fb74c-107">In this section</span></span>

-   [<span data-ttu-id="fb74c-108">Was sind Proxy Objekte?</span><span class="sxs-lookup"><span data-stu-id="fb74c-108">What Are Proxy Objects?</span></span>](what-are-proxy-objects.md)
-   [<span data-ttu-id="fb74c-109">Warum Proxy Objekte erforderlich sind</span><span class="sxs-lookup"><span data-stu-id="fb74c-109">Why Proxy Objects Are Needed</span></span>](why-proxy-objects-are-needed.md)
-   [<span data-ttu-id="fb74c-110">Entwurfs Überlegungen für Proxy Objekte</span><span class="sxs-lookup"><span data-stu-id="fb74c-110">Design Considerations for Proxy Objects</span></span>](design-considerations-for-proxy-objects.md)

 

 





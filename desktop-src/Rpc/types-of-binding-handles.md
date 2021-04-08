---
title: Typen von Bindungs Handles
description: Bindungs Handles können automatisch, implizit oder explizit sein.
ms.assetid: 7f026199-6045-4f60-9002-543636cf6275
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60a09b858dfc677d06cf5885dc7a5f7a6ba599eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037324"
---
# <a name="types-of-binding-handles"></a><span data-ttu-id="d4af2-103">Typen von Bindungs Handles</span><span class="sxs-lookup"><span data-stu-id="d4af2-103">Types of Binding Handles</span></span>

<span data-ttu-id="d4af2-104">Bindungs Handles können automatisch, implizit oder explizit sein.</span><span class="sxs-lookup"><span data-stu-id="d4af2-104">Binding handles can be automatic, implicit, or explicit.</span></span> <span data-ttu-id="d4af2-105">Sie unterscheiden sich in der Steuerungs Menge, die die Anwendung über den Bindungsprozess verfügt.</span><span class="sxs-lookup"><span data-stu-id="d4af2-105">They differ in the amount of control the application has over the binding process.</span></span> <span data-ttu-id="d4af2-106">Wie der Name bereits vermuten lässt, verarbeitet die automatische Bindung die automatisierte Bindung.</span><span class="sxs-lookup"><span data-stu-id="d4af2-106">As the name suggests, automatic binding handles automate binding.</span></span> <span data-ttu-id="d4af2-107">Die Client-und Server Anwendungen benötigen keinen Code, um den Bindungsprozess zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="d4af2-107">The client and server applications do not need code to handle the binding process.</span></span> <span data-ttu-id="d4af2-108">Mit impliziten Bindungs Handles können Client Programme das Bindungs handle konfigurieren, bevor die Bindung stattfindet.</span><span class="sxs-lookup"><span data-stu-id="d4af2-108">Implicit binding handles allow client programs to configure the binding handle before the binding takes place.</span></span> <span data-ttu-id="d4af2-109">Nachdem der Client eine Bindung eingerichtet hat, verarbeitet die RPC-Lauf Zeit Bibliothek den Rest.</span><span class="sxs-lookup"><span data-stu-id="d4af2-109">After the client establishes a binding, the RPC run-time library handles the rest.</span></span> <span data-ttu-id="d4af2-110">Explizite Bindungs Handles verschieben die gesamte Kontrolle über den Bindungsprozess in den Quellcode des Clients und der Serverprogramme.</span><span class="sxs-lookup"><span data-stu-id="d4af2-110">Explicit binding handles move complete control over the binding process into the source code of the client and the server programs.</span></span> <span data-ttu-id="d4af2-111">Mit diesem Steuerelement kommt es zu erhöhter Komplexität.</span><span class="sxs-lookup"><span data-stu-id="d4af2-111">With this control comes increased complexity.</span></span> <span data-ttu-id="d4af2-112">Die Anwendung muss RPC-Funktionen zum Verwalten der Bindung abrufen.</span><span class="sxs-lookup"><span data-stu-id="d4af2-112">Your application must call RPC functions to manage the binding.</span></span> <span data-ttu-id="d4af2-113">Dies geschieht nicht automatisch.</span><span class="sxs-lookup"><span data-stu-id="d4af2-113">It does not happen automatically.</span></span> <span data-ttu-id="d4af2-114">Es werden explizite Bindungs Handles empfohlen.</span><span class="sxs-lookup"><span data-stu-id="d4af2-114">Explicit binding handles are recommended.</span></span>

<span data-ttu-id="d4af2-115">Im folgenden Diagramm werden die Unterschiede zwischen automatischen, impliziten und expliziten Bindungs Handles veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="d4af2-115">The following diagram illustrates the differences between automatic, implicit, and explicit binding handles.</span></span>

![Unterschiede zwischen automatischen, impliziten und expliziten Bindungs Handles](images/bhand.png)

<span data-ttu-id="d4af2-117">Außerdem ist jedes Bindungs handle entweder primitiv oder Benutzer definiert.</span><span class="sxs-lookup"><span data-stu-id="d4af2-117">In addition, every binding handle is either primitive or custom.</span></span> <span data-ttu-id="d4af2-118">In den folgenden Themen wird jeder Typ von Bindungs handle erläutert:</span><span class="sxs-lookup"><span data-stu-id="d4af2-118">Each type of binding handle is discussed in the following topics:</span></span>

-   [<span data-ttu-id="d4af2-119">Automatische Bindungs Handles</span><span class="sxs-lookup"><span data-stu-id="d4af2-119">Automatic Binding Handles</span></span>](automatic-binding-handles.md)
-   [<span data-ttu-id="d4af2-120">Implizite Bindungs Handles</span><span class="sxs-lookup"><span data-stu-id="d4af2-120">Implicit Binding Handles</span></span>](implicit-binding-handles.md)
-   [<span data-ttu-id="d4af2-121">Explizite Bindungs Handles</span><span class="sxs-lookup"><span data-stu-id="d4af2-121">Explicit Binding Handles</span></span>](explicit-binding-handles.md)
-   [<span data-ttu-id="d4af2-122">Primitive und benutzerdefinierte Bindungs Handles</span><span class="sxs-lookup"><span data-stu-id="d4af2-122">Primitive and Custom Binding Handles</span></span>](primitive-and-custom-binding-handles.md)

 

 





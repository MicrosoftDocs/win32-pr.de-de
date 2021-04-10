---
description: In TSPI werden nicht transparente Handles verwendet, um auf die Datenstrukturen zu verweisen, die Linien, Telefone und Aufrufe darstellen.
ms.assetid: aa1742aa-6cd4-461a-ad92-972eefcf637f
title: Nicht transparente Handles und private Datenstrukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2cd8c7b911de5f85f84b56a8e25e28eb805c5bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959103"
---
# <a name="opaque-handles-and-private-data-structures"></a><span data-ttu-id="b95ae-103">Nicht transparente Handles und private Datenstrukturen</span><span class="sxs-lookup"><span data-stu-id="b95ae-103">Opaque Handles and Private Data Structures</span></span>

<span data-ttu-id="b95ae-104">In TSPI werden nicht transparente Handles verwendet, um auf die Datenstrukturen zu verweisen, die Linien, Telefone und Aufrufe darstellen.</span><span class="sxs-lookup"><span data-stu-id="b95ae-104">Opaque handles are used in TSPI to refer to the data structures representing lines, phones, and call appearances.</span></span> <span data-ttu-id="b95ae-105">Diese werden als Parameter für die meisten Funktionen und Rückrufe angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b95ae-105">These appear as parameters to most of the functions and callbacks.</span></span> <span data-ttu-id="b95ae-106">Es gibt nur wenige Funktionen, die auf das Gerät mit einem Geräte Bezeichner anstelle eines opaken Handles verweisen.</span><span class="sxs-lookup"><span data-stu-id="b95ae-106">There are few functions that refer to the device using a device identifier instead of an opaque handle.</span></span> <span data-ttu-id="b95ae-107">In einem solchen Fall bezieht sich der Verweis auf das Gerät selbst und nicht auf eine Datenstruktur.</span><span class="sxs-lookup"><span data-stu-id="b95ae-107">In such a case, the reference is to the device itself rather than to a data structure.</span></span> <span data-ttu-id="b95ae-108">Funktionen, die auf diese Weise funktionieren, sind in der Regel jene, die zu frühen Initialisierungs Zeiten aufgerufen werden, bevor Datenstrukturen erstellt und nicht transparente Handles ausgetauscht werden.</span><span class="sxs-lookup"><span data-stu-id="b95ae-108">Functions that work in this fashion are typically those called at early initialization times before data structures are created and opaque handles are exchanged.</span></span>

<span data-ttu-id="b95ae-109">Der Dienstanbieter muss entscheiden, wie diese Handles interpretiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b95ae-109">The service provider must decide how to interpret these handles.</span></span> <span data-ttu-id="b95ae-110">Ein Dienstanbieter verwendet in der Regel den Zeiger auf seine Datenstruktur oder den Index in ein Array von Datenstrukturen als undurchsichtiges handle.</span><span class="sxs-lookup"><span data-stu-id="b95ae-110">A service provider typically uses the pointer to its data structure or to the index into an array of data structures as its opaque handle.</span></span> <span data-ttu-id="b95ae-111">Die einzige Einschränkung besteht darin, dass der Dienstanbieter den Wert 0 nicht als [hdrvline](hdrvline.md), hdrvcalloder [hdrvphone](hdrvphone.md)verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="b95ae-111">The only restriction is that the service provider cannot use the value 0 as an [HDRVLINE](hdrvline.md), HDRVCALL, or [HDRVPHONE](hdrvphone.md).</span></span> <span data-ttu-id="b95ae-112">Der Wert 0 oder **null** für ein Handle hat in einigen Vorgängen eine besondere Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="b95ae-112">The value 0 or **NULL** for a handle has a special meaning in some operations.</span></span>

 

 




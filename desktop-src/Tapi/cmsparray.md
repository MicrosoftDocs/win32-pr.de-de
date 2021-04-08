---
description: Die cmsparray-Vorlage implementiert ein intelligentes Array, das Bedarfs gesteuert vergrößert wird.
ms.assetid: 9b30885c-01a4-4aea-a1c3-5d7966e4697f
title: Cmsparray
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a6c14d4bdc0b57a295efa5bcc2adfd79d23d31d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959849"
---
# <a name="cmsparray"></a><span data-ttu-id="558d0-103">Cmsparray</span><span class="sxs-lookup"><span data-stu-id="558d0-103">CMSPArray</span></span>

<span data-ttu-id="558d0-104">Die cmsparray-Vorlage implementiert ein intelligentes Array, das Bedarfs gesteuert vergrößert wird.</span><span class="sxs-lookup"><span data-stu-id="558d0-104">The CMSPArray template implements a smart array that will grow on demand.</span></span> <span data-ttu-id="558d0-105">Es ist so konzipiert, dass kleine Arrays mit einfachen Datentypen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="558d0-105">It is designed to hold small arrays with simple data types.</span></span> <span data-ttu-id="558d0-106">Es weist keinen kritischen Abschnitt auf.</span><span class="sxs-lookup"><span data-stu-id="558d0-106">It doesn't have a critical section.</span></span> <span data-ttu-id="558d0-107">Die einzigen Abhängigkeiten sind **rezuzuweisungen** und **memmove**.</span><span class="sxs-lookup"><span data-stu-id="558d0-107">Its only dependencies are **realloc** and **memmove**.</span></span> <span data-ttu-id="558d0-108">Sie wird intern verwendet, um Listen von Objekt Zeigern beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="558d0-108">It is used internally to keep lists of object pointers.</span></span> <span data-ttu-id="558d0-109">Sie ähnelt der **CSimpleArray** -Implementierung von ATL, ist aber für anfängliche Zuordnungen effizienter.</span><span class="sxs-lookup"><span data-stu-id="558d0-109">It is similar to ATL's **CSimpleArray** implementation, but it is more efficient for initial allocations.</span></span>

<span data-ttu-id="558d0-110">Diese Vorlage ist in "msputils. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="558d0-110">This template is defined in MSPutils.h.</span></span>

 

 




---
description: In diesem Abschnitt werden Probleme aufgelistet, die bei der Arbeit mit Direct3D 9 für Treiber auftreten können, die für frühere Versionen von Direct3D als Direct3D 9 geschrieben wurden.
ms.assetid: 891198e8-6c45-4f03-99bb-e24a4082b0d8
title: Arbeiten mit früheren Treibern (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76567bc4778924835e20a476b03dc94ea77739fd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392413"
---
# <a name="working-with-earlier-drivers-direct3d-9"></a><span data-ttu-id="e30a5-103">Arbeiten mit früheren Treibern (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e30a5-103">Working with Earlier Drivers (Direct3D 9)</span></span>

<span data-ttu-id="e30a5-104">In diesem Abschnitt werden Probleme aufgelistet, die bei der Arbeit mit Direct3D 9 für Treiber auftreten können, die für frühere Versionen von Direct3D als Direct3D 9 geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="e30a5-104">This section lists issues that can be encountered when working with Direct3D 9 on drivers written for versions of Direct3D earlier than Direct3D 9.</span></span>

-   <span data-ttu-id="e30a5-105">Beim Arbeiten mit einem T&L HAL-Gerät wird die Nebel Intensität berechnet, aber der absolute Wert Vorgang wird nicht auf diesen Wert angewendet.</span><span class="sxs-lookup"><span data-stu-id="e30a5-105">When working with a T&L HAL device, the fog intensity is computed but the absolute value operation is not applied to this value.</span></span> <span data-ttu-id="e30a5-106">Stattdessen bleibt der Wert negativ, wenn dies der berechnete Wert ist.</span><span class="sxs-lookup"><span data-stu-id="e30a5-106">Rather, the value is left negative if that is what is computed.</span></span> <span data-ttu-id="e30a5-107">Die beste Möglichkeit, diese Situation zu vermeiden, ist die angemessene Einrichtung von Transformationen.</span><span class="sxs-lookup"><span data-stu-id="e30a5-107">The best way to avoid this situation is to set up transforms appropriately.</span></span> <span data-ttu-id="e30a5-108">Eine weniger bevorzugte Methode besteht darin, die Werte für "Nebel Start" und "Nebel" zu ändern, um Sie abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="e30a5-108">A less-preferred method is to make the fog-start and fog-end values negative to match.</span></span>

<span data-ttu-id="e30a5-109">Um nach einem Direct3D 9-Treiber zu suchen, suchen Sie im DevCaps2-Member von D3DCAPS9 nach einem Wert ungleich 0 (null) für D3DDEVCAPS2 \_ Streamoffset. [](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)</span><span class="sxs-lookup"><span data-stu-id="e30a5-109">To check for a Direct3D 9 driver, look for a nonzero value for D3DDEVCAPS2\_STREAMOFFSET in the DevCaps2 member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e30a5-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e30a5-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e30a5-111">Programmiertipps</span><span class="sxs-lookup"><span data-stu-id="e30a5-111">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 




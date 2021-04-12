---
description: Primitive, die sich teilweise innerhalb (oder ganz außerhalb) der ansichtsansicht befinden, können abgeschnitten werden, sodass nur der sichtbare Teil des primitiven gerendert wird.
ms.assetid: 096683a4-2d8f-49d3-b1a0-832150907f11
title: Primitiver Clipping-Zustand (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e5a305118d8db5c71e0e3cfa97132052777be68
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392885"
---
# <a name="primitive-clipping-state-direct3d-9"></a><span data-ttu-id="0a945-103">Primitiver Clipping-Zustand (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0a945-103">Primitive Clipping State (Direct3D 9)</span></span>

<span data-ttu-id="0a945-104">Primitive, die sich teilweise innerhalb (oder ganz außerhalb) der [ansichtsansicht](viewports-and-clipping.md) befinden, können abgeschnitten werden, sodass nur der sichtbare Teil des primitiven gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="0a945-104">Primitives that lie partially inside (or completely outside) the [view frustum](viewports-and-clipping.md) can be clipped so that only the visible portion of the primitive will be rendered.</span></span> <span data-ttu-id="0a945-105">Durch das Abschneiden wird der Arbeitsaufwand reduziert, der nur für die primitiven oder Teile eines primitiven erfolgt, die sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="0a945-105">Clipping reduces the amount of work that is done to only those primitives or portions of a primitive that will be visible.</span></span>

<span data-ttu-id="0a945-106">Um die Pipeline für das Abschneiden zu verwenden, legen Sie den D3DRS \_ Clipping-renderzustand auf **true** (den Standardwert) fest, um das Abschneiden zu aktivieren, oder auf **false** , um Direct3D Clipping zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="0a945-106">To use the pipeline for clipping, set the D3DRS\_CLIPPING render state to **TRUE** (the default value) to enable clipping, or to **FALSE** to disable Direct3D clipping.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0a945-107">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0a945-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a945-108">Rendering-Zustände</span><span class="sxs-lookup"><span data-stu-id="0a945-108">Render States</span></span>](render-states.md)
</dt> </dl>

 

 




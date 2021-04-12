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
# <a name="primitive-clipping-state-direct3d-9"></a>Primitiver Clipping-Zustand (Direct3D 9)

Primitive, die sich teilweise innerhalb (oder ganz außerhalb) der [ansichtsansicht](viewports-and-clipping.md) befinden, können abgeschnitten werden, sodass nur der sichtbare Teil des primitiven gerendert wird. Durch das Abschneiden wird der Arbeitsaufwand reduziert, der nur für die primitiven oder Teile eines primitiven erfolgt, die sichtbar sind.

Um die Pipeline für das Abschneiden zu verwenden, legen Sie den D3DRS \_ Clipping-renderzustand auf **true** (den Standardwert) fest, um das Abschneiden zu aktivieren, oder auf **false** , um Direct3D Clipping zu deaktivieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rendering-Zustände](render-states.md)
</dt> </dl>

 

 




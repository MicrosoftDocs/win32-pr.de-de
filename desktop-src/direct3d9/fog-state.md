---
description: Durch Nebeleffekte kann eine 3D-Szene mehr realistisch sein.
ms.assetid: 26fe4f7c-7bb3-4a52-b539-5de2b11256e9
title: Nebelzustand (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d3103cbbd3dfb220e2ddd75078040702fd7557
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392331"
---
# <a name="fog-state-direct3d-9"></a>Nebelzustand (Direct3D 9)

Durch Nebeleffekte kann eine 3D-Szene mehr realistisch sein. Sie können Nebeleffekte zum Simulieren von Nebel verwenden. Sie können auch die Klarheit einer Szene mit Distanz verringern. Dies spiegelt, was in der realen Welt passiert. Wenn Objekte vom Benutzer entfernter werden, sind die Details weniger unterschiedlich.

Weitere Informationen zur Verwendung von Nebel in der Anwendung finden Sie unter [Nebel (Direct3D 9)](fog.md).

Eine C++-Anwendung steuert den Nebel durch Renderingzustände des Geräts. Der [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) -Enumerationstyp enthält Zustände, mit denen gesteuert werden kann, ob Pixel (Tabelle) oder Scheitelpunkt Nebel verwendet wird, welche Farbe es ist, welche Farbe das System anwendet und welche Parameter der Formel verwendet werden.

Sie aktivieren den Nebel, indem Sie den D3DRS \_ fogenable-Rendering-Zustand auf " **true**" festlegen. Die Schnebel Farbe kann auf einen beliebigen Farbwert festgelegt werden, indem der D3DRS \_ fogcolor-Rendering-Zustand verwendet wird. die Alpha Komponente der Nebelfarbe wird ignoriert.

Die \_ renderzustände D3DRS fogtablemode und D3DRS \_ fogvertexmode steuern die auf Nebel Berechnungen angewendete Nebel Formel und Steuern indirekt, welcher Typ von Nebel angewendet wird. Beide Rendering-Zustände können auf einen Member des [**D3DFOGMODE**](./d3dfogmode.md) -enumerierten Typs festgelegt werden. Wenn Sie den renderzustand auf D3DFOG \_ None festlegen, wird der Pixel-bzw. Scheitelpunkt Nebel deaktiviert. Wenn beide renderzustände auf gültige Modi festgelegt sind, wendet das System nur Pixel Nebeleffekte an.

Mit den \_ Renderingzuständen D3DRS fogstart und D3DRS \_ fogend werden die Nebel Formel Parameter für den D3DFOG \_ Linear-Modus gesteuert. Der D3DRS \_ fogdensity-renderzustand steuert die Nebeldichte in den exponentialnebelmodi.

Weitere Informationen finden Sie unter " [Fog Parameters" (Direct3D 9)](fog-parameters.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rendering-Zustände](render-states.md)
</dt> </dl>

 

 

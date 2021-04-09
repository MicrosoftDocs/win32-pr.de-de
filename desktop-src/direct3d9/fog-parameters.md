---
description: Nebel Parameter werden über den Geräte Rendering gesteuert.
ms.assetid: a3c5f439-6937-4ba9-991f-5a4154447cf9
title: Nebel Parameter (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a03104df36aba0868c15ccc0b8ddc78d1352bef7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860194"
---
# <a name="fog-parameters-direct3d-9"></a>Nebel Parameter (Direct3D 9)

Nebel Parameter werden über den Geräte Rendering gesteuert. Sowohl Pixel-als auch Scheitelpunkt Typen unterstützen alle in [Nebel Formeln (Direct3D 9)](fog-formulas.md)eingeführten Nebel Formeln. Der [**D3DFOGMODE**](./d3dfogmode.md) -enumerierte Typ definiert Konstanten, die Sie verwenden können, um die von Microsoft Direct3D zu verwendende Nebel Formel zu identifizieren. Der D3DRS \_ fogtablemode-renderzustand steuert den Nebelmodus, den Direct3D für den Pixel Nebel verwendet, und der D3DRS \_ fogvertexmode-renderzustand steuert den Modus für Scheitelpunkt Nebel.

Wenn Sie die lineare Nebel Formel verwenden, legen Sie die Start-und die endabstände über die \_ renderzustände D3DRS fogstart und D3DRS \_ fogend fest. Wie das System diese Werte interpretiert, hängt vom Typ des schachtels, den Ihre Anwendung verwendet (Pixel oder Scheitelpunkt), und bei Verwendung von Pixel Nebel, wenn die z-oder w-basierte Tiefe verwendet wird. In der folgenden Tabelle werden die Typen und deren Start-und Endeinheiten zusammengefasst.



| Nebeltyp  | Start-/Endeinheiten für Nebel      |
|-----------|--------------------------|
| Pixel (Z) | Geräteraum \[ 0,0, 1.0\] |
| Pixel (W) | Kamerabereich             |
| Scheitelpunkt    | Kamerabereich             |



 

Der D3DRS \_ fogdensity-Rendering-Zustand steuert die beim Aktivieren einer exponentialnebelformel angewendete Nebeldichte. Die Nebeldichte ist im Wesentlichen ein Gewichtungsfaktor, der zwischen 0,0 und 1,0 (einschließlich) liegt, der den Entfernungs Wert im Exponent skaliert.

Die Farbe, die das System für die Schnebel Mischung verwendet, wird über den D3DRS \_ fogcolor Device-Rendering-Zustand gesteuert. Weitere Informationen finden Sie unter [Nebelfarbe (Direct3D 9)](fog-color.md) und [Nebel Mischung (Direct3D 9)](fog-blending.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Nebel Typen](fog-types.md)
</dt> </dl>

 

 

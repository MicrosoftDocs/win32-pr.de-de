---
description: Die Tiefenpufferung ist eine Methode zum Entfernen ausgeblendeter Linien und Oberflächen. Standardmäßig verwendet Direct3D keine Tiefenpufferung.
ms.assetid: 03795e4e-1daa-48e3-8724-8dd4b5187edc
title: Tiefenpufferungszustand (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54d6d0494511c7fc0434d97988152426eb888d6c3044de4e2359ac2cb41110ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988311"
---
# <a name="depth-buffering-state-direct3d-9"></a>Tiefenpufferungszustand (Direct3D 9)

Die Tiefenpufferung ist eine Methode zum Entfernen ausgeblendeter Linien und Oberflächen. Standardmäßig verwendet Direct3D keine Tiefenpufferung.

Eine konzeptionelle Übersicht über Tiefenpuffer finden Sie unter [Tiefenpuffer (Direct3D 9).](depth-buffers.md)

C++-Anwendungen aktualisieren den Tiefenpufferungszustand mit dem D3DRS ZENABLE-Renderzustand, indem sie einen Member der \_ [**D3DUFFUFFERTYPE-Enumeration**](./d3dzbuffertype.md) verwenden, um den neuen Zustandswert anzugeben.

Wenn Ihre Anwendung verhindern muss, dass Direct3D in den Tiefenpuffer schreibt, kann sie den D3DRS ZWRITEENABLE-Aufzählwert verwenden und D3DVIN FALSE als zweiten Parameter für den Aufruf von \_ \_ [**IDirect3DDevice9::SetRenderState angeben.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)

Das folgende Codebeispiel zeigt, wie der Tiefenpufferzustand festgelegt wird, um Z-Pufferung zu aktivieren.


```
// This code example assumes that d3dDevice is a 
// valid pointer to an IDirect3DDevice9 interface.
// Enable z-buffering.
d3dDevice->SetRenderState(D3DRS_ZENABLE, D3DZB_TRUE);
```



Ihre Anwendung kann auch den D3DRS-RENDERZUSTAND DES FARBUNC-Renders verwenden, um die Vergleichsfunktion zu steuern, die Direct3D beim Ausführen der \_ Tiefenpufferung verwendet.

Z-Biasing ist eine Methode, um eine Oberfläche vor einer anderen anzuzeigen, auch wenn ihre Tiefenwerte identisch sind. Sie können diese Technik für eine Vielzahl von Effekten verwenden. Ein gängiges Beispiel ist das Rendern von Schatten an Wänden. Sowohl der Schatten als auch die Wand haben denselben Tiefenwert. Sie möchten jedoch, dass Ihre Anwendung den Schatten an der Wand zeigt. Wenn der Schatten z-bias dargestellt wird, werden sie von Direct3D ordnungsgemäß angezeigt (siehe D3DRS \_ DEPTHBIAS).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Renderzustände](render-states.md)
</dt> </dl>

 

 

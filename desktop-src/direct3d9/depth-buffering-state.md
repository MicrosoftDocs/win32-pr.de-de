---
description: Die tiefen Pufferung ist eine Methode zum Entfernen ausgeblendeter Linien und Oberflächen. Standardmäßig verwendet Direct3D keine tiefen Pufferung.
ms.assetid: 03795e4e-1daa-48e3-8724-8dd4b5187edc
title: Status der tiefen Pufferung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e632d3dfe6eebd54970c59ef6a666cfcb0950fcb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481555"
---
# <a name="depth-buffering-state-direct3d-9"></a>Status der tiefen Pufferung (Direct3D 9)

Die tiefen Pufferung ist eine Methode zum Entfernen ausgeblendeter Linien und Oberflächen. Standardmäßig verwendet Direct3D keine tiefen Pufferung.

Eine konzeptionelle Übersicht über tiefen Puffer finden Sie unter [tiefen Puffer (Direct3D 9)](depth-buffers.md).

C++-Anwendungen aktualisieren den tiefen Puffer Zustand mit dem D3DRS \_ zenable-renderzustand, wobei ein Member der [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) -Enumeration verwendet wird, um den neuen Zustandswert anzugeben.

Wenn Ihre Anwendung verhindern soll, dass Direct3D in den tiefen Puffer schreibt, kann Sie den D3DRS \_ zwriteenable-Enumerationswert verwenden, wobei D3DZB \_ false als zweiter Parameter für den Aufrufen von [**IDirect3DDevice9:: setrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)angegeben wird.

Im folgenden Codebeispiel wird gezeigt, wie der tiefen Puffer Zustand festgelegt wird, um z-Pufferung zu aktivieren.


```
// This code example assumes that d3dDevice is a 
// valid pointer to an IDirect3DDevice9 interface.
// Enable z-buffering.
d3dDevice->SetRenderState(D3DRS_ZENABLE, D3DZB_TRUE);
```



Die Anwendung kann auch den D3DRS \_ zfunc-renderzustand verwenden, um die Vergleichsfunktion zu steuern, die Direct3D beim Durchführen von tiefen Pufferungen verwendet.

Z-Biasing ist eine Methode, eine Oberfläche vor einer anderen anzuzeigen, auch wenn deren tiefen Werte identisch sind. Diese Technik kann für eine Vielzahl von Effekten verwendet werden. Ein gängiges Beispiel ist das Rendern von Schatten auf Wänden. Der Schatten und die Wand haben denselben tiefen Wert. Sie möchten jedoch, dass Ihre Anwendung den Schatten auf der Wand anzeigt. Durch die Angabe eines z-Bias zum Schatten macht Direct3D diese korrekt anzeigen (siehe D3DRS \_ depthbias).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rendering-Zustände](render-states.md)
</dt> </dl>

 

 

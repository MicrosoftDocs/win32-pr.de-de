---
description: C++-Anwendungen können Alphatests verwenden, um zu steuern, wann Pixel auf die Renderzieloberfläche geschrieben werden.
ms.assetid: 368c3d12-2c8b-43e3-94c3-bccfe6c73e66
title: Alphatestzustand (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b853eb779860d5fc490f4061fde03c852a9c3d9f7bda48baa8e5a84ebd43173c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989440"
---
# <a name="alpha-testing-state-direct3d-9"></a>Alphatestzustand (Direct3D 9)

C++-Anwendungen können Alphatests verwenden, um zu steuern, wann Pixel auf die Renderzieloberfläche geschrieben werden. Mithilfe des [**D3DRS \_ ALPHATESTENABLE-Renderzustands**](./d3drenderstatetype.md) legt Ihre Anwendung das aktuelle Direct3D-Gerät so fest, dass es jedes Pixel gemäß einer Alphatestfunktion testet. Wenn der Test erfolgreich ist, wird das Pixel auf die Oberfläche geschrieben. Wenn dies nicht dere ist, ignoriert Direct3D das Pixel. Wählen Sie die Alphatestfunktion mit dem **D3DRS \_ ALPHAFUNC-Renderzustand** aus. Ihre Anwendung kann mithilfe des **D3DRS \_ ALPHAREF-Renderzustands** einen Alpha-Verweiswert für alle Pixel festlegen, mit dem verglichen werden soll.

Die gängigste Verwendung für Alphatests ist die Verbesserung der Leistung beim Rastern von Objekten, die nahezu transparent sind. Wenn die Rasterung der Farbdaten nicht transparent ist als die Farbe in einem bestimmten Pixel (D3DPCMPCAPS \_ GREATEREQUAL), wird das Pixel geschrieben. Andernfalls ignoriert der Rasterizer das Pixel vollständig und speichert die Verarbeitung, die zum Mischen der beiden Farben erforderlich ist. Im folgenden Codebeispiel wird überprüft, ob eine bestimmte Vergleichsfunktion unterstützt wird, und wenn ja, werden die Vergleichsfunktionsparameter festgelegt, die zur Verbesserung der Leistung während des Renderings erforderlich sind.


```
// This code example assumes that pCaps is a
// D3DCAPS9 structure that was filled with a 
// previous call to IDirect3D9::GetDeviceCaps.

if (pCaps.AlphaCmpCaps & D3DPCMPCAPS_GREATEREQUAL)
{
    dev->SetRenderState(D3DRS_ALPHAREF, (DWORD)0x00000001);
    dev->SetRenderState(D3DRS_ALPHATESTENABLE, TRUE); 
    dev->SetRenderState(D3DRS_ALPHAFUNC, D3DCMP_GREATEREQUAL);
}

// If the comparison is not supported, render anyway. 
// The only drawback is no performance gain.
```



Nicht die gesamte Hardware unterstützt alle Alphatestfeatures. Sie können die Gerätefunktionen überprüfen, indem Sie die [**IDirect3D9::GetDeviceCaps-Methode**](/windows/desktop/api) aufrufen. Überprüfen Sie nach dem Abrufen der Gerätefunktionen den AlphaCmpCaps-Member der zugeordneten [**D3DCAPS9-Struktur**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) auf die gewünschte Vergleichsfunktion. Wenn der AlphaCmpCaps-Member nur die D3DPCMPCAPS \_ ALWAYS-Funktion oder nur die D3DPCMPCAPS \_ NEVER-Funktion enthält, unterstützt der Treiber keine Alphatests.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Renderzustände](render-states.md)
</dt> </dl>

 

 

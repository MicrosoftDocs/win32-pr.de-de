---
description: C++-Anwendungen können Alpha Tests verwenden, um zu steuern, wann Pixel auf die renderzieloberfläche geschrieben werden.
ms.assetid: 368c3d12-2c8b-43e3-94c3-bccfe6c73e66
title: Alpha Test Status (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 020322ee31bc08352dbb2796ea5e7141d03c77c3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346449"
---
# <a name="alpha-testing-state-direct3d-9"></a>Alpha Test Status (Direct3D 9)

C++-Anwendungen können Alpha Tests verwenden, um zu steuern, wann Pixel auf die renderzieloberfläche geschrieben werden. Wenn Sie den renderzustand [**D3DRS \_ Alpha atestenable**](./d3drenderstatetype.md) verwenden, legt ihre Anwendung das aktuelle Direct3D-Gerät so fest, dass jedes Pixel gemäß einer Alpha-Testfunktion getestet wird. Wenn der Test erfolgreich ist, wird das Pixel auf die-Oberfläche geschrieben. Wenn dies nicht der Fall ist, wird das Pixel von Direct3D ignoriert. Wählen Sie die Alpha-Testfunktion mit dem **D3DRS \_ alphafunc** -gerengerzustand aus. Die Anwendung kann einen Referenz-Alpha-Wert für alle Pixel festlegen, mit denen der **D3DRS- \_ Alpha Aref** -Rendering-Zustand verglichen werden soll.

Die häufigste Verwendung für Alpha Tests ist die Verbesserung der Leistung bei der fast transparenten rasterisierung von Objekten. Wenn die zu ragenden Farbdaten transparenter sind als die Farbe an einem bestimmten Pixel (D3DPCMPCAPS \_ greaterequal), wird das Pixel geschrieben. Andernfalls ignoriert der Raster das Pixel vollständig und speichert die Verarbeitung, die zum Mischen der beiden Farben erforderlich ist. Im folgenden Codebeispiel wird überprüft, ob eine angegebene Vergleichsfunktion unterstützt wird, und wenn dies der Fall ist, werden die Vergleichs Funktionsparameter festgelegt, die zum Verbessern der Leistung beim Rendern


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



Nicht alle Hardware unterstützt alle Alpha Test Features. Sie können die Gerätefunktionen überprüfen, indem Sie die [**IDirect3D9:: GetDeviceCaps**](/windows/desktop/api) -Methode aufrufen. Überprüfen Sie nach dem Abrufen der Gerätefunktionen den Alpha acmpcaps-Member der zugeordneten [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) -Struktur auf die gewünschte Vergleichsfunktion. Wenn das Alpha acmpcaps-Element nur die Funktion "D3DPCMPCAPS \_ Always" oder nur die Funktion "D3DPCMPCAPS Never" enthält \_ , unterstützt der Treiber keine Alpha Tests.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rendering-Zustände](render-states.md)
</dt> </dl>

 

 

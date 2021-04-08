---
description: Wie bei allen Features unterstützt der Treiber, den Ihre Anwendung verwendet, möglicherweise nicht alle Arten der tiefen Pufferung.
ms.assetid: 8bf022f6-fd97-43f5-ac19-6a75ddb45f5e
title: Abfragen der Tiefe Puffer Unterstützung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bfe7555c1fa0fccddcfcb12ff8bc53f1a0f5f81
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745521"
---
# <a name="querying-for-depth-buffer-support-direct3d-9"></a>Abfragen der Tiefe Puffer Unterstützung (Direct3D 9)

Wie bei allen Features unterstützt der Treiber, den Ihre Anwendung verwendet, möglicherweise nicht alle Arten der tiefen Pufferung. Überprüfen Sie immer die Funktionen des Treibers. Obwohl die meisten Treiber z-basierte tiefen Pufferung unterstützen, unterstützen nicht alle die w-basierte tiefen Pufferung. Treiber schlagen nicht fehl, wenn Sie versuchen, ein nicht unterstütztes Schema zu aktivieren. Sie werden stattdessen auf eine andere tiefen Puffer Methode zurückgreifen, oder Sie deaktivieren manchmal die Tiefe Pufferung, was dazu führen kann, dass Szenen mit extrem tiefen Sortier Artefakten gerendert werden.

Sie können die allgemeine Unterstützung von tiefen Puffern überprüfen, indem Sie Direct3D für das Anzeigegerät Abfragen, das von der Anwendung verwendet wird, bevor Sie ein Direct3D-Gerät erstellen. Wenn das Direct3D-Objekt meldet, dass die tiefen Pufferung unterstützt wird, unterstützen alle Hardware Geräte, die Sie aus diesem Direct3D-Objekt erstellen, z-Pufferung.

Um die Unterstützung der tiefen Pufferung abzufragen, können Sie die [**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) -Methode verwenden, wie im folgenden Codebeispiel gezeigt.


```
// The following example assumes that pCaps is a valid pointer to an 
// initialized D3DCAPS9 structure
if(FAILED(m_pD3D->CheckDeviceFormat(pCaps->AdapterOrdinal, 
                                    pCaps->DeviceType, 
                                    AdapterFormat, 
                                    D3DUSAGE_DEPTHSTENCIL, 
                                    D3DRTYPE_SURFACE,
                                    D3DFMT_D16)))
    return E_FAIL;
```



[**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) ermöglicht Ihnen die Auswahl eines zu erstellenden Geräts basierend auf den Funktionen dieses Geräts. In diesem Fall werden Geräte, die 16-Bit-Tiefen Puffer nicht unterstützen, zurückgewiesen.

Die Verwendung von [**IDirect3D9:: checkdepthstencilmatch**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdepthstencilmatch) zum Ermitteln der tiefen Schablone-Kompatibilität mit einem Renderziel wird im folgenden Codebeispiel veranschaulicht.


```
// Reject devices that cannot create a render target of RTFormat while
// the back buffer is of RTFormat and the depth-stencil buffer is
// at least 8 bits of stencil
if(FAILED(m_pD3D->CheckDepthStencilMatch(pCaps->AdapterOrdinal,
                                        pCaps->DeviceType, 
                                        AdapterFormat, 
                                        RTFormat, 
                                        D3DFMT_D24S8)))
    return E_FAIL;
```



Wenn Sie wissen, dass der Treiber Tiefe Puffer unterstützt, können Sie die Unterstützung für den w-Puffer überprüfen. Obwohl tiefen Puffer für alle Software Rasterizer unterstützt werden, werden w-Puffer nur vom Verweis Raster unterstützt, der nicht für die Verwendung durch reale Anwendungen geeignet ist. Überprüfen Sie unabhängig vom Gerätetyp, der von der Anwendung verwendet wird, die Unterstützung für w-Puffer, bevor Sie versuchen, die w-basierte tiefen Pufferung zu aktivieren.

1.  Nachdem Sie Ihr Gerät erstellt haben, können Sie die [**IDirect3DDevice9:: GetDeviceCaps**](/windows/desktop/api) -Methode aufrufen und dabei eine initialisierte [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) -Struktur übergeben.
2.  Nach dem-Befehl enthält das LineCaps-Element Informationen über die Unterstützung des Treibers für das Rendern von primitiven.
3.  Wenn das RasterCaps-Element dieser Struktur das D3DPRASTERCAPS \_ wbuffer-Flag enthält, unterstützt der Treiber die w-basierte tiefen Pufferung für diesen primitiven Typ.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Tiefen Puffer](depth-buffers.md)
</dt> </dl>

 

 

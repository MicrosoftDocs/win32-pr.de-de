---
title: Direct3D 11,4-Features
description: Die folgende Funktionalität wurde in Direct3D 11,4 hinzugefügt.
ms.assetid: 689A0460-5725-4C48-B960-41FE20499082
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5b0d2814aa1f9a7ac7b5f2c87ff9d918b36116f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948899"
---
# <a name="direct3d-114-features"></a>Direct3D 11,4-Features

Die folgende Funktionalität wurde in Direct3D 11,4 hinzugefügt.

Weitere Informationen finden Sie auch [unter wo ist das DirectX SDK?](../directx-sdk--august-2009-.md).

## <a name="direct3d-device-removal"></a>Direct3D Entfernen von Geräten

Die [**registerdeviceremovedevent**](/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-registerdeviceremovedevent)-Methode und die [**unregisterdeviceremoved**](/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-unregisterdeviceremoved) -Methode werden von der neuen Schnittstelle [**ID3D11Device4**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4)unterstützt, um den Empfang einer asynchronen Ereignis Benachrichtigung zu unterstützen, wenn ein Direct3D-Gerät entfernt wurde.

## <a name="multithreaded-protection"></a>Multithread-Schutz

Um sicherzustellen, dass Grafikbefehle speziell in einer bestimmten Reihenfolge ausgeführt werden, verfügt die [**ID3D11Multithread**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11multithread) -Schnittstelle über Methoden zum Aktivieren und Deaktivieren des multithreadschutzes sowie Methoden zum eingeben und verlassen von kritischem Code, der diesen Schutz erfordert.

## <a name="fences-for-multi-device-synchronization-and-interop-with-direct3d-12"></a>Zäune für die Synchronisierung von mehreren Geräten und Interop mit Direct3D 12

[**ID3D11Fence**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11fence), [**ID3D11Device5**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5) und [**ID3D11DeviceContext4**](/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4) bieten die gleiche Fence-Funktionalität wie Direct3D 12 für Direct3D 11. Mithilfe von Zäunen werden mehrere Direct3D11-Geräte und Interop zwischen Direct3D 11 und Direct3D 12 synchronisiert. Im Windows 10 Creators Update werden Zäune unterstützt.

## <a name="extended-nv12-texture-support"></a>Erweiterte NV12-Textur Unterstützung

NV12 Texturen mit Erfassungs-und videocodierfunktionen unterstützen jetzt die Freigabe. Ältere D3D11-Textur-Flags für videoencode und Capture sind für NV12 veraltet, da Sie für neue Treiber ständig festgelegt werden. Solche Texturen können nicht nur mit D3D11, sondern auch mit D3D12 freigegeben werden. In D3D12 stellen keine neuen Flags diese Textur Funktionen dar.

Weitere Informationen finden Sie in der booleschen Einstellung in [**D3D11 \_ Feature \_ Data \_ D3D11 \_ OPTIONS4**](/windows/desktop/api/d3d11_4/ns-d3d11_4-d3d11_feature_data_d3d11_options4).

## <a name="shader-caching"></a>Shader-Caching

Treiber unterstützen möglicherweise das vom Betriebssystem verwaltete Shader-Caching von Direct3D11-Anwendungen im Windows 10 Creators Update.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Neuerungen in Direct3D 11](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 
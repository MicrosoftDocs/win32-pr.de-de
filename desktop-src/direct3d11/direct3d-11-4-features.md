---
title: Direct3D 11.4-Features
description: Die folgenden Funktionen wurden in Direct3D 11.4 hinzugefügt.
ms.assetid: 689A0460-5725-4C48-B960-41FE20499082
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57190dbd244a565d579e807f7b7b2322ebfec0216d8a6862c4772c4cd4ebe142
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124535"
---
# <a name="direct3d-114-features"></a>Direct3D 11.4-Features

Die folgenden Funktionen wurden in Direct3D 11.4 hinzugefügt.

Siehe auch [Wo befindet sich das DirectX SDK?](../directx-sdk--august-2009-.md).

## <a name="direct3d-device-removal"></a>Entfernen von Direct3D-Geräten

Die [**Methoden RegisterDeviceRemovedEvent**](/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-registerdeviceremovedevent)und [**UnregisterDeviceRemoved**](/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-unregisterdeviceremoved) werden von der neuen Schnittstelle [**ID3D11Device4**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4)unterstützt, um das Empfangen einer asynchronen Ereignisbenachrichtigung zu unterstützen, wenn ein Direct3D-Gerät entfernt wurde.

## <a name="multithreaded-protection"></a>Multithreadschutz

Um sicherzustellen, dass insbesondere Grafikbefehle in einer bestimmten Reihenfolge ausgeführt werden, verfügt die [**ID3D11Multithread-Schnittstelle**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11multithread) über Methoden zum Aktivieren und Deaktivieren des Multithreadschutzes und Methoden zum Eingeben und Verlassen von kritischem Code, der diesen Schutz erfordert.

## <a name="fences-for-multi-device-synchronization-and-interop-with-direct3d-12"></a>Fences for multi-device synchronization and interop with Direct3D 12 (Umsperrungen für die Synchronisierung und Inop mit Direct3D 12 für mehrere Geräte)

[**ID3D11Fence,**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11fence) [**ID3D11Device5**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5) und [**ID3D11DeviceContext4**](/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4) bieten die gleiche Fence-Funktionalität wie Direct3D 12 für Direct3D 11. Fences werden verwendet, um mehrere Direct3D11-Geräte und die Inaktivität zwischen Direct3D 11 und Direct3D 12 zu synchronisieren. Fences werden in der Windows 10 Creators Update.

## <a name="extended-nv12-texture-support"></a>Erweiterte NV12-Texturunterstützung

NV12-Texturen mit Erfassungs- und Videocodierungsfunktionen unterstützen jetzt die Freigabe. Ältere D3D11-Texturflags für Videocodierung und -erfassung sind für NV12 veraltet, da sie für neue Treiber immer festgelegt werden. Solche Texturen können nicht nur für D3D11, sondern auch für D3D12 freigegeben werden. In D3D12 stellen keine neuen Flags diese Texturfunktionen dar.

Weitere Informationen finden Sie in der booleschen Einstellung unter [**D3D11 \_ FEATURE \_ DATA \_ D3D11 \_ OPTIONS4.**](/windows/desktop/api/d3d11_4/ns-d3d11_4-d3d11_feature_data_d3d11_options4)

## <a name="shader-caching"></a>Shaderzwischenspeicherung

Treiber unterstützen möglicherweise die vom Betriebssystem verwaltete Shaderzwischenspeicherung von Direct3D11-Anwendungen im Windows 10 Creators-Update.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Neues in Direct3D 11](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 
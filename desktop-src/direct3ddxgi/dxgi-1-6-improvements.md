---
description: In diesem Thema werden die Neuerungen in Microsoft DirectX Graphic Infrastructure (DXGI) 1.6 für verschiedene Releases von Windows 10 beschrieben.
ms.assetid: C68EC437-7600-43A8-8DEA-5A6AEE75D5AA
title: DXGI 1.6-Verbesserungen
ms.topic: article
ms.date: 12/04/2019
ms.openlocfilehash: 748878cc041b0987a013608556cd9ec30aaf638e0fcac1ef9386a4675f57ef0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119727580"
---
# <a name="dxgi-16-improvements"></a>DXGI 1.6-Verbesserungen

In diesem Thema werden die Neuerungen in Microsoft DirectX Graphic Infrastructure (DXGI) 1.6 für verschiedene Releases von Windows 10 beschrieben.

## <a name="windows-10-october-2018-update"></a>Windows 10-Update von Oktober 2018

Diese APIs wurden für Windows 10, Version 1809 (10.0; Build 17763) &mdash; auch als Windows 10 October 2018 Update bezeichnet.

- [**IDXGIFactory7-Schnittstelle**](/windows/win32/api/dxgi1_6/nn-dxgi1_6-idxgifactory7) und ihre Methoden.

## <a name="windows-10-april-2018-update"></a>Windows 10-Update vom April 2018

Diese APIs wurden für Windows 10 Version 1803 (10.0; Build 17134) &mdash; auch als Windows 10 April 2018 Update bezeichnet.

- [**DXGI_GPU_PREFERENCE-Enumeration.**](/windows/win32/api/dxgi1_6/ne-dxgi1_6-dxgi_gpu_preference)
- [**IDXGIFactory6-Schnittstelle**](/windows/win32/api/dxgi1_6/nn-dxgi1_6-idxgifactory6) und ihre Methoden.

## <a name="windows-10-fall-creators-update"></a>Windows 10 Fall Creators Update

Für Windows 10 Version 1709 (10.0; Build 16299) &mdash; wird auch als Windows 10 Fall Creators Update diese &mdash; Konstanten wurden der [**DXGI_ADAPTER_FLAG3-Enumeration**](/windows/win32/api/dxgi1_6/ne-dxgi1_6-dxgi_adapter_flag3) hinzugefügt. 

- **DXGI_ADAPTER_FLAG3_SUPPORT_MONITORED_FENCES**
- **DXGI_ADAPTER_FLAG3_SUPPORT_NON_MONITORED_FENCES**
- **DXGI_ADAPTER_FLAG3_KEYED_MUTEX_CONFORMANCE**

## <a name="windows-10-creators-update"></a>Windows 10 Creators Update

Für Windows 10 Version 1703 (10.0; Build 15063), auch bekannt als Windows 10 Creators Update die &mdash; folgenden Funktionen wurden Microsoft DirectX Graphic Infrastructure &mdash; (DXGI) 1.6 hinzugefügt, um HDR-Anzeigen zu erkennen.

### <a name="high-dynamic-range-hdr-detection"></a>Hdr-Erkennung (Hoher dynamischer Bereich)

Diese APIs wurden hinzugefügt, um HDR-Anzeigen zu erkennen.

- [**DXGI_ADAPTER_DESC3-Struktur**](/windows/win32/api/dxgi1_6/ns-dxgi1_6-dxgi_adapter_desc3)
- [**DXGI_ADAPTER_FLAG3-Enumeration**](/windows/win32/api/dxgi1_6/ne-dxgi1_6-dxgi_adapter_flag3)
- [**DXGI_HARDWARE_COMPOSITION_SUPPORT_FLAGS-Enumeration**](/windows/win32/api/dxgi1_6/ne-dxgi1_6-dxgi_hardware_composition_support_flags)
- [**DXGI_OUTPUT_DESC1-Struktur**](/windows/win32/api/dxgi1_6/ns-dxgi1_6-dxgi_output_desc1)
- [**DXGIDeclareAdapterRemovalSupport-Funktion**](/windows/win32/api/dxgi1_6/nf-dxgi1_6-dxgideclareadapterremovalsupport)
- [**IDXGIAdapter4-Schnittstelle**](/windows/win32/api/dxgi1_6/nn-dxgi1_6-idxgiadapter4) und ihre Methoden
- [**IDXGIOutput6-Schnittstelle**](/windows/win32/api/dxgi1_6/nn-dxgi1_6-idxgioutput6) und ihre Methoden

Außerdem wurden konstanten zur [**DXGI_COLOR_SPACE_TYPE-Enumeration**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) hinzugefügt, um diese APIs zu unterstützen.

## <a name="related-topics"></a>Zugehörige Themen
[Programmierhandbuch für DXGI](dx-graphics-dxgi-overviews.md)

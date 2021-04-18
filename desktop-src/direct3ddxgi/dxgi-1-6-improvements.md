---
description: In diesem Thema wird beschrieben, welche Neuerungen in Microsoft DirectX Graphics Infrastructure (DXGI) 1,6 für verschiedene Versionen von Windows 10 enthalten sind.
ms.assetid: C68EC437-7600-43A8-8DEA-5A6AEE75D5AA
title: DXGI 1,6-Verbesserungen
ms.topic: article
ms.date: 12/04/2019
ms.openlocfilehash: 03961b4f9af50675ee157c4840b9ed744c54f423
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522384"
---
# <a name="dxgi-16-improvements"></a>DXGI 1,6-Verbesserungen

In diesem Thema wird beschrieben, welche Neuerungen in Microsoft DirectX Graphics Infrastructure (DXGI) 1,6 für verschiedene Versionen von Windows 10 enthalten sind.

## <a name="windows-10-october-2018-update"></a>Windows 10-Update von Oktober 2018

Diese APIs wurden für Windows 10, Version 1809 (10,0;) hinzugefügt. Build 17763) &mdash; auch als Windows 10-Update vom Oktober 2018 bezeichnet.

- [**IDXGIFactory7**](/windows/win32/api/dxgi1_6/nn-dxgi1_6-idxgifactory7) -Schnittstelle und ihre Methoden.

## <a name="windows-10-april-2018-update"></a>Windows 10-Update vom April 2018

Diese APIs wurden für Windows 10, Version 1803 (10,0;) hinzugefügt. Build 17134) &mdash; auch als Windows 10-Update vom April 2018 bezeichnet.

- [**DXGI_GPU_PREFERENCE**](/windows/win32/api/dxgi1_6/ne-dxgi1_6-dxgi_gpu_preference) Enumeration.
- [**IDXGIFactory6**](/windows/win32/api/dxgi1_6/nn-dxgi1_6-idxgifactory6) -Schnittstelle und ihre Methoden.

## <a name="windows-10-fall-creators-update"></a>Windows 10 Fall Creators Update

Für Windows 10, Version 1709 (10,0; Build 16299) &mdash; auch als Windows 10 Fall Creators Update bezeichnet &mdash; , dass diese Konstanten der [**DXGI_ADAPTER_FLAG3**](/windows/win32/api/dxgi1_6/ne-dxgi1_6-dxgi_adapter_flag3) -Enumeration hinzugefügt wurden. 

- **DXGI_ADAPTER_FLAG3_SUPPORT_MONITORED_FENCES**
- **DXGI_ADAPTER_FLAG3_SUPPORT_NON_MONITORED_FENCES**
- **DXGI_ADAPTER_FLAG3_KEYED_MUTEX_CONFORMANCE**

## <a name="windows-10-creators-update"></a>Windows 10 Creators Update

Für Windows 10, Version 1703 (10,0; Build 15063) wird &mdash; auch als Windows 10 Creators Update bezeichnet &mdash; . die folgende Funktionalität wurde Microsoft DirectX Graphics Infrastructure (DXGI) 1,6 hinzugefügt, um HDR-anzeigen zu erkennen.

### <a name="high-dynamic-range-hdr-detection"></a>Erkennung von hohem dynamischen Bereich (HDR)

Diese APIs wurden hinzugefügt, um HDR-anzeigen zu erkennen.

- [**DXGI_ADAPTER_DESC3**](/windows/win32/api/dxgi1_6/ns-dxgi1_6-dxgi_adapter_desc3) Struktur
- [**DXGI_ADAPTER_FLAG3**](/windows/win32/api/dxgi1_6/ne-dxgi1_6-dxgi_adapter_flag3) -Enumeration
- [**DXGI_HARDWARE_COMPOSITION_SUPPORT_FLAGS**](/windows/win32/api/dxgi1_6/ne-dxgi1_6-dxgi_hardware_composition_support_flags) -Enumeration
- [**DXGI_OUTPUT_DESC1**](/windows/win32/api/dxgi1_6/ns-dxgi1_6-dxgi_output_desc1) Struktur
- [**Dxgideclareadapterremovalsupport**](/windows/win32/api/dxgi1_6/nf-dxgi1_6-dxgideclareadapterremovalsupport) -Funktion
- [**IDXGIAdapter4**](/windows/win32/api/dxgi1_6/nn-dxgi1_6-idxgiadapter4) -Schnittstelle und ihre Methoden
- [**IDXGIOutput6**](/windows/win32/api/dxgi1_6/nn-dxgi1_6-idxgioutput6) -Schnittstelle und ihre Methoden

Außerdem wurden Konstanten zur [**DXGI_COLOR_SPACE_TYPE**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) -Enumeration hinzugefügt, um diese APIs zu unterstützen.

## <a name="related-topics"></a>Zugehörige Themen
[Programmier Handbuch für DXGI](dx-graphics-dxgi-overviews.md)

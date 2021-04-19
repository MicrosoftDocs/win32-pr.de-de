---
title: DXCore-Adapterattribut-GUIDs
description: 'Die folgenden Adapter Attribut-GUIDs werden in deklariert `dxcore_interface.h` und mit den [idxcoreadapterfactory:: deateadapterlist](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-createadapterlist.md) -und [idxcoreadapter:: isattributesupportiert](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isattributesupported.md) -Methoden verwendet.'
keywords:
- DXCore, Adapter Attribut, GUIDs
topic_type:
- apiref
api_name:
- DXCore adapter attribute GUIDs
api_location:
- dxcore_interface.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: a532552f144dfc21aa5d6a368aecd915d30b40c8
ms.sourcegitcommit: 8737f32d64e5f01c1d38aab92736e4088d6c446e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "106367243"
---
# <a name="dxcore-adapter-attribute-guids"></a>DXCore-Adapterattribut-GUIDs

Die folgenden Adapter Attribut-GUIDs werden in deklariert `dxcore_interface.h` und mit den [idxcoreadapterfactory:: deateadapterlist](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-createadapterlist.md) -und [idxcoreadapter:: isattributesupportiert](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isattributesupported.md) -Methoden verwendet. Ein oder mehrere Attribute können für einen bestimmten Adapter angewendet werden.

| GUID | Wert |
|-|-|
| `DXCORE_ADAPTER_ATTRIBUTE_D3D11_GRAPHICS`. Gibt einen Adapter an, der die Verwendung mit den [Direct3D 11](/windows/win32/direct3d11) -Grafik-APIs unterstützt. Für bestimmte Features gibt es keine Garantien, und es besteht keine Garantie, dass das Betriebssystem in seiner aktuellen Konfiguration diese APIs unterstützt. | 0x8c47866b, 0x7583, 0x450d, 0xF 0, 0xF 0, 0x6b, 0xAD, 0xa8, 0x95, 0xaf, 0x4B |
| `DXCORE_ADAPTER_ATTRIBUTE_D3D12_GRAPHICS`. Gibt einen Adapter an, der die Verwendung mit den [Direct3D 12](/windows/win32/direct3d12) -Grafik-APIs unterstützt. Für bestimmte Features gibt es keine Garantien, und es besteht keine Garantie, dass das Betriebssystem in seiner aktuellen Konfiguration diese APIs unterstützt. | 0x0c9ece4d, 0x2F 6E, 0x4F, 0x8c, 0x96, 0xe8, 0x9E, 0x33, 0x1B, 0x47, 0xb1 |
| `DXCORE_ADAPTER_ATTRIBUTE_D3D12_CORE_COMPUTE`. Gibt einen Adapter an, der die Verwendung mit den [Direct3D 12 Core](../direct3d12/core-feature-levels.md) -Compute-APIs unterstützt. Für bestimmte Features gibt es keine Garantien, und es besteht keine Garantie, dass das Betriebssystem in seiner aktuellen Konfiguration diese APIs unterstützt. | 0x248e2800, 0xa793, 0x4724, 0xAB, 0xAA, 0x23, 0xA6, 0xde, 0x1B, 0xE0, 0x90 |

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Header | dxcore_interface. h |

## <a name="see-also"></a>Siehe auch

* [IDXCoreAdapterFactory::CreateAdapterList](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-createadapterlist.md)
* [IDXCoreAdapter::IsAttributeSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isattributesupported.md)
* [DXCore-Referenz](./dxcore-reference.md)
* [Verwenden von DXCore zum Auflisten von Adaptern](./dxcore-enum-adapters.md)
* [Direct3D 12-Grafiken](../direct3d12/direct3d-12-graphics.md)

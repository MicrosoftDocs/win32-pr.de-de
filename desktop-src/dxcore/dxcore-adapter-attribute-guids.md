---
title: DXCore-Adapterattribut-GUIDs
description: Die folgenden Adapterattribut-GUIDs werden in deklariert und mit den `dxcore_interface.h` [Methoden IDXCoreAdapterFactory::CreateAdapterList](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-createadapterlist.md) und [IDXCoreAdapter::IsAttributeSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isattributesupported.md) verwendet.
keywords:
- DXCore, Adapterattribut, GUIDs
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
ms.openlocfilehash: 44b6be239286e13cecbf6eb501b333cba5541f6de1dfd8e217166d9620bdfbd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118279660"
---
# <a name="dxcore-adapter-attribute-guids"></a>DXCore-Adapterattribut-GUIDs

Die folgenden Adapterattribut-GUIDs werden in deklariert und mit den `dxcore_interface.h` [Methoden IDXCoreAdapterFactory::CreateAdapterList](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-createadapterlist.md) und [IDXCoreAdapter::IsAttributeSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isattributesupported.md) verwendet. Für einen bestimmten Adapter kann mindestens eines der Attribute gelten.

| GUID | Wert |
|-|-|
| `DXCORE_ADAPTER_ATTRIBUTE_D3D11_GRAPHICS`. Gibt einen Adapter an, der die Verwendung mit den [Direct3D 11-Grafik-APIs](/windows/win32/direct3d11) unterstützt. Es werden keine Garantien für bestimmte Features gewährt, und es wird auch nicht garantiert, dass das Betriebssystem in seiner aktuellen Konfiguration diese APIs unterstützt. | 0x8c47866b, 0x7583, 0x450d, 0xf0, 0xf0, 0x6b, 0xad, 0xa8, 0x95, 0xaf, 0x4b |
| `DXCORE_ADAPTER_ATTRIBUTE_D3D12_GRAPHICS`. Gibt einen Adapter an, der die Verwendung mit den [Direct3D 12-Grafik-APIs](/windows/win32/direct3d12) unterstützt. Es werden keine Garantien für bestimmte Features gewährt, und es wird auch nicht garantiert, dass das Betriebssystem in seiner aktuellen Konfiguration diese APIs unterstützt. | 0x0c9ece4d, 0x2f6e, 0x4f01, 0x8c, 0x96, 0xe8, 0x9e, 0x33, 0x1b, 0x47, 0xb1 |
| `DXCORE_ADAPTER_ATTRIBUTE_D3D12_CORE_COMPUTE`. Gibt einen Adapter an, der die Verwendung mit den [Direct3D 12 Core-Compute-APIs](../direct3d12/core-feature-levels.md) unterstützt. Es werden keine Garantien für bestimmte Features gewährt, und es wird auch nicht garantiert, dass das Betriebssystem in seiner aktuellen Konfiguration diese APIs unterstützt. | 0x248e2800, 0xa793, 0x4724, 0xab, 0xaa, 0x23, 0xa6, 0xde, 0x1b, 0xe0, 0x90 |

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Header | dxcore_interface.h |

## <a name="see-also"></a>Siehe auch

* [IDXCoreAdapterFactory::CreateAdapterList](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-createadapterlist.md)
* [IDXCoreAdapter::IsAttributeSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isattributesupported.md)
* [DXCore-Referenz](./dxcore-reference.md)
* [Verwenden von DXCore zum Auflisten von Adaptern](./dxcore-enum-adapters.md)
* [Direct3D 12-Grafiken](../direct3d12/direct3d-12-graphics.md)

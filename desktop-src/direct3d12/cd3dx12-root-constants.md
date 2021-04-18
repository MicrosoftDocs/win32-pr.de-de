---
title: CD3DX12_ROOT_CONSTANTS-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12-Stamm \_ \_ Konstanten Struktur zu ermöglichen.
ms.assetid: 2F517DCE-BC0C-4678-9C25-D826036F99A8
keywords:
- CD3DX12_ROOT_CONSTANTS Struktur
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_CONSTANTS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7a1f81a429b083400adad60f316cc90c4ede1d9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365074"
---
# <a name="cd3dx12_root_constants-structure"></a>CD3DX12 \_ root \_ Konstanten-Struktur

Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12-Stamm \_ \_ Konstanten**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) Struktur zu ermöglichen.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_ROOT_CONSTANTS  : public D3D12_ROOT_CONSTANTS{
       CD3DX12_ROOT_CONSTANTS();
       explicit CD3DX12_ROOT_CONSTANTS(const D3D12_ROOT_CONSTANTS &o);
       CD3DX12_ROOT_CONSTANTS(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0);
  void inline Init(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0);
  void static inline Init(D3D12_ROOT_CONSTANTS &rootConstants, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0);
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ root- \_ Konstanten ()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz von CD3DX12 root- \_ \_ Konstanten.

</dd> <dt>

**explizite CD3DX12-Stamm \_ \_ Konstanten (konstant D3D12 \_ Stamm \_ Konstanten &o)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12 \_ root- \_ Konstante, die mit dem Inhalt einer anderen [**D3D12 \_ root \_ Constants**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) -Struktur initialisiert wird.

</dd> <dt>

**CD3DX12 \_ root \_ Konstanten (uint num32BitValues, uint shaderregister, uint registerspace = 0)**
</dt> <dd>

Erstellt eine neue Instanz der CD3DX12- \_ Stamm \_ Konstanten und initialisiert die folgenden Parameter:

Uint num32BitValues

Uint-shaderregister

Opt Uint registerspace = 0

</dd> <dt>

**Inline-init (uint num32BitValues, uint shaderregister, uint registerspace = 0)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

Uint num32BitValues

Uint-shaderregister

Opt Uint registerspace = 0

</dd> <dt>

**static Inline init (D3D12 \_ root \_ Konstanten &rootkonstanten, uint num32BitValues, uint shaderregister, uint registerspace = 0)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

[**D3D12 \_ Stamm \_ Konstanten**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) &rootkonstanten

Uint num32BitValues

Uint-shaderregister

Opt Uint registerspace = 0

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D3D12 \_ root- \_ Konstanten**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 






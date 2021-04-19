---
title: CD3DX12_ROOT_DESCRIPTOR-Struktur (D3dx12. h)
description: Eine hilfsstruktur, die die einfache Initialisierung einer D3D12 \_ - \_ stammdeskriptorstruktur ermöglicht.
ms.assetid: DB05BAB7-DD30-4EC7-8D66-C0B2D8DD7BAC
keywords:
- CD3DX12_ROOT_DESCRIPTOR Struktur
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 710064436e0287b570700ff5812b728ca62be56d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106357279"
---
# <a name="cd3dx12_root_descriptor-structure"></a>CD3DX12 \_ - \_ stammdeskriptorstruktur

Eine hilfsstruktur, die die einfache Initialisierung einer [**D3D12 \_ - \_ stammdeskriptorstruktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) ermöglicht.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_ROOT_DESCRIPTOR  : public D3D12_ROOT_DESCRIPTOR{
       CD3DX12_ROOT_DESCRIPTOR();
       explicit CD3DX12_ROOT_DESCRIPTOR(const D3D12_ROOT_DESCRIPTOR &o);
       CD3DX12_ROOT_DESCRIPTOR(UINT shaderRegister, UINT registerSpace = 0);
  void inline Init(UINT shaderRegister, UINT registerSpace = 0);
  void static inline Init(D3D12_ROOT_DESCRIPTOR &table, UINT shaderRegister, UINT registerSpace = 0);
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12-Stamm \_ \_ Deskriptor ()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12-Stamm \_ \_ Deskriptors.

</dd> <dt>

**expliziter CD3DX12-Stamm \_ \_ Deskriptor (konstant D3D12 Stamm \_ \_ Deskriptor &o)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12- \_ Stamm \_ Deskriptors, der mit dem Inhalt einer anderen [**D3D12- \_ \_ stammdeskriptorstruktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) initialisiert wird.

</dd> <dt>

**CD3DX12 \_ root \_ Descriptor (uint shaderregister, uint registerspace = 0)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12- \_ Stamm \_ Deskriptors und initialisiert die folgenden Parameter:

Uint-shaderregister

Opt Uint registerspace = 0

</dd> <dt>

**Inline-init (uint shaderregister, uint registerspace = 0)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

Uint-shaderregister

Opt Uint registerspace = 0

</dd> <dt>

**static Inline init (D3D12 \_ root \_ Descriptor &Table, uint shaderregister, uint registerspace = 0)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

[**D3D12 \_ Stamm \_ Deskriptor**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) &Tabelle

Uint-shaderregister

Opt Uint registerspace = 0

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D3D12-Stamm \_ \_ Deskriptor**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 






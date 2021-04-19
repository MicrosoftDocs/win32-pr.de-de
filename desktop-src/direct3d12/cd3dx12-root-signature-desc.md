---
title: CD3DX12_ROOT_SIGNATURE_DESC-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12-Stamm \_ \_ Signatur \_ DESC-Struktur zu ermöglichen.
ms.assetid: A3B820C1-51E8-4E35-A67F-2C4BE82A6B7F
keywords:
- CD3DX12_ROOT_SIGNATURE_DESC Struktur
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_SIGNATURE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f89f9cd0f5ad9be08af1fa9c2556ebfbd4fcff1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361899"
---
# <a name="cd3dx12_root_signature_desc-structure"></a>CD3DX12-Struktur der Stamm \_ \_ Signatur \_ DESC

Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12-Stamm \_ \_ Signatur \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) -Struktur zu ermöglichen.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_ROOT_SIGNATURE_DESC  : public D3D12_ROOT_SIGNATURE_DESC{
       CD3DX12_ROOT_SIGNATURE_DESC();
       explicit CD3DX12_ROOT_SIGNATURE_DESC(const D3D12_ROOT_SIGNATURE_DESC &o);
       CD3DX12_ROOT_SIGNATURE_DESC(UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
       CD3DX12_ROOT_SIGNATURE_DESC(CD3DX12_DEFAULT);
  void inline Init(UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
  void static inline Init(D3D12_ROOT_SIGNATURE_DESC &desc, UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ Stamm \_ Signatur \_ DESC ()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz einer CD3DX12 \_ root \_ Signature \_ DESC.

</dd> <dt>

**explizit CD3DX12 \_ Stamm \_ Signatur \_ DESC (konstant D3D12 Stamm \_ \_ Signatur \_ DESC &o)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12 \_ root \_ Signature \_ DESC, die mit dem Inhalt einer anderen [**D3D12 \_ root \_ Signature \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) -Struktur initialisiert wird.

</dd> <dt>

**CD3DX12 \_ root \_ Signature \_ DESC (uint numparameters, Konstanten D3D12 \_ root \_ Parameter \* \_ pparameters, uint numstaticsamplers = 0, Konstanten D3D12 \_ static \_ Sampler \_ DESC \* \_ pstaticsamplers = NULL, D3D12 \_ root \_ Signature \_ Flags Flags = D3D12 \_ root \_ Signature \_ Flag \_ None)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12 \_ root \_ Signature \_ DESC und initialisiert die folgenden Parameter:

Uint numparameters

[**D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) Pparameters-Stamm Parameter \* \_

Opt Uint numstaticsamplers = 0

Opt [**D3D12 \_ Statischer \_ Sampler- \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pstaticsamplers = NULL

Opt [**D3D12 \_ Flags für root \_ Signature \_ Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = \_ D3D12 \_ root Signature \_ Flag \_ None

</dd> <dt>

**CD3DX12 \_ root \_ Signature \_ DESC (CD3DX12 \_ Standard)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12 \_ root \_ Signature \_ DESC, die mit Standardparametern initialisiert wird.

``` syntax
CD3DX12_ROOT_SIGNATURE_DESC(0,NULL,0,NULL,D3D12_ROOT_SIGNATURE_FLAG_NONE)
```

</dd> <dt>

**Inline-init (uint numparameters, Konstanten D3D12 \_ root \_ Parameter \* \_ pparameters, uint numstaticsamplers = 0, Konstanten D3D12 \_ static \_ Sampler \_ DESC \* \_ pstaticsamplers = NULL, D3D12 \_ root \_ Signature \_ Flags Flags = D3D12 \_ root \_ Signature \_ Flag \_ None)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

Uint numparameters

[**D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) Pparameters-Stamm Parameter \* \_

Opt Uint numstaticsamplers = 0

Opt [**D3D12 \_ Statischer \_ Sampler- \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pstaticsamplers = NULL

Opt [**D3D12 \_ Flags für root \_ Signature \_ Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = \_ D3D12 \_ root Signature \_ Flag \_ None

</dd> <dt>

**static Inline init (D3D12 \_ root \_ Signature \_ DESC &DESC, uint numparameters, Konstanten D3D12 \_ root \_ Parameter \* \_ pparameters, uint numstaticsamplers = 0, Konstanten D3D12 \_ static \_ Sampler \_ DESC \* \_ pstaticsamplers = NULL, D3D12 \_ root \_ Signature \_ Flags Flags = D3D12 \_ root \_ Signature \_ Flag \_ None)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

[**D3D12 \_ Stamm \_ Signatur \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) &DESC

Uint numparameters

[**D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) Pparameters-Stamm Parameter \* \_

Opt Uint numstaticsamplers = 0

Opt [**D3D12 \_ Statischer \_ Sampler- \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pstaticsamplers = NULL

Opt [**D3D12 \_ Flags für root \_ Signature \_ Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = \_ D3D12 \_ root Signature \_ Flag \_ None

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D3D12 \_ Stamm \_ Signatur \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 






---
title: CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC -Struktur (D3dx12.h)
description: Eine Hilfsstruktur, um eine einfache Initialisierung einer D3D12 \_ VERSIONED \_ ROOT SIGNATURE \_ \_ DESC-Struktur zu ermöglichen.
ms.assetid: 4505C1CE-CAA5-4092-B990-75740A2B194C
keywords:
- CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC-Struktur
topic_type:
- apiref
api_name:
- CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b35c546dcfe5ed7c181dae3a9ae8baaa70aa05369ccb15e4cbd123ae92d75b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118808530"
---
# <a name="cd3dx12_versioned_root_signature_desc-structure"></a>CD3DX12 \_ VERSIONED \_ ROOT SIGNATURE \_ \_ DESC-Struktur

Eine Hilfsstruktur, um eine einfache Initialisierung einer [**D3D12 \_ VERSIONED \_ ROOT SIGNATURE \_ \_ DESC-Struktur zu**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) ermöglichen.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC  : public D3D12_VERSIONED_ROOT_SIGNATURE_DESC{
       CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC();
       explicit CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(const D3D12_VERSIONED_ROOT_SIGNATURE_DESC &o);
       explicit CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(const D3D12_ROOT_SIGNATURE_DESC &o);
       explicit CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(const D3D12_ROOT_SIGNATURE_DESC1 &o);
       CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
       CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(UINT numParameters, const D3D12_ROOT_PARAMETER1* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
       CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(CD3DX12_DEFAULT);
  void inline Init_1_0(UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
  void static inline Init_1_0(D3D12_VERSIONED_ROOT_SIGNATURE_DESC &desc, UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
  void inline Init_1_1(UINT numParameters, const D3D12_ROOT_PARAMETER1* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
  void static inline Init_1_1(D3D12_VERSIONED_ROOT_SIGNATURE_DESC &desc, UINT numParameters, const D3D12_ROOT_PARAMETER1* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
};
```



## <a name="members"></a>Member

<dl> <dt>

**STAMMSIGNATUR \_ \_ DESC() MIT CD3DX12-VERSION \_ \_**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz einer CD3DX12 \_ VERSIONED \_ ROOT SIGNATURE \_ \_ DESC.

</dd> <dt>

**explicit CD3DX12 \_ VERSIONED \_ ROOT SIGNATURE \_ \_ DESC(const D3D12 \_ VERSIONED ROOT SIGNATURE \_ \_ \_ DESC &o)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12 VERSIONED ROOT SIGNATURE DESC, initialisiert mit dem Inhalt einer \_ \_ \_ \_ [**D3D12 \_ VERSIONED \_ ROOT SIGNATURE \_ \_ DESC-Struktur.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc)

</dd> <dt>

**explicit CD3DX12 \_ VERSIONED \_ ROOT SIGNATURE \_ \_ DESC(const D3D12 \_ ROOT SIGNATURE \_ \_ DESC &o)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12 VERSIONED ROOT SIGNATURE DESC, initialisiert mit dem Inhalt einer \_ \_ \_ \_ [**D3D12 \_ ROOT \_ SIGNATURE \_ DESC-Struktur.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc)

</dd> <dt>

**explicit CD3DX12 \_ VERSIONED \_ ROOT SIGNATURE \_ \_ DESC(const D3D12 \_ ROOT SIGNATURE \_ \_ DESC1 &o)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12 VERSIONED ROOT SIGNATURE DESC, initialisiert mit dem Inhalt einer \_ \_ \_ \_ [**D3D12 \_ ROOT \_ SIGNATURE \_ DESC1-Struktur.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc1)

</dd> <dt>

**CD3DX12 \_ VERSIONED \_ ROOT \_ SIGNATURE \_ DESC(UINT numParameters, const D3D12 \_ ROOT \_ PARAMETER \* \_ pParameters, UINT numStaticSamplers = 0, const D3D12 \_ STATIC \_ SAMPLER \_ DESC \* \_ pStaticSamplers = NULL, D3D12 \_ ROOT \_ SIGNATURE \_ FLAGS flags = D3D12 \_ ROOT \_ SIGNATURE \_ FLAG \_ NONE)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12 \_ VERSIONED \_ ROOT SIGNATURE \_ \_ DESC und initialisiert die folgenden Parameter:

UINT numParameters

const [**D3D12 \_ ROOT \_ PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters

UINT numStaticSamplers = 0

const [**D3D12 \_ STATIC \_ SAMPLER \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = NULL

[**D3D12 \_ ROOT \_ SIGNATURE \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12 \_ ROOT \_ SIGNATURE \_ FLAG \_ NONE

</dd> <dt>

**CD3DX12 \_ VERSIONED \_ ROOT \_ SIGNATURE \_ DESC(UINT numParameters, const D3D12 \_ ROOT \_ PARAMETER1 \* \_ pParameters, UINT numStaticSamplers = 0, const D3D12 \_ STATIC \_ SAMPLER \_ DESC \* \_ pStaticSamplers = NULL, D3D12 \_ ROOT \_ SIGNATURE \_ FLAGS flags = D3D12 \_ ROOT \_ SIGNATURE \_ FLAG \_ NONE)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12 \_ VERSIONED \_ ROOT SIGNATURE \_ \_ DESC und initialisiert die folgenden Parameter:

UINT numParameters

const [**D3D12 \_ ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters

UINT numStaticSamplers = 0

const [**D3D12 \_ STATIC \_ SAMPLER \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = NULL

[**D3D12 \_ ROOT \_ SIGNATURE \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12 \_ ROOT \_ SIGNATURE \_ FLAG \_ NONE

</dd> <dt>

**CD3DX12 \_ ROOT \_ SIGNATURE \_ \_ DESC (CD3DX12 \_ DEFAULT)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12 \_ VERSIONED \_ ROOT SIGNATURE \_ \_ DESC, initialisiert mit den Standardparametern:

UINT numParameters = 0

const [**D3D12 \_ ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters = NULL

UINT numStaticSamplers = 0

const [**D3D12 \_ STATIC \_ SAMPLER \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = NULL

[**D3D12 \_ ROOT \_ SIGNATURE \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12 \_ ROOT \_ SIGNATURE \_ FLAG \_ NONE

</dd> <dt>

**inline Init \_ 1 \_ 0(UINT numParameters, const D3D12 \_ ROOT PARAMETER \_ \* \_ pParameters, UINT numStaticSamplers = 0, const D3D12 \_ STATIC \_ SAMPLER \_ DESC \* \_ pStaticSamplers = NULL, D3D12 \_ ROOT SIGNATURE \_ \_ FLAGS flags = D3D12 \_ ROOT SIGNATURE FLAG \_ \_ \_ NONE)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

UINT numParameters

const [**D3D12 \_ ROOT \_ PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters

UINT numStaticSamplers = 0

const [**D3D12 \_ STATIC \_ SAMPLER \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = NULL

[**D3D12 \_ ROOT \_ SIGNATURE \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12 \_ ROOT \_ SIGNATURE \_ FLAG \_ NONE

</dd> <dt>

**static inline Init \_ 1 \_ 0(D3D12 \_ VERSIONED \_ ROOT SIGNATURE \_ \_ DESC &desc, UINT numParameters, const D3D12 \_ ROOT PARAMETER \_ \* \_ pParameters, UINT numStaticSamplers = 0, const D3D12 STATIC \_ \_ SAMPLER \_ DESC \* \_ pStaticSamplers = NULL, D3D12 \_ ROOT SIGNATURE \_ \_ FLAGS flags = D3D12 \_ ROOT SIGNATURE FLAG \_ \_ \_ NONE)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

[**D3D12 \_ VERSIONED \_ ROOT \_ SIGNATURE \_ DESC &**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) desc

UINT numParameters

const [**D3D12 \_ ROOT \_ PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters

UINT numStaticSamplers = 0

const [**D3D12 \_ STATIC \_ SAMPLER \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = NULL

[**D3D12 \_ ROOT \_ SIGNATURE \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12 \_ ROOT \_ SIGNATURE \_ FLAG \_ NONE

</dd> <dt>

**inline Init \_ 1 \_ 1(UINT numParameters, const D3D12 \_ ROOT \_ PARAMETER1 \* \_ pParameters, UINT numStaticSamplers = 0, const D3D12 \_ STATIC \_ SAMPLER \_ DESC \* \_ pStaticSamplers = NULL, D3D12 \_ ROOT SIGNATURE \_ \_ FLAGS flags = D3D12 \_ ROOT SIGNATURE FLAG \_ \_ \_ NONE)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

UINT numParameters

const [**D3D12 \_ ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters

UINT numStaticSamplers = 0

const [**D3D12 \_ STATIC \_ SAMPLER \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = NULL

[**D3D12 \_ ROOT \_ SIGNATURE \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12 \_ ROOT \_ SIGNATURE \_ FLAG \_ NONE

</dd> <dt>

**static inline Init \_ 1 \_ 1(D3D12 \_ \_ VERSIONED ROOT \_ SIGNATURE \_ DESC &desc, UINT numParameters, const D3D12 \_ ROOT \_ PARAMETER1 \* \_ pParameters, UINT numStaticSamplers = 0, const D3D12 \_ STATIC \_ SAMPLER \_ DESC \* \_ pStaticSamplers = NULL, D3D12 \_ ROOT SIGNATURE \_ \_ FLAGS flags = D3D12 \_ ROOT SIGNATURE FLAG \_ \_ \_ NONE)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

[**D3D12 \_ VERSIONED \_ ROOT \_ SIGNATURE \_ DESC &**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) desc

UINT numParameters

const [**D3D12 \_ ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters

UINT numStaticSamplers = 0

const [**D3D12 \_ STATIC \_ SAMPLER \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = NULL

[**D3D12 \_ ROOT \_ SIGNATURE \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12 \_ ROOT \_ SIGNATURE \_ FLAG \_ NONE

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**STAMMSIGNATUR-DESC MIT D3D12-VERSION \_ \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 






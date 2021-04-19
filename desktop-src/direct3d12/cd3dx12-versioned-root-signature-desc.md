---
title: CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC-Struktur (D3dx12. h)
description: Eine hilfsstruktur, mit der die einfache Initialisierung einer mit D3D12 \_ versionierten Stamm \_ \_ Signatur- \_ DESC-Struktur ermöglicht wird.
ms.assetid: 4505C1CE-CAA5-4092-B990-75740A2B194C
keywords:
- CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC Struktur
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
ms.openlocfilehash: 695b60fef5aba124ce4e6f2ff729fdb9362c7b2c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366618"
---
# <a name="cd3dx12_versioned_root_signature_desc-structure"></a>CD3DX12-Struktur der Stamm \_ \_ \_ Signatur \_ DESC

Eine hilfsstruktur, mit der die einfache Initialisierung einer mit [**D3D12 \_ versionierten Stamm \_ Signatur- \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) -Struktur ermöglicht wird.

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

**CD3DX12 mit \_ versionierter Stamm \_ \_ Signatur \_ DESC ()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz einer Stamm \_ \_ \_ Signatur DESC mit CD3DX12 Versionierung \_ .

</dd> <dt>

**explizit CD3DX12 \_ versionierte \_ Stamm \_ Signatur \_ DESC (konstant D3D12 \_ versionierte Stamm \_ \_ Signatur \_ DESC &o)**
</dt> <dd>

Erstellt eine neue Instanz einer mit CD3DX12 \_ versionierten Stamm \_ \_ Signatur \_ DESC, die mit dem Inhalt einer mit [**D3D12 \_ versionierten Stamm \_ \_ Signatur \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) -Struktur initialisiert wird.

</dd> <dt>

**explizit CD3DX12 \_ versionierte \_ Stamm \_ Signatur \_ DESC (konstant D3D12 Stamm \_ \_ Signatur \_ DESC &o)**
</dt> <dd>

Erstellt eine neue Instanz einer mit CD3DX12 \_ versionierten Stamm \_ \_ Signatur \_ DESC, die mit dem Inhalt einer D3D12-Stamm [**\_ \_ Signatur \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) -Struktur initialisiert wird.

</dd> <dt>

**explizit CD3DX12 \_ versionierte \_ Stamm \_ Signatur \_ DESC (konstant D3D12 Stamm \_ \_ Signatur \_ DESC1 &o)**
</dt> <dd>

Erstellt eine neue Instanz einer mit CD3DX12 \_ versionierten Stamm \_ \_ Signatur \_ DESC, die mit dem Inhalt einer [**D3D12 \_ root \_ Signature \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc1) -Struktur initialisiert wird.

</dd> <dt>

**CD3DX12-Stamm \_ \_ \_ Signatur \_ DESC (uint numparameters, Konstanten D3D12 \_ root \_ Parameter \* \_ pparameters, uint numstaticsamplers = 0, Konstanten D3D12 \_ statischer \_ Sampler \_ DESC \* \_ pstaticsamplers = NULL, D3D12 \_ root \_ Signature \_ Flags Flags = D3D12 \_ root \_ Signature \_ Flag \_ None)**
</dt> <dd>

Erstellt eine neue Instanz einer mit CD3DX12 \_ versionierten Stamm \_ \_ Signatur \_ DESC und initialisiert die folgenden Parameter:

Uint numparameters

Konstanten [**D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pparameters für Stamm Parameter

Uint numstaticsamplers = 0

Konstanten [**D3D12 \_ statischer \_ Sampler \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pstaticsamplers = NULL

[**D3D12 \_ Flags für root \_ Signature \_ Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = \_ D3D12 \_ root Signature \_ Flag \_ None

</dd> <dt>

**CD3DX12 mit \_ versionierter Stamm \_ \_ Signatur \_ DESC (uint numparameters, Konstanten D3D12 \_ root \_ PARAMETER1 \* \_ pparameters, uint numstaticsamplers = 0, Konstanten D3D12 \_ static \_ Sampler \_ DESC \* \_ pstaticsamplers = NULL, D3D12 \_ root \_ Signature \_ Flags Flags = D3D12 \_ root \_ Signature \_ Flag \_ None)**
</dt> <dd>

Erstellt eine neue Instanz einer mit CD3DX12 \_ versionierten Stamm \_ \_ Signatur \_ DESC und initialisiert die folgenden Parameter:

Uint numparameters

Konstanten [**D3D12 \_ root \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pparameters

Uint numstaticsamplers = 0

Konstanten [**D3D12 \_ statischer \_ Sampler \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pstaticsamplers = NULL

[**D3D12 \_ Flags für root \_ Signature \_ Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = \_ D3D12 \_ root Signature \_ Flag \_ None

</dd> <dt>

**CD3DX12 mit \_ versionierter Stamm \_ \_ Signatur \_ DESC (CD3DX12 \_ Standard)**
</dt> <dd>

Erstellt eine neue Instanz einer mit CD3DX12 \_ versionierten Stamm \_ \_ Signatur \_ DESC, die mit den Standardparametern initialisiert wird:

Uint numparameters = 0

Konstanten [**D3D12 \_ root \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pparameters = NULL

Uint numstaticsamplers = 0

Konstanten [**D3D12 \_ statischer \_ Sampler \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pstaticsamplers = NULL

[**D3D12 \_ Flags für root \_ Signature \_ Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = \_ D3D12 \_ root Signature \_ Flag \_ None

</dd> <dt>

**Inline-init \_ 1 \_ 0 (uint numparameters, Konstanten D3D12 \_ root \_ Parameter \* \_ pparameters, uint numstaticsamplers = 0, Konstanten D3D12 \_ statischer \_ Sampler \_ DESC \* \_ pstaticsamplers = NULL, D3D12 \_ root \_ Signature \_ Flags Flags = D3D12 \_ root \_ Signature \_ Flag \_ None)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

Uint numparameters

Konstanten [**D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pparameters für Stamm Parameter

Uint numstaticsamplers = 0

Konstanten [**D3D12 \_ statischer \_ Sampler \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pstaticsamplers = NULL

[**D3D12 \_ Flags für root \_ Signature \_ Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = \_ D3D12 \_ root Signature \_ Flag \_ None

</dd> <dt>

**static Inline init \_ 1 \_ 0 (D3D12 mit Versions Angabe Stamm \_ \_ \_ Signatur \_ DESC &DESC, uint numparameters, Konstanten D3D12 \_ root \_ Parameter \* \_ pparameters, uint numstaticsamplers = 0, Konstanten D3D12 \_ static \_ Sampler \_ DESC \* \_ pstaticsamplers = NULL, D3D12 \_ root \_ Signature \_ Flags Flags = D3D12 \_ root \_ Signature \_ Flag \_ None)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

[**D3D12 \_ \_ \_ \_ DESC mit Versions**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) Angabe für Stamm Signatur &DESC

Uint numparameters

Konstanten [**D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pparameters für Stamm Parameter

Uint numstaticsamplers = 0

Konstanten [**D3D12 \_ statischer \_ Sampler \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pstaticsamplers = NULL

[**D3D12 \_ Flags für root \_ Signature \_ Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = \_ D3D12 \_ root Signature \_ Flag \_ None

</dd> <dt>

**Inline-init \_ 1 \_ 1 (uint numparameters, Konstanten D3D12 \_ root \_ PARAMETER1 \* \_ pparameters, uint numstaticsamplers = 0, Konstanten D3D12 \_ statischer \_ Sampler \_ DESC \* \_ pstaticsamplers = NULL, D3D12 \_ root \_ Signature \_ Flags Flags = D3D12 \_ root \_ Signature \_ Flag \_ None)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

Uint numparameters

Konstanten [**D3D12 \_ root \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pparameters

Uint numstaticsamplers = 0

Konstanten [**D3D12 \_ statischer \_ Sampler \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pstaticsamplers = NULL

[**D3D12 \_ Flags für root \_ Signature \_ Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = \_ D3D12 \_ root Signature \_ Flag \_ None

</dd> <dt>

**static Inline init \_ 1 \_ 1 (D3D12 mit Versions Angabe Stamm \_ \_ \_ Signatur \_ DESC &DESC, uint numparameters, Konstanten D3D12 \_ root \_ PARAMETER1 \* \_ pparameters, uint numstaticsamplers = 0, Konstanten D3D12 \_ statischer \_ Sampler \_ DESC \* \_ pstaticsamplers = NULL, D3D12 \_ root \_ Signature \_ Flags Flags = D3D12 \_ root \_ Signature \_ Flag \_ None)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

[**D3D12 \_ \_ \_ \_ DESC mit Versions**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) Angabe für Stamm Signatur &DESC

Uint numparameters

Konstanten [**D3D12 \_ root \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pparameters

Uint numstaticsamplers = 0

Konstanten [**D3D12 \_ statischer \_ Sampler \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pstaticsamplers = NULL

[**D3D12 \_ Flags für root \_ Signature \_ Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = \_ D3D12 \_ root Signature \_ Flag \_ None

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D3D12 mit \_ versionierter Stamm \_ \_ Signatur \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 






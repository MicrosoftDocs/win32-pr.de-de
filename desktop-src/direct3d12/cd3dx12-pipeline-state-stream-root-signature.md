---
title: CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE-Struktur (D3dx12. h)
description: Eine hilfsstruktur, die verwendet wird, um die Stamm Signatur als einzelnes Objekt zu beschreiben, das für eine Datenstrom Beschreibung geeignet ist.
ms.assetid: 351A78DC-9BDE-43B4-9A72-D65EE15CA441
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE Struktur
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61a97402fa267693de23ed2085b3d41973dc409e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363183"
---
# <a name="cd3dx12_pipeline_state_stream_root_signature-structure"></a>CD3DX12 \_ Pipeline \_ State-Datenstrom Stamm \_ \_ \_ Signatur Struktur

Eine hilfsstruktur, die verwendet wird, um die Stamm Signatur als einzelnes Objekt zu beschreiben, das für eine Datenstrom Beschreibung geeignet ist.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE {
                                               CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE;
                                               CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE(ID3D12RootSignature* const &i);
  CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE operator=(ID3D12RootSignature* const& i);
                                               operator ID3D12RootSignature*() const;
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ Pipeline-Statusdaten Strom-Stamm \_ \_ \_ \_ Signatur**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz einer CD3DX12 Pipeline- \_ Zustandsdaten Strom-Stamm \_ \_ \_ \_ Signatur.

</dd> <dt>

**CD3DX12 \_ Pipeline-Statusdaten Strom-Stamm \_ \_ \_ \_ Signatur (ID3D12RootSignature-Konstante \* &i)**
</dt> <dd>

Erstellt eine neue Instanz einer CD3DX12 \_ Pipeline- \_ Zustands \_ Datenstrom-Stamm \_ \_ Signatur, initialisiert mit einem untergeordneten Typ der Stamm Signatur des untergeordneten **D3D12 \_ Pipeline \_ State \_ \_ \_ \_** - *untergeordneten* Typs und aus einer [**ID3D12RootSignature**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignature) -Struktur kopierten untergeordneten Daten.

</dd> <dt>

**Operator = (ID3D12RootSignature \* Konstanten& i)**
</dt> <dd>

Kopier Zuweisungs Operator.

</dd> <dt>

**Operator ID3D12RootSignature \* () konstant**
</dt> <dd>

Implizite Konvertierung in einen [**ID3D12RootSignature**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignature) -Struktur Zeiger.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

\_Die CD3DX12 \_ -Stamm \_ Signatur des Pipeline Zustands Stroms \_ \_ ist eine typedef-Spezialisierung der untergeordneten Pipeline für den [**CD3DX12 \_ Pipeline \_ State \_ Stream \_**](cd3dx12-pipeline-state-stream-subobject.md) und ist wie folgt definiert:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<ID3D12RootSignature*, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_ROOT_SIGNATURE>
    CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE;
          
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**CD3DX12 \_ Pipeline State-Datenstrom-unter \_ \_ \_ Objekt**](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[**D3D12 \_ Pipeline \_ Status-unter Objekt- \_ \_ Typ**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 


---
title: ID3D12Resource GetDesc-Methode
description: Ruft die Ressourcenbeschreibung ab.
ms.assetid: B8D84D69-6B13-4E86-8EF6-A841354B1E5C
keywords:
- GetDesc-Methode
- GetDesc-Methode, ID3D12Resource-Schnittstelle
- ID3D12Resource-Schnittstelle, GetDesc-Methode
topic_type:
- apiref
api_name:
- ID3D12Resource.GetDesc
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
api_location:
- d3d12.h
ms.openlocfilehash: 179acfa051212a2f98eb94441cbfad9fd7d9bbab47e4616f82a4f4cff3d41035
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069630"
---
# <a name="id3d12resourcegetdesc-method"></a>ID3D12Resource::GetDesc-Methode

Ruft die Ressourcenbeschreibung ab.

## <a name="syntax"></a>Syntax


```C++
D3D12_RESOURCE_DESC GetDesc();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3D12 \_ RESOURCE \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc)**

Eine Direct3D 12-Ressourcenbeschreibungsstruktur.

## <a name="examples"></a>Beispiele

Gibt die erforderliche Größe eines Puffers zurück, der für den Datenupload verwendet werden soll.


```C++
// Returns required size of a buffer to be used for data upload
inline UINT64 GetRequiredIntermediateSize(
    _In_ ID3D12Resource* pDestinationResource,
    _In_range_(0,D3D12_REQ_SUBRESOURCES) UINT FirstSubresource,
    _In_range_(0,D3D12_REQ_SUBRESOURCES-FirstSubresource) UINT NumSubresources)
{
    D3D12_RESOURCE_DESC Desc = pDestinationResource->GetDesc();
    UINT64 RequiredSize = 0;
    
    ID3D12Device* pDevice;
    pDestinationResource->GetDevice(__uuidof(*pDevice), reinterpret_cast<void**>(&pDevice));
    pDevice->GetCopyableFootprints(&Desc, FirstSubresource, NumSubresources, 0, nullptr, nullptr, nullptr, &RequiredSize);
    pDevice->Release();
    
    return RequiredSize;
}
```



Weitere Informationen finden Sie [im Beispielcode in der D3D12-Referenz.](notes-on-example-code.md)

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)
</dt> </dl>

 

 





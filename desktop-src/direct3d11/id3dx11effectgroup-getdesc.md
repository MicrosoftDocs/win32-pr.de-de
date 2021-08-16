---
title: ID3DX11EffectGroup GetDesc-Methode (D3dx11effect.h)
description: Ruft eine Gruppenbeschreibung ab.
ms.assetid: 04bb707a-be21-43d1-8d9d-5a84d29fda74
keywords:
- GetDesc-Methode Direct3D 11
- GetDesc-Methode Direct3D 11, ID3DX11EffectGroup-Schnittstelle
- ID3DX11EffectGroup-Schnittstelle Direct3D 11 , GetDesc-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccbd7413748e19ca74b6663dd9ab775aa305bce741f458c86138050a919c5d1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118535512"
---
# <a name="id3dx11effectgroupgetdesc-method"></a>ID3DX11EffectGroup::GetDesc-Methode

Ruft eine Gruppenbeschreibung ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDesc(
   D3DX11_GROUP_DESC *pDesc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDesc* 
</dt> <dd>

Typ: **[ **D3DX11 \_ GROUP \_ DESC**](d3dx11-group-desc.md)\***

Ein Zeiger auf eine [**D3DX11 \_ GROUP \_ DESC-Struktur.**](d3dx11-group-desc.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Gibt einen der folgenden [Direct3D 11-Rückgabecodes zurück.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Hinweise

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit. Sie müssen die Quelle Effects 11 verwenden, um Ihre Effekttypanwendung zu erstellen. Weitere Informationen zur Verwendung der Quelle Effects 11 finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>Nicht verfügbar (eine Effects 11-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DX11EffectGroup](id3dx11effectgroup.md)
</dt> </dl>

 

 






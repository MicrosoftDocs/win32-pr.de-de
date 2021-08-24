---
title: ID3DX11Effect GetDesc-Methode (D3dx11effect.h)
description: Abrufen einer Effektbeschreibung.
ms.assetid: ca684786-c813-48d1-acad-e78aafd1c0db
keywords:
- GetDesc-Methode Direct3D 11
- GetDesc-Methode Direct3D 11 , ID3DX11Effect-Schnittstelle
- ID3DX11Effect-Schnittstelle Direct3D 11, GetDesc-Methode
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9461dafb6b8da66ffa2a84e0d9d61c119a67c33bd967ae5183252e875fb6192
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676950"
---
# <a name="id3dx11effectgetdesc-method"></a>ID3DX11Effect::GetDesc-Methode

Abrufen einer Effektbeschreibung.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDesc(
   D3DX11_EFFECT_DESC *pDesc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDesc* 
</dt> <dd>

Typ: **[ **D3DX11 \_ EFFECT \_ DESC**](d3dx11-effect-desc.md)\***

Ein Zeiger auf eine Effektbeschreibung (siehe [**D3DX11 \_ EFFECT \_ DESC**](d3dx11-effect-desc.md)).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Gibt einen der folgenden [Direct3D 11-Rückgabecodes zurück.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Hinweise

Eine Effektbeschreibung enthält grundlegende Informationen zu einem Effekt, z. B. die enthaltenen Techniken und die benötigten konstanten Pufferressourcen.

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte zur Verfügung. Sie müssen die Effects 11-Quelle verwenden, um ihre Effekte-Typ-Anwendung zu erstellen. Weitere Informationen zur Verwendung der Quelle Effects 11 finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>N/A (Eine Effects 11-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

 






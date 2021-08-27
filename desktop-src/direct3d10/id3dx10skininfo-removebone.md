---
description: Entfernen sie einen 160er.
ms.assetid: efb88108-5c76-47c8-b8ce-1ba29cb18ba4
title: ID3DX10SkinInfo::RemoveBone-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.RemoveBone
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8f26a19c0903056c6de62ae72852b19557b0926fe5b2616adfa8d77bd945cba4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119940"
---
# <a name="id3dx10skininforemovebone-method"></a>ID3DX10SkinInfo::RemoveBone-Methode

Entfernen sie einen 160er.

## <a name="syntax"></a>Syntax


```C++
HRESULT RemoveBone(
  [in] UINT Index
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Ein Index, der angibt, welches Element entfernt werden soll. Muss zwischen 0 und dem von [**ID3DX10SkinInfo::GetNumBones zurückgegebenen**](id3dx10skininfo-getnumbones.md)Wert sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert E \_ INVALIDARG sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX10SkinInfo](id3dx10skininfo.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

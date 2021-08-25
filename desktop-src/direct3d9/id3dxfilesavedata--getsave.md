---
description: Ruft einen Zeiger auf diesen ID3DXFileSaveObject-Dateidatenknoten ab.
ms.assetid: 092d1c6f-0a53-4b8e-84ec-bc76f3f647ac
title: ID3DXFileSaveData::GetSave-Methode (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.GetSave
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 05b30c34f7e9d1383270c06ee70aca63d3f24b0f4f721d6859366794f2df361a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856641"
---
# <a name="id3dxfilesavedatagetsave-method"></a>ID3DXFileSaveData::GetSave-Methode

Ruft einen Zeiger auf diesen [**ID3DXFileSaveObject-Dateidatenknoten**](id3dxfilesaveobject.md) ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSave(
  [out] ID3DXFileSaveObject **ppObj
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppObj* \[ out\]
</dt> <dd>

Typ: **[ **ID3DXFileSaveObject**](id3dxfilesaveobject.md)\*\***

Adresse eines Zeigers auf eine [**ID3DXFileSaveObject-Schnittstelle,**](id3dxfilesaveobject.md) die diesen Dateidatenknoten darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DXFERR \_ BADVALUE.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXFileSaveData](id3dxfilesavedata.md)
</dt> </dl>

 

 





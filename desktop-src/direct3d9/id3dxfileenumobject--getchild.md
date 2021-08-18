---
description: 'ID3DXFileEnumObject::GetChild-Methode: Ruft ein untergeordnetes Objekt in diesem Dateidatenobjekt ab.'
ms.assetid: d8f367dd-8858-48ae-9de5-17de1538aadf
title: ID3DXFileEnumObject::GetChild-Methode (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetChild
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 20075c0e30985ab4f5c7c691b40caf302db98d6b5c8cf863fd9c57fca895ee40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118802793"
---
# <a name="id3dxfileenumobjectgetchild-method"></a>ID3DXFileEnumObject::GetChild-Methode

Ruft ein untergeordnetes Objekt in diesem Dateidatenobjekt ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetChild(
  [in]  SIZE_T        id,
  [out] ID3DXFileData **ppObj
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*id* \[ in\]
</dt> <dd>

Typ: **[ **SIZE \_ T**](../winprog/windows-data-types.md)**

ID des abzurufenden untergeordneten Objekts.

</dd> <dt>

*ppObj* \[ out\]
</dt> <dd>

Typ: **[ **ID3DXFileData**](id3dxfiledata.md)\*\***

Adresse eines Zeigers zum Empfangen des Schnittstellenzeigers des untergeordneten Objekts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert einer der folgenden Sein: D3DXFERR \_ BADVALUE, D3DXFERR \_ NOMOREOBJECTS.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXFileEnumObject](id3dxfileenumobject.md)
</dt> </dl>

 

 

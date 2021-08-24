---
description: Ruft das Enumerationsobjekt in diesem Dateidatenobjekt ab.
ms.assetid: 383560e2-1888-4e37-9883-2ddbcb101cf6
title: ID3DXFileData::GetEnum-Methode (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetEnum
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 79ee6272f6b685c5e80b7c7b76b39925a08bb67cc07ba7af23a5b276b414f194
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748550"
---
# <a name="id3dxfiledatagetenum-method"></a>ID3DXFileData::GetEnum-Methode

Ruft das Enumerationsobjekt in diesem Dateidatenobjekt ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetEnum(
  [in] ID3DXFileEnumObject **ppObj
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppObj* \[ In\]
</dt> <dd>

Typ: **[ **ID3DXFileEnumObject**](id3dxfileenumobject.md)\*\***

Adresse eines Zeigers, der das Enumerationsobjekt in diesem Dateidatenobjekt empfangen soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DXFERR \_ BADVALUE.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXFileData](id3dxfiledata.md)
</dt> </dl>

 

 





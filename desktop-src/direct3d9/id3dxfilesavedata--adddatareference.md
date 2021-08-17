---
description: Fügt einen Datenverweis als untergeordnetes Element dieses ID3DXFileSaveData-Dateidatenknotens hinzu. Der Datenverweis verweist auf ein Dateidatenobjekt.
ms.assetid: 75bfe91e-15ea-41f3-b1f7-071fb7f0093f
title: ID3DXFileSaveData::AddDataReference-Methode (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.AddDataReference
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 862df88701cffd1059ca67e086cd49d05174bc66e9fa13807df2d2aeb0c9ff1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121349"
---
# <a name="id3dxfilesavedataadddatareference-method"></a>ID3DXFileSaveData::AddDataReference-Methode

Fügt einen Datenverweis als untergeordnetes Element dieses [**ID3DXFileSaveData-Dateidatenknotens**](id3dxfilesavedata.md) hinzu. Der Datenverweis verweist auf ein Dateidatenobjekt.

## <a name="syntax"></a>Syntax


```C++
HRESULT AddDataReference(
  [in]       LPCSTR szName,
  [in] const GUID   *pId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*szName* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Zeiger auf den Namen des Datenobjekts, das als Verweis hinzugefügt werden soll. Geben Sie **NULL** an, wenn das Datenobjekt keinen Namen hat.

</dd> <dt>

*pId* \[ In\]
</dt> <dd>

Typ: **const [**GUID**](guid.md) \***

Zeiger auf eine GUID, die das datenobjekt darstellt, das als Verweis hinzugefügt werden soll. Wenn **NULL,** wird ein Verweis hinzugefügt, der auf das Datenobjekt mit dem von szName angegebenen Namen verweist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Sein: D3DXFERR \_ BADOBJECT, D3DXFERR \_ BADVALUE, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Das Dateidatenobjekt, auf das verwiesen wird, muss entweder einen Namen oder eine GUID aufweisen. Das Dateidatenobjekt muss auch von einem anderen übergeordneten [**ID3DXFileSaveData-Objekt**](id3dxfilesavedata.md) abgeleitet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXFileSaveData](id3dxfilesavedata.md)
</dt> </dl>

 

 

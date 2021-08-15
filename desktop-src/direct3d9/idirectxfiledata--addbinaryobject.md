---
description: Erstellt ein binäres -Objekt und fügt es als untergeordnetes Objekt hinzu. Veraltet.
ms.assetid: 6164951d-dd87-4318-ac08-b97c22f58d45
title: IDirectXFileData::AddBinaryObject-Methode (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.AddBinaryObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 3d619fde6cd5d22f161188d46f710caeadfaedba2fbcf1167486e05dee539fd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728976"
---
# <a name="idirectxfiledataaddbinaryobject-method"></a>IDirectXFileData::AddBinaryObject-Methode

Erstellt ein binäres -Objekt und fügt es als untergeordnetes Objekt hinzu. Veraltet.

## <a name="syntax"></a>Syntax


```C++
HRESULT AddBinaryObject(
  [in]       LPCSTR szName,
  [in] const GUID   *pguid,
  [in]       LPCSTR szMimeType,
  [in]       LPVOID pvData,
  [in]       DWORD  cbSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*szName* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Zeiger auf den Namen des Objekts. Geben **Sie NULL** an, wenn das Objekt keinen Namen benötigt.

</dd> <dt>

*pguid* \[ In\]
</dt> <dd>

Typ: **const [**GUID**](guid.md) \***

Zeiger auf die GUID, die das Objekt darstellt. Geben **Sie NULL** an, wenn das Objekt keine GUID benötigt.

</dd> <dt>

*szMimeType* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Zeiger auf den MIME-Typ des Objekts.

</dd> <dt>

*pvData* \[ In\]
</dt> <dd>

Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**

Zeiger auf die Daten des Objekts.

</dd> <dt>

*cbSize* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Die Größe des Puffers, auf den pvData zeigt, in Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert DXFILE \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert einer der folgenden Werte sein. DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IDirectXFileData](idirectxfiledata.md)
</dt> <dt>

[**IDirectXFileBinary::GetMimeType**](idirectxfilebinary--getmimetype.md)
</dt> </dl>

 

 

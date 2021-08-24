---
description: Fügt ein Datenobjekt als untergeordnetes Element des Dateidatenknotens ID3DXFileSaveData hinzu.
ms.assetid: 47faad99-3ee8-4ca8-b8d7-413d4cd5b090
title: ID3DXFileSaveData::AddDataObject-Methode (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.AddDataObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: ed4b0abd35f9f53fb2111f40903e4b2b81a75c9d402a53fbb2fdb1cdc9a75750
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847840"
---
# <a name="id3dxfilesavedataadddataobject-method"></a>ID3DXFileSaveData::AddDataObject-Methode

Fügt ein Datenobjekt als untergeordnetes Element des Dateidatenknotens [**ID3DXFileSaveData**](id3dxfilesavedata.md) hinzu.

## <a name="syntax"></a>Syntax


```C++
HRESULT AddDataObject(
  [in]               REFGUID           rguidTemplate,
  [in]               LPCSTR            szName,
  [in]         const GUID              *pId,
  [in]               SIZE_T            cbSize,
  [in]               LPCVOID           pvData,
  [in, retval]       ID3DXFileSaveData **ppObj
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*rguidTemplate* \[ In\]
</dt> <dd>

Typ: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**

GUID, die die Vorlage des Datenobjekts darstellt.

</dd> <dt>

*szName* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Zeiger auf den Namen des hinzuzufügende Datenobjekts. Geben Sie **NULL** an, wenn das Objekt keinen Namen hat.

</dd> <dt>

*pId* \[ In\]
</dt> <dd>

Typ: **const [**GUID**](guid.md) \***

Zeiger auf eine GUID, die das Datenobjekt darstellt. Das Datenobjekt muss mit [**ID3DXFile::RegisterTemplates**](id3dxfile--registertemplates.md) oder [**ID3DXFile::RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md)registriert worden sein. Geben Sie **NULL** an, wenn das Objekt über keine GUID verfügt.

</dd> <dt>

*cbSize* \[ In\]
</dt> <dd>

Typ: **[ **SIZE \_ T**](../winprog/windows-data-types.md)**

Größe des Datenobjekts in Bytes.

</dd> <dt>

*pvData* \[ In\]
</dt> <dd>

Typ: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Zeiger auf einen Puffer, der alle erforderlichen Daten im Datenobjekt enthält.

</dd> <dt>

*ppObj* \[ in, retval\]
</dt> <dd>

Typ: **[ **ID3DXFileSaveData**](id3dxfilesavedata.md)\*\***

Adresse eines Zeigers auf eine [**ID3DXFileSaveData-Schnittstelle,**](id3dxfilesavedata.md) die den Dateidatenknoten darstellt, dem das Datenobjekt hinzugefügt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Sein: D3DXFERR \_ BADOBJECT, D3DXFERR \_ BADVALUE, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXFileSaveData](id3dxfilesavedata.md)
</dt> </dl>

 

 

---
description: Fügt ein Datenobjekt als untergeordnetes Element des ID3DXFileSaveData-Objekts hinzu.
ms.assetid: 710a1588-d766-4555-97a3-4b5a517ce805
title: ID3DXFileSaveObject::AddDataObject-Methode (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveObject.AddDataObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 8a1bdea820b90ae68c819ae2755f2abecd892cfd362116f6da37cb643a254048
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118802415"
---
# <a name="id3dxfilesaveobjectadddataobject-method"></a>ID3DXFileSaveObject::AddDataObject-Methode

Fügt ein Datenobjekt als untergeordnetes Element des [**ID3DXFileSaveData-Objekts**](id3dxfilesavedata.md) hinzu.

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

Zeiger auf den Namen des Datenobjekts. Geben Sie **NULL** an, wenn das Objekt keinen Namen hat.

</dd> <dt>

*pId* \[ In\]
</dt> <dd>

Typ: **const [**GUID**](guid.md) \***

Zeiger auf eine GUID, die das Datenobjekt darstellt. Geben Sie **NULL** an, wenn das Objekt über keine GUID verfügt.

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

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Sein: D3DXFERR \_ BADOBJECT, DXFILEERR \_ BADVALUE, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Wenn ein Datenverweisobjekt auf das Datenobjekt verweist, muss der szName- oder pId-Parameter ungleich **NULL** sein.

Speichern Sie die erstellten Daten mithilfe der [**ID3DXFileSaveObject::Save-Methode**](id3dxfilesaveobject--save.md) auf dem Datenträger.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXFileSaveObject](id3dxfilesaveobject.md)
</dt> </dl>

 

 

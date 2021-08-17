---
description: Erstellt ein Datenobjekt. Veraltet.
ms.assetid: bb0ef2cf-db76-40f6-968f-3599c58459a7
title: IDirectXFileSaveObject::CreateDataObject-Methode (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject.CreateDataObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: e1497ad06919833e0ba716877dc81b8df51a99361a49e43fa9a0f756e296040c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728912"
---
# <a name="idirectxfilesaveobjectcreatedataobject-method"></a>IDirectXFileSaveObject::CreateDataObject-Methode

Erstellt ein Datenobjekt. Veraltet.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateDataObject(
  [in]                REFGUID           rguidTemplate,
  [in]                LPCSTR            szName,
  [in]          const GUID              *pguid,
  [in]                DWORD             cbSize,
  [in]                LPVOID            pvData,
  [out, retval]       LPDIRECTXFILEDATA *ppDataObj
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

*pguid* \[ In\]
</dt> <dd>

Typ: **const [**GUID**](guid.md) \***

Zeiger auf eine GUID, die das Datenobjekt darstellt. Geben Sie **NULL** an, wenn das Objekt über keine GUID verfügt.

</dd> <dt>

*cbSize* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Größe des Datenobjekts in Bytes.

</dd> <dt>

*pvData* \[ In\]
</dt> <dd>

Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**

Zeiger auf einen Puffer, der alle erforderlichen Memberdaten enthält.

</dd> <dt>

*ppDataObj* \[ out, retval\]
</dt> <dd>

Typ: **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)\***

Adresse eines Zeigers auf eine [**IDirectXFileData-Schnittstelle,**](idirectxfiledata.md) die das erstellte Dateidatenobjekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert DXFILE \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein. DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE

## <a name="remarks"></a>Hinweise

Wenn ein Datenverweisobjekt auf das Datenobjekt verweist, muss der szName- oder pguid-Parameter ungleich **NULL** sein.

Speichern Sie alle Vorlagen mithilfe der [**IDirectXFileSaveObject::SaveTemplates-Methode,**](idirectxfilesaveobject--savetemplates.md) bevor Sie die von dieser Methode erstellten Daten speichern. Speichern Sie die erstellten Daten mithilfe der [**IDirectXFileSaveObject::SaveData-Methode.**](idirectxfilesaveobject--savedata.md)

Wenn Sie optionale Daten speichern müssen, verwenden Sie die [**IDirectXFileData::AddDataObject-Methode**](idirectxfiledata--adddataobject.md) nach der Verwendung dieser Methode und vor der Verwendung von [**IDirectXFileSaveObject::SaveData**](idirectxfilesaveobject--savedata.md). Wenn das Objekt über untergeordnete Objekte verfügt, fügen Sie diese hinzu, bevor **Sie IDirectXFileSaveObject::SaveData** aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IDirectXFileSaveObject](idirectxfilesaveobject.md)
</dt> <dt>

[**IDirectXFileData::AddDataObject**](idirectxfiledata--adddataobject.md)
</dt> <dt>

[**IDirectXFileSaveObject::SaveData**](idirectxfilesaveobject--savedata.md)
</dt> <dt>

[**IDirectXFileSaveObject::SaveTemplates**](idirectxfilesaveobject--savetemplates.md)
</dt> </dl>

 

 

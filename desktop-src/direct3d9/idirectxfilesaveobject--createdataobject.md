---
description: Erstellt ein Datenobjekt. Veraltet.
ms.assetid: bb0ef2cf-db76-40f6-968f-3599c58459a7
title: 'Idirectxfilesaveobject:: kreatedataobject-Methode (dxfile. h)'
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
ms.openlocfilehash: 7c5a67a72f6ff5a63730167d2fe2d12213a9ab72
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354676"
---
# <a name="idirectxfilesaveobjectcreatedataobject-method"></a>Idirectxfilesaveobject:: kreatedataobject-Methode

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

*rguidtemplate* \[ in\]
</dt> <dd>

Typ: **[reguid](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**

GUID, die die Vorlage des Datenobjekts darstellt.

</dd> <dt>

*szName* \[ in\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Zeiger auf den Namen des Datenobjekts. Geben Sie **null** an, wenn das Objekt keinen Namen hat.

</dd> <dt>

*pguid* \[ in\]
</dt> <dd>

Typ: Konstante **[**GUID**](guid.md) \***

Zeiger auf eine GUID, die das Datenobjekt darstellt. Geben Sie **null** an, wenn das Objekt nicht über eine GUID verfügt.

</dd> <dt>

*CBSIZE* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Größe des Datenobjekts in Bytes.

</dd> <dt>

*pvData* \[ in\]
</dt> <dd>

Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**

Zeiger auf einen Puffer, der alle erforderlichen Elementdaten enthält.

</dd> <dt>

*ppdataobj* \[ Out, retval\]
</dt> <dd>

Typ: **[ **lpdirectxfiledata**](idirectxfiledata.md)\***

Adresse eines Zeigers auf eine [**idirectxfiledata**](idirectxfiledata.md) -Schnittstelle, die das erstellte Datei Datenobjekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist dxfile OK der Rückgabewert \_ . Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein. dxfileerr \_ badzuweisung dxfileerr \_ badvalue

## <a name="remarks"></a>Bemerkungen

Wenn ein Daten Verweis Objekt auf das Datenobjekt verweist, muss der szName-Parameter oder der pguid-Parameter nicht **null** sein.

Speichern Sie alle Vorlagen, indem Sie die [**idirectxfilesaveobject:: savetemplates**](idirectxfilesaveobject--savetemplates.md) -Methode verwenden, bevor Sie die von dieser Methode erstellten Daten speichern. Speichern Sie die erstellten Daten mit der [**idirectxfilesaveobject:: SaveData**](idirectxfilesaveobject--savedata.md) -Methode.

Wenn Sie optionale Daten speichern müssen, verwenden Sie die [**idirectxfiledata:: adddataobject**](idirectxfiledata--adddataobject.md) -Methode, nachdem Sie diese Methode und vor der Verwendung von [**idirectxfilesaveobject:: SaveData**](idirectxfilesaveobject--savedata.md)verwendet haben. Wenn das Objekt über untergeordnete Objekte verfügt, fügen Sie diese vor dem Aufruf von **idirectxfilesaveobject:: SaveData** hinzu.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Dxfile. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Idirectxfilesaveobject](idirectxfilesaveobject.md)
</dt> <dt>

[**Idirectxfiledata:: adddataobject**](idirectxfiledata--adddataobject.md)
</dt> <dt>

[**Idirectxfilesaveobject:: SaveData**](idirectxfilesaveobject--savedata.md)
</dt> <dt>

[**Idirectxfilesaveobject:: savetemplates**](idirectxfilesaveobject--savetemplates.md)
</dt> </dl>

 

 

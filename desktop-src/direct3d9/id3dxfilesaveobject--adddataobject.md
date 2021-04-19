---
description: Fügt ein Datenobjekt als untergeordnetes Element des ID3DXFileSaveData-Objekts hinzu.
ms.assetid: 710a1588-d766-4555-97a3-4b5a517ce805
title: 'ID3DXFileSaveObject:: adddataobject-Methode (D3DX9Xof. h)'
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
ms.openlocfilehash: d1586035a0d8a81c2210009bad903aac5197bcf7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353718"
---
# <a name="id3dxfilesaveobjectadddataobject-method"></a>ID3DXFileSaveObject:: adddataobject-Methode

Fügt ein Datenobjekt als untergeordnetes Element des [**ID3DXFileSaveData**](id3dxfilesavedata.md) -Objekts hinzu.

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

*pId* \[ in\]
</dt> <dd>

Typ: Konstante **[**GUID**](guid.md) \***

Zeiger auf eine GUID, die das Datenobjekt darstellt. Geben Sie **null** an, wenn das Objekt nicht über eine GUID verfügt.

</dd> <dt>

*CBSIZE* \[ in\]
</dt> <dd>

Typ: **[ **Größe \_ T**](../winprog/windows-data-types.md)**

Größe des Datenobjekts in Bytes.

</dd> <dt>

*pvData* \[ in\]
</dt> <dd>

Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)**

Zeiger auf einen Puffer, der alle erforderlichen Daten im Datenobjekt enthält.

</dd> <dt>

*ppobj* \[ in, retval\]
</dt> <dd>

Typ: **[ **ID3DXFileSaveData**](id3dxfilesavedata.md)\*\***

Adresse eines Zeigers auf eine [**ID3DXFileSaveData**](id3dxfilesavedata.md) -Schnittstelle, die den Datei Datenknoten darstellt, dem das Datenobjekt hinzugefügt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DXFERR \_ badobject, dxfileerr \_ badvalue, E \_ ouyfimemory.

## <a name="remarks"></a>Bemerkungen

Wenn ein Daten Verweis Objekt auf das Datenobjekt verweist, muss der szName-Parameter oder der pId-Parameter nicht **null** sein.

Speichern Sie die erstellten Daten mithilfe der [**ID3DXFileSaveObject:: Save**](id3dxfilesaveobject--save.md) -Methode auf dem Datenträger.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXFileSaveObject](id3dxfilesaveobject.md)
</dt> </dl>

 

 

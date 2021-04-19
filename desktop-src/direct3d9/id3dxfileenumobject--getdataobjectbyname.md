---
description: Ruft das Datenobjekt ab, das über den angegebenen Namen verfügt.
ms.assetid: ed53d871-24e8-4c51-8897-1055ef8a9af1
title: 'ID3DXFileEnumObject:: getdataobjectbyname-Methode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetDataObjectByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 41850615726ac15e890162c6e28df9b638c582a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364372"
---
# <a name="id3dxfileenumobjectgetdataobjectbyname-method"></a>ID3DXFileEnumObject:: getdataobjectbyname-Methode

Ruft das Datenobjekt ab, das über den angegebenen Namen verfügt.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDataObjectByName(
  [in]  LPCSTR        szName,
  [out] ID3DXFileData **ppObj
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*szName* \[ in\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Zeiger auf den angeforderten Namen.

</dd> <dt>

*ppobj* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **ID3DXFileData**](id3dxfiledata.md)\*\***

Adresse eines Zeigers auf eine [**ID3DXFileData**](id3dxfiledata.md) -Schnittstelle, die das zurückgegebene Datei Datenobjekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: dxfileerr \_ badvalue, dxfileerr \_ NotFound.

## <a name="remarks"></a>Bemerkungen

Rufen Sie den Namen szName des aktuellen Datei Datenobjekts mit der [**ID3DXFileData:: GetName**](id3dxfiledata--getname.md) -Methode ab.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXFileEnumObject](id3dxfileenumobject.md)
</dt> </dl>

 

 

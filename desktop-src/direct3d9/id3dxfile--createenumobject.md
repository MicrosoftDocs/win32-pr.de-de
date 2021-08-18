---
description: Erstellt ein Enumeratorobjekt, das eine X-Datei liest.
ms.assetid: 86d05eab-601c-4beb-9dbe-c23fa524871c
title: ID3DXFile::CreateEnumObject-Methode (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile.CreateEnumObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 528ab441da6cd4370de4ecad5d8490e6e74b5977672d0c7d4126cea1b7bab8fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044398"
---
# <a name="id3dxfilecreateenumobject-method"></a>ID3DXFile::CreateEnumObject-Methode

Erstellt ein Enumeratorobjekt, das eine X-Datei liest.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateEnumObject(
  [out] LPCVOID               pvSource,
  [in]  D3DXF_FILELOADOPTIONS loadflags,
  [out] ID3DXFileEnumObject   **ppEnumObj
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pvSource* \[ out\]
</dt> <dd>

Typ: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Die Datenquelle. Entweder:

-   Ein Dateiname
-   Eine [**D3DXF \_ FILELOADMEMORY-Struktur**](d3dxf-fileloadmemory.md)
-   Eine [**D3DXF \_ FILELOADRESOURCE-Struktur**](d3dxf-fileloadresource.md)

Abhängig vom Wert von loadflags.

</dd> <dt>

*loadflags* \[ In\]
</dt> <dd>

Typ: **[D3DXF \_ FILELOADOPTIONS](d3dxf.md)**

Wert, der die Quelle der Daten angibt. Dieser Wert kann eines der [D3DXF \_ FILELOADOPTIONS-Flags](d3dxf.md) sein.

</dd> <dt>

*ppEnumObj* \[ out\]
</dt> <dd>

Typ: **[ **ID3DXFileEnumObject**](id3dxfileenumobject.md)\*\***

Adresse eines Zeigers auf eine [**ID3DXFileEnumObject-Schnittstelle,**](id3dxfileenumobject.md) die das erstellte Enumeratorobjekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Sein: D3DXFERR \_ BADVALUE, D3DXFERR \_ PARSEERROR.

## <a name="remarks"></a>Hinweise

Verwenden Sie nach der Verwendung dieser Methode eine der [**ID3DXFileEnumObject-Methoden,**](id3dxfileenumobject.md) um ein Datenobjekt abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXFile](id3dxfile.md)
</dt> <dt>

[**ID3DXFileEnumObject**](id3dxfileenumobject.md)
</dt> </dl>

 

 

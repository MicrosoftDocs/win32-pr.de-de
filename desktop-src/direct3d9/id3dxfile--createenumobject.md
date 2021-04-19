---
description: Erstellt ein Enumeratorobjekt, das eine x-Datei liest.
ms.assetid: 86d05eab-601c-4beb-9dbe-c23fa524871c
title: 'ID3DXFile:: kreateendumuject-Methode (D3DX9Xof. h)'
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
ms.openlocfilehash: a58a3341bacf9b323cc5753f8e9e51c4b703b966
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367383"
---
# <a name="id3dxfilecreateenumobject-method"></a>ID3DXFile:: kreateendumuject-Methode

Erstellt ein Enumeratorobjekt, das eine x-Datei liest.

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

*pvsource* \[ vorgenommen\]
</dt> <dd>

Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)**

Die Datenquelle. Entweder:

-   Ein Dateiname
-   Eine [**D3DXF \_ fileloadmemory**](d3dxf-fileloadmemory.md) -Struktur
-   Eine [**D3DXF \_ fileloadresource**](d3dxf-fileloadresource.md) -Struktur

Abhängig vom Wert von loadflags.

</dd> <dt>

*loadflags* \[ in\]
</dt> <dd>

Typ: **[D3DXF \_ fileloadoption](d3dxf.md)**

Der-Wert, der die Quelle der Daten angibt. Bei diesem Wert kann es sich um eines der [D3DXF \_ fileloadoptions](d3dxf.md) -Flags handeln.

</dd> <dt>

*ppumubj* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **ID3DXFileEnumObject**](id3dxfileenumobject.md)\*\***

Adresse eines Zeigers auf eine [**ID3DXFileEnumObject**](id3dxfileenumobject.md) -Schnittstelle, die das erstellte Enumeratorobjekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DXFERR \_ badvalue, D3DXFERR Parameter \_ Error.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie nach der Verwendung dieser Methode eine der [**ID3DXFileEnumObject**](id3dxfileenumobject.md) -Methoden, um ein Datenobjekt abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXFile](id3dxfile.md)
</dt> <dt>

[**ID3DXFileEnumObject**](id3dxfileenumobject.md)
</dt> </dl>

 

 

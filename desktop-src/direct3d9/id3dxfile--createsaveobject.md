---
description: Erstellt ein Speicherobjekt, das zum Speichern von Daten in einer X-Datei verwendet wird.
ms.assetid: da064e83-605f-4c86-985d-9a0961c18e01
title: ID3DXFile::CreateSaveObject-Methode (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile.CreateSaveObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: aaf9f884a651182429de20fe261a250c8c6567eacd99d635213682e4d755b79a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951610"
---
# <a name="id3dxfilecreatesaveobject-method"></a>ID3DXFile::CreateSaveObject-Methode

Erstellt ein Speicherobjekt, das zum Speichern von Daten in einer X-Datei verwendet wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateSaveObject(
  [in]  LPCVOID               pData,
  [in]  D3DXF_FILESAVEOPTIONS flags,
  [in]  D3DXF_FILEFORMAT      dwFileFormat,
  [out] ID3DXFileSaveObject   **ppSaveObj
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pData* \[ In\]
</dt> <dd>

Typ: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Zeiger auf den Namen der Datei, die zum Speichern von Daten verwendet werden soll.

</dd> <dt>

*Flags* \[ In\]
</dt> <dd>

Typ: **[D3DXF \_ FILESAVEOPTIONS](d3dxf.md)**

Wert, der den Namen der Datei angibt, in der Daten gespeichert werden sollen. Dieser Wert kann eines der Flags [dateispeicheroptionen](d3dxf.md) sein.

</dd> <dt>

*dwFileFormat* \[ In\]
</dt> <dd>

Typ: **[D3DXF \_ FILEFORMAT](d3dxf.md)**

Gibt das Format an, das beim Speichern der X-Datei verwendet werden soll. Dieser Wert kann eines der [Dateiformatflags](d3dxf.md) sein. Weitere Informationen finden Sie in den Hinweisen.

</dd> <dt>

*ppSaveObj* \[ out\]
</dt> <dd>

Typ: **[ **ID3DXFileSaveObject**](id3dxfilesaveobject.md)\*\***

Adresse eines Zeigers auf eine [**ID3DXFileSaveObject-Schnittstelle,**](id3dxfilesaveobject.md) die das erstellte Speicherobjekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Sein: D3DXFERR \_ BADVALUE, D3DXFERR \_ PARSEERROR.

## <a name="remarks"></a>Hinweise

Verwenden Sie nach der Verwendung dieser Methode Methoden der [**ID3DXFileSaveObject-Schnittstelle,**](id3dxfilesaveobject.md) um Datenobjekte zu erstellen und Vorlagen oder Daten zu speichern.

Für das gespeicherte Dateiformat *dwFileFormat* muss eines der Binär-, Legacybinär- oder Textflags in [Dateiformaten](d3dxf.md) angegeben werden. Die Datei kann mithilfe des optionalen D3DXF \_ FILEFORMAT \_ COMPRESSED-Flags komprimiert werden.

Die Dateiformatwerte können in einem logischen OR kombiniert werden, um komprimierten Text oder komprimierte Binärdateien zu erstellen. Wenn Sie angeben, dass das Dateiformat Text und komprimiert sein soll, wird die Datei zuerst als Text geschrieben und dann komprimiert. Komprimierte Textdateien sind jedoch nicht so effizient wie binäre Textdateien. In den meisten Fällen sollten Sie daher binär und komprimiert angeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXFile](id3dxfile.md)
</dt> <dt>

[**ID3DXFileSaveObject**](id3dxfilesaveobject.md)
</dt> </dl>

 

 

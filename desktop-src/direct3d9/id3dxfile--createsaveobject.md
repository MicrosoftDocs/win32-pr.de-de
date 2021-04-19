---
description: Erstellt ein Speicher Objekt, das zum Speichern von Daten in einer x-Datei verwendet wird.
ms.assetid: da064e83-605f-4c86-985d-9a0961c18e01
title: 'ID3DXFile:: kreatesaveobject-Methode (D3DX9Xof. h)'
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
ms.openlocfilehash: d7c5b3de020ad50abfd8834aabbdc8e6e848d71d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353379"
---
# <a name="id3dxfilecreatesaveobject-method"></a>ID3DXFile:: kreatesaveobject-Methode

Erstellt ein Speicher Objekt, das zum Speichern von Daten in einer x-Datei verwendet wird.

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

*pData* \[ in\]
</dt> <dd>

Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)**

Zeiger auf den Namen der Datei, die zum Speichern von Daten verwendet werden soll.

</dd> <dt>

*Flags* \[ in\]
</dt> <dd>

Type: **[D3DXF \_ filesaveoptions](d3dxf.md)**

-Wert, der den Namen der Datei angibt, in der Daten gespeichert werden sollen. Bei diesem Wert kann es sich um eines der Optionen für die [Dateispeicher Optionen](d3dxf.md) handeln.

</dd> <dt>

*dwfileformat* \[ in\]
</dt> <dd>

Type: **[D3DXF \_ File Format](d3dxf.md)**

Gibt das Format an, das beim Speichern der x-Datei verwendet werden soll. Bei diesem Wert kann es sich um eines der [dateiformatflags](d3dxf.md) handeln. Weitere Informationen finden Sie in den Hinweisen.

</dd> <dt>

*ppsaveobj* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **ID3DXFileSaveObject**](id3dxfilesaveobject.md)\*\***

Adresse eines Zeigers auf eine [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) -Schnittstelle, die das erstellte Save-Objekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DXFERR \_ badvalue, D3DXFERR Parameter \_ Error.

## <a name="remarks"></a>Bemerkungen

Nachdem Sie diese Methode verwendet haben, verwenden Sie Methoden der [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) -Schnittstelle zum Erstellen von Datenobjekten und zum Speichern von Vorlagen oder Daten.

Im gespeicherten Dateiformat *dwfileformat* muss eines der Binär-, Legacy-oder textflags in [Dateiformaten](d3dxf.md) angegeben werden. Die Datei kann mit dem optionalen D3DXF \_ File Format-Flag komprimiert werden \_ .

Die Dateiformat Werte können mit einem logischen OR kombiniert werden, um komprimierten Text oder komprimierte Binärdateien zu erstellen. Wenn Sie angeben, dass das Dateiformat Text und Komprimierung sein soll, wird die Datei zuerst als Text geschrieben und dann komprimiert. Komprimierte Textdateien sind jedoch nicht so effizient wie binäre Textdateien. in den meisten Fällen ist es daher ratsam, Binär und komprimierte anzugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXFile](id3dxfile.md)
</dt> <dt>

[**ID3DXFileSaveObject**](id3dxfilesaveobject.md)
</dt> </dl>

 

 

---
description: Erstellt ein Speicherobjekt. Veraltet.
ms.assetid: 50a7dbde-1dd4-4aae-a9ab-97d6f99618c0
title: IDirectXFile::CreateSaveObject-Methode (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFile.CreateSaveObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: c3646f54b1f232c6eec3e1b3d06441a8e6a7c090f784e3c4c016f7f1bcfc3b03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119491850"
---
# <a name="idirectxfilecreatesaveobject-method"></a>IDirectXFile::CreateSaveObject-Methode

Erstellt ein Speicherobjekt. Veraltet.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateSaveObject(
  [in]          LPCSTR                  szFileName,
  [in]          DXFILEFORMAT            dwFileFormat,
  [out, retval] LPDIRECTXFILESAVEOBJECT *ppSaveObj
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*szFileName* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Zeiger auf den Namen der Datei, die zum Speichern von Daten verwendet werden soll.

</dd> <dt>

*dwFileFormat* \[ In\]
</dt> <dd>

Typ: **[ **DXFILEFORMAT**](dxfile.md)**

Gibt das Format an, das beim Speichern der DirectX-Datei verwendet werden soll. Dieser Wert kann eines der DXFILEFORMAT \_ xxx-Flags in [DXFILE-Konstanten sein.](dxfile.md) Weitere Informationen finden Sie in den Hinweisen.

</dd> <dt>

*ppSaveObj* \[ out, retval\]
</dt> <dd>

Typ: **[ **LPDIRECTXFILESAVEOBJECT**](idirectxfilesaveobject.md)\***

Adresse eines Zeigers auf eine [**IDirectXFileSaveObject-Schnittstelle,**](idirectxfilesaveobject.md) die das erstellte Speicherobjekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert DXFILE \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: DXFILEERR \_ BADALLOC, DXFILEERR \_ BADFILE, DXFILEERR \_ BADVALUE.

## <a name="remarks"></a>Hinweise

Verwenden Sie nach der Verwendung dieser Methode Methoden der [**IDirectXFileSaveObject-Schnittstelle,**](idirectxfilesaveobject.md) um Datenobjekte zu erstellen und Vorlagen oder Daten zu speichern.

Der Standardwert für das Dateiformat ist DXFILEFORMAT \_ BINARY. Die Dateiformatwerte können in einem logischen OR kombiniert werden, um komprimierten Text oder komprimierte Binärdateien zu erstellen. Wenn eine Datei sowohl als binär (0) als auch als text (1) angegeben wird, wird sie als Textdatei gespeichert, da der Wert nicht vom Formatwert der Textdatei (0 + 1 = 1) zu unterscheiden ist. Wenn Sie angeben, dass das Dateiformat text- und komprimiert sein soll, wird die Datei zuerst als Text geschrieben und dann komprimiert. Komprimierte Textdateien sind jedoch nicht so effizient wie Binärtextdateien, daher sollten Sie in den meisten Fällen binäre und komprimierte Textdateien angeben. Das Festlegen einer Zu komprimierenden Datei ohne Angabe eines Formats führt zu einer binären, komprimierten Datei.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[IDirectXFile](idirectxfile.md)
</dt> <dt>

[**IDirectXFileSaveObject**](idirectxfilesaveobject.md)
</dt> </dl>

 

 

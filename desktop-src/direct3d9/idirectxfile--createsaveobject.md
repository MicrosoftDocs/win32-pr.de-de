---
description: Erstellt ein Save-Objekt. Veraltet.
ms.assetid: 50a7dbde-1dd4-4aae-a9ab-97d6f99618c0
title: 'Idirectxfile:: kreatesaveobject-Methode (dxfile. h)'
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
ms.openlocfilehash: 848010a1f701b39f5cc77a126272bc019ed01f4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365125"
---
# <a name="idirectxfilecreatesaveobject-method"></a>Idirectxfile:: erkreatesaveobject-Methode

Erstellt ein Save-Objekt. Veraltet.

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

*szFilename* \[ in\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Zeiger auf den Namen der Datei, die zum Speichern von Daten verwendet werden soll.

</dd> <dt>

*dwfileformat* \[ in\]
</dt> <dd>

Typ: **[ **dxfileformat**](dxfile.md)**

Gibt das Format an, das beim Speichern der DirectX-Datei verwendet werden soll. Bei diesem Wert kann es sich um eines der dxfileformat \_ xxx-Flags in [dxfile-Konstanten](dxfile.md)handeln. Weitere Informationen finden Sie in den Hinweisen.

</dd> <dt>

*ppsaveobj* \[ Out, retval\]
</dt> <dd>

Typ: **[ **lpdirectxfilesaveobject**](idirectxfilesaveobject.md)\***

Adresse eines Zeigers auf eine [**idirectxfilesaveobject**](idirectxfilesaveobject.md) -Schnittstelle, die das erstellte Save-Objekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist dxfile OK der Rückgabewert \_ . Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: dxfileerr \_ badzuzuweisung, dxfileerr \_ BadFile, dxfileerr \_ badvalue.

## <a name="remarks"></a>Bemerkungen

Nachdem Sie diese Methode verwendet haben, verwenden Sie die Methoden der [**idirectxfilesaveobject**](idirectxfilesaveobject.md) -Schnittstelle zum Erstellen von Datenobjekten und zum Speichern von Vorlagen oder Daten.

Der Standardwert für das Dateiformat lautet dxfileformat \_ Binary. Die Dateiformat Werte können mit einem logischen OR kombiniert werden, um komprimierten Text oder komprimierte Binärdateien zu erstellen. Wenn eine Datei sowohl als Binärdatei (0) als auch als Text (1) angegeben wird, wird Sie als Textdatei gespeichert, da der Wert nicht vom Textdatei-Format Wert (0 + 1 = 1) unterschieden werden kann. Wenn Sie angeben, dass das Dateiformat Text und Komprimierung sein soll, wird die Datei zunächst als Text geschrieben und dann komprimiert. Komprimierte Textdateien sind jedoch nicht so effizient wie binäre Textdateien. in den meisten Fällen sollten Sie Binär-und komprimierte Textdateien angeben. Wenn eine Datei festgelegt wird, die ohne Angabe eines Formats komprimiert werden soll, führt dies zu einer binären komprimierten Datei.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Dxfile. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Idirectxfile](idirectxfile.md)
</dt> <dt>

[**Idirectxfilesaveobject**](idirectxfilesaveobject.md)
</dt> </dl>

 

 

---
description: Erstellt eine Instanz eines DirectXFile-Objekts. Veraltet.
ms.assetid: c920d480-2557-491d-87ea-7eea1f470498
title: DirectXFileCreate-Funktion (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DirectXFileCreate
api_type:
- DllExport
api_location:
- d3dxof.dll
ms.openlocfilehash: 6dbcf4836c33fd2acfc1adc21e47430a54ba7c54aeb2b220199846d31572619e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952180"
---
# <a name="directxfilecreate-function"></a>DirectXFileCreate-Funktion

Erstellt eine Instanz eines DirectXFile-Objekts. Veraltet.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDAPICALLTYPE DirectXFileCreate(
   LPDIRECTXFILE *lplpDirectXFile
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lplpDirectXFile* 
</dt> <dd>

Typ: **[ **LPDIRECTXFILE**](idirectxfile.md)\***

Adresse eines Zeigers auf eine [**IDirectXFile-Schnittstelle,**](idirectxfile.md) die das erstellte DirectXFile-Objekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Sein: DXFILEERR \_ BADALLOC, DXFILEERR \_ BADVALUE.

## <a name="remarks"></a>Hinweise

Nachdem Sie diese Funktion verwendet haben, verwenden [**Sie RegisterTemplates**](idirectxfile--registertemplates.md) zum Registrieren von Vorlagen, [**CreateEnumObject**](idirectxfile--createenumobject.md) zum Erstellen eines Enumeratorobjekts oder [**CreateSaveObject**](idirectxfile--createsaveobject.md) zum Erstellen eines Speicherobjekts.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3dxof.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[X-Dateifunktionen](dx9-graphics-reference-x-file-functions.md)
</dt> <dt>

[**CreateEnumObject**](idirectxfile--createenumobject.md)
</dt> <dt>

[**CreateSaveObject**](idirectxfile--createsaveobject.md)
</dt> <dt>

[**RegisterTemplates**](idirectxfile--registertemplates.md)
</dt> </dl>

 

 





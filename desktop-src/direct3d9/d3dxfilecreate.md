---
description: Erstellt eine Instanz eines ID3DXFile-Objekts.
ms.assetid: c086cb66-b1dc-4180-b966-e9a3b1f36f22
title: D3DXFileCreate-Funktion (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFileCreate
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: ccafd6e3cffb71cccbdf3025ead6ad2cc012f4d62ecf52405cf82dcda06a1531
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849790"
---
# <a name="d3dxfilecreate-function"></a>D3DXFileCreate-Funktion

Erstellt eine Instanz eines [**ID3DXFile-Objekts.**](id3dxfile.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT STDAPICALLTYPE D3DXFileCreate(
   ID3DXFile **lplpDirectXFile
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lplpDirectXFile* 
</dt> <dd>

Typ: **[ **ID3DXFile**](id3dxfile.md)\*\***

Adresse eines Zeigers auf eine [**ID3DXFile-Schnittstelle,**](id3dxfile.md) die das erstellte X-Dateiobjekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert S \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Sein: E \_ POINTER, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Verwenden Sie nach der Verwendung dieser Funktion [**RegisterTemplates**](id3dxfile--registertemplates.md) oder [**RegisterEnumTemplates,**](id3dxfile--registerenumtemplates.md) um Vorlagen zu registrieren, [**CreateEnumObject**](id3dxfile--createenumobject.md) zum Erstellen eines Enumeratorobjekts oder [**CreateSaveObject,**](id3dxfile--createsaveobject.md) um ein Speicherobjekt zu erstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX X-Dateifunktionen](dx9-graphics-reference-d3dx-x-file-functions.md)
</dt> <dt>

[**CreateEnumObject**](id3dxfile--createenumobject.md)
</dt> <dt>

[**CreateSaveObject**](id3dxfile--createsaveobject.md)
</dt> <dt>

[**RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md)
</dt> <dt>

[**RegisterTemplates**](id3dxfile--registertemplates.md)
</dt> </dl>

 

 





---
description: Anwendungen verwenden die Methoden der IDirectXFileEnumObject-Schnittstelle, um die Datenobjekte in der Datei zu durchlaufen und ein Datenobjekt anhand seines guid (Globally Unique Identifier) oder seines Namens abzurufen. Veraltet.
ms.assetid: 9eefda2a-5b17-4330-8245-63a38c1b1469
title: IDirectXFileEnumObject-Schnittstelle (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 448751cf7160dd9f5bd44f8f7460f30acc731ddf783c840654c3634e80f66540
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119491750"
---
# <a name="idirectxfileenumobject-interface"></a>IDirectXFileEnumObject-Schnittstelle

Anwendungen verwenden die Methoden der IDirectXFileEnumObject-Schnittstelle, um die Datenobjekte in der Datei zu durchlaufen und ein Datenobjekt anhand seines guid (Globally Unique Identifier) oder seines Namens abzurufen. Veraltet.

## <a name="members"></a>Member

Die **IDirectXFileEnumObject-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IDirectXFileEnumObject** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IDirectXFileEnumObject-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                     | Beschreibung                                                                     |
|:---------------------------------------------------------------------------|:--------------------------------------------------------------------------------|
| [**GetDataObjectById**](idirectxfileenumobject--getdataobjectbyid.md)     | Ruft das Datenobjekt ab, das über die angegebene GUID verfügt. Veraltet.<br/>   |
| [**GetDataObjectByName**](idirectxfileenumobject--getdataobjectbyname.md) | Ruft das Datenobjekt ab, das über den angegebenen Namen verfügt. Veraltet.<br/>   |
| [**GetNextDataObject**](idirectxfileenumobject--getnextdataobject.md)     | Ruft das nächste Objekt der obersten Ebene in der DirectX-Datei ab. Veraltet.<br/> |



 

## <a name="remarks"></a>Hinweise

Die GUID für die IDirectXFileEnumObject-Schnittstelle ist IID \_ IDirectXFileEnumObject.

Der LPDIRECTXFILEENUMOBJECT-Typ wird als Zeiger auf diese Schnittstelle definiert.


```
typedef interface IDirectXFileEnumObject *LPDIRECTXFILEENUMOBJECT;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[X-Dateischnittstellen](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 

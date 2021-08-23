---
description: Anwendungen verwenden die Methoden der ID3DXFileEnumObject-Schnittstelle, um die untergeordneten Dateidatenobjekte in der Datei zu durchlaufen und ein untergeordnetes Objekt anhand seines guid (Globally Unique Identifier) oder seines Namens abzurufen.
ms.assetid: 23b28f07-5832-4163-953b-615d20e781f6
title: ID3DXFileEnumObject-Schnittstelle (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4c274a42a5e07f05af3b0b2ffe18dc3fbaf546591f23e6f24906cd1723578303
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121359"
---
# <a name="id3dxfileenumobject-interface"></a>ID3DXFileEnumObject-Schnittstelle

Anwendungen verwenden die Methoden der ID3DXFileEnumObject-Schnittstelle, um die untergeordneten Dateidatenobjekte in der Datei zu durchlaufen und ein untergeordnetes Objekt anhand seines guid (Globally Unique Identifier) oder seines Namens abzurufen.

## <a name="members"></a>Member

Die **ID3DXFileEnumObject-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXFileEnumObject** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXFileEnumObject-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                  | Beschreibung                                                                |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------|
| [**Getchild**](id3dxfileenumobject--getchild.md)                       | Ruft ein untergeordnetes -Objekt in diesem Dateidatenobjekt ab.<br/>              |
| [**GetChildren**](id3dxfileenumobject--getchildren.md)                 | Ruft die Anzahl der untergeordneten Objekte in diesem Dateidatenobjekt ab.<br/> |
| [**GetDataObjectById**](id3dxfileenumobject--getdataobjectbyid.md)     | Ruft das Datenobjekt ab, das über die angegebene GUID verfügt.<br/>          |
| [**GetDataObjectByName**](id3dxfileenumobject--getdataobjectbyname.md) | Ruft das Datenobjekt ab, das über den angegebenen Namen verfügt.<br/>          |
| [**Getfile**](id3dxfileenumobject--getfile.md)                         | Ruft das [**ID3DXFile-Objekt**](id3dxfile.md) ab.<br/>            |



 

## <a name="remarks"></a>Hinweise

Die GUID für die ID3DXFileEnumObject-Schnittstelle ist IID \_ ID3DXFileEnumObject.

Der LPD3DXFILEENUMOBJECT-Typ wird als Zeiger auf diese Schnittstelle definiert.


```
typedef interface ID3DXFileEnumObject *LPD3DXFILEENUMOBJECT;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX X-Dateischnittstellen](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 

---
description: Anwendungen verwenden die Methoden der ID3DXFileSaveData-Schnittstelle, um Datenobjekte als children-Objekte eines .x-Dateidatenknotens hinzuzufügen.
ms.assetid: ab5bdd9a-496a-4ae1-b93a-fe5856bd97d4
title: ID3DXFileSaveData-Schnittstelle (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 68d52c1c022ed292a879ae4f701df52524d4170160bc79b6f1956c744a530c22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121302"
---
# <a name="id3dxfilesavedata-interface"></a>ID3DXFileSaveData-Schnittstelle

Anwendungen verwenden die Methoden der ID3DXFileSaveData-Schnittstelle, um Datenobjekte als children-Objekte eines .x-Dateidatenknotens hinzuzufügen.

## <a name="members"></a>Member

Die **ID3DXFileSaveData-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXFileSaveData** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXFileSaveData-Schnittstelle** verfügt über diese Methoden.



| Methode                                                          | Beschreibung                                                                                                                                |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddDataObject**](id3dxfilesavedata--adddataobject.md)       | Fügt ein Datenobjekt als untergeordnetes Element des **Dateidatenknotens ID3DXFileSaveData** hinzu.<br/>                                                      |
| [**AddDataReference**](id3dxfilesavedata--adddatareference.md) | Fügt einen Datenverweis als untergeordnetes Element dieses **ID3DXFileSaveData-Dateidatenknotens** hinzu. Der Datenverweis verweist auf ein Dateidatenobjekt.<br/> |
| [**Getid**](id3dxfilesavedata--getid.md)                       | Ruft die GUID dieses **ID3DXFileSaveData-Dateidatenknotens** ab.<br/>                                                                |
| [**GetName**](id3dxfilesavedata--getname.md)                   | Ruft den Namen dieses **ID3DXFileSaveData-Dateidatenknotens** ab.<br/>                                                                |
| [**GetSave**](id3dxfilesavedata--getsave.md)                   | Ruft einen Zeiger auf diesen [**ID3DXFileSaveObject-Dateidatenknoten**](id3dxfilesaveobject.md) ab.<br/>                                  |
| [**Gettype**](id3dxfilesavedata--gettype.md)                   | Ruft die Vorlagen-ID dieses Dateidatenknotens ab.<br/>                                                                               |



 

## <a name="remarks"></a>Hinweise

Die GUID für die ID3DXFileSaveObject-Schnittstelle ist IID \_ ID3DXFileSaveObject.

Der LPD3DXFileSaveData-Typ ist als Zeiger auf diese Schnittstelle definiert.


```
typedef interface ID3DXFileSaveData *LPD3DXFILESAVEDATA;
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

 

 

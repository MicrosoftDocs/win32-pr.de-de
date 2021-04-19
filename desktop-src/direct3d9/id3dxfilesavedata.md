---
description: Anwendungen verwenden die Methoden der ID3DXFileSaveData-Schnittstelle zum Hinzufügen von Datenobjekten als untergeordnete Elemente eines x-Datei Daten Knotens.
ms.assetid: ab5bdd9a-496a-4ae1-b93a-fe5856bd97d4
title: ID3DXFileSaveData-Schnittstelle (D3DX9Xof. h)
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
ms.openlocfilehash: d42f431dbb2f9108c5e503aea07ba6b11915f0ac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353719"
---
# <a name="id3dxfilesavedata-interface"></a>ID3DXFileSaveData-Schnittstelle

Anwendungen verwenden die Methoden der ID3DXFileSaveData-Schnittstelle zum Hinzufügen von Datenobjekten als untergeordnete Elemente eines x-Datei Daten Knotens.

## <a name="members"></a>Member

Die **ID3DXFileSaveData** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **ID3DXFileSaveData** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXFileSaveData** -Schnittstelle verfügt über diese Methoden.



| Methode                                                          | BESCHREIBUNG                                                                                                                                |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**Adddataobject**](id3dxfilesavedata--adddataobject.md)       | Fügt ein Datenobjekt als untergeordnetes Element des **ID3DXFileSaveData** -Datei Daten Knotens hinzu.<br/>                                                      |
| [**Adddatareferenzierung**](id3dxfilesavedata--adddatareference.md) | Fügt einen Daten Verweis als untergeordnetes Element dieses **ID3DXFileSaveData** File Data-Knotens hinzu. Der Daten Verweis verweist auf ein Datei Datenobjekt.<br/> |
| [**GetId**](id3dxfilesavedata--getid.md)                       | Ruft die GUID dieses **ID3DXFileSaveData** File Data-Knotens ab.<br/>                                                                |
| [**GetName**](id3dxfilesavedata--getname.md)                   | Ruft den Namen dieses **ID3DXFileSaveData** File Data-Knotens ab.<br/>                                                                |
| [**Getsave**](id3dxfilesavedata--getsave.md)                   | Ruft einen Zeiger auf diesen [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) File Data-Knoten ab.<br/>                                  |
| [**GetType**](id3dxfilesavedata--gettype.md)                   | Ruft die Vorlagen-ID dieses Datei Daten Knotens ab.<br/>                                                                               |



 

## <a name="remarks"></a>Bemerkungen

Die GUID für die ID3DXFileSaveObject-Schnittstelle ist IID \_ ID3DXFileSaveObject.

Der LPD3DXFileSaveData-Typ wird als Zeiger auf diese Schnittstelle definiert.


```
typedef interface ID3DXFileSaveData *LPD3DXFILESAVEDATA;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX X-Datei Schnittstellen](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 

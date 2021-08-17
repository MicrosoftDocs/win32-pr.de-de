---
description: Anwendungen verwenden die Methoden der ID3DXFileData-Schnittstelle, um die direkte Hierarchie des Datenobjekts zu erstellen oder darauf zuzugreifen. Vorlageneinschränkungen bestimmen die Hierarchie.
ms.assetid: ce291e2b-b926-4502-8bee-55fe6d6d3267
title: ID3DXFileData-Schnittstelle (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5e85e66d5089183b1797842ab4e152a10298ebcc74a10c66291c6f6bc62743e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121426"
---
# <a name="id3dxfiledata-interface"></a>ID3DXFileData-Schnittstelle

Anwendungen verwenden die Methoden der ID3DXFileData-Schnittstelle, um die direkte Hierarchie des Datenobjekts zu erstellen oder darauf zuzugreifen. Vorlageneinschränkungen bestimmen die Hierarchie.

## <a name="members"></a>Member

Die **ID3DXFileData-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXFileData** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXFileData-Schnittstelle** verfügt über diese Methoden.



| Methode                                            | Beschreibung                                                                                                          |
|:--------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**Getchild**](id3dxfiledata--getchild.md)       | Ruft ein untergeordnetes -Objekt in diesem Dateidatenobjekt ab.<br/>                                                        |
| [**GetChildren**](id3dxfiledata--getchildren.md) | Ruft die Anzahl der untergeordneten Elemente in diesem Dateidatenobjekt ab.<br/>                                                |
| [**GetEnum**](id3dxfiledata--getenum.md)         | Ruft das Enumerationsobjekt in diesem Dateidatenobjekt ab.<br/>                                                |
| [**Getid**](id3dxfiledata--getid.md)             | Ruft die GUID dieses Dateidatenobjekts ab.<br/>                                                              |
| [**GetName**](id3dxfiledata--getname.md)         | Ruft den Namen dieses Dateidatenobjekts ab.<br/>                                                              |
| [**Gettype**](id3dxfiledata--gettype.md)         | Ruft die Vorlagen-ID in diesem Dateidatenobjekt ab.<br/>                                                       |
| [**Isreference**](id3dxfiledata--isreference.md) | Gibt an, ob dieses Dateidatenobjekt ein Verweisobjekt ist, das auf ein anderes untergeordnetes Datenobjekt verweist.<br/>   |
| [**Sperre**](id3dxfiledata--lock.md)               | Greift auf die X-Dateidaten zu.<br/>                                                                                |
| [**Entsperren**](id3dxfiledata--unlock.md)           | Beendet die Lebensdauer  des ppData-Zeigers, der von [**ID3DXFileData::Lock**](id3dxfiledata--lock.md)zurückgegeben wird.<br/> |



 

## <a name="remarks"></a>Hinweise

Datentypen, die von der Vorlage zugelassen werden, werden als optionale Member bezeichnet. Die optionalen Member sind nicht erforderlich, aber ein Objekt kann wichtige Informationen ohne sie übersehen. Diese optionalen Member werden als untergeordnete Elemente des Datenobjekts gespeichert. Ein untergeordnetes Element kann ein anderes Datenobjekt oder ein Verweis auf ein früheres Datenobjekt sein.

Die GUID für die ID3DXFileData-Schnittstelle ist IID \_ ID3DXFileData.

Der LPD3DXFILEDATA-Typ wird als Zeiger auf diese Schnittstelle definiert.


```
typedef interface ID3DXFileData *LPD3DXFILEDATA;
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

 

 

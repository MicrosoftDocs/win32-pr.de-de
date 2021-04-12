---
description: Anwendungen verwenden die Methoden der ID3DXFileData-Schnittstelle, um die unmittelbare Hierarchie des Datenobjekts zu erstellen oder darauf zuzugreifen. Durch Vorlagen Einschränkungen wird die Hierarchie bestimmt.
ms.assetid: ce291e2b-b926-4502-8bee-55fe6d6d3267
title: ID3DXFileData-Schnittstelle (D3DX9Xof. h)
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
ms.openlocfilehash: 1764787864c059e9c7417525a1a5ab5ff862f7d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219596"
---
# <a name="id3dxfiledata-interface"></a>ID3DXFileData-Schnittstelle

Anwendungen verwenden die Methoden der ID3DXFileData-Schnittstelle, um die unmittelbare Hierarchie des Datenobjekts zu erstellen oder darauf zuzugreifen. Durch Vorlagen Einschränkungen wird die Hierarchie bestimmt.

## <a name="members"></a>Member

Die **ID3DXFileData** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **ID3DXFileData** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXFileData** -Schnittstelle verfügt über diese Methoden.



| Methode                                            | BESCHREIBUNG                                                                                                          |
|:--------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**GetChild**](id3dxfiledata--getchild.md)       | Ruft ein untergeordnetes-Objekt in diesem Datei Datenobjekt ab.<br/>                                                        |
| [**GetChildren**](id3dxfiledata--getchildren.md) | Ruft die Anzahl der untergeordneten Elemente in diesem Datei Datenobjekt ab.<br/>                                                |
| [**Getenum**](id3dxfiledata--getenum.md)         | Ruft das Enumerationsobjekt in diesem Datei Datenobjekt ab.<br/>                                                |
| [**GetId**](id3dxfiledata--getid.md)             | Ruft die GUID dieses Datei Datenobjekts ab.<br/>                                                              |
| [**GetName**](id3dxfiledata--getname.md)         | Ruft den Namen dieses Datei Datenobjekts ab.<br/>                                                              |
| [**GetType**](id3dxfiledata--gettype.md)         | Ruft die Vorlagen-ID in diesem Datei Datenobjekt ab.<br/>                                                       |
| [**IsReference**](id3dxfiledata--isreference.md) | Gibt an, ob dieses Datei Datenobjekt ein Verweis Objekt ist, das auf ein anderes untergeordnetes Datenobjekt zeigt.<br/>   |
| [**Sperre**](id3dxfiledata--lock.md)               | Greift auf die x-Datei Daten zu.<br/>                                                                                |
| [**Entsperren**](id3dxfiledata--unlock.md)           | Beendet die Lebensdauer des *ppData* -Zeigers, der von [**ID3DXFileData:: Lock**](id3dxfiledata--lock.md)zurückgegeben wurde.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die von der Vorlage zugelassenen Datentypen werden als optionale Member bezeichnet. Die optionalen Member sind nicht erforderlich, aber in einem Objekt werden möglicherweise wichtige Informationen übersehen. Diese optionalen Member werden als untergeordnete Elemente des Datenobjekts gespeichert. Ein untergeordnetes Element kann ein anderes Datenobjekt oder ein Verweis auf ein früheres Datenobjekt sein.

Die GUID für die ID3DXFileData-Schnittstelle ist IID \_ ID3DXFileData.

Der LPD3DXFILEDATA-Typ wird als Zeiger auf diese Schnittstelle definiert.


```
typedef interface ID3DXFileData *LPD3DXFILEDATA;
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

 

 

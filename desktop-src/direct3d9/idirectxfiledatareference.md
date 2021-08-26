---
description: Anwendungen verwenden die Methoden der IDirectXFileDataReference-Schnittstelle, um Datenverweisobjekte zu unterstützen.
ms.assetid: e0f6046f-36d9-4a13-9a0c-0738ebb2e569
title: IDirectXFileDataReference-Schnittstelle (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileDataReference
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 4507bed7a5f3f461c80b8eed1e5c07c15cfd34b7aab7a02c3e803a43a88ae132
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095630"
---
# <a name="idirectxfiledatareference-interface"></a>IDirectXFileDataReference-Schnittstelle

Anwendungen verwenden die Methoden der IDirectXFileDataReference-Schnittstelle, um Datenverweisobjekte zu unterstützen. Ein Datenverweisobjekt verweist auf ein Datenobjekt, das zuvor in der Datei definiert wurde. Dadurch können Sie dasselbe Objekt mehrmals verwenden, ohne es in der Datei zu wiederholen. Veraltet.

## <a name="members"></a>Member

Die **IDirectXFileDataReference-Schnittstelle** erbt von [**IDirectXFileObject.**](idirectxfileobject.md) **IDirectXFileDataReference** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IDirectXFileDataReference-Schnittstelle** verfügt über diese Methoden.



| Methode                                                | BESCHREIBUNG                                      |
|:------------------------------------------------------|:-------------------------------------------------|
| [**Beheben**](idirectxfiledatareference--resolve.md) | Löst Datenverweise auf. Veraltet.<br/> |



 

## <a name="remarks"></a>Hinweise

Nachdem Sie ermittelt haben, dass ein Objekt ein Datenverweisobjekt ist, verwenden Sie die [**IDirectXFileDataReference::Resolve-Methode,**](idirectxfiledatareference--resolve.md) um das zuvor in der Datei definierte Objekt abzurufen, auf das verwiesen wird. Informationen zum Identifizieren eines Datenverweisobjekts finden Sie in der [**IDirectXFileData-Schnittstelle.**](idirectxfiledata.md)

Die GUID für die IDirectXFileDataReference-Schnittstelle ist IID \_ IDirectXFileDataReference.

Der LPDIRECTXFILEDataReference-Typ wird als Zeiger auf diese Schnittstelle definiert.


```
typedef interface IDirectXFileDataReference *LPDIRECTXFILEDATAREFERENCE;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDirectXFileObject**](idirectxfileobject.md)
</dt> <dt>

[X-Dateischnittstellen](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 





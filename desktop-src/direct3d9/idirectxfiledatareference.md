---
description: Anwendungen verwenden die Methoden der idirectxfiledatareferenzierungsschnittstelle, um Daten Verweis Objekte zu unterstützen.
ms.assetid: e0f6046f-36d9-4a13-9a0c-0738ebb2e569
title: Idirectxfiledatareferenzierungsschnittstelle (dxfile. h)
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
ms.openlocfilehash: d04d2367f914c2e8d64a3c9c64fb55df1e51e47c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132425"
---
# <a name="idirectxfiledatareference-interface"></a>Idirectxfiledatareferenzierungsschnittstelle

Anwendungen verwenden die Methoden der idirectxfiledatareferenzierungsschnittstelle, um Daten Verweis Objekte zu unterstützen. Ein Daten Verweis Objekt verweist auf ein Datenobjekt, das zuvor in der Datei definiert wurde. Dies ermöglicht es Ihnen, das gleiche Objekt mehrmals zu verwenden, ohne es in der Datei wiederholen zu müssen. Veraltet.

## <a name="members"></a>Member

Die **idirectxfiledatareferenzierungsschnittstelle** erbt von [**idirectxfileobject**](idirectxfileobject.md). **Idirectxfiledatareferenziert** auch diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **idirectxfiledatareferenzierungsschnittstelle** verfügt über diese Methoden.



| Methode                                                | BESCHREIBUNG                                      |
|:------------------------------------------------------|:-------------------------------------------------|
| [**Beheben**](idirectxfiledatareference--resolve.md) | Löst Daten Verweise auf. Veraltet.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Nachdem Sie festgestellt haben, dass ein Objekt ein Daten Verweis Objekt ist, verwenden Sie die [**idirectxfiledatareferen:: Resolve**](idirectxfiledatareference--resolve.md) -Methode, um das Objekt abzurufen, auf das verwiesen wird, das zuvor in der Datei definiert wurde. Weitere Informationen zum Identifizieren eines Daten Verweis Objekts finden Sie unter [**idirectxfiledata**](idirectxfiledata.md) -Schnittstelle.

Die GUID für die idirectxfiledatareferenzierungsschnittstelle ist IID \_ idirectxfiledatareferenziert.

Der lpdirectxfiledatareferenzierungstyp ist als Zeiger auf diese Schnittstelle definiert.


```
typedef interface IDirectXFileDataReference *LPDIRECTXFILEDATAREFERENCE;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Dxfile. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Idirectxfileobject**](idirectxfileobject.md)
</dt> <dt>

[X-Datei Schnittstellen](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 





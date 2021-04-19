---
description: Anwendungen verwenden die Methoden der idirectxfiledata-Schnittstelle, um die unmittelbare Hierarchie des Datenobjekts zu erstellen oder darauf zuzugreifen.
ms.assetid: 8810162f-76a8-45ba-b069-7910fd611a60
title: Idirectxfiledata-Schnittstelle (dxfile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 30d2fb26e3752e302726edce51354369f3b067eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361233"
---
# <a name="idirectxfiledata-interface"></a>Idirectxfiledata-Schnittstelle

Anwendungen verwenden die Methoden der idirectxfiledata-Schnittstelle, um die unmittelbare Hierarchie des Datenobjekts zu erstellen oder darauf zuzugreifen. Durch Vorlagen Einschränkungen wird die Hierarchie bestimmt. Die von der Vorlage zugelassenen Datentypen werden als optionale Member bezeichnet. Die optionalen Member sind nicht erforderlich, aber in einem Objekt werden möglicherweise wichtige Informationen übersehen. Diese optionalen Member werden als untergeordnete Elemente des Datenobjekts gespeichert. Die untergeordneten Elemente können ein anderes Datenobjekt, ein Verweis auf ein früheres Datenobjekt oder ein binäres Objekt sein. Veraltet.

## <a name="members"></a>Member

Die **idirectxfiledata** -Schnittstelle erbt von [**idirectxfileobject**](idirectxfileobject.md). **Idirectxfiledata** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **idirectxfiledata** -Schnittstelle verfügt über diese Methoden.



| Methode                                                         | BESCHREIBUNG                                                                                                               |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------|
| [**Addbinaryobject**](idirectxfiledata--addbinaryobject.md)   | Erstellt ein binäres Objekt und fügt es als untergeordnetes Objekt hinzu. Veraltet.<br/>                                             |
| [**Adddataobject**](idirectxfiledata--adddataobject.md)       | Fügt ein Datenobjekt als untergeordnetes Objekt hinzu. Veraltet.<br/>                                                              |
| [**Adddatareferenzierung**](idirectxfiledata--adddatareference.md) | Erstellt ein Daten Verweis Objekt als untergeordnetes Objekt und fügt es hinzu. Veraltet.<br/>                                        |
| [**GetData**](idirectxfiledata--getdata.md)                   | Ruft die Daten für eines der Member des Objekts oder die Daten für alle Elemente ab. Veraltet.<br/>                    |
| [**Getnextobject**](idirectxfiledata--getnextobject.md)       | Ruft das nächste untergeordnete Datenobjekt, das Daten Verweis Objekt oder das binäre Objekt in der DirectX-Datei ab. Veraltet.<br/> |
| [**GetType**](idirectxfiledata--gettype.md)                   | Ruft die GUID der Objekt Vorlage ab. Veraltet.<br/>                                                       |



 

## <a name="remarks"></a>Bemerkungen

Die GUID für die idirectxfiledata-Schnittstelle ist IID \_ idirectxfiledata.

Der lpdirectxfiledata-Typ wird als Zeiger auf diese Schnittstelle definiert.


```
typedef interface IDirectXFileData *LPDIRECTXFILEDATA;
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

 

 





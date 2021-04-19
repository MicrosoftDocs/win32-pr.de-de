---
title: IWMPMedia3 getItemInfoByType-Methode
description: Die getItemInfoByType-Methode gibt den Wert des Attributs zurück, das dem angegebenen Attributtyp und Index entspricht.
ms.assetid: e4cf14b4-3c59-485f-a573-734a0076647b
keywords:
- getItemInfoByType-Methode, Windows Media Player
- getItemInfoByType-Methode, Windows Media Player, IWMPMedia3-Schnittstelle
- IWMPMedia3 Interface, Windows Media Player, getItemInfoByType-Methode
topic_type:
- apiref
api_name:
- IWMPMedia3.getItemInfoByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2f37992201d5d19397724071f8c2a4b8e851aac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352819"
---
# <a name="iwmpmedia3getiteminfobytype-method"></a>IWMPMedia3:: getItemInfoByType-Methode

Die **getItemInfoByType** -Methode gibt den Wert des Attributs zurück, das dem angegebenen Attributtyp und Index entspricht.

## <a name="syntax"></a>Syntax


```CSharp
public System.Object getItemInfoByType(
  System.String bstrType,
  System.String bstrLanguage,
  System.Int32 lIndex
);
```


```VB

Public Function getItemInfoByType( _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String, _
  ByVal lIndex As System.Int32 _
) As System.Object
Implements IWMPMedia3.getItemInfoByType
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrintype* \[ in\]
</dt> <dd>

Ein **System. String** -Wert, der der Attributtyp ist.

</dd> <dt>

*bstraulanguage* \[ in\]
</dt> <dd>

Ein **System. String** -Wert, der die Sprache ist. Wenn der Wert auf NULL oder eine Zeichenfolge der Länge 0 (null) ("") festgelegt ist, wird die aktuelle Gebiets Schema Zeichenfolge verwendet. Andernfalls muss der Wert eine gültige RFC 1766-sprach Zeichenfolge sein, z. b. "en-US".

</dd> <dt>

*Lindex* \[ in\]
</dt> <dd>

Ein **System. Int32** -Wert, der der Attribut Index ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein **System. Object** , das den Wert des Attributs ist. Der Typ, in den dieses Objekt umgewandelt werden soll, hängt vom Typ des Attributs ab.

## <a name="remarks"></a>Bemerkungen

Diese Methode gibt die Metadaten für ein einzelnes digitales Medien Element oder ein Medien Element zurück, das Teil einer Wiedergabeliste ist.

Diese Methode unterstützt Attribute mit mehreren Werten und Attributen mit komplexen Werten. Die **getiteminfo** -Methode unterstützt keine Attribute mit mehreren Werten und Attributen mit komplexen Werten.

Die **AttributeCount** -Eigenschaft ruft die Anzahl der für ein bestimmtes Medien Element verfügbaren Attributnamen ab. Index Nummern können dann mit der **GetAttributeName** -Methode verwendet werden, um den Namen der einzelnen verfügbaren Attribute zu bestimmen. Einzelne Attributnamen können an den *Name* -Parameter von **getItemInfoByType** übergeben werden.

Die **getattributezähltbytype** -Methode gibt die Anzahl von Attributen zurück, die einem bestimmten Attributnamen für ein bestimmtes Medien Element entsprechen. Indexnummern können dann an den *Index* -Parameter von **getItemInfoByType** übergeben werden. Dies ist hilfreich, wenn ein Medien Element z. b. unter mehreren Genres kategorisiert wurde.

Wenn das Medien Element aus einer Bibliothek stammt, die durch den Aufruf von [iwmplibrary. mediacollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md)abgerufen wurde, unterscheidet sich der Satz verfügbarer Attribute von denjenigen, die von der lokalen Bibliothek abgerufen werden können, die durch Aufrufen von [AxWindowsMediaPlayer. mediacollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)abgerufen wurde. Beispielsweise sind die Attribute, die in der lokalen Bibliothek verfügbar sind, die mithilfe von **iwmplibrary** abgerufen werden, eine Teilmenge der Attribute, die in der lokalen Bibliothek verfügbar sind, die mithilfe von **AxWindowsMediaPlayer** abgerufen wurde. Der Satz von Attributen, der aus anderen Quellen (Remote Bibliotheken, portable Geräte oder CDs) verfügbar ist, wird von den anderen Quellen definiert.

Vor dem Aufrufen dieser Methode müssen Sie über Lesezugriff auf die Bibliothek verfügen. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPMedia3-Schnittstelle (VB und c#)**](iwmpmedia3--vb-and-c.md)
</dt> <dt>

[**Iwmpmedia. AttributeCount (VB und c#)**](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[**Iwmpmedia. GetAttributeName (VB und c#)**](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)
</dt> <dt>

[**Iwmpmedia. getiteminfo (VB und c#)**](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPMedia3. getattributezähltbytype (VB und c#)**](wmplibiwmpmedia3-iwmpmedia3-getattributecountbytype--vb-and-c.md)
</dt> </dl>

 

 






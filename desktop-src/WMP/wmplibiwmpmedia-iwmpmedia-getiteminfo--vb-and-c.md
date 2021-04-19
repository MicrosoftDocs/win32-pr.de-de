---
title: Iwmpmedia getiteminfo-Methode
description: Die getiteminfo-Methode gibt den Wert des angegebenen Attributs für das Medien Element zurück.
ms.assetid: b95fa61d-a600-4f31-a930-d80516204034
keywords:
- getiteminfo-Methode, Windows Media Player
- getiteminfo-Methode, Windows Media Player, iwmpmedia-Schnittstelle
- Iwmpmedia Interface, Windows Media Player, getiteminfo-Methode
topic_type:
- apiref
api_name:
- IWMPMedia.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 523e57e68d13df55395cd4deca6e09904723bbaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356068"
---
# <a name="iwmpmediagetiteminfo-method"></a>Iwmpmedia:: getiteminfo-Methode

Die **getiteminfo** -Methode gibt den Wert des angegebenen Attributs für das Medien Element zurück.

## <a name="syntax"></a>Syntax


```CSharp
public System.String getItemInfo(
  System.String bstrItemName
);
```


```VB

Public Function getItemInfo( _
  ByVal bstrItemName As System.String _
) As System.String
Implements IWMPMedia.getItemInfo
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*bstritemname* \[ in\]
</dt> <dd>

Ein **System. String** -Wert, der den Namen des Attributs ist. Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Attribut Referenz](attribute-reference.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein **System. String** -Wert, der den Wert des angegebenen Attributs ist.

## <a name="remarks"></a>Bemerkungen

Diese Methode gibt die Metadaten für ein einzelnes Medien Element oder ein Medien Element zurück, das Teil einer Wiedergabeliste ist.

Die **AttributeCount** -Eigenschaft ruft die Anzahl der für ein bestimmtes Medien Element verfügbaren Attributnamen ab. Index Nummern können dann mit der **GetAttributeName** -Methode verwendet werden, um den Namen der einzelnen verfügbaren Attribute zu bestimmen. Einzelne Attributnamen können an **getiteminfo** übermittelt werden.

Um Attribute mit mehreren Werten und Attributen mit komplexen Werten abzurufen, verwenden Sie die **getItemInfoByType** -Methode.

Wenn das Medien Element aus einer Bibliothek stammt, die durch den Aufruf von [iwmplibrary. mediacollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md)abgerufen wurde, unterscheidet sich der Satz verfügbarer Attribute von denjenigen, die von der lokalen Bibliothek abgerufen werden können, die durch Aufrufen von [AxWindowsMediaPlayer. mediacollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)abgerufen wurde. Beispielsweise sind die Attribute, die in der lokalen Bibliothek verfügbar sind, die mithilfe von **iwmplibrary** abgerufen werden, eine Teilmenge der Attribute, die in der lokalen Bibliothek verfügbar sind, die mithilfe von **iwmpcore** abgerufen wurde. Der Satz von Attributen, der aus anderen Quellen (Remote Bibliotheken, portable Geräte oder CDs) verfügbar ist, wird von den anderen Quellen definiert.

Vor dem Aufrufen dieser Methode müssen Sie über Lesezugriff auf die Bibliothek verfügen. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attribut Verweis**](attribute-reference.md)
</dt> <dt>

[**Iwmpmedia-Schnittstelle (VB und c#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Iwmpmedia. AttributeCount (VB und c#)**](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[**Iwmpmedia. GetAttributeName (VB und c#)**](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)
</dt> <dt>

[**Iwmpmedia. Einstellungs Verzeichnis (VB und c#)**](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPMedia3. getItemInfoByType (VB und c#)**](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 






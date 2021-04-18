---
title: Iwmpmedia getiteminfobyatom-Methode
description: Die getiteminfobyatom-Methode gibt den Wert des Attributs mit der angegebenen Indexnummer zurück.
ms.assetid: d9a4b737-add1-4bbd-8e03-e58f45d65a62
keywords:
- getiteminfobyatom-Methode, Windows Media Player
- getiteminfobyatom-Methode, Windows Media Player, iwmpmedia-Schnittstelle
- Iwmpmedia Interface, Windows Media Player, getiteminfobyatom-Methode
topic_type:
- apiref
api_name:
- IWMPMedia.getItemInfoByAtom
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb37243960360120fbfe508a39db31e37728ac39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371519"
---
# <a name="iwmpmediagetiteminfobyatom-method"></a>Iwmpmedia:: getiteminfobyatom-Methode

Die **getiteminfobyatom** -Methode gibt den Wert des Attributs mit der angegebenen Indexnummer zurück.

## <a name="syntax"></a>Syntax


```CSharp
public System.String getItemInfoByAtom(
  System.Int32 lAtom
);
```


```VB

Public Function getItemInfoByAtom( _
  ByVal lAtom As System.Int32 _
) As System.String
Implements IWMPMedia.getItemInfoByAtom
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*latom* \[ in\]
</dt> <dd>

Ein **System. Int32** -Wert, der den Index angibt, an dem das angeforderte Attribut innerhalb des Satzes verfügbarer Attribute liegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein **System. String** -Wert, der dem Wert des-Attributs entspricht.

## <a name="remarks"></a>Bemerkungen

Diese Methode kann verwendet werden, um Metadaten für ein bestimmtes Medien Element mithilfe einer Attribut Indexnummer abzurufen. Die **AttributeCount** -Eigenschaft kann verwendet werden, um die Anzahl der für das Medien Element verfügbaren Attribute zu bestimmen.

Die **getmediaatom** -Methode der **iwmpmediacollection** -Schnittstelle kann auch verwendet werden, um den Index eines bestimmten Attributs abzurufen. Diese Technik ist im Allgemeinen effizienter als die **getiteminfo** -Methode oder die **getItemInfoByType** -Methode bei der Arbeit mit großen Wiedergabelisten.

Vor dem Aufrufen dieser Methode müssen Sie über Lesezugriff auf die Bibliothek verfügen. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpmedia-Schnittstelle (VB und c#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Iwmpmedia. AttributeCount (VB und c#)**](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[**Iwmpmedia. getiteminfo (VB und c#)**](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> <dt>

[**Iwmpmedia. Einstellungs Verzeichnis (VB und c#)**](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPMedia3. getItemInfoByType (VB und c#)**](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> <dt>

[**Iwmpmediacollection. getmediaatom (VB und c#)**](wmplibiwmpmediacollection-iwmpmediacollection-getmediaatom--vb-and-c.md)
</dt> </dl>

 

 






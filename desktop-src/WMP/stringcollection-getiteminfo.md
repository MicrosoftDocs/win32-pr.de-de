---
title: StringCollection. getiteminfo-Methode
description: Die getiteminfo-Methode ruft die Zeichenfolge ab, die dem angegebenen Index und Namen des StringCollection-Elements entspricht.
ms.assetid: a031b91e-9d3b-47ac-bc5b-c111d5e3bc12
keywords:
- getiteminfo-Methode, Windows Media Player
- getiteminfo-Methode, Windows Media Player, StringCollection-Klasse
- StringCollection-Klasse, Windows Media Player, getiteminfo-Methode
topic_type:
- apiref
api_name:
- StringCollection.getItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c9552dcebbc7d565ebc797c62ac3bc00ee109fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358122"
---
# <a name="stringcollectiongetiteminfo-method"></a>StringCollection. getiteminfo-Methode

Die **getiteminfo** -Methode ruft die Zeichenfolge ab, die dem angegebenen Index und Namen des **StringCollection** -Elements entspricht.

## <a name="syntax"></a>Syntax


```JScript
strRetVal = StringCollection.getItemInfo(
  index,
  name
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ in\]
</dt> <dd>

**Number** (**Long**) gibt den NULL basierten Index des **StringCollection** -Elements an, aus dem das Attribut bezogen werden soll.

</dd> <dt>

*Name* \[ in\]
</dt> <dd>

**Zeichenfolge** , die den Attributnamen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine **Zeichenfolge** zurück, die den Wert des angegebenen Attributs darstellt. Bei Attributen, deren zugrunde liegender Wert **boolescher** Wert ist, wird die Zeichenfolge "true" oder "false" zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Um Attribute mit mehreren Werten und Attributen mit komplexen Werten abzurufen, verwenden Sie die **getItemInfoByType** -Methode.

Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**StringCollection. getItemInfoByType**](stringcollection-getiteminfobytype.md)
</dt> <dt>

[**StringCollection-Objekt**](stringcollection-object.md)
</dt> </dl>

 

 






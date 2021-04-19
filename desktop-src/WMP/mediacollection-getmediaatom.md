---
title: Mediacollection. getmediaatom-Methode
description: Die getmediaatom-Methode ruft den Index ab, bei dem ein angegebenes Attribut innerhalb des Satzes verfügbarer Attribute liegt.
ms.assetid: 17501a95-1196-43ff-9a4e-a78cf28e7a2d
keywords:
- getmediaatom-Methode, Windows-Media Player
- getmediaatom-Methode, Windows Media Player, mediacollection-Klasse
- Mediacollection-Klasse, Windows Media Player, getmediaatom-Methode
topic_type:
- apiref
api_name:
- MediaCollection.getMediaAtom
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16728b20c26b90c10f144f278f7dec24195b536a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370066"
---
# <a name="mediacollectiongetmediaatom-method"></a>Mediacollection. getmediaatom-Methode

Die **getmediaatom** -Methode ruft den Index ab, bei dem ein angegebenes Attribut innerhalb des Satzes verfügbarer Attribute liegt.

## <a name="syntax"></a>Syntax


```JScript
retVal = MediaCollection.getMediaAtom(
  attribute
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Attribut* \[ in\]
</dt> <dd>

**Zeichenfolge** , die den Attributnamen enthält. Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Referenz](attribute-reference.md)zu Windows Media Player-Attributen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine **Zahl** (**Long**) zurück.

## <a name="remarks"></a>Bemerkungen

Die mit dieser Methode abgerufene Indexnummer kann an die *Medien* übermittelt werden. die **getiteminfobyatom** -Methode, um auf Attributwerte zuzugreifen. Diese Technik ist in der Regel effizienter, wenn Sie mit großen Wiedergabelisten arbeiten, als der Zugriff auf einen Attribut Wert nach Namen über das *Medium*. **getiteminfo** oder *Medium*. **getItemInfoByType**.

Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Media. getiteminfo**](media-getiteminfo.md)
</dt> <dt>

[**Media. getiteminfobyatom**](media-getiteminfobyatom.md)
</dt> <dt>

[**Media. getItemInfoByType**](media-getiteminfobytype.md)
</dt> <dt>

[**Mediacollection-Objekt**](mediacollection-object.md)
</dt> <dt>

[**Settings. mediaaccessrights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestmediaaccessrights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 






---
title: MediaCollection.getMediaAtom-Methode
description: Die getMediaAtom-Methode ruft den Index ab, an dem sich ein angegebenes Attribut innerhalb des Sets verfügbarer Attribute befindet.
ms.assetid: 17501a95-1196-43ff-9a4e-a78cf28e7a2d
keywords:
- getMediaAtom-Windows Media Player
- getMediaAtom-Methode Windows Media Player , MediaCollection-Klasse
- MediaCollection-Klasse Windows Media Player , getMediaAtom-Methode
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
ms.openlocfilehash: 8f537b759516d5fa0f382d0c72aabbc0edb836ad8e4ae6d7f210d012fa19ea60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118837203"
---
# <a name="mediacollectiongetmediaatom-method"></a>MediaCollection.getMediaAtom-Methode

Die **getMediaAtom-Methode** ruft den Index ab, an dem sich ein angegebenes Attribut innerhalb des Sets verfügbarer Attribute befindet.

## <a name="syntax"></a>Syntax


```JScript
retVal = MediaCollection.getMediaAtom(
  attribute
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Attribut* \[ In\]
</dt> <dd>

**Eine Zeichenfolge,** die den Attributnamen enthält. Informationen zu den attributes, die von Windows Media Player unterstützt werden, finden Sie in der Windows Media Player [Attribute Reference](attribute-reference.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine **Zahl** **(long) zurück.**

## <a name="remarks"></a>Hinweise

Die mit dieser Methode abgerufene Indexnummer kann an das Medium *übergeben werden.* **getItemInfoByAtom-Methode** für den Zugriff auf Attributwerte. Diese Technik ist im Allgemeinen effizienter bei der Arbeit mit großen Wiedergabelisten als der Zugriff auf einen Attributwert nach Namen über *Media*. **getItemInfo** oder *Media*. **getItemInfoByType**.

Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Media.getItemInfo**](media-getiteminfo.md)
</dt> <dt>

[**Media.getItemInfoByAtom**](media-getiteminfobyatom.md)
</dt> <dt>

[**Media.getItemInfoByType**](media-getiteminfobytype.md)
</dt> <dt>

[**MediaCollection-Objekt**](mediacollection-object.md)
</dt> <dt>

[**Einstellungen.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Einstellungen.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 






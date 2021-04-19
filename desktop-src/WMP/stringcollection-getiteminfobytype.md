---
title: StringCollection. getItemInfoByType-Methode
description: Die getItemInfoByType-Methode ruft den Wert ab, der dem angegebenen StringCollection-Index, dem angegebenen Namen, der angegebenen Sprache und dem angegebenen Attribut Index entspricht.
ms.assetid: 32a25c69-9399-4857-84c1-143c529be58f
keywords:
- getItemInfoByType-Methode, Windows Media Player
- getItemInfoByType-Methode, Windows Media Player, StringCollection-Klasse
- StringCollection-Klasse, Windows Media Player, getItemInfoByType-Methode
topic_type:
- apiref
api_name:
- StringCollection.getItemInfoByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4b3aa8c5bc367095765f24f19f107dd7cb986ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366955"
---
# <a name="stringcollectiongetiteminfobytype-method"></a>StringCollection. getItemInfoByType-Methode

Die **getItemInfoByType** -Methode ruft den Wert ab, der dem angegebenen **StringCollection** -Index, dem angegebenen Namen, der angegebenen Sprache und dem angegebenen Attribut Index entspricht.

## <a name="syntax"></a>Syntax


```JScript
retVal = StringCollection.getItemInfoByType(
  index,
  name,
  language,
  attributeIndex
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

</dd> <dt>

*Sprache* \[ in\]
</dt> <dd>

**Zeichenfolge** , die die Sprache enthält. Wenn der Wert auf NULL oder eine leere Zeichenfolge ("") festgelegt ist, wird die aktuelle Gebiets Schema Zeichenfolge verwendet. Andernfalls muss der Wert eine gültige RFC 1766-sprach Zeichenfolge sein, z. b. "en-US".

</dd> <dt>

*attributeIndex* \[ in\]
</dt> <dd>

**Number** (**Long**), der den NULL basierten Index des Werts enthält, der aus dem Attribut abgerufen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine **Zahl**, ein **Zeichen** folgen Objekt, ein **MetadataPicture** -Objekt oder ein **MetadataText** -Objekt zurück, wie in der folgenden Tabelle angegeben.



| Attribut                   | Rückgabewert                   |
|-----------------------------|--------------------------------|
| **SyncState**               | **Number** (**Ganzzahl ohne Vorzeichen long**) |
| **Synchronisierte WM/Liedtexte \_** | **MetadataText** -Objekt        |
| **WM/Bild**              | **MetadataPicture** -Objekt     |
| **WM/userweburl**           | **MetadataText** -Objekt        |
| Alle anderen Attribute        | String                         |



 

Bei Attributen, deren zugrunde liegender Wert **boolescher** Wert ist, gibt diese Methode die Zeichenfolge "true" oder "false" zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode unterstützt Attribute mit mehreren Werten und Attribute mit komplexen Werten. Die **getiteminfo** -Methode unterstützt keine Attribute mit mehreren oder komplexen Werten.

Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MetadataPicture-Objekt**](metadatapicture-object.md)
</dt> <dt>

[**MetadataText-Objekt**](metadatatext-object.md)
</dt> <dt>

[**StringCollection. getiteminfo**](stringcollection-getiteminfo.md)
</dt> <dt>

[**StringCollection-Objekt**](stringcollection-object.md)
</dt> </dl>

 

 






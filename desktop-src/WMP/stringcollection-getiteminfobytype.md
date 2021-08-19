---
title: StringCollection.getItemInfoByType-Methode
description: Die getItemInfoByType-Methode ruft den Wert ab, der dem angegebenen StringCollection-Index, -Namen, der angegebenen Sprache und dem angegebenen Attributindex entspricht.
ms.assetid: 32a25c69-9399-4857-84c1-143c529be58f
keywords:
- getItemInfoByType-Methode Windows Media Player
- getItemInfoByType-Methode Windows Media Player , StringCollection-Klasse
- StringCollection-Klasse Windows Media Player , getItemInfoByType-Methode
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
ms.openlocfilehash: 7b9d270ab746618f81f7c2e4135f7a6057f207d2cc89961ebe7c8f47d9fd1abd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123030"
---
# <a name="stringcollectiongetiteminfobytype-method"></a>StringCollection.getItemInfoByType-Methode

Die **getItemInfoByType-Methode** ruft den Wert ab, der dem angegebenen **StringCollection-Index,** -Namen, der angegebenen Sprache und dem angegebenen Attributindex entspricht.

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

*Index* \[ In\]
</dt> <dd>

**Number** (**long**), die den nullbasierten Index des **StringCollection-Elements** angibt, aus dem das Attribut abzurufen ist.

</dd> <dt>

*name* \[ In\]
</dt> <dd>

**Zeichenfolge,** die den Attributnamen enthält.

</dd> <dt>

*Language (Sprache)* \[ In\]
</dt> <dd>

**Zeichenfolge,** die die Sprache enthält. Wenn der Wert auf NULL oder die leere Zeichenfolge ("") festgelegt ist, wird die aktuelle Gebietsschemazeichenfolge verwendet. Andernfalls muss der Wert eine gültige RFC 1766-Sprachzeichenfolge wie "en-us" sein.

</dd> <dt>

*attributeIndex* \[ In\]
</dt> <dd>

**Number** (**long**), die den nullbasierten Index des Werts enthält, der aus dem Attribut abgerufen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt ein **Number-,** **String-, MetadataPicture-** oder **MetadataText-Objekt** zurück, wie in der folgenden Tabelle angegeben. 



| attribute                   | Rückgabewert                   |
|-----------------------------|--------------------------------|
| **SyncState**               | **Number** (**unsigned long**) |
| **WM/Synchronisierte Wm/Wm-Synchronisierung \_** | **MetadataText-Objekt**        |
| **WM/Bild**              | **MetadataPicture-Objekt**     |
| **WM/UserWebURL**           | **MetadataText-Objekt**        |
| Alle anderen Attribute        | String                         |



 

Für Attribute, deren zugrunde liegender Wert **boolesch** ist, gibt diese Methode die Zeichenfolge "true" oder "false" zurück.

## <a name="remarks"></a>Hinweise

Diese Methode unterstützt Attribute mit mehreren Werten und Attribute mit komplexen Werten. Die **getItemInfo-Methode** unterstützt keine Attribute mit mehreren oder komplexen Werten.

Um diese Methode zu verwenden, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

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

[**StringCollection.getItemInfo**](stringcollection-getiteminfo.md)
</dt> <dt>

[**StringCollection-Objekt**](stringcollection-object.md)
</dt> </dl>

 

 






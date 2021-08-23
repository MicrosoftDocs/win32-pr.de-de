---
title: Media.getItemInfoByType-Methode
description: Die getItemInfoByType-Methode ruft den Wert des Attributs ab, das dem angegebenen Attributnamen, der angegebenen Sprache und dem angegebenen Index entspricht.
ms.assetid: 9d3377c2-7ae8-48ce-a42e-9c965f6b79f9
keywords:
- getItemInfoByType-Windows Media Player
- getItemInfoByType-Methode Windows Media Player , Media-Klasse
- Medienklasse Windows Media Player , getItemInfoByType-Methode
topic_type:
- apiref
api_name:
- Media.getItemInfoByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa180834d70c8dd078beafc360400c931e7058994f1cc46d4e9abb011987d158
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135123"
---
# <a name="mediagetiteminfobytype-method"></a>Media.getItemInfoByType-Methode

Die **getItemInfoByType-Methode** ruft den Wert des Attributs ab, das dem angegebenen Attributnamen, der angegebenen Sprache und dem angegebenen Index entspricht.

## <a name="syntax"></a>Syntax


```JScript
retVal = Media.getItemInfoByType(
  name,
  language,
  index
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Name* \[ In\]
</dt> <dd>

**Eine Zeichenfolge,** die den Namen des Attributs enthält. Informationen zu den attributes, die von Windows Media Player unterstützt werden, finden Sie in der Windows Media Player [Attribute Reference](attribute-reference.md).

</dd> <dt>

*Sprache* \[ In\]
</dt> <dd>

**Eine Zeichenfolge,** die die Sprache darstellt. Wenn der Wert auf NULL oder "" (leere Zeichenfolge) festgelegt ist, wird die aktuelle Locale String verwendet. Andernfalls muss der Wert eine gültige RFC 1766-Sprachzeichenfolge wie "en-us" sein.

</dd> <dt>

*Index* \[ In\]
</dt> <dd>

**Number** (**long**), die den nullbasierten Index des Werts enthält, der aus dem Attribut abgerufen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt ein **Number-,** **String-,** **MetadataPicture-** oder **MetadataText-Objekt** zurück, wie in der folgenden Tabelle angegeben.



| attribute                   | Rückgabewert                   |
|-----------------------------|--------------------------------|
| **SyncState**               | **Number** (**unsigned long**) |
| **WM/Synchronisierung \_** | **MetadataText-Objekt**        |
| **WM/Picture**              | **MetadataPicture-Objekt**     |
| **WM/UserWebURL**           | **MetadataText-Objekt**        |
| Alle anderen Attribute        | **String**                     |



 

Für Attribute, deren zugrunde liegender Wert **boolean ist,** gibt diese Methode die Zeichenfolge "true" oder "false" zurück.

## <a name="remarks"></a>Hinweise

Diese Methode ruft die Metadaten für ein einzelnes digitales Medienelement oder ein Medienelement ab, das Teil einer Wiedergabeliste ist.

Diese Methode unterstützt Attribute mit mehreren Werten und Attribute mit komplexen Werten. Die **getItemInfo-Methode** unterstützt keine Attribute mit mehreren Werten und Attribute mit komplexen Werten.

Die **attributeCount-Eigenschaft** enthält die Anzahl der Attributnamen, die für ein bestimmtes **Media-Objekt verfügbar** sind. Indexnummern können dann mit der **getAttributeName-Methode** verwendet werden, um den Namen jedes verfügbaren Attributs zu bestimmen. Einzelne Attributnamen können an den *Name-Parameter* von **getItemInfoByType übergeben werden.**

Die **getAttributeCountByType-Methode** gibt die Anzahl von Attributen zurück, die einem bestimmten Attributnamen für ein bestimmtes **Media-Objekt** entsprechen. Indexnummern können dann an  den Indexparameter von **getItemInfoByType übergeben werden.** Dies ist nützlich, wenn ein digitales Medienelement beispielsweise unter mehreren Genren kategorisiert wurde.

Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

Diese Methode kann Fehler verursachen. Beim Aufrufen dieser Methode sollten Sie Fehlerbehandlungscode verwenden. In diesem Beispiel JScript Sie die Fehlerbehandlung implementieren, indem Sie **try... Fangen... finally-Struktur.**

**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Medienobjekt**](media-object.md)
</dt> <dt>

[**Media.attributeCount**](media-attributecount.md)
</dt> <dt>

[**Media.getAttributeCountByType**](media-getattributecountbytype.md)
</dt> <dt>

[**Media.getAttributeName**](media-getattributename.md)
</dt> <dt>

[**Media.getItemInfo**](media-getiteminfo.md)
</dt> <dt>

[**Media.setItemInfo**](media-setiteminfo.md)
</dt> <dt>

[**MetadataPicture-Objekt**](metadatapicture-object.md)
</dt> <dt>

[**MetadataText-Objekt**](metadatatext-object.md)
</dt> <dt>

[**Lesen von Attributwerten**](reading-attribute-values.md)
</dt> <dt>

[**Einstellungen.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Einstellungen.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 






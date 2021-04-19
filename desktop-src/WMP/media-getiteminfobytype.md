---
title: Media. getItemInfoByType-Methode
description: Die getItemInfoByType-Methode ruft den Wert des Attributs ab, das dem angegebenen Attributnamen, der angegebenen Sprache und dem angegebenen Index entspricht.
ms.assetid: 9d3377c2-7ae8-48ce-a42e-9c965f6b79f9
keywords:
- getItemInfoByType-Methode, Windows Media Player
- getItemInfoByType-Methode, Windows Media Player, Medienklasse
- Media Class Windows Media Player, getItemInfoByType-Methode
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
ms.openlocfilehash: bc2aff2bee7641075bbac1dd04526ee751ea077a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362101"
---
# <a name="mediagetiteminfobytype-method"></a>Media. getItemInfoByType-Methode

Die **getItemInfoByType** -Methode ruft den Wert des Attributs ab, das dem angegebenen Attributnamen, der angegebenen Sprache und dem angegebenen Index entspricht.

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

*Name* \[ in\]
</dt> <dd>

**Zeichenfolge** , die den Namen des Attributs enthält. Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Referenz](attribute-reference.md)zu Windows Media Player-Attributen.

</dd> <dt>

*Sprache* \[ in\]
</dt> <dd>

**Zeichenfolge** , die die Sprache darstellt. Wenn der Wert auf NULL oder "" (leere Zeichenfolge) festgelegt ist, wird die aktuelle Gebiets Schema Zeichenfolge verwendet. Andernfalls muss der Wert eine gültige RFC 1766-sprach Zeichenfolge sein, z. b. "en-US".

</dd> <dt>

*Index* \[ in\]
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
| Alle anderen Attribute        | **String**                     |



 

Bei Attributen, deren zugrunde liegender Wert **boolescher** Wert ist, gibt diese Methode die Zeichenfolge "true" oder "false" zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode ruft die Metadaten für ein einzelnes digitales Medien Element oder ein Medien Element ab, das Teil einer Wiedergabeliste ist.

Diese Methode unterstützt Attribute mit mehreren Werten und Attributen mit komplexen Werten. Die **getiteminfo** -Methode unterstützt keine Attribute mit mehreren Werten und Attributen mit komplexen Werten.

Die **AttributeCount** -Eigenschaft enthält die Anzahl von Attributnamen, die für ein bestimmtes **Medien** Objekt verfügbar sind. Index Nummern können dann mit der **GetAttributeName** -Methode verwendet werden, um den Namen der einzelnen verfügbaren Attribute zu bestimmen. Einzelne Attributnamen können an den *Name* -Parameter von **getItemInfoByType** übergeben werden.

Die **getattributezähltbytype** -Methode gibt die Anzahl von Attributen zurück, die einem bestimmten Attributnamen für ein bestimmtes **Medien** Objekt entsprechen. Indexnummern können dann an den *Index* -Parameter von **getItemInfoByType** übergeben werden. Dies ist hilfreich, wenn ein digitales Medien Element z. b. unter mehreren Genres kategorisiert wurde.

Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

Diese Methode kann zu Fehlern führen. Wenn Sie diese Methode aufgerufen haben, sollten Sie Fehler Behandlungs Code einschließen. In JScript können Sie z. b. die Fehlerbehandlung mithilfe von **try... catch... Abschließend** Struktur.

**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9 oder höher.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Medienobjekt**](media-object.md)
</dt> <dt>

[**Media. AttributeCount**](media-attributecount.md)
</dt> <dt>

[**Media. getattributecountrytbytype**](media-getattributecountbytype.md)
</dt> <dt>

[**Media. GetAttributeName**](media-getattributename.md)
</dt> <dt>

[**Media. getiteminfo**](media-getiteminfo.md)
</dt> <dt>

[**"Media. mentiteminfo"**](media-setiteminfo.md)
</dt> <dt>

[**MetadataPicture-Objekt**](metadatapicture-object.md)
</dt> <dt>

[**MetadataText-Objekt**](metadatatext-object.md)
</dt> <dt>

[**Lesen von Attributwerten**](reading-attribute-values.md)
</dt> <dt>

[**Settings. mediaaccessrights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestmediaaccessrights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 






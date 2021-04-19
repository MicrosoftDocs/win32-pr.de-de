---
title: Media. getiteminfo-Methode
description: Die getiteminfo-Methode ruft den Wert des angegebenen Attributs für das aktuelle Medien Element ab.
ms.assetid: a1ee0d40-b979-424b-bd4e-d1acf6354d8d
keywords:
- getiteminfo-Methode, Windows Media Player
- getiteminfo-Methode, Windows Media Player, Medienklasse
- Media Class Windows Media Player, getiteminfo-Methode
topic_type:
- apiref
api_name:
- Media.getItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef7e7348e73e3550ed668f6694ccfe9ed615215b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361696"
---
# <a name="mediagetiteminfo-method"></a>Media. getiteminfo-Methode

Die **getiteminfo** -Methode ruft den Wert des angegebenen Attributs für das aktuelle Medien Element ab.

## <a name="syntax"></a>Syntax


```JScript
strRetVal = Media.getItemInfo(
  name
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Name* \[ in\]
</dt> <dd>

**Zeichenfolge** , die den Namen des Attributs enthält. Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Referenz](attribute-reference.md)zu Windows Media Player-Attributen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine **Zeichenfolge** zurück, die den Wert des angegebenen Attributs darstellt. Bei Attributen, deren zugrunde liegender Wert **boolescher** Wert ist, wird die Zeichenfolge "true" oder "false" zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Diese Methode ruft die Metadaten für ein einzelnes digitales Medien Element oder ein Medien Element ab, das Teil einer Wiedergabeliste ist.

Die **AttributeCount** -Eigenschaft enthält die Anzahl von Attributnamen, die für ein bestimmtes **Medien** Objekt verfügbar sind. Index Nummern können dann mit der **GetAttributeName** -Methode verwendet werden, um den Namen der einzelnen verfügbaren Attribute zu bestimmen. Einzelne Attributnamen können an **getiteminfo** übermittelt werden.

Um Attribute mit mehreren Werten und Attributen mit komplexen Werten abzurufen, verwenden Sie die **getItemInfoByType** -Methode.

Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

Zum Freigeben der Windows Media-Bibliotheken über UPnP erstellt Windows Media Player einen Inhaltsverzeichnis Dienst (CDs), der über UPnP verfügbar gemacht wird. Andere Geräte können dann navigieren und die Bibliotheken durchsuchen.

In Windows 7 kann eine Anwendung die Attribute "Windows Media Player [**trackingID**](trackingid-attribute.md) " und " [**mediaType**](mediatype-attribute.md) " verwenden, um die Objekt-ID der einzelnen Elemente in den CDs zu erstellen. Beachten Sie, dass sich diese Konstruktion in zukünftigen Versionen von Windows ändern kann. Die Anwendung übergibt jede dieser Attribut Zeichenfolgen im *Name* -Parameter in einem Aufrufen von **getiteminfo**. **getiteminfo** gibt den Wert für jedes Attribut im Rückgabewert zurück. Die Anwendung verwendet dann die folgende Syntax, um jede Objekt-ID zu erstellen:

*TrackingID*. 0. *Mediatypeid*

Diese Syntax hat die folgende Bedeutung:

-   *TrackingID* ist die Zeichenfolge, die im Windows Media Player [**trackingID**](trackingid-attribute.md) -Attribut des Medien Elements gespeichert ist.
-   *Mediatypeid* hängt vom Wert des [**mediaType**](mediatype-attribute.md) -Attributs ab, wie in der folgenden Tabelle gezeigt:

    | MediaType-Attribut                      | Mediatypeid |
    |------------------------------------------|-------------|
    | [Audioelemente](audio-item-attributes.md) | 4           |
    | [Foto Elemente](photo-item-attributes.md) | B           |
    | [Video Elemente](video-item-attributes.md) | 8           |

    

     

**Windows Media Player 10 Mobile:** Attribute für ein Medien Element sind nur während der Wiedergabe verfügbar, es sei denn, Sie werden über die Medien Auflistung aus dem Element abgerufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Medienobjekt**](media-object.md)
</dt> <dt>

[**Media. AttributeCount**](media-attributecount.md)
</dt> <dt>

[**Media. GetAttributeName**](media-getattributename.md)
</dt> <dt>

[**Media. getItemInfoByType**](media-getiteminfobytype.md)
</dt> <dt>

[**"Media. mentiteminfo"**](media-setiteminfo.md)
</dt> <dt>

[**Lesen von Attributwerten**](reading-attribute-values.md)
</dt> <dt>

[**Settings. mediaaccessrights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestmediaaccessrights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 






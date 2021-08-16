---
title: Media.getItemInfo-Methode
description: Die getItemInfo-Methode ruft den Wert des angegebenen Attributs für das aktuelle Medienelement ab.
ms.assetid: a1ee0d40-b979-424b-bd4e-d1acf6354d8d
keywords:
- getItemInfo-Methode Windows Media Player
- getItemInfo-Methode Windows Media Player , Media-Klasse
- Medienklasse Windows Media Player , getItemInfo-Methode
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
ms.openlocfilehash: ab885a8505f3637d21f4a406e5a7c324ee6b9ec90e5ad0434a385e321072ccaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135153"
---
# <a name="mediagetiteminfo-method"></a>Media.getItemInfo-Methode

Die **getItemInfo-Methode** ruft den Wert des angegebenen Attributs für das aktuelle Medienelement ab.

## <a name="syntax"></a>Syntax


```JScript
strRetVal = Media.getItemInfo(
  name
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*name* \[ In\]
</dt> <dd>

**Zeichenfolge,** die den Namen des Attributs enthält. Informationen zu den attributen, die von Windows Media Player unterstützt werden, finden Sie in der Windows Media Player [Attributreferenz.](attribute-reference.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine **Zeichenfolge** zurück, die den Wert des angegebenen Attributs darstellt. Für Attribute, deren zugrunde liegender Wert **boolesch** ist, wird die Zeichenfolge "true" oder "false" zurückgegeben.

## <a name="remarks"></a>Hinweise

Diese Methode ruft die Metadaten für ein einzelnes digitales Medienelement oder ein Medienelement ab, das Teil einer Wiedergabeliste ist.

Die **attributeCount-Eigenschaft** enthält die Anzahl der Attributnamen, die für ein bestimmtes **Media-Objekt** verfügbar sind. Indexnummern können dann mit der **getAttributeName-Methode** verwendet werden, um den Namen jedes verfügbaren Attributs zu bestimmen. Einzelne Attributnamen können an **getItemInfo** übergeben werden.

Verwenden Sie die **getItemInfoByType-Methode,** um Attribute mit mehreren Werten und Attribute mit komplexen Werten abzurufen.

Um diese Methode zu verwenden, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

Um die Windows Medienbibliotheken über UPnP freizugeben, erstellt Windows Media Player einen Inhaltsverzeichnisdienst (Content Directory Service, CDS), der über UPnP verfügbar gemacht wird. Andere Geräte können dann in den Bibliotheken navigieren und diese durchsuchen.

In Windows 7 kann eine Anwendung die Attribute Windows Media Player [**TrackingID**](trackingid-attribute.md) und [**MediaType**](mediatype-attribute.md) verwenden, um die Objekt-ID jedes Elements im CDS zu erstellen. Beachten Sie, dass sich diese Konstruktion in zukünftigen Versionen von Windows ändern kann. Die Anwendung übergibt jede dieser Attributzeichenfolgen im *name-Parameter* in einem Aufruf von **getItemInfo.** **getItemInfo** gibt den Wert für jedes Attribut im Rückgabewert zurück. Die Anwendung verwendet dann die folgende Syntax, um jede Objekt-ID zu erstellen:

*TrackingID*.0. *MediaTypeID*

Diese Syntax hat die folgende Bedeutung:

-   *TrackingID* ist die Zeichenfolge, die im Windows Media Player [**TrackingID-Attribut**](trackingid-attribute.md) des Medienelements gespeichert wird.
-   *MediaTypeID* hängt vom Wert des [**MediaType-Attributs**](mediatype-attribute.md) ab, wie in der folgenden Tabelle gezeigt:

    | MediaType-Attribut                      | MediaTypeID |
    |------------------------------------------|-------------|
    | [Audioelemente](audio-item-attributes.md) | 4           |
    | [Fotoelemente](photo-item-attributes.md) | B           |
    | [Videoelemente](video-item-attributes.md) | 8           |

    

     

**Windows Media Player 10 Mobile:** Attribute für ein Medienelement sind nur während der Wiedergabe verfügbar, es sei denn, sie werden über die Medienauflistung aus dem Element abgerufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Medienobjekt**](media-object.md)
</dt> <dt>

[**Media.attributeCount**](media-attributecount.md)
</dt> <dt>

[**Media.getAttributeName**](media-getattributename.md)
</dt> <dt>

[**Media.getItemInfoByType**](media-getiteminfobytype.md)
</dt> <dt>

[**Media.setItemInfo**](media-setiteminfo.md)
</dt> <dt>

[**Lesen von Attributwerten**](reading-attribute-values.md)
</dt> <dt>

[**Einstellungen.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Einstellungen.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 






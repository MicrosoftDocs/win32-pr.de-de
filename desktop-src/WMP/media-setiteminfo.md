---
title: Media. mentiteminfo-Methode
description: Die setiteminfo-Methode legt den Wert des angegebenen Attributs für das aktuelle Medien Element fest.
ms.assetid: 8c4ce954-45cb-4a67-9660-1a013ecd64c3
keywords:
- Media Player der Methode "stiteminfo"
- Methode "stiteminfo" (Windows Media Player, Medienklasse)
- Medienklasse, Windows Media Player, Methode "stiteminfo"
topic_type:
- apiref
api_name:
- Media.setItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b918e6a388cab750cc379611f5f55c6a1b1d256c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372619"
---
# <a name="mediasetiteminfo-method"></a>Media. mentiteminfo-Methode

Die **setiteminfo** -Methode legt den Wert des angegebenen Attributs für das aktuelle Medien Element fest.

## <a name="syntax"></a>Syntax


```JScript
Media.setItemInfo(
  attribute,
  value
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Attribut* \[ in\]
</dt> <dd>

**Zeichenfolge** , die den Attributnamen enthält. Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Referenz](attribute-reference.md)zu Windows Media Player-Attributen.

</dd> <dt>

*Wert* \[ in\]
</dt> <dd>

**Zeichenfolge** , die den neuen Wert enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die **AttributeCount** -Eigenschaft enthält die Anzahl der für ein bestimmtes **Medien** Objekt verfügbaren Attribute. Index Nummern können dann mit der **GetAttributeName** -Methode verwendet werden, um die Namen der integrierten Attribute zu bestimmen, die mit dieser Methode verwendet werden können.

Verwenden Sie vor der Verwendung dieser Methode die **isread onlyitem** -Methode, um zu bestimmen, ob ein bestimmtes Attribut festgelegt werden kann.

Um diese Methode verwenden zu können, ist der vollständige Zugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

**Hinweis**

Wenn Sie das Windows Media Player-Steuerelement in Ihre Anwendung einbetten, werden Dateiattribute, die Sie ändern, erst dann in die digitale Mediendatei geschrieben, wenn der Benutzer Windows Media Player ausführt. Wenn Sie das-Steuerelement in einer Remote Anwendung verwenden, die in C++ geschrieben ist, werden die Dateiattribute, die Sie ändern, kurz nach dem vornehmen der Änderungen in die digitale Mediendatei geschrieben. In beiden Fällen sind die Änderungen sofort über die Bibliothek für Ihren Code verfügbar.

**Windows Media Player 10 Mobile:** Diese Methode ist nicht implementiert.

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel werden *Medien* verwendet. " **stiteminfo** ", um den Wert des Genre-Attributs für das aktuelle Medien Element zu ändern. Mit einem HTML-Texteingabe Element namens gentext kann der Benutzer eine Text Zeichenfolge eingeben, mit der die Attributinformationen geändert werden. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```JScript
<!-- Create the button element. -->
<INPUT type = "BUTTON"  id = "NEWGEN"  name = "NEWGEN"  value = "Change Genre" 
onClick = "
    /* Store the current media item. */
    var cm = Player.currentMedia;

    /* Get the user input from the text box. */
    var atValue = genText.value;

    /* Test for read-only status of the attribute. */
    if(cm.isReadOnlyItem('Genre') == false){

        /* Change the attribute value. */
        cm.setItemInfo('Genre' ,atValue);
    } 
">

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Medienobjekt**](media-object.md)
</dt> <dt>

[**Media. getiteminfo**](media-getiteminfo.md)
</dt> <dt>

[**Media. isleseronlyitem**](media-isreadonlyitem.md)
</dt> <dt>

[**Settings. mediaaccessrights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestmediaaccessrights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 






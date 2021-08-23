---
title: Media.setItemInfo-Methode
description: Die setItemInfo-Methode legt den Wert des angegebenen Attributs für das aktuelle Medienelement fest.
ms.assetid: 8c4ce954-45cb-4a67-9660-1a013ecd64c3
keywords:
- setItemInfo-Windows Media Player
- setItemInfo-Methode Windows Media Player , Media-Klasse
- Medienklasse Windows Media Player , setItemInfo-Methode
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
ms.openlocfilehash: b1639b86ce1e0643f3d6ce255e5ca492bc4fae0c1301e1a568a0c5609ceda2a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119647970"
---
# <a name="mediasetiteminfo-method"></a>Media.setItemInfo-Methode

Die **setItemInfo-Methode** legt den Wert des angegebenen Attributs für das aktuelle Medienelement fest.

## <a name="syntax"></a>Syntax


```JScript
Media.setItemInfo(
  attribute,
  value
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Attribut* \[ In\]
</dt> <dd>

**Eine Zeichenfolge,** die den Attributnamen enthält. Informationen zu den attributes, die von Windows Media Player unterstützt werden, finden Sie in der Windows Media Player [Attribute Reference](attribute-reference.md).

</dd> <dt>

*value* \[ In\]
</dt> <dd>

**Eine Zeichenfolge,** die den neuen Wert enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **attributeCount-Eigenschaft** enthält die Anzahl von Attributen, die für ein bestimmtes **Media-Objekt verfügbar** sind. Indexnummern können dann mit der **getAttributeName-Methode** verwendet werden, um die Namen der integrierten Attribute zu bestimmen, die mit dieser Methode verwendet werden können.

Verwenden Sie vor der Verwendung dieser Methode die **isReadOnlyItem-Methode,** um zu bestimmen, ob ein bestimmtes Attribut festgelegt werden kann.

Um diese Methode verwenden zu können, ist Vollzugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

**Hinweis**

Wenn Sie das Windows Media Player-Steuerelement in Ihre Anwendung einbetten, werden dateiattribute, die Sie ändern, erst dann in die digitale Mediendatei geschrieben, wenn der Benutzer Windows Media Player. Wenn Sie das Steuerelement in einer in C++ geschriebenen Remoteanwendung verwenden, werden Dateiattribute, die Sie ändern, kurz nach dem Vornehmen der Änderungen in die digitale Mediendatei geschrieben. In beiden Fällen sind die Änderungen sofort über die Bibliothek für Ihren Code verfügbar.

**Windows Media Player 10 Mobile:** Diese Methode ist nicht implementiert.

## <a name="examples"></a>Beispiele

Im folgenden beispiel JScript Media *verwendet.* **setItemInfo,** um den Wert des Genre-Attributs für das aktuelle Medienelement zu ändern. Ein HTML TEXT-Eingabeelement mit dem Namen genText ermöglicht dem Benutzer die Eingabe einer Textzeichenfolge, die dann zum Ändern der Attributinformationen verwendet wird. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Medienobjekt**](media-object.md)
</dt> <dt>

[**Media.getItemInfo**](media-getiteminfo.md)
</dt> <dt>

[**Media.isReadOnlyItem**](media-isreadonlyitem.md)
</dt> <dt>

[**Einstellungen.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Einstellungen.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 






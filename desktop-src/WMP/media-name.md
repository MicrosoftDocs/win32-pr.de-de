---
title: Media.name
description: Die Name-Eigenschaft gibt den Namen des Medien Elements an oder ruft ihn ab.
ms.assetid: 68aba78a-86fd-4411-9ac4-58f38d915e2c
keywords:
- Media.Name Windows Media Player
topic_type:
- apiref
api_name:
- Media.name
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9de8095d88c3ddec9049e0b43461adcf5553ec74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368585"
---
# <a name="medianame"></a>Media.name

Die **Name** -Eigenschaft gibt den Namen des Medien Elements an oder ruft ihn ab.

## <a name="syntax"></a>Syntax

*Player*. *currentMedia*. **Name**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine Lese- **/schreibzeichenfolge** , die den Namen des Medien Elements enthält.

## <a name="remarks"></a>Bemerkungen

Zum Abrufen des Werts dieser Eigenschaft ist Lesezugriff auf die Bibliothek erforderlich. Um den Wert dieser Eigenschaft anzugeben, ist der vollständige Zugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

Bevor Sie diese Methode verwenden, um den Namen eines Medien Elements anzugeben, verwenden Sie **isleseronlyitem** , um zu bestimmen, ob der Name festgelegt werden kann.

**Windows Media Player 10 Mobile:** Diese Eigenschaft ist schreibgeschützt.

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel werden *Medien* verwendet. **Name** , um den Namen des aktuellen Medien Elements zu ändern. Mit einem HTML-Text Eingabe Element namens "NameText" kann der Benutzer eine Text Zeichenfolge für den neuen Namen eingeben. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```JScript
<!<entity type="mdash"/>-Create an HTML BUTTON element to execute the name change. -->
<INPUT type = "BUTTON"  id = "NewName"  name = "NewName"  value = "Change Name" 
    onClick = "

        /* Store the current media item. */
        var cm = Player.currentMedia;

        /* Change the name. */
        cm.name = NameText.value;
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

[**Settings. mediaaccessrights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestmediaaccessrights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 






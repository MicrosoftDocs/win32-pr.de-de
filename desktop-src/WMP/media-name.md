---
title: Media.name
description: Die Name-Eigenschaft gibt den Namen des Medienelements an oder ruft diesen ab.
ms.assetid: 68aba78a-86fd-4411-9ac4-58f38d915e2c
keywords:
- Media.name Windows Media Player
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
ms.openlocfilehash: 3abe6df00b5674cfbd443a5838b208814e30c5ecf75875586907314fc3a39d9f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119616856"
---
# <a name="medianame"></a>Media.name

Die **Name-Eigenschaft** gibt den Namen des Medienelements an oder ruft diesen ab.

## <a name="syntax"></a>Syntax

*Player*. *currentMedia*. **Name**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine  Zeichenfolge mit Lese-/Schreibzugriff, die den Namen des Medienelements enthält.

## <a name="remarks"></a>Hinweise

Zum Abrufen des Werts dieser Eigenschaft ist Lesezugriff auf die Bibliothek erforderlich. Um den Wert dieser Eigenschaft anzugeben, ist Vollzugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

Bevor Sie diese Methode verwenden, um den Namen eines Medienelements anzugeben, verwenden Sie **isReadOnlyItem,** um zu bestimmen, ob der Name festgelegt werden kann.

**Windows Media Player 10 Mobile:** Diese Eigenschaft ist schreibgeschützt.

## <a name="examples"></a>Beispiele

Im folgenden beispiel JScript Media *verwendet.* **Name,** um den Namen des aktuellen Medienelements zu ändern. Mit einem HTML TEXT-Eingabeelement namens NameText kann der Benutzer eine Textzeichenfolge für den neuen Namen eingeben. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Medienobjekt**](media-object.md)
</dt> <dt>

[**Einstellungen.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Einstellungen.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 






---
title: Player.launchURL-Methode
description: Die launchURL-Methode sendet eine URL an den Standardbrowser des Benutzers, der gerendert werden soll. | Player.launchURL-Methode
ms.assetid: 2b445e59-f884-4519-9acb-f349319429d2
keywords:
- launchURL-Methode Windows Media Player
- launchURL-Methode Windows Media Player , Player-Klasse
- Player-Klasse Windows Media Player , launchURL-Methode
topic_type:
- apiref
api_name:
- Player.launchURL
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79d22c65a29aaee9c849677dfa42acb5769bf30d2fb7079e305ee79632ef22e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134823"
---
# <a name="playerlaunchurl-method"></a>Player.launchURL-Methode

Die **launchURL-Methode** sendet eine URL an den Standardbrowser des Benutzers, der gerendert werden soll.

## <a name="syntax"></a>Syntax


```JScript
Player.launchURL(
  URL
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*URL* \[ In\]
</dt> <dd>

**Zeichenfolgenwert,** der die zu startde URL darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode öffnet nur Webseiten, die das HTTP- oder HTTPS-Protokoll verwenden.

**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein HTML BUTTON-Element erstellt, das beim Klicken die Microsoft-Website in einem neuen Browserfenster anzeigt. Das **Player-Element** wurde mit der ID = "Player" erstellt.


```JScript
<INPUT  TYPE = "BUTTON"  ID = "GOTOMS"  VALUE = "Microsoft.com"  onClick = "

    /* Open the Microsoft website. */
    Player.launchURL('https://www.microsoft.com');
">

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> </dl>

 

 






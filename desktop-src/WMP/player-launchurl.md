---
title: Player. launchurl-Methode
description: Die launchurl-Methode sendet eine URL an den Standardbrowser des Benutzers, der gerendert werden soll. | Player. launchurl-Methode
ms.assetid: 2b445e59-f884-4519-9acb-f349319429d2
keywords:
- launchurl-Methode, Windows Media Player
- launchurl-Methode, Windows Media Player, Player-Klasse
- Player-Klasse, Windows Media Player, launchurl-Methode
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
ms.openlocfilehash: 3c496e8f40f4d7c8a21e718b820e438d3ce32ad1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359281"
---
# <a name="playerlaunchurl-method"></a>Player. launchurl-Methode

Die **launchurl** -Methode sendet eine URL an den Standardbrowser des Benutzers, der gerendert werden soll.

## <a name="syntax"></a>Syntax


```JScript
Player.launchURL(
  URL
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*URL* \[ in\]
</dt> <dd>

**Zeichen** folgen Wert, der die zu startende URL darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode öffnet nur Webseiten mithilfe der http-oder HTTPS-Protokolle.

**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein HTML-Schaltflächen Element erstellt, das, wenn darauf geklickt wird, die Microsoft-Website in einem neuen Browserfenster anzeigt. Das **Player** -Element wurde mit ID = "Player" erstellt.


```JScript
<INPUT  TYPE = "BUTTON"  ID = "GOTOMS"  VALUE = "Microsoft.com"  onClick = "

    /* Open the Microsoft website. */
    Player.launchURL('https://www.microsoft.com');
">

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> </dl>

 

 






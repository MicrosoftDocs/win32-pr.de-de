---
title: Player.URL
description: Die URL-Eigenschaft gibt den Namen des zu wiedergebenden Medienelements an oder ruft diesen ab.
ms.assetid: 74987ffd-c625-4d30-9f5f-5170119158f9
keywords:
- Player.URL-Windows Media Player
topic_type:
- apiref
api_name:
- Player.URL
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a00a6513350ee9c39855aba8168faf9ced788a0686a0fdbe845013dcc521142f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572039"
---
# <a name="playerurl"></a>Player.URL

Die **URL-Eigenschaft** gibt den Namen des zu wiedergebenden Medienelements an oder ruft diesen ab.

## <a name="syntax"></a>Syntax

*Player* . **URL**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine **Zeichenfolge** mit Lese-/Schreibzugriff ohne Standardwert.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft kann nur auf eine URL in einer Sicherheitszone festgelegt werden, die identisch oder weniger restriktiv als die Sicherheitszone des aufrufenden Programms oder der Webseite ist.

Anwendungen, die Medienelemente hinter einer Firewall öffnen, haben eine bessere Leistung, wenn die Adresse mit dem DNS-Namen (Domain Name Server) anstelle der IP-Adresse angegeben wird.

Rufen Sie diese Methode nicht aus Ereignishandlercode auf. Aufrufen von *Player*. **Die URL** eines Ereignishandlers kann zu unerwarteten Ergebnissen führen.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel werden ein HTML TEXT-Eingabeelement und ein HTML BUTTON-Eingabeelement erstellt. Mit dem TEXT-Element kann der Benutzer einen Pfad eingeben, um eine zu wiedergebende digitale Mediendatei anzugeben. Das BUTTON-Element führt JScript aus, der die Datei öffnet und Windows Media Player startet. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


```JScript
<!-- Create an INPUT control to get a file path from the user. -->
<INPUT Type = "TEXT" ID = "inputURL">

<!-- Create a BUTTON control to execute the script. -->
<INPUT  Type = "BUTTON"  ID = "openMedia"  VALUE = "Open Media"
    onClick = "
        /* Specify the URL obtained from user input. */
        Player.URL = inputURL.value;

        /* Start the Player. */
        Player.controls.play();
">

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> </dl>

 

 






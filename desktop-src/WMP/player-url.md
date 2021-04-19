---
title: Player. URL
description: Die URL-Eigenschaft gibt den Namen des zu Wiedergabe enden Medien Elements an oder ruft ihn ab.
ms.assetid: 74987ffd-c625-4d30-9f5f-5170119158f9
keywords:
- Player. URL-Windows-Media Player
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
ms.openlocfilehash: 62d4f0c75ac0dddeeaced0f1a3a6f1247df4ae36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372336"
---
# <a name="playerurl"></a>Player. URL

Die **URL** -Eigenschaft gibt den Namen des zu Wiedergabe enden Medien Elements an oder ruft ihn ab.

## <a name="syntax"></a>Syntax

*Player* . **URL**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine Lese- **/schreibzeichenfolge** ohne Standardwert.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft kann nur auf eine URL in einer Sicherheitszone festgelegt werden, die identisch ist oder weniger restriktiv ist als die Sicherheitszone des aufrufenden Programms oder der Webseite.

Anwendungen, die Medienelemente hinter einer Firewall öffnen, haben eine bessere Leistung, wenn die Adresse anstelle der IP-Adresse mit dem DNS-Namen (Domain Nameserver) angegeben wird.

Diese Methode kann nicht aus dem Ereignishandlercode aufgerufen werden. Aufruf *Player*. Die **URL** eines Ereignis Handlers kann zu unerwarteten Ergebnissen führen.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel werden ein HTML-Text Eingabe Element und ein HTML-Schaltflächen-Eingabe Element erstellt. Mit dem Text-Element kann der Benutzer einen Pfad eingeben, um eine digitale Mediendatei anzugeben, die abgespielt werden soll. Das Button-Element führt JScript aus, das die Datei öffnet und Windows Media Player startet. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> </dl>

 

 






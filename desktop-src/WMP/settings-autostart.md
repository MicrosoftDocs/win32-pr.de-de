---
title: Einstellungen. Autostart
description: Mit der Autostart-Eigenschaft wird ein Wert angegeben oder abgerufen, der angibt, ob das aktuelle Medien Element automatisch wiedergegeben wird.
ms.assetid: 553f8534-9e3e-4fdc-bfc1-551939969289
keywords:
- Einstellungen. Autostart-Windows-Media Player
topic_type:
- apiref
api_name:
- Settings.autoStart
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d08b8f84f4a0b51225ed5692a25fa41cab809ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364816"
---
# <a name="settingsautostart"></a>Einstellungen. Autostart

Mit der **Autostart** -Eigenschaft wird ein Wert angegeben oder abgerufen, der angibt, ob das aktuelle Medien Element automatisch wiedergegeben wird.

## <a name="syntax"></a>Syntax

Player. Settings. Autostart

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist ein **boolescher** Wert mit Lese-/Schreibzugriff.



| Wert | BESCHREIBUNG                                                         |
|-------|---------------------------------------------------------------------|
| true  | Standard. Das Medien Element beginnt automatisch (siehe Hinweise). |
| false | Das Medien Element beginnt nicht automatisch mit der Wiedergabe.                |



 

## <a name="remarks"></a>Bemerkungen

Wenn **Autostart** auf true festgelegt ist, beginnt das Medien Element mit der Wiedergabe beim *Player*. **URL**, *Player*. **currentwiedergabe**, oder *Player*. **currentMedia** wird festgelegt. Andernfalls wird die Wiedergabe bis zu den Steuer *Elementen* nicht gestartet. die **Play** -Methode wird aufgerufen.

Da die **Autostart** -Eigenschaft für den vollständigen Modus von Windows Media Player Global durch externe Ereignisse (z. b. das Laden einer CD) festgelegt werden kann, gibt es keinen zuverlässigen Standardwert für Skins und Remote Player-Steuerelemente. Dies liegt daran, dass die Wiedergabe-Engine des vollmodusplayers in beiden Fällen verwendet wird.

Legen Sie **Autostart** direkt vor dem Festlegen von *Player* auf false fest. **URL**, *Player*. **currentwiedergabe**, oder *Player*. **currentMedia** in Skins und Remote Windows Media Player-Steuerelemente, wenn Sie sicherstellen möchten, dass das Medien Element nicht sofort wiedergegeben wird. Außerdem sollten Sie diese Einstellung nicht als Ersatz für die Verwendung der Steuer *Elemente* verwenden, es sei denn, Sie legen **Autostart** direkt vor der Angabe eines Medien Elements auf true fest. **Wiedergabe** Methode.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein HTML-Checkbox-Element erstellt, mit dem der Benutzer angeben kann, ob das aktuelle Medien Element vom Player-Steuerelement automatisch abgespielt wird. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```
<!-- Create an HTML CHECKBOX control. -->
<INPUT  TYPE = "CHECKBOX" ID = AS
              onClick = "
    /* Use the CHECKBOX state to specify the value 
       of the autoStart property. */
    Player.settings.autoStart = AS.checked;
"> 

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Player. currentMedia**](player-currentmedia.md)
</dt> <dt>

[**Player. URL**](player-url.md)
</dt> <dt>

[**Einstellungs Objekt**](settings-object.md)
</dt> </dl>

 

 






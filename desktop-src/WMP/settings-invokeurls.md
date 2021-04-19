---
title: Settings. invokeurls
description: Die invokeurls-Eigenschaft gibt einen Wert an, der angibt, ob URL-Ereignisse einen Webbrowser starten sollen, oder ruft ihn ab.
ms.assetid: 3a28d949-96b7-4c21-97c5-2442c2f7baa5
keywords:
- Settings. invokeurls-Windows-Media Player
topic_type:
- apiref
api_name:
- Settings.invokeURLs
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb55bb61243e6905a51a943a26adc120511335c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352956"
---
# <a name="settingsinvokeurls"></a>Settings. invokeurls

Die **invokeurls** -Eigenschaft gibt einen Wert an, der angibt, ob URL-Ereignisse einen Webbrowser starten sollen, oder ruft ihn ab.

## <a name="syntax"></a>Syntax

Player. Settings. invokeurls

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist ein **boolescher** Wert mit Lese-/Schreibzugriff.



| Wert | BESCHREIBUNG                                  |
|-------|----------------------------------------------|
| true  | Standard. Mit URL-Ereignissen sollte ein Browser gestartet werden. |
| false | Bei URL-Ereignissen sollte kein Browser gestartet werden.      |



 

## <a name="remarks"></a>Bemerkungen

Mediendateien können URLs enthalten. Wenn eine URL an das Windows Media Player-Steuerelement gesendet wird, wird Sie unabhängig vom Wert in **invokeurls** zuerst an den **ScriptCommand** -Ereignishandler übergeben. Nachdem **ScriptCommand** beendet wurde, prüft Windows Media Player **invokeurls** , ob der Standard Internet Browser mit der URL gestartet werden soll. Sie können URLs selektiv anzeigen, indem Sie Sie in **ScriptCommand** überprüfen und **invokeurls** wie gewünscht festlegen.

**Windows Media Player 10 Mobile**: Diese Eigenschaft akzeptiert nur "false" oder gibt "false" zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Player. ScriptCommand-Ereignis**](player-player-scriptcommand.md)
</dt> <dt>

[**Einstellungs Objekt**](settings-object.md)
</dt> </dl>

 

 






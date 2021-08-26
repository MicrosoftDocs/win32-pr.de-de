---
title: Einstellungen.invokeURLs
description: Die invokeURLs-Eigenschaft gibt einen Wert an, der angibt, ob URL-Ereignisse einen Webbrowser starten sollen, oder ruft diesen ab.
ms.assetid: 3a28d949-96b7-4c21-97c5-2442c2f7baa5
keywords:
- Einstellungen.invokeURLs Windows Media Player
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
ms.openlocfilehash: 75de25c5b4a18b6d53423657dc7180fe58cb095f3244800c2c42593d1d450e7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002402"
---
# <a name="settingsinvokeurls"></a>Einstellungen.invokeURLs

Die **invokeURLs-Eigenschaft** gibt einen Wert an, der angibt, ob URL-Ereignisse einen Webbrowser starten sollen, oder ruft diesen ab.

## <a name="syntax"></a>Syntax

player.settings.invokeURLs

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist ein **boolescher Lese-/Schreibzugriff.**



| Wert | BESCHREIBUNG                                  |
|-------|----------------------------------------------|
| true  | Standard. URL-Ereignisse sollten einen Browser starten. |
| false | URL-Ereignisse sollten keinen Browser starten.      |



 

## <a name="remarks"></a>Hinweise

Mediendateien können URLs enthalten. Wenn eine URL an das Windows Media Player-Steuerelement gesendet wird, wird sie unabhängig vom Wert in **invokeURLs** zuerst an den **ScriptCommand-Ereignishandler** übergeben. Nach dem Beenden von **ScriptCommand** überprüft Windows Media Player **invokeURLs,** um zu bestimmen, ob der Standardinternetbrowser mit der URL gestartet werden soll. Sie können URLs selektiv anzeigen, indem Sie sie in **ScriptCommand** überprüfen und **invokeURLs** wie gewünscht festlegen.

**Windows Media Player 10 Mobile:** Diese Eigenschaft akzeptiert nur false oder gibt sie zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Player.ScriptCommand-Ereignis**](player-player-scriptcommand.md)
</dt> <dt>

[**Einstellungen Objekt**](settings-object.md)
</dt> </dl>

 

 






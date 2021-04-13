---
description: Führt die erforderliche Initialisierung aus, damit die aufrufenden App eine miracast-Anzeige Senke werden kann.
ms.assetid: D87B427B-0B7F-44BB-BC34-726FDF87CCCC
title: Wsddisplaysink Start-Funktion (WF-Sink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDStartDisplaySink
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: 423ca68364fbe7c4beb89ab3b1d9f8e8fdb891be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528157"
---
# <a name="wfddisplaysinkstart-function"></a>Wsddisplaysink Start-Funktion

Führt die erforderliche Initialisierung aus, damit die aufrufenden App eine miracast-Anzeige Senke werden kann. Ihre APP sollte diese einmal beim Start abrufen.

## <a name="syntax"></a>Syntax


```C++
DWORD WINAPI WFDStartDisplaySink(
  _In_     USHORT                                 uDeviceCategory,
  _In_     USHORT                                 uSubCategory,
  _In_opt_ PVOID                                  pCallbackContext,
  _In_     WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK *pfnCallback
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ude vicecategory* \[ in\]
</dt> <dd>

Die Gerätekategorie.

</dd> <dt>

*usubcategory* \[ in\]
</dt> <dd>

Die Unterkategorie des Geräts.

</dd> <dt>

*pcallbackcontext* \[ in, optional\]
</dt> <dd>

Ein optionaler Kontext Zeiger, der an die Rückruffunktion übergeben wird, die im *pfncallback* -Parameter angegeben ist.

</dd> <dt>

*pfncallback* \[ in\]
</dt> <dd>

Ein Zeiger auf die Rückruffunktion, die aufgerufen werden soll, wenn eine Benachrichtigung für die APP vorliegt. Benachrichtigungen, die gesendet werden können, werden in [**WFD- \_ \_ \_ Benachrichtigungs \_ Rückruf-Benachrichtigungs Rückruf**](wfd-display-sink-notification-callback.md)beschrieben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.

Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Rückgabecodes sein.



| Rückgabecode                                                                                          | Beschreibung                                                    |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**Fehler \_ nicht \_ unterstützt**</dt> </dl> | Die Anzeige Senke wird auf dieser Hardware nicht unterstützt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Funktion führt die folgenden Aufgaben aus:

-   Macht den PC auffallen
-   Legt die P2P-Geräteinformationen so fest, dass Sie die angegebene Kategorie und Unterkategorie reflektieren.
-   Legt die miracast-IES in allen Wi-Fi direkten Frames mit dem Gerätetyp als Senke fest.
-   Registriert den angegebenen Rückruf, der immer dann aufgerufen wird, wenn eine eingehende Verbindung vorhanden ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows 10<br/>                                                                      |
| Ende des Supports (Server)<br/>    | Windows Server 2016<br/>                                                             |
| Header<br/>                   | <dl> <dt>WF-Senke. h</dt> </dl>       |
| Bibliothek<br/>                  | <dl> <dt>Wifdisplay. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wifidisplay.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WFD- \_ Anzeige \_ Senke- \_ Benachrichtigungs \_ Rückruf**](wfd-display-sink-notification-callback.md)
</dt> </dl>

 

 





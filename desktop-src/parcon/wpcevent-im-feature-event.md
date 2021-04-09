---
description: Pro-Benutzer-Ereignis, das von einem Instant Messaging-Client generiert wird, wenn definierte Funktionen in Eltern Steuerelementen verwendet werden.
ms.assetid: 45e80314-90b1-4fcf-9c8f-c9840ae1775b
title: WPCEVENT_IM_FEATURE-Ereignis (wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee28f004560ed287bc3cb94cbee1bda876355834
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959628"
---
# <a name="wpcevent_im_feature-event"></a>Wpcevent \_ im- \_ Funktions Ereignis

Pro-Benutzer-Ereignis, das von einem Instant Messaging-Client generiert wird, wenn definierte Funktionen in Eltern Steuerelementen verwendet werden.


```C++
const EVENT_DESCRIPTOR WPCEVENT_IM_FEATURE = {0xb, 0x0, 0x10, 0x4, 0x16, 0xb, 0x8000000000000030};
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*AppName* 
</dt> <dd>

Der Name der Instant Messaging-Anwendung.

</dd> <dt>

*AppVersion* 
</dt> <dd>

Die Versions Zeichenfolge für die Anwendung.

</dd> <dt>

*AccountName* 
</dt> <dd>

Der Instant Messaging-Konto Name dieses Benutzers.

</dd> <dt>

*Geseld* 
</dt> <dd>

Die ID für diese Konversation.

</dd> <dt>

*MediaType* 
</dt> <dd>

Ein Wert der [**wpcflag \_ im \_**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_im_feature) -featureenumeration, der Informationen zu den Funktionen angibt, auf die während einer sofortigen Messaging Interaktion zugegriffen wurde.

</dd> <dt>

*`Reason`* 
</dt> <dd>

Ein Wert der [**wpcflag \_ isblockierte**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) -Enumeration, die Informationen darüber angibt, welche Ereignisse von der Verwendung blockiert werden und welche Steuerelemente vorhanden sind.

</dd> <dt>

*Anzahl der Mitarbeiter* 
</dt> <dd>

Gibt die Anzahl von Instant Messaging-Benutzern an, die die Funktion erhalten und deren Identitäten im Feld Empfänger definiert sind.

</dd> <dt>

*Recipient* 
</dt> <dd>

Eine Zeichenfolge mit Trennzeichen, die Instant Messaging-Konto Identitäten aller Benutzer enthält, die das Feature erhalten.

</dd> <dt>

*Sender* 
</dt> <dd>

Der Instant Messaging-Kontoname für den Benutzer, der das Feature einrichtet.

</dd> <dt>

*Senderip* 
</dt> <dd>

Die IP-Adresse des Absenders des Absenders.

</dd> <dt>

*Daten* 
</dt> <dd>

Die Beschreibung der Daten in der Funktion.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                             |
| Header<br/>                   | <dl> <dt>Wpcevent. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Verwenden von Protokollierungs-APIs für Eltern Steuerelemente](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[**WPC \_ args \_ Conversation ationinitevent**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 





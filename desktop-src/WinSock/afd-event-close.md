---
description: Winsock-Netzwerkablaufverfolgungs-Ereignis für SocketClose.
ms.assetid: C59B2B51-288A-46C9-B390-26A18DB0C2FB
title: AFD_EVENT_CLOSE Ereignis
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AFD_EVENT_CLOSE
api_type:
- NA
api_location: ''
ms.openlocfilehash: fbc6c63a3084db6a9be0a4b4ea7672d84881a29a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751488"
---
# <a name="afd_event_close-event"></a>Ereignis zum Schließen von AFD- \_ Ereignissen \_

Das Ereignis für die **AFD- \_ Ereignis \_ Schließung** ist ein Winsock-Netzwerk Ablauf Verfolgungs Ereignis für den socketschließ Vorgang.


```C++
const EVENT_DESCRIPTOR AFD_EVENT_CLOSE = {0x3e9, 0x0, 0x10, 0x4, 0xf, 0x3e9, 0x8000000000000004};
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Enterexit* 
</dt> <dd>

Informationen zu diesem Ereignis.

In der folgenden Tabelle sind die möglichen Werte für den Parameter " *enterexit* " aufgeführt:



| Wert                                                                        | Bedeutung                                                                                              |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Der Start einer Winsock-Anforderung.<br/>                                                           |
| <dl> <dt>1</dt> </dl> | Die Winsock-Anforderung wurde abgeschlossen.<br/>                                                            |
| <dl> <dt>2</dt> </dl> | Der Winsock-AFD-Treiber hat eine interne Aktion ausgeführt (z. b. eine Verbindung abgebrochen).<br/>      |
| <dl> <dt>3</dt> </dl> | Der TCP/IP-Treiber hat dieses Ereignis verursacht. Dies weist normalerweise auf eine Daten Benachrichtigung hin.<br/> |
| <dl> <dt>4</dt> </dl> | Der Winsock-AFD-Treiber hat dieses Ereignis ausgelöst (z. b. das Festlegen einer Socketoption).<br/> |



 

</dd> <dt>

*Location* 
</dt> <dd>

Ein privates Feld, das intern verwendet wird.

</dd> <dt>

*Prozess* 
</dt> <dd>

Die [EPROCESS](/windows-hardware/drivers/kernel/eprocess) -Adresse des Prozesses, der den zugehörigen Socket besitzt. Dies ist eine nicht transparente Struktur, die als Prozess Objekt für einen Prozess dient. Weitere Informationen finden Sie in der Dokumentation zum Windows-Treiberkit für die [EPROCESS](/windows-hardware/drivers/kernel/eprocess) -Struktur.

</dd> <dt>

*Endpunkt* 
</dt> <dd>

Die AFD- \_ Endpunkt Adresse des Sockets.

</dd> <dt>

*Status* 
</dt> <dd>

Der NTSTATUS-Code für den Vorgang.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das Ereignis für die **AFD- \_ Ereignis \_ Schließung** wird nachverfolgt, wenn ein Winsock-Netzwerk Vorgang einen Socket schließt. Der Kanal für dieses Ereignis ist Winsock-AFD. Die Ebene für dieses Ereignis dient nur zu Informationszwecken.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Kontrolle über die Winsock-Ablauf Verfolgung](control-of-winsock-tracing.md)
</dt> <dt>

[**Ereignis \_ Deskriptor**](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor)
</dt> <dt>

[Winsock-Ablauf Verfolgung](winsock-tracing.md)
</dt> <dt>

[Winsock-Ablauf Verfolgungs Ebenen](winsock-tracing-levels.md)
</dt> <dt>

[Details zur Änderung der Winsock-Katalog Änderung](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 


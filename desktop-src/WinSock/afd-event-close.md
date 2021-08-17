---
description: Winsock-Netzwerkablaufverfolgungsereignis für socket- Close-Vorgang.
ms.assetid: C59B2B51-288A-46C9-B390-26A18DB0C2FB
title: AFD_EVENT_CLOSE-Ereignis
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
ms.openlocfilehash: 9068809c052638e33d45a5affadc23a289fa65ae04e6b1a71af1e40e4b508b15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993750"
---
# <a name="afd_event_close-event"></a>AFD \_ EVENT \_ CLOSE-Ereignis

Das **AFD \_ EVENT \_ CLOSE-Ereignis** ist ein Winsock-Netzwerkablaufverfolgungsereignis für den Vorgang zum Schließen des Sockets.


```C++
const EVENT_DESCRIPTOR AFD_EVENT_CLOSE = {0x3e9, 0x0, 0x10, 0x4, 0xf, 0x3e9, 0x8000000000000004};
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*EnterExit* 
</dt> <dd>

Informationen zu diesem Ereignis.

In der folgenden Tabelle sind die möglichen Werte für den *EnterExit-Parameter* aufgeführt:



| Wert                                                                        | Bedeutung                                                                                              |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Der Anfang einer Winsock-Anforderung.<br/>                                                           |
| <dl> <dt>1</dt> </dl> | Die Winsock-Anforderung wurde abgeschlossen.<br/>                                                            |
| <dl> <dt>2</dt> </dl> | Der Winsock AFD-Treiber hat eine interne Aktion (z. B. das Abbrechen einer Verbindung) verwendet.<br/>      |
| <dl> <dt>3</dt> </dl> | Der TCP/IP-Treiber hat dieses Ereignis verursacht. Dies weist in der Regel auf eine Datenbenachrichtigung hin.<br/> |
| <dl> <dt>4</dt> </dl> | Der Winsock AFD-Treiber hat dieses Ereignis ausgelöst (z. B. durch Festlegen einer Socketoption).<br/> |



 

</dd> <dt>

*Standort* 
</dt> <dd>

Ein intern verwendetes privates Feld.

</dd> <dt>

*Process* 
</dt> <dd>

Die [EPROCESS-Adresse](/windows-hardware/drivers/kernel/eprocess) des Prozesses, der den verknüpften Socket besitzt. Dies ist eine nicht transparente Struktur, die als Prozessobjekt für einen Prozess dient. Weitere Informationen finden Sie in der dokumentation Windows Driver Kit für die [EPROCESS-Struktur.](/windows-hardware/drivers/kernel/eprocess)

</dd> <dt>

*Endpunkt* 
</dt> <dd>

Die \_ AFD-ENDPUNKTadresse des Sockets.

</dd> <dt>

*Status* 
</dt> <dd>

Der NTSTATUS-Code für den Vorgang.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Das **AFD \_ EVENT \_ CLOSE-Ereignis** wird für einen Winsock-Netzwerkvorgang verfolgt, um einen Socket zu schließen. Der Kanal für dieses Ereignis ist Winsock-AFD. Die Ebene für dieses Ereignis ist informationell.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Steuerung der Winsock-Ablaufverfolgung](control-of-winsock-tracing.md)
</dt> <dt>

[**\_EREIGNISDESKRIPTOR**](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor)
</dt> <dt>

[Winsock-Ablaufverfolgung](winsock-tracing.md)
</dt> <dt>

[Winsock-Ablaufverfolgungsebenen](winsock-tracing-levels.md)
</dt> <dt>

[Details zur Ablaufverfolgung für Winsock-Katalogänderung](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 


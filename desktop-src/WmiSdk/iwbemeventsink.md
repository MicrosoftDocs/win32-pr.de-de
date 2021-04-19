---
description: Initiiert die Kommunikation mit einem Ereignis Anbieter unter Verwendung eines eingeschränkten Satzes von Abfragen.
ms.assetid: dd076dd0-ed39-47a2-86fb-a595baf3f464
ms.tgt_platform: multiple
title: Iwbemeventsink-Schnittstelle (wbemprov. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemEventSink
api_type:
- COM
api_location:
- Wbemsvc.dll
ms.openlocfilehash: 22a3a15920d26f482cedfa3a596fd439ea70c2f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364123"
---
# <a name="iwbemeventsink-interface"></a>Iwbemeventsink-Schnittstelle

Die **iwbemeventsink** -Schnittstelle initiiert die Kommunikation mit einem Ereignis Anbieter unter Verwendung eines eingeschränkten Satzes von Abfragen. Diese Schnittstelle erweitert [**iwbebobjectsink**](iwbemobjectsink.md)und bietet neue Methoden für Sicherheit und Leistung. Weitere Informationen zum Verwenden dieser Schnittstelle finden Sie unter [Schreiben eines Ereignis Anbieters](writing-an-event-provider.md) und [Sichern von WMI-Ereignissen](securing-wmi-events.md).

## <a name="members"></a>Member

Die **iwbemeventsink** -Schnittstelle verfügt über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iwbemeventsink** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                | BESCHREIBUNG                                                           |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------|
| [**Getrestrictedsink**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-getrestrictedsink)         | Wird vom Consumer aufgerufen, um eingeschränkte Ereignis Abfragen einzurichten.<br/> |
| [**IsActive**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-isactive)                           | Überprüft den Status der Ereignis Senke.<br/>                               |
| [**Setbatchingparameters**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setbatchingparameters) | Wird vom Consumer aufgerufen, um Batch Verarbeitungsparameter festzulegen.<br/>         |
| [**Setsink Security**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity)             | Wird verwendet, um die Sicherheits Beschreibung für eine Ereignis Senke zu aktualisieren.<br/>   |



 

## <a name="remarks"></a>Bemerkungen

Wenn Sie eine Ereignis-Abonnement-Senke ([**iwbewbjectsink**](iwbemobjectsink.md) oder **iwbemeventsink**) implementieren, sollten Sie in den Methoden des Sink-Objekts nicht WMI aufrufen. Beispielsweise kann das Aufrufen von [**IWbemServices:: cancelasynccall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) zum Abbrechen der Senke in einer Implementierung von [**iwbemeventsink:: setsink Security**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) den WMI-Status beeinträchtigen. Um ein Ereignis Abonnement abzubrechen, legen Sie ein Flag fest, und rufen Sie **IWbemServices:: cancelasynccall** von einem anderen Thread oder Objekt auf. Bei Implementierungen, die sich nicht auf eine Ereignis Senke beziehen, wie z. b. Object-, enum-und Abfrage-Abruf Werte, können Sie einen Rückruf in WMI durchlaufen.

Sink-Implementierungen sollten die Ereignis Benachrichtigung innerhalb von 100 MS verarbeiten, weil der WMI-Thread, der die Ereignis Benachrichtigung übermittelt, erst dann andere Aufgaben ausführen kann, wenn die Verarbeitung des Sink-Objekts abgeschlossen ist. Wenn für die Benachrichtigung eine große Menge an Verarbeitung erforderlich ist, kann die Senke eine interne Warteschlange für einen anderen Thread verwenden, um die Verarbeitung zu verarbeiten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                            |
| Header<br/>                   | <dl> <dt>Wbemprov. h (Include wbemittell. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Wbemuuid. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Wbemsvc.dll</dt> </dl>                    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[COM-API für WMI](com-api-for-wmi.md)
</dt> </dl>

 

 





---
description: Initiiert die Kommunikation mit einem Ereignisanbieter mithilfe eines eingeschränkten Satz von Abfragen.
ms.assetid: dd076dd0-ed39-47a2-86fb-a595baf3f464
ms.tgt_platform: multiple
title: IWbemEventSink-Schnittstelle (Wbemprov.h)
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
ms.openlocfilehash: 10c5fa56a96db3e46ce2c4c7941fd7a1d6fb27a1730dc3741890935782e4ace7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118318096"
---
# <a name="iwbemeventsink-interface"></a>IWbemEventSink-Schnittstelle

Die **IWbemEventSink-Schnittstelle** initiiert die Kommunikation mit einem Ereignisanbieter mithilfe eines eingeschränkten Satz von Abfragen. Diese Schnittstelle erweitert [**IWbemObjectSink**](iwbemobjectsink.md)und stellt neue Methoden für Sicherheit und Leistung bereit. Weitere Informationen zur Verwendung dieser Schnittstelle finden Sie unter [Schreiben eines Ereignisanbieters](writing-an-event-provider.md) und [Sichern von WMI-Ereignissen.](securing-wmi-events.md)

## <a name="members"></a>Member

Die **IWbemEventSink-Schnittstelle** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IWbemEventSink-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                | BESCHREIBUNG                                                           |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------|
| [**GetRestrictedSink**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-getrestrictedsink)         | Wird vom Consumer aufgerufen, um eingeschränkte Ereignisabfragen zu erstellen.<br/> |
| [**IsActive**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-isactive)                           | Überprüft den Status der Ereignissenke.<br/>                               |
| [**SetBatchingParameters**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setbatchingparameters) | Wird vom Consumer aufgerufen, um Batchverarbeitungsparameter festlegen.<br/>         |
| [**SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity)             | Wird verwendet, um den Sicherheitsdeskriptor für eine Ereignissenke zu aktualisieren.<br/>   |



 

## <a name="remarks"></a>Hinweise

Rufen Sie beim Implementieren einer Ereignisabonnementsenke [**(IWbemObjectSink**](iwbemobjectsink.md) oder **IWbemEventSink)** nicht aus den Methoden des Senkenobjekts in WMI auf. Wenn Sie beispielsweise [**IWbemServices::CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) aufrufen, um die Senke innerhalb einer Implementierung von [**IWbemEventSink::SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) abzubricht, kann der WMI-Zustand beeinträchtigt werden. Um ein Ereignisabonnement zu kündigen, legen Sie ein Flag fest, und rufen **Sie IWbemServices::CancelAsyncCall von** einem anderen Thread oder Objekt aus auf. Für Implementierungen, die nicht mit einer Ereignissenke verknüpft sind, z. B. Objekt-, Enum- und Abfrageabrufe, können Sie einen Rückruf in WMI ausführen.

Senkenimplementierungen sollten die Ereignisbenachrichtigung innerhalb von 100 MSEC verarbeiten, da der WMI-Thread, der die Ereignisbenachrichtigung übergibt, keine anderen Arbeiten mehr tun kann, bis die Verarbeitung des Senkenobjekts abgeschlossen ist. Wenn die Benachrichtigung eine große Menge an Verarbeitung erfordert, kann die Senke eine interne Warteschlange für einen anderen Thread verwenden, um die Verarbeitung zu verarbeiten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                            |
| Header<br/>                   | <dl> <dt>Wbemprov.h (einschließlich Wbemidl.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Wbemuuid.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Wbemsvc.dll</dt> </dl>                    |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[COM-API für WMI](com-api-for-wmi.md)
</dt> </dl>

 

 





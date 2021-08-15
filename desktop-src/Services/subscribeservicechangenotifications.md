---
description: Abonniert Dienststatusänderungsbenachrichtigungen mithilfe einer Rückruffunktion.
ms.assetid: d67113eb-2141-444c-9f09-eaa772bcad8a
title: SubscribeServiceChangeNotifications-Funktion (Winsvcp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SubscribeServiceChangeNotifications
api_type:
- DllExport
api_location:
- SecHost.dll
- API-MS-Win-Service-Private-L1-1-0.dll
- API-MS-Win-Service-Private-L1-1-1.dll
- Advapi32.dll
- API-MS-Win-Service-Private-L1-1-2.dll
ms.openlocfilehash: 83bd7bc3f937794f14cbe1d2877bc53ce7d347a8f45fd4f0ddb3e9d0ee9a52a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888456"
---
# <a name="subscribeservicechangenotifications-function"></a>SubscribeServiceChangeNotifications-Funktion

Abonniert Dienststatusänderungsbenachrichtigungen mithilfe einer Rückruffunktion.

## <a name="syntax"></a>Syntax


```C++
DWORD WINAPI SubscribeServiceChangeNotifications(
  _In_     SC_HANDLE                     hService,
  _In_     SC_EVENT_TYPE                 eEventType,
  _In_     PSC_NOTIFICATION_CALLBACK     pCallback,
  _In_opt_ PVOID                         pCallbackContext,
  _Out_    PSC_NOTIFICATION_REGISTRATION *pSubscription
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hService* \[ In\]
</dt> <dd>

Ein Handle für den Dienst oder ein Handle für den Dienststeuerungs-Manager (Service Control Manager, SCM), um Änderungen zu überwachen.

Handles für Dienste werden von der [**OpenService-**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) und [**CreateService-Funktion**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) zurückgegeben und müssen über das Zugriffsrecht **SERVICE QUERY \_ \_ STATUS** verfügen. Handles für den Dienststeuerungs-Manager werden von der [**OpenSCManager-Funktion**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) zurückgegeben und müssen über das **SC \_ \_ MANAGER-ENUMERATE \_ SERVICE-Zugriffsrecht** verfügen.

</dd> <dt>

*eEventType* \[ In\]
</dt> <dd>

Gibt den Typ der Statusänderungen an, die gemeldet werden sollen. Dieser Parameter wird auf einen der in [**SC \_ EVENT \_ TYPE**](sc-event-type.md)angegebenen Werte festgelegt. Das Verhalten für diese Funktion unterscheidet sich je nach Ereignistyp wie folgt.



| Wert                                                                                                                                                                                                                                                   | Bedeutung                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span id="SC_EVENT_DATABASE_CHANGE"></span><span id="sc_event_database_change"></span><dl> <dt>**SC \_ EVENT \_ DATABASE \_ CHANGE**</dt> <dt>0</dt> </dl> | Ein Dienst wurde hinzugefügt oder gelöscht. Der *hService-Parameter* muss ein Handle für den SCM sein.<br/>                  |
| <span id="SC_EVENT_PROPERTY_CHANGE"></span><span id="sc_event_property_change"></span><dl> <dt>**SC \_ \_ \_ EREIGNISEIGENSCHAFTSÄNDERUNG**</dt> <dt>1</dt> </dl> | Mindestens eine Diensteigenschaft wurde aktualisiert. Der *hService-Parameter* muss ein Handle für den Dienst sein.<br/> |
| <span id="SC_EVENT_STATUS_CHANGE"></span><span id="sc_event_status_change"></span><dl> <dt>**SC \_ \_ \_ EREIGNISSTATUSÄNDERUNG**</dt> <dt>2</dt> </dl>       | Der Status eines Diensts wurde geändert. Der *hService-Parameter* muss ein Handle für den Dienst sein.<br/>              |



 

</dd> <dt>

*pCallback* \[ In\]
</dt> <dd>

Gibt die Rückruffunktion an. Der Rückruf muss so definiert werden, dass er den Typ **SC \_ NOTIFICATION \_ CALLBACK aufweist.** Weitere Informationen finden Sie in den Hinweisen.

</dd> <dt>

*pCallbackContext* \[ in, optional\]
</dt> <dd>

Ein Zeiger, der den Kontext für diesen Benachrichtigungsrückruf darstellt.

</dd> <dt>

*pSubscription* \[ out\]
</dt> <dd>

Gibt einen Zeiger auf das Abonnement zurück, das sich aus der Registrierung des Benachrichtigungsrückrufs ergibt. Der Aufrufer ist dafür verantwortlich, [**UnsubscribeServiceChangeNotifications**](unsubscribeservicechangenotifications.md) aufzurufen, um den Empfang von Benachrichtigungen zu beenden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert **ERROR \_ SUCCESS**.

Wenn die Funktion fehlschlägt, ist der Rückgabewert einer der [Systemfehlercodes.](/windows/desktop/Debug/system-error-codes)

## <a name="remarks"></a>Hinweise

Die Rückruffunktion wird wie folgt deklariert:


```C++
typedef VOID CALLBACK SC_NOTIFICATION_CALLBACK(
    _In_    DWORD                   dwNotify,
    _In_    PVOID                   pCallbackContext
);
typedef SC_NOTIFICATION_CALLBACK* PSC_NOTIFICATION_CALLBACK;
```



Die Rückruffunktion empfängt einen Zeiger auf den vom Aufrufer bereitgestellten Kontext. Der Rückruf wird als Ergebnis des Dienststatusänderungsereignisses aufgerufen. Wenn der Rückruf aufgerufen wird, wird er mit einer Bitmaske von **SERVICE \_ NOTIFY \_ *XXX***-Werten bereitgestellt, die den Typ der Änderung des Dienststatus angeben. Wenn der Rückruf mit 0 (null) anstelle eines gültigen **SERVICE \_ NOTIFY \_ *XXX*-Werts** bereitgestellt wird, muss die Anwendung überprüfen, was geändert wurde.

Die Rückruffunktion darf die Ausführung nicht blockieren. Wenn Sie erwarten, dass die Ausführung der Rückruffunktion eine Zeit in Anspruch nimmt, sollten Sie die in der Rückruffunktion ausgeführte Arbeit in einen separaten Thread auslagern, indem Sie ein Arbeitselement einem Thread in einem Threadpool in die Warteschlange stellen. Einige Arten von Aufgaben, die die Rückruffunktion in Anspruch nehmen können, umfassen das Ausführen von Datei-E/A, das Warten auf ein Ereignis und das Ausführen externer Remoteprozeduraufrufe.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Winsvcp.h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>SecHost.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)
</dt> <dt>

[**Openservice**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea)
</dt> <dt>

[**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera)
</dt> <dt>

[**UnsubscribeServiceChangeNotifications**](unsubscribeservicechangenotifications.md)
</dt> <dt>

[**QueryServiceDynamicInformation**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicedynamicinformation)
</dt> </dl>

 


---
description: Abonniert Dienststatus-Änderungs Benachrichtigungen mithilfe einer Rückruffunktion.
ms.assetid: d67113eb-2141-444c-9f09-eaa772bcad8a
title: Abonneanservicechangenotifications-Funktion (winsvcp. h)
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
ms.openlocfilehash: e327a44d613b514123862b1ddcb1bf302fea63ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349599"
---
# <a name="subscribeservicechangenotifications-function"></a>Abonniert Service changenotifications-Funktion

Abonniert Dienststatus-Änderungs Benachrichtigungen mithilfe einer Rückruffunktion.

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

*hservice* \[ in\]
</dt> <dd>

Ein Handle für den Dienst oder ein Handle für den Dienststeuerungs-Manager (SCM), der auf Änderungen überwacht werden soll.

Handles für Dienste werden von der [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) -Funktion und der-Funktion für die Funktion [**"-Funktion**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) " zurückgegeben und müssen über das Zugriffsrecht für **Dienst \_ Abfragen \_** verfügen. Handles für den Dienststeuerungs-Manager werden von der [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) -Funktion zurückgegeben und müssen das **SC- \_ Manager- \_ \_ Dienst** Zugriffsrecht auflisten.

</dd> <dt>

*eeventtype* \[ in\]
</dt> <dd>

Gibt den Typ der Statusänderungen an, die gemeldet werden sollen. Dieser Parameter wird auf einen der Werte festgelegt, die im [**SC- \_ \_ Ereignistyp**](sc-event-type.md)angegeben sind. Das Verhalten dieser Funktion ist abhängig vom Ereignistyp wie folgt unterschiedlich.



| Wert                                                                                                                                                                                                                                                   | Bedeutung                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span id="SC_EVENT_DATABASE_CHANGE"></span><span id="sc_event_database_change"></span><dl> <dt>**SC \_ \_ \_ Änderung der Ereignis Datenbank**</dt> <dt>0</dt> </dl> | Es wurde ein Dienst hinzugefügt oder gelöscht. Der *hservice* -Parameter muss ein Handle für den SCM sein.<br/>                  |
| <span id="SC_EVENT_PROPERTY_CHANGE"></span><span id="sc_event_property_change"></span><dl> <dt>**SC \_ \_ \_ Änderung der Ereignis Eigenschaft**</dt> <dt>1</dt> </dl> | Mindestens eine Dienst Eigenschaft wurde aktualisiert. Der *hservice* -Parameter muss ein Handle für den Dienst sein.<br/> |
| <span id="SC_EVENT_STATUS_CHANGE"></span><span id="sc_event_status_change"></span><dl> <dt>**SC \_ Ereignis \_ Status \_ Änderung**</dt> <dt>2</dt> </dl>       | Der Status eines Dienstanbieter hat sich geändert. Der *hservice* -Parameter muss ein Handle für den Dienst sein.<br/>              |



 

</dd> <dt>

*pCallback* \[ in\]
</dt> <dd>

Gibt die Rückruffunktion an. Der Rückruf muss als Typ des **SC- \_ Benachrichtigungs \_ Rückrufs** definiert werden. Weitere Informationen finden Sie in den Hinweisen.

</dd> <dt>

*pcallbackcontext* \[ in, optional\]
</dt> <dd>

Ein Zeiger, der den Kontext für diesen Benachrichtigungs Rückruf darstellt.

</dd> <dt>

*pabonnement* \[ vorgenommen\]
</dt> <dd>

Gibt einen Zeiger auf das Abonnement zurück, das sich aus der Benachrichtigungs Rückruf Registrierung ergibt. Der Aufrufer ist für das Aufrufen von [**nicht abonniert beservicechangenotifications**](unsubscribeservicechangenotifications.md) verantwortlich, um den Empfang von Benachrichtigungen zu verhindern

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert **Fehler \_ erfolgreich**.

Wenn die Funktion fehlschlägt, ist der Rückgabewert einer der [Systemfehler Codes](/windows/desktop/Debug/system-error-codes).

## <a name="remarks"></a>Bemerkungen

Die Rückruffunktion wird wie folgt deklariert:


```C++
typedef VOID CALLBACK SC_NOTIFICATION_CALLBACK(
    _In_    DWORD                   dwNotify,
    _In_    PVOID                   pCallbackContext
);
typedef SC_NOTIFICATION_CALLBACK* PSC_NOTIFICATION_CALLBACK;
```



Die Rückruffunktion empfängt einen Zeiger auf den vom Aufrufer bereitgestellten Kontext. Der Rückruf wird als Ergebnis des Dienststatus-Änderungs Ereignisses aufgerufen. Wenn der Rückruf aufgerufen wird, wird er mit einer Bitmaske von **Dienst \_ Benachrichtigen \_ * xxx***-Werten bereitgestellt, die den Typ der Änderung des Dienststatus angeben. Wenn der Rückruf anstelle eines gültigen **\_ diensbenachrichtigungs- \_ * xxx***-Werts mit 0 (null) bereitgestellt wird, muss die Anwendung überprüfen, was geändert wurde.

Die Rückruffunktion darf die Ausführung nicht blockieren. Wenn Sie davon ausgehen, dass die Ausführung der Rückruffunktion Zeit in Anspruch nimmt, sollten Sie die in der Rückruffunktion durchzuführenden Aufgaben in einen separaten Thread auslagern, indem Sie eine Arbeitsaufgabe an einen Thread in einem Thread Pool in die Warteschlange eingereiht. Einige Arten von Aufgaben, die die Rückruffunktion in Anspruch nehmen können, sind u. a. das Ausführen von Datei-e/a, das warten auf ein Ereignis und das Ausführen externer Remote Prozedur Aufrufe.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Winsvcp. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>SecHost.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)
</dt> <dt>

[**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea)
</dt> <dt>

[**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera)
</dt> <dt>

[**Nicht abonniert beservicechangenotifications**](unsubscribeservicechangenotifications.md)
</dt> <dt>

[**Queryservicedynamicinformation**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicedynamicinformation)
</dt> </dl>

 


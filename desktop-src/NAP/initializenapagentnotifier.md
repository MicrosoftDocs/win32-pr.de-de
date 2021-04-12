---
title: Initializenapagentnotifier-Funktion (naputil. h)
description: Abonniert den aufrufenden Prozess zum Anzeigen von NAPAgent-Status Änderungs Benachrichtigungen und zum Quarantäne Status Änderungs Benachrichtigungen.
ms.assetid: 24180194-50d7-4f54-845d-25402af9cf9a
keywords:
- Initializenapagentnotifier-Funktion NAP
topic_type:
- apiref
api_name:
- InitializeNapAgentNotifier
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f59c4c342f693038040f374bbdbcdb8ab226f74d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949661"
---
# <a name="initializenapagentnotifier-function"></a>Initializenapagentnotifier-Funktion

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **initializenapagentnotifier** -Funktion abonniert den aufrufenden Prozess zum Anzeigen von NAPAgent-Status Änderungs Benachrichtigungen und zum Quarantäne Status Änderungs Benachrichtigungen. Diese Benachrichtigungen werden vom NAPAgent-Dienst bereitgestellt.

## <a name="syntax"></a>Syntax


```C++
NAPAPI HRESULT WINAPI InitializeNapAgentNotifier(
  _In_ NapNotifyType type,
  _In_ HANDLE        hNotifyEvent
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Typ* \[ in\]
</dt> <dd>

Ein [**napnotifytype**](/windows/win32/api/naptypes/ne-naptypes-napnotifytype) -Wert, der den Typ der zu empfangenden Dienst Benachrichtigungen angibt.

</dd> <dt>

*hnotischyevent* \[ in\]
</dt> <dd>

Ein Ereignis handle, das für die Benachrichtigung verwendet wird. Der Aufrufer muss ein geöffnetes Handle an den *hnotifyevent* -Parameter übergeben. Der Aufrufer muss auch das Ereignis handle schließen, wenn es nicht mehr benötigt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert



| Rückgabecode                                                                                                | Beschreibung                                                                                               |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Die Initialisierung wurde erfolgreich abgeschlossen.<br/>                                                         |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>                     | Fehler bei der Initialisierung.<br/>                                                                         |
| <dl> <dt>**Fehler \_ bereits \_ Initialisiert**</dt> </dl> | Der Prozess hat die NAPAgent-Dienst Benachrichtigungen vom angegebenen *Typ* bereits abonniert. <br/> |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>               | Ein ungültiges Argument wurde übergeben. <br/>                                                               |



 

## <a name="remarks"></a>Bemerkungen

Diese Funktion ist nicht threadsicher.

Bei jedem Prozess, bei dem ein Abonnement für die NAPAgent-Dienst Benachrichtigungen vom angegebenen *Typ* erforderlich ist, muss **initializenapagentnotifier** aufgerufen werden, um Benachrichtigungen zu abonnieren. Wenn ein Prozess mehr als einen Benachrichtigungstyp abonnieren muss, muss er für jeden Benachrichtigungstyp einmal **initializenapagentnotifier** aufruft.

Wenn ein Prozess keine weiteren Benachrichtigungen erfordert, muss der Prozess [**uninitializenapagentnotifier**](uninitializenapagentnotifier.md) für den angegebenen *Typ* aufzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Naputil. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Uninitializenapagentnotifier**](uninitializenapagentnotifier.md)
</dt> </dl>

 

 






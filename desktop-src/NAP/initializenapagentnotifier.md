---
title: InitializeNapAgentNotifier-Funktion (NapUtil.h)
description: Abonniert den aufrufenden Prozess für NapAgent-Zustandsänderungsbenachrichtigungen und Quarantänezustandsänderungsbenachrichtigungen.
ms.assetid: 24180194-50d7-4f54-845d-25402af9cf9a
keywords:
- InitializeNapAgentNotifier-Funktion NAP
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
ms.openlocfilehash: 1ac2d874f6138bcc1fbc97952d4464e56e05b0a497c7b0ff98e9c05e8c8434e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133455"
---
# <a name="initializenapagentnotifier-function"></a>InitializeNapAgentNotifier-Funktion

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Die **InitializeNapAgentNotifier-Funktion** abonniert den aufrufenden Prozess für NapAgent-Zustandsänderungsbenachrichtigungen und Quarantänestatusänderungsbenachrichtigungen. Diese Benachrichtigungen werden vom NapAgent-Dienst bereitgestellt.

## <a name="syntax"></a>Syntax


```C++
NAPAPI HRESULT WINAPI InitializeNapAgentNotifier(
  _In_ NapNotifyType type,
  _In_ HANDLE        hNotifyEvent
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*type* \[ In\]
</dt> <dd>

Ein [**NapNotifyType-Wert,**](/windows/win32/api/naptypes/ne-naptypes-napnotifytype) der den Typ der zu empfangenden Dienstbenachrichtigungen angibt.

</dd> <dt>

*hNotifyEvent* \[ In\]
</dt> <dd>

Ein Ereignishand handle, das für die Benachrichtigung verwendet wird. Der Aufrufer muss ein offenes Handle an den *hNotifyEvent-Parameter* übergeben. Der Aufrufer muss auch das Ereignishand handle schließen, wenn es nicht mehr benötigt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert



| Rückgabecode                                                                                                | Beschreibung                                                                                               |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Die Initialisierung wurde erfolgreich abgeschlossen.<br/>                                                         |
| <dl> <dt>**E \_ FAIL**</dt> </dl>                     | Fehler bei der Initialisierung.<br/>                                                                         |
| <dl> <dt>**FEHLER \_ BEREITS \_ INITIALISIERT**</dt> </dl> | Der Prozess hat bereits NapAgent-Dienstbenachrichtigungen des angegebenen *Typs abonniert.* <br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>               | Ein ungültiges Argument wurde übergeben. <br/>                                                               |



 

## <a name="remarks"></a>Hinweise

Diese Funktion ist nicht threadsicher.

Jeder Prozess, der ein Abonnement für NapAgent-Dienstbenachrichtigungen des angegebenen Typs erfordert, muss **InitializeNapAgentNotifier** aufrufen, um Benachrichtigungen zu abonnieren.  Wenn ein Prozess mehrere Benachrichtigungstypen abonnieren muss, muss er **InitializeNapAgentNotifier** einmal für jeden Benachrichtigungstyp aufrufen.

Sobald ein Prozess keine weiteren Benachrichtigungen erfordert, muss der Prozess [**UninitializeNapAgentNotifier**](uninitializenapagentnotifier.md) für den angegebenen Typ *aufrufen.*

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>NapUtil.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**UninitializeNapAgentNotifier**](uninitializenapagentnotifier.md)
</dt> </dl>

 

 






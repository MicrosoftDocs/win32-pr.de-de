---
description: Abonniert die Dienststatus-Änderungs Benachrichtigungen.
ms.assetid: 8c04ebf7-4d61-4617-b120-dbe26b2f9ad2
title: Unabonneatchangenotifications-Funktion (winsvcp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UnsubscribeServiceChangeNotifications
api_type:
- DllExport
api_location:
- SecHost.dll
- API-MS-Win-Service-Private-L1-1-0.dll
- API-MS-Win-Service-Private-L1-1-1.dll
- Advapi32.dll
- API-MS-Win-Service-Private-L1-1-2.dll
ms.openlocfilehash: ebecfb133172c9c7a56ed6d28f7ad6b395d8afce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866627"
---
# <a name="unsubscribeservicechangenotifications-function"></a>Unabonneanservicechangenotifications-Funktion

Abonniert die Dienststatus-Änderungs Benachrichtigungen. Diese Funktion verwendet Abonnements, die von [**abonbeservicechangenotifications**](subscribeservicechangenotifications.md)zurückgegeben werden.

## <a name="syntax"></a>Syntax


```C++
 VOID WINAPI UnsubscribeServiceChangeNotifications(
  _In_ PSC_NOTIFICATION_REGISTRATION pSubscription
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pabonnement* \[ in\]
</dt> <dd>

Ein Zeiger auf das Abonnement, das abonniert werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Nicht **abonniert beservicechangenotifications** gibt erst zurück, wenn ausstehende Prozess interne Rückrufe beendet sind. Daher ist es nicht möglich, nicht **abonniert beservicechangenotifications** innerhalb des Rückrufs aufzurufen, ohne einen Deadlock zu verursachen.

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

[**Abonniert-servicechangenotifications**](subscribeservicechangenotifications.md)
</dt> <dt>

[**Queryservicedynamicinformation**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicedynamicinformation)
</dt> </dl>

 

 





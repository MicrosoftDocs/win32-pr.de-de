---
description: Kündigen von Dienststatusänderungsbenachrichtigungen.
ms.assetid: 8c04ebf7-4d61-4617-b120-dbe26b2f9ad2
title: UnsubscribeServiceChangeNotifications-Funktion (Winsvcp.h)
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
ms.openlocfilehash: 3e37f2b786d32ab9f42738e6a8522c6f4593aa6b21a490a6fdd969233b4a6dff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888169"
---
# <a name="unsubscribeservicechangenotifications-function"></a>UnsubscribeServiceChangeNotifications-Funktion

Kündigen von Dienststatusänderungsbenachrichtigungen. Diese Funktion verwendet Abonnements, die von [**SubscribeServiceChangeNotifications zurückgegeben werden.**](subscribeservicechangenotifications.md)

## <a name="syntax"></a>Syntax


```C++
 VOID WINAPI UnsubscribeServiceChangeNotifications(
  _In_ PSC_NOTIFICATION_REGISTRATION pSubscription
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSubscription* \[ In\]
</dt> <dd>

Ein Zeiger auf das Abonnement, für das das Abonnement gekündigt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

**UnsubscribeServiceChangeNotifications gibt** erst dann zurück, wenn ausstehende In-Process-Rückrufe abgeschlossen sind. Daher können Sie **UnsubscribeServiceChangeNotifications** nicht innerhalb des Rückrufs aufrufen, ohne einen Deadlock zu verursachen.

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

[**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md)
</dt> <dt>

[**QueryServiceDynamicInformation**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicedynamicinformation)
</dt> </dl>

 

 





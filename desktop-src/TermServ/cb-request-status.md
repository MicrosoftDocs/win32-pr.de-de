---
title: CB_REQUEST_STATUS-Enumeration (Cbclient.h)
description: Gibt den Status einer asynchronen Anforderung an.
ms.assetid: 35FAC8EA-BA17-405F-AE10-33A816029F62
ms.tgt_platform: multiple
keywords:
- CB_REQUEST_STATUS Enumerations-Remotedesktopdienste
topic_type:
- apiref
api_name:
- CB_REQUEST_STATUS
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6647f10ab91fd5cb1919d49c4c00d22b8b1722de9b20d9b83fdee8fcceaef95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871970"
---
# <a name="cb_request_status-enumeration"></a>CB \_ REQUEST \_ STATUS-Enumeration

Gibt den Status einer asynchronen Anforderung an. Diese Enumeration wird mit der [**IConnectionBrokerRequest::CheckStatus-Methode**](iconnectionbrokerrequest-checkstatus.md) verwendet.

## <a name="syntax"></a>Syntax


```C++
typedef enum _CB_REQUEST_STATUS { 
  CB_STATUS_INVALID                     = 1,
  CB_STATUS_INITIATING_REQUEST          = 0,
  CB_STATUS_REQUEST_COMPLETED,
  CB_STATUS_REQUEST_FAILED,
  CB_STATUS_REQUEST_ABORTED,
  CB_STATUS_FINDING_DESTINATION,
  CB_STATUS_LOADING_DESTINATION,
  CB_STATUS_BRINGING_SESSION_ONLINE,
  CB_STATUS_REDIRECTING_TO_DESTINATION
} CB_REQUEST_STATUS;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="CB_STATUS_INVALID"></span><span id="cb_status_invalid"></span>**\_CB-STATUS \_ UNGÜLTIG**
</dt> <dd>

Das Anforderungsobjekt wird nicht initialisiert.

</dd> <dt>

<span id="CB_STATUS_INITIATING_REQUEST"></span><span id="cb_status_initiating_request"></span>**\_CB-STATUS: \_ INITIIERENDE \_ ANFORDERUNG**
</dt> <dd>

Wird nicht verwendet.

</dd> <dt>

<span id="CB_STATUS_REQUEST_COMPLETED"></span><span id="cb_status_request_completed"></span>**\_CB-STATUSANFORDERUNG \_ \_ ABGESCHLOSSEN**
</dt> <dd>

Die Anforderung ist abgeschlossen.

</dd> <dt>

<span id="CB_STATUS_REQUEST_FAILED"></span><span id="cb_status_request_failed"></span>**\_FEHLER BEI CB-STATUSANFORDERUNG \_ \_**
</dt> <dd>

Fehler bei der Anforderung.

</dd> <dt>

<span id="CB_STATUS_REQUEST_ABORTED"></span><span id="cb_status_request_aborted"></span>**\_CB-STATUSANFORDERUNG \_ \_ ABGEBROCHEN**
</dt> <dd>

Die Anforderung wurde abgebrochen.

</dd> <dt>

<span id="CB_STATUS_FINDING_DESTINATION"></span><span id="cb_status_finding_destination"></span>**CB \_ STATUS \_ FINDING \_ DESTINATION**
</dt> <dd>

Wird nicht verwendet.

</dd> <dt>

<span id="CB_STATUS_LOADING_DESTINATION"></span><span id="cb_status_loading_destination"></span>**ZIEL FÜR \_ DAS LADEN DES CB-STATUS \_ \_**
</dt> <dd>

Wird nicht verwendet.

</dd> <dt>

<span id="CB_STATUS_BRINGING_SESSION_ONLINE"></span><span id="cb_status_bringing_session_online"></span>**\_CB-STATUS: \_ SITZUNG ONLINE \_ \_ GESCHALTET**
</dt> <dd>

Wird nicht verwendet.

</dd> <dt>

<span id="CB_STATUS_REDIRECTING_TO_DESTINATION"></span><span id="cb_status_redirecting_to_destination"></span>**\_ \_ CB-STATUSUMLEITUNG \_ ZUM \_ ZIEL**
</dt> <dd>

Wird nicht verwendet.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                        |
| Header<br/>                   | <dl> <dt>Cbclient.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IConnectionBrokerRequest::CheckStatus**](iconnectionbrokerrequest-checkstatus.md)
</dt> </dl>

 

 






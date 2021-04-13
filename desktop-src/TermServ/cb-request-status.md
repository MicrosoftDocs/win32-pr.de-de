---
title: CB_REQUEST_STATUS-Enumeration (cbclient. h)
description: Gibt den Status einer asynchronen Anforderung an.
ms.assetid: 35FAC8EA-BA17-405F-AE10-33A816029F62
ms.tgt_platform: multiple
keywords:
- CB_REQUEST_STATUS Enumeration Remotedesktopdienste
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
ms.openlocfilehash: cd57efd12d3fb5c708d5c4861ee144543bb49f6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340537"
---
# <a name="cb_request_status-enumeration"></a>CB- \_ Anforderungs \_ Status-Enumeration

Gibt den Status einer asynchronen Anforderung an. Diese Enumeration wird mit der [**iconnectionbrokerrequest:: CheckStatus**](iconnectionbrokerrequest-checkstatus.md) -Methode verwendet.

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

<span id="CB_STATUS_INVALID"></span><span id="cb_status_invalid"></span>**CB- \_ Status \_ ungültig**
</dt> <dd>

Das Anforderungs Objekt ist nicht initialisiert.

</dd> <dt>

<span id="CB_STATUS_INITIATING_REQUEST"></span><span id="cb_status_initiating_request"></span>**CB- \_ Status \_ Initiierungs \_ Anforderung**
</dt> <dd>

Nicht verwendet.

</dd> <dt>

<span id="CB_STATUS_REQUEST_COMPLETED"></span><span id="cb_status_request_completed"></span>**CB- \_ Status \_ Anforderung \_ abgeschlossen**
</dt> <dd>

Die Anforderung ist fertiggestellt.

</dd> <dt>

<span id="CB_STATUS_REQUEST_FAILED"></span><span id="cb_status_request_failed"></span>**Fehler bei der CB- \_ Status \_ Anforderung \_**
</dt> <dd>

Fehler bei der Anforderung.

</dd> <dt>

<span id="CB_STATUS_REQUEST_ABORTED"></span><span id="cb_status_request_aborted"></span>**CB- \_ Status \_ Anforderung \_ abgebrochen**
</dt> <dd>

Die Anforderung wurde abgebrochen.

</dd> <dt>

<span id="CB_STATUS_FINDING_DESTINATION"></span><span id="cb_status_finding_destination"></span>**CB \_ - \_ Status \_ Suchziel**
</dt> <dd>

Nicht verwendet.

</dd> <dt>

<span id="CB_STATUS_LOADING_DESTINATION"></span><span id="cb_status_loading_destination"></span>**CB- \_ Status \_ Lade \_ Ziel**
</dt> <dd>

Nicht verwendet.

</dd> <dt>

<span id="CB_STATUS_BRINGING_SESSION_ONLINE"></span><span id="cb_status_bringing_session_online"></span>**CB \_ -Status der \_ \_ Sitzung \_ Online**
</dt> <dd>

Nicht verwendet.

</dd> <dt>

<span id="CB_STATUS_REDIRECTING_TO_DESTINATION"></span><span id="cb_status_redirecting_to_destination"></span>**CB- \_ Status Umleitung \_ \_ zum \_ Ziel**
</dt> <dd>

Nicht verwendet.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                        |
| Header<br/>                   | <dl> <dt>Cbclient. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iconnectionbrokerrequest:: CheckStatus**](iconnectionbrokerrequest-checkstatus.md)
</dt> </dl>

 

 






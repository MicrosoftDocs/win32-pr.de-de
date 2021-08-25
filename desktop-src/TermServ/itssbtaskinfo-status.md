---
title: ITsSbTaskInfo-Statuseigenschaft
description: Ruft einen RDV \_ TASK \_ STATUS-Enumerationswert ab, der den Zustand der Aufgabe darstellt.
ms.assetid: 779af127-133c-47ff-8fca-bfd2c96c9768
ms.tgt_platform: multiple
keywords:
- Statuseigenschaft Remotedesktopdienste
- Status-Eigenschaft Remotedesktopdienste , ITsSbTaskInfo-Schnittstelle
- ITsSbTaskInfo-Schnittstelle Remotedesktopdienste , Status-Eigenschaft
topic_type:
- apiref
api_name:
- ITsSbTaskInfo.Status
- ITsSbTaskInfo.get_Status
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d497bd46d1adfca88cce3a4b5c58cf72619ef1c38a03823ff26a14f2e6dfebd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009240"
---
# <a name="itssbtaskinfostatus-property"></a>ITsSbTaskInfo::Status-Eigenschaft

Ruft einen [**RDV \_ TASK \_ STATUS-Enumerationswert**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) ab, der den Zustand der Aufgabe darstellt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Status(
  [out, retval] RDV_TASK_STATUS *pStatus
);
```



## <a name="property-value"></a>Eigenschaftswert

Ein [**RDV \_ TASK STATUS-Enumerationswert, \_**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) der den Zustand des Tasks darstellt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                       |
| Idl<br/>                      | <dl> <dt>Sbtsv.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ITsSbTaskInfo**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> </dl>

 

 






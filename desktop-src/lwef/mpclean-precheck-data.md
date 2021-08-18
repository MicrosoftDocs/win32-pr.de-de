---
title: MPCLEAN_PRECHECK_DATA -Struktur (MpClient.h)
description: Benachrichtigungsdaten, die an eine bereinigte Precheck-Rückruffunktion übergeben werden.
ms.assetid: 65B3B116-6E83-46F5-AE2B-92A41AE39480
keywords:
- MPCLEAN_PRECHECK_DATA struktur Legacy Windows Umgebungsfeatures
- PMPCLEAN_PRECHECK_DATA strukturzeiger Legacy-Windows-Umgebungsfeatures
topic_type:
- apiref
api_name:
- MPCLEAN_PRECHECK_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc272ed230a67811497f0eebb99624d74369c8c55419fba970f326fba502e8b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747926"
---
# <a name="mpclean_precheck_data-structure"></a>MPCLEAN \_ PRECHECK \_ DATA-Struktur

Benachrichtigungsdaten, die an eine bereinigte Precheck-Rückruffunktion übergeben werden.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMPCLEAN_PRECHECK_DATA {
  PMPRESOURCE_INFO     BlockedResourceInfo;
  BlockingResourceInfo PMPRESOURCE_INFO;
} MPCLEAN_PRECHECK_DATA, *PMPCLEAN_PRECHECK_DATA;
```



## <a name="members"></a>Member

<dl> <dt>

**BlockedResourceInfo**
</dt> <dd>

Typ: **PMPRESOURCE \_ INFO**

</dd> <dd>

Ressourceninformationen zur Ressource, die blockiert wird. Wenn der Fortschritt beispielsweise **MPNOTIFY \_ PRECHECK \_ RESOURCE BLOCKED \_ ist.** Weitere Informationen [**finden Sie unter MPRESOURCE \_ INFO**](mpresource-info.md).

</dd> <dt>

**\_PMPRESOURCE-INFORMATIONEN**
</dt> <dd>

Typ: **BlockingResourceInfo**

</dd> <dd>

Ressourceninformationen zu der Ressource, die blockiert wird. Wenn der Fortschritt beispielsweise **MPNOTIFY \_ PRECHECK \_ RESOURCE BLOCKED \_ ist.** Weitere Informationen [**finden Sie unter MPRESOURCE \_ INFO**](mpresource-info.md).

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MPRESOURCE-INFORMATIONEN \_**](mpresource-info.md)
</dt> </dl>

 

 






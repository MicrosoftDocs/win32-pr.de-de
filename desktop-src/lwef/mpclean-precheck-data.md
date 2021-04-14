---
title: MPCLEAN_PRECHECK_DATA Struktur (mpclient. h)
description: Benachrichtigungs Daten wurden an eine Clean Vorüberprüfung-Rückruffunktion übermittelt.
ms.assetid: 65B3B116-6E83-46F5-AE2B-92A41AE39480
keywords:
- MPCLEAN_PRECHECK_DATA Struktur Funktionen der Legacy-Windows-Umgebung
- PMPCLEAN_PRECHECK_DATA Struktur Zeiger Legacy-Windows-Umgebungs Features
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
ms.openlocfilehash: bc3d67e0c71c95db49b633feeb3048cc9f104b2f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476116"
---
# <a name="mpclean_precheck_data-structure"></a>Mpclean- \_ \_ Datenstruktur (Precheck)

Benachrichtigungs Daten wurden an eine Clean Vorüberprüfung-Rückruffunktion übermittelt.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMPCLEAN_PRECHECK_DATA {
  PMPRESOURCE_INFO     BlockedResourceInfo;
  BlockingResourceInfo PMPRESOURCE_INFO;
} MPCLEAN_PRECHECK_DATA, *PMPCLEAN_PRECHECK_DATA;
```



## <a name="members"></a>Member

<dl> <dt>

**Blockedresourceingefo**
</dt> <dd>

Typ: **pmpresource- \_ Informationen**

</dd> <dd>

Ressourcen Informationen über die Ressource, die blockiert wird. Wenn der Status z. b. auf **mpnotify \_ Precheck- \_ Ressource \_ blockiert** ist. Informationen finden Sie unter [**mpresource- \_ Informationen**](mpresource-info.md).

</dd> <dt>

**Informationen zu pmpresource \_**
</dt> <dd>

Typ: **blockingresourceinfo**

</dd> <dd>

Ressourcen Informationen über die Ressource, die blockiert wird. Wenn der Status z. b. auf **mpnotify \_ Precheck- \_ Ressource \_ blockiert** ist. Informationen finden Sie unter [**mpresource- \_ Informationen**](mpresource-info.md).

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Mpclient. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**mpresource- \_ Informationen**](mpresource-info.md)
</dt> </dl>

 

 






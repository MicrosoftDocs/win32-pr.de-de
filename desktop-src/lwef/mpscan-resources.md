---
title: MPSCAN_RESOURCES Struktur (mpclient. h)
description: Während eines Scanvorgangs übergebenen Ressourcen Informationen.
ms.assetid: D97712A6-547D-44CC-B55D-039A5CCE20BF
keywords:
- MPSCAN_RESOURCES Struktur Funktionen der Legacy-Windows-Umgebung
- PMPSCAN_RESOURCES Struktur Zeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPSCAN_RESOURCES
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69ee9ea259bca6bf66eb81fcd17b13d509d5a065
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957195"
---
# <a name="mpscan_resources-structure"></a>Mpscan- \_ Ressourcenstruktur

Während eines Scanvorgangs übergebenen Ressourcen Informationen.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMPSCAN_RESOURCES {
  DWORD            dwResourceCount;
  PMPRESOURCE_INFO pResourceList;
} MPSCAN_RESOURCES, *PMPSCAN_RESOURCES;
```



## <a name="members"></a>Member

<dl> <dt>

**dwresourcecount**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Anzahl der Ressourcen.

</dd> <dt>

**präsourcelist**
</dt> <dd>

Typ: **pmpresource- \_ Informationen**

</dd> <dd>

Array von Ressourcen. Informationen finden Sie unter [**mpresource- \_ Informationen**](mpresource-info.md).

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

 

 






---
title: MPSCAN_RESOURCES-Struktur (MpClient.h)
description: Ressourceninformationen, die während eines Scanvorgangs übergeben werden.
ms.assetid: D97712A6-547D-44CC-B55D-039A5CCE20BF
keywords:
- MPSCAN_RESOURCES Struktur legacy Windows Environment Features
- PMPSCAN_RESOURCES Strukturzeiger Legacy Windows Umgebungsfeatures
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
ms.openlocfilehash: dd70b442e7179d516d2e9c60b81e6c52b0f696f5719a255871e8687773bf71ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747349"
---
# <a name="mpscan_resources-structure"></a>MPSCAN \_ RESOURCES-Struktur

Ressourceninformationen, die während eines Scanvorgangs übergeben werden.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMPSCAN_RESOURCES {
  DWORD            dwResourceCount;
  PMPRESOURCE_INFO pResourceList;
} MPSCAN_RESOURCES, *PMPSCAN_RESOURCES;
```



## <a name="members"></a>Member

<dl> <dt>

**dwResourceCount**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Anzahl der Ressourcen.

</dd> <dt>

**pResourceList**
</dt> <dd>

Typ: **PMPRESOURCE \_ INFO**

</dd> <dd>

Array von Ressourcen. Weitere Informationen finden Sie unter [**MPRESOURCE \_ INFO**](mpresource-info.md).

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_MPRESOURCE-INFORMATIONEN**](mpresource-info.md)
</dt> </dl>

 

 






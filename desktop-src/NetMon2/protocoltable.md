---
description: Die protocoltable-Struktur enthält eine Liste von Protokollen.
ms.assetid: dad2b228-5916-44fe-b78e-ebc6507dc555
title: Protocoltable-Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROTOCOLTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3ad79beca7ce79611747a02704ffc05da5fc3d4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373192"
---
# <a name="protocoltable-structure"></a>Protocoltable-Struktur

Die **protocoltable** -Struktur enthält eine Liste von Protokollen.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PROTOCOLTABLE {
  DWORD     nProtocols;
  HPROTOCOL hProtocol[1];
} PROTOCOLTABLE;
```



## <a name="members"></a>Member

<dl> <dt>

**nprotokolle**
</dt> <dd>

Anzahl der aktivierten Protokolle.

</dd> <dt>

**hprotocol**
</dt> <dd>

Array von Handles für aktivierte Protokolle.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 





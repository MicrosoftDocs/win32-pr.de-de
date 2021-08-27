---
description: Die PROTOCOLTABLE-Struktur enthält eine Liste von Protokollen.
ms.assetid: dad2b228-5916-44fe-b78e-ebc6507dc555
title: PROTOCOLTABLE-Struktur (Netmon.h)
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
ms.openlocfilehash: a30d890fa5b6dcbbca1797a53722b97b2109cc9943ce07260c7f47514cfeb7b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036980"
---
# <a name="protocoltable-structure"></a>PROTOCOLTABLE-Struktur

Die **PROTOCOLTABLE-Struktur** enthält eine Liste von Protokollen.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PROTOCOLTABLE {
  DWORD     nProtocols;
  HPROTOCOL hProtocol[1];
} PROTOCOLTABLE;
```



## <a name="members"></a>Member

<dl> <dt>

**nProtocols**
</dt> <dd>

Anzahl der aktivierten Protokolle.

</dd> <dt>

**hProtocol**
</dt> <dd>

Array von Handles für aktivierte Protokolle.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 





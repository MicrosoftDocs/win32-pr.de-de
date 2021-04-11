---
description: Die Struktur "konfiguritsxpert" ordnet einen Experten seinen Konfigurationsdaten zu.
ms.assetid: 96a6650b-6d6f-495e-83bb-385d44ff015d
title: Konfigurier-Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CONFIGUREDEXPERT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3f3d40bf5d38c6b5151691a7d15bd93bef01eee5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216219"
---
# <a name="configuredexpert-structure"></a>Konfigurier-Struktur

Die Struktur " **konfiguritsxpert** " ordnet einen Experten seinen Konfigurationsdaten zu.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  HEXPERT       hExpert;
  DWORD         StartupFlags;
  PEXPERTCONFIG pConfig;
} CONFIGUREDEXPERT, *PCONFIGUREDEXPERT;
```



## <a name="members"></a>Member

<dl> <dt>

**hexpert**
</dt> <dd>

Handle für einen Experten.

</dd> <dt>

**StartupFlags**
</dt> <dd>

Startflag-Werte des Experten.

</dd> <dt>

**pConfig**
</dt> <dd>

Zeiger auf eine " [**expertenconfig**](expertconfig.md) "-Struktur.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 





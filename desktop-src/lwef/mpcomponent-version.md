---
title: MPCOMPONENT_VERSION -Struktur (MpClient.h)
description: Versions- und Aktualisierungszeit für eine einzelne Komponente.
ms.assetid: 43468230-EE13-4630-8C09-F8DF983EF748
keywords:
- MPCOMPONENT_VERSION struktur Legacy Windows Umgebungsfeatures
- PMPCOMPONENT_VERSION strukturzeiger Legacy-Windows-Umgebungsfeatures
topic_type:
- apiref
api_name:
- MPCOMPONENT_VERSION
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6092fe2f3ec7ba921b1ef3adfc9355feeeae67f2381836056f2af65b276921cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976070"
---
# <a name="mpcomponent_version-structure"></a>\_MPCOMPONENT-VERSIONSstruktur

Versions- und Aktualisierungszeit für eine einzelne Komponente.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMPCOMPONENT_VERSION {
  ULONGLONG      Version;
  ULARGE_INTEGER UpdateTime;
} MPCOMPONENT_VERSION, *PMPCOMPONENT_VERSION;
```



## <a name="members"></a>Member

<dl> <dt>

**Version**
</dt> <dd>

Typ: **ULONGLONG**

</dd> <dd>

Versionsfeld. Jedes **WORD stellt** Haupt-, Neben-, Build- und Revisionsversionen dar.

</dd> <dt>

**UpdateTime**
</dt> <dd>

Typ: **ULARGE \_ INTEGER**

</dd> <dd>

Zeitpunkt der letzten Aktualisierung der Komponente im **FILETIME-Format.**

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 






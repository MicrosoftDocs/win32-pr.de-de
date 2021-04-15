---
description: Gibt den aktuellen Status eines laufenden Experten an.
ms.assetid: 49107459-599c-4710-8935-4b2c789081de
title: Expertenstatus-Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTSTATUS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: a9e201b692bb82c78f88a35f22f2688d096f1771
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525157"
---
# <a name="expertstatus-structure"></a>Expertenstatus-Struktur

Die Struktur " **Expertenstatus** " gibt den aktuellen Status eines laufenden Experten an.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  EXPERTSTATUSENUMERATION Status;
  DWORD                   SubStatus;
  DWORD                   PercentDone;
  DWORD                   Frame;
  char                    szStatusText[EXPERTSTRINGLENGTH];
} EXPERTSTATUS, *PEXPERTSTATUS;
```



## <a name="members"></a>Member

<dl> <dt>

**Status**
</dt> <dd>

Aktueller von der [**expertstatusenumeration**](expertstatusenumeration.md) -Enumeration definierter Wert des Expertenstatus.

</dd> <dt>

**Unter Status**
</dt> <dd>

Unter Statuswert.

</dd> <dt>

**Prozentuabgeschlossen**
</dt> <dd>

Prozentualer Abschluss der Expertenanalyse von Netzwerkdaten.

</dd> <dt>

**Frame**
</dt> <dd>

Frame Nummer.

</dd> <dt>

**szStatusText**
</dt> <dd>

Text, der den Expertenstatus beschreibt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 





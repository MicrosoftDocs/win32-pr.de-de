---
description: Die Auftrags \_ Info \_ 3-Struktur wird verwendet, um einen Satz von Druckaufträgen miteinander zu verknüpfen.
ms.assetid: a110f555-dc33-450c-ae77-ea26f0f69448
title: JOB_INFO_3 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JOB_INFO_3
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: c76cbb6c019878d9c392d21caa40c604df3a5f12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218218"
---
# <a name="job_info_3-structure"></a>Auftrags \_ Info \_ 3-Struktur

Die **Auftrags \_ Info \_ 3** -Struktur wird verwendet, um einen Satz von Druckaufträgen miteinander zu verknüpfen.

## <a name="syntax"></a>Syntax


```C++
typedef struct _JOB_INFO_3 {
  DWORD JobId;
  DWORD NextJobId;
  DWORD Reserved;
} JOB_INFO_3, *PJOB_INFO_3;
```



## <a name="members"></a>Member

<dl> <dt>

**JobId**
</dt> <dd>

Der Bezeichner des Druckauftrags.

</dd> <dt>

**Nextjobid**
</dt> <dd>

Der Druckauftrags Bezeichner für den nächsten Druckauftrag in dem verknüpften Satz von Druckaufträgen.

</dd> <dt>

**Reserved**
</dt> <dd>

Dieser Wert ist für die zukünftige Verwendung reserviert. Sie müssen ihn auf 0 (null) festlegen.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druck Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumJobs**](enumjobs.md)
</dt> <dt>

[**GetJob**](getjob.md)
</dt> <dt>

[**Setjob**](setjob.md)
</dt> </dl>

 

 





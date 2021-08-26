---
description: Die JOB \_ INFO \_ 3-Struktur wird verwendet, um einen Satz von Druckaufträgen zu verknüpfen.
ms.assetid: a110f555-dc33-450c-ae77-ea26f0f69448
title: JOB_INFO_3 -Struktur (Winspool.h)
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
ms.openlocfilehash: 111b292c5f355aceefa95fb01bafc2cb9220757618d39d4b3ca29bbf77ca4570
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119948680"
---
# <a name="job_info_3-structure"></a>JOB \_ INFO \_ 3-Struktur

Die **JOB \_ INFO \_ 3-Struktur** wird verwendet, um einen Satz von Druckaufträgen zu verknüpfen.

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

**Jobid**
</dt> <dd>

Der Bezeichner des Druckauftrags.

</dd> <dt>

**NextJobId**
</dt> <dd>

Der Druckauftragsbezeichner für den nächsten Druckauftrag im verknüpften Satz von Druckaufträgen.

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
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Drucken von Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumJobs**](enumjobs.md)
</dt> <dt>

[**GetJob**](getjob.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> </dl>

 

 





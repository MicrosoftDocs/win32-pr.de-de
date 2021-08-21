---
title: BG_JOB_PRIORITY-Enumeration (Deliveryoptimization.h)
description: Die BG_JOB_PRIORITY-Enumeration definiert die konstanten Werte, die die Prioritätsebene eines Auftrags angeben.
ms.assetid: AF1F1F6D-473A-49E5-B24D-644A70DF304C
keywords:
- BG_JOB_PRIORITY-Enumeration
- BG_JOB_PRIORITY-Enumeration
topic_type:
- apiref
api_name:
- BG_JOB_PRIORITY
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ddeb3ea128f173d53c71467d4098c1b777beea48f7b1304922f7468d55fc3b89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118810949"
---
# <a name="bg_job_priority-enumeration"></a>BG_JOB_PRIORITY-Enumeration

Die **BG_JOB_PRIORITY-Enumeration** definiert die konstanten Werte, die die Prioritätsebene eines Auftrags angeben.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  BG_JOB_PRIORITY_FOREGROUND,
  BG_JOB_PRIORITY_HIGH,
  BG_JOB_PRIORITY_NORMAL,
  BG_JOB_PRIORITY_LOW
} BG_JOB_PRIORITY;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="BG_JOB_PRIORITY_FOREGROUND"></span><span id="bg_job_priority_foreground"></span>**BG_JOB_PRIORITY_FOREGROUND**
</dt> <dd>

Überträgt den Auftrag im Vordergrund. Vordergrundübertragungen konkurrieren um Netzwerkbandbreite mit anderen Anwendungen, was die Netzwerkerfahrung des Benutzers beeinträchtigen kann. Dies ist die höchste Prioritätsstufe.

</dd> <dt>

<span id="BG_JOB_PRIORITY_HIGH"></span><span id="bg_job_priority_high"></span>**BG_JOB_PRIORITY_HIGH**
</dt> <dd>

Überträgt den Auftrag im Hintergrund. Hintergrundübertragungen verwenden einen kleinen Prozentsatz der Netzwerkbandbreite.

</dd> <dt>

<span id="BG_JOB_PRIORITY_NORMAL"></span><span id="bg_job_priority_normal"></span>**BG_JOB_PRIORITY_NORMAL**
</dt> <dd>

Das DO-Verhalten ist für alle Nicht-Vordergrund-Aufgaben identisch. Weitere Informationen finden Sie in den Kommentaren in BG_JOB_PRIORITY_HIGH.

</dd> <dt>

<span id="BG_JOB_PRIORITY_LOW"></span><span id="bg_job_priority_low"></span>**BG_JOB_PRIORITY_LOW**
</dt> <dd>

Das DO-Verhalten ist für alle Nicht-Vordergrund-Aufgaben identisch. Weitere Informationen finden Sie in den Kommentaren in BG_JOB_PRIORITY_HIGH.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Mehrere Vordergrund- und Hintergrundübertragungen können gleichzeitig erfolgen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, nur Desktop-Apps der Version 1709 \[\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, nur Desktop-Apps der Version 1709 \[\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IBackgroundCopyJob::GetPriority**](ibackgroundcopyjob-getpriority.md)
</dt> <dt>

[**IBackgroundCopyJob::SetPriority**](ibackgroundcopyjob-setpriority.md)
</dt> </dl>

 

 






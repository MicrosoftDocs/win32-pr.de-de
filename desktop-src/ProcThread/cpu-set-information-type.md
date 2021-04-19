---
description: Stellt den Typ der Informationen in der System- \_ CPU- \_ Satz \_ Informationsstruktur dar.
ms.assetid: B42CB8E8-0010-4B11-AB0D-6D196DCCC90A
title: CPU_SET_INFORMATION_TYPE-Enumeration (processthreadapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPU_SET_INFORMATION_TYPE
api_type:
- HeaderDef
api_location:
- Processthreadapi.h
ms.openlocfilehash: 0283275856e8e68bf983aaeb9a7660a5a0a6bf59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106363463"
---
# <a name="cpu_set_information_type-enumeration"></a>\_ \_ \_ Datentyp-Enumeration für den CPU-Satz

Stellt den Typ der Informationen in der [**System- \_ CPU- \_ Satz \_ Informations**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information) Struktur dar.

## <a name="syntax"></a>Syntax


```C++
typedef enum _CPU_SET_INFORMATION_TYPE { 
  CpuSetInformation
} CPU_SET_INFORMATION_TYPE, *PCPU_SET_INFORMATION_TYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="CpuSetInformation"></span><span id="cpusetinformation"></span><span id="CPUSETINFORMATION"></span>**Cpusetinformation**
</dt> <dd>

Die-Struktur enthält Informationen zur CPU-Menge.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2016 \[ -Desktop-Apps\]<br/>                                                              |
| Header<br/>                   | <dl> <dt>Processthreadsapi. h (Include Windows. h)</dt> </dl> |



 

 





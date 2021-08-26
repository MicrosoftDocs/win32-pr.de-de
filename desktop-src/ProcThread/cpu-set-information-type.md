---
description: Stellt den Informationstyp in der SYSTEM \_ CPU \_ SET \_ INFORMATION-Struktur dar.
ms.assetid: B42CB8E8-0010-4B11-AB0D-6D196DCCC90A
title: CPU_SET_INFORMATION_TYPE -Enumeration (Processthreadapi.h)
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
ms.openlocfilehash: 7c932a143553c1101d6a81bac86ba54e21603eaf80ed5d2613484bff22a7e625
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101930"
---
# <a name="cpu_set_information_type-enumeration"></a>CPU \_ SET \_ INFORMATION \_ TYPE-Enumeration

Stellt den Informationstyp in der [**SYSTEM \_ CPU SET \_ \_ INFORMATION-Struktur**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information) dar.

## <a name="syntax"></a>Syntax


```C++
typedef enum _CPU_SET_INFORMATION_TYPE { 
  CpuSetInformation
} CPU_SET_INFORMATION_TYPE, *PCPU_SET_INFORMATION_TYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="CpuSetInformation"></span><span id="cpusetinformation"></span><span id="CPUSETINFORMATION"></span>**CpuSetInformation**
</dt> <dd>

Die -Struktur enthält CPU-Set-Informationen.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                                       |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2016 Nur Desktop-Apps\]<br/>                                                              |
| Header<br/>                   | <dl> <dt>Processthreadsapi.h (include Windows.h)</dt> </dl> |



 

 





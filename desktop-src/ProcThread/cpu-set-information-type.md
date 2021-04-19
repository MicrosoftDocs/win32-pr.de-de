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
# <a name="cpu_set_information_type-enumeration"></a><span data-ttu-id="1106b-103">\_ \_ \_ Datentyp-Enumeration für den CPU-Satz</span><span class="sxs-lookup"><span data-stu-id="1106b-103">CPU\_SET\_INFORMATION\_TYPE enumeration</span></span>

<span data-ttu-id="1106b-104">Stellt den Typ der Informationen in der [**System- \_ CPU- \_ Satz \_ Informations**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information) Struktur dar.</span><span class="sxs-lookup"><span data-stu-id="1106b-104">Represents the type of information in the [**SYSTEM\_CPU\_SET\_INFORMATION**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="1106b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1106b-105">Syntax</span></span>


```C++
typedef enum _CPU_SET_INFORMATION_TYPE { 
  CpuSetInformation
} CPU_SET_INFORMATION_TYPE, *PCPU_SET_INFORMATION_TYPE;
```



## <a name="constants"></a><span data-ttu-id="1106b-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="1106b-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1106b-107"><span id="CpuSetInformation"></span><span id="cpusetinformation"></span><span id="CPUSETINFORMATION"></span>**Cpusetinformation**</span><span class="sxs-lookup"><span data-stu-id="1106b-107"><span id="CpuSetInformation"></span><span id="cpusetinformation"></span><span id="CPUSETINFORMATION"></span>**CpuSetInformation**</span></span>
</dt> <dd>

<span data-ttu-id="1106b-108">Die-Struktur enthält Informationen zur CPU-Menge.</span><span class="sxs-lookup"><span data-stu-id="1106b-108">The structure contains CPU Set information.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1106b-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1106b-109">Requirements</span></span>



| <span data-ttu-id="1106b-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1106b-110">Requirement</span></span> | <span data-ttu-id="1106b-111">Wert</span><span class="sxs-lookup"><span data-stu-id="1106b-111">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1106b-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1106b-112">Minimum supported client</span></span><br/> | <span data-ttu-id="1106b-113">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1106b-113">Windows 10 \[desktop apps only\]</span></span><br/>                                                                       |
| <span data-ttu-id="1106b-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1106b-114">Minimum supported server</span></span><br/> | <span data-ttu-id="1106b-115">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1106b-115">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1106b-116">Header</span><span class="sxs-lookup"><span data-stu-id="1106b-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="1106b-117"><dt>Processthreadsapi. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1106b-117"><dt>Processthreadsapi.h (include Windows.h)</dt></span></span> </dl> |



 

 





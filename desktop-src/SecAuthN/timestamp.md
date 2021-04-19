---
description: Der timestamp-Datentyp enthält Informationen über die Gültigkeitsdauer von Sicherheits Token. Das Format des Werts des timestamp-Datentyps entspricht dem Format der FILETIME-Struktur.
ms.assetid: 0a609b32-dbd7-4905-8990-65ebabcd0668
title: Timestamp (SSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4898e85b0c11f55e5bb0dba2dbdefe2a3b6a2e4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356651"
---
# <a name="timestamp"></a><span data-ttu-id="5bcc5-104">TimeStamp</span><span class="sxs-lookup"><span data-stu-id="5bcc5-104">TimeStamp</span></span>

<span data-ttu-id="5bcc5-105">Der **timestamp** -Datentyp enthält Informationen über die Gültigkeitsdauer von Sicherheits Token.</span><span class="sxs-lookup"><span data-stu-id="5bcc5-105">The **TimeStamp** data type holds information about the time validity of security tokens.</span></span> <span data-ttu-id="5bcc5-106">Das Format des Werts des **timestamp** -Datentyps entspricht dem Format der [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="5bcc5-106">The format of the value of the **TimeStamp** data type is the same as that of the [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure.</span></span>


```C++
typedef SECURITY_INTEGER TimeStamp, *PTimeStamp;
```



## <a name="requirements"></a><span data-ttu-id="5bcc5-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5bcc5-107">Requirements</span></span>



| <span data-ttu-id="5bcc5-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5bcc5-108">Requirement</span></span> | <span data-ttu-id="5bcc5-109">Wert</span><span class="sxs-lookup"><span data-stu-id="5bcc5-109">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bcc5-110">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5bcc5-110">Minimum supported client</span></span><br/> | <span data-ttu-id="5bcc5-111">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5bcc5-111">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="5bcc5-112">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5bcc5-112">Minimum supported server</span></span><br/> | <span data-ttu-id="5bcc5-113">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5bcc5-113">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="5bcc5-114">Header</span><span class="sxs-lookup"><span data-stu-id="5bcc5-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="5bcc5-115"><dt>SSPI. h (Include Security. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5bcc5-115"><dt>Sspi.h (include Security.h)</dt></span></span> </dl> |



 

 

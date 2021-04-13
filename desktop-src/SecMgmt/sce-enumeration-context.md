---
description: Der SCE- \_ \_ EnumerationContext-Datentyp ist ein nicht transparentes Handle, das vom Sicherheitskonfigurations-Toolset bereitgestellt wird. Sie wird von der pfsce- \_ Abfrage \_ Info-Funktion verwendet, um durch die Sicherheitsdatenbank zu navigieren.
ms.assetid: 05629c49-e36b-4045-93d0-d0f4bc09b08a
title: SCE_ENUMERATION_CONTEXT (scesvc. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e380f6f99d68ad63199c3b82f5aa1e5ace8ddf0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343118"
---
# <a name="sce_enumeration_context"></a><span data-ttu-id="fe453-104">SCE- \_ \_ enumerationskontext</span><span class="sxs-lookup"><span data-stu-id="fe453-104">SCE\_ENUMERATION\_CONTEXT</span></span>

<span data-ttu-id="fe453-105">Der **SCE- \_ EnumerationContext \_** -Datentyp ist ein nicht transparentes Handle, das vom Sicherheitskonfigurations-Toolset bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="fe453-105">The **SCE\_ENUMERATION\_CONTEXT** data type is an opaque handle provided by the Security Configuration tool set.</span></span> <span data-ttu-id="fe453-106">Sie wird von der [**pfsce- \_ Abfrage \_ Info**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) -Funktion verwendet, um durch die Sicherheitsdatenbank zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="fe453-106">It is used by the [**PFSCE\_QUERY\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) function to navigate through the security database.</span></span>


```C++
typedef ULONG SCE_ENUMERATION_CONTEXT, *PSCE_ENUMERATION_CONTEXT;
```



## <a name="requirements"></a><span data-ttu-id="fe453-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe453-107">Requirements</span></span>



| <span data-ttu-id="fe453-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fe453-108">Requirement</span></span> | <span data-ttu-id="fe453-109">Wert</span><span class="sxs-lookup"><span data-stu-id="fe453-109">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fe453-110">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fe453-110">Minimum supported client</span></span><br/> | <span data-ttu-id="fe453-111">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fe453-111">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="fe453-112">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fe453-112">Minimum supported server</span></span><br/> | <span data-ttu-id="fe453-113">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fe453-113">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="fe453-114">Header</span><span class="sxs-lookup"><span data-stu-id="fe453-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe453-115"><dt>Scesvc. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe453-115"><dt>Scesvc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe453-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fe453-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe453-117">**pfsce- \_ Abfrage \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="fe453-117">**PFSCE\_QUERY\_INFO**</span></span>](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info)
</dt> </dl>

 


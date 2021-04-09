---
description: Der SCE- \_ handle-Datentyp ist ein nicht transparentes Handle, das vom Sicherheitskonfigurations-Toolset bereitgestellt wird. Sie wird von pfsce \_ -Abfrage \_ Informationen und pfsce \_ Set \_ Info-Unterstützungsfunktionen verwendet, um Informationen zwischen der Anlage und der Sicherheitsdatenbank zu übergeben.
ms.assetid: 8db91e6f-b31e-40c6-a158-b4b3b00ba0c0
title: SCE_HANDLE (scesvc. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fef21dbe03d97dfa14537d5df132ba3cb222643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128773"
---
# <a name="sce_handle"></a><span data-ttu-id="b011b-104">SCE- \_ handle</span><span class="sxs-lookup"><span data-stu-id="b011b-104">SCE\_HANDLE</span></span>

<span data-ttu-id="b011b-105">Der **SCE- \_ handle** -Datentyp ist ein nicht transparentes Handle, das vom Sicherheitskonfigurations-Toolset bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="b011b-105">The **SCE\_HANDLE** data type is an opaque handle provided by the Security Configuration tool set.</span></span> <span data-ttu-id="b011b-106">Sie wird von [**pfsce- \_ Abfrage \_ Informationen**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) und [**pfsce \_ Set \_ Info**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) -Unterstützungsfunktionen verwendet, um Informationen zwischen der Anlage und der Sicherheitsdatenbank zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="b011b-106">It is used by [**PFSCE\_QUERY\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) and [**PFSCE\_SET\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) support functions to pass information between the attachment and the security database.</span></span>


```C++
typedef PVOID SCE_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="b011b-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b011b-107">Requirements</span></span>



| <span data-ttu-id="b011b-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b011b-108">Requirement</span></span> | <span data-ttu-id="b011b-109">Wert</span><span class="sxs-lookup"><span data-stu-id="b011b-109">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b011b-110">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b011b-110">Minimum supported client</span></span><br/> | <span data-ttu-id="b011b-111">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b011b-111">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b011b-112">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b011b-112">Minimum supported server</span></span><br/> | <span data-ttu-id="b011b-113">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b011b-113">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b011b-114">Header</span><span class="sxs-lookup"><span data-stu-id="b011b-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="b011b-115"><dt>Scesvc. h</dt></span><span class="sxs-lookup"><span data-stu-id="b011b-115"><dt>Scesvc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b011b-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b011b-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b011b-117">**pfsce- \_ Abfrage \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="b011b-117">**PFSCE\_QUERY\_INFO**</span></span>](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info)
</dt> <dt>

[<span data-ttu-id="b011b-118">**pfsce- \_ festgelegte \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="b011b-118">**PFSCE\_SET\_INFO**</span></span>](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info)
</dt> </dl>

 


---
description: Der Datentyp scesvc \_ handle ist ein nicht transparentes Handle, das vom Sicherheitskonfigurations-Toolset bereitgestellt wird.
ms.assetid: 478d7d4b-7983-4247-b8be-2e2cd3327533
title: SCESVC_HANDLE (scesvc. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09fbc115326361e4cbfe1152361a70a36007a302
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525712"
---
# <a name="scesvc_handle"></a><span data-ttu-id="a4ddf-103">scesvc- \_ handle</span><span class="sxs-lookup"><span data-stu-id="a4ddf-103">SCESVC\_HANDLE</span></span>

<span data-ttu-id="a4ddf-104">Der Datentyp **scesvc \_ handle** ist ein nicht transparentes Handle, das vom Sicherheitskonfigurations-Toolset bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="a4ddf-104">The **SCESVC\_HANDLE** data type is an opaque handle provided by the Security Configuration tool set.</span></span> <span data-ttu-id="a4ddf-105">Sie wird von Methoden der Schnittstellen [**iscesvplattachmentdata**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) und [**iscesvplattachmentpersistinfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) verwendet, um Informationen zwischen dem Snap-in "Sicherheitskonfiguration" und der Snap-in-Erweiterung zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="a4ddf-105">It is used by methods of the [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) and [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) interfaces to pass information between the Security Configuration snap-in and the snap-in extension.</span></span>


```C++
typedef PVOID SCESVC_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="a4ddf-106">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a4ddf-106">Requirements</span></span>



| <span data-ttu-id="a4ddf-107">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a4ddf-107">Requirement</span></span> | <span data-ttu-id="a4ddf-108">Wert</span><span class="sxs-lookup"><span data-stu-id="a4ddf-108">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a4ddf-109">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a4ddf-109">Minimum supported client</span></span><br/> | <span data-ttu-id="a4ddf-110">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a4ddf-110">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a4ddf-111">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a4ddf-111">Minimum supported server</span></span><br/> | <span data-ttu-id="a4ddf-112">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a4ddf-112">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a4ddf-113">Header</span><span class="sxs-lookup"><span data-stu-id="a4ddf-113">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4ddf-114"><dt>Scesvc. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4ddf-114"><dt>Scesvc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4ddf-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a4ddf-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4ddf-116">**Iscesvstreamtachmentdata**</span><span class="sxs-lookup"><span data-stu-id="a4ddf-116">**ISceSvcAttachmentData**</span></span>](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata)
</dt> <dt>

[<span data-ttu-id="a4ddf-117">**Iscesvplattachmentpersistinfo**</span><span class="sxs-lookup"><span data-stu-id="a4ddf-117">**ISceSvcAttachmentPersistInfo**</span></span>](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo)
</dt> </dl>

 

 





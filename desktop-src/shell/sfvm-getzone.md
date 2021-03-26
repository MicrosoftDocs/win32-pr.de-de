---
description: 'Ermöglicht dem Rückruf Objekt, Internet Zonen Informationen bereitzustellen. Wird von ishellfolderviewcb:: messagesfvcb verwendet.'
ms.assetid: 6fae7925-b1be-4270-9318-7fa517563dad
title: SFVM_GETZONE Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5586188aeab6a054e22e4b242039beaae1ce390d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530182"
---
# <a name="sfvm_getzone-message"></a><span data-ttu-id="a3571-104">Sfvm- \_ getzone-Nachricht</span><span class="sxs-lookup"><span data-stu-id="a3571-104">SFVM\_GETZONE message</span></span>

<span data-ttu-id="a3571-105">\[Diese Benachrichtigung wird durch Windows XP Service Pack 2 (SP2) und Windows Server 2003 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a3571-105">\[This notification is supported through Windows XP Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="a3571-106">Sie wird möglicherweise in nachfolgenden Versionen von Windows nicht unterstützt.\]</span><span class="sxs-lookup"><span data-stu-id="a3571-106">It might be unsupported in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="a3571-107">Ermöglicht dem Rückruf Objekt, Internet Zonen Informationen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="a3571-107">Allows the callback object to provide Internet zone information.</span></span> <span data-ttu-id="a3571-108">Wird von [**ishellfolderviewcb:: messagesfvcb**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.</span><span class="sxs-lookup"><span data-stu-id="a3571-108">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETZONE
    lParam = (LPARAM)(DWORD*) zone;
            
```



## <a name="parameters"></a><span data-ttu-id="a3571-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3571-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3571-110">*Zone* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a3571-110">*zone* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3571-111">Einer der folgenden Werte, der die Internet Zone angibt.</span><span class="sxs-lookup"><span data-stu-id="a3571-111">One of the following values indicating the Internet zone.</span></span> <span data-ttu-id="a3571-112">Diese Werte bilden die [**urlzone**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537175(v=vs.85)) -Enumeration, die in Urlmon. h definiert ist.</span><span class="sxs-lookup"><span data-stu-id="a3571-112">These values constitute the [**URLZONE**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537175(v=vs.85)) enumeration, defined in Urlmon.h.</span></span>

<dt>

<span id="URLZONE_LOCAL_MACHINE"></span><span id="urlzone_local_machine"></span>

<span data-ttu-id="a3571-113"><span id="URLZONE_LOCAL_MACHINE"></span><span id="urlzone_local_machine"></span>**lokaler urlzone- \_ \_ Computer**</span><span class="sxs-lookup"><span data-stu-id="a3571-113"><span id="URLZONE_LOCAL_MACHINE"></span><span id="urlzone_local_machine"></span>**URLZONE\_LOCAL\_MACHINE**</span></span>


</dt> <dd>

<span data-ttu-id="a3571-114">Die für den Inhalt verwendete Zone, die sich bereits auf dem lokalen Computer des Benutzers befindet.</span><span class="sxs-lookup"><span data-stu-id="a3571-114">Zone used for content already on the user's local computer.</span></span> <span data-ttu-id="a3571-115">Diese Zone wird nicht von der Benutzeroberfläche verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="a3571-115">This zone is not exposed by the user interface.</span></span>

</dd> <dt>

<span id="URLZONE_INTRANET"></span><span id="urlzone_intranet"></span>

<span data-ttu-id="a3571-116"><span id="URLZONE_INTRANET"></span><span id="urlzone_intranet"></span>**urlzone- \_ Intranet**</span><span class="sxs-lookup"><span data-stu-id="a3571-116"><span id="URLZONE_INTRANET"></span><span id="urlzone_intranet"></span>**URLZONE\_INTRANET**</span></span>


</dt> <dd>

<span data-ttu-id="a3571-117">Zone für Inhalte, die in einem Intranet gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="a3571-117">Zone used for content found on an intranet.</span></span>

</dd> <dt>

<span id="URLZONE_TRUSTED"></span><span id="urlzone_trusted"></span>

<span data-ttu-id="a3571-118"><span id="URLZONE_TRUSTED"></span><span id="urlzone_trusted"></span>**urlzone \_ vertrauenswürdig**</span><span class="sxs-lookup"><span data-stu-id="a3571-118"><span id="URLZONE_TRUSTED"></span><span id="urlzone_trusted"></span>**URLZONE\_TRUSTED**</span></span>


</dt> <dd>

<span data-ttu-id="a3571-119">Zone, die für vertrauenswürdige Websites im Internet verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a3571-119">Zone used for trusted websites on the Internet.</span></span>

</dd> <dt>

<span id="URLZONE_INTERNET"></span><span id="urlzone_internet"></span>

<span data-ttu-id="a3571-120"><span id="URLZONE_INTERNET"></span><span id="urlzone_internet"></span>**urlzone- \_ Internet**</span><span class="sxs-lookup"><span data-stu-id="a3571-120"><span id="URLZONE_INTERNET"></span><span id="urlzone_internet"></span>**URLZONE\_INTERNET**</span></span>


</dt> <dd>

<span data-ttu-id="a3571-121">Zone, die für die meisten Inhalte im Internet verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a3571-121">Zone used for most of the content on the Internet.</span></span>

</dd> <dt>

<span id="URLZONE_UNTRUSTED"></span><span id="urlzone_untrusted"></span>

<span data-ttu-id="a3571-122"><span id="URLZONE_UNTRUSTED"></span><span id="urlzone_untrusted"></span>**urlzone \_ nicht vertrauenswürdig**</span><span class="sxs-lookup"><span data-stu-id="a3571-122"><span id="URLZONE_UNTRUSTED"></span><span id="urlzone_untrusted"></span>**URLZONE\_UNTRUSTED**</span></span>


</dt> <dd>

<span data-ttu-id="a3571-123">Zone, die für nicht vertrauenswürdige Websites verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a3571-123">Zone used for websites that are not trusted.</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a3571-124">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="a3571-124">Requirements</span></span>



| <span data-ttu-id="a3571-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a3571-125">Requirement</span></span> | <span data-ttu-id="a3571-126">Wert</span><span class="sxs-lookup"><span data-stu-id="a3571-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a3571-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a3571-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a3571-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a3571-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a3571-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a3571-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a3571-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a3571-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a3571-131">Header</span><span class="sxs-lookup"><span data-stu-id="a3571-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3571-132"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3571-132"><dt>Shlobj.h</dt></span></span> </dl> |



 

 

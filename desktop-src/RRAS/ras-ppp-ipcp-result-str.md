---
title: RAS_PPP_IPCP_RESULT Struktur (rassapi. h)
description: Die RAS \_ \_ -PPP-IPCP \_ -Ergebnis Struktur wird verwendet, um das Ergebnis einer PPP-IP (Internet Protocol)-Projektions Operation für einen Port zu melden.
ms.assetid: edbdc8f2-ba56-4d34-8908-f7eccc2ebf61
keywords:
- RAS_PPP_IPCP_RESULT Struktur-RAS
topic_type:
- apiref
api_name:
- RAS_PPP_IPCP_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eedcd7c7390e01849371eee2cbb24ffa2593900d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517879"
---
# <a name="ras_ppp_ipcp_result-structure"></a><span data-ttu-id="80def-104">RAS- \_ PPP- \_ IPCP- \_ Ergebnis Struktur</span><span class="sxs-lookup"><span data-stu-id="80def-104">RAS\_PPP\_IPCP\_RESULT structure</span></span>

<span data-ttu-id="80def-105">\[Die **RAS- \_ PPP- \_ IPCP- \_ Ergebnis** Struktur wird ab Windows Vista nicht unterstützt.\]</span><span class="sxs-lookup"><span data-stu-id="80def-105">\[The **RAS\_PPP\_IPCP\_RESULT** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="80def-106">Die **RAS- \_ PPP- \_ IPCP- \_ Ergebnis** Struktur wird verwendet, um das Ergebnis einer PPP-IP (Internet Protocol)-Projektions Operation für einen Port zu melden.</span><span class="sxs-lookup"><span data-stu-id="80def-106">The **RAS\_PPP\_IPCP\_RESULT** structure is used to report the result of a PPP Internet Protocol (IP) projection operation for a port.</span></span>

## <a name="syntax"></a><span data-ttu-id="80def-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="80def-107">Syntax</span></span>


```C++
typedef struct _RAS_PPP_IPCP_RESULT {
  DWORD dwError;
  WCHAR wszAddress[RAS_IPADDRESSLEN + 1];
} RAS_PPP_IPCP_RESULT;
```



## <a name="members"></a><span data-ttu-id="80def-108">Member</span><span class="sxs-lookup"><span data-stu-id="80def-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="80def-109">**dwError**</span><span class="sxs-lookup"><span data-stu-id="80def-109">**dwError**</span></span>
</dt> <dd>

<span data-ttu-id="80def-110">Gibt die Ergebnisse des IP-Projektions Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="80def-110">Indicates the results of the IP projection operation.</span></span> <span data-ttu-id="80def-111">Der Wert kein \_ Fehler gibt einen Erfolg an. in diesem Fall ist der Member **wszaddress** gültig.</span><span class="sxs-lookup"><span data-stu-id="80def-111">A value of NO\_ERROR indicates success, in which case, the **wszAddress** member is valid.</span></span> <span data-ttu-id="80def-112">Wenn der Projektions Vorgang nicht erfolgreich war, ist **dwError** ein Fehlercode aus "Winerror. h" oder "raserror. h".</span><span class="sxs-lookup"><span data-stu-id="80def-112">If the projection operation was not successful, **dwError** is an error code from Winerror.h or Raserror.h.</span></span>

</dd> <dt>

<span data-ttu-id="80def-113">**wszaddress**</span><span class="sxs-lookup"><span data-stu-id="80def-113">**wszAddress**</span></span>
</dt> <dd>

<span data-ttu-id="80def-114">Eine NULL-terminierte Unicode-Zeichenfolge, die die dem Remote Client zugewiesene IP-Adresse angibt.</span><span class="sxs-lookup"><span data-stu-id="80def-114">A null-terminated Unicode string that specifies the IP address assigned to the remote client.</span></span> <span data-ttu-id="80def-115">Diese Zeichenfolge hat die Form \*a ***.** _b_* _._ *_c_*_._ \* _d_.</span><span class="sxs-lookup"><span data-stu-id="80def-115">This string has the form *a\***.**_b_*_._*_c_*_._\*_d_.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="80def-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="80def-116">Requirements</span></span>



| <span data-ttu-id="80def-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="80def-117">Requirement</span></span> | <span data-ttu-id="80def-118">Wert</span><span class="sxs-lookup"><span data-stu-id="80def-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="80def-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="80def-119">Minimum supported client</span></span><br/> | <span data-ttu-id="80def-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="80def-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="80def-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="80def-121">Minimum supported server</span></span><br/> | <span data-ttu-id="80def-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="80def-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="80def-123">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="80def-123">End of client support</span></span><br/>    | <span data-ttu-id="80def-124">Windows XP</span><span class="sxs-lookup"><span data-stu-id="80def-124">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="80def-125">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="80def-125">End of server support</span></span><br/>    | <span data-ttu-id="80def-126">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="80def-126">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="80def-127">Header</span><span class="sxs-lookup"><span data-stu-id="80def-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="80def-128"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="80def-128"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80def-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="80def-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80def-130">Remote Zugriffs Dienst (RAS) (Übersicht)</span><span class="sxs-lookup"><span data-stu-id="80def-130">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="80def-131">RAS-Server-Verwaltungsstrukturen</span><span class="sxs-lookup"><span data-stu-id="80def-131">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="80def-132">**RAS- \_ Port \_ 1**</span><span class="sxs-lookup"><span data-stu-id="80def-132">**RAS\_PORT\_1**</span></span>](ras-port-1-str.md)
</dt> <dt>

[<span data-ttu-id="80def-133">**Ergebnis der RAS- \_ PPP- \_ Projektion \_**</span><span class="sxs-lookup"><span data-stu-id="80def-133">**RAS\_PPP\_PROJECTION\_RESULT**</span></span>](ras-ppp-projection-result-str.md)
</dt> <dt>

[<span data-ttu-id="80def-134">**Rasadminportgetinfo**</span><span class="sxs-lookup"><span data-stu-id="80def-134">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

 






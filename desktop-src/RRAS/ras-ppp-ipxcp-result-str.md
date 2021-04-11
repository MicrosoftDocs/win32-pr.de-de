---
title: RAS_PPP_IPXCP_RESULT Struktur (rassapi. h)
description: Die RAS- \_ PPP- \_ IPXCP- \_ Ergebnis Struktur wird verwendet, um das Ergebnis einer PPP-IPX-Projektions Operation (Internetwork Packet Exchange) für einen Port zu melden.
ms.assetid: e1236e1b-f0ef-46cf-a12f-35529215752c
keywords:
- RAS_PPP_IPXCP_RESULT Struktur-RAS
topic_type:
- apiref
api_name:
- RAS_PPP_IPXCP_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bb7ca4d006bd1a1df5a645799998b463c0b14f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040684"
---
# <a name="ras_ppp_ipxcp_result-structure"></a><span data-ttu-id="ff1b3-104">RAS- \_ PPP- \_ IPXCP- \_ Ergebnis Struktur</span><span class="sxs-lookup"><span data-stu-id="ff1b3-104">RAS\_PPP\_IPXCP\_RESULT structure</span></span>

<span data-ttu-id="ff1b3-105">\[Die **RAS- \_ PPP- \_ IPXCP- \_ Ergebnis** Struktur wird ab Windows Vista nicht unterstützt.\]</span><span class="sxs-lookup"><span data-stu-id="ff1b3-105">\[The **RAS\_PPP\_IPXCP\_RESULT** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="ff1b3-106">Die **RAS- \_ PPP- \_ IPXCP- \_ Ergebnis** Struktur wird verwendet, um das Ergebnis einer PPP-IPX-Projektions Operation (Internetwork Packet Exchange) für einen Port zu melden.</span><span class="sxs-lookup"><span data-stu-id="ff1b3-106">The **RAS\_PPP\_IPXCP\_RESULT** structure is used to report the result of a PPP Internetwork Packet Exchange (IPX) projection operation for a port.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff1b3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff1b3-107">Syntax</span></span>


```C++
typedef struct _RAS_PPP_IPXCP_RESULT {
  DWORD dwError;
  WCHAR wszAddress[RAS_IPXADDRESSLEN + 1];
} RAS_PPP_IPXCP_RESULT;
```



## <a name="members"></a><span data-ttu-id="ff1b3-108">Member</span><span class="sxs-lookup"><span data-stu-id="ff1b3-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="ff1b3-109">**dwError**</span><span class="sxs-lookup"><span data-stu-id="ff1b3-109">**dwError**</span></span>
</dt> <dd>

<span data-ttu-id="ff1b3-110">Gibt die Ergebnisse der IPX-Projektions Operation an.</span><span class="sxs-lookup"><span data-stu-id="ff1b3-110">Indicates the results of the IPX projection operation.</span></span> <span data-ttu-id="ff1b3-111">Der Wert kein \_ Fehler gibt einen Erfolg an. in diesem Fall ist der Member **wszaddress** gültig.</span><span class="sxs-lookup"><span data-stu-id="ff1b3-111">A value of NO\_ERROR indicates success, in which case, the **wszAddress** member is valid.</span></span> <span data-ttu-id="ff1b3-112">Wenn der Projektions Vorgang nicht erfolgreich war, ist **dwError** ein Fehlercode aus "Winerror. h" oder "raserror. h".</span><span class="sxs-lookup"><span data-stu-id="ff1b3-112">If the projection operation was not successful, **dwError** is an error code from Winerror.h or Raserror.h.</span></span>

</dd> <dt>

<span data-ttu-id="ff1b3-113">**wszaddress**</span><span class="sxs-lookup"><span data-stu-id="ff1b3-113">**wszAddress**</span></span>
</dt> <dd>

<span data-ttu-id="ff1b3-114">Eine NULL-terminierte Unicode-Zeichenfolge, die die dem Remote Client zugewiesene IPX-Adresse angibt.</span><span class="sxs-lookup"><span data-stu-id="ff1b3-114">A null-terminated Unicode string that specifies the IPX address assigned to the remote client.</span></span> <span data-ttu-id="ff1b3-115">Diese Zeichenfolge weist das \* NET \* auf **.** _Knoten_ Formular.</span><span class="sxs-lookup"><span data-stu-id="ff1b3-115">This string has the \*net\***.**_node_ form.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ff1b3-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ff1b3-116">Requirements</span></span>



| <span data-ttu-id="ff1b3-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ff1b3-117">Requirement</span></span> | <span data-ttu-id="ff1b3-118">Wert</span><span class="sxs-lookup"><span data-stu-id="ff1b3-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ff1b3-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ff1b3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ff1b3-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ff1b3-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="ff1b3-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ff1b3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ff1b3-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ff1b3-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ff1b3-123">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="ff1b3-123">End of client support</span></span><br/>    | <span data-ttu-id="ff1b3-124">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ff1b3-124">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="ff1b3-125">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="ff1b3-125">End of server support</span></span><br/>    | <span data-ttu-id="ff1b3-126">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ff1b3-126">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="ff1b3-127">Header</span><span class="sxs-lookup"><span data-stu-id="ff1b3-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff1b3-128"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff1b3-128"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff1b3-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff1b3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff1b3-130">Remote Zugriffs Dienst (RAS) (Übersicht)</span><span class="sxs-lookup"><span data-stu-id="ff1b3-130">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="ff1b3-131">RAS-Server-Verwaltungsstrukturen</span><span class="sxs-lookup"><span data-stu-id="ff1b3-131">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="ff1b3-132">**RAS- \_ Port \_ 1**</span><span class="sxs-lookup"><span data-stu-id="ff1b3-132">**RAS\_PORT\_1**</span></span>](ras-port-1-str.md)
</dt> <dt>

[<span data-ttu-id="ff1b3-133">**Ergebnis der RAS- \_ PPP- \_ Projektion \_**</span><span class="sxs-lookup"><span data-stu-id="ff1b3-133">**RAS\_PPP\_PROJECTION\_RESULT**</span></span>](ras-ppp-projection-result-str.md)
</dt> <dt>

[<span data-ttu-id="ff1b3-134">**Rasadminportgetinfo**</span><span class="sxs-lookup"><span data-stu-id="ff1b3-134">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

 






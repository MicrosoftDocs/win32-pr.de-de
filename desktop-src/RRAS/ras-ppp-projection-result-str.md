---
title: RAS_PPP_PROJECTION_RESULT Struktur (rassapi. h)
description: Die Ergebnis Struktur der RAS- \_ PPP- \_ Projektion \_ wird verwendet, um die Ergebnisse der verschiedenen PPP-Projektions Vorgänge für einen Port zu melden.
ms.assetid: 061b1b51-4b6f-4127-8ee5-8a1913a2aa99
keywords:
- RAS_PPP_PROJECTION_RESULT Struktur-RAS
topic_type:
- apiref
api_name:
- RAS_PPP_PROJECTION_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a9aa3aef828249b5c72f9e7cdd1bd3b69c96832
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741793"
---
# <a name="ras_ppp_projection_result-structure"></a><span data-ttu-id="41cad-104">\_ \_ \_ Ergebnis Struktur der RAS-PPP-Projektion</span><span class="sxs-lookup"><span data-stu-id="41cad-104">RAS\_PPP\_PROJECTION\_RESULT structure</span></span>

<span data-ttu-id="41cad-105">\[Die **Ergebnis Struktur der RAS- \_ PPP- \_ Projektion \_** wird ab Windows Vista nicht unterstützt.\]</span><span class="sxs-lookup"><span data-stu-id="41cad-105">\[The **RAS\_PPP\_PROJECTION\_RESULT** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="41cad-106">Die **Ergebnis Struktur der RAS- \_ PPP- \_ Projektion \_** wird verwendet, um die Ergebnisse der verschiedenen PPP-Projektions Vorgänge für einen Port zu melden.</span><span class="sxs-lookup"><span data-stu-id="41cad-106">The **RAS\_PPP\_PROJECTION\_RESULT** structure is used to report the results of the various PPP projection operations for a port.</span></span>

## <a name="syntax"></a><span data-ttu-id="41cad-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="41cad-107">Syntax</span></span>


```C++
typedef struct _RAS_PPP_PROJECTION_RESULT {
  RAS_PPP_NBFCP_RESULT nbf;
  RAS_PPP_IPCP_RESULT  ip;
  RAS_PPP_IPXCP_RESULT ipx;
  RAS_PPP_ATCP_RESULT  at;
} RAS_PPP_PROJECTION_RESULT;
```



## <a name="members"></a><span data-ttu-id="41cad-108">Member</span><span class="sxs-lookup"><span data-stu-id="41cad-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="41cad-109">**nbf**</span><span class="sxs-lookup"><span data-stu-id="41cad-109">**nbf**</span></span>
</dt> <dd>

<span data-ttu-id="41cad-110">Eine [**RAS- \_ PPP- \_ NBFCP- \_ Ergebnis**](ras-ppp-nbfcp-result-str.md) Struktur, die das Ergebnis einer PPP-Pipeline mit NetBEUI Framer (NBF) meldet.</span><span class="sxs-lookup"><span data-stu-id="41cad-110">A [**RAS\_PPP\_NBFCP\_RESULT**](ras-ppp-nbfcp-result-str.md) structure that reports the result of a PPP NetBEUI Framer (NBF) projection operation.</span></span>

</dd> <dt>

<span data-ttu-id="41cad-111">**-**</span><span class="sxs-lookup"><span data-stu-id="41cad-111">**ip**</span></span>
</dt> <dd>

<span data-ttu-id="41cad-112">Eine [**RAS- \_ PPP- \_ IPCP- \_ Ergebnis**](ras-ppp-ipcp-result-str.md) Struktur, die das Ergebnis einer PPP-IP (Internet Protocol)-Projektions Operation meldet.</span><span class="sxs-lookup"><span data-stu-id="41cad-112">A [**RAS\_PPP\_IPCP\_RESULT**](ras-ppp-ipcp-result-str.md) structure that reports the result of a PPP Internet Protocol (IP) projection operation.</span></span>

</dd> <dt>

<span data-ttu-id="41cad-113">**IPX**</span><span class="sxs-lookup"><span data-stu-id="41cad-113">**ipx**</span></span>
</dt> <dd>

<span data-ttu-id="41cad-114">Eine [**RAS- \_ PPP- \_ IPXCP- \_ Ergebnis**](ras-ppp-ipxcp-result-str.md) Struktur, die das Ergebnis eines PPP-IPX-Projektions Vorgangs (Internetwork Packet Exchange) meldet.</span><span class="sxs-lookup"><span data-stu-id="41cad-114">A [**RAS\_PPP\_IPXCP\_RESULT**](ras-ppp-ipxcp-result-str.md) structure that reports the result of a PPP Internetwork Packet Exchange (IPX) projection operation.</span></span>

</dd> <dt>

<span data-ttu-id="41cad-115">**at**</span><span class="sxs-lookup"><span data-stu-id="41cad-115">**at**</span></span>
</dt> <dd>

<span data-ttu-id="41cad-116">Eine [**RAS- \_ PPP- \_ ATCP- \_ Ergebnis**](ras-ppp-atcp-result-str.md) Struktur.</span><span class="sxs-lookup"><span data-stu-id="41cad-116">A [**RAS\_PPP\_ATCP\_RESULT**](ras-ppp-atcp-result-str.md) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="41cad-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="41cad-117">Remarks</span></span>

<span data-ttu-id="41cad-118">Diese Struktur meldet die Projektions Ergebnisse für NetBEUI-, TCP/IP-und IPX-Protokolle.</span><span class="sxs-lookup"><span data-stu-id="41cad-118">This structure reports the projection results for NetBEUI, TCP/IP, and IPX protocols.</span></span> <span data-ttu-id="41cad-119">Jede PPP-Struktur verfügt über einen **dwError** -Member, der angibt, ob die anderen Informationen in der Struktur gültig sind.</span><span class="sxs-lookup"><span data-stu-id="41cad-119">Each PPP structure has a **dwError** member that indicates whether the other information in the structure is valid.</span></span> <span data-ttu-id="41cad-120">Wenn **dwError** keinen \_ Fehler hat, sind die anderen Informationen gültig.</span><span class="sxs-lookup"><span data-stu-id="41cad-120">If **dwError** is NO\_ERROR, the other information is valid.</span></span> <span data-ttu-id="41cad-121">Wenn **dwError** einer der Fehlercodes in WinError. h oder raserror. h ist, sind die anderen Informationen ungültig.</span><span class="sxs-lookup"><span data-stu-id="41cad-121">If **dwError** is one of the error codes in Winerror.h or Raserror.h, the other information is not valid.</span></span>

## <a name="requirements"></a><span data-ttu-id="41cad-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="41cad-122">Requirements</span></span>



| <span data-ttu-id="41cad-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="41cad-123">Requirement</span></span> | <span data-ttu-id="41cad-124">Wert</span><span class="sxs-lookup"><span data-stu-id="41cad-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="41cad-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="41cad-125">Minimum supported client</span></span><br/> | <span data-ttu-id="41cad-126">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="41cad-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="41cad-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="41cad-127">Minimum supported server</span></span><br/> | <span data-ttu-id="41cad-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="41cad-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="41cad-129">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="41cad-129">End of client support</span></span><br/>    | <span data-ttu-id="41cad-130">Windows XP</span><span class="sxs-lookup"><span data-stu-id="41cad-130">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="41cad-131">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="41cad-131">End of server support</span></span><br/>    | <span data-ttu-id="41cad-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="41cad-132">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="41cad-133">Header</span><span class="sxs-lookup"><span data-stu-id="41cad-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="41cad-134"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="41cad-134"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41cad-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41cad-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41cad-136">Remote Zugriffs Dienst (RAS) (Übersicht)</span><span class="sxs-lookup"><span data-stu-id="41cad-136">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="41cad-137">RAS-Server-Verwaltungsstrukturen</span><span class="sxs-lookup"><span data-stu-id="41cad-137">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="41cad-138">**RAS- \_ Port \_ 1**</span><span class="sxs-lookup"><span data-stu-id="41cad-138">**RAS\_PORT\_1**</span></span>](ras-port-1-str.md)
</dt> <dt>

[<span data-ttu-id="41cad-139">**Ergebnis des RAS- \_ PPP- \_ ATCP \_**</span><span class="sxs-lookup"><span data-stu-id="41cad-139">**RAS\_PPP\_ATCP\_RESULT**</span></span>](ras-ppp-atcp-result-str.md)
</dt> <dt>

[<span data-ttu-id="41cad-140">**Ergebnis des RAS- \_ PPP- \_ IPCP \_**</span><span class="sxs-lookup"><span data-stu-id="41cad-140">**RAS\_PPP\_IPCP\_RESULT**</span></span>](ras-ppp-ipcp-result-str.md)
</dt> <dt>

[<span data-ttu-id="41cad-141">**Ergebnis der RAS- \_ PPP- \_ IPXCP \_**</span><span class="sxs-lookup"><span data-stu-id="41cad-141">**RAS\_PPP\_IPXCP\_RESULT**</span></span>](ras-ppp-ipxcp-result-str.md)
</dt> <dt>

[<span data-ttu-id="41cad-142">**RAS- \_ PPP- \_ NBF- \_ Ergebnis**</span><span class="sxs-lookup"><span data-stu-id="41cad-142">**RAS\_PPP\_NBFCP\_RESULT**</span></span>](ras-ppp-nbfcp-result-str.md)
</dt> <dt>

[<span data-ttu-id="41cad-143">**Rasadminportgetinfo**</span><span class="sxs-lookup"><span data-stu-id="41cad-143">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

 






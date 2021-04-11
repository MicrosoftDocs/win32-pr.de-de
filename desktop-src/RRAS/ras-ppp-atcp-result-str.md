---
title: RAS_PPP_ATCP_RESULT Struktur (rassapi. h)
description: Die RAS- \_ PPP- \_ ATCP- \_ Ergebnis Struktur wird verwendet, um das Ergebnis einer AppleTalk-Protokoll Projektions Operation für einen Port zu melden.
ms.assetid: ac9df618-f79c-4066-a37e-f92e64e951dd
keywords:
- RAS_PPP_ATCP_RESULT Struktur-RAS
topic_type:
- apiref
api_name:
- RAS_PPP_ATCP_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66f3f950af9d5bdde8feef085457a895212ad04b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956574"
---
# <a name="ras_ppp_atcp_result-structure"></a><span data-ttu-id="7fe87-104">RAS- \_ PPP- \_ ATCP- \_ Ergebnis Struktur</span><span class="sxs-lookup"><span data-stu-id="7fe87-104">RAS\_PPP\_ATCP\_RESULT structure</span></span>

<span data-ttu-id="7fe87-105">\[Die **RAS- \_ PPP- \_ ATCP- \_ Ergebnis** Struktur wird ab Windows Vista nicht unterstützt.\]</span><span class="sxs-lookup"><span data-stu-id="7fe87-105">\[The **RAS\_PPP\_ATCP\_RESULT** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="7fe87-106">Die **RAS- \_ PPP- \_ ATCP- \_ Ergebnis** Struktur wird verwendet, um das Ergebnis einer AppleTalk-Protokoll Projektions Operation für einen Port zu melden.</span><span class="sxs-lookup"><span data-stu-id="7fe87-106">The **RAS\_PPP\_ATCP\_RESULT** structure is used to report the result of an AppleTalk protocol projection operation for a port.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fe87-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7fe87-107">Syntax</span></span>


```C++
typedef struct _RAS_PPP_ATCP_RESULT {
  DWORD dwError;
  WCHAR wszAddress[RAS_ATADDRESSLEN + 1];
} RAS_PPP_ATCP_RESULT;
```



## <a name="members"></a><span data-ttu-id="7fe87-108">Member</span><span class="sxs-lookup"><span data-stu-id="7fe87-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="7fe87-109">**dwError**</span><span class="sxs-lookup"><span data-stu-id="7fe87-109">**dwError**</span></span>
</dt> <dd>

<span data-ttu-id="7fe87-110">Gibt einen Wert an, der die Ergebnisse der AppleTalk-Projektions Operation angibt.</span><span class="sxs-lookup"><span data-stu-id="7fe87-110">Specifies a value that indicates the results of the AppleTalk projection operation.</span></span> <span data-ttu-id="7fe87-111">Der Wert kein \_ Fehler gibt einen Erfolg an. in diesem Fall ist der Member **wszaddress** gültig.</span><span class="sxs-lookup"><span data-stu-id="7fe87-111">A value of NO\_ERROR indicates success, in which case, the **wszAddress** member is valid.</span></span> <span data-ttu-id="7fe87-112">Wenn der Projektions Vorgang nicht erfolgreich ist, ist **dwError** ein Fehlercode von "Winerror. h" oder "raserror. h".</span><span class="sxs-lookup"><span data-stu-id="7fe87-112">If the projection operation is not successful, **dwError** is an error code from Winerror.h or Raserror.h.</span></span>

</dd> <dt>

<span data-ttu-id="7fe87-113">**wszaddress**</span><span class="sxs-lookup"><span data-stu-id="7fe87-113">**wszAddress**</span></span>
</dt> <dd>

<span data-ttu-id="7fe87-114">Gibt eine NULL-terminierte Unicode-Zeichenfolge an, die die dem Remote Client zugewiesene IP-Adresse angibt.</span><span class="sxs-lookup"><span data-stu-id="7fe87-114">Specifies a null-terminated Unicode string that specifies the IP address assigned to the remote client.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7fe87-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7fe87-115">Requirements</span></span>



| <span data-ttu-id="7fe87-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7fe87-116">Requirement</span></span> | <span data-ttu-id="7fe87-117">Wert</span><span class="sxs-lookup"><span data-stu-id="7fe87-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7fe87-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7fe87-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7fe87-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7fe87-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="7fe87-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7fe87-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7fe87-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7fe87-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7fe87-122">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="7fe87-122">End of client support</span></span><br/>    | <span data-ttu-id="7fe87-123">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7fe87-123">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="7fe87-124">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="7fe87-124">End of server support</span></span><br/>    | <span data-ttu-id="7fe87-125">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7fe87-125">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="7fe87-126">Header</span><span class="sxs-lookup"><span data-stu-id="7fe87-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fe87-127"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fe87-127"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fe87-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7fe87-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fe87-129">Remote Zugriffs Dienst (RAS) (Übersicht)</span><span class="sxs-lookup"><span data-stu-id="7fe87-129">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="7fe87-130">RAS-Server-Verwaltungsstrukturen</span><span class="sxs-lookup"><span data-stu-id="7fe87-130">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="7fe87-131">**Ergebnis der RAS- \_ PPP- \_ Projektion \_**</span><span class="sxs-lookup"><span data-stu-id="7fe87-131">**RAS\_PPP\_PROJECTION\_RESULT**</span></span>](ras-ppp-projection-result-str.md)
</dt> </dl>

 

 






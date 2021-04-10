---
title: RAS_PPP_NBFCP_RESULT Struktur (rassapi. h)
description: Die RAS- \_ PPP- \_ NBFCP- \_ Ergebnis Struktur wird verwendet, um das Ergebnis einer PPP-NetBEUI Framer (NBF)-Projektions Operation für einen Port zu melden.
ms.assetid: 670bf125-cad5-481f-89e4-858e636316bd
keywords:
- RAS_PPP_NBFCP_RESULT Struktur-RAS
topic_type:
- apiref
api_name:
- RAS_PPP_NBFCP_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddcb1cfe28a72e390cedbcc35fa299dddbfb8634
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104000"
---
# <a name="ras_ppp_nbfcp_result-structure"></a><span data-ttu-id="a8e94-104">RAS- \_ PPP- \_ NBF- \_ Ergebnis Struktur</span><span class="sxs-lookup"><span data-stu-id="a8e94-104">RAS\_PPP\_NBFCP\_RESULT structure</span></span>

<span data-ttu-id="a8e94-105">\[Die **RAS- \_ PPP- \_ NBS-Ergebnisstruktur \_** wird ab Windows Vista nicht unterstützt.\]</span><span class="sxs-lookup"><span data-stu-id="a8e94-105">\[The **RAS\_PPP\_NBFCP\_RESULT** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="a8e94-106">Die **RAS- \_ PPP- \_ NBFCP- \_ Ergebnis** Struktur wird verwendet, um das Ergebnis einer PPP-NetBEUI Framer (NBF)-Projektions Operation für einen Port zu melden.</span><span class="sxs-lookup"><span data-stu-id="a8e94-106">The **RAS\_PPP\_NBFCP\_RESULT** structure is used to report the result of a PPP NetBEUI Framer (NBF) projection operation for a port.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8e94-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8e94-107">Syntax</span></span>


```C++
typedef struct _RAS_PPP_NBFCP_RESULT {
  DWORD dwError;
  DWORD dwNetBiosError;
  CHAR  szName[NETBIOS_NAME_LEN + 1];
  WCHAR wszWksta[NETBIOS_NAME_LEN + 1];
} RAS_PPP_NBFCP_RESULT;
```



## <a name="members"></a><span data-ttu-id="a8e94-108">Member</span><span class="sxs-lookup"><span data-stu-id="a8e94-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="a8e94-109">**dwError**</span><span class="sxs-lookup"><span data-stu-id="a8e94-109">**dwError**</span></span>
</dt> <dd>

<span data-ttu-id="a8e94-110">Gibt die Ergebnisse der NBF-Projektions Operation an.</span><span class="sxs-lookup"><span data-stu-id="a8e94-110">Indicates the results of the NBF projection operation.</span></span> <span data-ttu-id="a8e94-111">Der Wert kein \_ Fehler weist auf einen Erfolg hin. in diesem Fall enthält das Element **wszwksta** den Namen des Remote Computers.</span><span class="sxs-lookup"><span data-stu-id="a8e94-111">A value of NO\_ERROR indicates success, in which case, the **wszWksta** member contains the name of the remote computer.</span></span> <span data-ttu-id="a8e94-112">Wenn der Projektions Vorgang nicht erfolgreich war, ist **dwError** ein Fehlercode aus "Winerror. h" oder "raserror. h".</span><span class="sxs-lookup"><span data-stu-id="a8e94-112">If the projection operation was not successful, **dwError** is an error code from Winerror.h or Raserror.h.</span></span>

</dd> <dt>

<span data-ttu-id="a8e94-113">**dwnetbioserror**</span><span class="sxs-lookup"><span data-stu-id="a8e94-113">**dwNetBiosError**</span></span>
</dt> <dd>

<span data-ttu-id="a8e94-114">Diesen Member auf dem Server ignorieren; Sie ist nur auf dem Client relevant.</span><span class="sxs-lookup"><span data-stu-id="a8e94-114">Ignore this member on the server; it is relevant only on the client.</span></span>

</dd> <dt>

<span data-ttu-id="a8e94-115">**szName**</span><span class="sxs-lookup"><span data-stu-id="a8e94-115">**szName**</span></span>
</dt> <dd>

<span data-ttu-id="a8e94-116">Diesen Member auf dem Server ignorieren; Sie ist nur auf dem Client relevant.</span><span class="sxs-lookup"><span data-stu-id="a8e94-116">Ignore this member on the server; it is relevant only on the client.</span></span>

</dd> <dt>

<span data-ttu-id="a8e94-117">**wszwksta**</span><span class="sxs-lookup"><span data-stu-id="a8e94-117">**wszWksta**</span></span>
</dt> <dd>

<span data-ttu-id="a8e94-118">Eine NULL-terminierte Unicode-Zeichenfolge, die den NetBIOS-Namen der RAS-Client Arbeitsstation angibt.</span><span class="sxs-lookup"><span data-stu-id="a8e94-118">A null-terminated Unicode string that specifies the NetBIOS name of the RAS client workstation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a8e94-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a8e94-119">Requirements</span></span>



| <span data-ttu-id="a8e94-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a8e94-120">Requirement</span></span> | <span data-ttu-id="a8e94-121">Wert</span><span class="sxs-lookup"><span data-stu-id="a8e94-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a8e94-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a8e94-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a8e94-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a8e94-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="a8e94-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a8e94-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a8e94-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a8e94-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a8e94-126">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="a8e94-126">End of client support</span></span><br/>    | <span data-ttu-id="a8e94-127">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a8e94-127">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="a8e94-128">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="a8e94-128">End of server support</span></span><br/>    | <span data-ttu-id="a8e94-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a8e94-129">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="a8e94-130">Header</span><span class="sxs-lookup"><span data-stu-id="a8e94-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8e94-131"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8e94-131"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8e94-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8e94-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8e94-133">Remote Zugriffs Dienst (RAS) (Übersicht)</span><span class="sxs-lookup"><span data-stu-id="a8e94-133">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="a8e94-134">RAS-Server-Verwaltungsstrukturen</span><span class="sxs-lookup"><span data-stu-id="a8e94-134">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="a8e94-135">**RAS- \_ Port \_ 1**</span><span class="sxs-lookup"><span data-stu-id="a8e94-135">**RAS\_PORT\_1**</span></span>](ras-port-1-str.md)
</dt> <dt>

[<span data-ttu-id="a8e94-136">**Ergebnis der RAS- \_ PPP- \_ Projektion \_**</span><span class="sxs-lookup"><span data-stu-id="a8e94-136">**RAS\_PPP\_PROJECTION\_RESULT**</span></span>](ras-ppp-projection-result-str.md)
</dt> <dt>

[<span data-ttu-id="a8e94-137">**Rasadminportgetinfo**</span><span class="sxs-lookup"><span data-stu-id="a8e94-137">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

 






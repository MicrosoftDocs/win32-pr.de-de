---
description: Definiert Werte, die bestimmen, wie die Anmelde Informationen eines Gruppen verwalteten Dienst Kontos (GMSA) abgerufen werden.
ms.assetid: 90891448-22F6-497A-A612-3DAB8622C325
title: CRED_FETCH-Enumeration (secpkg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRED_FETCH
api_type:
- HeaderDef
api_location:
- Secpkg.h
ms.openlocfilehash: 6a7c30f29826b017bc7a3badd796955ec31a1ca7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960258"
---
# <a name="cred_fetch-enumeration"></a><span data-ttu-id="6fa7f-103">Fed- \_ Fetch-Enumeration</span><span class="sxs-lookup"><span data-stu-id="6fa7f-103">CRED\_FETCH enumeration</span></span>

<span data-ttu-id="6fa7f-104">Definiert Werte, die bestimmen, wie die Anmelde Informationen eines Gruppen verwalteten Dienst Kontos (GMSA) abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="6fa7f-104">Defines values that determine how to fetch the credential of a Group Managed Service Account (gMSA).</span></span>

## <a name="syntax"></a><span data-ttu-id="6fa7f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6fa7f-105">Syntax</span></span>


```C++
typedef enum _CRED_FETCH { 
  CredFetchDefault  = 0,
  CredFetchDPAPI    = 1,
  CredFetchForced   = 2
} CRED_FETCH;
```



## <a name="constants"></a><span data-ttu-id="6fa7f-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="6fa7f-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6fa7f-107"><span id="CredFetchDefault"></span><span id="credfetchdefault"></span><span id="CREDFETCHDEFAULT"></span>**"Kredfetchdefault"**</span><span class="sxs-lookup"><span data-stu-id="6fa7f-107"><span id="CredFetchDefault"></span><span id="credfetchdefault"></span><span id="CREDFETCHDEFAULT"></span>**CredFetchDefault**</span></span>
</dt> <dd>

<span data-ttu-id="6fa7f-108">Gibt an, dass das Betriebssystem zuerst versuchen soll, das Kennwort aus dem lokalen Cache abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6fa7f-108">Signifies that the operating system should first attempt to retrieve the password from the local cache.</span></span> <span data-ttu-id="6fa7f-109">Wenn es an der Zeit ist, das Kennwort abzurufen, sollte das Betriebssystem eine Verbindung mit einem Domänen Controller für das Kennwort aufnehmen.</span><span class="sxs-lookup"><span data-stu-id="6fa7f-109">If it is time to fetch the password, then the operating system should contact a domain controller for the password.</span></span> <span data-ttu-id="6fa7f-110">Wenn dies nicht möglich ist, geben Sie alle zwischengespeicherten Kenn Wörter mit dem Statuswert Erfolg zurück.</span><span class="sxs-lookup"><span data-stu-id="6fa7f-110">If that fails, then return any cached passwords with the status value of success.</span></span>

</dd> <dt>

<span data-ttu-id="6fa7f-111"><span id="CredFetchDPAPI"></span><span id="credfetchdpapi"></span><span id="CREDFETCHDPAPI"></span>**"Kredfetchdpapi"**</span><span class="sxs-lookup"><span data-stu-id="6fa7f-111"><span id="CredFetchDPAPI"></span><span id="credfetchdpapi"></span><span id="CREDFETCHDPAPI"></span>**CredFetchDPAPI**</span></span>
</dt> <dd>

<span data-ttu-id="6fa7f-112">Gibt die lokalen DPAPI-Anmelde Informationen an den Aufrufer zurück.</span><span class="sxs-lookup"><span data-stu-id="6fa7f-112">Returns the local DPAPI credential to the caller.</span></span> <span data-ttu-id="6fa7f-113">SSPs ( [*Security Support Providers*](/windows/desktop/SecGloss/s-gly) ) erfordern im Allgemeinen nicht die Verwendung dieser Enumeration.</span><span class="sxs-lookup"><span data-stu-id="6fa7f-113">[*Security support providers*](/windows/desktop/SecGloss/s-gly) (SSPs) generally would not require the use of this enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="6fa7f-114"><span id="CredFetchForced"></span><span id="credfetchforced"></span><span id="CREDFETCHFORCED"></span>**"Kredfetchforced"**</span><span class="sxs-lookup"><span data-stu-id="6fa7f-114"><span id="CredFetchForced"></span><span id="credfetchforced"></span><span id="CREDFETCHFORCED"></span>**CredFetchForced**</span></span>
</dt> <dd>

<span data-ttu-id="6fa7f-115">Erzwingt, dass das Betriebssystem versucht, das Kennwort vom Domänen Controller zu lesen.</span><span class="sxs-lookup"><span data-stu-id="6fa7f-115">Forces the operating system to attempt to read the password from the domain controller.</span></span> <span data-ttu-id="6fa7f-116">Während der Kenn Wort rolloverzeit wurde das Kennwort möglicherweise auf dem Domänen Controller und anderen Mitglieds Hosts geändert, aber der GMSA-Mitglieds Host erkennt das Kennwort als noch gültig.</span><span class="sxs-lookup"><span data-stu-id="6fa7f-116">During the password rollover time, the password may have changed at the domain controller and other member hosts, but the gMSA member host recognizes the password as still valid.</span></span> <span data-ttu-id="6fa7f-117">Dies kann auf Probleme mit der Takt Abweichung zwischen verschiedenen Domänen Controllern zurückzuführen sein.</span><span class="sxs-lookup"><span data-stu-id="6fa7f-117">This can happen due to clock skew issues between different domain controllers.</span></span> <span data-ttu-id="6fa7f-118">Wenn dieser Wert angegeben ist, bestimmt das Betriebssystem, ob eine mögliche Kenn Wort Änderung aufgrund einer Zeit Abweichung möglich wäre, und ruft das Kennwort ab, wenn dies der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="6fa7f-118">When this value is specified, the operating system determines if there could be a possible password change due to clock skew, and if so, retrieves the password.</span></span> <span data-ttu-id="6fa7f-119">Andernfalls werden die zwischengespeicherten Anmelde Informationen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6fa7f-119">Otherwise, the cached credential is returned.</span></span> <span data-ttu-id="6fa7f-120">Wenn keine zwischengespeicherten Anmelde Informationen vorhanden sind, versucht das Betriebssystem, eine vom Domänen Controller zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6fa7f-120">If there is no cached credential, then the operating system attempts to get one from the domain controller.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6fa7f-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6fa7f-121">Requirements</span></span>



| <span data-ttu-id="6fa7f-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6fa7f-122">Requirement</span></span> | <span data-ttu-id="6fa7f-123">Wert</span><span class="sxs-lookup"><span data-stu-id="6fa7f-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6fa7f-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6fa7f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6fa7f-125">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6fa7f-125">Windows 8 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="6fa7f-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6fa7f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6fa7f-127">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6fa7f-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6fa7f-128">Header</span><span class="sxs-lookup"><span data-stu-id="6fa7f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fa7f-129"><dt>Secpkg. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fa7f-129"><dt>Secpkg.h</dt></span></span> </dl> |



 


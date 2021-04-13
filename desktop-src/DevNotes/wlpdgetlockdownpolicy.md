---
description: Ruft die Bibliothek auf, um den Sicherheitszustand relativ zum Host zu erhalten, und zu verwendetes Skript oder MSI.
ms.assetid: 4CCDA3B7-7661-47F6-A015-720BDEAEDBB1
title: Wldpgetlockdownpolicy-Funktion (wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpGetLockdownPolicy
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: a8f5e4da11e8ce7443d9a9bab323742cfc1b3a9d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523464"
---
# <a name="wldpgetlockdownpolicy-function"></a><span data-ttu-id="88611-103">Wldpgetlockdownpolicy-Funktion</span><span class="sxs-lookup"><span data-stu-id="88611-103">WldpGetLockdownPolicy function</span></span>

<span data-ttu-id="88611-104">Ruft die Bibliothek auf, um den Sicherheitszustand relativ zum Host zu erhalten, und zu verwendetes Skript oder MSI.</span><span class="sxs-lookup"><span data-stu-id="88611-104">Calls the library to get the security state relative to the host, and script or msi to be used.</span></span> <span data-ttu-id="88611-105">Die Funktion verfügt über keine zugeordnete Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="88611-105">The function has no associated import library.</span></span> <span data-ttu-id="88611-106">Sie müssen die LoadLibrary-Funktion und die GetProcAddress-Funktion verwenden, um dynamisch mit wldp.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="88611-106">You must use the LoadLibrary and GetProcAddress functions to dynamically link to wldp.dll.</span></span>

## <a name="syntax"></a><span data-ttu-id="88611-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="88611-107">Syntax</span></span>


```C++
HRESULT WINAPI WldpGetLockdownPolicy(
  _In_opt_ PWLDP_HOST_INFORMATION hostInformation,
  _Out_    PDWORD                 lockdownState,
  _In_     DWORD                  lockdownFlags
);
```



## <a name="parameters"></a><span data-ttu-id="88611-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="88611-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88611-109">*Hostinformationen* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="88611-109">*hostInformation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="88611-110">Eine [**wldp- \_ Host \_ Informations**](wldp-host-information.md) Struktur, die den zu bewertenden Host und die zu bewertende Quelldatei identifiziert.</span><span class="sxs-lookup"><span data-stu-id="88611-110">A [**WLDP\_HOST\_INFORMATION**](wldp-host-information.md) structure identifying the host and source file to be evaluated.</span></span>

</dd> <dt>

<span data-ttu-id="88611-111">*lockdownstate* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="88611-111">*lockdownState* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="88611-112">Stellt den resultierenden sicheren Richtlinien Wert bereit.</span><span class="sxs-lookup"><span data-stu-id="88611-112">Provides the resulting policy secure value.</span></span> <span data-ttu-id="88611-113">Sei! WLDP_LOCKDOWN_IS_OFF, dann ist die Option "mehr CI" aktiviert.</span><span class="sxs-lookup"><span data-stu-id="88611-113">If !WLDP_LOCKDOWN_IS_OFF, then UMCI is enabled.</span></span> <span data-ttu-id="88611-114">Sie können auch WLDP_LOCKDOWN_IS_AUDIT und WLDP_LOCKDOWN_IS_ENFORCE überprüfen, um festzustellen, ob eine Richtlinie im Überwachungs-oder Erzwingungs Modus ist.</span><span class="sxs-lookup"><span data-stu-id="88611-114">You can also check WLDP_LOCKDOWN_IS_AUDIT and WLDP_LOCKDOWN_IS_ENFORCE to determine if a policy is in audit or enforce mode.</span></span>
</dd> <dt>

<span data-ttu-id="88611-115">*LOCKDOWNFLAGS* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="88611-115">*lockdownFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88611-116">Die folgenden Flagwerte sind definiert: wldp- \_ Flags \_ skipsignaturevalidation 0x00000100 – Wenn festgelegt, überspringen Sie die Überprüfung von SaferIdentifyLevel, wodurch ignoriert wird, ob ein Skript signiert ist.</span><span class="sxs-lookup"><span data-stu-id="88611-116">The following flag values are defined WLDP\_FLAGS\_SKIPSIGNATUREVALIDATION 0x00000100 – when set, skip the SaferIdentifyLevel validation, which will ignore whether a script is signed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88611-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="88611-117">Return value</span></span>

<span data-ttu-id="88611-118">Diese Methode gibt \_ bei Erfolg S OK zurück oder andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="88611-118">This method returns S\_OK if successful or a failure code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="88611-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="88611-119">Remarks</span></span>

<span data-ttu-id="88611-120">Beim Aufruf mit wldp- \_ Host \_ Informationen. szsource = NULL wird die generische Richtlinie für den Host zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="88611-120">When called with WLDP\_HOST\_INFORMATION.szSource = NULL, the generic policy for the host is returned.</span></span>

<span data-ttu-id="88611-121">Beim Aufrufen mit wldp \_ \_ -Hostinformationen. dwhostid = wldp \_ Host- \_ ID \_ Global, wldp- \_ Host \_ Informationen. szsource muss NULL sein, und die Funktion gibt die globale System Richtlinie zurück.</span><span class="sxs-lookup"><span data-stu-id="88611-121">When called with WLDP\_HOST\_INFORMATION.dwHostId = WLDP\_HOST\_ID\_GLOBAL, WLDP\_HOST\_INFORMATION.szSource must be NULL, and the function will return the global system policy.</span></span>

<span data-ttu-id="88611-122">Das dwFlag wldp-Flag \_ \_ skipsignaturevalidation kann verwendet werden, um die SaferIdentifyLevel ()-Überprüfung zu überspringen. Dadurch wird ignoriert, ob ein Skript signiert ist.</span><span class="sxs-lookup"><span data-stu-id="88611-122">The dwFlag WLDP\_FLAGS\_SKIPSIGNATUREVALIDATION can be used to skip the SaferIdentifyLevel() validation, which will ignore whether a script is signed.</span></span>

## <a name="requirements"></a><span data-ttu-id="88611-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="88611-123">Requirements</span></span>



| <span data-ttu-id="88611-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="88611-124">Requirement</span></span> | <span data-ttu-id="88611-125">Wert</span><span class="sxs-lookup"><span data-stu-id="88611-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="88611-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="88611-126">Minimum supported client</span></span><br/> | <span data-ttu-id="88611-127">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="88611-127">Windows 10 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="88611-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="88611-128">Minimum supported server</span></span><br/> | <span data-ttu-id="88611-129">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="88611-129">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="88611-130">Header</span><span class="sxs-lookup"><span data-stu-id="88611-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="88611-131"><dt>Wldp. h</dt></span><span class="sxs-lookup"><span data-stu-id="88611-131"><dt>Wldp.h</dt></span></span> </dl>   |
| <span data-ttu-id="88611-132">DLL</span><span class="sxs-lookup"><span data-stu-id="88611-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88611-133"><dt>Wldp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88611-133"><dt>Wldp.dll</dt></span></span> </dl> |



 

 





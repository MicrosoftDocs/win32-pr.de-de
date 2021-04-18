---
description: Die GetOwnerSID&\# 8194; Die WMI-Klassenmethode Ruft die Sicherheits-ID (SID) für den Besitzer dieses Prozesses ab.
ms.assetid: f856b06c-8080-4145-a775-51361f741873
ms.tgt_platform: multiple
title: GetOwnerSID-Methode der Win32_Process-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.GetOwnerSid
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c3ed34d132d363c0ce9f83511459ec40f340a06c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344349"
---
# <a name="getownersid-method-of-the-win32_process-class"></a><span data-ttu-id="ec14c-103">GetOwnerSID-Methode der Win32- \_ Prozess Klasse</span><span class="sxs-lookup"><span data-stu-id="ec14c-103">GetOwnerSid method of the Win32\_Process class</span></span>

<span data-ttu-id="ec14c-104">Die Methode " **GetOwnerSID** [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) " Ruft die Sicherheits-ID (SID) für den Besitzer dieses Prozesses ab.</span><span class="sxs-lookup"><span data-stu-id="ec14c-104">The **GetOwnerSid** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method retrieves the security identifier (SID) for the owner of this process.</span></span>

<span data-ttu-id="ec14c-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="ec14c-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ec14c-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ec14c-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ec14c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec14c-107">Syntax</span></span>


```mof
uint32 GetOwnerSid(
  [out] string Sid
);
```



## <a name="parameters"></a><span data-ttu-id="ec14c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec14c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec14c-109">*Sid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ec14c-109">*Sid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ec14c-110">Gibt den sicherheitsbezeichnerdeskriptor für diesen Prozess zurück.</span><span class="sxs-lookup"><span data-stu-id="ec14c-110">Returns the security identifier descriptor for this process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec14c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ec14c-111">Return value</span></span>

<span data-ttu-id="ec14c-112">Gibt NULL (0) zurück, um den Erfolg anzugeben.</span><span class="sxs-lookup"><span data-stu-id="ec14c-112">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="ec14c-113">Jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="ec14c-113">Any other number indicates an error.</span></span> <span data-ttu-id="ec14c-114">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="ec14c-114">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="ec14c-115">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="ec14c-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="ec14c-116">**Erfolgreicher Abschluss** (0)</span><span class="sxs-lookup"><span data-stu-id="ec14c-116">**Successful completion** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ec14c-117">**Zugriff verweigert** (2)</span><span class="sxs-lookup"><span data-stu-id="ec14c-117">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ec14c-118">**Unzureichende Berechtigungen** (3)</span><span class="sxs-lookup"><span data-stu-id="ec14c-118">**Insufficient privilege** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ec14c-119">**Unbekannter Fehler** (8)</span><span class="sxs-lookup"><span data-stu-id="ec14c-119">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="ec14c-120">Der **Pfad wurde nicht gefunden** (9).</span><span class="sxs-lookup"><span data-stu-id="ec14c-120">**Path not found** (9)</span></span>
</dt> <dt>

<span data-ttu-id="ec14c-121">**Ungültiger Parameter** (21)</span><span class="sxs-lookup"><span data-stu-id="ec14c-121">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="ec14c-122">**Sonstige** (22 4294967295)</span><span class="sxs-lookup"><span data-stu-id="ec14c-122">**Other** (22 4294967295)</span></span>
</dt> </dl>

## <a name="examples"></a><span data-ttu-id="ec14c-123">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ec14c-123">Examples</span></span>

<span data-ttu-id="ec14c-124">Im PowerShell-Codebeispiel " [angemeldeter Benutzer auf einem Remote System/s Version 2-](https://Gallery.TechNet.Microsoft.Com/Find-the-logged-on-users-1161bd92) PowerShell-Code" werden Remote Computer abgefragt, um festzustellen, wer angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="ec14c-124">The [Find the logged on users on a remote system/s version 2](https://Gallery.TechNet.Microsoft.Com/Find-the-logged-on-users-1161bd92) PowerShell code example queries remote machines to see who is logged on.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec14c-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ec14c-125">Requirements</span></span>



| <span data-ttu-id="ec14c-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ec14c-126">Requirement</span></span> | <span data-ttu-id="ec14c-127">Wert</span><span class="sxs-lookup"><span data-stu-id="ec14c-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec14c-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ec14c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ec14c-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ec14c-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ec14c-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ec14c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ec14c-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ec14c-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ec14c-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="ec14c-132">Namespace</span></span><br/>                | <span data-ttu-id="ec14c-133">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ec14c-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ec14c-134">MOF</span><span class="sxs-lookup"><span data-stu-id="ec14c-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ec14c-135"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ec14c-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ec14c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="ec14c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec14c-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec14c-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec14c-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ec14c-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="ec14c-139">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ec14c-139">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ec14c-140">**Win32- \_ Prozess**</span><span class="sxs-lookup"><span data-stu-id="ec14c-140">**Win32\_Process**</span></span>](win32-process.md)
</dt> </dl>

 


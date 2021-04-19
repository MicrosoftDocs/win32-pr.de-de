---
description: Der SetDateTime-&\# 8194; WMI-Klassenmethode legt die aktuelle Systemzeit auf dem Computer fest.
ms.assetid: b9b86a52-c3d7-489d-8632-b297970dbeac
ms.tgt_platform: multiple
title: SetDateTime-Methode der Win32_OperatingSystem-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.SetDateTime
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 60316904d58ffec38aa912a1454082e7edfae5a8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346625"
---
# <a name="setdatetime-method-of-the-win32_operatingsystem-class"></a><span data-ttu-id="fb341-103">SetDateTime-Methode der Win32- \_ OperatingSystem-Klasse</span><span class="sxs-lookup"><span data-stu-id="fb341-103">SetDateTime method of the Win32\_OperatingSystem class</span></span>

<span data-ttu-id="fb341-104">Die [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode **SetDateTime** legt die aktuelle Systemzeit auf dem Computer fest.</span><span class="sxs-lookup"><span data-stu-id="fb341-104">The **SetDateTime** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method sets the current system time on the computer.</span></span>

<span data-ttu-id="fb341-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="fb341-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="fb341-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="fb341-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="fb341-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb341-107">Syntax</span></span>


```mof
uint32 SetDateTime(
  [in] datetime LocalDatetime
);
```



## <a name="parameters"></a><span data-ttu-id="fb341-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb341-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb341-109">*LocalDateTime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fb341-109">*LocalDatetime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb341-110">Der Wert der aktuellen Uhrzeit.</span><span class="sxs-lookup"><span data-stu-id="fb341-110">Value of the current time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb341-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fb341-111">Return value</span></span>

<span data-ttu-id="fb341-112">Gibt NULL (0) zurück, um den Erfolg anzugeben.</span><span class="sxs-lookup"><span data-stu-id="fb341-112">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="fb341-113">Jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="fb341-113">Any other number indicates an error.</span></span> <span data-ttu-id="fb341-114">Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="fb341-114">For error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="fb341-115">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="fb341-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="fb341-116">**Erfolg** (0)</span><span class="sxs-lookup"><span data-stu-id="fb341-116">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fb341-117">**Sonstige** (1 4294967295)</span><span class="sxs-lookup"><span data-stu-id="fb341-117">**Other** (1 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="fb341-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fb341-118">Remarks</span></span>

<span data-ttu-id="fb341-119">Der Aufrufprozess muss über die Berechtigung "SE \_ SYSTEMTIME Name" verfügen \_ .</span><span class="sxs-lookup"><span data-stu-id="fb341-119">The calling process must have the SE\_SYSTEMTIME\_NAME privilege.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb341-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fb341-120">Requirements</span></span>



| <span data-ttu-id="fb341-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fb341-121">Requirement</span></span> | <span data-ttu-id="fb341-122">Wert</span><span class="sxs-lookup"><span data-stu-id="fb341-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb341-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fb341-123">Minimum supported client</span></span><br/> | <span data-ttu-id="fb341-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fb341-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fb341-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fb341-125">Minimum supported server</span></span><br/> | <span data-ttu-id="fb341-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fb341-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fb341-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="fb341-127">Namespace</span></span><br/>                | <span data-ttu-id="fb341-128">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="fb341-128">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fb341-129">MOF</span><span class="sxs-lookup"><span data-stu-id="fb341-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fb341-130"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="fb341-130"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fb341-131">DLL</span><span class="sxs-lookup"><span data-stu-id="fb341-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb341-132"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb341-132"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb341-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb341-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="fb341-134">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fb341-134">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="fb341-135">**Win32- \_ OperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="fb341-135">**Win32\_OperatingSystem**</span></span>](win32-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="fb341-136">WMI-Tasks: Desktop Verwaltung</span><span class="sxs-lookup"><span data-stu-id="fb341-136">WMI Tasks: Desktop Management</span></span>](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> </dl>

 


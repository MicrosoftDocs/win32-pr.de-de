---
description: Der Lösch&\# 8194; WMI-Klassenmethode löscht einen geplanten Auftrag.
ms.assetid: 064ff3f8-6d41-4f8d-a511-6c051bb48a5b
ms.tgt_platform: multiple
title: Delete-Methode der Win32_ScheduledJob-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ScheduledJob.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: dd375c3da85bd72bddfc97ed3f57e52103578441
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127760"
---
# <a name="delete-method-of-the-win32_scheduledjob-class"></a><span data-ttu-id="5ebd4-103">Delete-Methode der Win32 \_ ScheduledJob-Klasse</span><span class="sxs-lookup"><span data-stu-id="5ebd4-103">Delete method of the Win32\_ScheduledJob class</span></span>

<span data-ttu-id="5ebd4-104">Die **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) -Methode löscht einen geplanten Auftrag.</span><span class="sxs-lookup"><span data-stu-id="5ebd4-104">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes a scheduled job.</span></span>

<span data-ttu-id="5ebd4-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="5ebd4-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="5ebd4-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="5ebd4-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="5ebd4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ebd4-107">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="5ebd4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ebd4-108">Parameters</span></span>

<span data-ttu-id="5ebd4-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="5ebd4-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5ebd4-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5ebd4-110">Return value</span></span>

<span data-ttu-id="5ebd4-111">Gibt bei Erfolg den Wert 0 (null) zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="5ebd4-111">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="5ebd4-112">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="5ebd4-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="5ebd4-113">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="5ebd4-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="5ebd4-114">**Erfolgreicher Abschluss**</span><span class="sxs-lookup"><span data-stu-id="5ebd4-114">**Successful completion**</span></span>
</dt> <dd>

<span data-ttu-id="5ebd4-115">0</span><span class="sxs-lookup"><span data-stu-id="5ebd4-115">0</span></span>

<span data-ttu-id="5ebd4-116">Die Anforderung wurde akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="5ebd4-116">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="5ebd4-117">**Nicht unterstützt**</span><span class="sxs-lookup"><span data-stu-id="5ebd4-117">**Not supported**</span></span>
</dt> <dd>

<span data-ttu-id="5ebd4-118">1</span><span class="sxs-lookup"><span data-stu-id="5ebd4-118">1</span></span>

<span data-ttu-id="5ebd4-119">Die Anforderung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5ebd4-119">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="5ebd4-120">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="5ebd4-120">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="5ebd4-121">2</span><span class="sxs-lookup"><span data-stu-id="5ebd4-121">2</span></span>

<span data-ttu-id="5ebd4-122">Der Benutzer verfügte nicht über die erforderlichen Zugriffsrechte.</span><span class="sxs-lookup"><span data-stu-id="5ebd4-122">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="5ebd4-123">**Unbekannter Fehler.**</span><span class="sxs-lookup"><span data-stu-id="5ebd4-123">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="5ebd4-124">8</span><span class="sxs-lookup"><span data-stu-id="5ebd4-124">8</span></span>

<span data-ttu-id="5ebd4-125">Interaktiver Prozess.</span><span class="sxs-lookup"><span data-stu-id="5ebd4-125">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="5ebd4-126">**Der Pfad wurde nicht gefunden**</span><span class="sxs-lookup"><span data-stu-id="5ebd4-126">**Path not found**</span></span>
</dt> <dd>

<span data-ttu-id="5ebd4-127">9</span><span class="sxs-lookup"><span data-stu-id="5ebd4-127">9</span></span>

<span data-ttu-id="5ebd4-128">Der Verzeichnispfad zur ausführbaren Dienst Datei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="5ebd4-128">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="5ebd4-129">**Ungültiger Parameter**</span><span class="sxs-lookup"><span data-stu-id="5ebd4-129">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="5ebd4-130">21</span><span class="sxs-lookup"><span data-stu-id="5ebd4-130">21</span></span>

<span data-ttu-id="5ebd4-131">An den Dienst wurden ungültige Parameter übermittelt.</span><span class="sxs-lookup"><span data-stu-id="5ebd4-131">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="5ebd4-132">**Dienst wurde nicht gestartet.**</span><span class="sxs-lookup"><span data-stu-id="5ebd4-132">**Service not started**</span></span>
</dt> <dd>

<span data-ttu-id="5ebd4-133">22</span><span class="sxs-lookup"><span data-stu-id="5ebd4-133">22</span></span>

<span data-ttu-id="5ebd4-134">Das Konto, unter dem dieser Dienst ausgeführt werden soll, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="5ebd4-134">The account which this service is to run under is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="5ebd4-135">**Andere**</span><span class="sxs-lookup"><span data-stu-id="5ebd4-135">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="5ebd4-136">23 4294967295</span><span class="sxs-lookup"><span data-stu-id="5ebd4-136">23 4294967295</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5ebd4-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ebd4-137">Requirements</span></span>



| <span data-ttu-id="5ebd4-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5ebd4-138">Requirement</span></span> | <span data-ttu-id="5ebd4-139">Wert</span><span class="sxs-lookup"><span data-stu-id="5ebd4-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ebd4-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5ebd4-140">Minimum supported client</span></span><br/> | <span data-ttu-id="5ebd4-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5ebd4-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5ebd4-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5ebd4-142">Minimum supported server</span></span><br/> | <span data-ttu-id="5ebd4-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5ebd4-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5ebd4-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="5ebd4-144">Namespace</span></span><br/>                | <span data-ttu-id="5ebd4-145">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5ebd4-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5ebd4-146">MOF</span><span class="sxs-lookup"><span data-stu-id="5ebd4-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5ebd4-147"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5ebd4-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5ebd4-148">DLL</span><span class="sxs-lookup"><span data-stu-id="5ebd4-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ebd4-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ebd4-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ebd4-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ebd4-150">See also</span></span>

<dl> <dt>

<span data-ttu-id="5ebd4-151">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5ebd4-151">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="5ebd4-152">**Win32 \_ ScheduledJob**</span><span class="sxs-lookup"><span data-stu-id="5ebd4-152">**Win32\_ScheduledJob**</span></span>](win32-scheduledjob.md)
</dt> </dl>

 


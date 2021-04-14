---
description: Ändert den Start Modus eines Win32- \_ systemtreiberdienstanbieter.
ms.assetid: 34f4e0ac-d8a0-4be7-8c84-0252e50db441
ms.tgt_platform: multiple
title: ChangeStartMode-Methode der Win32_SystemDriver-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.ChangeStartMode
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: edb6dfc9d745f5e408871246b581e6fab7eb72d3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523496"
---
# <a name="changestartmode-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="f38fc-103">ChangeStartMode-Methode der Win32 \_ systemdriver-Klasse</span><span class="sxs-lookup"><span data-stu-id="f38fc-103">ChangeStartMode method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="f38fc-104">Die [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode **ChangeStartMode** ändert den Start Modus eines [**Win32 \_ systemdriver**](win32-systemdriver.md) -Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="f38fc-104">The **ChangeStartMode** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies the start mode of a [**Win32\_SystemDriver**](win32-systemdriver.md) service.</span></span>

<span data-ttu-id="f38fc-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="f38fc-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f38fc-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f38fc-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f38fc-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f38fc-107">Syntax</span></span>


```mof
uint32 ChangeStartMode(
  [in] string StartMode = Auto Start
);
```



## <a name="parameters"></a><span data-ttu-id="f38fc-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f38fc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f38fc-109">*StartMode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f38fc-109">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f38fc-110">Der Start Modus des Windows-Basis Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="f38fc-110">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span data-ttu-id="f38fc-111"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Start Start** ("Start")</span><span class="sxs-lookup"><span data-stu-id="f38fc-111"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Boot Start** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="f38fc-112">Der Gerätetreiber wurde vom Betriebssystem Lader gestartet.</span><span class="sxs-lookup"><span data-stu-id="f38fc-112">Device driver started by the operating system loader.</span></span> <span data-ttu-id="f38fc-113">Dieses Wert ist nur für Treiberdienste gültig.</span><span class="sxs-lookup"><span data-stu-id="f38fc-113">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="f38fc-114"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")</span><span class="sxs-lookup"><span data-stu-id="f38fc-114"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="f38fc-115">Der Gerätetreiber wurde durch den Initialisierungs Prozess des Betriebssystems gestartet.</span><span class="sxs-lookup"><span data-stu-id="f38fc-115">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="f38fc-116">Dieses Wert ist nur für Treiberdienste gültig.</span><span class="sxs-lookup"><span data-stu-id="f38fc-116">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span data-ttu-id="f38fc-117"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>Automatischer **Start** ("automatisch")</span><span class="sxs-lookup"><span data-stu-id="f38fc-117"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Auto Start** ("Automatic")</span></span>


</dt> <dd>

<span data-ttu-id="f38fc-118">Der Dienst soll während des Systemstarts automatisch vom Dienstkontroll-Manager gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="f38fc-118">Service to be started automatically by the service control manager during system startup.</span></span>

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span data-ttu-id="f38fc-119"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Bedarfs Start** ("manuell")</span><span class="sxs-lookup"><span data-stu-id="f38fc-119"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Demand Start** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="f38fc-120">Der Dienst, der vom Dienststeuerungs-Manager gestartet werden soll, wenn ein Prozess die [**StartService**](startservice-method-in-class-win32-systemdriver.md) -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="f38fc-120">Service to be started by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-systemdriver.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="f38fc-121"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** ("deaktiviert")</span><span class="sxs-lookup"><span data-stu-id="f38fc-121"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="f38fc-122">Dienst, der nicht mehr gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f38fc-122">Service that can no longer be started.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f38fc-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f38fc-123">Return value</span></span>

<span data-ttu-id="f38fc-124">Gibt den Wert 0 (null) zurück, wenn der Dienst erfolgreich geändert wurde. der Wert ist 1 (eins), wenn die Anforderung nicht unterstützt wird, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="f38fc-124">Returns a value of 0 (zero) if the service was successfully modified, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="f38fc-125">**Erfolg** (0)</span><span class="sxs-lookup"><span data-stu-id="f38fc-125">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f38fc-126">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="f38fc-126">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f38fc-127">**Zugriff verweigert** (2)</span><span class="sxs-lookup"><span data-stu-id="f38fc-127">**Access Denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f38fc-128">**Abhängige Dienste werden ausgeführt** (3)</span><span class="sxs-lookup"><span data-stu-id="f38fc-128">**Dependent Services Running** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f38fc-129">**Ungültige Dienst Kontrolle** (4).</span><span class="sxs-lookup"><span data-stu-id="f38fc-129">**Invalid Service Control** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f38fc-130">Der **Dienst kann die Steuerung nicht akzeptieren** (5).</span><span class="sxs-lookup"><span data-stu-id="f38fc-130">**Service Cannot Accept Control** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f38fc-131">Der **Dienst ist nicht aktiv** (6).</span><span class="sxs-lookup"><span data-stu-id="f38fc-131">**Service Not Active** (6)</span></span>
</dt> <dt>

<span data-ttu-id="f38fc-132">**Timeout für Dienst Anforderungen** (7)</span><span class="sxs-lookup"><span data-stu-id="f38fc-132">**Service Request Timeout** (7)</span></span>
</dt> <dt>

<span data-ttu-id="f38fc-133">**Unbekannter Fehler** (8)</span><span class="sxs-lookup"><span data-stu-id="f38fc-133">**Unknown Failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="f38fc-134">Der **Pfad wurde nicht gefunden** (9).</span><span class="sxs-lookup"><span data-stu-id="f38fc-134">**Path Not Found** (9)</span></span>
</dt> <dt>

<span data-ttu-id="f38fc-135">Der **Dienst wird bereits ausgeführt** (10).</span><span class="sxs-lookup"><span data-stu-id="f38fc-135">**Service Already Running** (10)</span></span>
</dt> <dt>

<span data-ttu-id="f38fc-136">**Dienst Datenbank gesperrt** (11)</span><span class="sxs-lookup"><span data-stu-id="f38fc-136">**Service Database Locked** (11)</span></span>
</dt> <dt>

<span data-ttu-id="f38fc-137">**Dienst Abhängigkeit gelöscht** (12)</span><span class="sxs-lookup"><span data-stu-id="f38fc-137">**Service Dependency Deleted** (12)</span></span>
</dt> <dt>

<span data-ttu-id="f38fc-138">**Dienst Abhängigkeitsfehler** (13)</span><span class="sxs-lookup"><span data-stu-id="f38fc-138">**Service Dependency Failure** (13)</span></span>
</dt> <dt>

<span data-ttu-id="f38fc-139">**Dienst deaktiviert** (14)</span><span class="sxs-lookup"><span data-stu-id="f38fc-139">**Service Disabled** (14)</span></span>
</dt> <dt>

<span data-ttu-id="f38fc-140">Fehler bei der **Dienst Anmeldung** (15).</span><span class="sxs-lookup"><span data-stu-id="f38fc-140">**Service Logon Failed** (15)</span></span>
</dt> <dt>

<span data-ttu-id="f38fc-141">Der **Dienst wurde zum Löschen markiert** (16).</span><span class="sxs-lookup"><span data-stu-id="f38fc-141">**Service Marked For Deletion** (16)</span></span>
</dt> <dt>

<span data-ttu-id="f38fc-142">**Dienst ohne Thread** (17)</span><span class="sxs-lookup"><span data-stu-id="f38fc-142">**Service No Thread** (17)</span></span>
</dt> <dt>

<span data-ttu-id="f38fc-143">**Status zirkuläre Abhängigkeit** (18)</span><span class="sxs-lookup"><span data-stu-id="f38fc-143">**Status Circular Dependency** (18)</span></span>
</dt> <dt>

<span data-ttu-id="f38fc-144">**Doppelter Name des Status** (19)</span><span class="sxs-lookup"><span data-stu-id="f38fc-144">**Status Duplicate Name** (19)</span></span>
</dt> <dt>

<span data-ttu-id="f38fc-145">**Ungültiger Name** (20).</span><span class="sxs-lookup"><span data-stu-id="f38fc-145">**Status Invalid Name** (20)</span></span>
</dt> <dt>

<span data-ttu-id="f38fc-146">**Ungültiger Parameter** (21).</span><span class="sxs-lookup"><span data-stu-id="f38fc-146">**Status Invalid Parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="f38fc-147">**Ungültiges Dienst Konto** (22).</span><span class="sxs-lookup"><span data-stu-id="f38fc-147">**Status Invalid Service Account** (22)</span></span>
</dt> <dt>

<span data-ttu-id="f38fc-148">**Status Dienst vorhanden** (23)</span><span class="sxs-lookup"><span data-stu-id="f38fc-148">**Status Service Exists** (23)</span></span>
</dt> <dt>

<span data-ttu-id="f38fc-149">Der **Dienst wurde bereits angeh** alten (24).</span><span class="sxs-lookup"><span data-stu-id="f38fc-149">**Service Already Paused** (24)</span></span>
</dt> <dt>

<span data-ttu-id="f38fc-150">**Sonstige** (25 4294967295)</span><span class="sxs-lookup"><span data-stu-id="f38fc-150">**Other** (25 4294967295)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f38fc-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f38fc-151">Requirements</span></span>



| <span data-ttu-id="f38fc-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f38fc-152">Requirement</span></span> | <span data-ttu-id="f38fc-153">Wert</span><span class="sxs-lookup"><span data-stu-id="f38fc-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f38fc-154">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f38fc-154">Minimum supported client</span></span><br/> | <span data-ttu-id="f38fc-155">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f38fc-155">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f38fc-156">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f38fc-156">Minimum supported server</span></span><br/> | <span data-ttu-id="f38fc-157">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f38fc-157">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f38fc-158">Namespace</span><span class="sxs-lookup"><span data-stu-id="f38fc-158">Namespace</span></span><br/>                | <span data-ttu-id="f38fc-159">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f38fc-159">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f38fc-160">MOF</span><span class="sxs-lookup"><span data-stu-id="f38fc-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f38fc-161"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f38fc-161"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f38fc-162">DLL</span><span class="sxs-lookup"><span data-stu-id="f38fc-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f38fc-163"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f38fc-163"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f38fc-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f38fc-164">See also</span></span>

<dl> <dt>

<span data-ttu-id="f38fc-165">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f38fc-165">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f38fc-166">**Win32- \_ System Treiber**</span><span class="sxs-lookup"><span data-stu-id="f38fc-166">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> </dl>

 


---
description: Startet den Debugger, der derzeit für diesen Prozess registriert ist.
ms.assetid: 63c30db8-6117-4353-9132-4f39c72a6637
ms.tgt_platform: multiple
title: AttachDebugger-Methode der Win32_Process-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.AttachDebugger
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 041bdeeab634ebed5c7ec2eccffe01f7cecce709
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860768"
---
# <a name="attachdebugger-method-of-the-win32_process-class"></a><span data-ttu-id="12a93-103">AttachDebugger-Methode der Win32- \_ Prozess Klasse</span><span class="sxs-lookup"><span data-stu-id="12a93-103">AttachDebugger method of the Win32\_Process class</span></span>

<span data-ttu-id="12a93-104">Die [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode " **AttachDebugger** " startet den Debugger, der derzeit für diesen Prozess registriert ist.</span><span class="sxs-lookup"><span data-stu-id="12a93-104">The **AttachDebugger** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method starts the debugger that is currently registered for this process.</span></span>

<span data-ttu-id="12a93-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="12a93-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="12a93-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="12a93-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="12a93-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="12a93-107">Syntax</span></span>


```mof
uint32 AttachDebugger();
```



## <a name="parameters"></a><span data-ttu-id="12a93-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="12a93-108">Parameters</span></span>

<span data-ttu-id="12a93-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="12a93-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="12a93-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="12a93-110">Return value</span></span>

<span data-ttu-id="12a93-111">Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="12a93-111">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="12a93-112">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="12a93-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="12a93-113">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="12a93-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="12a93-114">**Erfolgreicher Abschluss**</span><span class="sxs-lookup"><span data-stu-id="12a93-114">**Successful completion**</span></span>
</dt> <dd>

<span data-ttu-id="12a93-115">0</span><span class="sxs-lookup"><span data-stu-id="12a93-115">0</span></span>

<span data-ttu-id="12a93-116">Erfolgreicher Abschluss.</span><span class="sxs-lookup"><span data-stu-id="12a93-116">Successful completion.</span></span>

</dd> <dt>

<span data-ttu-id="12a93-117">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="12a93-117">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="12a93-118">2</span><span class="sxs-lookup"><span data-stu-id="12a93-118">2</span></span>

<span data-ttu-id="12a93-119">Der Benutzer hat keinen Zugriff auf die angeforderten Informationen.</span><span class="sxs-lookup"><span data-stu-id="12a93-119">The user does not have access to the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="12a93-120">**Unzureichende Berechtigungen**</span><span class="sxs-lookup"><span data-stu-id="12a93-120">**Insufficient privilege**</span></span>
</dt> <dd>

<span data-ttu-id="12a93-121">3</span><span class="sxs-lookup"><span data-stu-id="12a93-121">3</span></span>

<span data-ttu-id="12a93-122">Der Benutzer verfügt nicht über ausreichende Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="12a93-122">The user does not have sufficient privilege.</span></span>

</dd> <dt>

<span data-ttu-id="12a93-123">**Unbekannter Fehler.**</span><span class="sxs-lookup"><span data-stu-id="12a93-123">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="12a93-124">8</span><span class="sxs-lookup"><span data-stu-id="12a93-124">8</span></span>

<span data-ttu-id="12a93-125">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="12a93-125">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="12a93-126">**Der Pfad wurde nicht gefunden**</span><span class="sxs-lookup"><span data-stu-id="12a93-126">**Path not found**</span></span>
</dt> <dd>

<span data-ttu-id="12a93-127">9</span><span class="sxs-lookup"><span data-stu-id="12a93-127">9</span></span>

<span data-ttu-id="12a93-128">Der angegebene Pfad ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="12a93-128">The path specified does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="12a93-129">**Ungültiger Parameter**</span><span class="sxs-lookup"><span data-stu-id="12a93-129">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="12a93-130">21</span><span class="sxs-lookup"><span data-stu-id="12a93-130">21</span></span>

<span data-ttu-id="12a93-131">Der angegebene Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="12a93-131">The specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="12a93-132">**Andere**</span><span class="sxs-lookup"><span data-stu-id="12a93-132">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="12a93-133">22 4294967295</span><span class="sxs-lookup"><span data-stu-id="12a93-133">22 4294967295</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="12a93-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="12a93-134">Requirements</span></span>



| <span data-ttu-id="12a93-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="12a93-135">Requirement</span></span> | <span data-ttu-id="12a93-136">Wert</span><span class="sxs-lookup"><span data-stu-id="12a93-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="12a93-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="12a93-137">Minimum supported client</span></span><br/> | <span data-ttu-id="12a93-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="12a93-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="12a93-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="12a93-139">Minimum supported server</span></span><br/> | <span data-ttu-id="12a93-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="12a93-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="12a93-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="12a93-141">Namespace</span></span><br/>                | <span data-ttu-id="12a93-142">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="12a93-142">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="12a93-143">MOF</span><span class="sxs-lookup"><span data-stu-id="12a93-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="12a93-144"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="12a93-144"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="12a93-145">DLL</span><span class="sxs-lookup"><span data-stu-id="12a93-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12a93-146"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12a93-146"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12a93-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="12a93-147">See also</span></span>

<dl> <dt>

<span data-ttu-id="12a93-148">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="12a93-148">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="12a93-149">**Win32- \_ Prozess**</span><span class="sxs-lookup"><span data-stu-id="12a93-149">**Win32\_Process**</span></span>](win32-process.md)
</dt> </dl>

 


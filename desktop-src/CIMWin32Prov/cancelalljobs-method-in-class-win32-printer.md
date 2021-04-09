---
description: Entfernt alle Aufträge, einschließlich der derzeit aus der Warteschlange druckbaren Aufträge.
ms.assetid: d7466513-b123-43af-ab17-b3213ba80284
ms.tgt_platform: multiple
title: Cancelalljobs-Methode der Win32_Printer-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.CancelAllJobs
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d2d816dab837aafd7b6e9c6beff75c4e62b19b2f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860767"
---
# <a name="cancelalljobs-method-of-the-win32_printer-class"></a><span data-ttu-id="461b8-103">Cancelalljobs-Methode der Win32- \_ Drucker Klasse</span><span class="sxs-lookup"><span data-stu-id="461b8-103">CancelAllJobs method of the Win32\_Printer class</span></span>

<span data-ttu-id="461b8-104">Die [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode **cancelalljobs** entfernt alle Aufträge, einschließlich der derzeit aus der Warteschlange druckbaren Aufträge.</span><span class="sxs-lookup"><span data-stu-id="461b8-104">The **CancelAllJobs** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method removes all jobs, including the one currently printing from the queue.</span></span>

<span data-ttu-id="461b8-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="461b8-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="461b8-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="461b8-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="461b8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="461b8-107">Syntax</span></span>


```mof
uint32 CancelAllJobs();
```



## <a name="parameters"></a><span data-ttu-id="461b8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="461b8-108">Parameters</span></span>

<span data-ttu-id="461b8-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="461b8-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="461b8-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="461b8-110">Return value</span></span>

<span data-ttu-id="461b8-111">Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="461b8-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="461b8-112">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="461b8-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="461b8-113">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="461b8-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="461b8-114">**0**</span><span class="sxs-lookup"><span data-stu-id="461b8-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="461b8-115">Erfolg</span><span class="sxs-lookup"><span data-stu-id="461b8-115">Success</span></span>

</dd> <dt>

<span data-ttu-id="461b8-116">**5**</span><span class="sxs-lookup"><span data-stu-id="461b8-116">**5**</span></span>
</dt> <dd>

<span data-ttu-id="461b8-117">Zugriff verweigert</span><span class="sxs-lookup"><span data-stu-id="461b8-117">Access Denied</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="461b8-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="461b8-118">Examples</span></span>

<span data-ttu-id="461b8-119">Die [Meldung Benutzer benachrichtigen, wenn eine Druck Warteschlange gelöscht wird](https://Gallery.TechNet.Microsoft.Com/9f8ad84e-239d-45bf-a14f-ad8f3fc4988a) verwendet Msg.exe, um eine Netzwerk Warnung an alle Benutzer zu senden, die Dokumente in einer Druck Warteschlange für den Löschvorgang verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="461b8-119">The [Notify Users When a Print Queue is Purged](https://Gallery.TechNet.Microsoft.Com/9f8ad84e-239d-45bf-a14f-ad8f3fc4988a) uses Msg.exe to send a network alert to any users who had documents in a print queue about to be purged.</span></span> <span data-ttu-id="461b8-120">Nach dem Senden der Warnungen löscht das Skript die Druck Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="461b8-120">After sending the alerts, the script purges the print queue.</span></span>

<span data-ttu-id="461b8-121">Das Codebeispiel [delete all Print Jobs](https://Gallery.TechNet.Microsoft.Com/0e89fa7c-a837-4607-b421-c870142e7323) VBScript löscht alle Druckaufträge auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="461b8-121">The [Delete all print jobs](https://Gallery.TechNet.Microsoft.Com/0e89fa7c-a837-4607-b421-c870142e7323) VBScript code sample deletes all print jobs on the local computer.</span></span>

<span data-ttu-id="461b8-122">Im folgenden VBScript-Beispiel werden alle Druckaufträge für einen Drucker mit dem Namen HP QuietJet gelöscht.</span><span class="sxs-lookup"><span data-stu-id="461b8-122">The following VBScript sample deletes all the print jobs for a printer named HP QuietJet.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colInstalledPrinters =  objWMIService.ExecQuery _ 
    ("Select * from Win32_Printer Where Name = 'HP QuietJet'") 
 
For Each objPrinter in colInstalledPrinters 
    objPrinter.CancelAllJobs() 
Next 
```



## <a name="requirements"></a><span data-ttu-id="461b8-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="461b8-123">Requirements</span></span>



| <span data-ttu-id="461b8-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="461b8-124">Requirement</span></span> | <span data-ttu-id="461b8-125">Wert</span><span class="sxs-lookup"><span data-stu-id="461b8-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="461b8-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="461b8-126">Minimum supported client</span></span><br/> | <span data-ttu-id="461b8-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="461b8-127">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="461b8-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="461b8-128">Minimum supported server</span></span><br/> | <span data-ttu-id="461b8-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="461b8-129">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="461b8-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="461b8-130">Namespace</span></span><br/>                | <span data-ttu-id="461b8-131">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="461b8-131">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="461b8-132">MOF</span><span class="sxs-lookup"><span data-stu-id="461b8-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="461b8-133"><dt>Win32 \_ Printer. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="461b8-133"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="461b8-134">DLL</span><span class="sxs-lookup"><span data-stu-id="461b8-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="461b8-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="461b8-135"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="461b8-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="461b8-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="461b8-137">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="461b8-137">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="461b8-138">**Win32- \_ Drucker**</span><span class="sxs-lookup"><span data-stu-id="461b8-138">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> </dl>

 


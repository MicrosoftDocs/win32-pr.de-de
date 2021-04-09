---
description: Die Methode zum Anhalten der WMI-Klasse hält einen Druckauftrag an.
ms.assetid: f1e3906f-1ca2-45c0-9863-5762e4e2119a
ms.tgt_platform: multiple
title: Pause-Methode der Win32_PrintJob-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrintJob.Pause
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 785ba54b56c65fd298b6ef763ec2d7eca0d8f61a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861748"
---
# <a name="pause-method-of-the-win32_printjob-class"></a><span data-ttu-id="fbbe9-103">Pause-Methode der Win32 \_ PrintJob-Klasse</span><span class="sxs-lookup"><span data-stu-id="fbbe9-103">Pause method of the Win32\_PrintJob class</span></span>

<span data-ttu-id="fbbe9-104">Die **Methode** zum Anhalten der [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) hält einen Druckauftrag an.</span><span class="sxs-lookup"><span data-stu-id="fbbe9-104">The **Pause** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method suspends a print job.</span></span>

<span data-ttu-id="fbbe9-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="fbbe9-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="fbbe9-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="fbbe9-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="fbbe9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="fbbe9-107">Syntax</span></span>


```mof
uint32 Pause();
```



## <a name="parameters"></a><span data-ttu-id="fbbe9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fbbe9-108">Parameters</span></span>

<span data-ttu-id="fbbe9-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="fbbe9-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fbbe9-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fbbe9-110">Return value</span></span>

<span data-ttu-id="fbbe9-111">Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="fbbe9-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="fbbe9-112">**0**</span><span class="sxs-lookup"><span data-stu-id="fbbe9-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="fbbe9-113">Erfolg</span><span class="sxs-lookup"><span data-stu-id="fbbe9-113">Success</span></span>

</dd> <dt>

<span data-ttu-id="fbbe9-114">**5**</span><span class="sxs-lookup"><span data-stu-id="fbbe9-114">**5**</span></span>
</dt> <dd>

<span data-ttu-id="fbbe9-115">Zugriff verweigert</span><span class="sxs-lookup"><span data-stu-id="fbbe9-115">Access Denied</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="fbbe9-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fbbe9-116">Examples</span></span>

<span data-ttu-id="fbbe9-117">Das VBScript-Codebeispiel " [alle Drucker mit leeren Druck Warteschlangen](https://Gallery.TechNet.Microsoft.Com/cf2b6b61-8ffe-444b-857b-e3a205bc693c) anhalten" hält alle Drucker an, für die keine ausstehenden Druckaufträge vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="fbbe9-117">The [Pause All Printers with Empty Print Queues](https://Gallery.TechNet.Microsoft.Com/cf2b6b61-8ffe-444b-857b-e3a205bc693c) VBScript code sample pauses any printers that have no pending print jobs.</span></span>

<span data-ttu-id="fbbe9-118">Im folgenden VBScript-Codebeispiel werden alle Druckaufträge auf einem Druckserver angehalten.</span><span class="sxs-lookup"><span data-stu-id="fbbe9-118">The following VBScript code sample pauses all the print jobs on a print server.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colPrintJobs =  objWMIService.ExecQuery _ 
    ("Select * from Win32_PrintJob") 
 
For Each objPrintJob in colPrintJobs  
    objPrintJob.Pause 
Next 
```



## <a name="requirements"></a><span data-ttu-id="fbbe9-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fbbe9-119">Requirements</span></span>



| <span data-ttu-id="fbbe9-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fbbe9-120">Requirement</span></span> | <span data-ttu-id="fbbe9-121">Wert</span><span class="sxs-lookup"><span data-stu-id="fbbe9-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbbe9-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fbbe9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="fbbe9-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fbbe9-123">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="fbbe9-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fbbe9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="fbbe9-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fbbe9-125">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="fbbe9-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="fbbe9-126">Namespace</span></span><br/>                | <span data-ttu-id="fbbe9-127">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="fbbe9-127">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="fbbe9-128">MOF</span><span class="sxs-lookup"><span data-stu-id="fbbe9-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fbbe9-129"><dt>Win32 \_ Printer. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="fbbe9-129"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="fbbe9-130">DLL</span><span class="sxs-lookup"><span data-stu-id="fbbe9-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fbbe9-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fbbe9-131"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="fbbe9-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fbbe9-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbbe9-133">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="fbbe9-133">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="fbbe9-134">**Win32- \_ PrintJob**</span><span class="sxs-lookup"><span data-stu-id="fbbe9-134">**Win32\_PrintJob**</span></span>](win32-printjob.md)
</dt> </dl>

 


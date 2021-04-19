---
description: Die Methode Resume WMI class setzt einen angehaltenen Druckauftrag fort.
ms.assetid: acfbca2b-19af-4339-bbca-834db50c3d8d
ms.tgt_platform: multiple
title: Resume-Methode der Win32_PrintJob-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrintJob.Resume
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f8ca1602eb29e1e18d83d2e8b79760d13f63e101
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106338891"
---
# <a name="resume-method-of-the-win32_printjob-class"></a><span data-ttu-id="67f70-103">Resume-Methode der Win32 \_ PrintJob-Klasse</span><span class="sxs-lookup"><span data-stu-id="67f70-103">Resume method of the Win32\_PrintJob class</span></span>

<span data-ttu-id="67f70-104">Die Methode **Resume** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) setzt einen angehaltenen Druckauftrag fort.</span><span class="sxs-lookup"><span data-stu-id="67f70-104">The **Resume** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method continues a paused print job.</span></span>

<span data-ttu-id="67f70-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="67f70-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="67f70-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="67f70-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="67f70-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="67f70-107">Syntax</span></span>


```mof
uint32 Resume();
```



## <a name="parameters"></a><span data-ttu-id="67f70-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="67f70-108">Parameters</span></span>

<span data-ttu-id="67f70-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="67f70-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="67f70-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="67f70-110">Return value</span></span>

<span data-ttu-id="67f70-111">Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="67f70-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="67f70-112">**0**</span><span class="sxs-lookup"><span data-stu-id="67f70-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="67f70-113">Erfolg</span><span class="sxs-lookup"><span data-stu-id="67f70-113">Success</span></span>

</dd> <dt>

<span data-ttu-id="67f70-114">**5**</span><span class="sxs-lookup"><span data-stu-id="67f70-114">**5**</span></span>
</dt> <dd>

<span data-ttu-id="67f70-115">Zugriff verweigert</span><span class="sxs-lookup"><span data-stu-id="67f70-115">Access Denied</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="67f70-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="67f70-116">Examples</span></span>

<span data-ttu-id="67f70-117">Im folgenden VBScript-Codebeispiel werden alle Druckaufträge auf einem Computer fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="67f70-117">The following VBScript code sample resumes all the print jobs on a computer.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colPrintJobs =  objWMIService.ExecQuery _ 
    ("Select * from Win32_PrintJob") 
 
For Each objPrintJob in colPrintJobs  
    objPrintJob.Resume 
Next 
```



## <a name="requirements"></a><span data-ttu-id="67f70-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="67f70-118">Requirements</span></span>



| <span data-ttu-id="67f70-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="67f70-119">Requirement</span></span> | <span data-ttu-id="67f70-120">Wert</span><span class="sxs-lookup"><span data-stu-id="67f70-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="67f70-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="67f70-121">Minimum supported client</span></span><br/> | <span data-ttu-id="67f70-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="67f70-122">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="67f70-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="67f70-123">Minimum supported server</span></span><br/> | <span data-ttu-id="67f70-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="67f70-124">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="67f70-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="67f70-125">Namespace</span></span><br/>                | <span data-ttu-id="67f70-126">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="67f70-126">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="67f70-127">MOF</span><span class="sxs-lookup"><span data-stu-id="67f70-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="67f70-128"><dt>Win32 \_ Printer. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="67f70-128"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="67f70-129">DLL</span><span class="sxs-lookup"><span data-stu-id="67f70-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67f70-130"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67f70-130"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="67f70-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="67f70-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67f70-132">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="67f70-132">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="67f70-133">**Win32- \_ PrintJob**</span><span class="sxs-lookup"><span data-stu-id="67f70-133">**Win32\_PrintJob**</span></span>](win32-printjob.md)
</dt> </dl>

 


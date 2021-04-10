---
description: Benennt einen Drucker um.
ms.assetid: afbef871-5153-4b9e-9ad3-4d271a497c37
ms.tgt_platform: multiple
title: Renameprinter-Methode der Win32_Printer-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.RenamePrinter
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6066dfd4280f7c43c9804933fb1ed5fb931bfa08
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214025"
---
# <a name="renameprinter-method-of-the-win32_printer-class"></a><span data-ttu-id="10373-103">Renameprinter-Methode der Win32- \_ Drucker Klasse</span><span class="sxs-lookup"><span data-stu-id="10373-103">RenamePrinter method of the Win32\_Printer class</span></span>

<span data-ttu-id="10373-104">Die [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode **renameprinter** benennt einen Drucker um.</span><span class="sxs-lookup"><span data-stu-id="10373-104">The **RenamePrinter** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method renames a printer.</span></span>

<span data-ttu-id="10373-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="10373-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="10373-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="10373-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="10373-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="10373-107">Syntax</span></span>


```mof
uint32 RenamePrinter(
  [in] string NewPrinterName
);
```



## <a name="parameters"></a><span data-ttu-id="10373-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="10373-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10373-109">*NewPrinterName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="10373-109">*NewPrinterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10373-110">Neuer Druckername.</span><span class="sxs-lookup"><span data-stu-id="10373-110">New printer name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10373-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="10373-111">Return value</span></span>

<span data-ttu-id="10373-112">Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="10373-112">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="10373-113">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="10373-113">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="10373-114">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="10373-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="10373-115">**0**</span><span class="sxs-lookup"><span data-stu-id="10373-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="10373-116">Erfolg</span><span class="sxs-lookup"><span data-stu-id="10373-116">Success</span></span>

</dd> <dt>

<span data-ttu-id="10373-117">**5**</span><span class="sxs-lookup"><span data-stu-id="10373-117">**5**</span></span>
</dt> <dd>

<span data-ttu-id="10373-118">Zugriff verweigert</span><span class="sxs-lookup"><span data-stu-id="10373-118">Access Denied</span></span>

</dd> <dt>

<span data-ttu-id="10373-119">**1801**</span><span class="sxs-lookup"><span data-stu-id="10373-119">**1801**</span></span>
</dt> <dd>

<span data-ttu-id="10373-120">Ungültiger Drucker Name</span><span class="sxs-lookup"><span data-stu-id="10373-120">Invalid Printer Name</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="10373-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="10373-121">Examples</span></span>

<span data-ttu-id="10373-122">Das folgende VBScript-Beispiel benennt sowohl einen Drucker als auch den Druckerfreigabe Namen um.</span><span class="sxs-lookup"><span data-stu-id="10373-122">The following VBScript example renames both a printer and its printer share name.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colPrinters =  objWMIService.ExecQuery _ 
    ("Select * from Win32_Printer Where DeviceID = 'HP LaserJet 4Si M'") 
 
For Each objPrinter in colPrinters 
    objPrinter.RenamePrinter("ArtDepartmentPrinter") 
Next 
 
Set colPrinters = objWMIService.ExecQuery _ 
    ("Select * From Win32_Printer Where DeviceID = 'ArtDepartmentPrinter' ") 
 
For Each objPrinter in colPrinters 
    objPrinter.ShareName = "ArtDepartmentPrinter" 
    objPrinter.Put_ 
Next 
```



## <a name="requirements"></a><span data-ttu-id="10373-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="10373-123">Requirements</span></span>



| <span data-ttu-id="10373-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="10373-124">Requirement</span></span> | <span data-ttu-id="10373-125">Wert</span><span class="sxs-lookup"><span data-stu-id="10373-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="10373-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="10373-126">Minimum supported client</span></span><br/> | <span data-ttu-id="10373-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="10373-127">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="10373-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="10373-128">Minimum supported server</span></span><br/> | <span data-ttu-id="10373-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="10373-129">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="10373-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="10373-130">Namespace</span></span><br/>                | <span data-ttu-id="10373-131">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="10373-131">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="10373-132">MOF</span><span class="sxs-lookup"><span data-stu-id="10373-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="10373-133"><dt>Win32 \_ Printer. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="10373-133"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="10373-134">DLL</span><span class="sxs-lookup"><span data-stu-id="10373-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10373-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10373-135"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="10373-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="10373-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10373-137">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="10373-137">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="10373-138">**Win32- \_ Drucker**</span><span class="sxs-lookup"><span data-stu-id="10373-138">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> </dl>

 


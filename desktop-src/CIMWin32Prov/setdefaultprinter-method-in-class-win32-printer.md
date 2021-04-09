---
description: Die WMI-Klassenmethode SetDefaultPrinter legt den Standardsystem Drucker für den Benutzer fest, der die-Methode aufruft.
ms.assetid: 7e896961-363d-4b8b-9d22-bbfc9681e97b
ms.tgt_platform: multiple
title: SetDefaultPrinter-Methode der Win32_Printer-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.SetDefaultPrinter
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a18c6d7771eb0e95d86142f41262d721509eb6f8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861739"
---
# <a name="setdefaultprinter-method-of-the-win32_printer-class"></a><span data-ttu-id="5ea5a-103">SetDefaultPrinter-Methode der Win32- \_ Drucker Klasse</span><span class="sxs-lookup"><span data-stu-id="5ea5a-103">SetDefaultPrinter method of the Win32\_Printer class</span></span>

<span data-ttu-id="5ea5a-104">Die [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode **SetDefaultPrinter** legt den Standardsystem Drucker für den Benutzer fest, der die-Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="5ea5a-104">The **SetDefaultPrinter** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method sets the default system printer for the user calling the method.</span></span>

<span data-ttu-id="5ea5a-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="5ea5a-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="5ea5a-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="5ea5a-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="5ea5a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ea5a-107">Syntax</span></span>


```mof
uint32 SetDefaultPrinter();
```



## <a name="parameters"></a><span data-ttu-id="5ea5a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ea5a-108">Parameters</span></span>

<span data-ttu-id="5ea5a-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="5ea5a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5ea5a-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5ea5a-110">Return value</span></span>

<span data-ttu-id="5ea5a-111">Gibt bei Erfolg 0 (null) und einen anderen Wert zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="5ea5a-111">Returns 0 (zero) if successful, and some other value if an error occurs.</span></span> <span data-ttu-id="5ea5a-112">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="5ea5a-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="5ea5a-113">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="5ea5a-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

## <a name="examples"></a><span data-ttu-id="5ea5a-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5ea5a-114">Examples</span></span>

<span data-ttu-id="5ea5a-115">Im Beispiel [Installieren eines TCP/IP-Drucker Ports und eines Druckers](https://Gallery.TechNet.Microsoft.Com/41a4c996-b7f7-4d58-808d-2acac20ddbf7) VBScript wird ein TCP/IP-Druckerport installiert, ein Drucker installiert und der Drucker als Standardwert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5ea5a-115">The [Install a TCP/IP Printer Port and Printer](https://Gallery.TechNet.Microsoft.Com/41a4c996-b7f7-4d58-808d-2acac20ddbf7) VBScript sample installs a TCP/IP printer port, installs a printer, and then sets the printer to be default.</span></span>

<span data-ttu-id="5ea5a-116">Im folgenden VBScript-Codebeispiel wird der Standarddrucker auf einem Computer festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5ea5a-116">The following VBScript code sample sets the default printer on a computer.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colInstalledPrinters =  objWMIService.ExecQuery _ 
    ("Select * from Win32_Printer Where Name = 'ScriptedPrinter'") 
 
For Each objPrinter in colInstalledPrinters 
    objPrinter.SetDefaultPrinter() 
Next 
```



## <a name="requirements"></a><span data-ttu-id="5ea5a-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ea5a-117">Requirements</span></span>



| <span data-ttu-id="5ea5a-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5ea5a-118">Requirement</span></span> | <span data-ttu-id="5ea5a-119">Wert</span><span class="sxs-lookup"><span data-stu-id="5ea5a-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea5a-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5ea5a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5ea5a-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5ea5a-121">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="5ea5a-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5ea5a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5ea5a-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5ea5a-123">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="5ea5a-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="5ea5a-124">Namespace</span></span><br/>                | <span data-ttu-id="5ea5a-125">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5ea5a-125">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="5ea5a-126">MOF</span><span class="sxs-lookup"><span data-stu-id="5ea5a-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5ea5a-127"><dt>Win32 \_ Printer. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5ea5a-127"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="5ea5a-128">DLL</span><span class="sxs-lookup"><span data-stu-id="5ea5a-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ea5a-129"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ea5a-129"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="5ea5a-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ea5a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ea5a-131">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="5ea5a-131">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="5ea5a-132">WMI-Tasks: Drucker und Drucken</span><span class="sxs-lookup"><span data-stu-id="5ea5a-132">WMI Tasks: Printers and Printing</span></span>](/windows/desktop/WmiSdk/wmi-tasks--printers-and-printing)
</dt> <dt>

[<span data-ttu-id="5ea5a-133">**Win32- \_ Drucker**</span><span class="sxs-lookup"><span data-stu-id="5ea5a-133">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> </dl>

 


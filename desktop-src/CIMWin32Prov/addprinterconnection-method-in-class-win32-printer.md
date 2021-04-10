---
description: Stellt eine Verbindung mit einem vorhandenen Drucker im Netzwerk her und fügt ihn der Liste der verfügbaren Drucker hinzu.
ms.assetid: 44149051-4abf-4428-8999-355dd0b0ce69
ms.tgt_platform: multiple
title: AddPrinterConnection-Methode der Win32_Printer-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.AddPrinterConnection
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e2ad9e225a60e33fdf51d5f677dd4342acd148b3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860772"
---
# <a name="addprinterconnection-method-of-the-win32_printer-class"></a><span data-ttu-id="96ba1-103">AddPrinterConnection-Methode der Win32- \_ Drucker Klasse</span><span class="sxs-lookup"><span data-stu-id="96ba1-103">AddPrinterConnection method of the Win32\_Printer class</span></span>

<span data-ttu-id="96ba1-104">Die [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode **addprconnection** stellt eine Verbindung mit einem vorhandenen Drucker im Netzwerk her und fügt Sie der Liste der verfügbaren Drucker hinzu.</span><span class="sxs-lookup"><span data-stu-id="96ba1-104">The **AddPrinterConnection** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method provides a connection to an existing printer on the network, and adds it to the list of available printers.</span></span>

<span data-ttu-id="96ba1-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="96ba1-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="96ba1-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="96ba1-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="96ba1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="96ba1-107">Syntax</span></span>


```mof
uint32 AddPrinterConnection(
  [in] string Name
);
```



## <a name="parameters"></a><span data-ttu-id="96ba1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="96ba1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96ba1-109">*Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="96ba1-109">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96ba1-110">Anzeige Name für den Drucker.</span><span class="sxs-lookup"><span data-stu-id="96ba1-110">Friendly name for the printer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96ba1-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="96ba1-111">Return value</span></span>

<span data-ttu-id="96ba1-112">Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="96ba1-112">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="96ba1-113">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="96ba1-113">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="96ba1-114">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="96ba1-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="96ba1-115">**0**</span><span class="sxs-lookup"><span data-stu-id="96ba1-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="96ba1-116">Erfolg</span><span class="sxs-lookup"><span data-stu-id="96ba1-116">Success</span></span>

</dd> <dt>

<span data-ttu-id="96ba1-117">**5**</span><span class="sxs-lookup"><span data-stu-id="96ba1-117">**5**</span></span>
</dt> <dd>

<span data-ttu-id="96ba1-118">Zugriff verweigert</span><span class="sxs-lookup"><span data-stu-id="96ba1-118">Access Denied</span></span>

</dd> <dt>

<span data-ttu-id="96ba1-119">**1801**</span><span class="sxs-lookup"><span data-stu-id="96ba1-119">**1801**</span></span>
</dt> <dd>

<span data-ttu-id="96ba1-120">Ungültiger Drucker Name</span><span class="sxs-lookup"><span data-stu-id="96ba1-120">Invalid Printer Name</span></span>

</dd> <dt>

<span data-ttu-id="96ba1-121">**1930**</span><span class="sxs-lookup"><span data-stu-id="96ba1-121">**1930**</span></span>
</dt> <dd>

<span data-ttu-id="96ba1-122">Nicht kompatibler Druckertreiber</span><span class="sxs-lookup"><span data-stu-id="96ba1-122">Incompatible Printer Driver</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="96ba1-123">Beispiele</span><span class="sxs-lookup"><span data-stu-id="96ba1-123">Examples</span></span>

<span data-ttu-id="96ba1-124">Mit dem PowerShell [-Beispiel Add-PrinterDriver](https://Gallery.TechNet.Microsoft.Com/1c8f4c0d-9439-4af0-8840-59686d9b4bc1) werden alle Druckertreiber von einem angegebenen Drucker Server installiert.</span><span class="sxs-lookup"><span data-stu-id="96ba1-124">The [Add-PrinterDriver](https://Gallery.TechNet.Microsoft.Com/1c8f4c0d-9439-4af0-8840-59686d9b4bc1) PowerShell sample installs all printer drivers from a specified print server.</span></span>

<span data-ttu-id="96ba1-125">Das [ListSharedPrintersAddPrintConnection.ps1](https://Gallery.TechNet.Microsoft.Com/b7f74333-e78b-49d8-b23a-f1307d5b1ee6) PowerShell-Beispiel listet freigegebene Drucker in einem remotecomptuer auf und bietet Ihnen die Möglichkeit, dem Computer eine Druckerverbindung vom Remote Computer hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="96ba1-125">The [ListSharedPrintersAddPrintConnection.ps1](https://Gallery.TechNet.Microsoft.Com/b7f74333-e78b-49d8-b23a-f1307d5b1ee6) PowerShell sample lists shared printers on a remote comptuer, and gives you the ability to add a printer connection from the remote computer to your computer.</span></span>

<span data-ttu-id="96ba1-126">Im folgenden VBScript-Codebeispiel wird ein lokaler Drucker hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="96ba1-126">The following VBScript code sample adds a local printer.</span></span>


```VB
Dim strPrinterName as String = "Isidoros Printer"
Dim strComputer AsString = My.Computer.Name
Dim objWMIService, objPrinter AsObject
objWMIService = GetObject(
"winmgmts:" _

& 
"{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

objPrinter = objWMIService.Get(
"Win32_Printer").SpawnInstance_
objPrinter.Name = strPrinterName
objPrinter.DriverName = "Generic / Text Only"
objPrinter.PortName = 
"c:\temp\file.prn"
objPrinter.DeviceID = strPrinterName
'objPrinter.Location = "Athens, Greece"
objPrinter.Network = 
False
objPrinter.Shared = 
False'objPrinter.ShareName = "MyShareName"
objPrinter.Put_()
```



## <a name="requirements"></a><span data-ttu-id="96ba1-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="96ba1-127">Requirements</span></span>



| <span data-ttu-id="96ba1-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="96ba1-128">Requirement</span></span> | <span data-ttu-id="96ba1-129">Wert</span><span class="sxs-lookup"><span data-stu-id="96ba1-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="96ba1-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="96ba1-130">Minimum supported client</span></span><br/> | <span data-ttu-id="96ba1-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="96ba1-131">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="96ba1-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="96ba1-132">Minimum supported server</span></span><br/> | <span data-ttu-id="96ba1-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="96ba1-133">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="96ba1-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="96ba1-134">Namespace</span></span><br/>                | <span data-ttu-id="96ba1-135">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="96ba1-135">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="96ba1-136">MOF</span><span class="sxs-lookup"><span data-stu-id="96ba1-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="96ba1-137"><dt>Win32 \_ Printer. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="96ba1-137"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="96ba1-138">DLL</span><span class="sxs-lookup"><span data-stu-id="96ba1-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96ba1-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96ba1-139"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="96ba1-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="96ba1-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96ba1-141">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="96ba1-141">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="96ba1-142">WMI-Tasks: Drucker und Drucken</span><span class="sxs-lookup"><span data-stu-id="96ba1-142">WMI Tasks: Printers and Printing</span></span>](/windows/desktop/WmiSdk/wmi-tasks--printers-and-printing)
</dt> <dt>

[<span data-ttu-id="96ba1-143">**Win32- \_ Drucker**</span><span class="sxs-lookup"><span data-stu-id="96ba1-143">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> </dl>

 


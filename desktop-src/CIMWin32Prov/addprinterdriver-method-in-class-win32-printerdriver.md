---
description: Erstellt einen neuen Druckertreiber.
ms.assetid: 23d9ec50-235a-4bf8-ab6b-be3509c3869f
ms.tgt_platform: multiple
title: Addprinterdriver-Methode der Win32_PrinterDriver-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriver.AddPrinterDriver
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 03c029d7689743150235d20b0658cd154ef64a4c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104392966"
---
# <a name="addprinterdriver-method-of-the-win32_printerdriver-class"></a><span data-ttu-id="37b7d-103">Addprinterdriver-Methode der Win32 \_ PrinterDriver-Klasse</span><span class="sxs-lookup"><span data-stu-id="37b7d-103">AddPrinterDriver method of the Win32\_PrinterDriver class</span></span>

<span data-ttu-id="37b7d-104">Die **addprinterdriver** -Klassenmethode erstellt einen neuen Druckertreiber.</span><span class="sxs-lookup"><span data-stu-id="37b7d-104">The **AddPrinterDriver** class method creates a new printer driver.</span></span>

<span data-ttu-id="37b7d-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="37b7d-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="37b7d-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="37b7d-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="37b7d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="37b7d-107">Syntax</span></span>


```mof
uint32 AddPrinterDriver(
  [in] Win32_PrinterDriver DriverInfo
);
```



## <a name="parameters"></a><span data-ttu-id="37b7d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="37b7d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37b7d-109">*DriverInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="37b7d-109">*DriverInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37b7d-110">Eine Instanz der Win32-Klasse " [**\_ PrinterDriver**](win32-printerdriver.md) ", die den Druckertreiber darstellt.</span><span class="sxs-lookup"><span data-stu-id="37b7d-110">An instance of the [**Win32\_PrinterDriver**](win32-printerdriver.md) class that represents the printer driver.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37b7d-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="37b7d-111">Return value</span></span>

<span data-ttu-id="37b7d-112">Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="37b7d-112">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="37b7d-113">Werte, die sich von den in der folgenden Liste aufgeführten Werten unterscheiden, finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants).</span><span class="sxs-lookup"><span data-stu-id="37b7d-113">For values different from those listed in the following list, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants).</span></span>

<dl> <dt>

<span data-ttu-id="37b7d-114">**0**</span><span class="sxs-lookup"><span data-stu-id="37b7d-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="37b7d-115">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="37b7d-115">Success.</span></span>

</dd> <dt>

<span data-ttu-id="37b7d-116">**5**</span><span class="sxs-lookup"><span data-stu-id="37b7d-116">**5**</span></span>
</dt> <dd>

<span data-ttu-id="37b7d-117">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="37b7d-117">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="37b7d-118">**87**</span><span class="sxs-lookup"><span data-stu-id="37b7d-118">**87**</span></span>
</dt> <dd>

<span data-ttu-id="37b7d-119">„Der Parameter ist falsch.“</span><span class="sxs-lookup"><span data-stu-id="37b7d-119">The parameter is incorrect.</span></span> <span data-ttu-id="37b7d-120">Kann auftreten, wenn das Objekt nicht ordnungsgemäß ausgefüllt ist oder wenn der Treiber im System nicht gefunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="37b7d-120">May occur when the object is not correctly filled or when driver can not be found in the system.</span></span> <span data-ttu-id="37b7d-121">Alternativ kann sich das Name-Attribut von dem in der INF-Datei angegebenen Modell unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="37b7d-121">Alternately, the name attribute may be different than the model specified in the .inf file.</span></span> <span data-ttu-id="37b7d-122">Möglicherweise ist auch ein umgekehrter umgekehrter Schrägstrich (" \\ ") für ein pathfile-Attribut vorhanden.</span><span class="sxs-lookup"><span data-stu-id="37b7d-122">Or, there may be a missing backslash ("\\") on a PathFile attribute.</span></span>

</dd> <dt>

<span data-ttu-id="37b7d-123">**1797**</span><span class="sxs-lookup"><span data-stu-id="37b7d-123">**1797**</span></span>
</dt> <dd>

<span data-ttu-id="37b7d-124">Der Druckertreiber ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="37b7d-124">The printer driver is unknown.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="37b7d-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="37b7d-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="37b7d-126">Bei Verwendung der **addprinterdriver** -Methode müssen Sie " **SeLoadDriverPrivilege** " verwenden, um einen Gerätetreiber zu laden oder zu entladen.</span><span class="sxs-lookup"><span data-stu-id="37b7d-126">When using the **AddPrinterDriver** method you must use **SeLoadDriverPrivilege** to load or unload a device driver.</span></span>

 

## <a name="examples"></a><span data-ttu-id="37b7d-127">Beispiele</span><span class="sxs-lookup"><span data-stu-id="37b7d-127">Examples</span></span>

<span data-ttu-id="37b7d-128">Mit dem Codebeispiel "[install a Printer Driver that CAB](https://Gallery.TechNet.Microsoft.Com/1aac6333-a794-48d3-b7da-46d87df56ee1) VBScript" wird ein hypothetischer Drucker mithilfe eines Druck Treibers installiert, der in Drivers.cab nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="37b7d-128">The[Install a Printer Driver not Found in Drivers Cab](https://Gallery.TechNet.Microsoft.Com/1aac6333-a794-48d3-b7da-46d87df56ee1) VBScript code example installs a hypothetical printer using a print driver not found in Drivers.cab.</span></span>

<span data-ttu-id="37b7d-129">Im folgenden VBScript-Beispiel wird der Druckertreiber für einen Apple LaserWriter 8500-Drucker installiert.</span><span class="sxs-lookup"><span data-stu-id="37b7d-129">The following VBScript sample installs the printer driver for an Apple LaserWriter 8500 printer.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
objWMIService.Security_.Privileges.AddAsString "SeLoadDriverPrivilege", True 
 
Set objDriver = objWMIService.Get("Win32_PrinterDriver") 
 
objDriver.Name = "NewPrinter Model 2900" 
objDriver.SupportedPlatform = "Windows NT x86" 
objDriver.Version = "3" 
objDriver.DriverPath = "C:\Scripts\NewPrinter.dll" 
objDriver.Infname = "C:\Scripts\NewPrinter.inf" 
intResult = objDriver.AddPrinterDriver(objDriver) 
```



## <a name="requirements"></a><span data-ttu-id="37b7d-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="37b7d-130">Requirements</span></span>



| <span data-ttu-id="37b7d-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="37b7d-131">Requirement</span></span> | <span data-ttu-id="37b7d-132">Wert</span><span class="sxs-lookup"><span data-stu-id="37b7d-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="37b7d-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="37b7d-133">Minimum supported client</span></span><br/> | <span data-ttu-id="37b7d-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="37b7d-134">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="37b7d-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="37b7d-135">Minimum supported server</span></span><br/> | <span data-ttu-id="37b7d-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="37b7d-136">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="37b7d-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="37b7d-137">Namespace</span></span><br/>                | <span data-ttu-id="37b7d-138">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="37b7d-138">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="37b7d-139">MOF</span><span class="sxs-lookup"><span data-stu-id="37b7d-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="37b7d-140"><dt>Win32 \_ Printer. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="37b7d-140"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="37b7d-141">DLL</span><span class="sxs-lookup"><span data-stu-id="37b7d-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37b7d-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37b7d-142"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="37b7d-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37b7d-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37b7d-144">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="37b7d-144">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="37b7d-145">**Win32- \_ PrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="37b7d-145">**Win32\_PrinterDriver**</span></span>](win32-printerdriver.md)
</dt> </dl>

 


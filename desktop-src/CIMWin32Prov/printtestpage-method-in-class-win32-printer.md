---
description: Druckt eine Testseite.
ms.assetid: 7968e637-9817-4111-89f5-d3c6961395e5
ms.tgt_platform: multiple
title: PrintTestpage-Methode der Win32_Printer-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.PrintTestPage
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: abf31237918d533ec43586ddd3d71204f2c8ae21
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344006"
---
# <a name="printtestpage-method-of-the-win32_printer-class"></a><span data-ttu-id="93a31-103">PrintTestpage-Methode der Win32- \_ Drucker Klasse</span><span class="sxs-lookup"><span data-stu-id="93a31-103">PrintTestPage method of the Win32\_Printer class</span></span>

<span data-ttu-id="93a31-104">Die [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode von **PrintTestPage** druckt eine Testseite.</span><span class="sxs-lookup"><span data-stu-id="93a31-104">The **PrintTestPage** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method prints a test page.</span></span>

<span data-ttu-id="93a31-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="93a31-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="93a31-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="93a31-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="93a31-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="93a31-107">Syntax</span></span>


```mof
uint32 PrintTestPage();
```



## <a name="parameters"></a><span data-ttu-id="93a31-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="93a31-108">Parameters</span></span>

<span data-ttu-id="93a31-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="93a31-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="93a31-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="93a31-110">Return value</span></span>

<span data-ttu-id="93a31-111">Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="93a31-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="93a31-112">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="93a31-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="93a31-113">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="93a31-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="93a31-114">**0**</span><span class="sxs-lookup"><span data-stu-id="93a31-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="93a31-115">Erfolg</span><span class="sxs-lookup"><span data-stu-id="93a31-115">Success</span></span>

</dd> <dt>

<span data-ttu-id="93a31-116">**5**</span><span class="sxs-lookup"><span data-stu-id="93a31-116">**5**</span></span>
</dt> <dd>

<span data-ttu-id="93a31-117">Zugriff verweigert</span><span class="sxs-lookup"><span data-stu-id="93a31-117">Access Denied</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="93a31-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="93a31-118">Examples</span></span>

<span data-ttu-id="93a31-119">Im folgenden PowerShell-Codebeispiel wird eine Testseite gedruckt.</span><span class="sxs-lookup"><span data-stu-id="93a31-119">The following PowerShell code sample prints a test page.</span></span>


```PowerShell
# Get printer objects from  WMI
$printers=Get-WmiObject Win32_Printer
"{0} Printers defined on this system" -f $printers.count

# Get a specific printer
$printer = $printers | where {$_.name -eq "\\smallguy\HP LaserJet 5M"}

# Display info
"Printer share name: {0}\{1}" -f $printer.servername, $printer.sharename
"Printer Port      : {0}    " -f $printer.PortName
  
# Print a test page
$printer.PrintTestPage()
```



## <a name="requirements"></a><span data-ttu-id="93a31-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="93a31-120">Requirements</span></span>



| <span data-ttu-id="93a31-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="93a31-121">Requirement</span></span> | <span data-ttu-id="93a31-122">Wert</span><span class="sxs-lookup"><span data-stu-id="93a31-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="93a31-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="93a31-123">Minimum supported client</span></span><br/> | <span data-ttu-id="93a31-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="93a31-124">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="93a31-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="93a31-125">Minimum supported server</span></span><br/> | <span data-ttu-id="93a31-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="93a31-126">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="93a31-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="93a31-127">Namespace</span></span><br/>                | <span data-ttu-id="93a31-128">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="93a31-128">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="93a31-129">MOF</span><span class="sxs-lookup"><span data-stu-id="93a31-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93a31-130"><dt>Win32 \_ Printer. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="93a31-130"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="93a31-131">DLL</span><span class="sxs-lookup"><span data-stu-id="93a31-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93a31-132"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93a31-132"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="93a31-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93a31-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93a31-134">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="93a31-134">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="93a31-135">**Win32- \_ Drucker**</span><span class="sxs-lookup"><span data-stu-id="93a31-135">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> </dl>

 


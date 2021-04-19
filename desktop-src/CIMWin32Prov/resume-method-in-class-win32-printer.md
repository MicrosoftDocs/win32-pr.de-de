---
description: Setzt eine angehaltene Druck Warteschlange fort.
ms.assetid: 6d6d21e9-f469-4e2c-9a89-3e9febe229fc
ms.tgt_platform: multiple
title: Resume-Methode der Win32_Printer-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.Resume
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3eca8849fd1c5c449261dac1a9530f4da42e9482
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342749"
---
# <a name="resume-method-of-the-win32_printer-class"></a><span data-ttu-id="66800-103">Resume-Methode der Win32- \_ Drucker Klasse</span><span class="sxs-lookup"><span data-stu-id="66800-103">Resume method of the Win32\_Printer class</span></span>

<span data-ttu-id="66800-104">Die Methode **Resume** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) setzt eine angehaltene Druck Warteschlange fort.</span><span class="sxs-lookup"><span data-stu-id="66800-104">The **Resume** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method resumes a paused print queue.</span></span>

<span data-ttu-id="66800-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="66800-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="66800-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="66800-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="66800-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="66800-107">Syntax</span></span>


```mof
uint32 Resume();
```



## <a name="parameters"></a><span data-ttu-id="66800-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="66800-108">Parameters</span></span>

<span data-ttu-id="66800-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="66800-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="66800-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="66800-110">Return value</span></span>

<span data-ttu-id="66800-111">Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="66800-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="66800-112">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="66800-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="66800-113">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="66800-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="66800-114">**0**</span><span class="sxs-lookup"><span data-stu-id="66800-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="66800-115">Erfolg</span><span class="sxs-lookup"><span data-stu-id="66800-115">Success</span></span>

</dd> <dt>

<span data-ttu-id="66800-116">**5**</span><span class="sxs-lookup"><span data-stu-id="66800-116">**5**</span></span>
</dt> <dd>

<span data-ttu-id="66800-117">Zugriff verweigert</span><span class="sxs-lookup"><span data-stu-id="66800-117">Access Denied</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="66800-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="66800-118">Requirements</span></span>



| <span data-ttu-id="66800-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="66800-119">Requirement</span></span> | <span data-ttu-id="66800-120">Wert</span><span class="sxs-lookup"><span data-stu-id="66800-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="66800-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="66800-121">Minimum supported client</span></span><br/> | <span data-ttu-id="66800-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="66800-122">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="66800-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="66800-123">Minimum supported server</span></span><br/> | <span data-ttu-id="66800-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="66800-124">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="66800-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="66800-125">Namespace</span></span><br/>                | <span data-ttu-id="66800-126">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="66800-126">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="66800-127">MOF</span><span class="sxs-lookup"><span data-stu-id="66800-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="66800-128"><dt>Win32 \_ Printer. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="66800-128"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="66800-129">DLL</span><span class="sxs-lookup"><span data-stu-id="66800-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66800-130"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66800-130"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="66800-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66800-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66800-132">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="66800-132">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="66800-133">**Win32- \_ Drucker**</span><span class="sxs-lookup"><span data-stu-id="66800-133">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> <dt>

[<span data-ttu-id="66800-134">**Pause-Methode**</span><span class="sxs-lookup"><span data-stu-id="66800-134">**Pause Method**</span></span>](pause-method-in-class-win32-printer.md)
</dt> </dl>

 


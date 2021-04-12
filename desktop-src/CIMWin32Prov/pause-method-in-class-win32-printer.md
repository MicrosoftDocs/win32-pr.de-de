---
description: Hält die Druckwarteschlange an.
ms.assetid: 0f425318-a7c0-4bba-bb44-e7635fa3ca03
ms.tgt_platform: multiple
title: Pause-Methode der Win32_Printer-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.Pause
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 12d7e84351d77730b580242a58b38d7506af451a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393202"
---
# <a name="pause-method-of-the-win32_printer-class"></a><span data-ttu-id="51997-103">Pause-Methode der Win32- \_ Drucker Klasse</span><span class="sxs-lookup"><span data-stu-id="51997-103">Pause method of the Win32\_Printer class</span></span>

<span data-ttu-id="51997-104">Die **Pause** - [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode hält die Druck Warteschlange an.</span><span class="sxs-lookup"><span data-stu-id="51997-104">The **Pause** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method pauses the print queue.</span></span> <span data-ttu-id="51997-105">Solange die Warteschlange nicht fortgesetzt wird, können keine Aufträge gedruckt werden.</span><span class="sxs-lookup"><span data-stu-id="51997-105">No jobs can print until the queue is resumed.</span></span>

<span data-ttu-id="51997-106">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="51997-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="51997-107">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="51997-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="51997-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="51997-108">Syntax</span></span>


```mof
uint32 Pause();
```



## <a name="parameters"></a><span data-ttu-id="51997-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="51997-109">Parameters</span></span>

<span data-ttu-id="51997-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="51997-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="51997-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="51997-111">Return value</span></span>

<span data-ttu-id="51997-112">Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="51997-112">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="51997-113">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="51997-113">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="51997-114">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="51997-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="51997-115">**0**</span><span class="sxs-lookup"><span data-stu-id="51997-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="51997-116">Erfolg</span><span class="sxs-lookup"><span data-stu-id="51997-116">Success</span></span>

</dd> <dt>

<span data-ttu-id="51997-117">**5**</span><span class="sxs-lookup"><span data-stu-id="51997-117">**5**</span></span>
</dt> <dd>

<span data-ttu-id="51997-118">Zugriff verweigert</span><span class="sxs-lookup"><span data-stu-id="51997-118">Access Denied</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="51997-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="51997-119">Requirements</span></span>



| <span data-ttu-id="51997-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="51997-120">Requirement</span></span> | <span data-ttu-id="51997-121">Wert</span><span class="sxs-lookup"><span data-stu-id="51997-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="51997-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="51997-122">Minimum supported client</span></span><br/> | <span data-ttu-id="51997-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="51997-123">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="51997-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="51997-124">Minimum supported server</span></span><br/> | <span data-ttu-id="51997-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="51997-125">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="51997-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="51997-126">Namespace</span></span><br/>                | <span data-ttu-id="51997-127">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="51997-127">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="51997-128">MOF</span><span class="sxs-lookup"><span data-stu-id="51997-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="51997-129"><dt>Win32 \_ Printer. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="51997-129"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="51997-130">DLL</span><span class="sxs-lookup"><span data-stu-id="51997-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51997-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51997-131"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="51997-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51997-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51997-133">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="51997-133">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="51997-134">**Win32- \_ Drucker**</span><span class="sxs-lookup"><span data-stu-id="51997-134">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> <dt>

[<span data-ttu-id="51997-135">**Resume-Methode**</span><span class="sxs-lookup"><span data-stu-id="51997-135">**Resume method**</span></span>](resume-method-in-class-win32-printer.md)
</dt> </dl>

 


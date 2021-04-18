---
description: Die Start Service-Methode versetzt den Dienst in den Zustand "gestartet".
ms.assetid: 0f221db1-29ad-4071-98d3-6d06e4f5e026
ms.tgt_platform: multiple
title: Start Service-Methode der Win32_PrinterDriver-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriver.StartService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 44e6fedb9e1d0edd9f355c654c7fe2cd25760ec7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344608"
---
# <a name="startservice-method-of-the-win32_printerdriver-class"></a><span data-ttu-id="e373a-103">Start Service-Methode der Win32 \_ PrinterDriver-Klasse</span><span class="sxs-lookup"><span data-stu-id="e373a-103">StartService method of the Win32\_PrinterDriver class</span></span>

<span data-ttu-id="e373a-104">Die **Start Service** -Methode versetzt den Dienst in den Zustand "gestartet".</span><span class="sxs-lookup"><span data-stu-id="e373a-104">The **StartService** method places the service in the started state.</span></span>

<span data-ttu-id="e373a-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="e373a-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e373a-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="e373a-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e373a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e373a-107">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="e373a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e373a-108">Parameters</span></span>

<span data-ttu-id="e373a-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="e373a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e373a-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e373a-110">Return value</span></span>

<span data-ttu-id="e373a-111">Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e373a-111">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="e373a-112">Werte, die sich von den in der folgenden Liste aufgeführten Werten unterscheiden, finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants).</span><span class="sxs-lookup"><span data-stu-id="e373a-112">For values different from those listed in the following list, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants).</span></span>

<dl> <dt>

<span data-ttu-id="e373a-113">**0**</span><span class="sxs-lookup"><span data-stu-id="e373a-113">**0**</span></span>
</dt> <dd>

<span data-ttu-id="e373a-114">Der Dienst wurde erfolgreich gestartet.</span><span class="sxs-lookup"><span data-stu-id="e373a-114">Service successfully started.</span></span>

</dd> <dt>

<span data-ttu-id="e373a-115">**1**</span><span class="sxs-lookup"><span data-stu-id="e373a-115">**1**</span></span>
</dt> <dd>

<span data-ttu-id="e373a-116">Die Anforderung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e373a-116">Request not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e373a-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e373a-117">Requirements</span></span>



| <span data-ttu-id="e373a-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e373a-118">Requirement</span></span> | <span data-ttu-id="e373a-119">Wert</span><span class="sxs-lookup"><span data-stu-id="e373a-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e373a-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e373a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e373a-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e373a-121">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="e373a-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e373a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e373a-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e373a-123">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="e373a-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="e373a-124">Namespace</span></span><br/>                | <span data-ttu-id="e373a-125">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e373a-125">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="e373a-126">MOF</span><span class="sxs-lookup"><span data-stu-id="e373a-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e373a-127"><dt>Win32 \_ Printer. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e373a-127"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="e373a-128">DLL</span><span class="sxs-lookup"><span data-stu-id="e373a-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e373a-129"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e373a-129"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="e373a-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e373a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e373a-131">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="e373a-131">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="e373a-132">**Win32- \_ PrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="e373a-132">**Win32\_PrinterDriver**</span></span>](win32-printerdriver.md)
</dt> </dl>

 


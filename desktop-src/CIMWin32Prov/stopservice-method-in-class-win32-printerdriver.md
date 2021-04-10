---
description: Platziert den Dienst, der durch das Win32 \_ PrinterDriver-Objekt dargestellt wird, im beendeten Zustand.
ms.assetid: 0e730fe6-ff9f-4866-a255-be6d372f2d7d
ms.tgt_platform: multiple
title: Stop Service-Methode der Win32_PrinterDriver-Klasse (sdoias. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriver.StopService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: faed7e9ed22ddcacbd8720e589463fd9a75fd87a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041441"
---
# <a name="stopservice-method-of-the-win32_printerdriver-class"></a><span data-ttu-id="478bf-103">Stop Service-Methode der Win32 \_ PrinterDriver-Klasse</span><span class="sxs-lookup"><span data-stu-id="478bf-103">StopService method of the Win32\_PrinterDriver class</span></span>

<span data-ttu-id="478bf-104">Die **StopService** - [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode versetzt den Dienst, der durch das [**Win32 \_ PrinterDriver**](win32-printerdriver.md) -Objekt dargestellt wird, in den Zustand "beendet".</span><span class="sxs-lookup"><span data-stu-id="478bf-104">The **StopService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method places the service represented by the [**Win32\_PrinterDriver**](win32-printerdriver.md) object in the stopped state.</span></span>

<span data-ttu-id="478bf-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="478bf-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="478bf-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="478bf-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="478bf-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="478bf-107">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="478bf-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="478bf-108">Parameters</span></span>

<span data-ttu-id="478bf-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="478bf-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="478bf-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="478bf-110">Return value</span></span>

<span data-ttu-id="478bf-111">Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="478bf-111">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="478bf-112">Werte, die sich von den in der folgenden Liste aufgeführten Werten unterscheiden, finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants).</span><span class="sxs-lookup"><span data-stu-id="478bf-112">For values different from those listed in the following list, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants).</span></span>

<dl> <dt>

<span data-ttu-id="478bf-113">**0**</span><span class="sxs-lookup"><span data-stu-id="478bf-113">**0**</span></span>
</dt> <dd>

<span data-ttu-id="478bf-114">Der Dienst wurde erfolgreich beendet.</span><span class="sxs-lookup"><span data-stu-id="478bf-114">Service successfully stopped.</span></span>

</dd> <dt>

<span data-ttu-id="478bf-115">**1**</span><span class="sxs-lookup"><span data-stu-id="478bf-115">**1**</span></span>
</dt> <dd>

<span data-ttu-id="478bf-116">Die Anforderung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="478bf-116">Request not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="478bf-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="478bf-117">Requirements</span></span>



| <span data-ttu-id="478bf-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="478bf-118">Requirement</span></span> | <span data-ttu-id="478bf-119">Wert</span><span class="sxs-lookup"><span data-stu-id="478bf-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="478bf-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="478bf-120">Minimum supported client</span></span><br/> | <span data-ttu-id="478bf-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="478bf-121">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="478bf-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="478bf-122">Minimum supported server</span></span><br/> | <span data-ttu-id="478bf-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="478bf-123">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="478bf-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="478bf-124">Namespace</span></span><br/>                | <span data-ttu-id="478bf-125">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="478bf-125">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="478bf-126">Header</span><span class="sxs-lookup"><span data-stu-id="478bf-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="478bf-127"><dt>Sdoias. h</dt></span><span class="sxs-lookup"><span data-stu-id="478bf-127"><dt>Sdoias.h</dt></span></span> </dl>           |
| <span data-ttu-id="478bf-128">MOF</span><span class="sxs-lookup"><span data-stu-id="478bf-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="478bf-129"><dt>Win32 \_ Printer. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="478bf-129"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="478bf-130">DLL</span><span class="sxs-lookup"><span data-stu-id="478bf-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="478bf-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="478bf-131"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="478bf-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="478bf-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="478bf-133">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="478bf-133">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="478bf-134">**Win32- \_ PrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="478bf-134">**Win32\_PrinterDriver**</span></span>](win32-printerdriver.md)
</dt> </dl>

 


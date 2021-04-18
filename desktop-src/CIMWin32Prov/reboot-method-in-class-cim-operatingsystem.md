---
description: Bei der Neustart Methode wird ein Neustart des Betriebssystems angefordert.
ms.assetid: 2ce766dd-51a4-4ffb-a45a-40399f1110f6
ms.tgt_platform: multiple
title: Reboot-Methode der CIM_OperatingSystem-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OperatingSystem.Reboot
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e498dd16372503b23aa56471224faf4d5d0ff012
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344805"
---
# <a name="reboot-method-of-the-cim_operatingsystem-class"></a><span data-ttu-id="c6aa2-103">Reboot-Methode der CIM \_ OperatingSystem-Klasse</span><span class="sxs-lookup"><span data-stu-id="c6aa2-103">Reboot method of the CIM\_OperatingSystem class</span></span>

<span data-ttu-id="c6aa2-104">Bei der **Neustart** Methode wird ein Neustart des Betriebssystems angefordert.</span><span class="sxs-lookup"><span data-stu-id="c6aa2-104">The **Reboot** method requests a reboot of the operating system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c6aa2-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="c6aa2-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c6aa2-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c6aa2-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c6aa2-107">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="c6aa2-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c6aa2-108">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c6aa2-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c6aa2-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6aa2-109">Syntax</span></span>


```mof
uint32 Reboot();
```



## <a name="parameters"></a><span data-ttu-id="c6aa2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6aa2-110">Parameters</span></span>

<span data-ttu-id="c6aa2-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="c6aa2-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c6aa2-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c6aa2-112">Return value</span></span>

<span data-ttu-id="c6aa2-113">Gibt bei Erfolg den Wert 0 (null) zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="c6aa2-113">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6aa2-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c6aa2-114">Remarks</span></span>

<span data-ttu-id="c6aa2-115">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="c6aa2-115">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="c6aa2-116">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="c6aa2-116">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="c6aa2-117">Informationen zu WMI-Klassen, die vom [**CIM- \_ OperatingSystem**](cim-operatingsystem.md)abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c6aa2-117">For WMI classes that are derived from [**CIM\_OperatingSystem**](cim-operatingsystem.md), see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="c6aa2-118">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="c6aa2-118">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c6aa2-119">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c6aa2-119">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

<span data-ttu-id="c6aa2-120">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="c6aa2-120">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c6aa2-121">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c6aa2-121">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6aa2-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c6aa2-122">Requirements</span></span>



| <span data-ttu-id="c6aa2-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c6aa2-123">Requirement</span></span> | <span data-ttu-id="c6aa2-124">Wert</span><span class="sxs-lookup"><span data-stu-id="c6aa2-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6aa2-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c6aa2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c6aa2-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c6aa2-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c6aa2-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c6aa2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c6aa2-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c6aa2-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c6aa2-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="c6aa2-129">Namespace</span></span><br/>                | <span data-ttu-id="c6aa2-130">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c6aa2-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c6aa2-131">MOF</span><span class="sxs-lookup"><span data-stu-id="c6aa2-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c6aa2-132"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c6aa2-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c6aa2-133">DLL</span><span class="sxs-lookup"><span data-stu-id="c6aa2-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6aa2-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6aa2-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6aa2-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c6aa2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6aa2-136">CIM- \_ OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="c6aa2-136">CIM\_OperatingSystem</span></span>](reboot-method-in-class-cim-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="c6aa2-137">**CIM- \_ OperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="c6aa2-137">**CIM\_OperatingSystem**</span></span>](cim-operatingsystem.md)
</dt> </dl>

 


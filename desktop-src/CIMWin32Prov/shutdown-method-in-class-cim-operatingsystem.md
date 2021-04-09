---
description: Die Methode zum Herunterfahren fordert das Herunterfahren des Betriebssystems an.
ms.assetid: f2a2a98b-2f4f-4aa1-9f54-515660273c8d
ms.tgt_platform: multiple
title: Shutdown-Methode der CIM_OperatingSystem-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OperatingSystem.Shutdown
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 78a11f325b8682b0024ff281a48989b837d3073a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860636"
---
# <a name="shutdown-method-of-the-cim_operatingsystem-class"></a><span data-ttu-id="5f240-103">Shutdown-Methode der CIM \_ OperatingSystem-Klasse</span><span class="sxs-lookup"><span data-stu-id="5f240-103">Shutdown method of the CIM\_OperatingSystem class</span></span>

<span data-ttu-id="5f240-104">Die Methode zum **herunter** fahren fordert das Herunterfahren des Betriebssystems an.</span><span class="sxs-lookup"><span data-stu-id="5f240-104">The **Shutdown** method requests a shutdown of the operating system.</span></span> <span data-ttu-id="5f240-105">Die Implementierung oder Unterklasse des Betriebssystems kann Abhängigkeiten zwischen den Methoden zum **herunter** fahren und [**Neustarten**](reboot-method-in-class-cim-operatingsystem.md) herstellen.</span><span class="sxs-lookup"><span data-stu-id="5f240-105">The implementation or subclass of the operating system can establish dependencies between the **Shutdown** and [**Reboot**](reboot-method-in-class-cim-operatingsystem.md) methods.</span></span> <span data-ttu-id="5f240-106">Beispielsweise können anspruchsvollere Funktionen bereitgestellt werden, z. b. ein geplantes Herunterfahren und ein Neustart.</span><span class="sxs-lookup"><span data-stu-id="5f240-106">For example, more sophisticated capabilities can be provided, such as a scheduled shutdown and reboot.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5f240-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="5f240-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5f240-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5f240-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5f240-109">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="5f240-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="5f240-110">Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="5f240-110">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="5f240-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f240-111">Syntax</span></span>


```mof
uint32 Shutdown();
```



## <a name="parameters"></a><span data-ttu-id="5f240-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f240-112">Parameters</span></span>

<span data-ttu-id="5f240-113">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="5f240-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5f240-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5f240-114">Return value</span></span>

<span data-ttu-id="5f240-115">Gibt bei Erfolg den Wert 0 (null) zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="5f240-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f240-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5f240-116">Remarks</span></span>

<span data-ttu-id="5f240-117">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="5f240-117">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="5f240-118">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="5f240-118">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="5f240-119">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="5f240-119">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5f240-120">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="5f240-120">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f240-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5f240-121">Requirements</span></span>



| <span data-ttu-id="5f240-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5f240-122">Requirement</span></span> | <span data-ttu-id="5f240-123">Wert</span><span class="sxs-lookup"><span data-stu-id="5f240-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f240-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5f240-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5f240-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5f240-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5f240-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5f240-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5f240-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5f240-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5f240-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="5f240-128">Namespace</span></span><br/>                | <span data-ttu-id="5f240-129">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5f240-129">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5f240-130">MOF</span><span class="sxs-lookup"><span data-stu-id="5f240-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5f240-131"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5f240-131"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5f240-132">DLL</span><span class="sxs-lookup"><span data-stu-id="5f240-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f240-133"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f240-133"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f240-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f240-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f240-135">CIM- \_ OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="5f240-135">CIM\_OperatingSystem</span></span>](shutdown-method-in-class-cim-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="5f240-136">**CIM- \_ OperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="5f240-136">**CIM\_OperatingSystem**</span></span>](cim-operatingsystem.md)
</dt> </dl>

 


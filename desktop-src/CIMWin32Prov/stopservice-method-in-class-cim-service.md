---
description: Beendet den Dienst, der durch das vom CIM-Dienst abgeleitete Objekt dargestellt wird \_ .
ms.assetid: f9eedde7-8d71-40a2-b1e9-7ba97e634f64
ms.tgt_platform: multiple
title: Stop Service-Methode der CIM_Service-Klasse (sdoias. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service.StopService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 14a7d378b514a93906c3be4f711bd6ab5b88bf17
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126848"
---
# <a name="stopservice-method-of-the-cim_service-class-sdoiash"></a><span data-ttu-id="a22de-103">Stop Service-Methode der CIM_Service-Klasse (sdoias. h)</span><span class="sxs-lookup"><span data-stu-id="a22de-103">StopService method of the CIM_Service class (Sdoias.h)</span></span>

<span data-ttu-id="a22de-104">Die **Stop Service** -Methode beendet den Dienst, der durch das vom [**CIM- \_ Dienst**](cim-service.md)abgeleitete Objekt dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="a22de-104">The **StopService** method stops the service represented by the object derived from [**CIM\_Service**](cim-service.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a22de-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a22de-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a22de-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a22de-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a22de-107">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="a22de-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a22de-108">Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="a22de-108">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a22de-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a22de-109">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="a22de-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a22de-110">Parameters</span></span>

<span data-ttu-id="a22de-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="a22de-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a22de-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a22de-112">Return value</span></span>

<span data-ttu-id="a22de-113">Gibt den Wert 0 (null) zurück, wenn der Dienst erfolgreich beendet wurde, 1 (eins), wenn die Anforderung nicht unterstützt wird, und jede andere Zahl, die auf einen Fehler hinweist.</span><span class="sxs-lookup"><span data-stu-id="a22de-113">Returns a value of 0 (zero) if the service was successfully stopped, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="a22de-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a22de-114">Remarks</span></span>

<span data-ttu-id="a22de-115">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="a22de-115">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="a22de-116">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="a22de-116">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="a22de-117">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="a22de-117">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a22de-118">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a22de-118">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a22de-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a22de-119">Requirements</span></span>



| <span data-ttu-id="a22de-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a22de-120">Requirement</span></span> | <span data-ttu-id="a22de-121">Wert</span><span class="sxs-lookup"><span data-stu-id="a22de-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a22de-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a22de-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a22de-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a22de-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a22de-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a22de-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a22de-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a22de-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a22de-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="a22de-126">Namespace</span></span><br/>                | <span data-ttu-id="a22de-127">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a22de-127">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a22de-128">Header</span><span class="sxs-lookup"><span data-stu-id="a22de-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a22de-129"><dt>Sdoias. h</dt></span><span class="sxs-lookup"><span data-stu-id="a22de-129"><dt>Sdoias.h</dt></span></span> </dl>     |
| <span data-ttu-id="a22de-130">MOF</span><span class="sxs-lookup"><span data-stu-id="a22de-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a22de-131"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a22de-131"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a22de-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a22de-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a22de-133"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a22de-133"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a22de-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a22de-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a22de-135">CIM- \_ Dienst</span><span class="sxs-lookup"><span data-stu-id="a22de-135">CIM\_Service</span></span>](stopservice-method-in-class-cim-service.md)
</dt> <dt>

[<span data-ttu-id="a22de-136">**CIM- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="a22de-136">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 


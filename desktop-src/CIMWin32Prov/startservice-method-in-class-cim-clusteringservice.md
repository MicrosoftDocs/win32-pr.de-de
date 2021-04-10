---
description: Die Start Service-Methode versetzt den Dienst in den Zustand "gestartet".
ms.assetid: 2efd2a06-a03c-4f4c-b2fa-889f84faac0f
ms.tgt_platform: multiple
title: Start Service-Methode der CIM_ClusteringService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ClusteringService.StartService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: b8abdeffa234461952f99013524042dcbba6e682
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214166"
---
# <a name="startservice-method-of-the-cim_clusteringservice-class"></a><span data-ttu-id="601ef-103">Start Service-Methode der CIM \_ clusteringservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="601ef-103">StartService method of the CIM\_ClusteringService class</span></span>

<span data-ttu-id="601ef-104">Die **Start Service** -Methode versetzt den Dienst in den Zustand "gestartet".</span><span class="sxs-lookup"><span data-stu-id="601ef-104">The **StartService** method puts the service in a started state.</span></span> <span data-ttu-id="601ef-105">In einer Unterklasse kann der Satz möglicher Rückgabecodes mit einem **ValueMap** -Qualifizierer für die-Methode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="601ef-105">In a subclass, the set of possible return codes can be specified using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="601ef-106">Die Zeichen folgen, in die der **ValueMap** -Inhalt übersetzt wird, können auch in der Unterklasse als **Werte** Array Qualifizierer angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="601ef-106">The strings to which the **ValueMap** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="601ef-107">Diese Methode wird vom [**CIM- \_ Dienst**](cim-service.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="601ef-107">This method is inherited from [**CIM\_Service**](cim-service.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="601ef-108">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="601ef-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="601ef-109">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="601ef-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="601ef-110">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="601ef-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="601ef-111">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="601ef-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="601ef-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="601ef-112">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="601ef-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="601ef-113">Parameters</span></span>

<span data-ttu-id="601ef-114">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="601ef-114">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="601ef-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="601ef-115">Return value</span></span>

<span data-ttu-id="601ef-116">Gibt den Wert 0 (null) zurück, wenn der Dienst erfolgreich gestartet wurde, 1 (eins), wenn die Anforderung nicht unterstützt wird, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="601ef-116">Returns a value of 0 (zero) if the service was successfully started, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="601ef-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="601ef-117">Remarks</span></span>

<span data-ttu-id="601ef-118">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="601ef-118">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="601ef-119">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="601ef-119">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="601ef-120">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="601ef-120">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="601ef-121">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="601ef-121">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="601ef-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="601ef-122">Requirements</span></span>



| <span data-ttu-id="601ef-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="601ef-123">Requirement</span></span> | <span data-ttu-id="601ef-124">Wert</span><span class="sxs-lookup"><span data-stu-id="601ef-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="601ef-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="601ef-125">Minimum supported client</span></span><br/> | <span data-ttu-id="601ef-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="601ef-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="601ef-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="601ef-127">Minimum supported server</span></span><br/> | <span data-ttu-id="601ef-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="601ef-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="601ef-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="601ef-129">Namespace</span></span><br/>                | <span data-ttu-id="601ef-130">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="601ef-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="601ef-131">MOF</span><span class="sxs-lookup"><span data-stu-id="601ef-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="601ef-132"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="601ef-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="601ef-133">DLL</span><span class="sxs-lookup"><span data-stu-id="601ef-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="601ef-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="601ef-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="601ef-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="601ef-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="601ef-136">CIM- \_ clusteringservice</span><span class="sxs-lookup"><span data-stu-id="601ef-136">CIM\_ClusteringService</span></span>](startservice-method-in-class-cim-clusteringservice.md)
</dt> <dt>

[<span data-ttu-id="601ef-137">**CIM- \_ clusteringservice**</span><span class="sxs-lookup"><span data-stu-id="601ef-137">**CIM\_ClusteringService**</span></span>](cim-clusteringservice.md)
</dt> </dl>

 


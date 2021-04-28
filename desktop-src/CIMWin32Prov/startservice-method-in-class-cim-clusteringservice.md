---
description: 'StartService-Methode der CIM_ClusteringService Klasse: Die StartService-Methode versetzt den Dienst in einen gestarteten Zustand.'
ms.assetid: 2efd2a06-a03c-4f4c-b2fa-889f84faac0f
ms.tgt_platform: multiple
title: StartService-Methode der CIM_ClusteringService Klasse
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
ms.openlocfilehash: dcd18af37da9302256776cfee844fd83f989c9b7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086188"
---
# <a name="startservice-method-of-the-cim_clusteringservice-class"></a><span data-ttu-id="20fcb-103">StartService-Methode der CIM \_ ClusteringService-Klasse</span><span class="sxs-lookup"><span data-stu-id="20fcb-103">StartService method of the CIM\_ClusteringService class</span></span>

<span data-ttu-id="20fcb-104">Die **StartService-Methode** versetzt den Dienst in einen gestarteten Zustand.</span><span class="sxs-lookup"><span data-stu-id="20fcb-104">The **StartService** method puts the service in a started state.</span></span> <span data-ttu-id="20fcb-105">In einer Unterklasse kann der Satz möglicher Rückgabecodes mithilfe eines ValueMap-Qualifizierers für die -Methode angegeben werden. </span><span class="sxs-lookup"><span data-stu-id="20fcb-105">In a subclass, the set of possible return codes can be specified using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="20fcb-106">Die Zeichenfolgen, in die **der ValueMap-Inhalt** übersetzt wird, können auch in der Unterklasse als Values-Arrayqualifizierer angegeben werden. </span><span class="sxs-lookup"><span data-stu-id="20fcb-106">The strings to which the **ValueMap** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="20fcb-107">Diese Methode wird vom [**CIM-Dienst \_ geerbt.**](cim-service.md)</span><span class="sxs-lookup"><span data-stu-id="20fcb-107">This method is inherited from [**CIM\_Service**](cim-service.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="20fcb-108">Die CIM-Klassen (Distributed Management Task Force) (DMTF) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="20fcb-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="20fcb-109">WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)</span><span class="sxs-lookup"><span data-stu-id="20fcb-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="20fcb-110">In diesem Thema wird Managed Object Format -Syntax (MOF) verwendet.</span><span class="sxs-lookup"><span data-stu-id="20fcb-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="20fcb-111">Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)</span><span class="sxs-lookup"><span data-stu-id="20fcb-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="20fcb-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="20fcb-112">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="20fcb-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="20fcb-113">Parameters</span></span>

<span data-ttu-id="20fcb-114">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="20fcb-114">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="20fcb-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="20fcb-115">Return value</span></span>

<span data-ttu-id="20fcb-116">Gibt den Wert 0 (null) zurück, wenn der Dienst erfolgreich gestartet wurde, 1 (eins), wenn die Anforderung nicht unterstützt wird, und eine beliebige andere Zahl, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="20fcb-116">Returns a value of 0 (zero) if the service was successfully started, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="20fcb-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="20fcb-117">Remarks</span></span>

<span data-ttu-id="20fcb-118">Diese Methode wird derzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="20fcb-118">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="20fcb-119">Um diese Methode zu verwenden, müssen Sie sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="20fcb-119">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="20fcb-120">Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von DMTF veröffentlicht wurden.</span><span class="sxs-lookup"><span data-stu-id="20fcb-120">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="20fcb-121">Microsoft hat möglicherweise Änderungen vorgenommen, um kleinere Fehler zu beheben, die Dokumentationsstandards des Microsoft SDK zu erfüllen oder weitere Informationen zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="20fcb-121">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="20fcb-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="20fcb-122">Requirements</span></span>



| <span data-ttu-id="20fcb-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="20fcb-123">Requirement</span></span> | <span data-ttu-id="20fcb-124">Wert</span><span class="sxs-lookup"><span data-stu-id="20fcb-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="20fcb-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="20fcb-125">Minimum supported client</span></span><br/> | <span data-ttu-id="20fcb-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="20fcb-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="20fcb-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="20fcb-127">Minimum supported server</span></span><br/> | <span data-ttu-id="20fcb-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="20fcb-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="20fcb-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="20fcb-129">Namespace</span></span><br/>                | <span data-ttu-id="20fcb-130">\\Stamm-CIMV2</span><span class="sxs-lookup"><span data-stu-id="20fcb-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="20fcb-131">MOF</span><span class="sxs-lookup"><span data-stu-id="20fcb-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="20fcb-132"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="20fcb-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="20fcb-133">DLL</span><span class="sxs-lookup"><span data-stu-id="20fcb-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20fcb-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20fcb-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20fcb-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="20fcb-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20fcb-136">CIM \_ ClusteringService</span><span class="sxs-lookup"><span data-stu-id="20fcb-136">CIM\_ClusteringService</span></span>](startservice-method-in-class-cim-clusteringservice.md)
</dt> <dt>

[<span data-ttu-id="20fcb-137">**CIM \_ ClusteringService**</span><span class="sxs-lookup"><span data-stu-id="20fcb-137">**CIM\_ClusteringService**</span></span>](cim-clusteringservice.md)
</dt> </dl>

 


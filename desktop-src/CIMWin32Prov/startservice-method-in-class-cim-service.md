---
description: 'StartService-Methode der CIM_Service-Klasse (CIMWin32-WMI-Anbieter): Die StartService-Methode versetzt den Dienst in einen gestarteten Zustand.'
ms.assetid: 0f2880ed-1643-4211-8684-12493711b1f8
ms.tgt_platform: multiple
title: StartService-Methode der CIM_Service-Klasse (CIMWin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service.StartService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6027112323fc14abf4c4a8dc667b921025a5e652
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086168"
---
# <a name="startservice-method-of-the-cim_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="e0dab-103">StartService-Methode der CIM_Service-Klasse (CIMWin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="e0dab-103">StartService method of the CIM_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="e0dab-104">Die **StartService-Methode** versetzt den Dienst in einen gestarteten Zustand.</span><span class="sxs-lookup"><span data-stu-id="e0dab-104">The **StartService** method puts the service in a started state.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e0dab-105">Die CIM-Klassen (Distributed Management Task Force) (DMTF (Distributed Management Task Force) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="e0dab-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e0dab-106">WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)</span><span class="sxs-lookup"><span data-stu-id="e0dab-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e0dab-107">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="e0dab-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e0dab-108">Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)</span><span class="sxs-lookup"><span data-stu-id="e0dab-108">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e0dab-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0dab-109">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="e0dab-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0dab-110">Parameters</span></span>

<span data-ttu-id="e0dab-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="e0dab-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e0dab-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e0dab-112">Return value</span></span>

<span data-ttu-id="e0dab-113">Gibt bei Erfolg den Wert 0 (null) und eine beliebige andere Zahl zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e0dab-113">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="e0dab-114">In einer Unterklasse kann der Satz möglicher Rückgabecodes  mithilfe eines ValueMap-Qualifizierers für die -Methode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e0dab-114">In a subclass, the set of possible return codes can be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="e0dab-115">Die Zeichenfolgen, in die der **ValueMap-Inhalt** übersetzt wird, können auch in der Unterklasse als Values-Arrayqualifizierer angegeben werden. </span><span class="sxs-lookup"><span data-stu-id="e0dab-115">The strings to which the **ValueMap** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0dab-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e0dab-116">Remarks</span></span>

<span data-ttu-id="e0dab-117">Diese Methode wird derzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="e0dab-117">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="e0dab-118">Um diese Methode verwenden zu können, müssen Sie sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="e0dab-118">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="e0dab-119">Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von dmtf veröffentlicht wurden.</span><span class="sxs-lookup"><span data-stu-id="e0dab-119">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e0dab-120">Möglicherweise hat Microsoft Änderungen vorgenommen, um kleinere Fehler zu korrigieren, den Dokumentationsstandards des Microsoft SDK zu entsprechen oder weitere Informationen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e0dab-120">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0dab-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e0dab-121">Requirements</span></span>



| <span data-ttu-id="e0dab-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e0dab-122">Requirement</span></span> | <span data-ttu-id="e0dab-123">Wert</span><span class="sxs-lookup"><span data-stu-id="e0dab-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0dab-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e0dab-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e0dab-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e0dab-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e0dab-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e0dab-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e0dab-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e0dab-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e0dab-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="e0dab-128">Namespace</span></span><br/>                | <span data-ttu-id="e0dab-129">Stamm \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e0dab-129">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e0dab-130">MOF</span><span class="sxs-lookup"><span data-stu-id="e0dab-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e0dab-131"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="e0dab-131"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e0dab-132">DLL</span><span class="sxs-lookup"><span data-stu-id="e0dab-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0dab-133"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0dab-133"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0dab-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e0dab-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0dab-135">\_CIM-Dienst</span><span class="sxs-lookup"><span data-stu-id="e0dab-135">CIM\_Service</span></span>](startservice-method-in-class-cim-service.md)
</dt> <dt>

[<span data-ttu-id="e0dab-136">**\_CIM-Dienst**</span><span class="sxs-lookup"><span data-stu-id="e0dab-136">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 


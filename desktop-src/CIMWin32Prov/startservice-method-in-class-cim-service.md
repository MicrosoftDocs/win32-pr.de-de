---
description: Die Start Service-Methode versetzt den Dienst in den Zustand "gestartet".
ms.assetid: 0f2880ed-1643-4211-8684-12493711b1f8
ms.tgt_platform: multiple
title: Start Service-Methode der CIM_Service-Klasse (cimwin32-WMI-Anbieter)
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
ms.openlocfilehash: 1592552595c06ec7111041cbb1c1b1d2628f8b6a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748417"
---
# <a name="startservice-method-of-the-cim_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="d7fe8-103">Start Service-Methode der CIM_Service-Klasse (cimwin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="d7fe8-103">StartService method of the CIM_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="d7fe8-104">Die **Start Service** -Methode versetzt den Dienst in den Zustand "gestartet".</span><span class="sxs-lookup"><span data-stu-id="d7fe8-104">The **StartService** method puts the service in a started state.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d7fe8-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d7fe8-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d7fe8-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d7fe8-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d7fe8-107">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="d7fe8-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d7fe8-108">Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="d7fe8-108">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d7fe8-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7fe8-109">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="d7fe8-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7fe8-110">Parameters</span></span>

<span data-ttu-id="d7fe8-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="d7fe8-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d7fe8-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d7fe8-112">Return value</span></span>

<span data-ttu-id="d7fe8-113">Gibt bei Erfolg den Wert 0 (null) zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="d7fe8-113">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="d7fe8-114">In einer Unterklasse kann der Satz möglicher Rückgabecodes mit einem **ValueMap** -Qualifizierer für die-Methode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d7fe8-114">In a subclass, the set of possible return codes can be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="d7fe8-115">Die Zeichen folgen, in die der **ValueMap** -Inhalt übersetzt wird, können auch in der Unterklasse als **Werte** Array Qualifizierer angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d7fe8-115">The strings to which the **ValueMap** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7fe8-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d7fe8-116">Remarks</span></span>

<span data-ttu-id="d7fe8-117">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="d7fe8-117">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="d7fe8-118">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="d7fe8-118">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="d7fe8-119">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="d7fe8-119">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d7fe8-120">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d7fe8-120">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7fe8-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d7fe8-121">Requirements</span></span>



| <span data-ttu-id="d7fe8-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d7fe8-122">Requirement</span></span> | <span data-ttu-id="d7fe8-123">Wert</span><span class="sxs-lookup"><span data-stu-id="d7fe8-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7fe8-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d7fe8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d7fe8-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d7fe8-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d7fe8-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d7fe8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d7fe8-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d7fe8-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d7fe8-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="d7fe8-128">Namespace</span></span><br/>                | <span data-ttu-id="d7fe8-129">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d7fe8-129">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d7fe8-130">MOF</span><span class="sxs-lookup"><span data-stu-id="d7fe8-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d7fe8-131"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d7fe8-131"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d7fe8-132">DLL</span><span class="sxs-lookup"><span data-stu-id="d7fe8-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7fe8-133"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7fe8-133"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7fe8-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d7fe8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7fe8-135">CIM- \_ Dienst</span><span class="sxs-lookup"><span data-stu-id="d7fe8-135">CIM\_Service</span></span>](startservice-method-in-class-cim-service.md)
</dt> <dt>

[<span data-ttu-id="d7fe8-136">**CIM- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="d7fe8-136">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 


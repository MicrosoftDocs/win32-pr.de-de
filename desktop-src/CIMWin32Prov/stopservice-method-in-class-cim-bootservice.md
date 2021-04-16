---
description: Beendet den Dienst, der durch das vom CIM-Bootservice abgeleitete Objekt dargestellt wird \_ .
ms.assetid: 443a2afa-ed46-4378-a06f-5f9f94af51c9
ms.tgt_platform: multiple
title: Stop Service-Methode der CIM_BootService-Klasse (sdoias. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BootService.StopService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c054a9d05410ddbe7ee7d11c5bd4adba9e0ce83b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523691"
---
# <a name="stopservice-method-of-the-cim_bootservice-class"></a><span data-ttu-id="5cac6-103">Stop Service-Methode der CIM \_ Bootservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="5cac6-103">StopService method of the CIM\_BootService class</span></span>

<span data-ttu-id="5cac6-104">Die **Stop Service** -Methode beendet den Dienst, der durch das vom [**CIM- \_ Bootservice**](cim-bootservice.md)abgeleitete Objekt dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="5cac6-104">The **StopService** method stops the service represented by the object derived from [**CIM\_BootService**](cim-bootservice.md).</span></span> <span data-ttu-id="5cac6-105">Diese Methode wird vom [**CIM- \_ Dienst**](cim-service.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5cac6-105">This method is inherited from [**CIM\_Service**](cim-service.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5cac6-106">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="5cac6-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5cac6-107">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5cac6-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5cac6-108">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="5cac6-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="5cac6-109">Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="5cac6-109">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="5cac6-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="5cac6-110">Syntax</span></span>


```mof
Integer StopService();
```



## <a name="parameters"></a><span data-ttu-id="5cac6-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="5cac6-111">Parameters</span></span>

<span data-ttu-id="5cac6-112">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="5cac6-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5cac6-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5cac6-113">Return value</span></span>

<span data-ttu-id="5cac6-114">Gibt bei Erfolg den Wert 0 (null) zurück, 1 (eins), wenn die Anforderung nicht unterstützt wird, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="5cac6-114">Returns a value of 0 (zero) on success, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="5cac6-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5cac6-115">Remarks</span></span>

<span data-ttu-id="5cac6-116">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="5cac6-116">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="5cac6-117">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="5cac6-117">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="5cac6-118">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="5cac6-118">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5cac6-119">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="5cac6-119">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5cac6-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5cac6-120">Requirements</span></span>



| <span data-ttu-id="5cac6-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5cac6-121">Requirement</span></span> | <span data-ttu-id="5cac6-122">Wert</span><span class="sxs-lookup"><span data-stu-id="5cac6-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5cac6-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5cac6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5cac6-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5cac6-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5cac6-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5cac6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5cac6-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5cac6-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5cac6-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="5cac6-127">Namespace</span></span><br/>                | <span data-ttu-id="5cac6-128">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5cac6-128">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5cac6-129">Header</span><span class="sxs-lookup"><span data-stu-id="5cac6-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="5cac6-130"><dt>Sdoias. h</dt></span><span class="sxs-lookup"><span data-stu-id="5cac6-130"><dt>Sdoias.h</dt></span></span> </dl>     |
| <span data-ttu-id="5cac6-131">MOF</span><span class="sxs-lookup"><span data-stu-id="5cac6-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5cac6-132"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5cac6-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5cac6-133">DLL</span><span class="sxs-lookup"><span data-stu-id="5cac6-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5cac6-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5cac6-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5cac6-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5cac6-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cac6-136">CIM- \_ Bootservice</span><span class="sxs-lookup"><span data-stu-id="5cac6-136">CIM\_BootService</span></span>](stopservice-method-in-class-cim-bootservice.md)
</dt> <dt>

[<span data-ttu-id="5cac6-137">**CIM- \_ Bootservice**</span><span class="sxs-lookup"><span data-stu-id="5cac6-137">**CIM\_BootService**</span></span>](cim-bootservice.md)
</dt> </dl>

 


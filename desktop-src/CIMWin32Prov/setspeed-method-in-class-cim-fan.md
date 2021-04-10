---
description: Die setSpeed-Methode fordert an, dass die Lüfter Geschwindigkeit auf den im Eingabeparameter der Methode angegebenen Wert festgelegt wird.
ms.assetid: 7dd1cd57-66c5-4b50-9a73-31caf0b824e6
ms.tgt_platform: multiple
title: SetSpeed-Methode der CIM_Fan-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Fan.SetSpeed
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 16d90dbef3a9318ad144303e5720cea0abbde03e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861728"
---
# <a name="setspeed-method-of-the-cim_fan-class"></a><span data-ttu-id="d6d96-103">SetSpeed-Methode der CIM- \_ Lüfter-Klasse</span><span class="sxs-lookup"><span data-stu-id="d6d96-103">SetSpeed method of the CIM\_Fan class</span></span>

<span data-ttu-id="d6d96-104">Die **setSpeed** -Methode fordert an, dass die Lüfter Geschwindigkeit auf den im Eingabeparameter der Methode angegebenen Wert festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="d6d96-104">The **SetSpeed** method requests that the fan speed be set to the value specified in the method's input parameter.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d6d96-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d6d96-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d6d96-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d6d96-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d6d96-107">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="d6d96-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d6d96-108">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="d6d96-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d6d96-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6d96-109">Syntax</span></span>


```mof
uint32 SetSpeed(
  [in] uint64 DesiredSpeed
);
```



## <a name="parameters"></a><span data-ttu-id="d6d96-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6d96-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6d96-111">*Desiredspeed* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d6d96-111">*DesiredSpeed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6d96-112">Die angeforderte Lüfter-Geschwindigkeit in Umdrehungen pro Minute.</span><span class="sxs-lookup"><span data-stu-id="d6d96-112">Requested fan speed, in revolutions per minute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6d96-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d6d96-113">Return value</span></span>

<span data-ttu-id="d6d96-114">Gibt bei Erfolg den Wert 0 (null) zurück, 1 (eins), wenn die Anforderung nicht unterstützt wird, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="d6d96-114">Returns a value of 0 (zero) on success, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6d96-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d6d96-115">Remarks</span></span>

<span data-ttu-id="d6d96-116">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="d6d96-116">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="d6d96-117">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="d6d96-117">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="d6d96-118">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="d6d96-118">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d6d96-119">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d6d96-119">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6d96-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d6d96-120">Requirements</span></span>



| <span data-ttu-id="d6d96-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d6d96-121">Requirement</span></span> | <span data-ttu-id="d6d96-122">Wert</span><span class="sxs-lookup"><span data-stu-id="d6d96-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6d96-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d6d96-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d6d96-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d6d96-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d6d96-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d6d96-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d6d96-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d6d96-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d6d96-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="d6d96-127">Namespace</span></span><br/>                | <span data-ttu-id="d6d96-128">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d6d96-128">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d6d96-129">MOF</span><span class="sxs-lookup"><span data-stu-id="d6d96-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d6d96-130"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d6d96-130"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d6d96-131">DLL</span><span class="sxs-lookup"><span data-stu-id="d6d96-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6d96-132"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6d96-132"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6d96-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6d96-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6d96-134">CIM- \_ Lüfter</span><span class="sxs-lookup"><span data-stu-id="d6d96-134">CIM\_Fan</span></span>](setspeed-method-in-class-cim-fan.md)
</dt> <dt>

[<span data-ttu-id="d6d96-135">**CIM- \_ Lüfter**</span><span class="sxs-lookup"><span data-stu-id="d6d96-135">**CIM\_Fan**</span></span>](cim-fan.md)
</dt> </dl>

 


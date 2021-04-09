---
description: Die ResetCounter-Methode setzt die Fehler-und Warnungs Zähler zurück.
ms.assetid: 5bc6c939-cd97-40ca-a16c-5227e7f27c76
ms.tgt_platform: multiple
title: ResetCounter-Methode der CIM_DeviceErrorCounts-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceErrorCounts.ResetCounter
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 386547362f5a7aa52bddfbf9df3af01949aecbdd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860707"
---
# <a name="resetcounter-method-of-the-cim_deviceerrorcounts-class"></a><span data-ttu-id="ce851-103">ResetCounter-Methode der CIM \_ deviceerrorcounts-Klasse</span><span class="sxs-lookup"><span data-stu-id="ce851-103">ResetCounter method of the CIM\_DeviceErrorCounts class</span></span>

<span data-ttu-id="ce851-104">Die **ResetCounter** -Methode setzt die Fehler-und Warnungs Zähler zurück.</span><span class="sxs-lookup"><span data-stu-id="ce851-104">The **ResetCounter** method resets the error and warning counters.</span></span> <span data-ttu-id="ce851-105">Eine-Methode wird verwendet, damit die Instrumentation des logischen Geräts, das die Fehler und Warnungen in der Tabelle auffüllt, auch die interne Verarbeitung und Leistungsindikatoren zurücksetzen kann.</span><span class="sxs-lookup"><span data-stu-id="ce851-105">A method is used so that the logical device's instrumentation, which tabulates the errors and warnings, can also reset its internal processing and counters.</span></span> <span data-ttu-id="ce851-106">In einer Unterklasse kann der Satz möglicher Rückgabecodes mit einem **ValueMap** -Qualifizierer für die-Methode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ce851-106">In a subclass, the set of possible return codes can be specified using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="ce851-107">Die Zeichen folgen, in die der **ValueMap** -Inhalt übersetzt wird, können auch in der Unterklasse als **Werte** Array Qualifizierer angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ce851-107">The strings to which the **ValueMap** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ce851-108">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="ce851-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ce851-109">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ce851-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ce851-110">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="ce851-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ce851-111">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ce851-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ce851-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce851-112">Syntax</span></span>


```mof
uint32 ResetCounter(
  [in] uint16 SelectedCounter
);
```



## <a name="parameters"></a><span data-ttu-id="ce851-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce851-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce851-114">*Selectedcounter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ce851-114">*SelectedCounter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce851-115">Der zurück zusetzenden Fehlerwert.</span><span class="sxs-lookup"><span data-stu-id="ce851-115">Error counter to reset.</span></span>

<dt>

<span id="All"></span><span id="all"></span><span id="ALL"></span>

<span data-ttu-id="ce851-116">**Alle** (0)</span><span class="sxs-lookup"><span data-stu-id="ce851-116">**All** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Indeterminate_Error_Counter"></span><span id="indeterminate_error_counter"></span><span id="INDETERMINATE_ERROR_COUNTER"></span>

<span data-ttu-id="ce851-117">**Unbestimmter Fehler Zählers** (1)</span><span class="sxs-lookup"><span data-stu-id="ce851-117">**Indeterminate Error Counter** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical_Error_Counter"></span><span id="critical_error_counter"></span><span id="CRITICAL_ERROR_COUNTER"></span>

<span data-ttu-id="ce851-118">**Kritischer Fehler Zählers** (2)</span><span class="sxs-lookup"><span data-stu-id="ce851-118">**Critical Error Counter** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Major_Error_Counter"></span><span id="major_error_counter"></span><span id="MAJOR_ERROR_COUNTER"></span>

<span data-ttu-id="ce851-119">**Hauptfehler-Counter** (3)</span><span class="sxs-lookup"><span data-stu-id="ce851-119">**Major Error Counter** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Minor_Error_Counter"></span><span id="minor_error_counter"></span><span id="MINOR_ERROR_COUNTER"></span>

<span data-ttu-id="ce851-120">**Kleiner Fehler-Counter** (4)</span><span class="sxs-lookup"><span data-stu-id="ce851-120">**Minor Error Counter** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning_Counter"></span><span id="warning_counter"></span><span id="WARNING_COUNTER"></span>

<span data-ttu-id="ce851-121">**Warnungs Counter** (5)</span><span class="sxs-lookup"><span data-stu-id="ce851-121">**Warning Counter** (5)</span></span>


<span data-ttu-id="ce851-122"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ce851-122"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="ce851-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ce851-123">Return value</span></span>

<span data-ttu-id="ce851-124">Gibt bei Erfolg 0 (null) zurück, 1 (eins), wenn nicht unterstützt, und einen anderen Wert, wenn ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="ce851-124">Returns 0 (zero) if successful, 1 (one) if not supported, and any other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce851-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ce851-125">Remarks</span></span>

<span data-ttu-id="ce851-126">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="ce851-126">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="ce851-127">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="ce851-127">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="ce851-128">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="ce851-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ce851-129">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="ce851-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce851-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce851-130">Requirements</span></span>



| <span data-ttu-id="ce851-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ce851-131">Requirement</span></span> | <span data-ttu-id="ce851-132">Wert</span><span class="sxs-lookup"><span data-stu-id="ce851-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce851-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ce851-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ce851-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ce851-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ce851-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ce851-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ce851-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ce851-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ce851-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="ce851-137">Namespace</span></span><br/>                | <span data-ttu-id="ce851-138">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ce851-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ce851-139">MOF</span><span class="sxs-lookup"><span data-stu-id="ce851-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ce851-140"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ce851-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ce851-141">DLL</span><span class="sxs-lookup"><span data-stu-id="ce851-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce851-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce851-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce851-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce851-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce851-144">CIM \_ deviceerrorcounts</span><span class="sxs-lookup"><span data-stu-id="ce851-144">CIM\_DeviceErrorCounts</span></span>](resetcounter-method-in-class-cim-deviceerrorcounts.md)
</dt> <dt>

[<span data-ttu-id="ce851-145">**CIM \_ deviceerrorcounts**</span><span class="sxs-lookup"><span data-stu-id="ce851-145">**CIM\_DeviceErrorCounts**</span></span>](cim-deviceerrorcounts.md)
</dt> </dl>

 


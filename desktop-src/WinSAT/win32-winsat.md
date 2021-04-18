---
title: Win32_WinSAT-Klasse
description: Definiert Übersichts Bewertungsinformationen für die aktuellste formale Bewertung.
ms.assetid: adf4de42-9dfd-46a7-ae75-3bbcfd15dd68
keywords:
- Win32_WinSAT Klasse WinSAT
- Win32_WinSAT Klasse WinSAT, beschrieben
topic_type:
- apiref
api_name:
- Win32_WinSAT
- Win32_WinSAT.TimeTaken
- Win32_WinSAT.WinSPRLevel
- Win32_WinSAT.WinSATAssessmentState
- Win32_WinSAT.MemoryScore
- Win32_WinSAT.CPUScore
- Win32_WinSAT.DiskScore
- Win32_WinSAT.D3DScore
- Win32_WinSAT.GraphicsScore
api_location:
- WinSATAPI.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 829e5e1b3658771728aab9ef30634d90a8bc6450
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344109"
---
# <a name="win32_winsat-class"></a><span data-ttu-id="f9eef-105">Win32- \_ WinSAT-Klasse</span><span class="sxs-lookup"><span data-stu-id="f9eef-105">Win32\_WinSAT class</span></span>

<span data-ttu-id="f9eef-106">\[**Win32 \_ WinSAT** kann nach Windows 8.1 geändert werden oder für Releases nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="f9eef-106">\[**Win32\_WinSAT** may be altered or unavailable for releases after Windows 8.1.\]</span></span>

<span data-ttu-id="f9eef-107">Definiert Übersichts Bewertungsinformationen für die aktuellste formale Bewertung.</span><span class="sxs-lookup"><span data-stu-id="f9eef-107">Defines summary assessment information for the most recent formal assessment.</span></span>

<span data-ttu-id="f9eef-108">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="f9eef-108">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9eef-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9eef-109">Syntax</span></span>

``` syntax
class Win32_WinSAT
{
  string TimeTaken = "MostRecentAssessment";
  real32 WinSPRLevel;
  uint32 WinSATAssessmentState;
  real32 MemoryScore;
  real32 CPUScore;
  real32 DiskScore;
  real32 D3DScore;
  real32 GraphicsScore;
};
```

## <a name="members"></a><span data-ttu-id="f9eef-110">Member</span><span class="sxs-lookup"><span data-stu-id="f9eef-110">Members</span></span>

<span data-ttu-id="f9eef-111">Die **Win32- \_ WinSAT** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f9eef-111">The **Win32\_WinSAT** class has these types of members:</span></span>

-   [<span data-ttu-id="f9eef-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f9eef-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f9eef-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f9eef-113">Properties</span></span>

<span data-ttu-id="f9eef-114">Die **Win32- \_ WinSAT** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f9eef-114">The **Win32\_WinSAT** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f9eef-115">**Cpuscore**</span><span class="sxs-lookup"><span data-stu-id="f9eef-115">**CPUScore**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9eef-116">Datentyp: **real32**</span><span class="sxs-lookup"><span data-stu-id="f9eef-116">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="f9eef-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9eef-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9eef-118">Eine Bewertung der Prozessoren auf dem Computer.</span><span class="sxs-lookup"><span data-stu-id="f9eef-118">A score for the processors on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="f9eef-119">**D3DScore**</span><span class="sxs-lookup"><span data-stu-id="f9eef-119">**D3DScore**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9eef-120">Datentyp: **real32**</span><span class="sxs-lookup"><span data-stu-id="f9eef-120">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="f9eef-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9eef-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9eef-122">Nach Windows 8.1 bewertet WinSAT nicht mehr die dreidimensionalen Grafikfunktionen (Gaming) des Computers, und die Fähigkeit des Grafik Treibers, Objekte zu rendern und mithilfe dieser Bewertung Shader auszuführen.</span><span class="sxs-lookup"><span data-stu-id="f9eef-122">After Windows 8.1, WinSAT no longer assess the three-dimensional graphics (gaming) capabilities of the computer and the graphics driver's ability to render objects and execute shaders using this assessment.</span></span> <span data-ttu-id="f9eef-123">Aus Kompatibilitätsgründen werden WinSAT-Werte für die Metriken und Ergebnisse in WinSAT-Berichten angezeigt. Diese werden jedoch nicht in Echtzeit berechnet.</span><span class="sxs-lookup"><span data-stu-id="f9eef-123">For compatibility, WinSAT report sentinel values for the metrics and scores, however these are not calculated in real time.</span></span>

</dd> <dt>

<span data-ttu-id="f9eef-124">**Diskscore**</span><span class="sxs-lookup"><span data-stu-id="f9eef-124">**DiskScore**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9eef-125">Datentyp: **real32**</span><span class="sxs-lookup"><span data-stu-id="f9eef-125">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="f9eef-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9eef-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9eef-127">Ein Ergebnis für den sequenziellen Lesedurchsatz auf der primären Festplatte auf dem Computer.</span><span class="sxs-lookup"><span data-stu-id="f9eef-127">A score for the sequential read throughput on the primary hard disk on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="f9eef-128">**Graphicsscore**</span><span class="sxs-lookup"><span data-stu-id="f9eef-128">**GraphicsScore**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9eef-129">Datentyp: **real32**</span><span class="sxs-lookup"><span data-stu-id="f9eef-129">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="f9eef-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9eef-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9eef-131">Eine Bewertung für die Grafikfunktionen des Computers.</span><span class="sxs-lookup"><span data-stu-id="f9eef-131">A score for the graphics capabilities of the computer.</span></span>

</dd> <dt>

<span data-ttu-id="f9eef-132">**Memoryscore**</span><span class="sxs-lookup"><span data-stu-id="f9eef-132">**MemoryScore**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9eef-133">Datentyp: **real32**</span><span class="sxs-lookup"><span data-stu-id="f9eef-133">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="f9eef-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9eef-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9eef-135">Ein Ergebnis für den Arbeitsspeicher Durchsatz und die Kapazität des Computers.</span><span class="sxs-lookup"><span data-stu-id="f9eef-135">A score for the memory throughput and capacity of the computer.</span></span>

</dd> <dt>

<span data-ttu-id="f9eef-136">**TimeTaken**</span><span class="sxs-lookup"><span data-stu-id="f9eef-136">**TimeTaken**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9eef-137">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f9eef-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9eef-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9eef-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9eef-139">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="f9eef-139">Qualifiers: **key**</span></span>
</dt> </dl>

<span data-ttu-id="f9eef-140">Diese Eigenschaft muss in der WHERE-Klausel der WQL-Abfrage auf "mustrecentassessment" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f9eef-140">This property must be set to "MostRecentAssessment" in the WHERE clause of your WQL query.</span></span>

</dd> <dt>

<span data-ttu-id="f9eef-141">**Winsatbewermentstate**</span><span class="sxs-lookup"><span data-stu-id="f9eef-141">**WinSATAssessmentState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9eef-142">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f9eef-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f9eef-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9eef-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9eef-144">Der Status der Bewertung.</span><span class="sxs-lookup"><span data-stu-id="f9eef-144">State of the assessment.</span></span> <span data-ttu-id="f9eef-145">Eine Beschreibung der möglichen Werte finden Sie in der [**WinSAT- \_ Bewertungs \_ Zustands**](/windows/win32/api/winsatcominterfacei/ne-winsatcominterfacei-winsat_assessment_state) Enumeration.</span><span class="sxs-lookup"><span data-stu-id="f9eef-145">For a description of the possible values, see the [**WINSAT\_ASSESSMENT\_STATE**](/windows/win32/api/winsatcominterfacei/ne-winsatcominterfacei-winsat_assessment_state) enumeration.</span></span>

<dl> <dt>

<span data-ttu-id="f9eef-146"><span id="StateUnknown"></span><span id="stateunknown"></span><span id="STATEUNKNOWN"></span>**Stateunknown** (0)</span><span class="sxs-lookup"><span data-stu-id="f9eef-146"><span id="StateUnknown"></span><span id="stateunknown"></span><span id="STATEUNKNOWN"></span>**StateUnknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f9eef-147"><span id="Valid"></span><span id="valid"></span><span id="VALID"></span>**Gültig** (1)</span><span class="sxs-lookup"><span data-stu-id="f9eef-147"><span id="Valid"></span><span id="valid"></span><span id="VALID"></span>**Valid** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f9eef-148"><span id="IncoherentWithHardware"></span><span id="incoherentwithhardware"></span><span id="INCOHERENTWITHHARDWARE"></span>**Incoherent entwithhardware** (2)</span><span class="sxs-lookup"><span data-stu-id="f9eef-148"><span id="IncoherentWithHardware"></span><span id="incoherentwithhardware"></span><span id="INCOHERENTWITHHARDWARE"></span>**IncoherentWithHardware** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f9eef-149"><span id="NoAssessmentAvailable"></span><span id="noassessmentavailable"></span><span id="NOASSESSMENTAVAILABLE"></span>**Nogutamentavailable** (3)</span><span class="sxs-lookup"><span data-stu-id="f9eef-149"><span id="NoAssessmentAvailable"></span><span id="noassessmentavailable"></span><span id="NOASSESSMENTAVAILABLE"></span>**NoAssessmentAvailable** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f9eef-150"><span id="Invalid"></span><span id="invalid"></span><span id="INVALID"></span>**Ungültig** (4)</span><span class="sxs-lookup"><span data-stu-id="f9eef-150"><span id="Invalid"></span><span id="invalid"></span><span id="INVALID"></span>**Invalid** (4)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f9eef-151">**Winsprlevel**</span><span class="sxs-lookup"><span data-stu-id="f9eef-151">**WinSPRLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9eef-152">Datentyp: **real32**</span><span class="sxs-lookup"><span data-stu-id="f9eef-152">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="f9eef-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f9eef-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9eef-154">Die Basisbewertung für den Computer.</span><span class="sxs-lookup"><span data-stu-id="f9eef-154">Base score for the computer.</span></span> <span data-ttu-id="f9eef-155">Ausführliche Informationen zum Wert "Score" finden Sie in der [**iprovidebug**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-get_systemrating) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f9eef-155">For details on the score value, see the [**IProvideWinSATResultsInfo::SystemRating**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-get_systemrating) property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f9eef-156">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9eef-156">Remarks</span></span>

<span data-ttu-id="f9eef-157">Informationen zu den unter Komponenten Bewertungen, wie z. b. **memoryscore**, finden Sie in der [**iprovidewinsatprocessmentinfo:: Score**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatassessmentinfo-get_score) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f9eef-157">For information on the subcomponent scores, such as **MemoryScore**, see the [**IProvideWinSATAssessmentInfo::Score**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatassessmentinfo-get_score) property.</span></span>

## <a name="examples"></a><span data-ttu-id="f9eef-158">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f9eef-158">Examples</span></span>

<span data-ttu-id="f9eef-159">Ein Beispiel für die Verwendung von WMI zum Abrufen von Daten aus dieser Klasse finden Sie in der [**iprovidewinsatvisuals:: get- \_ Bitmap**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatvisuals-get_bitmap) -Methode.</span><span class="sxs-lookup"><span data-stu-id="f9eef-159">For an example that shows how to use WMI to retrieve data from this class, see the [**IProvideWinSATVisuals::get\_Bitmap**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatvisuals-get_bitmap) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9eef-160">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f9eef-160">Requirements</span></span>



| <span data-ttu-id="f9eef-161">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f9eef-161">Requirement</span></span> | <span data-ttu-id="f9eef-162">Wert</span><span class="sxs-lookup"><span data-stu-id="f9eef-162">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9eef-163">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f9eef-163">Minimum supported client</span></span><br/> | <span data-ttu-id="f9eef-164">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f9eef-164">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f9eef-165">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f9eef-165">Minimum supported server</span></span><br/> | <span data-ttu-id="f9eef-166">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f9eef-166">None supported</span></span><br/>                                                                |
| <span data-ttu-id="f9eef-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="f9eef-167">Namespace</span></span><br/>                | <span data-ttu-id="f9eef-168">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="f9eef-168">Root\\CIMv2</span></span><br/>                                                                   |
| <span data-ttu-id="f9eef-169">MOF</span><span class="sxs-lookup"><span data-stu-id="f9eef-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f9eef-170"><dt>WinSAT. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f9eef-170"><dt>WinSAT.mof</dt></span></span> </dl>    |
| <span data-ttu-id="f9eef-171">DLL</span><span class="sxs-lookup"><span data-stu-id="f9eef-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9eef-172"><dt>WinSATAPI.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9eef-172"><dt>WinSATAPI.dll</dt></span></span> </dl> |



 

 






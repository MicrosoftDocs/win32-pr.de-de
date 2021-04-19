---
description: Die isaktivierte Methode der Win32- \_ TPM-Klasse gibt an, ob das Gerät aktiviert ist. Dieser Wert kann durch die Methoden enable und deaktivieren geändert werden.
ms.assetid: e1d5513f-33eb-49e3-9582-d6c103ca5d03
title: Isaktivierte Methode der Win32_Tpm-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsEnabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: d808bb68e53b1a24ff668d1b7a9680b5d57b5e9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345031"
---
# <a name="isenabled-method-of-the-win32_tpm-class"></a><span data-ttu-id="b219d-104">Isaktivierte Methode der Win32 \_ TPM-Klasse</span><span class="sxs-lookup"><span data-stu-id="b219d-104">IsEnabled method of the Win32\_Tpm class</span></span>

<span data-ttu-id="b219d-105">Die **isaktivierte** Methode der [**Win32- \_ TPM**](win32-tpm.md) -Klasse gibt an, ob das Gerät aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b219d-105">The **IsEnabled** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether the device is enabled.</span></span> <span data-ttu-id="b219d-106">Dieser Wert kann durch die Methoden [**enable**](enable-win32-tpm.md) und [**Deaktivieren**](disable-win32-tpm.md) geändert werden.</span><span class="sxs-lookup"><span data-stu-id="b219d-106">This value can be changed by the [**Enable**](enable-win32-tpm.md) and [**Disable**](disable-win32-tpm.md) methods.</span></span>

## <a name="syntax"></a><span data-ttu-id="b219d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b219d-107">Syntax</span></span>


```mof
uint32 IsEnabled(
  [out] boolean IsEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="b219d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b219d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b219d-109">*Isaktiviert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b219d-109">*IsEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b219d-110">Typ: **booleschen**</span><span class="sxs-lookup"><span data-stu-id="b219d-110">Type: **boolean**</span></span>

<span data-ttu-id="b219d-111">**True** gibt an, dass das Gerät aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b219d-111">If **true**, the device is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b219d-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b219d-112">Return value</span></span>

<span data-ttu-id="b219d-113">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b219d-113">Type: **uint32**</span></span>

<span data-ttu-id="b219d-114">Alle TPM-Fehler sowie Fehler, die für die TPM-Basisdienste spezifisch sind, können zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b219d-114">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="b219d-115">Allgemeine Rückgabecodes sind unten aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="b219d-115">Common return codes are listed below.</span></span>



| <span data-ttu-id="b219d-116">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="b219d-116">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="b219d-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b219d-117">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="b219d-118"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="b219d-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="b219d-119">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="b219d-119">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b219d-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b219d-120">Remarks</span></span>

<span data-ttu-id="b219d-121">Gemäß der Trusted Computing Group (TCG) v 1.2-Spezifikation sind nur die folgenden Befehle verfügbar, wenn sich das Gerät in einem deaktivierten Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="b219d-121">According to the Trusted Computing Group (TCG) v1.2 specification only the following commands are available when the device is in a deactivated state.</span></span>

-   <span data-ttu-id="b219d-122">TPM \_ continueselftest</span><span class="sxs-lookup"><span data-stu-id="b219d-122">TPM\_ContinueSelfTest</span></span>
-   <span data-ttu-id="b219d-123">TPM- \_ DSAP</span><span class="sxs-lookup"><span data-stu-id="b219d-123">TPM\_DSAP</span></span>
-   <span data-ttu-id="b219d-124">TPM \_ flushspecific</span><span class="sxs-lookup"><span data-stu-id="b219d-124">TPM\_FlushSpecific</span></span>
-   <span data-ttu-id="b219d-125">TPM- \_ getcapability</span><span class="sxs-lookup"><span data-stu-id="b219d-125">TPM\_GetCapability</span></span>
-   <span data-ttu-id="b219d-126">TPM \_ gettestresult</span><span class="sxs-lookup"><span data-stu-id="b219d-126">TPM\_GetTestResult</span></span>
-   <span data-ttu-id="b219d-127">TPM- \_ Init</span><span class="sxs-lookup"><span data-stu-id="b219d-127">TPM\_Init</span></span>
-   <span data-ttu-id="b219d-128">TPM- \_ OIAP</span><span class="sxs-lookup"><span data-stu-id="b219d-128">TPM\_OIAP</span></span>
-   <span data-ttu-id="b219d-129">TPM- \_ OSAP</span><span class="sxs-lookup"><span data-stu-id="b219d-129">TPM\_OSAP</span></span>
-   <span data-ttu-id="b219d-130">TPM-Besitzer \_ setdeaktivierung</span><span class="sxs-lookup"><span data-stu-id="b219d-130">TPM\_OwnerSetDisable</span></span>
-   <span data-ttu-id="b219d-131">TPM- \_ PCR- \_ zurück Setzung</span><span class="sxs-lookup"><span data-stu-id="b219d-131">TPM\_PCR\_Reset</span></span>
-   <span data-ttu-id="b219d-132">TPM- \_ physicaldeaktivieren</span><span class="sxs-lookup"><span data-stu-id="b219d-132">TPM\_PhysicalDisable</span></span>
-   <span data-ttu-id="b219d-133">TPM- \_ physicalenable</span><span class="sxs-lookup"><span data-stu-id="b219d-133">TPM\_PhysicalEnable</span></span>
-   <span data-ttu-id="b219d-134">TPM \_ physicalsetdeaktiviert</span><span class="sxs-lookup"><span data-stu-id="b219d-134">TPM\_PhysicalSetDeactivated</span></span>
-   <span data-ttu-id="b219d-135">TPM- \_ zurück Setzung</span><span class="sxs-lookup"><span data-stu-id="b219d-135">TPM\_Reset</span></span>
-   <span data-ttu-id="b219d-136">TPM- \_ SaveState</span><span class="sxs-lookup"><span data-stu-id="b219d-136">TPM\_SaveState</span></span>
-   <span data-ttu-id="b219d-137">TPM \_ selftestfull</span><span class="sxs-lookup"><span data-stu-id="b219d-137">TPM\_SelfTestFull</span></span>
-   <span data-ttu-id="b219d-138">TPM- \_ setcapability</span><span class="sxs-lookup"><span data-stu-id="b219d-138">TPM\_SetCapability</span></span>
-   <span data-ttu-id="b219d-139">TPM \_ SHA1Complete</span><span class="sxs-lookup"><span data-stu-id="b219d-139">TPM\_SHA1Complete</span></span>
-   <span data-ttu-id="b219d-140">TPM \_ SHA1Start</span><span class="sxs-lookup"><span data-stu-id="b219d-140">TPM\_SHA1Start</span></span>
-   <span data-ttu-id="b219d-141">TPM \_ SHA1Update</span><span class="sxs-lookup"><span data-stu-id="b219d-141">TPM\_SHA1Update</span></span>
-   <span data-ttu-id="b219d-142">TPM- \_ Start</span><span class="sxs-lookup"><span data-stu-id="b219d-142">TPM\_Startup</span></span>
-   <span data-ttu-id="b219d-143">TPM- \_ Besitz</span><span class="sxs-lookup"><span data-stu-id="b219d-143">TPM\_TakeOwnership</span></span>
-   <span data-ttu-id="b219d-144">TPM-Beendigungs \_ \_ handle</span><span class="sxs-lookup"><span data-stu-id="b219d-144">TPM\_Terminate\_Handle</span></span>

<span data-ttu-id="b219d-145">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="b219d-145">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b219d-146">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="b219d-146">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="b219d-147">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b219d-147">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b219d-148">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="b219d-148">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b219d-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b219d-149">Requirements</span></span>



| <span data-ttu-id="b219d-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b219d-150">Requirement</span></span> | <span data-ttu-id="b219d-151">Wert</span><span class="sxs-lookup"><span data-stu-id="b219d-151">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b219d-152">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b219d-152">Minimum supported client</span></span><br/> | <span data-ttu-id="b219d-153">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b219d-153">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="b219d-154">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b219d-154">Minimum supported server</span></span><br/> | <span data-ttu-id="b219d-155">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b219d-155">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="b219d-156">Namespace</span><span class="sxs-lookup"><span data-stu-id="b219d-156">Namespace</span></span><br/>                | <span data-ttu-id="b219d-157">Root \\ CIMV2 \\ Security- \\ mikrosofttpm</span><span class="sxs-lookup"><span data-stu-id="b219d-157">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="b219d-158">MOF</span><span class="sxs-lookup"><span data-stu-id="b219d-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b219d-159"><dt>Win32- \_ TPM. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b219d-159"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="b219d-160">DLL</span><span class="sxs-lookup"><span data-stu-id="b219d-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b219d-161"><dt>Win32- \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b219d-161"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b219d-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b219d-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b219d-163">**Win32- \_ TPM**</span><span class="sxs-lookup"><span data-stu-id="b219d-163">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="b219d-164">**Deaktivieren**</span><span class="sxs-lookup"><span data-stu-id="b219d-164">**Disable**</span></span>](disable-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="b219d-165">**Aktivieren**</span><span class="sxs-lookup"><span data-stu-id="b219d-165">**Enable**</span></span>](enable-win32-tpm.md)
</dt> </dl>

 

 

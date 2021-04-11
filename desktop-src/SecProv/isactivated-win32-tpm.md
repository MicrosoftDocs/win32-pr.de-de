---
description: Die isaktivierte Methode der Win32- \_ TPM-Klasse gibt an, ob das Gerät aktiviert ist.
ms.assetid: 862c386c-c5b5-44d2-89a5-3735b99bf8bc
title: Isaktivierte Methode der Win32_Tpm-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsActivated
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 6482163a27f211b4f4ce24284a8339f2b7254f3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217424"
---
# <a name="isactivated-method-of-the-win32_tpm-class"></a><span data-ttu-id="be33a-103">Isaktivierte Methode der Win32- \_ TPM-Klasse</span><span class="sxs-lookup"><span data-stu-id="be33a-103">IsActivated method of the Win32\_Tpm class</span></span>

<span data-ttu-id="be33a-104">Die **isaktivierte** Methode der [**Win32- \_ TPM**](win32-tpm.md) -Klasse gibt an, ob das Gerät aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="be33a-104">The **IsActivated** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether the device is activated.</span></span>

## <a name="syntax"></a><span data-ttu-id="be33a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="be33a-105">Syntax</span></span>


```mof
uint32 IsActivated(
  [out] boolean IsActivated
);
```



## <a name="parameters"></a><span data-ttu-id="be33a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="be33a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be33a-107">*Isaktiviert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="be33a-107">*IsActivated* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="be33a-108">Typ: **booleschen**</span><span class="sxs-lookup"><span data-stu-id="be33a-108">Type: **boolean**</span></span>

<span data-ttu-id="be33a-109">**True** gibt an, dass das Gerät aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="be33a-109">If **true**, the device is activated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be33a-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="be33a-110">Return value</span></span>

<span data-ttu-id="be33a-111">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="be33a-111">Type: **uint32**</span></span>

<span data-ttu-id="be33a-112">Alle TPM-Fehler sowie Fehler, die für die TPM-Basisdienste spezifisch sind, können zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="be33a-112">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="be33a-113">Allgemeine Rückgabecodes sind unten aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="be33a-113">Common return codes are listed below.</span></span>



| <span data-ttu-id="be33a-114">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="be33a-114">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="be33a-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="be33a-115">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="be33a-116"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="be33a-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="be33a-117">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="be33a-117">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="be33a-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="be33a-118">Remarks</span></span>

<span data-ttu-id="be33a-119">Die Deaktivierung ist ähnlich wie bei deaktiviertem, aber Betriebsstatus Änderungen sind möglich.</span><span class="sxs-lookup"><span data-stu-id="be33a-119">Deactivation is similar to disabled, but operational state changes are possible.</span></span> <span data-ttu-id="be33a-120">Gemäß der Trusted Computing Group (TCG) v 1.2-Spezifikation sind nur die folgenden Befehle verfügbar, wenn sich das Gerät in einem deaktivierten Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="be33a-120">According to the Trusted Computing Group (TCG) v1.2 specification only the following commands are available when the device is in a deactivated state.</span></span>

-   <span data-ttu-id="be33a-121">TPM \_ continueselftest</span><span class="sxs-lookup"><span data-stu-id="be33a-121">TPM\_ContinueSelfTest</span></span>
-   <span data-ttu-id="be33a-122">TPM- \_ DSAP</span><span class="sxs-lookup"><span data-stu-id="be33a-122">TPM\_DSAP</span></span>
-   <span data-ttu-id="be33a-123">TPM \_ flushspecific</span><span class="sxs-lookup"><span data-stu-id="be33a-123">TPM\_FlushSpecific</span></span>
-   <span data-ttu-id="be33a-124">TPM- \_ getcapability</span><span class="sxs-lookup"><span data-stu-id="be33a-124">TPM\_GetCapability</span></span>
-   <span data-ttu-id="be33a-125">TPM \_ gettestresult</span><span class="sxs-lookup"><span data-stu-id="be33a-125">TPM\_GetTestResult</span></span>
-   <span data-ttu-id="be33a-126">TPM- \_ Init</span><span class="sxs-lookup"><span data-stu-id="be33a-126">TPM\_Init</span></span>
-   <span data-ttu-id="be33a-127">TPM- \_ OIAP</span><span class="sxs-lookup"><span data-stu-id="be33a-127">TPM\_OIAP</span></span>
-   <span data-ttu-id="be33a-128">TPM- \_ OSAP</span><span class="sxs-lookup"><span data-stu-id="be33a-128">TPM\_OSAP</span></span>
-   <span data-ttu-id="be33a-129">TPM-Besitzer \_ setdeaktivierung</span><span class="sxs-lookup"><span data-stu-id="be33a-129">TPM\_OwnerSetDisable</span></span>
-   <span data-ttu-id="be33a-130">TPM- \_ PCR- \_ zurück Setzung</span><span class="sxs-lookup"><span data-stu-id="be33a-130">TPM\_PCR\_Reset</span></span>
-   <span data-ttu-id="be33a-131">TPM- \_ physicaldeaktivieren</span><span class="sxs-lookup"><span data-stu-id="be33a-131">TPM\_PhysicalDisable</span></span>
-   <span data-ttu-id="be33a-132">TPM- \_ physicalenable</span><span class="sxs-lookup"><span data-stu-id="be33a-132">TPM\_PhysicalEnable</span></span>
-   <span data-ttu-id="be33a-133">TPM \_ physicalsetdeaktiviert</span><span class="sxs-lookup"><span data-stu-id="be33a-133">TPM\_PhysicalSetDeactivated</span></span>
-   <span data-ttu-id="be33a-134">TPM- \_ zurück Setzung</span><span class="sxs-lookup"><span data-stu-id="be33a-134">TPM\_Reset</span></span>
-   <span data-ttu-id="be33a-135">TPM- \_ SaveState</span><span class="sxs-lookup"><span data-stu-id="be33a-135">TPM\_SaveState</span></span>
-   <span data-ttu-id="be33a-136">TPM \_ selftestfull</span><span class="sxs-lookup"><span data-stu-id="be33a-136">TPM\_SelfTestFull</span></span>
-   <span data-ttu-id="be33a-137">TPM- \_ setcapability</span><span class="sxs-lookup"><span data-stu-id="be33a-137">TPM\_SetCapability</span></span>
-   <span data-ttu-id="be33a-138">TPM \_ SHA1Complete</span><span class="sxs-lookup"><span data-stu-id="be33a-138">TPM\_SHA1Complete</span></span>
-   <span data-ttu-id="be33a-139">TPM \_ SHA1Start</span><span class="sxs-lookup"><span data-stu-id="be33a-139">TPM\_SHA1Start</span></span>
-   <span data-ttu-id="be33a-140">TPM \_ SHA1Update</span><span class="sxs-lookup"><span data-stu-id="be33a-140">TPM\_SHA1Update</span></span>
-   <span data-ttu-id="be33a-141">TPM- \_ Start</span><span class="sxs-lookup"><span data-stu-id="be33a-141">TPM\_Startup</span></span>
-   <span data-ttu-id="be33a-142">TPM- \_ Besitz</span><span class="sxs-lookup"><span data-stu-id="be33a-142">TPM\_TakeOwnership</span></span>
-   <span data-ttu-id="be33a-143">TPM-Beendigungs \_ \_ handle</span><span class="sxs-lookup"><span data-stu-id="be33a-143">TPM\_Terminate\_Handle</span></span>

<span data-ttu-id="be33a-144">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="be33a-144">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="be33a-145">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="be33a-145">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="be33a-146">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="be33a-146">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="be33a-147">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="be33a-147">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="be33a-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="be33a-148">Requirements</span></span>



| <span data-ttu-id="be33a-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="be33a-149">Requirement</span></span> | <span data-ttu-id="be33a-150">Wert</span><span class="sxs-lookup"><span data-stu-id="be33a-150">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="be33a-151">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="be33a-151">Minimum supported client</span></span><br/> | <span data-ttu-id="be33a-152">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="be33a-152">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="be33a-153">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="be33a-153">Minimum supported server</span></span><br/> | <span data-ttu-id="be33a-154">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="be33a-154">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="be33a-155">Namespace</span><span class="sxs-lookup"><span data-stu-id="be33a-155">Namespace</span></span><br/>                | <span data-ttu-id="be33a-156">Root \\ CIMV2 \\ Security- \\ mikrosofttpm</span><span class="sxs-lookup"><span data-stu-id="be33a-156">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="be33a-157">MOF</span><span class="sxs-lookup"><span data-stu-id="be33a-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="be33a-158"><dt>Win32- \_ TPM. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="be33a-158"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="be33a-159">DLL</span><span class="sxs-lookup"><span data-stu-id="be33a-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be33a-160"><dt>Win32- \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be33a-160"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be33a-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="be33a-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be33a-162">**Win32- \_ TPM**</span><span class="sxs-lookup"><span data-stu-id="be33a-162">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 

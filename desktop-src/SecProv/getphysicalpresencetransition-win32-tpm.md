---
description: Gibt die Benutzeraktion an, die erforderlich ist, um den physischen Anwesenheits Vorgang Trusted Platform Module (TPM) auszuführen. Verwenden Sie die setphysicalpresencerequest-Methode, um einen Vorgang anzufordern.
ms.assetid: abbd9702-c3a7-468a-bc83-2b7739d0b7bf
title: Getphysicalpresencetransition-Methode der Win32_Tpm-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetPhysicalPresenceTransition
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 4e6a3ab2295cc26cd439465b569f594dd1e0580a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352238"
---
# <a name="getphysicalpresencetransition-method-of-the-win32_tpm-class"></a><span data-ttu-id="0d907-104">Getphysicalpresencetransition-Methode der Win32- \_ TPM-Klasse</span><span class="sxs-lookup"><span data-stu-id="0d907-104">GetPhysicalPresenceTransition method of the Win32\_Tpm class</span></span>

<span data-ttu-id="0d907-105">Die **getphysicalpresencetransition** -Methode der [**Win32- \_ TPM**](win32-tpm.md) -Klasse gibt die Benutzeraktion an, die zum Durchführen der physischen Anwesenheits Operation Trusted Platform Module (TPM) erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="0d907-105">The **GetPhysicalPresenceTransition** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates the user action that is needed to perform the Trusted Platform Module (TPM) physical presence operation.</span></span> <span data-ttu-id="0d907-106">Verwenden Sie die [**setphysicalpresencerequest**](setphysicalpresencerequest-win32-tpm.md) -Methode, um einen Vorgang anzufordern.</span><span class="sxs-lookup"><span data-stu-id="0d907-106">Use the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method to request an operation.</span></span> <span data-ttu-id="0d907-107">Die erforderliche Benutzeraktion ist für den Computer zum Zeitpunkt der Herstellung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0d907-107">The required user action is set for your computer at the time of manufacture.</span></span> <span data-ttu-id="0d907-108">Normalerweise ist ein Neustart des Computers erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0d907-108">Usually a computer restart is needed.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d907-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d907-109">Syntax</span></span>


```mof
uint32 GetPhysicalPresenceTransition(
  [out] uint32 Transition
);
```



## <a name="parameters"></a><span data-ttu-id="0d907-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0d907-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d907-111">*Übergang* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0d907-111">*Transition* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d907-112">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0d907-112">Type: **uint32**</span></span>

<span data-ttu-id="0d907-113">Ein ganzzahliger Wert, der den Übergang angibt, der zum Ausführen eines physischen TPM-Anwesenheits Vorgangs erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="0d907-113">An integer value that specifies the transition needed to perform a TPM physical presence operation.</span></span>



| <span data-ttu-id="0d907-114">Wert</span><span class="sxs-lookup"><span data-stu-id="0d907-114">Value</span></span>                                                                        | <span data-ttu-id="0d907-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0d907-115">Meaning</span></span>                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0d907-116"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0d907-116"><dt>0</dt></span></span> </dl> | <span data-ttu-id="0d907-117">Es ist keine Benutzeraktion erforderlich, um einen physischen TPM-Anwesenheits Vorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="0d907-117">No user action is needed to perform a TPM physical presence operation.</span></span><br/>                                                                                                                                                                              |
| <dl> <span data-ttu-id="0d907-118"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="0d907-118"><dt>1</dt></span></span> </dl> | <span data-ttu-id="0d907-119">Um einen physischen TPM-Anwesenheits Vorgang auszuführen, muss der Benutzer den Computer Herunterfahren und dann mithilfe des Schaltflächen Einschalten wieder einschalten.</span><span class="sxs-lookup"><span data-stu-id="0d907-119">To perform a TPM physical presence operation, the user must shutdown the computer and then turn it back on by using the power button.</span></span> <span data-ttu-id="0d907-120">Der Benutzer muss physisch auf dem Computer anwesend sein, um die Änderung zu akzeptieren oder abzulehnen, wenn Sie vom BIOS aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="0d907-120">The user must be physically present at the computer to accept or reject the change when prompted by the BIOS.</span></span><br/> |
| <dl> <span data-ttu-id="0d907-121"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="0d907-121"><dt>2</dt></span></span> </dl> | <span data-ttu-id="0d907-122">Um einen physischen TPM-Anwesenheits Vorgang auszuführen, muss der Benutzer den Computer mithilfe eines warmen Neustarts neu starten.</span><span class="sxs-lookup"><span data-stu-id="0d907-122">To perform a TPM physical presence operation, the user must restart the computer by using a warm reboot.</span></span> <span data-ttu-id="0d907-123">Der Benutzer muss physisch auf dem Computer anwesend sein, um die Änderung zu akzeptieren oder abzulehnen, wenn Sie vom BIOS aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="0d907-123">The user must be physically present at the computer to accept or reject the change when prompted by the BIOS.</span></span><br/>                              |
| <dl> <span data-ttu-id="0d907-124"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="0d907-124"><dt>3</dt></span></span> </dl> | <span data-ttu-id="0d907-125">Die erforderliche Benutzeraktion ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="0d907-125">The required user action is unknown.</span></span><br/>                                                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d907-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0d907-126">Return value</span></span>

<span data-ttu-id="0d907-127">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0d907-127">Type: **uint32**</span></span>

<span data-ttu-id="0d907-128">Alle TPM-Fehler sowie Fehler, die für die TPM-Basisdienste spezifisch sind, können zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0d907-128">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="0d907-129">In der folgenden Tabelle sind einige der allgemeinen Rückgabecodes aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="0d907-129">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="0d907-130">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="0d907-130">Return code/value</span></span>                                                                                                                                                                      | <span data-ttu-id="0d907-131">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0d907-131">Description</span></span>                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0d907-132"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="0d907-132"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                      | <span data-ttu-id="0d907-133">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="0d907-133">The method was successful.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="0d907-134"><dt>**TPM \_ E- \_ ppi- \_ ACPI- \_ Fehler**</dt> <dt>2150171392 (0x80290300)</dt></span><span class="sxs-lookup"><span data-stu-id="0d907-134"><dt>**TPM\_E\_PPI\_ACPI\_FAILURE**</dt> <dt>2150171392 (0x80290300)</dt></span></span> </dl> | <span data-ttu-id="0d907-135">Ein Hardwarefehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="0d907-135">A hardware failure occurred.</span></span> <span data-ttu-id="0d907-136">Weitere Informationen hierzu erhalten Sie von Ihrem Computerhersteller.</span><span class="sxs-lookup"><span data-stu-id="0d907-136">Consult your computer manufacturer for more information.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0d907-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0d907-137">Remarks</span></span>

<span data-ttu-id="0d907-138">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="0d907-138">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0d907-139">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="0d907-139">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="0d907-140">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0d907-140">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0d907-141">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="0d907-141">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0d907-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0d907-142">Requirements</span></span>



| <span data-ttu-id="0d907-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0d907-143">Requirement</span></span> | <span data-ttu-id="0d907-144">Wert</span><span class="sxs-lookup"><span data-stu-id="0d907-144">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d907-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0d907-145">Minimum supported client</span></span><br/> | <span data-ttu-id="0d907-146">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0d907-146">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="0d907-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0d907-147">Minimum supported server</span></span><br/> | <span data-ttu-id="0d907-148">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0d907-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="0d907-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="0d907-149">Namespace</span></span><br/>                | <span data-ttu-id="0d907-150">Root \\ CIMV2 \\ Security- \\ mikrosofttpm</span><span class="sxs-lookup"><span data-stu-id="0d907-150">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="0d907-151">MOF</span><span class="sxs-lookup"><span data-stu-id="0d907-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0d907-152"><dt>Win32- \_ TPM. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0d907-152"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="0d907-153">DLL</span><span class="sxs-lookup"><span data-stu-id="0d907-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d907-154"><dt>Win32- \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d907-154"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d907-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0d907-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d907-156">**Win32- \_ TPM**</span><span class="sxs-lookup"><span data-stu-id="0d907-156">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="0d907-157">**Setphysicalpresencerequest**</span><span class="sxs-lookup"><span data-stu-id="0d907-157">**SetPhysicalPresenceRequest**</span></span>](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 

---
description: Die isendorsementkeypaunpresent-Methode der Win32- \_ TPM-Klasse gibt an, ob das Endorsement Key-paar auf dem Gerät vorhanden ist.
ms.assetid: c36cd0b5-1ac2-4fcf-b140-c5ecb0b3b211
title: Isendorsementkeypaarpresent-Methode der Win32_Tpm-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsEndorsementKeyPairPresent
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 63561a4971523fd1554e1d973861c3f0737df2ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131988"
---
# <a name="isendorsementkeypairpresent-method-of-the-win32_tpm-class"></a><span data-ttu-id="a5dd0-103">Isendorsementkeypaarpresent-Methode der Win32- \_ TPM-Klasse</span><span class="sxs-lookup"><span data-stu-id="a5dd0-103">IsEndorsementKeyPairPresent method of the Win32\_Tpm class</span></span>

<span data-ttu-id="a5dd0-104">Die **isendorsementkeypaunpresent** -Methode der [**Win32- \_ TPM**](win32-tpm.md) -Klasse gibt an, ob das Endorsement Key-paar auf dem Gerät vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a5dd0-104">The **IsEndorsementKeyPairPresent** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether the endorsement key pair exists on the device.</span></span> <span data-ttu-id="a5dd0-105">Das Endorsement Key-Paar ist erforderlich, bevor das Gerät im Besitz des Geräts sein kann.</span><span class="sxs-lookup"><span data-stu-id="a5dd0-105">The endorsement key pair is required before the device can be owned.</span></span> <span data-ttu-id="a5dd0-106">Dieses Schlüsselpaar kann mit der Methode " [**kreateendorsegmentkeypair**](createendorsementkeypair-win32-tpm.md) " erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a5dd0-106">This key pair can be created by the [**CreateEndorsementKeyPair**](createendorsementkeypair-win32-tpm.md) method.</span></span>

<span data-ttu-id="a5dd0-107">Das Gerät muss aktiviert und aktiviert sein, damit diese Methode erfolgreich ausgeführt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="a5dd0-107">The device must be enabled and activated for this method to succeed.</span></span> <span data-ttu-id="a5dd0-108">Informationen zum Aktivieren und Aktivieren eines nicht eigenen Geräts finden Sie unter der [**setphysicalpresencerequest**](setphysicalpresencerequest-win32-tpm.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="a5dd0-108">To enable and activate an unowned device, see the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5dd0-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5dd0-109">Syntax</span></span>


```mof
uint32 IsEndorsementKeyPairPresent(
  [out] boolean IsEndorsementKeyPairPresent
);
```



## <a name="parameters"></a><span data-ttu-id="a5dd0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5dd0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5dd0-111">*Isendorsementkeypaarpresent* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a5dd0-111">*IsEndorsementKeyPairPresent* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5dd0-112">Typ: **booleschen**</span><span class="sxs-lookup"><span data-stu-id="a5dd0-112">Type: **boolean**</span></span>

<span data-ttu-id="a5dd0-113">**True** gibt an, dass das Endorsement Key-paar auf dem Gerät vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a5dd0-113">If **true**, the endorsement key pair exists on the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5dd0-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a5dd0-114">Return value</span></span>

<span data-ttu-id="a5dd0-115">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a5dd0-115">Type: **uint32**</span></span>

<span data-ttu-id="a5dd0-116">Alle TPM-Fehler sowie Fehler, die für die TPM-Basisdienste spezifisch sind, können zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a5dd0-116">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="a5dd0-117">Allgemeine Rückgabecodes sind unten aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="a5dd0-117">Common return codes are listed below.</span></span>



| <span data-ttu-id="a5dd0-118">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="a5dd0-118">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="a5dd0-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a5dd0-119">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="a5dd0-120"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="a5dd0-120"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="a5dd0-121">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="a5dd0-121">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a5dd0-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a5dd0-122">Remarks</span></span>

<span data-ttu-id="a5dd0-123">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="a5dd0-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a5dd0-124">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="a5dd0-124">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="a5dd0-125">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a5dd0-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a5dd0-126">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="a5dd0-126">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a5dd0-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a5dd0-127">Requirements</span></span>



| <span data-ttu-id="a5dd0-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a5dd0-128">Requirement</span></span> | <span data-ttu-id="a5dd0-129">Wert</span><span class="sxs-lookup"><span data-stu-id="a5dd0-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5dd0-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a5dd0-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a5dd0-131">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a5dd0-131">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="a5dd0-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a5dd0-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a5dd0-133">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a5dd0-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="a5dd0-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="a5dd0-134">Namespace</span></span><br/>                | <span data-ttu-id="a5dd0-135">Root \\ CIMV2 \\ Security- \\ mikrosofttpm</span><span class="sxs-lookup"><span data-stu-id="a5dd0-135">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="a5dd0-136">MOF</span><span class="sxs-lookup"><span data-stu-id="a5dd0-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a5dd0-137"><dt>Win32- \_ TPM. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a5dd0-137"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="a5dd0-138">DLL</span><span class="sxs-lookup"><span data-stu-id="a5dd0-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5dd0-139"><dt>Win32- \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5dd0-139"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5dd0-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a5dd0-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5dd0-141">**Win32- \_ TPM**</span><span class="sxs-lookup"><span data-stu-id="a5dd0-141">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="a5dd0-142">**"Kreateendorsegmentkeypair"**</span><span class="sxs-lookup"><span data-stu-id="a5dd0-142">**CreateEndorsementKeyPair**</span></span>](createendorsementkeypair-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="a5dd0-143">**Setphysicalpresencerequest**</span><span class="sxs-lookup"><span data-stu-id="a5dd0-143">**SetPhysicalPresenceRequest**</span></span>](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 

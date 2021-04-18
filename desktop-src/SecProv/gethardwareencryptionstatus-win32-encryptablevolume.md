---
description: Bestimmt, ob sich das Volume auf einem Laufwerk befindet, das die Hardware Verschlüsselung unterstützt oder unterstützt.
ms.assetid: C6007BC4-71CD-404A-A0E9-D9662906151F
title: Gethardwareverschlüsseltionstatus-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetHardwareEncryptionStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 2f48bb7115d19779f437a849078238cee967f2d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345033"
---
# <a name="gethardwareencryptionstatus-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="e9eb2-103">Gethardwareverschlüsseltionstatus-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="e9eb2-103">GetHardwareEncryptionStatus method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="e9eb2-104">Die **gethardwareverschlüsseltionstatus** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " bestimmt, ob sich das Volume auf einem Laufwerk befindet, das die Hardware Verschlüsselung unterstützt oder unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e9eb2-104">The **GetHardwareEncryptionStatus** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class determines whether the volume is located on a drive that supports or can support hardware encryption.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9eb2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9eb2-105">Syntax</span></span>


```mof
uint32 GetHardwareEncryptionStatus(
  [out] uint32 HardwareEncryptionStatus
);
```



## <a name="parameters"></a><span data-ttu-id="e9eb2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9eb2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9eb2-107">*Hardwareverschlüsselungsstatus* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e9eb2-107">*HardwareEncryptionStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9eb2-108">Gibt an, ob das Laufwerk die Hardware Verschlüsselung unterstützen kann.</span><span class="sxs-lookup"><span data-stu-id="e9eb2-108">Specifies whether the drive can support hardware encryption.</span></span> <span data-ttu-id="e9eb2-109">Dies kann einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="e9eb2-109">This can be one of the following values.</span></span>



| <span data-ttu-id="e9eb2-110">Wert</span><span class="sxs-lookup"><span data-stu-id="e9eb2-110">Value</span></span>                                                                                                                                                                                                                                               | <span data-ttu-id="e9eb2-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e9eb2-111">Meaning</span></span>                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="Not_supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span><dl> <span data-ttu-id="e9eb2-112"><dt>**Nicht unterstützt**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e9eb2-112"><dt>**Not supported**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="e9eb2-113">Die Hardware Verschlüsselung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e9eb2-113">Hardware encryption is not supported.</span></span><br/>    |
| <span id="No_protection"></span><span id="no_protection"></span><span id="NO_PROTECTION"></span><dl> <span data-ttu-id="e9eb2-114"><dt>**Kein Schutz**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e9eb2-114"><dt>**No protection**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="e9eb2-115">Laufwerk Verschlüsselung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e9eb2-115">Drive encryption is not supported.</span></span><br/>       |
| <span id="Uses_software"></span><span id="uses_software"></span><span id="USES_SOFTWARE"></span><dl> <span data-ttu-id="e9eb2-116"><dt>**Verwendet Software**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e9eb2-116"><dt>**Uses software**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="e9eb2-117">Die Verschlüsselungsmethode ist Software basiert.</span><span class="sxs-lookup"><span data-stu-id="e9eb2-117">The encryption method is software-based.</span></span><br/> |
| <span id="Uses_hardware"></span><span id="uses_hardware"></span><span id="USES_HARDWARE"></span><dl> <span data-ttu-id="e9eb2-118"><dt>**Verwendung von Hardware**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e9eb2-118"><dt>**Uses hardware**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="e9eb2-119">Das Laufwerk unterstützt die Hardware Verschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="e9eb2-119">The drive supports hardware encryption.</span></span><br/>  |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9eb2-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e9eb2-120">Return value</span></span>

<span data-ttu-id="e9eb2-121">Diese Funktion gibt 0 (null) zurück, wenn das Volume mit der BitLocker-Hardware Verschlüsselung kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="e9eb2-121">This function returns zero (0) if the volume is compatible with BitLocker hardware encryption.</span></span> <span data-ttu-id="e9eb2-122">Andernfalls gibt die Funktion einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="e9eb2-122">Otherwise, the function returns an error.</span></span>



| <span data-ttu-id="e9eb2-123">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="e9eb2-123">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="e9eb2-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e9eb2-124">Description</span></span>                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e9eb2-125"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="e9eb2-125"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="e9eb2-126">Das Volume ist mit der BitLocker-Hardware Verschlüsselung kompatibel.</span><span class="sxs-lookup"><span data-stu-id="e9eb2-126">The volume is compatible with BitLocker hardware encryption.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e9eb2-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e9eb2-127">Requirements</span></span>



| <span data-ttu-id="e9eb2-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e9eb2-128">Requirement</span></span> | <span data-ttu-id="e9eb2-129">Wert</span><span class="sxs-lookup"><span data-stu-id="e9eb2-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9eb2-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e9eb2-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e9eb2-131">Nur Windows 8 Enterprise, Windows 8 pro \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e9eb2-131">Windows 8 Enterprise, Windows 8 Pro \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e9eb2-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e9eb2-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e9eb2-133">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e9eb2-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e9eb2-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="e9eb2-134">Namespace</span></span><br/>                | <span data-ttu-id="e9eb2-135">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="e9eb2-135">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="e9eb2-136">MOF</span><span class="sxs-lookup"><span data-stu-id="e9eb2-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e9eb2-137"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e9eb2-137"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9eb2-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e9eb2-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9eb2-139">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="e9eb2-139">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 





---
description: 'UnlockWithPassphrase-Methode der Win32_EncryptableVolume Klasse: Verwendet die Passphrase, um den abgeleiteten Schlüssel zu erhalten.'
ms.assetid: 09b4ae7f-7084-42bd-8bbe-da686d6280e9
title: UnlockWithPassphrase-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithPassphrase
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 0206bf7884ffa204bc768ddfcf5a4a590bf25b60
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116458"
---
# <a name="unlockwithpassphrase-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="ea056-103">UnlockWithPassphrase-Methode der Win32 \_ EncryptableVolume-Klasse</span><span class="sxs-lookup"><span data-stu-id="ea056-103">UnlockWithPassphrase method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="ea056-104">Die **UnlockWithPassphrase-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) verwendet die Passphrase, um den abgeleiteten Schlüssel zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ea056-104">The **UnlockWithPassphrase** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses the passphrase to obtain the derived key.</span></span> <span data-ttu-id="ea056-105">Nachdem der abgeleitete Schlüssel berechnet wurde, wird der abgeleitete Schlüssel verwendet, um den Hauptschlüssel des verschlüsselten Volumes zu entsperren.</span><span class="sxs-lookup"><span data-stu-id="ea056-105">After the derived key is calculated, the derived key is used to unlock the encrypted volume's master key.</span></span>

> [!Note]  
> <span data-ttu-id="ea056-106">Wenn der Datenträger Hardwareverschlüsselung unterstützt, legt diese Funktion den Bandstatus auf "Entsperrt" fest.</span><span class="sxs-lookup"><span data-stu-id="ea056-106">If the disc supports hardware encryption this function sets the band status to "unlocked""</span></span>

 

## <a name="syntax"></a><span data-ttu-id="ea056-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea056-107">Syntax</span></span>


```mof
uint32 UnlockWithPassphrase(
  [in] string Passphrase
);
```



## <a name="parameters"></a><span data-ttu-id="ea056-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea056-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea056-109">*Passphrase* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ea056-109">*Passphrase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea056-110">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ea056-110">Type: **string**</span></span>

<span data-ttu-id="ea056-111">Eine Zeichenfolge, die die Passphrase angibt.</span><span class="sxs-lookup"><span data-stu-id="ea056-111">A string that specifies the passphrase.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea056-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ea056-112">Return value</span></span>

<span data-ttu-id="ea056-113">Typ: **uint32**</span><span class="sxs-lookup"><span data-stu-id="ea056-113">Type: **uint32**</span></span>

<span data-ttu-id="ea056-114">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="ea056-114">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="ea056-115">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="ea056-115">Return code/value</span></span>                                                                                                                                                                                       | <span data-ttu-id="ea056-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ea056-116">Description</span></span>                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ea056-117"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="ea056-117"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                       | <span data-ttu-id="ea056-118">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="ea056-118">The method was successful.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="ea056-119"><dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="ea056-119"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>                      | <span data-ttu-id="ea056-120">BitLocker ist auf dem Volume nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ea056-120">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="ea056-121">Fügen Sie eine Schlüsselschutzvorrichtung hinzu, um BitLocker zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="ea056-121">Add a key protector to enable BitLocker.</span></span> <br/>                              |
| <dl> <span data-ttu-id="ea056-122"><dt>**FVE \_ E \_ FIPS \_ VERHINDERT \_ PASSPHRASE**</dt> <dt>2150695020 (0x8031006C)</dt></span><span class="sxs-lookup"><span data-stu-id="ea056-122"><dt>**FVE\_E\_FIPS\_PREVENTS\_PASSPHRASE**</dt> <dt>2150695020 (0x8031006C)</dt></span></span> </dl>          | <span data-ttu-id="ea056-123">Die Gruppenrichtlinieneinstellung, die FIPS-Konformität erfordert, hat verhindert, dass die Passphrase generiert oder verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ea056-123">The group policy setting that requires FIPS compliance prevented the passphrase from being generated or used.</span></span> <br/> |
| <dl> <span data-ttu-id="ea056-124"><dt>**FVE \_ E \_ POLICY \_ INVALID \_ PASSPHRASE \_ LENGTH**</dt> <dt>2150695040 (0x80310080)</dt></span><span class="sxs-lookup"><span data-stu-id="ea056-124"><dt>**FVE\_E\_POLICY\_INVALID\_PASSPHRASE\_LENGTH**</dt> <dt>2150695040 (0x80310080)</dt></span></span> </dl> | <span data-ttu-id="ea056-125">Die bereitgestellte Passphrase erfüllt nicht die Mindest- oder Höchstlängenanforderungen.</span><span class="sxs-lookup"><span data-stu-id="ea056-125">The passphrase provided does not meet the minimum or maximum length requirements.</span></span><br/>                              |
| <dl> <span data-ttu-id="ea056-126"><dt>**FVE \_ E \_ POLICY \_ PASSPHRASE \_ TOO \_ SIMPLE**</dt> <dt>2150695041 (0x80310081)</dt></span><span class="sxs-lookup"><span data-stu-id="ea056-126"><dt>**FVE\_E\_POLICY\_PASSPHRASE\_TOO\_SIMPLE**</dt> <dt>2150695041 (0x80310081)</dt></span></span> </dl>     | <span data-ttu-id="ea056-127">Die Passphrase erfüllt nicht die Komplexitätsanforderungen, die der Administrator in der Gruppenrichtlinie festgelegt hat.</span><span class="sxs-lookup"><span data-stu-id="ea056-127">The passphrase does not meet the complexity requirements set by the administrator in group policy.</span></span><br/>             |
| <dl> <span data-ttu-id="ea056-128"><dt>**FVE \_ E \_ FAILED \_ AUTHENTICATION**</dt> <dt>2150694951 (0x80310027)</dt></span><span class="sxs-lookup"><span data-stu-id="ea056-128"><dt>**FVE\_E\_FAILED\_AUTHENTICATION**</dt> <dt>2150694951 (0x80310027)</dt></span></span> </dl>              | <span data-ttu-id="ea056-129">Das Volume kann nicht mit den bereitgestellten Informationen entsperrt werden.</span><span class="sxs-lookup"><span data-stu-id="ea056-129">The volume cannot be unlocked with the provided information.</span></span> <br/>                                                  |
| <dl> <span data-ttu-id="ea056-130"><dt>**FVE \_ \_E-SCHUTZVORRICHTUNG \_ NICHT \_ GEFUNDEN**</dt> <dt>2150694963 (0x80310033)</dt></span><span class="sxs-lookup"><span data-stu-id="ea056-130"><dt>**FVE\_E\_PROTECTOR\_NOT\_FOUND**</dt> <dt>2150694963 (0x80310033)</dt></span></span> </dl>               | <span data-ttu-id="ea056-131">Die bereitgestellte Schlüsselschutzvorrichtung ist auf dem Volume nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ea056-131">The provided key protector does not exist on the volume.</span></span> <span data-ttu-id="ea056-132">Sie müssen eine andere Schlüsselschutzvorrichtung eingeben.</span><span class="sxs-lookup"><span data-stu-id="ea056-132">You must enter another key protector.</span></span><br/>                 |



 

## <a name="requirements"></a><span data-ttu-id="ea056-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ea056-133">Requirements</span></span>



| <span data-ttu-id="ea056-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ea056-134">Requirement</span></span> | <span data-ttu-id="ea056-135">Wert</span><span class="sxs-lookup"><span data-stu-id="ea056-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea056-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ea056-136">Minimum supported client</span></span><br/> | <span data-ttu-id="ea056-137">Nur Windows 7 Enterprise- und Windows 7 \[ Ultimate-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ea056-137">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ea056-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ea056-138">Minimum supported server</span></span><br/> | <span data-ttu-id="ea056-139">Nur Windows Server 2008 \[ R2-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ea056-139">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ea056-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="ea056-140">Namespace</span></span><br/>                | <span data-ttu-id="ea056-141">Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="ea056-141">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="ea056-142">MOF</span><span class="sxs-lookup"><span data-stu-id="ea056-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ea056-143"><dt>Win32 \_ encryptablevolume.mof</dt></span><span class="sxs-lookup"><span data-stu-id="ea056-143"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea056-144">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ea056-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea056-145">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="ea056-145">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 





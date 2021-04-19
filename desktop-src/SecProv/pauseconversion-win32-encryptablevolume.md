---
description: Hält die Verschlüsselung oder Entschlüsselung eines Volumes an.
ms.assetid: 3c365299-f0e1-480e-ad96-c91bb4108bb2
title: Pauseconversion-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.PauseConversion
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 1c9756da2339a6a3d8e87466651f61c8ff3f83a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363619"
---
# <a name="pauseconversion-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="bd9a4-103">Pauseconversion-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="bd9a4-103">PauseConversion method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="bd9a4-104">Die Methode " **pauseconversion** " der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " hält die Verschlüsselung oder Entschlüsselung eines Volumes an.</span><span class="sxs-lookup"><span data-stu-id="bd9a4-104">The **PauseConversion** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class pauses the encryption or decryption of a volume.</span></span>

> [!Note]  
> <span data-ttu-id="bd9a4-105">Wenn die Festplatte die Hardware Verschlüsselung unterstützt, kann diese Funktion einen Zurücksetzungs Vorgang anhalten, aber die hardwarebasierte Verschlüsselung nicht anhalten.</span><span class="sxs-lookup"><span data-stu-id="bd9a4-105">If the disc supports hardware encryption, this function can pause a wiping operation but cannot pause hardware-based encryption.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="bd9a4-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd9a4-106">Syntax</span></span>


```mof
uint32 PauseConversion();
```



## <a name="parameters"></a><span data-ttu-id="bd9a4-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="bd9a4-107">Parameters</span></span>

<span data-ttu-id="bd9a4-108">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="bd9a4-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bd9a4-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bd9a4-109">Return value</span></span>

<span data-ttu-id="bd9a4-110">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bd9a4-110">Type: **uint32**</span></span>

<span data-ttu-id="bd9a4-111">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="bd9a4-111">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="bd9a4-112">Wenn diese Methode auf einem vollständig verschlüsselten oder vollständig entschlüsselten Volume verwendet wird oder wenn die Verschlüsselung/Entschlüsselung auf dem Volume bereits angehalten wurde, wird 0 zurückgegeben, wenn keine anderen Fehler auftreten.</span><span class="sxs-lookup"><span data-stu-id="bd9a4-112">If this method is used on a fully encrypted or fully decrypted volume, or if encryption/decryption is already paused on the volume, 0 is returned assuming no other errors occur.</span></span>



| <span data-ttu-id="bd9a4-113">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="bd9a4-113">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="bd9a4-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bd9a4-114">Description</span></span>                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="bd9a4-115"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="bd9a4-115"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="bd9a4-116">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="bd9a4-116">The method was successful.</span></span><br/> |
| <dl> <span data-ttu-id="bd9a4-117"><dt>**F \_ E \_ gesperrt \_ Volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="bd9a4-117"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="bd9a4-118">Das Volume ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="bd9a4-118">The volume is locked.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="bd9a4-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bd9a4-119">Remarks</span></span>

<span data-ttu-id="bd9a4-120">Wenn diese Methode auf einem Volume mit verschlüsselter Verschlüsselung und Entschlüsselung verwendet wird, bewirkt die erfolgreiche Ausführung dieser Methode, dass " [**getkonversionstatus**](getconversionstatus-win32-encryptablevolume.md) " angibt, dass die Verschlüsselung oder Entschlüsselung angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="bd9a4-120">If this method is used on a volume with encryption/decryption in progress, successfully running this method causes [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) to indicate that encryption or decryption is paused.</span></span>

<span data-ttu-id="bd9a4-121">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="bd9a4-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="bd9a4-122">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="bd9a4-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="bd9a4-123">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="bd9a4-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="bd9a4-124">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="bd9a4-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bd9a4-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bd9a4-125">Requirements</span></span>



| <span data-ttu-id="bd9a4-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bd9a4-126">Requirement</span></span> | <span data-ttu-id="bd9a4-127">Wert</span><span class="sxs-lookup"><span data-stu-id="bd9a4-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd9a4-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bd9a4-128">Minimum supported client</span></span><br/> | <span data-ttu-id="bd9a4-129">Nur Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bd9a4-129">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="bd9a4-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bd9a4-130">Minimum supported server</span></span><br/> | <span data-ttu-id="bd9a4-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bd9a4-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bd9a4-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="bd9a4-132">Namespace</span></span><br/>                | <span data-ttu-id="bd9a4-133">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="bd9a4-133">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="bd9a4-134">MOF</span><span class="sxs-lookup"><span data-stu-id="bd9a4-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bd9a4-135"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="bd9a4-135"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd9a4-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bd9a4-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd9a4-137">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="bd9a4-137">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 

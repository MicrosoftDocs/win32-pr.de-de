---
description: Nimmt die Verschlüsselung oder Entschlüsselung eines Volumes wieder auf.
ms.assetid: e37f3e32-5510-431e-9782-11908e65300d
title: Resumeconversion-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ResumeConversion
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: eafa700f86e51310096835e2f24b53a28e66f800
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750833"
---
# <a name="resumeconversion-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="73aca-103">Resumeconversion-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="73aca-103">ResumeConversion method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="73aca-104">Die **resumeconversion** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " nimmt die Verschlüsselung oder Entschlüsselung eines Volumes wieder auf.</span><span class="sxs-lookup"><span data-stu-id="73aca-104">The **ResumeConversion** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class resumes the encryption or decryption of a volume.</span></span>

> [!Note]  
> <span data-ttu-id="73aca-105">Wenn die Festplatte die Hardware Verschlüsselung unterstützt, kann diese Funktion nur einen Zurücksetzungs Vorgang fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="73aca-105">If the disc supports hardware encryption, this function can resume a wiping operation only.</span></span> <span data-ttu-id="73aca-106">Weitere Informationen finden Sie unter " [**pauseconversion**](pauseconversion-win32-encryptablevolume.md)".</span><span class="sxs-lookup"><span data-stu-id="73aca-106">For more information, see [**PauseConversion**](pauseconversion-win32-encryptablevolume.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="73aca-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="73aca-107">Syntax</span></span>


```mof
uint32 ResumeConversion();
```



## <a name="parameters"></a><span data-ttu-id="73aca-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="73aca-108">Parameters</span></span>

<span data-ttu-id="73aca-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="73aca-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="73aca-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="73aca-110">Return value</span></span>

<span data-ttu-id="73aca-111">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="73aca-111">Type: **uint32**</span></span>

<span data-ttu-id="73aca-112">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="73aca-112">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="73aca-113">Wenn diese Methode auf einem vollständig verschlüsselten oder vollständig entschlüsselten Volume verwendet wird, oder wenn auf dem Volume bereits eine Verschlüsselung/Entschlüsselung ausgeführt wird, wird 0 zurückgegeben, wenn keine anderen Fehler auftreten.</span><span class="sxs-lookup"><span data-stu-id="73aca-113">If this method is used on a fully encrypted or fully decrypted volume, or if encryption/decryption is already in progress on the volume, 0 is returned assuming no other errors occur.</span></span>



| <span data-ttu-id="73aca-114">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="73aca-114">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="73aca-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="73aca-115">Description</span></span>                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="73aca-116"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="73aca-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="73aca-117">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="73aca-117">The method was successful.</span></span><br/> |
| <dl> <span data-ttu-id="73aca-118"><dt>**F \_ E \_ gesperrt \_ Volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="73aca-118"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="73aca-119">Das Volume ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="73aca-119">The volume is locked.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="73aca-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="73aca-120">Remarks</span></span>

<span data-ttu-id="73aca-121">Wenn diese Methode auf einem Volume mit angehaltenen Verschlüsselung/Entschlüsselung verwendet wird, bewirkt die erfolgreiche Ausführung dieser Methode, dass [**getkonversionstatus**](getconversionstatus-win32-encryptablevolume.md) anzeigt, dass die Verschlüsselung oder Entschlüsselung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="73aca-121">If this method is used on a volume with paused encryption/decryption, successfully running this method causes [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) to indicate that encryption or decryption is in progress.</span></span>

<span data-ttu-id="73aca-122">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="73aca-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="73aca-123">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="73aca-123">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="73aca-124">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="73aca-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="73aca-125">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="73aca-125">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="73aca-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="73aca-126">Requirements</span></span>



| <span data-ttu-id="73aca-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="73aca-127">Requirement</span></span> | <span data-ttu-id="73aca-128">Wert</span><span class="sxs-lookup"><span data-stu-id="73aca-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73aca-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="73aca-129">Minimum supported client</span></span><br/> | <span data-ttu-id="73aca-130">Nur Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="73aca-130">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="73aca-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="73aca-131">Minimum supported server</span></span><br/> | <span data-ttu-id="73aca-132">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="73aca-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="73aca-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="73aca-133">Namespace</span></span><br/>                | <span data-ttu-id="73aca-134">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="73aca-134">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="73aca-135">MOF</span><span class="sxs-lookup"><span data-stu-id="73aca-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="73aca-136"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="73aca-136"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73aca-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="73aca-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73aca-138">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="73aca-138">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 

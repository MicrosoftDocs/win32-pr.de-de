---
description: Gibt die in den Metadaten des Volumes verfügbare Bezeichnerzeichenfolge zurück.
ms.assetid: 0573cbcd-6fb1-4648-bb06-4433796f6bb5
title: Getidentificationfield-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetIdentificationField
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: bb70f76d9556df5bed70639471eb7a0f3afaaecc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128753"
---
# <a name="getidentificationfield-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="11fd2-103">Getidentificationfield-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="11fd2-103">GetIdentificationField method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="11fd2-104">Die **getidentificationfield** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " gibt die in den Metadaten des Volumes verfügbare Bezeichnerzeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="11fd2-104">The **GetIdentificationField** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class returns the identifier string available in the volume's metadata.</span></span>

## <a name="syntax"></a><span data-ttu-id="11fd2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="11fd2-105">Syntax</span></span>


```mof
uint32 GetIdentificationField(
  [out] string IdentificationField
);
```



## <a name="parameters"></a><span data-ttu-id="11fd2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="11fd2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11fd2-107">*Identificationfield* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="11fd2-107">*IdentificationField* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11fd2-108">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="11fd2-108">Type: **string**</span></span>

<span data-ttu-id="11fd2-109">Eine Zeichenfolge, die das Identifikations Feld angibt, das dem Volume zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="11fd2-109">A string that specifies the identification field that is assigned to the volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11fd2-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="11fd2-110">Return value</span></span>

<span data-ttu-id="11fd2-111">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="11fd2-111">Type: **uint32**</span></span>

<span data-ttu-id="11fd2-112">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="11fd2-112">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="11fd2-113">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="11fd2-113">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="11fd2-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="11fd2-114">Description</span></span>                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="11fd2-115"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="11fd2-115"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="11fd2-116">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="11fd2-116">The method was successful.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="11fd2-117"><dt>**F \_ E \_ gesperrt \_ Volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="11fd2-117"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="11fd2-118">Dieses Laufwerk ist BitLocker-Laufwerkverschlüsselung gesperrt.</span><span class="sxs-lookup"><span data-stu-id="11fd2-118">This drive is locked by BitLocker Drive Encryption.</span></span> <span data-ttu-id="11fd2-119">Dieses Volume muss in der Systemsteuerung entsperrt werden.</span><span class="sxs-lookup"><span data-stu-id="11fd2-119">You must unlock this volume from Control Panel.</span></span> <br/> |
| <dl> <span data-ttu-id="11fd2-120"><dt>**F \_ E \_ nicht \_ aktiviert**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="11fd2-120"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="11fd2-121">BitLocker ist auf dem Volume nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="11fd2-121">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="11fd2-122">Fügen Sie eine Schlüssel Schutzvorrichtung zum Aktivieren von BitLocker hinzu.</span><span class="sxs-lookup"><span data-stu-id="11fd2-122">Add a key protector to enable BitLocker.</span></span> <br/>                    |



 

## <a name="requirements"></a><span data-ttu-id="11fd2-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11fd2-123">Requirements</span></span>



| <span data-ttu-id="11fd2-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11fd2-124">Requirement</span></span> | <span data-ttu-id="11fd2-125">Wert</span><span class="sxs-lookup"><span data-stu-id="11fd2-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11fd2-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="11fd2-126">Minimum supported client</span></span><br/> | <span data-ttu-id="11fd2-127">Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11fd2-127">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="11fd2-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="11fd2-128">Minimum supported server</span></span><br/> | <span data-ttu-id="11fd2-129">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11fd2-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="11fd2-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="11fd2-130">Namespace</span></span><br/>                | <span data-ttu-id="11fd2-131">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="11fd2-131">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="11fd2-132">MOF</span><span class="sxs-lookup"><span data-stu-id="11fd2-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="11fd2-133"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="11fd2-133"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11fd2-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11fd2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11fd2-135">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="11fd2-135">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 





---
description: Legt die angegebene Bezeichnerzeichenfolge in den Metadaten des Volumes fest.
ms.assetid: 21355669-2052-4e7a-9c9d-aaa67533dd5e
title: Die "cationfield"-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.SetIdentificationField
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: e8405be7aef91571bd3bd5d7dcb97214dcdfdb4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868191"
---
# <a name="setidentificationfield-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="2f692-103">Die Methode "nettidentificationfield" der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="2f692-103">SetIdentificationField method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="2f692-104">Mit der **setidentificationfield** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " wird die angegebene Bezeichnerzeichenfolge in den Metadaten des Volumes festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2f692-104">The **SetIdentificationField** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class sets the specified identifier string in the volume's metadata.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f692-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f692-105">Syntax</span></span>


```mof
uint32 SetIdentificationField(
  [in, optional] string IdentificationField
);
```



## <a name="parameters"></a><span data-ttu-id="2f692-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f692-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f692-107">*Identificationfield* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="2f692-107">*IdentificationField* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2f692-108">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2f692-108">Type: **string**</span></span>

<span data-ttu-id="2f692-109">Eine Zeichenfolge, die das Identifikations Feld angibt, das dem Volume zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="2f692-109">A string that specifies the identification field that is assigned to the volume.</span></span> <span data-ttu-id="2f692-110">Wenn die optionale Zeichenfolge nicht vorhanden ist, werden die Registrierungs Satz Werte verwendet.</span><span class="sxs-lookup"><span data-stu-id="2f692-110">If the optional string is not present, the registry set values are used.</span></span> <span data-ttu-id="2f692-111">Wenn die Zeichenfolge vorhanden und nicht leer ist, wird der angegebene-Wert verwendet.</span><span class="sxs-lookup"><span data-stu-id="2f692-111">If the string is present and not empty, the specified value is used.</span></span> <span data-ttu-id="2f692-112">Beim *identificationfield* -Parameter wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="2f692-112">The *IdentificationField* parameter is not case-sensitive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f692-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2f692-113">Return value</span></span>

<span data-ttu-id="2f692-114">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2f692-114">Type: **uint32**</span></span>

<span data-ttu-id="2f692-115">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="2f692-115">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="2f692-116">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="2f692-116">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="2f692-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2f692-117">Description</span></span>                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2f692-118"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="2f692-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="2f692-119">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="2f692-119">The method was successful.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="2f692-120"><dt>**F \_ E \_ gesperrt \_ Volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="2f692-120"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="2f692-121">Dieses Laufwerk ist BitLocker-Laufwerkverschlüsselung gesperrt.</span><span class="sxs-lookup"><span data-stu-id="2f692-121">This drive is locked by BitLocker Drive Encryption.</span></span> <span data-ttu-id="2f692-122">Dieses Volume muss in der Systemsteuerung entsperrt werden.</span><span class="sxs-lookup"><span data-stu-id="2f692-122">You must unlock this volume from Control Panel.</span></span> <br/> |
| <dl> <span data-ttu-id="2f692-123"><dt>**F \_ E \_ nicht \_ aktiviert**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="2f692-123"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="2f692-124">BitLocker ist auf dem Volume nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="2f692-124">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="2f692-125">Fügen Sie eine Schlüssel Schutzvorrichtung zum Aktivieren von BitLocker hinzu.</span><span class="sxs-lookup"><span data-stu-id="2f692-125">Add a key protector to enable BitLocker.</span></span> <br/>                    |



 

## <a name="requirements"></a><span data-ttu-id="2f692-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2f692-126">Requirements</span></span>



| <span data-ttu-id="2f692-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2f692-127">Requirement</span></span> | <span data-ttu-id="2f692-128">Wert</span><span class="sxs-lookup"><span data-stu-id="2f692-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f692-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2f692-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2f692-130">Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2f692-130">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2f692-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2f692-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2f692-132">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2f692-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2f692-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="2f692-133">Namespace</span></span><br/>                | <span data-ttu-id="2f692-134">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="2f692-134">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="2f692-135">MOF</span><span class="sxs-lookup"><span data-stu-id="2f692-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2f692-136"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2f692-136"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f692-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f692-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f692-138">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="2f692-138">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 





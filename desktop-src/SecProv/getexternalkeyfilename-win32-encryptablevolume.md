---
description: Gibt den Namen der Datei zurück, die den externen Schlüssel enthält.
ms.assetid: c02d8dca-f30b-4ab5-a770-1ec6ac0b81c6
title: Getexternalkeyfilename-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetExternalKeyFileName
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: bf8de41befa7414c9970ac451d34ee7c5f40dd84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344424"
---
# <a name="getexternalkeyfilename-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="08362-103">Getexternalkeyfilename-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="08362-103">GetExternalKeyFileName method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="08362-104">Die **getexternalkeyfilename** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " gibt den Namen der Datei zurück, die den externen Schlüssel enthält, wenn dieser externe Schlüssel mithilfe der [**saveexternalkeytofile**](saveexternalkeytofile-win32-encryptablevolume.md) -Methode an einem Datei Speicherort gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="08362-104">The **GetExternalKeyFileName** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class returns the name of the file that contains the external key, if this external key is saved to a file location by using the [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md) method.</span></span>

<span data-ttu-id="08362-105">Diese Methode gilt nur für Schlüssel Schutzvorrichtungen vom Typ "externer Schlüssel", "TPM und PIN und Systemstart Schlüssel" oder "TPM und Systemstart Schlüssel".</span><span class="sxs-lookup"><span data-stu-id="08362-105">This method is only applicable for key protectors of the type "External Key", "TPM And PIN And Startup Key", or "TPM And Startup Key".</span></span>

## <a name="syntax"></a><span data-ttu-id="08362-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="08362-106">Syntax</span></span>


```mof
uint32 GetExternalKeyFileName(
  [in]  string VolumeKeyProtectorID,
  [out] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="08362-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="08362-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08362-108">*Volumekeyprotectorid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08362-108">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08362-109">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="08362-109">Type: **string**</span></span>

<span data-ttu-id="08362-110">Ein eindeutiger Zeichen folgen Bezeichner zum Verwalten einer verschlüsselten volumeschlüsselschutzvorrichtung.</span><span class="sxs-lookup"><span data-stu-id="08362-110">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="08362-111">*Dateiname* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="08362-111">*FileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="08362-112">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="08362-112">Type: **string**</span></span>

<span data-ttu-id="08362-113">Eine Zeichenfolge, die den Namen der Datei mit der Erweiterung, aber ohne den Dateipfad der Datei angibt, die den externen Schlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="08362-113">A string that specifies the name with extension but without the file path, of the file that contains the external key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08362-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="08362-114">Return value</span></span>

<span data-ttu-id="08362-115">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="08362-115">Type: **uint32**</span></span>

<span data-ttu-id="08362-116">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="08362-116">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="08362-117">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="08362-117">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="08362-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="08362-118">Description</span></span>                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="08362-119"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="08362-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="08362-120">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="08362-120">The method was successful.</span></span><br/>                                                                                                                                  |
| <dl> <span data-ttu-id="08362-121"><dt>**E \_ InvalidArg**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="08362-121"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="08362-122">Der *volumekeyprotectorid-* Parameter verweist nicht auf eine Schlüssel Schutzvorrichtung vom Typ "externer Schlüssel", "TPM und PIN und Systemstart Schlüssel" oder "TPM und Systemstart Schlüssel".</span><span class="sxs-lookup"><span data-stu-id="08362-122">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "External Key", "TPM And PIN And Startup Key", or "TPM And Startup Key".</span></span><br/> |
| <dl> <span data-ttu-id="08362-123"><dt>**F \_ E \_ gesperrt \_ Volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="08362-123"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="08362-124">Das Volume ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="08362-124">The volume is locked.</span></span><br/>                                                                                                                                       |
| <dl> <span data-ttu-id="08362-125"><dt>**F \_ E \_ nicht \_ aktiviert**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="08362-125"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="08362-126">BitLocker ist auf dem Volume nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="08362-126">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="08362-127">Fügen Sie eine Schlüssel Schutzvorrichtung zum Aktivieren von BitLocker hinzu.</span><span class="sxs-lookup"><span data-stu-id="08362-127">Add a key protector to enable BitLocker.</span></span> <br/>                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="08362-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="08362-128">Remarks</span></span>

<span data-ttu-id="08362-129">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="08362-129">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="08362-130">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="08362-130">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="08362-131">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="08362-131">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="08362-132">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="08362-132">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="08362-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="08362-133">Requirements</span></span>



| <span data-ttu-id="08362-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="08362-134">Requirement</span></span> | <span data-ttu-id="08362-135">Wert</span><span class="sxs-lookup"><span data-stu-id="08362-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08362-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="08362-136">Minimum supported client</span></span><br/> | <span data-ttu-id="08362-137">Nur Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="08362-137">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="08362-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="08362-138">Minimum supported server</span></span><br/> | <span data-ttu-id="08362-139">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="08362-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="08362-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="08362-140">Namespace</span></span><br/>                | <span data-ttu-id="08362-141">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="08362-141">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="08362-142">MOF</span><span class="sxs-lookup"><span data-stu-id="08362-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="08362-143"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="08362-143"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08362-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08362-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08362-145">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="08362-145">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="08362-146">**Saveexternalkeydefile**</span><span class="sxs-lookup"><span data-stu-id="08362-146">**SaveExternalKeyToFile**</span></span>](saveexternalkeytofile-win32-encryptablevolume.md)
</dt> </dl>

 

 

---
description: Schreibt den externen Schlüssel, der der angegebenen volumeschlüsselschutzvorrichtung zugeordnet ist, in eine ausgeblendete, schreibgeschützte Datei im angegebenen Ordner.
ms.assetid: 8d928f85-b392-4119-aebb-f16021eb5c6a
title: Saveexternalkeyyfile-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.SaveExternalKeyToFile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 879536940ff36a005e1936dffcd7821fff585a65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349962"
---
# <a name="saveexternalkeytofile-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="79913-103">Saveexternalkeyyfile-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="79913-103">SaveExternalKeyToFile method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="79913-104">Die **saveexternalkeytofile** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " schreibt den externen Schlüssel, der der angegebenen volumeschlüsselschutzvorrichtung zugeordnet ist, in eine ausgeblendete, schreibgeschützte Datei im angegebenen Ordner.</span><span class="sxs-lookup"><span data-stu-id="79913-104">The **SaveExternalKeyToFile** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class writes the external key associated with the specified volume key protector to a system, hidden, read-only file in the specified folder.</span></span>

<span data-ttu-id="79913-105">Diese Methode ist nur für Schlüssel Schutzvorrichtungen vom Typ "externer Schlüssel" oder "TPM und Systemstart Schlüssel" anwendbar.</span><span class="sxs-lookup"><span data-stu-id="79913-105">This method is only applicable for key protectors of the type "External Key" or "TPM And Startup Key".</span></span>

## <a name="syntax"></a><span data-ttu-id="79913-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="79913-106">Syntax</span></span>


```mof
uint32 SaveExternalKeyToFile(
  [in] string VolumeKeyProtectorID,
  [in] string Path
);
```



## <a name="parameters"></a><span data-ttu-id="79913-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="79913-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79913-108">*Volumekeyprotectorid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="79913-108">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79913-109">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="79913-109">Type: **string**</span></span>

<span data-ttu-id="79913-110">Ein eindeutiger Zeichen folgen Bezeichner zum Verwalten einer verschlüsselten volumeschlüsselschutzvorrichtung.</span><span class="sxs-lookup"><span data-stu-id="79913-110">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="79913-111">*Pfad* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="79913-111">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79913-112">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="79913-112">Type: **string**</span></span>

<span data-ttu-id="79913-113">Eine Zeichenfolge, die das Volume oder den Ordner Speicherort enthält, an dem der der angegebenen Schlüssel Schutzvorrichtung zugeordnete externe Schlüssel gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="79913-113">A string that contains the volume or folder location where the external key associated with the specified key protector is to be saved.</span></span> <span data-ttu-id="79913-114">Dieser Pfad enthält nicht den Namen der Datei, die intern ist und sich von Version zu Version ändern kann.</span><span class="sxs-lookup"><span data-stu-id="79913-114">This path does not include the name of the file, which is internal and may change from version to version.</span></span> <span data-ttu-id="79913-115">Verwenden Sie **getexternalkeyfilename** , um den Dateinamen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="79913-115">Use **GetExternalKeyFileName** to get the file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79913-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="79913-116">Return value</span></span>

<span data-ttu-id="79913-117">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79913-117">Type: **uint32**</span></span>

<span data-ttu-id="79913-118">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="79913-118">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="79913-119">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="79913-119">Return code/value</span></span>                                                                                                                                                                   | <span data-ttu-id="79913-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="79913-120">Description</span></span>                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="79913-121"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="79913-121"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                   | <span data-ttu-id="79913-122">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="79913-122">The method was successful.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="79913-123"><dt>**F \_ E \_ gesperrt \_ Volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="79913-123"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>  | <span data-ttu-id="79913-124">Das Volume ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="79913-124">The volume is locked.</span></span><br/>                                                                                                                  |
| <dl> <span data-ttu-id="79913-125"><dt>**E \_ InvalidArg**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="79913-125"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>           | <span data-ttu-id="79913-126">Der *volumekeyprotectorid-* Parameter verweist nicht auf eine Schlüssel Schutzvorrichtung vom Typ "externer Schlüssel" oder "TPM und Systemstart Schlüssel".</span><span class="sxs-lookup"><span data-stu-id="79913-126">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "External Key" or "TPM And Startup Key".</span></span><br/>            |
| <dl> <span data-ttu-id="79913-127"><dt>**Fehler \_ Der Pfad wurde \_ nicht \_ gefunden**</dt> <dt>2147942403 (0x80070003)</dt> .</span><span class="sxs-lookup"><span data-stu-id="79913-127"><dt>**ERROR\_PATH\_NOT\_FOUND**</dt> <dt>2147942403 (0x80070003)</dt></span></span> </dl> | <span data-ttu-id="79913-128">Der *path* -Parameter verweist nicht auf einen gültigen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="79913-128">The *Path* parameter does not refer to a valid location.</span></span><br/> <span data-ttu-id="79913-129">Stellen Sie sicher, dass der Dateiname nicht im *path* -Parameter enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="79913-129">Ensure that the file name is not included in the *Path* parameter.</span></span><br/> |
| <dl> <span data-ttu-id="79913-130"><dt>**F \_ E \_ nicht \_ aktiviert**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="79913-130"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>  | <span data-ttu-id="79913-131">BitLocker ist auf dem Volume nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="79913-131">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="79913-132">Fügen Sie eine Schlüssel Schutzvorrichtung zum Aktivieren von BitLocker hinzu.</span><span class="sxs-lookup"><span data-stu-id="79913-132">Add a key protector to enable BitLocker.</span></span> <br/>                                                      |



 

## <a name="remarks"></a><span data-ttu-id="79913-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="79913-133">Remarks</span></span>

<span data-ttu-id="79913-134">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="79913-134">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="79913-135">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="79913-135">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="79913-136">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="79913-136">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="79913-137">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="79913-137">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="79913-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="79913-138">Requirements</span></span>



| <span data-ttu-id="79913-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="79913-139">Requirement</span></span> | <span data-ttu-id="79913-140">Wert</span><span class="sxs-lookup"><span data-stu-id="79913-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79913-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="79913-141">Minimum supported client</span></span><br/> | <span data-ttu-id="79913-142">Nur Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="79913-142">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="79913-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="79913-143">Minimum supported server</span></span><br/> | <span data-ttu-id="79913-144">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="79913-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="79913-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="79913-145">Namespace</span></span><br/>                | <span data-ttu-id="79913-146">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="79913-146">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="79913-147">MOF</span><span class="sxs-lookup"><span data-stu-id="79913-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="79913-148"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="79913-148"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79913-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79913-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79913-150">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="79913-150">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 

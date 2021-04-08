---
description: Verwendet ein bereitgestelltes numerisches Kennwort für den Zugriff auf den Inhalt eines Datenvolumens.
ms.assetid: ee968372-18a4-4748-ab18-2f1b8d297f0e
title: Unlockwithnumericalpassword-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithNumericalPassword
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 09676e4a57e03f86b18259a7ffb472a6682eafd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862275"
---
# <a name="unlockwithnumericalpassword-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="85145-103">Unlockwithnumericalpassword-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="85145-103">UnlockWithNumericalPassword method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="85145-104">Die **unlockwithnumericalpassword** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " verwendet ein bereitgestelltes numerisches Kennwort für den Zugriff auf den Inhalt eines Datenvolumens.</span><span class="sxs-lookup"><span data-stu-id="85145-104">The **UnlockWithNumericalPassword** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses a provided numerical password to access the contents of a data volume.</span></span>

<span data-ttu-id="85145-105">Der Verschlüsselungsschlüssel des Volumes muss mit einer oder mehreren Schlüssel Schutzvorrichtungen des Typs "numerisches Kennwort" gesichert werden (mithilfe der [**protectkeywithnumericalpassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) -Methode), um das Volume mit dieser Methode entsperren zu können.</span><span class="sxs-lookup"><span data-stu-id="85145-105">The volume's encryption key must have been secured with one or more key protectors of the type "Numerical Password" (by using the [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) method) to be able to unlock the volume with this method.</span></span>

> [!Note]  
> <span data-ttu-id="85145-106">Wenn die Festplatte Hardware Verschlüsselung unterstützt, legt diese Funktion den Bandstatus auf "entsperrt" fest.</span><span class="sxs-lookup"><span data-stu-id="85145-106">If the disc supports hardware encryption this function sets the band status to "unlocked""</span></span>

 

## <a name="syntax"></a><span data-ttu-id="85145-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="85145-107">Syntax</span></span>


```mof
uint32 UnlockWithNumericalPassword(
  [in] string NumericalPassword
);
```



## <a name="parameters"></a><span data-ttu-id="85145-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="85145-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85145-109">*Numericalpassword* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="85145-109">*NumericalPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85145-110">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="85145-110">Type: **string**</span></span>

<span data-ttu-id="85145-111">Eine Zeichenfolge, die das numerische Kennwort angibt.</span><span class="sxs-lookup"><span data-stu-id="85145-111">A string that specifies the numerical password.</span></span>

<span data-ttu-id="85145-112">Das numerische Kennwort muss 48 Ziffern enthalten.</span><span class="sxs-lookup"><span data-stu-id="85145-112">The numerical password must contain 48 digits.</span></span> <span data-ttu-id="85145-113">Diese Ziffern können in 8 Gruppen mit 6 Ziffern aufgeteilt werden, wobei die letzte Ziffer in jeder Gruppe einen Prüfsummen Wert für die Gruppe angibt.</span><span class="sxs-lookup"><span data-stu-id="85145-113">These digits can be divided into 8 groups of 6 digits, with the last digit in each group indicating a checksum value for the group.</span></span> <span data-ttu-id="85145-114">Jede Gruppe von 6 Ziffern muss von 11 teilbar sein und muss kleiner als 65536 sein.</span><span class="sxs-lookup"><span data-stu-id="85145-114">Each group of 6 digits must be divisible by 11 and must be less than 65536.</span></span> <span data-ttu-id="85145-115">Wenn eine Gruppe von sechs Ziffern als x1, x2, X3, X4, x5 und x6 bezeichnet wird, wird die Ziffer "Prüfsumme x6" als "– x1 + x2 – X3 + X4 – x5 mod 11" berechnet.</span><span class="sxs-lookup"><span data-stu-id="85145-115">Assuming a group of six digits is labeled as x1, x2, x3, x4, x5, and x6, the checksum x6 digit is calculated as –x1+x2–x3+x4–x5 mod 11.</span></span>

<span data-ttu-id="85145-116">Die Gruppen von Ziffern können optional durch ein Leerzeichen oder einen Bindestrich getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="85145-116">The groups of digits can optionally be separated by a space or hyphen.</span></span> <span data-ttu-id="85145-117">"Xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" oder "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" kann daher auch gültige numerische Kenn Wörter enthalten.</span><span class="sxs-lookup"><span data-stu-id="85145-117">Therefore, "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" or "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" may also contain valid numerical passwords.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85145-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="85145-118">Return value</span></span>

<span data-ttu-id="85145-119">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="85145-119">Type: **uint32**</span></span>

<span data-ttu-id="85145-120">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="85145-120">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="85145-121">Wenn das Volume bereits entsperrt ist und keine weiteren Fehler auftreten, gibt diese Methode 0 zurück.</span><span class="sxs-lookup"><span data-stu-id="85145-121">If the volume is already unlocked and no other errors occur, this method returns 0.</span></span>



| <span data-ttu-id="85145-122">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="85145-122">Return code/value</span></span>                                                                                                                                                                             | <span data-ttu-id="85145-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="85145-123">Description</span></span>                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="85145-124"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="85145-124"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                             | <span data-ttu-id="85145-125">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="85145-125">The method was successful.</span></span><br/>                                                                                                                                                                                          |
| <dl> <span data-ttu-id="85145-126"><dt>**F \_ E \_ nicht \_ aktiviert**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="85145-126"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>            | <span data-ttu-id="85145-127">BitLocker ist auf dem Volume nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="85145-127">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="85145-128">Fügen Sie eine Schlüssel Schutzvorrichtung zum Aktivieren von BitLocker hinzu.</span><span class="sxs-lookup"><span data-stu-id="85145-128">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                                                                   |
| <dl> <span data-ttu-id="85145-129"><dt>**F \_ E \_ Protector \_ nicht \_ gefunden**</dt> <dt>2150694963 (0x80310033)</dt></span><span class="sxs-lookup"><span data-stu-id="85145-129"><dt>**FVE\_E\_PROTECTOR\_NOT\_FOUND**</dt> <dt>2150694963 (0x80310033)</dt></span></span> </dl>     | <span data-ttu-id="85145-130">Das Volume weist keine Schlüssel Schutzvorrichtung des Typs "numerisches Kennwort" auf.</span><span class="sxs-lookup"><span data-stu-id="85145-130">The volume does not have a key protector of the type "Numerical Password".</span></span><br/> <span data-ttu-id="85145-131">Der *numericalpassword* -Parameter hat ein gültiges Format, aber Sie können kein numerisches Kennwort verwenden, um das Volume zu entsperren.</span><span class="sxs-lookup"><span data-stu-id="85145-131">The *NumericalPassword* parameter has a valid format, but you cannot use a numerical password to unlock the volume.</span></span><br/>           |
| <dl> <span data-ttu-id="85145-132"><dt>**F \_ E \_ \_**</dt> -Fehler bei Authentifizierung <dt>2150694951 (0x80310027)</dt></span><span class="sxs-lookup"><span data-stu-id="85145-132"><dt>**FVE\_E\_FAILED\_AUTHENTICATION**</dt> <dt>2150694951 (0x80310027)</dt></span></span> </dl>    | <span data-ttu-id="85145-133">Der *numericalpassword* -Parameter kann das Volume nicht entsperren.</span><span class="sxs-lookup"><span data-stu-id="85145-133">The *NumericalPassword* parameter cannot unlock the volume.</span></span><br/> <span data-ttu-id="85145-134">Mindestens eine Schlüssel Schutzvorrichtung des Typs "numerisches Kennwort" ist vorhanden, aber der angegebene *numericalpassword* -Parameter kann das Volume nicht entsperren.</span><span class="sxs-lookup"><span data-stu-id="85145-134">One or more key protectors of the type "Numerical Password" exist, but the specified *NumericalPassword* parameter cannot unlock the volume.</span></span><br/> |
| <dl> <span data-ttu-id="85145-135"><dt>**F \_ E \_ Ungültiges Kenn \_ Wort \_ Format**</dt> <dt>2150694965 (0x80310035)</dt></span><span class="sxs-lookup"><span data-stu-id="85145-135"><dt>**FVE\_E\_INVALID\_PASSWORD\_FORMAT**</dt> <dt>2150694965 (0x80310035)</dt></span></span> </dl> | <span data-ttu-id="85145-136">Der *numericalpassword* -Parameter weist kein gültiges Format auf.</span><span class="sxs-lookup"><span data-stu-id="85145-136">The *NumericalPassword* parameter does not have a valid format.</span></span><br/>                                                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="85145-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="85145-137">Remarks</span></span>

<span data-ttu-id="85145-138">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="85145-138">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="85145-139">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="85145-139">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="85145-140">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="85145-140">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="85145-141">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="85145-141">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="85145-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="85145-142">Requirements</span></span>



| <span data-ttu-id="85145-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="85145-143">Requirement</span></span> | <span data-ttu-id="85145-144">Wert</span><span class="sxs-lookup"><span data-stu-id="85145-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85145-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="85145-145">Minimum supported client</span></span><br/> | <span data-ttu-id="85145-146">Nur Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="85145-146">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="85145-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="85145-147">Minimum supported server</span></span><br/> | <span data-ttu-id="85145-148">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="85145-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="85145-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="85145-149">Namespace</span></span><br/>                | <span data-ttu-id="85145-150">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="85145-150">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="85145-151">MOF</span><span class="sxs-lookup"><span data-stu-id="85145-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="85145-152"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="85145-152"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85145-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="85145-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85145-154">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="85145-154">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 

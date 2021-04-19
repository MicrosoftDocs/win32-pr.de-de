---
description: Gibt den externen Schlüssel aus einer Datei zurück.
ms.assetid: b61b71fb-af6f-4fe3-859b-a9f2f42ca6d2
title: Getexternalkeyfromfile-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetExternalKeyFromFile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: ba0c2cf4744c12143090488d730a1d49bab9b431
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355311"
---
# <a name="getexternalkeyfromfile-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="51ad2-103">Getexternalkeyfromfile-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="51ad2-103">GetExternalKeyFromFile method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="51ad2-104">Die **getexternalkeyfromfile** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " gibt den externen Schlüssel aus einer Datei zurück, die von [**saveexternalkeytofile**](saveexternalkeytofile-win32-encryptablevolume.md)erstellt wurde, wenn der Speicherort dieser Datei ist.</span><span class="sxs-lookup"><span data-stu-id="51ad2-104">The **GetExternalKeyFromFile** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class returns the external key from a file created by [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md), given the location of that file.</span></span>

## <a name="syntax"></a><span data-ttu-id="51ad2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="51ad2-105">Syntax</span></span>


```mof
uint32 GetExternalKeyFromFile(
  [in]  string PathWithFileName,
  [out] uint8  ExternalKey[]
);
```



## <a name="parameters"></a><span data-ttu-id="51ad2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="51ad2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51ad2-107">*Pathwithfilename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="51ad2-107">*PathWithFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51ad2-108">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51ad2-108">Type: **string**</span></span>

<span data-ttu-id="51ad2-109">Eine Zeichenfolge, die den Speicherort der Datei angibt, die einen externen Schlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="51ad2-109">A string that specifies the location of the file containing an external key.</span></span>

</dd> <dt>

<span data-ttu-id="51ad2-110">*ExternalKey* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="51ad2-110">*ExternalKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="51ad2-111">Typ: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="51ad2-111">Type: **uint8\[\]**</span></span>

<span data-ttu-id="51ad2-112">Ein Bytearray, bei dem es sich um den in der Datei enthaltenen, externen 256-Bit-Schlüssel handelt, der zum Entsperren eines Volumes verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="51ad2-112">An array of bytes that is the 256-bit external key contained within the file that can be used to unlock a volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51ad2-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="51ad2-113">Return value</span></span>

<span data-ttu-id="51ad2-114">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51ad2-114">Type: **uint32**</span></span>

<span data-ttu-id="51ad2-115">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="51ad2-115">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="51ad2-116">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="51ad2-116">Return code/value</span></span>                                                                                                                                                                   | <span data-ttu-id="51ad2-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="51ad2-117">Description</span></span>                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="51ad2-118"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="51ad2-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                   | <span data-ttu-id="51ad2-119">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="51ad2-119">The method was successful.</span></span><br/>                  |
| <dl> <span data-ttu-id="51ad2-120"><dt>**E \_ InvalidArg**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="51ad2-120"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>           | <span data-ttu-id="51ad2-121">Die Datei enthält keinen externen Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="51ad2-121">The file does not contain an external key.</span></span><br/>  |
| <dl> <span data-ttu-id="51ad2-122"><dt>**Fehler \_ Die Datei wurde \_ nicht \_ gefunden**</dt> <dt>2147942402 (0x80070002)</dt> .</span><span class="sxs-lookup"><span data-stu-id="51ad2-122"><dt>**ERROR\_FILE\_NOT\_FOUND**</dt> <dt>2147942402 (0x80070002)</dt></span></span> </dl> | <span data-ttu-id="51ad2-123">Die Datei wurde am angegebenen Speicherort nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="51ad2-123">Cannot find file at the location specified.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="51ad2-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="51ad2-124">Remarks</span></span>

<span data-ttu-id="51ad2-125">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="51ad2-125">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="51ad2-126">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="51ad2-126">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="51ad2-127">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="51ad2-127">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="51ad2-128">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="51ad2-128">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="51ad2-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="51ad2-129">Requirements</span></span>



| <span data-ttu-id="51ad2-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="51ad2-130">Requirement</span></span> | <span data-ttu-id="51ad2-131">Wert</span><span class="sxs-lookup"><span data-stu-id="51ad2-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51ad2-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="51ad2-132">Minimum supported client</span></span><br/> | <span data-ttu-id="51ad2-133">Nur Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="51ad2-133">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="51ad2-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="51ad2-134">Minimum supported server</span></span><br/> | <span data-ttu-id="51ad2-135">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="51ad2-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="51ad2-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="51ad2-136">Namespace</span></span><br/>                | <span data-ttu-id="51ad2-137">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="51ad2-137">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="51ad2-138">MOF</span><span class="sxs-lookup"><span data-stu-id="51ad2-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="51ad2-139"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="51ad2-139"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51ad2-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51ad2-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51ad2-141">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="51ad2-141">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 

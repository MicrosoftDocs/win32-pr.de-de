---
description: Gibt die Version der Vollversion des Volumes zurück.
ms.assetid: 21d5bf6d-c613-4200-b35c-1bad1ee72ec7
title: GetVersion-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetVersion
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 25952c29b6db6db045fe839951d76994cc907b91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354450"
---
# <a name="getversion-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="d3a94-103">GetVersion-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="d3a94-103">GetVersion method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="d3a94-104">Die **GetVersion** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " gibt die Version der Vollversion des Volumes zurück.</span><span class="sxs-lookup"><span data-stu-id="d3a94-104">The **GetVersion** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class returns the FVE metadata version of the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3a94-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3a94-105">Syntax</span></span>


```mof
uint32 GetVersion(
  [out] uint32 Version
);
```



## <a name="parameters"></a><span data-ttu-id="d3a94-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d3a94-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3a94-107">*Version* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d3a94-107">*Version* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3a94-108">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d3a94-108">Type: **uint32**</span></span>

<span data-ttu-id="d3a94-109">Eine Ganzzahl ohne Vorzeichen, die die Metadatenversion des Volumes angibt.</span><span class="sxs-lookup"><span data-stu-id="d3a94-109">An unsigned integer that indicates the metadata version of the volume.</span></span>



| <span data-ttu-id="d3a94-110">Wert</span><span class="sxs-lookup"><span data-stu-id="d3a94-110">Value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="d3a94-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d3a94-111">Meaning</span></span>                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="d3a94-112"><dt>**Unbekannter**</dt> Wert <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d3a94-112"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="d3a94-113">Das Betriebssystem ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="d3a94-113">The operating system is unknown.</span></span><br/>                                                                                                                                                                                               |
| <span id="Vista"></span><span id="vista"></span><span id="VISTA"></span><dl> <span data-ttu-id="d3a94-114"><dt>**Vista**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="d3a94-114"><dt>**Vista**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="d3a94-115">Windows Vista-Format, d. h., das Volume wurde mit BitLocker auf einem Computer mit Windows Vista geschützt.</span><span class="sxs-lookup"><span data-stu-id="d3a94-115">Windows Vista format, meaning that the volume was protected with BitLocker on a computer running Windows Vista.</span></span><br/>                                                                                                                |
| <span id="Win7"></span><span id="win7"></span><span id="WIN7"></span><dl> <span data-ttu-id="d3a94-116"><dt>**Win7**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d3a94-116"><dt>**Win7**</dt> <dt>2</dt></span></span> </dl>             | <span data-ttu-id="d3a94-117">Windows 7-Format, d. h., das Volume wurde mit BitLocker auf einem Computer mit Windows 7 geschützt, oder das Metadatenformat wurde mit der [**UpgradeVolume**](upgradevolume-win32-encryptablevolume.md) -Methode aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="d3a94-117">Windows 7 format, meaning that the volume was protected with BitLocker on a computer running Windows 7 or the metadata format was upgraded by using the [**UpgradeVolume**](upgradevolume-win32-encryptablevolume.md) method.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3a94-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d3a94-118">Return value</span></span>

<span data-ttu-id="d3a94-119">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d3a94-119">Type: **uint32**</span></span>

<span data-ttu-id="d3a94-120">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="d3a94-120">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="d3a94-121">Wenn das Volume bereits entsperrt ist und keine weiteren Fehler auftreten, gibt diese Methode 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="d3a94-121">If the volume is already unlocked and no other errors occur, this method returns zero.</span></span>



| <span data-ttu-id="d3a94-122">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="d3a94-122">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="d3a94-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d3a94-123">Description</span></span>                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="d3a94-124"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="d3a94-124"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                       | <span data-ttu-id="d3a94-125">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d3a94-125">The method succeeded.</span></span><br/>                               |
| <dl> <span data-ttu-id="d3a94-126"><dt>**E \_ InvalidArg**</dt> <dt>214794287 (0xccd802f)</dt></span><span class="sxs-lookup"><span data-stu-id="d3a94-126"><dt>**E\_INVALIDARG**</dt> <dt>214794287 (0xCCD802F)</dt></span></span> </dl> | <span data-ttu-id="d3a94-127">Der Wert für den *Versions* Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="d3a94-127">The value for the *Version* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="d3a94-128"><dt>**Fehler \_ Ungültige \_ Daten**</dt> <dt>13 (0xD)</dt></span><span class="sxs-lookup"><span data-stu-id="d3a94-128"><dt>**ERROR\_INVALID\_DATA**</dt> <dt>13 (0xD)</dt></span></span> </dl>       | <span data-ttu-id="d3a94-129">Der Treiber hat ein nicht unterstütztes Datenformat zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d3a94-129">The driver returned an unsupported data format.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="d3a94-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d3a94-130">Remarks</span></span>

<span data-ttu-id="d3a94-131">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="d3a94-131">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d3a94-132">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="d3a94-132">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="d3a94-133">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d3a94-133">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d3a94-134">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="d3a94-134">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d3a94-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d3a94-135">Requirements</span></span>



| <span data-ttu-id="d3a94-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d3a94-136">Requirement</span></span> | <span data-ttu-id="d3a94-137">Wert</span><span class="sxs-lookup"><span data-stu-id="d3a94-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3a94-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d3a94-138">Minimum supported client</span></span><br/> | <span data-ttu-id="d3a94-139">Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d3a94-139">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d3a94-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d3a94-140">Minimum supported server</span></span><br/> | <span data-ttu-id="d3a94-141">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d3a94-141">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d3a94-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="d3a94-142">Namespace</span></span><br/>                | <span data-ttu-id="d3a94-143">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="d3a94-143">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="d3a94-144">MOF</span><span class="sxs-lookup"><span data-stu-id="d3a94-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d3a94-145"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d3a94-145"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3a94-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d3a94-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3a94-147">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="d3a94-147">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 

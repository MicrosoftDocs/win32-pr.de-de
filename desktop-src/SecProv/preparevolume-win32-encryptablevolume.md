---
description: Erstellt ein BitLocker-Volume mit dem angegebenen Dateisystemtyp des Discovery-Volumes.
ms.assetid: 088e7224-a336-4742-a12f-86755defe16c
title: Preparevolume-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.PrepareVolume
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 918e4289f8f2c38af2a4a51bfe92f82a74b30b22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128749"
---
# <a name="preparevolume-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="9c9b7-103">Preparevolume-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="9c9b7-103">PrepareVolume method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="9c9b7-104">Die **preparevolume** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " erstellt ein BitLocker-Volume mit dem angegebenen Dateisystemtyp des Discovery-Volumes.</span><span class="sxs-lookup"><span data-stu-id="9c9b7-104">The **PrepareVolume** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class creates a BitLocker volume with the specified file system type of the discovery volume.</span></span> <span data-ttu-id="9c9b7-105">Diese Methode muss aufgerufen werden, bevor das Volume mit einer der \**protectkeywith \** _-Methoden geschützt werden kann.</span><span class="sxs-lookup"><span data-stu-id="9c9b7-105">This method must be called before the volume can be protected with any of the \**ProtectKeyWith\** _ methods.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c9b7-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c9b7-106">Syntax</span></span>

```mof
uint32 PrepareVolume(
  [in] string DiscoveryVolumeType,
  [in] uint32 ForceEncryptionType
);
```

## <a name="parameters"></a><span data-ttu-id="9c9b7-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="9c9b7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c9b7-108">_DiscoveryVolumeType \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9c9b7-108">_DiscoveryVolumeType\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c9b7-109">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9c9b7-109">Type: **string**</span></span>

<span data-ttu-id="9c9b7-110">Eine Zeichenfolge, die den Typ des Ermittlungs Volumens angibt.</span><span class="sxs-lookup"><span data-stu-id="9c9b7-110">A string that specifies the type of discovery volume.</span></span>

| <span data-ttu-id="9c9b7-111">Wert</span><span class="sxs-lookup"><span data-stu-id="9c9b7-111">Value</span></span>               | <span data-ttu-id="9c9b7-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9c9b7-112">Meaning</span></span>                                                            |
|---------------------|--------------------------------------------------------------------|
| <span data-ttu-id="9c9b7-113">**&lt;gar&gt;**</span><span class="sxs-lookup"><span data-stu-id="9c9b7-113">**&lt;none&gt;**</span></span>    | <span data-ttu-id="9c9b7-114">Kein suchvolume.</span><span class="sxs-lookup"><span data-stu-id="9c9b7-114">No discovery volume.</span></span> <span data-ttu-id="9c9b7-115">Dieser Wert erstellt ein System eigenes BitLocker-Volume.</span><span class="sxs-lookup"><span data-stu-id="9c9b7-115">This value creates a native BitLocker volume.</span></span> |
| <span data-ttu-id="9c9b7-116">**&lt;vorgegebene&gt;**</span><span class="sxs-lookup"><span data-stu-id="9c9b7-116">**&lt;default&gt;**</span></span> | <span data-ttu-id="9c9b7-117">Dieser Wert ist das Standardverhalten.</span><span class="sxs-lookup"><span data-stu-id="9c9b7-117">This value is the default behavior.</span></span>                                |
| <span data-ttu-id="9c9b7-118">**FAT32**</span><span class="sxs-lookup"><span data-stu-id="9c9b7-118">**FAT32**</span></span>           | <span data-ttu-id="9c9b7-119">Dieser Wert erstellt ein FAT32-Ermittlungs Volume.</span><span class="sxs-lookup"><span data-stu-id="9c9b7-119">This value creates a FAT32 discovery volume.</span></span>                       |

</dd> <dt>

<span data-ttu-id="9c9b7-120">*Forceverschlüsseltiontype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9c9b7-120">*ForceEncryptionType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c9b7-121">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c9b7-121">Type: **uint32**</span></span>

<span data-ttu-id="9c9b7-122">Eine ganze Zahl, die den Verschlüsselungstyp angibt.</span><span class="sxs-lookup"><span data-stu-id="9c9b7-122">Integer that specifies the encryption type.</span></span> <span data-ttu-id="9c9b7-123">Dies kann einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="9c9b7-123">This can be one of the following values.</span></span>

| <span data-ttu-id="9c9b7-124">Wert</span><span class="sxs-lookup"><span data-stu-id="9c9b7-124">Value</span></span>                                                                                                                                                                                                                                       | <span data-ttu-id="9c9b7-125">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9c9b7-125">Meaning</span></span>                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span><dl> <span data-ttu-id="9c9b7-126"><dt>**Nicht angegeben**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9c9b7-126"><dt>**Unspecified**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="9c9b7-127">Der Verschlüsselungstyp ist nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="9c9b7-127">The encryption type is not specified.</span></span><br/> |
| <span id="Software"></span><span id="software"></span><span id="SOFTWARE"></span><dl> <span data-ttu-id="9c9b7-128"><dt>**Software**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="9c9b7-128"><dt>**Software**</dt> <dt>1</dt></span></span> </dl>             | <span data-ttu-id="9c9b7-129">Software Verschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="9c9b7-129">Software encryption.</span></span><br/>                  |
| <span id="Hardware"></span><span id="hardware"></span><span id="HARDWARE"></span><dl> <span data-ttu-id="9c9b7-130"><dt>**Hardware**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9c9b7-130"><dt>**Hardware**</dt> <dt>2</dt></span></span> </dl>             | <span data-ttu-id="9c9b7-131">Hardware Verschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="9c9b7-131">Hardware encryption.</span></span><br/>                  |

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c9b7-132">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9c9b7-132">Return value</span></span>

<span data-ttu-id="9c9b7-133">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c9b7-133">Type: **uint32**</span></span>

<span data-ttu-id="9c9b7-134">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="9c9b7-134">This method returns one of the following codes or another error code if it fails.</span></span>

| <span data-ttu-id="9c9b7-135">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="9c9b7-135">Return code/value</span></span>      | <span data-ttu-id="9c9b7-136">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9c9b7-136">Description</span></span>                     |
|------------------------|---------------------------------|
| <span data-ttu-id="9c9b7-137">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="9c9b7-137">**S_OK**</span></span> <br/> <span data-ttu-id="9c9b7-138">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="9c9b7-138">0 (0x0)</span></span> | <span data-ttu-id="9c9b7-139">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="9c9b7-139">The method was successful.</span></span><br/> |

## <a name="remarks"></a><span data-ttu-id="9c9b7-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9c9b7-140">Remarks</span></span>

<span data-ttu-id="9c9b7-141">Wenn Sie diese Methode beim Aktivieren eines BitLocker-Volumes nicht aufrufen, entspricht dies dem Aufrufen dieser Methode mit dem Standardwert im *discoveryvolumetype* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="9c9b7-141">If you do not call this method when enabling a BitLocker volume, it is the same as calling this method with the default value in the *DiscoveryVolumeType* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c9b7-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9c9b7-142">Requirements</span></span>

| <span data-ttu-id="9c9b7-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9c9b7-143">Requirement</span></span> | <span data-ttu-id="9c9b7-144">Wert</span><span class="sxs-lookup"><span data-stu-id="9c9b7-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c9b7-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9c9b7-145">Minimum supported client</span></span><br/> | <span data-ttu-id="9c9b7-146">Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9c9b7-146">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9c9b7-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9c9b7-147">Minimum supported server</span></span><br/> | <span data-ttu-id="9c9b7-148">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9c9b7-148">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9c9b7-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="9c9b7-149">Namespace</span></span><br/>                | <span data-ttu-id="9c9b7-150">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="9c9b7-150">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="9c9b7-151">MOF</span><span class="sxs-lookup"><span data-stu-id="9c9b7-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9c9b7-152"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9c9b7-152"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="9c9b7-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9c9b7-153">See also</span></span>

[<span data-ttu-id="9c9b7-154">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="9c9b7-154">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)

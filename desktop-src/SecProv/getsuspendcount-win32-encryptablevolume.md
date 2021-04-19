---
description: Ruft ab, wie oft BitLocker angehalten wurde.
ms.assetid: B8C87352-62BA-4E5D-A273-CE74F3E1A7A8
title: Getsuspendcount-Methode der Win32_EncryptableVolume-Klasse (activdbg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetSuspendCount
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: eb28f019674f39946674399f8931fb63421ef982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373222"
---
# <a name="getsuspendcount-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="0851c-103">Getsuspendcount-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="0851c-103">GetSuspendCount method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="0851c-104">Die **getsuspendcount** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " Ruft die Anzahl der Neustarts ab, bevor der Schutz automatisch fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="0851c-104">The **GetSuspendCount** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class retrieves the number of reboots before protection will automatically be resumed.</span></span>

## <a name="syntax"></a><span data-ttu-id="0851c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0851c-105">Syntax</span></span>


```mof
uint32 GetSuspendCount(
   uint32 SuspendCount
);
```



## <a name="parameters"></a><span data-ttu-id="0851c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0851c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0851c-107">*SuspendCount*</span><span class="sxs-lookup"><span data-stu-id="0851c-107">*SuspendCount*</span></span> 
</dt> <dd>

<span data-ttu-id="0851c-108">Ein ganzzahliger Wert zwischen 0 und 15.</span><span class="sxs-lookup"><span data-stu-id="0851c-108">An integer value from 0 to 15.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0851c-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0851c-109">Return value</span></span>

<span data-ttu-id="0851c-110">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="0851c-110">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="0851c-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="0851c-111">Return code</span></span>                                                                                          | <span data-ttu-id="0851c-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0851c-112">Description</span></span>                                                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0851c-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0851c-113"><dt>**S\_OK**</dt></span></span> </dl>                 | <span data-ttu-id="0851c-114">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="0851c-114">The method was successful.</span></span><br/>                                      |
| <dl> <span data-ttu-id="0851c-115"><dt>**Fehler \_ nicht \_ unterstützt**</dt></span><span class="sxs-lookup"><span data-stu-id="0851c-115"><dt>**ERROR\_NOT\_SUPPORTED**</dt></span></span> </dl> | <span data-ttu-id="0851c-116">Wird zurückgegeben, wenn das Volume nicht angehalten wird oder kein Betriebssystem Volume ist.</span><span class="sxs-lookup"><span data-stu-id="0851c-116">Returned if the volume is not suspended or is not an OS volume.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0851c-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0851c-117">Remarks</span></span>

<span data-ttu-id="0851c-118">Diese Methode gilt nur für das Betriebssystem Volume und nur, wenn Sie zu diesem Zeitpunkt tatsächlich angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="0851c-118">This method only applies to the OS volume, and only if it is actually suspended at the time.</span></span> <span data-ttu-id="0851c-119">Wenn das Volume nicht angehalten wird oder kein Betriebssystem Volume ist, wird ein Fehler zurückgegeben, der **\_ nicht \_ unterstützt** wird.</span><span class="sxs-lookup"><span data-stu-id="0851c-119">If the volume is not suspended or is not an OS volume, **ERROR\_NOT\_SUPPORTED** will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="0851c-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0851c-120">Requirements</span></span>



| <span data-ttu-id="0851c-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0851c-121">Requirement</span></span> | <span data-ttu-id="0851c-122">Wert</span><span class="sxs-lookup"><span data-stu-id="0851c-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0851c-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0851c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0851c-124">Nur Windows 8 Enterprise, Windows 8 pro \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0851c-124">Windows 8 Enterprise, Windows 8 Pro \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0851c-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0851c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0851c-126">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0851c-126">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0851c-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="0851c-127">Namespace</span></span><br/>                | <span data-ttu-id="0851c-128">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="0851c-128">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="0851c-129">Header</span><span class="sxs-lookup"><span data-stu-id="0851c-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="0851c-130"><dt>Activdbg. h</dt></span><span class="sxs-lookup"><span data-stu-id="0851c-130"><dt>Activdbg.h</dt></span></span> </dl>                   |
| <span data-ttu-id="0851c-131">MOF</span><span class="sxs-lookup"><span data-stu-id="0851c-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0851c-132"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0851c-132"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0851c-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0851c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0851c-134">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="0851c-134">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 





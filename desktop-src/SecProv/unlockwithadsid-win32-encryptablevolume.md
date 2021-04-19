---
description: Verwendet die angegebene Active Directory Sicherheits-ID (SID)-Zeichenfolge, um den abgeleiteten Schlüssel abzurufen und das verschlüsselte Volume zu entsperren.
ms.assetid: 89FBC815-859D-415A-8F26-170FB2DB7387
title: Unlockwithadsid-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithAdSid
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: cbd2a327a2ede322c01009fe32aa0492a7e65610
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352699"
---
# <a name="unlockwithadsid-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="715cf-103">Unlockwithadsid-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="715cf-103">UnlockWithAdSid method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="715cf-104">Die **unlockwithadsid** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " verwendet die angegebene Active Directory sid-Zeichenfolge (Security Identifier), um den abgeleiteten Schlüssel abzurufen und das verschlüsselte Volume zu entsperren.</span><span class="sxs-lookup"><span data-stu-id="715cf-104">The **UnlockWithAdSid** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses the provided Active Directory security identifier (SID) string to obtain the derived key and unlock the encrypted volume.</span></span>

> [!Note]  
> <span data-ttu-id="715cf-105">Wenn die Festplatte Hardware Verschlüsselung unterstützt, legt diese Funktion den Bandstatus auf "entsperrt" fest.</span><span class="sxs-lookup"><span data-stu-id="715cf-105">If the disc supports hardware encryption this function sets the band status to "unlocked""</span></span>

 

## <a name="syntax"></a><span data-ttu-id="715cf-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="715cf-106">Syntax</span></span>


```mof
uint32 UnlockWithAdSid(
  [in]  string SidString
);
```



## <a name="parameters"></a><span data-ttu-id="715cf-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="715cf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="715cf-108">*Sidstring* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="715cf-108">*SidString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="715cf-109">Eine Zeichenfolge, die die Active Directory sid enthält.</span><span class="sxs-lookup"><span data-stu-id="715cf-109">String that contains the Active Directory SID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="715cf-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="715cf-110">Return value</span></span>

<span data-ttu-id="715cf-111">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="715cf-111">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="715cf-112">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="715cf-112">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="715cf-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="715cf-113">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="715cf-114"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="715cf-114"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="715cf-115">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="715cf-115">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="715cf-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="715cf-116">Remarks</span></span>

<span data-ttu-id="715cf-117">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="715cf-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="715cf-118">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="715cf-118">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="715cf-119">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="715cf-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="715cf-120">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="715cf-120">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="715cf-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="715cf-121">Requirements</span></span>



| <span data-ttu-id="715cf-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="715cf-122">Requirement</span></span> | <span data-ttu-id="715cf-123">Wert</span><span class="sxs-lookup"><span data-stu-id="715cf-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="715cf-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="715cf-124">Minimum supported client</span></span><br/> | <span data-ttu-id="715cf-125">Nur Windows 8 Enterprise, Windows 8 pro \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="715cf-125">Windows 8 Enterprise, Windows 8 Pro \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="715cf-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="715cf-126">Minimum supported server</span></span><br/> | <span data-ttu-id="715cf-127">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="715cf-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="715cf-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="715cf-128">Namespace</span></span><br/>                | <span data-ttu-id="715cf-129">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="715cf-129">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="715cf-130">MOF</span><span class="sxs-lookup"><span data-stu-id="715cf-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="715cf-131"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="715cf-131"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="715cf-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="715cf-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="715cf-133">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="715cf-133">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 

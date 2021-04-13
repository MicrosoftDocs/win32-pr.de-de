---
description: Listet alle Zertifikate auf dem System auf, die mit den angegebenen Kriterien übereinstimmen, und gibt eine Liste von Fingerabdrücken zurück.
ms.assetid: 69522afe-9870-4ae9-8c69-cf8787913615
title: Findvalidzertifikate-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.FindValidCertificates
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 69612d860284f6a47dfa38c2aafc3e73f209c796
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347258"
---
# <a name="findvalidcertificates-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="0948a-103">Findvalidzertifikats-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="0948a-103">FindValidCertificates method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="0948a-104">Die **findvalidzertifikate** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " listet alle Zertifikate auf dem System auf, die den angegebenen Kriterien entsprechen, und gibt eine Liste von Fingerabdrücken zurück.</span><span class="sxs-lookup"><span data-stu-id="0948a-104">The **FindValidCertificates** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class enumerates all certificates on the system that match the indicated criteria and returns a list of thumbprints.</span></span> <span data-ttu-id="0948a-105">Die zurückgegebene Liste enthält nur Zertifikate mit einem gültigen [*Objekt Bezeichner*](../secgloss/o-gly.md) (OID).</span><span class="sxs-lookup"><span data-stu-id="0948a-105">The returned list only contains certificates with a valid [*object identifier*](../secgloss/o-gly.md) (OID).</span></span> <span data-ttu-id="0948a-106">Die OID ist möglicherweise der Standardwert oder kann im Gruppenrichtlinie angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0948a-106">The OID may be the default, or it may be specified in the Group Policy.</span></span>

## <a name="syntax"></a><span data-ttu-id="0948a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0948a-107">Syntax</span></span>


```mof
uint32 FindValidCertificates(
  [out] string CertificateThumbprint[]
);
```



## <a name="parameters"></a><span data-ttu-id="0948a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0948a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0948a-109">*Certifi-ethumschlag-Druck* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0948a-109">*CertificateThumbprint* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0948a-110">Typ: **Zeichen \[ \] Folge**</span><span class="sxs-lookup"><span data-stu-id="0948a-110">Type: **string\[\]**</span></span>

<span data-ttu-id="0948a-111">Ein Array von Zeichen folgen, das die Liste gültiger Zertifikate enthält.</span><span class="sxs-lookup"><span data-stu-id="0948a-111">An array of strings that contains the list of valid certificates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0948a-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0948a-112">Return value</span></span>

<span data-ttu-id="0948a-113">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0948a-113">Type: **uint32**</span></span>

<span data-ttu-id="0948a-114">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="0948a-114">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="0948a-115">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="0948a-115">Return code/value</span></span>                                                                                                                                                                           | <span data-ttu-id="0948a-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0948a-116">Description</span></span>                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="0948a-117"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="0948a-117"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                           | <span data-ttu-id="0948a-118">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="0948a-118">The method was successful.</span></span><br/>                |
| <dl> <span data-ttu-id="0948a-119"><dt>**F \_ E \_ ungültige \_ BitLocker- \_ OID**</dt> <dt>2150695022 (0x8031006e)</dt></span><span class="sxs-lookup"><span data-stu-id="0948a-119"><dt>**FVE\_E\_INVALID\_BITLOCKER\_OID**</dt> <dt>2150695022 (0x8031006E)</dt></span></span> </dl> | <span data-ttu-id="0948a-120">Die verfügbare BitLocker-OID ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="0948a-120">The available BitLocker OID is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0948a-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0948a-121">Requirements</span></span>



| <span data-ttu-id="0948a-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0948a-122">Requirement</span></span> | <span data-ttu-id="0948a-123">Wert</span><span class="sxs-lookup"><span data-stu-id="0948a-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0948a-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0948a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0948a-125">Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0948a-125">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0948a-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0948a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0948a-127">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0948a-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0948a-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="0948a-128">Namespace</span></span><br/>                | <span data-ttu-id="0948a-129">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="0948a-129">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="0948a-130">MOF</span><span class="sxs-lookup"><span data-stu-id="0948a-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0948a-131"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0948a-131"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0948a-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0948a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0948a-133">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="0948a-133">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 

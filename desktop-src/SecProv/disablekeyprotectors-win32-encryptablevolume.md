---
description: Hiermit werden alle diesem Volume zugeordneten Schlüssel Schutzvorrichtungen deaktiviert oder angehalten.
ms.assetid: 19eed858-a116-4ec8-937a-2eea7aadbdc6
title: Disablekeyprotector-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.DisableKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 1de392c50f6665d793883582e2679cd502efbe37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359072"
---
# <a name="disablekeyprotectors-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="c167e-103">Disablekeyprotector-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="c167e-103">DisableKeyProtectors method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="c167e-104">Mit der **disablekeyprotector** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " werden alle diesem Volume zugeordneten Schlüssel Schutzvorrichtungen deaktiviert oder angehalten.</span><span class="sxs-lookup"><span data-stu-id="c167e-104">The **DisableKeyProtectors** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class disables or suspends all key protectors associated with this volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="c167e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c167e-105">Syntax</span></span>


```mof
uint32 DisableKeyProtectors(
  [in, optional] uint32 DisableCount
);
```



## <a name="parameters"></a><span data-ttu-id="c167e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c167e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c167e-107">*Disablecount* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c167e-107">*DisableCount* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c167e-108">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c167e-108">Type: **uint32**</span></span>

<span data-ttu-id="c167e-109">Eine ganze Zahl, die die Anzahl der Neustarts angibt, für die die Schlüssel Schutzvorrichtungen deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="c167e-109">Integer that specifies the number of reboots for which the key protectors will be disabled.</span></span> <span data-ttu-id="c167e-110">Dieser Parameter ist nur auf Betriebssystemvolumes verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c167e-110">This parameter is only available on OS volumes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c167e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c167e-111">Return value</span></span>

<span data-ttu-id="c167e-112">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c167e-112">Type: **uint32**</span></span>

<span data-ttu-id="c167e-113">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="c167e-113">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="c167e-114">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="c167e-114">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="c167e-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c167e-115">Description</span></span>                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="c167e-116"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="c167e-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="c167e-117">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="c167e-117">The method was successful.</span></span><br/> |
| <dl> <span data-ttu-id="c167e-118"><dt>**F \_ E \_ gesperrt \_ Volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="c167e-118"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="c167e-119">Das Volume ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="c167e-119">The volume is locked.</span></span><br/>      |



 

## <a name="security-considerations"></a><span data-ttu-id="c167e-120">Überlegungen zur Sicherheit</span><span class="sxs-lookup"><span data-stu-id="c167e-120">Security Considerations</span></span>

<span data-ttu-id="c167e-121">Diese Methode macht den Verschlüsselungsschlüssel des Volumes im Klartext auf der Festplatte verfügbar und deaktiviert den volumeschutz.</span><span class="sxs-lookup"><span data-stu-id="c167e-121">This method exposes the volume's encryption key in the clear on the hard disk, turning off any volume protection.</span></span> <span data-ttu-id="c167e-122">Es wird davon abgeraten, ein Kennwort oder einen Verschlüsselungsschlüssel als Klartext anzugeben.</span><span class="sxs-lookup"><span data-stu-id="c167e-122">We recommend against having any password or encryption key in plaintext.</span></span>

## <a name="remarks"></a><span data-ttu-id="c167e-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c167e-123">Remarks</span></span>

<span data-ttu-id="c167e-124">Neue Schlüssel Schutzvorrichtungen können auch dann hinzugefügt werden, wenn Schlüssel Schutzvorrichtungen deaktiviert oder angehalten wurden.</span><span class="sxs-lookup"><span data-stu-id="c167e-124">New key protectors can be added even when key protectors are disabled or suspended.</span></span> <span data-ttu-id="c167e-125">Diese Schlüsselschutz Vorrichtungen bleiben deaktiviert, sofern [**enablekeyprotector**](enablekeyprotectors-win32-encryptablevolume.md) nicht aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c167e-125">These key protectors will remain disabled unless [**EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md) is called.</span></span>

<span data-ttu-id="c167e-126">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="c167e-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c167e-127">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="c167e-127">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="c167e-128">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c167e-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c167e-129">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="c167e-129">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c167e-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c167e-130">Requirements</span></span>



| <span data-ttu-id="c167e-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c167e-131">Requirement</span></span> | <span data-ttu-id="c167e-132">Wert</span><span class="sxs-lookup"><span data-stu-id="c167e-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c167e-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c167e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c167e-134">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="c167e-134">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="c167e-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c167e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c167e-136">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c167e-136">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c167e-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="c167e-137">Namespace</span></span><br/>                | <span data-ttu-id="c167e-138">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="c167e-138">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="c167e-139">MOF</span><span class="sxs-lookup"><span data-stu-id="c167e-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c167e-140"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c167e-140"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c167e-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c167e-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c167e-142">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="c167e-142">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="c167e-143">**Enablekeyprotector**</span><span class="sxs-lookup"><span data-stu-id="c167e-143">**EnableKeyProtectors**</span></span>](enablekeyprotectors-win32-encryptablevolume.md)
</dt> </dl>

 

 

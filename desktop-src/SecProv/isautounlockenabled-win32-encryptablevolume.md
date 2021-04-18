---
description: Gibt an, ob das Volume bei der Bereitstellung automatisch entsperrt wird.
ms.assetid: cba04d77-1e7c-4191-8eb7-b8c43694193f
title: Isautounlockaktivierte Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsAutoUnlockEnabled
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 2a144d54ff4564fa322efadd521e44c2fa9a8173
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340177"
---
# <a name="isautounlockenabled-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="3da36-103">Isautounlockaktivierte Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="3da36-103">IsAutoUnlockEnabled method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="3da36-104">Die **isautounlockaktivierte** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " gibt an, ob das Volume bei der Bereitstellung automatisch entsperrt wird (z. b. Wenn Wechselmedien mit dem Computer verbunden sind).</span><span class="sxs-lookup"><span data-stu-id="3da36-104">The **IsAutoUnlockEnabled** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates whether the volume is automatically unlocked when it is mounted (for example, when removable memory devices are connected to the computer).</span></span>

## <a name="syntax"></a><span data-ttu-id="3da36-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3da36-105">Syntax</span></span>


```mof
uint32 IsAutoUnlockEnabled(
  [out] boolean IsAutoUnlockEnabled,
  [out] string  VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="3da36-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3da36-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3da36-107">*Isautounlockaktivierte* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3da36-107">*IsAutoUnlockEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3da36-108">Typ: **booleschen**</span><span class="sxs-lookup"><span data-stu-id="3da36-108">Type: **boolean**</span></span>

<span data-ttu-id="3da36-109">Ein boolescher Wert, der true ist, wenn der zum automatischen Entsperren des Volumes verwendete externe Schlüssel vorhanden ist und auf dem momentan laufenden Betriebssystem Volume gespeichert ist, andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="3da36-109">A Boolean value that is true if the external key used to automatically unlock the volume exists and has been stored in the currently running operating system volume, otherwise it is false.</span></span>

</dd> <dt>

<span data-ttu-id="3da36-110">*Volumekeyprotectorid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3da36-110">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3da36-111">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3da36-111">Type: **string**</span></span>

<span data-ttu-id="3da36-112">Ein eindeutiger Zeichen folgen Bezeichner, der die zugeordnete verschlüsselte volumeschlüsselschutzkennung enthält, wenn *isautounlockaktiviaktiviert* ist.</span><span class="sxs-lookup"><span data-stu-id="3da36-112">A unique string identifier that contains the associated encrypted volume key protector ID if *IsAutoUnlockEnabled* is true.</span></span>

<span data-ttu-id="3da36-113">Wenn *isautounlockaktivierte* den Wert false hat, ist *volumekeyprotectorid* eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="3da36-113">If *IsAutoUnlockEnabled* is false, *VolumeKeyProtectorID* is an empty string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3da36-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3da36-114">Return value</span></span>

<span data-ttu-id="3da36-115">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3da36-115">Type: **uint32**</span></span>

<span data-ttu-id="3da36-116">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="3da36-116">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="3da36-117">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="3da36-117">Return code/value</span></span>                                                                                                                                                                     | <span data-ttu-id="3da36-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3da36-118">Description</span></span>                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3da36-119"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="3da36-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                     | <span data-ttu-id="3da36-120">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="3da36-120">The method was successful.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="3da36-121"><dt>**F \_ E \_ nicht \_ aktiviert**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="3da36-121"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>    | <span data-ttu-id="3da36-122">BitLocker ist auf dem Volume nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="3da36-122">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="3da36-123">Fügen Sie eine Schlüssel Schutzvorrichtung zum Aktivieren von BitLocker hinzu.</span><span class="sxs-lookup"><span data-stu-id="3da36-123">Add a key protector to enable BitLocker.</span></span><br/> |
| <dl> <span data-ttu-id="3da36-124"><dt>**F \_ E \_ Not \_ Data \_ Volume**</dt> <dt>2150694937 (0x80310019)</dt></span><span class="sxs-lookup"><span data-stu-id="3da36-124"><dt>**FVE\_E\_NOT\_DATA\_VOLUME**</dt> <dt>2150694937 (0x80310019)</dt></span></span> </dl> | <span data-ttu-id="3da36-125">Die Methode kann nicht für das aktuell laufende Betriebssystem Volume ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="3da36-125">The method cannot be run for the currently running operating system volume.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="3da36-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3da36-126">Remarks</span></span>

<span data-ttu-id="3da36-127">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="3da36-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="3da36-128">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="3da36-128">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="3da36-129">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3da36-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="3da36-130">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="3da36-130">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3da36-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3da36-131">Requirements</span></span>



| <span data-ttu-id="3da36-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3da36-132">Requirement</span></span> | <span data-ttu-id="3da36-133">Wert</span><span class="sxs-lookup"><span data-stu-id="3da36-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3da36-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3da36-134">Minimum supported client</span></span><br/> | <span data-ttu-id="3da36-135">Nur Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3da36-135">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3da36-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3da36-136">Minimum supported server</span></span><br/> | <span data-ttu-id="3da36-137">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3da36-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3da36-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="3da36-138">Namespace</span></span><br/>                | <span data-ttu-id="3da36-139">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="3da36-139">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="3da36-140">MOF</span><span class="sxs-lookup"><span data-stu-id="3da36-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3da36-141"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3da36-141"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3da36-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3da36-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3da36-143">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="3da36-143">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 

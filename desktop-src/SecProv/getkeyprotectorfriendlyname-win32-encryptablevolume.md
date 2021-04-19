---
description: Ruft den anzeigen Amen ab, der verwendet wird, um eine angegebene Schlüssel Schutzvorrichtung zu identifizieren.
ms.assetid: 2f310494-7873-4d05-836e-f09e5784571b
title: Getkeyprotectorfriendlyname-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorFriendlyName
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 45da91d08aadda2d1a25254fe36d0d266b7c53d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349601"
---
# <a name="getkeyprotectorfriendlyname-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="b693c-103">Getkeyprotectorfriendlyname-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="b693c-103">GetKeyProtectorFriendlyName method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="b693c-104">Die **getkeyprotectorfriendlyname** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " Ruft den anzeigen Amen ab, der zum Identifizieren einer bestimmten Schlüssel Schutzvorrichtung verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="b693c-104">The **GetKeyProtectorFriendlyName** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class retrieves the display name used to identify a given key protector.</span></span>

## <a name="syntax"></a><span data-ttu-id="b693c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b693c-105">Syntax</span></span>


```mof
uint32 GetKeyProtectorFriendlyName(
  [in]  string VolumeKeyProtectorID,
  [out] string FriendlyName
);
```



## <a name="parameters"></a><span data-ttu-id="b693c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b693c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b693c-107">*Volumekeyprotectorid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b693c-107">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b693c-108">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b693c-108">Type: **string**</span></span>

<span data-ttu-id="b693c-109">Ein eindeutiger Zeichen folgen Bezeichner zum Verwalten einer verschlüsselten volumeschlüsselschutzvorrichtung.</span><span class="sxs-lookup"><span data-stu-id="b693c-109">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="b693c-110">*FriendlyName* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b693c-110">*FriendlyName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b693c-111">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b693c-111">Type: **string**</span></span>

<span data-ttu-id="b693c-112">Eine Zeichenfolge, die den vom Benutzer angegebenen Namen enthält, mit dem die angegebene Schlüssel Schutzvorrichtung identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="b693c-112">A string that contains the user-specified name used to identify the given key protector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b693c-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b693c-113">Return value</span></span>

<span data-ttu-id="b693c-114">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b693c-114">Type: **uint32**</span></span>

<span data-ttu-id="b693c-115">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="b693c-115">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="b693c-116">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="b693c-116">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="b693c-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b693c-117">Description</span></span>                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b693c-118"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="b693c-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="b693c-119">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="b693c-119">The method was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="b693c-120"><dt>**E \_ InvalidArg**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="b693c-120"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="b693c-121">Der *volumekeyprotectorid-* Parameter verweist nicht auf eine gültige Schlüssel Schutzvorrichtung.</span><span class="sxs-lookup"><span data-stu-id="b693c-121">The *VolumeKeyProtectorID* parameter does not refer to a valid key protector.</span></span><br/>     |
| <dl> <span data-ttu-id="b693c-122"><dt>**F \_ E \_ nicht \_ aktiviert**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="b693c-122"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="b693c-123">BitLocker ist auf dem Volume nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="b693c-123">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="b693c-124">Fügen Sie eine Schlüssel Schutzvorrichtung zum Aktivieren von BitLocker hinzu.</span><span class="sxs-lookup"><span data-stu-id="b693c-124">Add a key protector to enable BitLocker.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="b693c-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b693c-125">Remarks</span></span>

<span data-ttu-id="b693c-126">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="b693c-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b693c-127">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="b693c-127">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="b693c-128">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b693c-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b693c-129">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="b693c-129">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b693c-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b693c-130">Requirements</span></span>



| <span data-ttu-id="b693c-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b693c-131">Requirement</span></span> | <span data-ttu-id="b693c-132">Wert</span><span class="sxs-lookup"><span data-stu-id="b693c-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b693c-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b693c-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b693c-134">Nur Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b693c-134">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b693c-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b693c-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b693c-136">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b693c-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b693c-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="b693c-137">Namespace</span></span><br/>                | <span data-ttu-id="b693c-138">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="b693c-138">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="b693c-139">MOF</span><span class="sxs-lookup"><span data-stu-id="b693c-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b693c-140"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b693c-140"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b693c-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b693c-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b693c-142">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="b693c-142">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 

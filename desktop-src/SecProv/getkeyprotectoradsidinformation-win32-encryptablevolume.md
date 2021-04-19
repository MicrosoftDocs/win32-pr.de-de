---
description: Ruft die Sicherheits-ID und Flags ab, die zum Schützen eines Schlüssels verwendet werden.
ms.assetid: 5EF97F44-78FF-4FBF-9142-F2DD0A849057
title: Getkeyprotectoradsidinformation-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorCertificate
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 57e72488a9e53f49383d179b0bcb1a8b9ff1f706
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/26/2021
ms.locfileid: "106367162"
---
# <a name="getkeyprotectoradsidinformation-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="8e9ca-103">Getkeyprotectoradsidinformation-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="8e9ca-103">GetKeyProtectorAdSidInformation method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="8e9ca-104">Die **getkeyprotectoradsidinformation** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " Ruft die Sicherheits-ID und Flags ab, die zum Schützen eines Schlüssels verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8e9ca-104">The **GetKeyProtectorAdSidInformation** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class retrieves the security identifier and flags used to protect a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e9ca-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e9ca-105">Syntax</span></span>


```mof
uint32 GetKeyProtectorCertificate(
  [in]  string VolumeKeyProtectorID,
  [out] string SidString,
  [out] uint32 Flags
);
```



## <a name="parameters"></a><span data-ttu-id="8e9ca-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e9ca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e9ca-107">*Volumekeyprotectorid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8e9ca-107">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e9ca-108">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8e9ca-108">Type: **string**</span></span>

<span data-ttu-id="8e9ca-109">Ein Zeichen folgen Bezeichner, der zum Verwalten einer verschlüsselten volumeschlüsselschutzvorrichtung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="8e9ca-109">A string identifier that can be used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="8e9ca-110">*Sidstring* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8e9ca-110">*SidString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8e9ca-111">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8e9ca-111">Type: **string**</span></span>

<span data-ttu-id="8e9ca-112">Eine Zeichenfolge, die die Sicherheits-ID (SID) enthält.</span><span class="sxs-lookup"><span data-stu-id="8e9ca-112">A string that contains the security identifier (SID).</span></span>

</dd> <dt>

<span data-ttu-id="8e9ca-113">*Flags* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8e9ca-113">*Flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8e9ca-114">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e9ca-114">Type: **uint32**</span></span>

<span data-ttu-id="8e9ca-115">Flags, die das Funktionsverhalten ändern.</span><span class="sxs-lookup"><span data-stu-id="8e9ca-115">Flags that change the function behavior.</span></span> <span data-ttu-id="8e9ca-116">Dies kann einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="8e9ca-116">This can be one of the following values.</span></span>



| <span data-ttu-id="8e9ca-117">Wert</span><span class="sxs-lookup"><span data-stu-id="8e9ca-117">Value</span></span>                                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="8e9ca-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="8e9ca-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FVE_DPAPI_NG_FLAG_NONE"></span><span id="fve_dpapi_ng_flag_none"></span><dl> <span data-ttu-id="8e9ca-119"><dt>**F \_ DPAPI \_ ng \_ Flag \_ None**</dt> <dt>0x0000</dt></span><span class="sxs-lookup"><span data-stu-id="8e9ca-119"><dt>**FVE\_DPAPI\_NG\_FLAG\_NONE**</dt> <dt>0x0000</dt></span></span> </dl>                                                                   | <span data-ttu-id="8e9ca-120">Keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="8e9ca-120">No effect.</span></span><br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="FVE_DPAPI_NG_FLAG_UNLOCK_AS_SERVICE_ACCOUNT"></span><span id="fve_dpapi_ng_flag_unlock_as_service_account"></span><dl> <span data-ttu-id="8e9ca-121"><dt>**F \_ DPAPI \_ ng \_ Flag \_ Unlock \_ As \_ Dienst \_ Konto**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="8e9ca-121"><dt>**FVE\_DPAPI\_NG\_FLAG\_UNLOCK\_AS\_SERVICE\_ACCOUNT**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="8e9ca-122">Gibt an, dass die SID-basierte Schutzvorrichtung in einem Dienst Konto geschützt wurde.</span><span class="sxs-lookup"><span data-stu-id="8e9ca-122">Specifies that the SID-based protector was protected to a service account.</span></span> <span data-ttu-id="8e9ca-123">Wenn dieses Flag angegeben ist, sollte der Aufrufer sicherstellen, dass er vor dem Aufrufen von [**unlockwithadsid**](unlockwithadsid-win32-encryptablevolume.md) als geeignetes Dienst Konto ausgeführt wird (z. b. durch vorübergehendes verwerfen des Identitäts Wechsels).</span><span class="sxs-lookup"><span data-stu-id="8e9ca-123">If this flag is specified, the caller should ensure that it is running as the appropriate service account before calling [**UnlockWithAdSid**](unlockwithadsid-win32-encryptablevolume.md) (by temporarily dropping impersonation, for example).</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e9ca-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8e9ca-124">Return value</span></span>

<span data-ttu-id="8e9ca-125">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e9ca-125">Type: **uint32**</span></span>

<span data-ttu-id="8e9ca-126">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="8e9ca-126">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="8e9ca-127">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="8e9ca-127">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="8e9ca-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8e9ca-128">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="8e9ca-129"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="8e9ca-129"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="8e9ca-130">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="8e9ca-130">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8e9ca-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8e9ca-131">Remarks</span></span>

<span data-ttu-id="8e9ca-132">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="8e9ca-132">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8e9ca-133">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="8e9ca-133">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="8e9ca-134">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8e9ca-134">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8e9ca-135">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="8e9ca-135">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8e9ca-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8e9ca-136">Requirements</span></span>



| <span data-ttu-id="8e9ca-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8e9ca-137">Requirement</span></span> | <span data-ttu-id="8e9ca-138">Wert</span><span class="sxs-lookup"><span data-stu-id="8e9ca-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e9ca-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8e9ca-139">Minimum supported client</span></span><br/> | <span data-ttu-id="8e9ca-140">Nur Windows 8 Enterprise, Windows 8 pro \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8e9ca-140">Windows 8 Enterprise, Windows 8 Pro \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8e9ca-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8e9ca-141">Minimum supported server</span></span><br/> | <span data-ttu-id="8e9ca-142">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8e9ca-142">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8e9ca-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="8e9ca-143">Namespace</span></span><br/>                | <span data-ttu-id="8e9ca-144">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="8e9ca-144">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="8e9ca-145">MOF</span><span class="sxs-lookup"><span data-stu-id="8e9ca-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8e9ca-146"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8e9ca-146"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e9ca-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8e9ca-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e9ca-148">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="8e9ca-148">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 

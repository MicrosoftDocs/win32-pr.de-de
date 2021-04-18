---
description: Sichert den Verschlüsselungsschlüssel des Volumes mithilfe einer Active Directory-Sicherheits-ID (SID).
ms.assetid: 881EEAF2-49C5-4BBD-B2AA-5E30B61E7D3A
title: Protectkeywithadsid-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithAdSid
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 0279a6edc8aaa275fdf75a855452d987de802d86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357925"
---
# <a name="protectkeywithadsid-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="d3d5c-103">Protectkeywithadsid-Methode der Win32- \_ Klasse "verschlüsseltablevolume"</span><span class="sxs-lookup"><span data-stu-id="d3d5c-103">ProtectKeyWithAdSid method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="d3d5c-104">Die **protectkeywithadsid** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " sichert den Verschlüsselungsschlüssel des Volumes mithilfe einer Sicherheits-ID (Active Directory Security Identifier, SID).</span><span class="sxs-lookup"><span data-stu-id="d3d5c-104">The **ProtectKeyWithAdSid** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class secures the volume's encryption key by using a Active Directory security identifier (SID).</span></span>

## <a name="syntax"></a><span data-ttu-id="d3d5c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3d5c-105">Syntax</span></span>


```mof
uint32 ProtectKeyWithAdSid(
  [in, optional] string FriendlyName,
  [in]           string SidString,
  [in]           uint32 Flags,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="d3d5c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d3d5c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3d5c-107">*FriendlyName* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="d3d5c-107">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d3d5c-108">Eine Zeichenfolge, die einen vom Benutzer zugewiesenen Bezeichner für diese Schlüssel Schutzvorrichtung angibt.</span><span class="sxs-lookup"><span data-stu-id="d3d5c-108">A string that specifies a user-assigned identifier for this key protector.</span></span> <span data-ttu-id="d3d5c-109">Wenn dieser Parameter nicht angegeben wird, wird ein leerer Wert verwendet.</span><span class="sxs-lookup"><span data-stu-id="d3d5c-109">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="d3d5c-110">*Sidstring* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d3d5c-110">*SidString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3d5c-111">Eine Zeichenfolge, die die Active Directory sid enthält, mit der der Verschlüsselungsschlüssel geschützt wird.</span><span class="sxs-lookup"><span data-stu-id="d3d5c-111">String that contains the Active Directory SID used to protect the encryption key.</span></span>

</dd> <dt>

<span data-ttu-id="d3d5c-112">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="d3d5c-112">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3d5c-113">Flags, die das Funktionsverhalten ändern.</span><span class="sxs-lookup"><span data-stu-id="d3d5c-113">Flags that change the function behavior.</span></span> <span data-ttu-id="d3d5c-114">Dies kann einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="d3d5c-114">This can be one of the following values.</span></span>



| <span data-ttu-id="d3d5c-115">Wert</span><span class="sxs-lookup"><span data-stu-id="d3d5c-115">Value</span></span>                                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="d3d5c-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d3d5c-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FVE_DPAPI_NG_FLAG_NONE"></span><span id="fve_dpapi_ng_flag_none"></span><dl> <span data-ttu-id="d3d5c-117"><dt>**F \_ DPAPI \_ ng \_ Flag \_ None**</dt> <dt>0x0000</dt></span><span class="sxs-lookup"><span data-stu-id="d3d5c-117"><dt>**FVE\_DPAPI\_NG\_FLAG\_NONE**</dt> <dt>0x0000</dt></span></span> </dl>                                                                   | <span data-ttu-id="d3d5c-118">Keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="d3d5c-118">No effect.</span></span><br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="FVE_DPAPI_NG_FLAG_UNLOCK_AS_SERVICE_ACCOUNT"></span><span id="fve_dpapi_ng_flag_unlock_as_service_account"></span><dl> <span data-ttu-id="d3d5c-119"><dt>**F \_ DPAPI \_ ng \_ Flag \_ Unlock \_ As \_ Dienst \_ Konto**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="d3d5c-119"><dt>**FVE\_DPAPI\_NG\_FLAG\_UNLOCK\_AS\_SERVICE\_ACCOUNT**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="d3d5c-120">Gibt an, dass die SID-basierte Schutzvorrichtung in einem Dienst Konto geschützt wurde.</span><span class="sxs-lookup"><span data-stu-id="d3d5c-120">Specifies that the SID-based protector was protected to a service account.</span></span> <span data-ttu-id="d3d5c-121">Wenn dieses Flag angegeben ist, sollte der Aufrufer sicherstellen, dass er vor dem Aufrufen von [**unlockwithadsid**](unlockwithadsid-win32-encryptablevolume.md) als geeignetes Dienst Konto ausgeführt wird (z. b. durch vorübergehendes verwerfen des Identitäts Wechsels).</span><span class="sxs-lookup"><span data-stu-id="d3d5c-121">If this flag is specified, the caller should ensure that it is running as the appropriate service account before calling [**UnlockWithAdSid**](unlockwithadsid-win32-encryptablevolume.md) (by temporarily dropping impersonation, for example).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d3d5c-122">*Volumekeyprotectorid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d3d5c-122">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3d5c-123">Ein eindeutiger Bezeichner, der der erstellten Schutzvorrichtung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d3d5c-123">A unique identifier associated with the created protector.</span></span> <span data-ttu-id="d3d5c-124">Mit dieser Zeichenfolge können Sie die Schlüssel Schutzvorrichtung verwalten.</span><span class="sxs-lookup"><span data-stu-id="d3d5c-124">You can use this string to manage the key protector.</span></span>

<span data-ttu-id="d3d5c-125">Wenn das Laufwerk die Hardware Verschlüsselung unterstützt und BitLocker keinen bandbesitz hat, wird die ID-Zeichenfolge auf "BitLocker" festgelegt, und die Schlüssel Schutzvorrichtung wird in die pro-Band-Metadaten geschrieben.</span><span class="sxs-lookup"><span data-stu-id="d3d5c-125">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3d5c-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d3d5c-126">Return value</span></span>

<span data-ttu-id="d3d5c-127">Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="d3d5c-127">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="d3d5c-128">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="d3d5c-128">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="d3d5c-129">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d3d5c-129">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="d3d5c-130"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="d3d5c-130"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="d3d5c-131">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="d3d5c-131">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d3d5c-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d3d5c-132">Remarks</span></span>

<span data-ttu-id="d3d5c-133">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="d3d5c-133">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d3d5c-134">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="d3d5c-134">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="d3d5c-135">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d3d5c-135">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d3d5c-136">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md) .</span><span class="sxs-lookup"><span data-stu-id="d3d5c-136">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md)</span></span>

<span data-ttu-id="d3d5c-137">Standardmäßig ist es nicht möglich, ein Active Directory Konto oder eine Gruppen Schutzvorrichtung Remote hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="d3d5c-137">By default, you cannot add an Active Directory account or group protector remotely.</span></span> <span data-ttu-id="d3d5c-138">Sie müssen die eingeschränkte Delegierung auf dem Domänen Controller und dem Quellcomputer aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d3d5c-138">You must enable constrained delegation on the domain controller and source computer.</span></span> <span data-ttu-id="d3d5c-139">Führen Sie auf dem Domänen Controller die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="d3d5c-139">On the domain controller, perform the following steps:</span></span>

1.  <span data-ttu-id="d3d5c-140">Server-Manager öffnen</span><span class="sxs-lookup"><span data-stu-id="d3d5c-140">Open Server Manager</span></span>
2.  <span data-ttu-id="d3d5c-141">Computer in Active Directory Rollen auswählen</span><span class="sxs-lookup"><span data-stu-id="d3d5c-141">Select Computers in Active Directory roles</span></span>
3.  <span data-ttu-id="d3d5c-142">Ziel Client Computer auswählen und mit der rechten Maustaste klicken</span><span class="sxs-lookup"><span data-stu-id="d3d5c-142">Select the target client computer and right click</span></span>
4.  <span data-ttu-id="d3d5c-143">Registerkarte "Delegierung" auswählen</span><span class="sxs-lookup"><span data-stu-id="d3d5c-143">Select the Delegation tab</span></span>
5.  <span data-ttu-id="d3d5c-144">Aktivieren Sie das Optionsfeld "Computer nur bei Delegierungen angegebener Dienste vertrauen".</span><span class="sxs-lookup"><span data-stu-id="d3d5c-144">Select the "Trust this computer for delegation to specified services only" radio button</span></span>
6.  <span data-ttu-id="d3d5c-145">Aktivieren Sie das Optionsfeld "nur Kerberos verwenden".</span><span class="sxs-lookup"><span data-stu-id="d3d5c-145">Select the "Use Kerberos only" radio button</span></span>
7.  <span data-ttu-id="d3d5c-146">Klicken Sie auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="d3d5c-146">Click Add</span></span>
8.  <span data-ttu-id="d3d5c-147">Wählen Sie "Benutzer oder Computer" aus.</span><span class="sxs-lookup"><span data-stu-id="d3d5c-147">Select "Users or Computers"</span></span>
9.  <span data-ttu-id="d3d5c-148">Host/als Dienst Prinzipal Namen auswählen</span><span class="sxs-lookup"><span data-stu-id="d3d5c-148">Select host/ as the Service Principal Name</span></span>

<span data-ttu-id="d3d5c-149">Führen Sie die Schritte 3 bis 9 auf dem Quellcomputer aus.</span><span class="sxs-lookup"><span data-stu-id="d3d5c-149">Perform steps 3 through 9 on the source computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3d5c-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d3d5c-150">Requirements</span></span>



| <span data-ttu-id="d3d5c-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d3d5c-151">Requirement</span></span> | <span data-ttu-id="d3d5c-152">Wert</span><span class="sxs-lookup"><span data-stu-id="d3d5c-152">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3d5c-153">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d3d5c-153">Minimum supported client</span></span><br/> | <span data-ttu-id="d3d5c-154">Nur Windows 8 Enterprise, Windows 8 pro \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d3d5c-154">Windows 8 Enterprise, Windows 8 Pro \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d3d5c-155">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d3d5c-155">Minimum supported server</span></span><br/> | <span data-ttu-id="d3d5c-156">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d3d5c-156">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d3d5c-157">Namespace</span><span class="sxs-lookup"><span data-stu-id="d3d5c-157">Namespace</span></span><br/>                | <span data-ttu-id="d3d5c-158">Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)</span><span class="sxs-lookup"><span data-stu-id="d3d5c-158">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="d3d5c-159">MOF</span><span class="sxs-lookup"><span data-stu-id="d3d5c-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d3d5c-160"><dt>Win32 \_ verschlüsseltablevolume. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d3d5c-160"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3d5c-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d3d5c-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3d5c-162">**Win32- \_ verschlüsseltablevolume**</span><span class="sxs-lookup"><span data-stu-id="d3d5c-162">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 

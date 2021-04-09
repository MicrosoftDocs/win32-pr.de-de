---
description: Installiert einen Besitzer für das TPM.
ms.assetid: 7b4c8785-0925-41a8-a878-7c1f38d31853
title: TakeOwnership-Methode der Win32_Tpm-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.TakeOwnership
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: acb0cb03f5e422695623bf6e183d1fd89f63ab60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050428"
---
# <a name="takeownership-method-of-the-win32_tpm-class"></a><span data-ttu-id="bee8b-103">TakeOwnership-Methode der Win32- \_ TPM-Klasse</span><span class="sxs-lookup"><span data-stu-id="bee8b-103">TakeOwnership method of the Win32\_Tpm class</span></span>

<span data-ttu-id="bee8b-104">Mit der **TakeOwnership** -Methode der [**Win32- \_ TPM**](win32-tpm.md) -Klasse wird ein Besitzer für das TPM installiert.</span><span class="sxs-lookup"><span data-stu-id="bee8b-104">The **TakeOwnership** method of the [**Win32\_Tpm**](win32-tpm.md) class installs an owner for the TPM.</span></span> <span data-ttu-id="bee8b-105">Der Besitzer des TPM kann die TPM-Funktionen in vollem Umfang nutzen.</span><span class="sxs-lookup"><span data-stu-id="bee8b-105">The owner of the TPM can make full use of TPM capabilities.</span></span> <span data-ttu-id="bee8b-106">Nachdem ein Besitzer festgelegt wurde, kann kein anderer Benutzer oder keine Software den Besitz des TPM beanspruchen.</span><span class="sxs-lookup"><span data-stu-id="bee8b-106">After an owner is set, no other user or software can claim ownership of the TPM.</span></span>

<span data-ttu-id="bee8b-107">Die Methoden [**is-aktiviert**](isenabled-win32-tpm.md), [**isaktiviert**](isactivated-win32-tpm.md)und [**isownershipallowed**](isownershipallowed-win32-tpm.md) müssen alle zutreffen, bevor die **TakeOwnership** -Methode erfolgreich ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="bee8b-107">The [**IsEnabled**](isenabled-win32-tpm.md), [**IsActivated**](isactivated-win32-tpm.md), and [**IsOwnershipAllowed**](isownershipallowed-win32-tpm.md) methods must all be true before the **TakeOwnership** method can succeed.</span></span>

## <a name="syntax"></a><span data-ttu-id="bee8b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="bee8b-108">Syntax</span></span>


```mof
uint32 TakeOwnership(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="bee8b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="bee8b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bee8b-110">Besitzer *des Besitzers* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="bee8b-110">*OwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bee8b-111">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bee8b-111">Type: **string**</span></span>

<span data-ttu-id="bee8b-112">Eine Zeichenfolge, die den TPM-Besitzer angibt.</span><span class="sxs-lookup"><span data-stu-id="bee8b-112">A string that identifies the TPM owner.</span></span> <span data-ttu-id="bee8b-113">Diese Zeichenfolge muss eine Base64-codierte NULL-terminierte Zeichenfolge sein, die genau 20 Bytes Binärdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="bee8b-113">This string must be a base64-encoded null-terminated string that contains exactly 20 bytes of binary data.</span></span> <span data-ttu-id="bee8b-114">Verwenden Sie die [**converttobesitzauth**](converttoownerauth-win32-tpm.md) -Methode, um eine Passphrase in dieses erwartete Format zu übersetzen.</span><span class="sxs-lookup"><span data-stu-id="bee8b-114">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a passphrase to this expected format.</span></span> <span data-ttu-id="bee8b-115">Der Parameter " *besitzauth* " wird aus der Registrierung gelesen, wenn kein Wert angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="bee8b-115">The *OwnerAuth* parameter is read from the registry if none is provided.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bee8b-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bee8b-116">Return value</span></span>

<span data-ttu-id="bee8b-117">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bee8b-117">Type: **uint32**</span></span>

<span data-ttu-id="bee8b-118">Alle TPM-Fehler sowie Fehler, die für die TPM-Basisdienste spezifisch sind, können zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="bee8b-118">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="bee8b-119">In der folgenden Tabelle sind einige der allgemeinen Rückgabecodes aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="bee8b-119">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="bee8b-120">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="bee8b-120">Return code/value</span></span>                                                                                                                                                                         | <span data-ttu-id="bee8b-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bee8b-121">Description</span></span>                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bee8b-122"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="bee8b-122"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                         | <span data-ttu-id="bee8b-123">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="bee8b-123">The method was successful.</span></span><br/>                                                                                                                                                                              |
| <dl> <span data-ttu-id="bee8b-124"><dt>**E \_ InvalidArg**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="bee8b-124"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                 | <span data-ttu-id="bee8b-125">Der Parameter " *besitzauth* " ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="bee8b-125">The *OwnerAuth* parameter is not valid.</span></span><br/>                                                                                                                                                                 |
| <dl> <span data-ttu-id="bee8b-126"><dt>**TPM \_ E- \_ Besitzer \_ Satz**</dt> <dt>2150105108 (0x80280014)</dt></span><span class="sxs-lookup"><span data-stu-id="bee8b-126"><dt>**TPM\_E\_OWNER\_SET**</dt> <dt>2150105108 (0x80280014)</dt></span></span> </dl>            | <span data-ttu-id="bee8b-127">Ein Besitzer ist bereits auf dem TPM vorhanden.</span><span class="sxs-lookup"><span data-stu-id="bee8b-127">An owner already exists on the TPM.</span></span><br/>                                                                                                                                                                     |
| <dl> <span data-ttu-id="bee8b-128"><dt>**TPM \_ E \_ keine \_ Bestätigung**</dt> <dt>2150105123 (0x80280023)</dt></span><span class="sxs-lookup"><span data-stu-id="bee8b-128"><dt>**TPM\_E\_NO\_ENDORSEMENT**</dt> <dt>2150105123 (0x80280023)</dt></span></span> </dl>       | <span data-ttu-id="bee8b-129">Es wurde kein Endorsement Key auf dem TPM gefunden.</span><span class="sxs-lookup"><span data-stu-id="bee8b-129">No endorsement key can be found on the TPM.</span></span><br/> <span data-ttu-id="bee8b-130">Informationen zum Erstellen eines Endorsement Key-Paars auf dem TPM finden Sie unter der Methode " [**kreateendorsegmentkeypair**](createendorsementkeypair-win32-tpm.md) ".</span><span class="sxs-lookup"><span data-stu-id="bee8b-130">To create an endorsement key pair on the TPM, see the [**CreateEndorsementKeyPair**](createendorsementkeypair-win32-tpm.md) method.</span></span><br/>             |
| <dl> <span data-ttu-id="bee8b-131"><dt>**TPM \_ E \_ Installation \_ deaktiviert**</dt> <dt>2150105099 (0x8028000b)</dt></span><span class="sxs-lookup"><span data-stu-id="bee8b-131"><dt>**TPM\_E\_INSTALL\_DISABLED**</dt> <dt>2150105099 (0x8028000B)</dt></span></span> </dl>     | <span data-ttu-id="bee8b-132">Ein Besitzer kann nicht auf diesem TPM installiert werden.</span><span class="sxs-lookup"><span data-stu-id="bee8b-132">An owner cannot be installed on this TPM.</span></span><br/> <span data-ttu-id="bee8b-133">Informationen dazu, wie Sie die Installation eines Geräte Besitzers zulassen, finden Sie unter [**setphysicalpresencerequest**](setphysicalpresencerequest-win32-tpm.md).</span><span class="sxs-lookup"><span data-stu-id="bee8b-133">For information about how to allow installation of a device owner, see [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md).</span></span><br/> |
| <dl> <span data-ttu-id="bee8b-134"><dt>**TPM \_ E \_ Verteidigung \_ der \_ Sperre**</dt> mit <dt>2150107139 (0x80280803)</dt></span><span class="sxs-lookup"><span data-stu-id="bee8b-134"><dt>**TPM\_E\_DEFEND\_LOCK\_RUNNING**</dt> <dt>2150107139 (0x80280803)</dt></span></span> </dl> | <span data-ttu-id="bee8b-135">Das TPM steht für Wörterbuchangriffe und befindet sich in einem Timeout Zeitraum.</span><span class="sxs-lookup"><span data-stu-id="bee8b-135">The TPM is defending against dictionary attacks and is in a time-out period.</span></span> <span data-ttu-id="bee8b-136">Weitere Informationen finden Sie unter der [**resetauthlockout**](resetauthlockout-win32-tpm.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="bee8b-136">For more information, see the [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) method.</span></span><br/>                               |



 

## <a name="remarks"></a><span data-ttu-id="bee8b-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bee8b-137">Remarks</span></span>

<span data-ttu-id="bee8b-138">Die Methoden [](isenabled-win32-tpm.md) [**isaktivierte, isaktivierte**](isactivated-win32-tpm.md)und [**isownershipallowed**](isownershipallowed-win32-tpm.md) müssen alle wahr sein, damit der **Take Ownership** -Vorgang erfolgreich ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="bee8b-138">The methods [**IsEnabled**](isenabled-win32-tpm.md), [**IsActivated**](isactivated-win32-tpm.md), and [**IsOwnershipAllowed**](isownershipallowed-win32-tpm.md) must all be true before **TakeOwnership** can succeed.</span></span>

<span data-ttu-id="bee8b-139">Sie sollten die [**convertdebesitzauth**](converttoownerauth-win32-tpm.md) -Methode verwenden, um eine Passphrase in den Eingabe Wert zu ändern, der für den Parameter " *besitzauth* " verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bee8b-139">You should use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to change a passphrase into the input value used for the *OwnerAuth* parameter.</span></span>

<span data-ttu-id="bee8b-140">Die **TakeOwnership** -Methode sichert den Besitzer Autorisierungs Wert, um Active Directory, wenn die entsprechenden Gruppenrichtlinie Einstellungen konfiguriert wurden.</span><span class="sxs-lookup"><span data-stu-id="bee8b-140">The **TakeOwnership** method backs up the owner authorization value to Active Directory if the appropriate Group Policy settings have been configured.</span></span>

<span data-ttu-id="bee8b-141">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="bee8b-141">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="bee8b-142">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="bee8b-142">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="bee8b-143">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="bee8b-143">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="bee8b-144">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="bee8b-144">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bee8b-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bee8b-145">Requirements</span></span>



| <span data-ttu-id="bee8b-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bee8b-146">Requirement</span></span> | <span data-ttu-id="bee8b-147">Wert</span><span class="sxs-lookup"><span data-stu-id="bee8b-147">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="bee8b-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bee8b-148">Minimum supported client</span></span><br/> | <span data-ttu-id="bee8b-149">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bee8b-149">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="bee8b-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bee8b-150">Minimum supported server</span></span><br/> | <span data-ttu-id="bee8b-151">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bee8b-151">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="bee8b-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="bee8b-152">Namespace</span></span><br/>                | <span data-ttu-id="bee8b-153">Root \\ CIMV2 \\ Security- \\ mikrosofttpm</span><span class="sxs-lookup"><span data-stu-id="bee8b-153">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="bee8b-154">MOF</span><span class="sxs-lookup"><span data-stu-id="bee8b-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bee8b-155"><dt>Win32- \_ TPM. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="bee8b-155"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="bee8b-156">DLL</span><span class="sxs-lookup"><span data-stu-id="bee8b-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bee8b-157"><dt>Win32- \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bee8b-157"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bee8b-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bee8b-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bee8b-159">**Win32- \_ TPM**</span><span class="sxs-lookup"><span data-stu-id="bee8b-159">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 

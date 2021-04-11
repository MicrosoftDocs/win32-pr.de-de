---
description: Setzt das TPM auf seine Werkseinstellungen zurück.
ms.assetid: 55d6702f-bd57-43e3-b790-617940dd2e01
title: Clear-Methode der Win32_Tpm-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.Clear
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: cf75a8af6764e542cecd9bd296c1b1511c4f4513
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217426"
---
# <a name="clear-method-of-the-win32_tpm-class"></a><span data-ttu-id="8f43c-103">Clear-Methode der Win32- \_ TPM-Klasse</span><span class="sxs-lookup"><span data-stu-id="8f43c-103">Clear method of the Win32\_Tpm class</span></span>

<span data-ttu-id="8f43c-104">Die **Clear** -Methode der [**Win32- \_ TPM**](win32-tpm.md) -Klasse setzt das TPM auf den Standardzustand der Factory zurück.</span><span class="sxs-lookup"><span data-stu-id="8f43c-104">The **Clear** method of the [**Win32\_Tpm**](win32-tpm.md) class resets the TPM to its factory-default state.</span></span> <span data-ttu-id="8f43c-105">Ein TPM-Besitzer kann diese Methode verwenden, um den TPM-Besitz abzubrechen und kryptografiematerialien ungültig zu machen, die vom vorherigen Besitzer erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="8f43c-105">A TPM owner can use this method to cancel TPM ownership and invalidate cryptographic materials created by the previous owner.</span></span> <span data-ttu-id="8f43c-106">Diese Methode hält BitLocker an, wenn durch den Aufruf von eine BitLocker-Wiederherstellung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="8f43c-106">This method suspends BitLocker if calling could cause BitLocker recovery to be required.</span></span> <span data-ttu-id="8f43c-107">BitLocker wird automatisch fortgesetzt, sobald TPM bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="8f43c-107">BitLocker would automatically resume once TPM has been provisioned.</span></span>

> [!Caution]  
> <span data-ttu-id="8f43c-108">Durch das Löschen des TPM verlieren Sie alle TPM-Schlüssel, die von Anwendungen erstellt und verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8f43c-108">By clearing the TPM, you will lose all TPM keys created and used by applications.</span></span> <span data-ttu-id="8f43c-109">Wenn diese Schlüssel zum Verschlüsseln von Daten verwendet wurden, stellen Sie sicher, dass Sie vor dem Löschen des TPM eine andere Möglichkeit haben, auf die Daten zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="8f43c-109">If these keys were used to encrypt data, ensure that you have another way to access the data before clearing the TPM.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="8f43c-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f43c-110">Syntax</span></span>


```mof
uint32 Clear(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="8f43c-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f43c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f43c-112">Besitzer *des Besitzers* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="8f43c-112">*OwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8f43c-113">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8f43c-113">Type: **string**</span></span>

<span data-ttu-id="8f43c-114">Eine Zeichenfolge, die den TPM-Besitzer angibt.</span><span class="sxs-lookup"><span data-stu-id="8f43c-114">A string that identifies the TPM owner.</span></span> <span data-ttu-id="8f43c-115">Bei dieser Zeichenfolge muss es sich um eine Base64-codierte Zeichenfolge handeln, die genau 20 Byte Binärdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="8f43c-115">This string must be a base64-encoded string that contains exactly 20 bytes of binary data.</span></span> <span data-ttu-id="8f43c-116">Verwenden Sie die [**converttobesitzauth**](converttoownerauth-win32-tpm.md) -Methode, um eine Passphrase in dieses erwartete Format zu übersetzen.</span><span class="sxs-lookup"><span data-stu-id="8f43c-116">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a passphrase to this expected format.</span></span> <span data-ttu-id="8f43c-117">Der Parameter " *besitzauth* " wird aus der Registrierung gelesen, wenn kein Wert angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8f43c-117">The *OwnerAuth* parameter is read from the registry if none is provided.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f43c-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8f43c-118">Return value</span></span>

<span data-ttu-id="8f43c-119">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f43c-119">Type: **uint32**</span></span>

<span data-ttu-id="8f43c-120">Alle TPM-Fehler sowie Fehler, die für die TPM-Basisdienste spezifisch sind, können zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8f43c-120">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="8f43c-121">In der folgenden Tabelle sind einige der allgemeinen Rückgabecodes aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="8f43c-121">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="8f43c-122">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="8f43c-122">Return code/value</span></span>                                                                                                                                                                         | <span data-ttu-id="8f43c-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8f43c-123">Description</span></span>                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8f43c-124"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="8f43c-124"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                         | <span data-ttu-id="8f43c-125">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="8f43c-125">The method was successful.</span></span><br/>                                                                                                                                                |
| <dl> <span data-ttu-id="8f43c-126"><dt>**TPM \_ E \_ authfail**</dt> <dt>2150105089 (0x80280001)</dt></span><span class="sxs-lookup"><span data-stu-id="8f43c-126"><dt>**TPM\_E\_AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span></span> </dl>              | <span data-ttu-id="8f43c-127">Der angegebene Besitzer Autorisierungs Wert kann die Anforderung nicht ausführen.</span><span class="sxs-lookup"><span data-stu-id="8f43c-127">The provided owner authorization value cannot perform the request.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="8f43c-128"><dt>**TPM \_ E \_ Verteidigung \_ der \_ Sperre**</dt> mit <dt>2150107139 (0x80280803)</dt></span><span class="sxs-lookup"><span data-stu-id="8f43c-128"><dt>**TPM\_E\_DEFEND\_LOCK\_RUNNING**</dt> <dt>2150107139 (0x80280803)</dt></span></span> </dl> | <span data-ttu-id="8f43c-129">Das TPM steht für Wörterbuchangriffe und befindet sich in einem Timeout Zeitraum.</span><span class="sxs-lookup"><span data-stu-id="8f43c-129">The TPM is defending against dictionary attacks and is in a time-out period.</span></span> <span data-ttu-id="8f43c-130">Weitere Informationen finden Sie unter der [**resetauthlockout**](resetauthlockout-win32-tpm.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="8f43c-130">For more information, see the [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8f43c-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8f43c-131">Remarks</span></span>

<span data-ttu-id="8f43c-132">Durch das Ausführen dieser Methode kann ein TPM-Computer für die Wiederverwendung vorbereitet werden.</span><span class="sxs-lookup"><span data-stu-id="8f43c-132">Running this method can help prepare a TPM-equipped computer for recycling.</span></span>

<span data-ttu-id="8f43c-133">Um das TPM zu löschen, aber nicht mehr über die TPM-Besitzer Autorisierung verfügen, benötigen Sie physischen Zugriff auf den Computer.</span><span class="sxs-lookup"><span data-stu-id="8f43c-133">To clear the TPM but no longer have the TPM owner authorization, you need physical access to the computer.</span></span> <span data-ttu-id="8f43c-134">Die [**setphysicalpresencerequest**](setphysicalpresencerequest-win32-tpm.md) -Methode enthält Funktionen, die das Löschen des TPM ohne TPM-Besitzer Autorisierung erleichtern.</span><span class="sxs-lookup"><span data-stu-id="8f43c-134">The [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method includes functionality to help clear the TPM without TPM owner authorization.</span></span>

<span data-ttu-id="8f43c-135">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="8f43c-135">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8f43c-136">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="8f43c-136">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="8f43c-137">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8f43c-137">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8f43c-138">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="8f43c-138">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8f43c-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8f43c-139">Requirements</span></span>



| <span data-ttu-id="8f43c-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8f43c-140">Requirement</span></span> | <span data-ttu-id="8f43c-141">Wert</span><span class="sxs-lookup"><span data-stu-id="8f43c-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f43c-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8f43c-142">Minimum supported client</span></span><br/> | <span data-ttu-id="8f43c-143">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8f43c-143">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="8f43c-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8f43c-144">Minimum supported server</span></span><br/> | <span data-ttu-id="8f43c-145">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8f43c-145">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="8f43c-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="8f43c-146">Namespace</span></span><br/>                | <span data-ttu-id="8f43c-147">Root \\ CIMV2 \\ Security- \\ mikrosofttpm</span><span class="sxs-lookup"><span data-stu-id="8f43c-147">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="8f43c-148">MOF</span><span class="sxs-lookup"><span data-stu-id="8f43c-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8f43c-149"><dt>Win32- \_ TPM. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8f43c-149"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="8f43c-150">DLL</span><span class="sxs-lookup"><span data-stu-id="8f43c-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f43c-151"><dt>Win32- \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f43c-151"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f43c-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8f43c-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f43c-153">**Win32- \_ TPM**</span><span class="sxs-lookup"><span data-stu-id="8f43c-153">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 

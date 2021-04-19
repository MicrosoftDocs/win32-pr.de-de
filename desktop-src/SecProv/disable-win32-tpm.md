---
description: Ermöglicht dem TPM-Besitzer, das TPM zu deaktivieren oder anzuhalten.
ms.assetid: d910334d-6da6-423d-ae8d-6e86f300dd52
title: Deaktivieren der Methode der Win32_Tpm-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.Disable
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 32012c338646ce11c96d2657233642808fdcdaec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348147"
---
# <a name="disable-method-of-the-win32_tpm-class"></a><span data-ttu-id="7a4d6-103">Deaktivieren der Methode der Win32- \_ TPM-Klasse</span><span class="sxs-lookup"><span data-stu-id="7a4d6-103">Disable method of the Win32\_Tpm class</span></span>

<span data-ttu-id="7a4d6-104">Die **Deaktivierungs Methode** der [**Win32 \_ TPM**](win32-tpm.md) -Klasse ermöglicht es dem TPM-Besitzer, das TPM zu deaktivieren oder anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="7a4d6-104">The **Disable** method of the [**Win32\_Tpm**](win32-tpm.md) class allows the TPM owner to disable or suspend the TPM.</span></span> <span data-ttu-id="7a4d6-105">Diese Methode hält BitLocker an, wenn durch den Aufruf von eine BitLocker-Wiederherstellung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="7a4d6-105">This method suspends BitLocker if calling could cause BitLocker recovery to be required.</span></span> <span data-ttu-id="7a4d6-106">BitLocker wird automatisch fortgesetzt, sobald TPM bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="7a4d6-106">BitLocker would automatically resume once TPM has been provisioned.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a4d6-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a4d6-107">Syntax</span></span>


```mof
uint32 Disable(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="7a4d6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a4d6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a4d6-109">Besitzer *des Besitzers* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="7a4d6-109">*OwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7a4d6-110">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7a4d6-110">Type: **string**</span></span>

<span data-ttu-id="7a4d6-111">Eine Zeichenfolge, die den TPM-Besitzer angibt.</span><span class="sxs-lookup"><span data-stu-id="7a4d6-111">A string that identifies the TPM owner.</span></span> <span data-ttu-id="7a4d6-112">Bei dieser Zeichenfolge muss es sich um eine Base64-codierte Zeichenfolge handeln, die genau 20 Byte Binärdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="7a4d6-112">This string must be a base64-encoded string that contains exactly 20 bytes of binary data.</span></span> <span data-ttu-id="7a4d6-113">Verwenden Sie die [**converttobesitzauth**](converttoownerauth-win32-tpm.md) -Methode, um eine Passphrase in dieses erwartete Format zu übersetzen.</span><span class="sxs-lookup"><span data-stu-id="7a4d6-113">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a passphrase to this expected format.</span></span> <span data-ttu-id="7a4d6-114">Der Parameter " *besitzauth* " wird aus der Registrierung gelesen, wenn kein Wert angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7a4d6-114">The *OwnerAuth* parameter is read from the registry if none is provided.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a4d6-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7a4d6-115">Return value</span></span>

<span data-ttu-id="7a4d6-116">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7a4d6-116">Type: **uint32**</span></span>

<span data-ttu-id="7a4d6-117">Alle TPM-Fehler sowie Fehler, die für die TPM-Basisdienste spezifisch sind, können zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7a4d6-117">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="7a4d6-118">In der folgenden Tabelle sind einige der allgemeinen Rückgabecodes aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="7a4d6-118">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="7a4d6-119">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="7a4d6-119">Return code/value</span></span>                                                                                                                                                                         | <span data-ttu-id="7a4d6-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7a4d6-120">Description</span></span>                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7a4d6-121"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="7a4d6-121"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                         | <span data-ttu-id="7a4d6-122">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="7a4d6-122">The method was successful.</span></span><br/>                                                                                                                                                |
| <dl> <span data-ttu-id="7a4d6-123"><dt>**TPM \_ E \_ authfail**</dt> <dt>2150105089 (0x80280001)</dt></span><span class="sxs-lookup"><span data-stu-id="7a4d6-123"><dt>**TPM\_E\_AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span></span> </dl>              | <span data-ttu-id="7a4d6-124">Der angegebene Besitzer Autorisierungs Wert kann die Anforderung nicht ausführen.</span><span class="sxs-lookup"><span data-stu-id="7a4d6-124">The provided owner authorization value cannot perform the request.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="7a4d6-125"><dt>**TPM \_ E \_ Verteidigung \_ der \_ Sperre**</dt> mit <dt>2150107139 (0x80280803)</dt></span><span class="sxs-lookup"><span data-stu-id="7a4d6-125"><dt>**TPM\_E\_DEFEND\_LOCK\_RUNNING**</dt> <dt>2150107139 (0x80280803)</dt></span></span> </dl> | <span data-ttu-id="7a4d6-126">Das TPM steht für Wörterbuchangriffe und befindet sich in einem Timeout Zeitraum.</span><span class="sxs-lookup"><span data-stu-id="7a4d6-126">The TPM is defending against dictionary attacks and is in a time-out period.</span></span> <span data-ttu-id="7a4d6-127">Weitere Informationen finden Sie unter der [**resetauthlockout**](resetauthlockout-win32-tpm.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="7a4d6-127">For more information, see the [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7a4d6-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a4d6-128">Remarks</span></span>

<span data-ttu-id="7a4d6-129">Um das TPM zu deaktivieren, ohne den TPM-Besitzer Autorisierungs Wert zu verwenden, verwenden Sie die [**setphysicalpresencerequest**](setphysicalpresencerequest-win32-tpm.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="7a4d6-129">To disable the TPM without having the TPM owner authorization value, use the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method.</span></span>

<span data-ttu-id="7a4d6-130">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="7a4d6-130">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7a4d6-131">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="7a4d6-131">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="7a4d6-132">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="7a4d6-132">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7a4d6-133">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="7a4d6-133">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7a4d6-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7a4d6-134">Requirements</span></span>



| <span data-ttu-id="7a4d6-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7a4d6-135">Requirement</span></span> | <span data-ttu-id="7a4d6-136">Wert</span><span class="sxs-lookup"><span data-stu-id="7a4d6-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a4d6-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7a4d6-137">Minimum supported client</span></span><br/> | <span data-ttu-id="7a4d6-138">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7a4d6-138">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="7a4d6-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7a4d6-139">Minimum supported server</span></span><br/> | <span data-ttu-id="7a4d6-140">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7a4d6-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="7a4d6-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="7a4d6-141">Namespace</span></span><br/>                | <span data-ttu-id="7a4d6-142">Root \\ CIMV2 \\ Security- \\ mikrosofttpm</span><span class="sxs-lookup"><span data-stu-id="7a4d6-142">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="7a4d6-143">MOF</span><span class="sxs-lookup"><span data-stu-id="7a4d6-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7a4d6-144"><dt>Win32- \_ TPM. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7a4d6-144"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="7a4d6-145">DLL</span><span class="sxs-lookup"><span data-stu-id="7a4d6-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a4d6-146"><dt>Win32- \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a4d6-146"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a4d6-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a4d6-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a4d6-148">**Win32- \_ TPM**</span><span class="sxs-lookup"><span data-stu-id="7a4d6-148">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="7a4d6-149">**Setphysicalpresencerequest**</span><span class="sxs-lookup"><span data-stu-id="7a4d6-149">**SetPhysicalPresenceRequest**</span></span>](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 

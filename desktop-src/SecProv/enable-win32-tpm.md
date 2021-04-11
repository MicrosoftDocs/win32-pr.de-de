---
description: Ermöglicht dem TPM-Besitzer, das TPM zu aktivieren oder fortzusetzen.
ms.assetid: 9fb0b0aa-a569-4c0c-859e-8640480dbb3e
title: Enable-Methode der Win32_Tpm-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.Enable
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 6fe79ee44cb2ef6494b770a53cb57f7b88943dc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216191"
---
# <a name="enable-method-of-the-win32_tpm-class"></a><span data-ttu-id="17e3d-103">Enable-Methode der Win32- \_ TPM-Klasse</span><span class="sxs-lookup"><span data-stu-id="17e3d-103">Enable method of the Win32\_Tpm class</span></span>

<span data-ttu-id="17e3d-104">Mit der **enable** -Methode der [**Win32 \_ TPM**](win32-tpm.md) -Klasse kann der TPM-Besitzer das TPM aktivieren oder fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="17e3d-104">The **Enable** method of the [**Win32\_Tpm**](win32-tpm.md) class allows the TPM owner to enable or resume the TPM.</span></span>

<span data-ttu-id="17e3d-105">Zum Ausführen dieser Methode muss das TPM bereits über einen Besitzer verfügen.</span><span class="sxs-lookup"><span data-stu-id="17e3d-105">To run this method, the TPM must already have an owner.</span></span> <span data-ttu-id="17e3d-106">Verwenden Sie die [**setphysicalpresencerequest**](setphysicalpresencerequest-win32-tpm.md) -Methode, um ein TPM zu aktivieren, das nicht bereits über einen Besitzer verfügt.</span><span class="sxs-lookup"><span data-stu-id="17e3d-106">To enable a TPM that does not already have an owner, use the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="17e3d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="17e3d-107">Syntax</span></span>


```mof
uint32 Enable(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="17e3d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="17e3d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17e3d-109">Besitzer *des Besitzers* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="17e3d-109">*OwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="17e3d-110">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="17e3d-110">Type: **string**</span></span>

<span data-ttu-id="17e3d-111">Eine Zeichenfolge, die den TPM-Besitzer angibt.</span><span class="sxs-lookup"><span data-stu-id="17e3d-111">A string that identifies the TPM owner.</span></span> <span data-ttu-id="17e3d-112">Bei dieser Zeichenfolge muss es sich um eine Base64-codierte Zeichenfolge handeln, die genau 20 Byte Binärdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="17e3d-112">This string must be a base64-encoded string that contains exactly 20 bytes of binary data.</span></span> <span data-ttu-id="17e3d-113">Verwenden Sie die [**converttobesitzauth**](converttoownerauth-win32-tpm.md) -Methode, um eine Passphrase in dieses erwartete Format zu übersetzen.</span><span class="sxs-lookup"><span data-stu-id="17e3d-113">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a passphrase to this expected format.</span></span> <span data-ttu-id="17e3d-114">Der Parameter " *besitzauth* " wird aus der Registrierung gelesen, wenn kein Wert angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="17e3d-114">The *OwnerAuth* parameter is read from the registry if none is provided.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17e3d-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="17e3d-115">Return value</span></span>

<span data-ttu-id="17e3d-116">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="17e3d-116">Type: **uint32**</span></span>

<span data-ttu-id="17e3d-117">Alle TPM-Fehler sowie Fehler, die für die TPM-Basisdienste spezifisch sind, können zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="17e3d-117">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="17e3d-118">In der folgenden Tabelle sind einige der allgemeinen Rückgabecodes aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="17e3d-118">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="17e3d-119">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="17e3d-119">Return code/value</span></span>                                                                                                                                                                         | <span data-ttu-id="17e3d-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="17e3d-120">Description</span></span>                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="17e3d-121"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="17e3d-121"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                         | <span data-ttu-id="17e3d-122">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="17e3d-122">The method was successful.</span></span><br/>                                                                                                                                                |
| <dl> <span data-ttu-id="17e3d-123"><dt>**TPM \_ E \_ authfail**</dt> <dt>2150105089 (0x80280001)</dt></span><span class="sxs-lookup"><span data-stu-id="17e3d-123"><dt>**TPM\_E\_AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span></span> </dl>              | <span data-ttu-id="17e3d-124">Der angegebene Besitzer Autorisierungs Wert kann die Anforderung nicht ausführen.</span><span class="sxs-lookup"><span data-stu-id="17e3d-124">The provided owner authorization value cannot perform the request.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="17e3d-125"><dt>**TPM \_ E \_ Verteidigung \_ der \_ Sperre**</dt> mit <dt>2150107139 (0x80280803)</dt></span><span class="sxs-lookup"><span data-stu-id="17e3d-125"><dt>**TPM\_E\_DEFEND\_LOCK\_RUNNING**</dt> <dt>2150107139 (0x80280803)</dt></span></span> </dl> | <span data-ttu-id="17e3d-126">Das TPM steht für Wörterbuchangriffe und befindet sich in einem Timeout Zeitraum.</span><span class="sxs-lookup"><span data-stu-id="17e3d-126">The TPM is defending against dictionary attacks and is in a time-out period.</span></span> <span data-ttu-id="17e3d-127">Weitere Informationen finden Sie unter der [**resetauthlockout**](resetauthlockout-win32-tpm.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="17e3d-127">For more information, see the [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="17e3d-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="17e3d-128">Remarks</span></span>

<span data-ttu-id="17e3d-129">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="17e3d-129">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="17e3d-130">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="17e3d-130">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="17e3d-131">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="17e3d-131">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="17e3d-132">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="17e3d-132">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="17e3d-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="17e3d-133">Requirements</span></span>



| <span data-ttu-id="17e3d-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="17e3d-134">Requirement</span></span> | <span data-ttu-id="17e3d-135">Wert</span><span class="sxs-lookup"><span data-stu-id="17e3d-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="17e3d-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="17e3d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="17e3d-137">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="17e3d-137">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="17e3d-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="17e3d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="17e3d-139">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="17e3d-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="17e3d-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="17e3d-140">Namespace</span></span><br/>                | <span data-ttu-id="17e3d-141">Root \\ CIMV2 \\ Security- \\ mikrosofttpm</span><span class="sxs-lookup"><span data-stu-id="17e3d-141">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="17e3d-142">MOF</span><span class="sxs-lookup"><span data-stu-id="17e3d-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="17e3d-143"><dt>Win32- \_ TPM. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="17e3d-143"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="17e3d-144">DLL</span><span class="sxs-lookup"><span data-stu-id="17e3d-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17e3d-145"><dt>Win32- \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17e3d-145"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17e3d-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17e3d-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17e3d-147">**Win32- \_ TPM**</span><span class="sxs-lookup"><span data-stu-id="17e3d-147">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="17e3d-148">**Setphysicalpresencerequest**</span><span class="sxs-lookup"><span data-stu-id="17e3d-148">**SetPhysicalPresenceRequest**</span></span>](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 

---
description: Setzt den SRK-Autorisierungs Wert (Storage Root Key) so zurück, dass er mit dem Betriebssystem kompatibel ist.
ms.assetid: af008733-b43c-4017-9e79-bdd98f2e20b6
title: Resegzrkauth-Methode der Win32_Tpm-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ResetSrkAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 7d838ded7051511b6a8f9117327ee7cdb1a00d7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348909"
---
# <a name="resetsrkauth-method-of-the-win32_tpm-class"></a><span data-ttu-id="2241e-103">Resegzrkauth-Methode der Win32- \_ TPM-Klasse</span><span class="sxs-lookup"><span data-stu-id="2241e-103">ResetSrkAuth method of the Win32\_Tpm class</span></span>

<span data-ttu-id="2241e-104">Die **resetsrkauth** -Methode der [**Win32- \_ TPM**](win32-tpm.md) -Klasse setzt den SRK-Autorisierungs Wert (Storage Root Key) zurück, sodass er mit dem Betriebssystem kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="2241e-104">The **ResetSrkAuth** method of the [**Win32\_Tpm**](win32-tpm.md) class resets the Storage Root Key (SRK) authorization value to be compatible with the operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="2241e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2241e-105">Syntax</span></span>


```mof
uint32 ResetSrkAuth(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="2241e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2241e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2241e-107">Besitzer *des Besitzers* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="2241e-107">*OwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2241e-108">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2241e-108">Type: **string**</span></span>

<span data-ttu-id="2241e-109">Eine Zeichenfolge, die den TPM-Besitzer angibt.</span><span class="sxs-lookup"><span data-stu-id="2241e-109">A string that identifies the TPM owner.</span></span> <span data-ttu-id="2241e-110">Diese Zeichenfolge muss eine Base64-codierte NULL-terminierte Zeichenfolge sein, die genau 20 Bytes Binärdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="2241e-110">This string must be a base64-encoded null-terminated string that contains exactly 20 bytes of binary data.</span></span> <span data-ttu-id="2241e-111">Verwenden Sie die [**converttobesitzauth**](converttoownerauth-win32-tpm.md) -Methode, um eine Passphrase in dieses erwartete Format zu übersetzen.</span><span class="sxs-lookup"><span data-stu-id="2241e-111">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a passphrase to this expected format.</span></span> <span data-ttu-id="2241e-112">Der Parameter " *besitzauth* " wird aus der Registrierung gelesen, wenn kein Wert angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2241e-112">The *OwnerAuth* parameter is read from the registry if none is provided.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2241e-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2241e-113">Return value</span></span>

<span data-ttu-id="2241e-114">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2241e-114">Type: **uint32**</span></span>

<span data-ttu-id="2241e-115">Alle TPM-Fehler sowie Fehler, die für die TPM-Basisdienste spezifisch sind, können zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2241e-115">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="2241e-116">In der folgenden Tabelle sind einige der allgemeinen Rückgabecodes aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="2241e-116">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="2241e-117">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="2241e-117">Return code/value</span></span>                                                                                                                                                                         | <span data-ttu-id="2241e-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2241e-118">Description</span></span>                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2241e-119"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="2241e-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                         | <span data-ttu-id="2241e-120">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="2241e-120">The method was successful.</span></span><br/>                                                                                                                                                |
| <dl> <span data-ttu-id="2241e-121"><dt> **TPM \_ E \_ authfail**</dt> <dt>2150105089 (0x80280001)</dt></span><span class="sxs-lookup"><span data-stu-id="2241e-121"><dt>**TPM\_E\_AUTHFAIL** </dt> <dt>2150105089 (0x80280001)</dt></span></span> </dl>             | <span data-ttu-id="2241e-122">Der angegebene Besitzer Autorisierungs Wert kann die Anforderung nicht erfüllen.</span><span class="sxs-lookup"><span data-stu-id="2241e-122">The provided owner authorization value cannot fulfill the request.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="2241e-123"><dt>**TPM \_ E \_ Verteidigung \_ der \_ Sperre**</dt> mit <dt>2150107139 (0x80280803)</dt></span><span class="sxs-lookup"><span data-stu-id="2241e-123"><dt>**TPM\_E\_DEFEND\_LOCK\_RUNNING**</dt> <dt>2150107139 (0x80280803)</dt></span></span> </dl> | <span data-ttu-id="2241e-124">Das TPM steht für Wörterbuchangriffe und befindet sich in einem Timeout Zeitraum.</span><span class="sxs-lookup"><span data-stu-id="2241e-124">The TPM is defending against dictionary attacks and is in a time-out period.</span></span> <span data-ttu-id="2241e-125">Weitere Informationen finden Sie unter der [**resetauthlockout**](resetauthlockout-win32-tpm.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="2241e-125">For more information, see the [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2241e-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2241e-126">Remarks</span></span>

<span data-ttu-id="2241e-127">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="2241e-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="2241e-128">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="2241e-128">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="2241e-129">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="2241e-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="2241e-130">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="2241e-130">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2241e-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2241e-131">Requirements</span></span>



| <span data-ttu-id="2241e-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2241e-132">Requirement</span></span> | <span data-ttu-id="2241e-133">Wert</span><span class="sxs-lookup"><span data-stu-id="2241e-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="2241e-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2241e-134">Minimum supported client</span></span><br/> | <span data-ttu-id="2241e-135">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2241e-135">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="2241e-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2241e-136">Minimum supported server</span></span><br/> | <span data-ttu-id="2241e-137">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2241e-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="2241e-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="2241e-138">Namespace</span></span><br/>                | <span data-ttu-id="2241e-139">Root \\ CIMV2 \\ Security- \\ mikrosofttpm</span><span class="sxs-lookup"><span data-stu-id="2241e-139">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="2241e-140">MOF</span><span class="sxs-lookup"><span data-stu-id="2241e-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2241e-141"><dt>Win32- \_ TPM. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2241e-141"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="2241e-142">DLL</span><span class="sxs-lookup"><span data-stu-id="2241e-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2241e-143"><dt>Win32- \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2241e-143"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2241e-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2241e-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2241e-145">**Win32- \_ TPM**</span><span class="sxs-lookup"><span data-stu-id="2241e-145">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 

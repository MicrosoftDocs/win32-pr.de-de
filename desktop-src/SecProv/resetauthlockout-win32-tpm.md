---
description: Setzt den Timeout Zeitraum oder einen anderen Mechanismus, den TPM-Hersteller implementiert, zum Schutz vor Wörterbuchangriffen auf TPM-Autorisierungs Werten zurück.
ms.assetid: c2fba6a2-2d03-4ffd-9841-4a9eac0a20ac
title: Resetauthlockout-Methode der Win32_Tpm-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ResetAuthLockOut
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: d28287e410fbaf65ce5b1e617113c35cfece160b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345680"
---
# <a name="resetauthlockout-method-of-the-win32_tpm-class"></a><span data-ttu-id="74649-103">Resetauthlockout-Methode der Win32 \_ TPM-Klasse</span><span class="sxs-lookup"><span data-stu-id="74649-103">ResetAuthLockOut method of the Win32\_Tpm class</span></span>

<span data-ttu-id="74649-104">Die **resetauthlockout** -Methode der [**Win32 \_ TPM**](win32-tpm.md) -Klasse setzt den Timeout Zeitraum oder einen anderen Mechanismus zurück, den TPM-Hersteller implementieren, um gegen Wörterbuchangriffe auf TPM-Autorisierungs Werte zu schützen.</span><span class="sxs-lookup"><span data-stu-id="74649-104">The **ResetAuthLockOut** method of the [**Win32\_Tpm**](win32-tpm.md) class resets the time-out period or other mechanism that TPM manufacturers implement to protect against dictionary attacks on TPM authorization values.</span></span> <span data-ttu-id="74649-105">Bei einem Wörterbuch Angriff versucht ein Angreifer, einen korrekten TPM-Autorisierungs Wert zu erraten, indem er alle möglichen Werte vollständig versucht.</span><span class="sxs-lookup"><span data-stu-id="74649-105">In a dictionary attack, an attacker tries to guess a correct TPM authorization value by exhaustively attempting all possible values.</span></span>

<span data-ttu-id="74649-106">Verwenden Sie diese Methode, wenn das TPM gesperrt ist, weil zu viele falsche Versuche bei der Eingabe der Besitzer Autorisierung oder anderer Autorisierungs Werte aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="74649-106">Use this method if the TPM is locked out due to too many incorrect attempts at entering the owner authorization or other authorization values.</span></span> <span data-ttu-id="74649-107">Wenn das TPM gesperrt ist, geben einige oder alle Befehle, die für das TPM ausgegeben werden, einen Fehler zurück, TPM \_ E verteidigt die Sperre, die \_ ausgeführt wird \_ \_ (0x80280803).</span><span class="sxs-lookup"><span data-stu-id="74649-107">When the TPM is locked out, some or all commands issued to the TPM will return an error, TPM\_E\_DEFEND\_LOCK\_RUNNING (0x80280803).</span></span>

> [!Note]  
> <span data-ttu-id="74649-108">Diese Methode kann nur einmal verwendet werden, wenn das TPM gesperrt ist. Wenn die für diese Methode angegebene Besitzer Autorisierung falsch ist, wird das TPM für den gesamten Timeout Zeitraum gesperrt, und zusätzliche Versuche beim Zurücksetzen der Sperre sind nicht erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="74649-108">This method can only be used exactly once when the TPM is locked out. If the owner authorization provided to this method is incorrect, the TPM will lock out for the entire time-out period and additional attempts at resetting the lock will fail.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="74649-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="74649-109">Syntax</span></span>


```mof
uint32 ResetAuthLockOut(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="74649-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="74649-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74649-111">Besitzer *des Besitzers* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="74649-111">*OwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="74649-112">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="74649-112">Type: **string**</span></span>

<span data-ttu-id="74649-113">Eine Zeichenfolge, die den TPM-Besitzer angibt.</span><span class="sxs-lookup"><span data-stu-id="74649-113">A string that identifies the TPM owner.</span></span>

<span data-ttu-id="74649-114">Diese Zeichenfolge muss eine Base64-codierte NULL-terminierte Zeichenfolge sein, die genau 20 Bytes Binärdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="74649-114">This string must be a base64-encoded null-terminated string that contains exactly 20 bytes of binary data.</span></span> <span data-ttu-id="74649-115">Verwenden Sie die [**converttobesitzauth**](converttoownerauth-win32-tpm.md) -Methode, um eine Passphrase in dieses erwartete Format zu übersetzen.</span><span class="sxs-lookup"><span data-stu-id="74649-115">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a passphrase to this expected format.</span></span> <span data-ttu-id="74649-116">Der Parameter " *besitzauth* " wird aus der Registrierung gelesen, wenn kein Wert angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="74649-116">The *OwnerAuth* parameter is read from the registry if none is provided.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74649-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="74649-117">Return value</span></span>

<span data-ttu-id="74649-118">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74649-118">Type: **uint32**</span></span>

<span data-ttu-id="74649-119">Alle TPM-Fehler sowie Fehler, die für die TPM-Basisdienste spezifisch sind, können zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="74649-119">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span> <span data-ttu-id="74649-120">In der folgenden Tabelle sind einige der gemeinsamen Rückgabewerte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="74649-120">The following table lists some of the common return values.</span></span>



| <span data-ttu-id="74649-121">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="74649-121">Return code/value</span></span>                                                                                                                                                            | <span data-ttu-id="74649-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="74649-122">Description</span></span>                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="74649-123"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="74649-123"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                            | <span data-ttu-id="74649-124">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="74649-124">The method was successful.</span></span><br/>                                                                                                                                                                                                                                     |
| <dl> <span data-ttu-id="74649-125"><dt>**TPM \_ E \_ authfail**</dt> <dt>2150105089 (0x80280001)</dt></span><span class="sxs-lookup"><span data-stu-id="74649-125"><dt>**TPM\_E\_AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span></span> </dl> | <span data-ttu-id="74649-126">Der angegebene Besitzer Autorisierungs Wert ist falsch.</span><span class="sxs-lookup"><span data-stu-id="74649-126">The provided owner authorization value is incorrect.</span></span> <span data-ttu-id="74649-127">Weitere Versuche, die Sperre zurückzusetzen, führen zu diesem Fehler.</span><span class="sxs-lookup"><span data-stu-id="74649-127">Additional attempts at resetting the lock will fail with this same error.</span></span> <span data-ttu-id="74649-128">Warten Sie, bis der Timeout Zeitraum oder ein anderer Hersteller spezifischer Mechanismus abgelaufen ist, bevor Sie die gesperrten TPM-Befehle wiederholen.</span><span class="sxs-lookup"><span data-stu-id="74649-128">Please wait until the time-out period or other manufacturer-specific mechanism has expired before retrying locked TPM commands.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="74649-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="74649-129">Remarks</span></span>

<span data-ttu-id="74649-130">Diese Methode ruft den TPM \_ resetlockvalue-Befehl auf dem TPM auf.</span><span class="sxs-lookup"><span data-stu-id="74649-130">This method calls the TPM\_ResetLockValue command on the TPM.</span></span> <span data-ttu-id="74649-131">Das genaue Verhalten dieser Methode variiert je nach TPM-Hersteller.</span><span class="sxs-lookup"><span data-stu-id="74649-131">The exact behavior of this method varies among TPM manufacturers.</span></span> <span data-ttu-id="74649-132">Die Dokumentation des Computers oder des TPM-Herstellers bietet möglicherweise zusätzliche Informationen zur Implementierung des antidictionary-Angriffs Mechanismus.</span><span class="sxs-lookup"><span data-stu-id="74649-132">Documentation from the computer or TPM manufacturer may provide additional information on the implementation of the anti-dictionary attack mechanism.</span></span>

<span data-ttu-id="74649-133">Im Allgemeinen können Hersteller von Wörterbuchangriffen erkennen, indem Sie fehlgeschlagene Authentifizierungen verfolgen.</span><span class="sxs-lookup"><span data-stu-id="74649-133">In general, manufacturers can detect dictionary attacks by keeping track of failed authentications.</span></span> <span data-ttu-id="74649-134">Wenn die Anzahl oder Häufigkeit von Fehlern hoch genug ist, sperrt das TPM weitere Befehle für eine bestimmte Zeit.</span><span class="sxs-lookup"><span data-stu-id="74649-134">If the number or frequency of failures become high enough, the TPM will lock out further commands for a certain time.</span></span> <span data-ttu-id="74649-135">Im Allgemeinen ist der anfängliche Timeout Zeitraum kurz, damit ein berechtigter Benutzer die Möglichkeit hat, die Situation zu beheben.</span><span class="sxs-lookup"><span data-stu-id="74649-135">Generally, the initial time-out period will be short, to allow a legitimate user a chance to correct the situation.</span></span> <span data-ttu-id="74649-136">Wenn der Fehler weiterhin auftritt, kann sich die Dauer der nachfolgenden Timeout Zeiten schnell erhöhen.</span><span class="sxs-lookup"><span data-stu-id="74649-136">If failures continue, the duration of each subsequent time-out period may increase rapidly.</span></span>

<span data-ttu-id="74649-137">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="74649-137">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="74649-138">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="74649-138">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="74649-139">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="74649-139">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="74649-140">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="74649-140">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="74649-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="74649-141">Requirements</span></span>



| <span data-ttu-id="74649-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="74649-142">Requirement</span></span> | <span data-ttu-id="74649-143">Wert</span><span class="sxs-lookup"><span data-stu-id="74649-143">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="74649-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="74649-144">Minimum supported client</span></span><br/> | <span data-ttu-id="74649-145">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="74649-145">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="74649-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="74649-146">Minimum supported server</span></span><br/> | <span data-ttu-id="74649-147">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="74649-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="74649-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="74649-148">Namespace</span></span><br/>                | <span data-ttu-id="74649-149">Root \\ CIMV2 \\ Security- \\ mikrosofttpm</span><span class="sxs-lookup"><span data-stu-id="74649-149">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="74649-150">MOF</span><span class="sxs-lookup"><span data-stu-id="74649-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="74649-151"><dt>Win32- \_ TPM. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="74649-151"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="74649-152">DLL</span><span class="sxs-lookup"><span data-stu-id="74649-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74649-153"><dt>Win32- \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74649-153"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74649-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="74649-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74649-155">**Win32- \_ TPM**</span><span class="sxs-lookup"><span data-stu-id="74649-155">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 

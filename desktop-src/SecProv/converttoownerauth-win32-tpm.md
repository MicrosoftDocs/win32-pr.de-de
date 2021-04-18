---
description: Übersetzt eine vom Benutzer bereitgestellte Passphrase-Eingabe in eine 20-Byte-Besitzer Autorisierung, die für die Interaktion mit dem TPM verwendet werden kann. Methoden wie TakeOwnership und resetauthlockout erfordern den resultierenden Besitzer Autorisierungs Wert.
ms.assetid: 69eed934-1668-495a-b5b7-cd4a87df1ab3
title: Converttbesitzauth-Methode der Win32_Tpm-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ConvertToOwnerAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: f3de5803d10458156fb453e964d782f7c9760333
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358589"
---
# <a name="converttoownerauth-method-of-the-win32_tpm-class"></a><span data-ttu-id="5f8b0-104">Converttbesitzauth-Methode der Win32- \_ TPM-Klasse</span><span class="sxs-lookup"><span data-stu-id="5f8b0-104">ConvertToOwnerAuth method of the Win32\_Tpm class</span></span>

<span data-ttu-id="5f8b0-105">Die **converttobesitzauth** -Methode der [**Win32- \_ TPM**](win32-tpm.md) -Klasse übersetzt eine vom Benutzer bereitgestellte Passphrase-Eingabe in eine 20-Byte-Besitzer Autorisierung, die für die Interaktion mit dem TPM verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="5f8b0-105">The **ConvertToOwnerAuth** method of the [**Win32\_Tpm**](win32-tpm.md) class translates a user-provided passphrase input into a 20-byte owner authorization that can be used to interact with the TPM.</span></span> <span data-ttu-id="5f8b0-106">Methoden wie [**TakeOwnership**](takeownership-win32-tpm.md) und [**resetauthlockout**](resetauthlockout-win32-tpm.md) erfordern den resultierenden Besitzer Autorisierungs Wert.</span><span class="sxs-lookup"><span data-stu-id="5f8b0-106">Methods such as [**TakeOwnership**](takeownership-win32-tpm.md) and [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) require the resulting owner authorization value.</span></span>

<span data-ttu-id="5f8b0-107">Der Konvertierungsprozess folgt den Spezifikationen aus der [Trusted Computing Group](https://www.trustedcomputinggroup.org/).</span><span class="sxs-lookup"><span data-stu-id="5f8b0-107">The conversion process follows the specifications from the [Trusted Computing Group](https://www.trustedcomputinggroup.org/).</span></span>

## <a name="syntax"></a><span data-ttu-id="5f8b0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f8b0-108">Syntax</span></span>


```mof
uint32 ConvertToOwnerAuth(
  [in]  string OwnerPassPhrase,
  [out] string OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="5f8b0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f8b0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f8b0-110">Besitzer *Passphrase* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5f8b0-110">*OwnerPassPhrase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f8b0-111">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5f8b0-111">Type: **string**</span></span>

<span data-ttu-id="5f8b0-112">Eine Zeichenfolge, die in einen Besitzer Autorisierungs Wert konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="5f8b0-112">A string to convert to an owner authorization value.</span></span> <span data-ttu-id="5f8b0-113">Die Zeichenfolge kann eine beliebige Anzahl von alphanumerischen Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="5f8b0-113">The string can contain any number of alphanumeric characters.</span></span>

</dd> <dt>

<span data-ttu-id="5f8b0-114">Besitzer *des Besitzers* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5f8b0-114">*OwnerAuth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f8b0-115">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5f8b0-115">Type: **string**</span></span>

<span data-ttu-id="5f8b0-116">Eine Zeichenfolge, die vom Besitzer *Passphrase* -Parameter abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="5f8b0-116">A string derived from the *OwnerPassPhrase* parameter.</span></span> <span data-ttu-id="5f8b0-117">Dieser Wert ist ein 20-Byte-Binärwert, der in eine mit **null** endender Base64-NULL endenden Zeichenfolge codiert ist</span><span class="sxs-lookup"><span data-stu-id="5f8b0-117">This value is a 20-byte binary value encoded to a 28-byte base64 **null**-terminated string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f8b0-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5f8b0-118">Return value</span></span>

<span data-ttu-id="5f8b0-119">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5f8b0-119">Type: **uint32**</span></span>

<span data-ttu-id="5f8b0-120">Alle TPM-Fehler sowie Fehler, die für die TPM-Basisdienste spezifisch sind, können zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5f8b0-120">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="5f8b0-121">In der folgenden Tabelle sind einige der allgemeinen Rückgabecodes aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="5f8b0-121">The following tables lists some of the common return codes.</span></span>



| <span data-ttu-id="5f8b0-122">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="5f8b0-122">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="5f8b0-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5f8b0-123">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="5f8b0-124"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="5f8b0-124"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="5f8b0-125">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="5f8b0-125">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5f8b0-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5f8b0-126">Remarks</span></span>

<span data-ttu-id="5f8b0-127">Eine Unicode-UTF-16LE-codierte Zeichenfolge wird in den 20-Byte-TPM-Besitzer Autorisierungs Wert konvertiert, indem der SHA-1-Hash der binären Darstellung der Zeichenfolge verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5f8b0-127">A Unicode UTF-16LE encoded string is converted to the 20-byte TPM owner authorization value by taking the SHA-1 hash of the string's binary representation.</span></span> <span data-ttu-id="5f8b0-128">Der **null** -Abbruch der Unicode-Zeichenfolge ist nicht im Hash enthalten.</span><span class="sxs-lookup"><span data-stu-id="5f8b0-128">The **null** termination of the Unicode string is not included in the hash.</span></span> <span data-ttu-id="5f8b0-129">Im SHA-1-Hash wird kein Salt verwendet.</span><span class="sxs-lookup"><span data-stu-id="5f8b0-129">No salt is used in the SHA-1 hash.</span></span>

<span data-ttu-id="5f8b0-130">Wenn Sie z. b. die TPM-Besitzer Passphrase "1sample" in einen TPM-Besitzer Autorisierungs Wert konvertieren möchten, wird der SHA-1-Hash aus dem folgenden Bytestream entnommen:</span><span class="sxs-lookup"><span data-stu-id="5f8b0-130">For example, to convert the TPM owner passphrase "1Sample" to a TPM owner authorization value, the SHA-1 hash is taken from the following byte stream:</span></span>

`0x31 0x00 0x53 0x00 0x61 0x00 0x6D 0x00 0x70 0x00 0x6C 0x00 0x65 0x00`

<span data-ttu-id="5f8b0-131">Um eine Passphrase der Länge 0 (null) in einen Besitzer Autorisierungs Wert zu konvertieren, wird der SHA-1-Hash aus dem **null** -Bytestream entnommen.</span><span class="sxs-lookup"><span data-stu-id="5f8b0-131">To convert a zero-length passphrase to an owner authorization value, the SHA-1 hash is taken of the **NULL** byte stream.</span></span>

<span data-ttu-id="5f8b0-132">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="5f8b0-132">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5f8b0-133">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="5f8b0-133">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="5f8b0-134">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5f8b0-134">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5f8b0-135">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="5f8b0-135">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5f8b0-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5f8b0-136">Requirements</span></span>



| <span data-ttu-id="5f8b0-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5f8b0-137">Requirement</span></span> | <span data-ttu-id="5f8b0-138">Wert</span><span class="sxs-lookup"><span data-stu-id="5f8b0-138">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f8b0-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5f8b0-139">Minimum supported client</span></span><br/> | <span data-ttu-id="5f8b0-140">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5f8b0-140">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="5f8b0-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5f8b0-141">Minimum supported server</span></span><br/> | <span data-ttu-id="5f8b0-142">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5f8b0-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="5f8b0-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="5f8b0-143">Namespace</span></span><br/>                | <span data-ttu-id="5f8b0-144">Root \\ CIMV2 \\ Security- \\ mikrosofttpm</span><span class="sxs-lookup"><span data-stu-id="5f8b0-144">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="5f8b0-145">MOF</span><span class="sxs-lookup"><span data-stu-id="5f8b0-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5f8b0-146"><dt>Win32- \_ TPM. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5f8b0-146"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="5f8b0-147">DLL</span><span class="sxs-lookup"><span data-stu-id="5f8b0-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f8b0-148"><dt>Win32- \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f8b0-148"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f8b0-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f8b0-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f8b0-150">**Win32- \_ TPM**</span><span class="sxs-lookup"><span data-stu-id="5f8b0-150">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="5f8b0-151">**TakeOwnership**</span><span class="sxs-lookup"><span data-stu-id="5f8b0-151">**TakeOwnership**</span></span>](takeownership-win32-tpm.md)
</dt> </dl>

 

 

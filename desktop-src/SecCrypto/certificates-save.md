---
description: Speichert die Zertifikat Objekte in der Auflistung.
ms.assetid: 1d4b7bd5-3ed3-4ace-9894-4e89c5cf844f
title: Zertifikats. Save-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Save
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 36ab04b394bddcd829d9f15e7562b72125388d33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367833"
---
# <a name="certificatessave-method"></a><span data-ttu-id="f8fe5-103">Zertifikats. Save-Methode</span><span class="sxs-lookup"><span data-stu-id="f8fe5-103">Certificates.Save method</span></span>

<span data-ttu-id="f8fe5-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f8fe5-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="f8fe5-105">Verwenden Sie stattdessen die [**X509Certificate2Collection-Klasse**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="f8fe5-105">Instead, use the [**X509Certificate2Collection Class**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="f8fe5-106">Mit der **Save** -Methode werden die [**Zertifikat**](certificate.md) Objekte in der Auflistung gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f8fe5-106">The **Save** method saves the [**Certificate**](certificate.md) objects in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8fe5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8fe5-107">Syntax</span></span>


```VB
Certificates.Save( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal SaveAs ], _
  [ ByVal ExportFlag ] _
)
```



## <a name="parameters"></a><span data-ttu-id="f8fe5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8fe5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8fe5-109">*Dateiname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f8fe5-109">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8fe5-110">Eine Zeichenfolge, die den Namen der Ausgabedatei enthält, in der die Zertifikate gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="f8fe5-110">A string that contains the name of the output file where the certificates will be saved.</span></span>

</dd> <dt>

<span data-ttu-id="f8fe5-111">*Kennwort* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="f8fe5-111">*Password* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f8fe5-112">Eine Zeichenfolge, die das [*Klartext*](../secgloss/p-gly.md) -Kennwort für eine Datei mit einem [*privaten Schlüssel*](../secgloss/p-gly.md) enthält.</span><span class="sxs-lookup"><span data-stu-id="f8fe5-112">A string that contains the [*plaintext*](../secgloss/p-gly.md) password for a [*private key*](../secgloss/p-gly.md) file.</span></span> <span data-ttu-id="f8fe5-113">Der Standardwert ist eine leere Zeichenfolge ("").</span><span class="sxs-lookup"><span data-stu-id="f8fe5-113">The default value is the empty string ("").</span></span> <span data-ttu-id="f8fe5-114">Bis zu 32 Unicode-Zeichen, einschließlich eines abschließenden NULL-Zeichens, können für das Kennwort verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f8fe5-114">Up to 32 Unicode characters, including a terminating null character, can be used for the password.</span></span> <span data-ttu-id="f8fe5-115">Informationen zum Schützen des Kennworts finden Sie unter Behandeln von Kenn [Wörtern](../secbp/handling-passwords.md).</span><span class="sxs-lookup"><span data-stu-id="f8fe5-115">For information about protecting the password, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8fe5-116">*SaveAs* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="f8fe5-116">*SaveAs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f8fe5-117">Ein Wert der [**CAPICOM- \_ Zertifikate \_ Save \_ As \_ Type**](capicom-certificates-save-as-type.md) -Enumeration, die das Format der Ausgabedatei angibt.</span><span class="sxs-lookup"><span data-stu-id="f8fe5-117">A value of the [**CAPICOM\_CERTIFICATES\_SAVE\_AS\_TYPE**](capicom-certificates-save-as-type.md) enumeration that specifies the format of the output file.</span></span> <span data-ttu-id="f8fe5-118">Der Standardwert sind CAPICOM-Zertifikate, die \_ \_ \_ als \_ PFX gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="f8fe5-118">The default is CAPICOM\_CERTIFICATES\_SAVE\_AS\_PFX.</span></span> <span data-ttu-id="f8fe5-119">In der folgenden Tabelle sind die möglichen Werte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="f8fe5-119">The following table shows the possible values.</span></span>



| <span data-ttu-id="f8fe5-120">Wert</span><span class="sxs-lookup"><span data-stu-id="f8fe5-120">Value</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="f8fe5-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f8fe5-121">Meaning</span></span>                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATES_SAVE_AS_PFX"></span><span id="capicom_certificates_save_as_pfx"></span><dl> <span data-ttu-id="f8fe5-122"><dt>**CAPICOM \_ - \_ Zertifikate \_ als \_ PFX speichern**</dt></span><span class="sxs-lookup"><span data-stu-id="f8fe5-122"><dt>**CAPICOM\_CERTIFICATES\_SAVE\_AS\_PFX**</dt></span></span> </dl>                      | <span data-ttu-id="f8fe5-123">Die Zertifikate werden als PFX gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f8fe5-123">The certificates are saved as a PFX.</span></span><br/>      |
| <span id="CAPICOM_CERTIFICATES_SAVE_AS_PKCS7"></span><span id="capicom_certificates_save_as_pkcs7"></span><dl> <span data-ttu-id="f8fe5-124"><dt>**CAPICOM- \_ Zertifikate \_ speichern \_ als \_ PKCS7**</dt></span><span class="sxs-lookup"><span data-stu-id="f8fe5-124"><dt>**CAPICOM\_CERTIFICATES\_SAVE\_AS\_PKCS7**</dt></span></span> </dl>                | <span data-ttu-id="f8fe5-125">Die Zertifikate werden als PKCS 7 gespeichert \# .</span><span class="sxs-lookup"><span data-stu-id="f8fe5-125">The certificates are saved as a PKCS \#7.</span></span><br/> |
| <span id="CAPICOM_CERTIFICATES_SAVE_AS_SERIALIZED"></span><span id="capicom_certificates_save_as_serialized"></span><dl> <span data-ttu-id="f8fe5-126"><dt>**CAPICOM- \_ Zertifikate werden \_ \_ als \_ serialisiert gespeichert.**</dt></span><span class="sxs-lookup"><span data-stu-id="f8fe5-126"><dt>**CAPICOM\_CERTIFICATES\_SAVE\_AS\_SERIALIZED**</dt></span></span> </dl> | <span data-ttu-id="f8fe5-127">Die Zertifikate werden als serialisiert gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f8fe5-127">The certificates are saved as serialized.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f8fe5-128">*Exportflag* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="f8fe5-128">*ExportFlag* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f8fe5-129">Ein Wert der [**CAPICOM- \_ \_ exportflag**](capicom-export-flag.md) -Enumeration, der angibt, ob Export Fehler des privaten Schlüssels ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="f8fe5-129">A value of the [**CAPICOM\_EXPORT\_FLAG**](capicom-export-flag.md) enumeration that specifies whether any private key export errors are ignored.</span></span> <span data-ttu-id="f8fe5-130">Der Standardwert ist "CAPICOM \_ Export \_ default".</span><span class="sxs-lookup"><span data-stu-id="f8fe5-130">The default is CAPICOM\_EXPORT\_DEFAULT.</span></span> <span data-ttu-id="f8fe5-131">In der folgenden Tabelle sind die möglichen Werte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="f8fe5-131">The following table shows the possible values.</span></span>



| <span data-ttu-id="f8fe5-132">Wert</span><span class="sxs-lookup"><span data-stu-id="f8fe5-132">Value</span></span>                                                                                                                                                                                                                                                                                          | <span data-ttu-id="f8fe5-133">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f8fe5-133">Meaning</span></span>                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="CAPICOM_EXPORT_DEFAULT"></span><span id="capicom_export_default"></span><dl> <span data-ttu-id="f8fe5-134"><dt>**Standardwert für CAPICOM- \_ Export \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f8fe5-134"><dt>**CAPICOM\_EXPORT\_DEFAULT**</dt></span></span> </dl>                                                                                                      | <span data-ttu-id="f8fe5-135">Export Fehler des privaten Schlüssels werden nicht ignoriert.</span><span class="sxs-lookup"><span data-stu-id="f8fe5-135">Private key export errors are not ignored.</span></span><br/> |
| <span id="CAPICOM_EXPORT_IGNORE_PRIVATE_KEY_NOT_EXPORTABLE_ERROR"></span><span id="capicom_export_ignore_private_key_not_exportable_error"></span><dl> <span data-ttu-id="f8fe5-136"><dt>**CAPICOM \_ - \_ Export \_ \_ Fehler beim \_ nicht \_ exportierbaren privaten Schlüssel \_ ignorieren**</dt></span><span class="sxs-lookup"><span data-stu-id="f8fe5-136"><dt>**CAPICOM\_EXPORT\_IGNORE\_PRIVATE\_KEY\_NOT\_EXPORTABLE\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="f8fe5-137">Export Fehler des privaten Schlüssels werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="f8fe5-137">Private key export errors are ignored.</span></span><br/>     |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8fe5-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f8fe5-138">Return value</span></span>

<span data-ttu-id="f8fe5-139">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f8fe5-139">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8fe5-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f8fe5-140">Remarks</span></span>

<span data-ttu-id="f8fe5-141">Diese Methode löst CAPICOM \_ E \_ nicht \_ zulässig aus, wenn eine Skripterstellung aus einer webbasierten Anwendung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="f8fe5-141">This method raises CAPICOM\_E\_NOT\_ALLOWED when it is scripted from a web-based application.</span></span>

<span data-ttu-id="f8fe5-142">Die [**Zertifikat**](certificate.md) Objekte können mithilfe der [**Store. Load**](store-load.md) -Methode abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f8fe5-142">The [**Certificate**](certificate.md) objects can be retrieved by using the [**Store.Load**](store-load.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8fe5-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f8fe5-143">Requirements</span></span>



| <span data-ttu-id="f8fe5-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f8fe5-144">Requirement</span></span> | <span data-ttu-id="f8fe5-145">Wert</span><span class="sxs-lookup"><span data-stu-id="f8fe5-145">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8fe5-146">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="f8fe5-146">End of client support</span></span><br/> | <span data-ttu-id="f8fe5-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f8fe5-147">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f8fe5-148">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="f8fe5-148">End of server support</span></span><br/> | <span data-ttu-id="f8fe5-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f8fe5-149">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f8fe5-150">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="f8fe5-150">Redistributable</span></span><br/>       | <span data-ttu-id="f8fe5-151">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="f8fe5-151">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f8fe5-152">DLL</span><span class="sxs-lookup"><span data-stu-id="f8fe5-152">DLL</span></span><br/>                   | <dl> <span data-ttu-id="f8fe5-153"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8fe5-153"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8fe5-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f8fe5-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8fe5-155">**Zertifikate**</span><span class="sxs-lookup"><span data-stu-id="f8fe5-155">**Certificates**</span></span>](certificates.md)
</dt> </dl>

 

 

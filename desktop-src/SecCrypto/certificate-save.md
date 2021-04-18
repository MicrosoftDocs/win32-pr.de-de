---
description: Speichert das Zertifikat in einer Datei.
ms.assetid: 2012b39b-47fd-4071-9752-98bb10954fc0
title: 'ICertificate2:: Save-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Save
- ICertificate2.Save
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3427feb86c705f5558d083bc39673fdf77553f58
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364911"
---
# <a name="icertificate2save-method"></a><span data-ttu-id="db64c-103">ICertificate2:: Save-Methode</span><span class="sxs-lookup"><span data-stu-id="db64c-103">ICertificate2::Save method</span></span>

<span data-ttu-id="db64c-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="db64c-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="db64c-105">Verwenden Sie stattdessen die [**X509Certificate2-Klasse**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="db64c-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="db64c-106">Mit der **Save** -Methode wird das Zertifikat in einer Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="db64c-106">The **Save** method saves the certificate to a file.</span></span> <span data-ttu-id="db64c-107">Diese Methode wurde in CAPICOM 2,0 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="db64c-107">This method was introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="db64c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="db64c-108">Syntax</span></span>


```VB
Certificate.Save( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal SaveAs ], _
  [ ByVal IncludeOption ] _
)
```



## <a name="parameters"></a><span data-ttu-id="db64c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="db64c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db64c-110">*Dateiname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="db64c-110">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db64c-111">Eine Zeichenfolge, die den Namen der Ausgabedatei enthält, in der das Zertifikat gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="db64c-111">A string that contains the name of the output file where the certificate will be saved.</span></span>

</dd> <dt>

<span data-ttu-id="db64c-112">*Kennwort* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="db64c-112">*Password* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="db64c-113">Eine Zeichenfolge, die das [*Klartext*](../secgloss/p-gly.md) -Kennwort für eine Datei mit einem [*privaten Schlüssel*](../secgloss/p-gly.md) enthält.</span><span class="sxs-lookup"><span data-stu-id="db64c-113">A string that contains the [*plaintext*](../secgloss/p-gly.md) password for a [*private key*](../secgloss/p-gly.md) file.</span></span> <span data-ttu-id="db64c-114">Das Kennwort kann bis zu 32 Unicode-Zeichen enthalten, einschließlich eines abschließenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="db64c-114">The password can contain up to 32 Unicode characters, including a terminating null character.</span></span> <span data-ttu-id="db64c-115">Informationen zum Schützen des Kennworts finden Sie unter Behandeln von Kenn [Wörtern](../secbp/handling-passwords.md).</span><span class="sxs-lookup"><span data-stu-id="db64c-115">For information about protecting the password, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

</dd> <dt>

<span data-ttu-id="db64c-116">*SaveAs* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="db64c-116">*SaveAs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="db64c-117">Ein Wert des [**CAPICOM- \_ Zertifikats " \_ Save \_ As \_ Type**](capicom-certificate-save-as-type.md) Enumeration", das das Format der Ausgabedatei angibt.</span><span class="sxs-lookup"><span data-stu-id="db64c-117">A value of the [**CAPICOM\_CERTIFICATE\_SAVE\_AS\_TYPE**](capicom-certificate-save-as-type.md) enumeration that specifies the format of the output file.</span></span> <span data-ttu-id="db64c-118">Der Standardwert ist **CAPICOM \_ Certificate \_ Save \_ As \_ CER**.</span><span class="sxs-lookup"><span data-stu-id="db64c-118">The default is **CAPICOM\_CERTIFICATE\_SAVE\_AS\_CER**.</span></span> <span data-ttu-id="db64c-119">In der folgenden Tabelle sind die möglichen Werte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="db64c-119">The following table shows the possible values.</span></span>



| <span data-ttu-id="db64c-120">Wert</span><span class="sxs-lookup"><span data-stu-id="db64c-120">Value</span></span>                                                                                                                                                                                                                  | <span data-ttu-id="db64c-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="db64c-121">Meaning</span></span>                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_SAVE_AS_CER"></span><span id="capicom_certificate_save_as_cer"></span><dl> <span data-ttu-id="db64c-122"><dt>**CAPICOM- \_ Zertifikat \_ speichern \_ als \_ CER**</dt></span><span class="sxs-lookup"><span data-stu-id="db64c-122"><dt>**CAPICOM\_CERTIFICATE\_SAVE\_AS\_CER**</dt></span></span> </dl> | <span data-ttu-id="db64c-123">Die Ausgabedatei wird als CER-Datei formatiert, ohne dass private Schlüssel gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="db64c-123">The output file will be formatted as a .cer file with no private keys saved.</span></span><br/>                                                         |
| <span id="CAPICOM_CERTIFICATE_SAVE_AS_PFX"></span><span id="capicom_certificate_save_as_pfx"></span><dl> <span data-ttu-id="db64c-124"><dt>**CAPICOM \_ - \_ Zertifikat \_ als \_ PFX speichern**</dt></span><span class="sxs-lookup"><span data-stu-id="db64c-124"><dt>**CAPICOM\_CERTIFICATE\_SAVE\_AS\_PFX**</dt></span></span> </dl> | <span data-ttu-id="db64c-125">Die Ausgabedatei wird als PFX-Datei (PKCS \# 12) formatiert, und alle zugehörigen privaten Schlüssel, die exportierbar sind, werden ebenfalls gespeichert.</span><span class="sxs-lookup"><span data-stu-id="db64c-125">The output file will be formatted as a .pfx (PKCS \#12) file and any associated private keys that are exportable will also be saved.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="db64c-126">*IncludeOption* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="db64c-126">*IncludeOption* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="db64c-127">Ein Wert der [**CAPICOM \_ Certificate \_ include- \_ Option**](capicom-certificate-include-option.md) -Enumeration, die angibt, wie viele Zertifikate in der Kette in der Ausgabedatei gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="db64c-127">A value of the [**CAPICOM\_CERTIFICATE\_INCLUDE\_OPTION**](capicom-certificate-include-option.md) enumeration that specifies how many certificates in the chain are saved to the output file.</span></span> <span data-ttu-id="db64c-128">Der Standardwert ist "CAPICOM \_ Certificate \_ include \_ End \_ Entity \_ only".</span><span class="sxs-lookup"><span data-stu-id="db64c-128">The default is CAPICOM\_CERTIFICATE\_INCLUDE\_END\_ENTITY\_ONLY.</span></span> <span data-ttu-id="db64c-129">In der folgenden Tabelle sind die möglichen Werte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="db64c-129">The following table shows the possible values.</span></span>



| <span data-ttu-id="db64c-130">Wert</span><span class="sxs-lookup"><span data-stu-id="db64c-130">Value</span></span>                                                                                                                                                                                                                                                             | <span data-ttu-id="db64c-131">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="db64c-131">Meaning</span></span>                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_INCLUDE_CHAIN_EXCEPT_ROOT"></span><span id="capicom_certificate_include_chain_except_root"></span><dl> <span data-ttu-id="db64c-132"><dt>**CAPICOM- \_ Zertifikats \_ include- \_ Kette \_ mit Ausnahme von \_ root**</dt></span><span class="sxs-lookup"><span data-stu-id="db64c-132"><dt>**CAPICOM\_CERTIFICATE\_INCLUDE\_CHAIN\_EXCEPT\_ROOT**</dt></span></span> </dl> | <span data-ttu-id="db64c-133">Speichert alle Zertifikate in der Kette mit Ausnahme der Stamm Entität.</span><span class="sxs-lookup"><span data-stu-id="db64c-133">Saves all certificates in the chain with the exception of the root entity</span></span><br/> |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_WHOLE_CHAIN"></span><span id="capicom_certificate_include_whole_chain"></span><dl> <span data-ttu-id="db64c-134"><dt>**CAPICOM- \_ Zertifikat \_ einschließlich \_ ganzer \_ Kette**</dt></span><span class="sxs-lookup"><span data-stu-id="db64c-134"><dt>**CAPICOM\_CERTIFICATE\_INCLUDE\_WHOLE\_CHAIN**</dt></span></span> </dl>                    | <span data-ttu-id="db64c-135">Speichert die komplette Zertifikatskette.</span><span class="sxs-lookup"><span data-stu-id="db64c-135">Saves the complete certificate chain</span></span><br/>                                      |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_END_ENTITY_ONLY"></span><span id="capicom_certificate_include_end_entity_only"></span><dl> <span data-ttu-id="db64c-136"><dt>**CAPICOM- \_ Zertifikat \_ schließt \_ nur End- \_ Entität \_ ein.**</dt></span><span class="sxs-lookup"><span data-stu-id="db64c-136"><dt>**CAPICOM\_CERTIFICATE\_INCLUDE\_END\_ENTITY\_ONLY**</dt></span></span> </dl>       | <span data-ttu-id="db64c-137">Speichert nur das Endentitäts Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="db64c-137">Saves only the end entity certificate</span></span><br/>                                     |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db64c-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="db64c-138">Return value</span></span>

<span data-ttu-id="db64c-139">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="db64c-139">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="db64c-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="db64c-140">Remarks</span></span>

<span data-ttu-id="db64c-141">Diese Methode löst CAPICOM \_ E \_ nicht \_ zulässig aus, wenn eine Skripterstellung aus einer webbasierten Anwendung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="db64c-141">This method raises CAPICOM\_E\_NOT\_ALLOWED when it is scripted from a web-based application.</span></span>

## <a name="requirements"></a><span data-ttu-id="db64c-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="db64c-142">Requirements</span></span>



| <span data-ttu-id="db64c-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="db64c-143">Requirement</span></span> | <span data-ttu-id="db64c-144">Wert</span><span class="sxs-lookup"><span data-stu-id="db64c-144">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="db64c-145">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="db64c-145">End of client support</span></span><br/> | <span data-ttu-id="db64c-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="db64c-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="db64c-147">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="db64c-147">End of server support</span></span><br/> | <span data-ttu-id="db64c-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="db64c-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="db64c-149">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="db64c-149">Redistributable</span></span><br/>       | <span data-ttu-id="db64c-150">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="db64c-150">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="db64c-151">DLL</span><span class="sxs-lookup"><span data-stu-id="db64c-151">DLL</span></span><br/>                   | <dl> <span data-ttu-id="db64c-152"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db64c-152"><dt>Capicom.dll</dt></span></span> </dl> |



 

 

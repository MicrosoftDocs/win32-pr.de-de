---
description: Ruft Informationen aus dem Zertifikat ab.
ms.assetid: 57f1c6f9-f06d-4ac7-9070-2a2e6afe93d2
title: 'ICertificate2:: GetInfo-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.GetInfo
- ICertificate2.GetInfo
- ICertificate.GetInfo
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 41b3cb6cde796f64ee3a5953ed848d105a10bc5e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373653"
---
# <a name="icertificate2getinfo-method"></a><span data-ttu-id="717ea-103">ICertificate2:: GetInfo-Methode</span><span class="sxs-lookup"><span data-stu-id="717ea-103">ICertificate2::GetInfo method</span></span>

<span data-ttu-id="717ea-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="717ea-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="717ea-105">Verwenden Sie stattdessen die [**X509Certificate2-Klasse**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="717ea-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="717ea-106">Die **GetInfo** -Methode ruft Informationen aus dem [*Zertifikat*](../secgloss/c-gly.md)ab.</span><span class="sxs-lookup"><span data-stu-id="717ea-106">The **GetInfo** method retrieves information from the [*certificate*](../secgloss/c-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="717ea-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="717ea-107">Syntax</span></span>


```VB
Certificate.GetInfo( _
  ByVal InfoType _
)
```



## <a name="parameters"></a><span data-ttu-id="717ea-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="717ea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="717ea-109">*InfoType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="717ea-109">*InfoType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="717ea-110">Ein Wert der [**CAPICOM \_ CERT \_ Info \_ Type**](capicom-cert-info-type.md) -Enumeration, der angibt, welcher Datentyp aus dem Zertifikat abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="717ea-110">A value of the [**CAPICOM\_CERT\_INFO\_TYPE**](capicom-cert-info-type.md) enumeration that specifies what type of data is retrieved from the certificate.</span></span> <span data-ttu-id="717ea-111">In der folgenden Tabelle sind die möglichen Werte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="717ea-111">The following table shows the possible values.</span></span>



| <span data-ttu-id="717ea-112">Wert</span><span class="sxs-lookup"><span data-stu-id="717ea-112">Value</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="717ea-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="717ea-113">Meaning</span></span>                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERT_INFO_SUBJECT_SIMPLE_NAME"></span><span id="capicom_cert_info_subject_simple_name"></span><dl> <span data-ttu-id="717ea-114"><dt>**CAPICOM \_ CERT \_ Info \_ Subject \_ Simple \_ Name**</dt></span><span class="sxs-lookup"><span data-stu-id="717ea-114"><dt>**CAPICOM\_CERT\_INFO\_SUBJECT\_SIMPLE\_NAME**</dt></span></span> </dl> | <span data-ttu-id="717ea-115">Gibt den anzeigen amen des Zertifikats Antragstellers zurück.</span><span class="sxs-lookup"><span data-stu-id="717ea-115">Returns the display name from the certificate subject.</span></span><br/>                            |
| <span id="CAPICOM_CERT_INFO_ISSUER_SIMPLE_NAME"></span><span id="capicom_cert_info_issuer_simple_name"></span><dl> <span data-ttu-id="717ea-116"><dt>**Name der von CAPICOM \_ CERT \_ Info \_ Aussteller \_ einfacher \_**</dt></span><span class="sxs-lookup"><span data-stu-id="717ea-116"><dt>**CAPICOM\_CERT\_INFO\_ISSUER\_SIMPLE\_NAME**</dt></span></span> </dl>    | <span data-ttu-id="717ea-117">Gibt den anzeigen amen des Zertifikats Ausstellers zurück.</span><span class="sxs-lookup"><span data-stu-id="717ea-117">Returns the display name of the issuer of the certificate.</span></span><br/>                        |
| <span id="CAPICOM_CERT_INFO_SUBJECT_EMAIL_NAME"></span><span id="capicom_cert_info_subject_email_name"></span><dl> <span data-ttu-id="717ea-118"><dt>**Name der "CAPICOM \_ CERT \_ Info \_ Subject \_ Email \_ "**</dt></span><span class="sxs-lookup"><span data-stu-id="717ea-118"><dt>**CAPICOM\_CERT\_INFO\_SUBJECT\_EMAIL\_NAME**</dt></span></span> </dl>    | <span data-ttu-id="717ea-119">Gibt die e-Mail-Adresse des Zertifikat Antragstellers zurück.</span><span class="sxs-lookup"><span data-stu-id="717ea-119">Returns the email address of the certificate subject.</span></span><br/>                             |
| <span id="CAPICOM_CERT_INFO_ISSUER_EMAIL_NAME"></span><span id="capicom_cert_info_issuer_email_name"></span><dl> <span data-ttu-id="717ea-120"><dt>**Name der \_ \_ \_ Aussteller \_ -e-Mail \_ des CAPICOM-Zertifikats**</dt></span><span class="sxs-lookup"><span data-stu-id="717ea-120"><dt>**CAPICOM\_CERT\_INFO\_ISSUER\_EMAIL\_NAME**</dt></span></span> </dl>       | <span data-ttu-id="717ea-121">Gibt die e-Mail-Adresse des Zertifikats Ausstellers zurück.</span><span class="sxs-lookup"><span data-stu-id="717ea-121">Returns the email address of the issuer of the certificate.</span></span><br/>                       |
| <span id="CAPICOM_CERT_INFO_SUBJECT_UPN"></span><span id="capicom_cert_info_subject_upn"></span><dl> <span data-ttu-id="717ea-122"><dt>**Antragsteller \_ - \_ \_ \_ UPN für CAPICOM CERT Info**</dt></span><span class="sxs-lookup"><span data-stu-id="717ea-122"><dt>**CAPICOM\_CERT\_INFO\_SUBJECT\_UPN**</dt></span></span> </dl>                          | <span data-ttu-id="717ea-123">Gibt den UPN des Zertifikat Antragstellers zurück.</span><span class="sxs-lookup"><span data-stu-id="717ea-123">Returns the UPN of the certificate subject.</span></span> <span data-ttu-id="717ea-124">Eingeführt in CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="717ea-124">Introduced in CAPICOM 2.0.</span></span><br/>            |
| <span id="CAPICOM_CERT_INFO_ISSUER_UPN"></span><span id="capicom_cert_info_issuer_upn"></span><dl> <span data-ttu-id="717ea-125"><dt>**-UPN des CAPICOM \_ CERT \_ Info- \_ Ausstellers \_**</dt></span><span class="sxs-lookup"><span data-stu-id="717ea-125"><dt>**CAPICOM\_CERT\_INFO\_ISSUER\_UPN**</dt></span></span> </dl>                             | <span data-ttu-id="717ea-126">Gibt den UPN des Zertifikats Ausstellers zurück.</span><span class="sxs-lookup"><span data-stu-id="717ea-126">Returns the UPN of the issuer of the certificate.</span></span> <span data-ttu-id="717ea-127">Eingeführt in CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="717ea-127">Introduced in CAPICOM 2.0.</span></span><br/>      |
| <span id="CAPICOM_CERT_INFO_SUBJECT_DNS_NAME"></span><span id="capicom_cert_info_subject_dns_name"></span><dl> <span data-ttu-id="717ea-128"><dt>**"CAPICOM \_ CERT \_ Info \_ Subject \_ DNS \_ Name"**</dt></span><span class="sxs-lookup"><span data-stu-id="717ea-128"><dt>**CAPICOM\_CERT\_INFO\_SUBJECT\_DNS\_NAME**</dt></span></span> </dl>          | <span data-ttu-id="717ea-129">Gibt den DNS-Namen des Zertifikat Antragstellers zurück.</span><span class="sxs-lookup"><span data-stu-id="717ea-129">Returns the DNS name of the certificate subject.</span></span> <span data-ttu-id="717ea-130">Eingeführt in CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="717ea-130">Introduced in CAPICOM 2.0.</span></span><br/>       |
| <span id="CAPICOM_CERT_INFO_ISSUER_DNS_NAME"></span><span id="capicom_cert_info_issuer_dns_name"></span><dl> <span data-ttu-id="717ea-131"><dt>**Name des CAPICOM \_ CERT \_ Info-Aussteller- \_ \_ DNS \_**</dt></span><span class="sxs-lookup"><span data-stu-id="717ea-131"><dt>**CAPICOM\_CERT\_INFO\_ISSUER\_DNS\_NAME**</dt></span></span> </dl>             | <span data-ttu-id="717ea-132">Gibt den DNS-Namen des Zertifikats Ausstellers zurück.</span><span class="sxs-lookup"><span data-stu-id="717ea-132">Returns the DNS name of the issuer of the certificate.</span></span> <span data-ttu-id="717ea-133">Eingeführt in CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="717ea-133">Introduced in CAPICOM 2.0.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="717ea-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="717ea-134">Return value</span></span>

<span data-ttu-id="717ea-135">Eine Zeichenfolge, die die angeforderten Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="717ea-135">A string that contains the requested information.</span></span>

## <a name="requirements"></a><span data-ttu-id="717ea-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="717ea-136">Requirements</span></span>



| <span data-ttu-id="717ea-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="717ea-137">Requirement</span></span> | <span data-ttu-id="717ea-138">Wert</span><span class="sxs-lookup"><span data-stu-id="717ea-138">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="717ea-139">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="717ea-139">End of client support</span></span><br/> | <span data-ttu-id="717ea-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="717ea-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="717ea-141">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="717ea-141">End of server support</span></span><br/> | <span data-ttu-id="717ea-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="717ea-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="717ea-143">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="717ea-143">Redistributable</span></span><br/>       | <span data-ttu-id="717ea-144">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="717ea-144">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="717ea-145">DLL</span><span class="sxs-lookup"><span data-stu-id="717ea-145">DLL</span></span><br/>                   | <dl> <span data-ttu-id="717ea-146"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="717ea-146"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="717ea-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="717ea-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="717ea-148">Kryptografieobjekte</span><span class="sxs-lookup"><span data-stu-id="717ea-148">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="717ea-149">**Stellt**</span><span class="sxs-lookup"><span data-stu-id="717ea-149">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 

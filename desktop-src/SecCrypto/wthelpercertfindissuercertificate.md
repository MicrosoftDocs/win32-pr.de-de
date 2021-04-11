---
description: Sucht ein Aussteller Zertifikat aus den angegebenen Zertifikat speichern, das mit dem angegebenen Antragsteller Zertifikat übereinstimmt.
ms.assetid: c724f602-fc73-4857-941f-0f22a9e472d1
title: Wthelpercertfinrevoercertificate-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WTHelperCertFindIssuerCertificate
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: 99135ac22509b288726732ca4a16248b304f294b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216197"
---
# <a name="wthelpercertfindissuercertificate-function"></a><span data-ttu-id="8c570-103">Wthelpercertfinrevoercertificate-Funktion</span><span class="sxs-lookup"><span data-stu-id="8c570-103">WTHelperCertFindIssuerCertificate function</span></span>

<span data-ttu-id="8c570-104">\[Die Funktion " **wthelpercertfinrevoercertificate** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="8c570-104">\[The **WTHelperCertFindIssuerCertificate** function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8c570-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="8c570-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="8c570-106">Die **wthelpercertfinrevoercertificate** -Funktion sucht ein Aussteller Zertifikat aus den angegebenen Zertifikat speichern, das mit dem angegebenen Antragsteller Zertifikat übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="8c570-106">The **WTHelperCertFindIssuerCertificate** function finds an issuer certificate from the specified certificate stores that matches the specified subject certificate.</span></span>

> [!Note]  
> <span data-ttu-id="8c570-107">Diese Funktion verfügt über keine zugeordnete Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="8c570-107">This function has no associated import library.</span></span> <span data-ttu-id="8c570-108">Sie müssen die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Wintrust.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="8c570-108">You must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Wintrust.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="8c570-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c570-109">Syntax</span></span>


```C++
PCCERT_CONTEXT WINAPI WTHelperCertFindIssuerCertificate(
  _In_      PCCERT_CONTEXT pChildContext,
  _In_      DWORD          chStores,
  _In_      HCERTSTORE     *pahStores,
  _In_      FILETIME       *psftVerifyAsOf,
  _In_      DWORD          dwEncoding,
  _Out_opt_ DWORD          *pdwConfidence,
  _Out_     DWORD          *dwError
);
```



## <a name="parameters"></a><span data-ttu-id="8c570-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c570-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c570-111">*pchildcontext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8c570-111">*pChildContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c570-112">Das Antragsteller Zertifikat, für das ein entsprechendes Aussteller Zertifikat gefunden werden soll.</span><span class="sxs-lookup"><span data-stu-id="8c570-112">The subject certificate for which to find a matching issuer certificate.</span></span>

</dd> <dt>

<span data-ttu-id="8c570-113">*chstores* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8c570-113">*chStores* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c570-114">Die Anzahl der Elemente *im Array von* Arrays.</span><span class="sxs-lookup"><span data-stu-id="8c570-114">The number of elements in the *pahStores* array.</span></span>

</dd> <dt>

<span data-ttu-id="8c570-115">*Filialen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8c570-115">*pahStores* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c570-116">Ein Array von Zertifikat speichern, in denen gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="8c570-116">An array of certificate stores in which to search.</span></span>

</dd> <dt>

<span data-ttu-id="8c570-117">*psftverif-of* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8c570-117">*psftVerifyAsOf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c570-118">Der Zeitpunkt der Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="8c570-118">The time of verification.</span></span>

</dd> <dt>

<span data-ttu-id="8c570-119">*dwencoding* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8c570-119">*dwEncoding* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c570-120">Ein **DWORD** -Wert, der die Codierungs Typen des Zertifikats angibt, das überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="8c570-120">A **DWORD** value that specifies the encoding types of the certificate to check.</span></span> <span data-ttu-id="8c570-121">Informationen zu möglichen Codierungs Typen finden Sie unter [Zertifikat-und Nachrichten Codierungs Typen](certificate-and-message-encoding-types.md).</span><span class="sxs-lookup"><span data-stu-id="8c570-121">For information about possible encoding types, see [Certificate and Message Encoding Types](certificate-and-message-encoding-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c570-122">*pdwconfidence* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="8c570-122">*pdwConfidence* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8c570-123">Dieser Parameter kann eine bitweise Kombination von 0 (null) oder mehr der folgenden Konfidenz Werte sein.</span><span class="sxs-lookup"><span data-stu-id="8c570-123">This parameter can be a bitwise combination of zero or more of the following confidence values.</span></span>



| <span data-ttu-id="8c570-124">Wert</span><span class="sxs-lookup"><span data-stu-id="8c570-124">Value</span></span>                                                                                                                                                                                                                                                                 | <span data-ttu-id="8c570-125">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="8c570-125">Meaning</span></span>                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="CERT_CONFIDENCE_SIG"></span><span id="cert_confidence_sig"></span><dl> <span data-ttu-id="8c570-126"><dt>**Zertifikat \_ Zuverlässigkeit \_ sig**</dt> <dt> 0x10000000</dt></span><span class="sxs-lookup"><span data-stu-id="8c570-126"><dt>**CERT\_CONFIDENCE\_SIG**</dt> <dt> 0x10000000</dt></span></span> </dl>                     | <span data-ttu-id="8c570-127">Die Signatur des Zertifikats ist gültig.</span><span class="sxs-lookup"><span data-stu-id="8c570-127">The signature of the certificate is valid.</span></span><br/>                                           |
| <span id="CERT_CONFIDENCE_TIME"></span><span id="cert_confidence_time"></span><dl> <span data-ttu-id="8c570-128"><dt>**Zertifikat \_ Vertrauens \_ Zeit**</dt> <dt> 0x01000000</dt></span><span class="sxs-lookup"><span data-stu-id="8c570-128"><dt>**CERT\_CONFIDENCE\_TIME**</dt> <dt> 0x01000000</dt></span></span> </dl>                  | <span data-ttu-id="8c570-129">Die Zeit des Zertifikat Ausstellers ist gültig.</span><span class="sxs-lookup"><span data-stu-id="8c570-129">The time of the certificate issuer is valid.</span></span><br/>                                         |
| <span id="_CERT_CONFIDENCE_TIMENEST"></span><span id="_cert_confidence_timenest"></span><dl> <span data-ttu-id="8c570-130"><dt> **CERT \_ Confidence \_ timenest**</dt> <dt>0x00100000</dt></span><span class="sxs-lookup"><span data-stu-id="8c570-130"><dt> **CERT\_CONFIDENCE\_TIMENEST**</dt> <dt>0x00100000</dt></span></span> </dl>    | <span data-ttu-id="8c570-131">Die Uhrzeit des Zertifikats ist gültig.</span><span class="sxs-lookup"><span data-stu-id="8c570-131">The time of the certificate is valid.</span></span><br/>                                                |
| <span id="_CERT_CONFIDENCE_AUTHIDEXT"></span><span id="_cert_confidence_authidext"></span><dl> <span data-ttu-id="8c570-132"><dt> **CERT \_ Confidence \_ authidext**</dt> <dt>0x00010000 bis</dt></span><span class="sxs-lookup"><span data-stu-id="8c570-132"><dt> **CERT\_CONFIDENCE\_AUTHIDEXT**</dt> <dt>0x00010000</dt></span></span> </dl> | <span data-ttu-id="8c570-133">Die Autoritäts-ID-Erweiterung ist gültig.</span><span class="sxs-lookup"><span data-stu-id="8c570-133">The authority ID extension is valid.</span></span><br/>                                                 |
| <span id="_CERT_CONFIDENCE_HYGIENE"></span><span id="_cert_confidence_hygiene"></span><dl> <span data-ttu-id="8c570-134"><dt> **Zertifikat \_ Vertrauens \_ Pflege**</dt> <dt>0x00001000</dt></span><span class="sxs-lookup"><span data-stu-id="8c570-134"><dt> **CERT\_CONFIDENCE\_HYGIENE**</dt> <dt>0x00001000</dt></span></span> </dl>       | <span data-ttu-id="8c570-135">Die Signatur der Zertifikat-und Autoritäts-ID-Erweiterung ist mindestens gültig.</span><span class="sxs-lookup"><span data-stu-id="8c570-135">At a minimum, the signature of the certificate and authority ID extension are valid.</span></span><br/> |
| <span id="_CERT_CONFIDENCE_HIGHEST"></span><span id="_cert_confidence_highest"></span><dl> <span data-ttu-id="8c570-136"><dt> **CERT \_ Confidence \_ höchste**</dt> <dt>0x11111000</dt></span><span class="sxs-lookup"><span data-stu-id="8c570-136"><dt> **CERT\_CONFIDENCE\_HIGHEST**</dt> <dt>0x11111000</dt></span></span> </dl>       | <span data-ttu-id="8c570-137">Eine Kombination aus allen anderen Vertrauens Werten.</span><span class="sxs-lookup"><span data-stu-id="8c570-137">A combination of all of the other confidence values.</span></span><br/>                                 |



 

</dd> <dt>

<span data-ttu-id="8c570-138">*dwError* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8c570-138">*dwError* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c570-139">Ein Zeiger auf eine **DWORD** -Variable, die ggf. den Fehlerwert für dieses Zertifikat enthält.</span><span class="sxs-lookup"><span data-stu-id="8c570-139">A pointer to a **DWORD** variable that contains the error value for this certificate, if applicable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c570-140">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8c570-140">Return value</span></span>

<span data-ttu-id="8c570-141">Ein Aussteller Zertifikat, das mit dem vom *pchildcontext* -Parameter angegebenen Antragsteller Zertifikat übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="8c570-141">An issuer certificate that matches the subject certificate specified by the *pChildContext* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c570-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8c570-142">Remarks</span></span>

<span data-ttu-id="8c570-143">Die folgenden Anforderungen müssen erfüllt sein, damit ein entsprechendes Aussteller Zertifikat gefunden werden kann:</span><span class="sxs-lookup"><span data-stu-id="8c570-143">To successfully find a matching issuer certificate, the following requirements must be met:</span></span>

-   <span data-ttu-id="8c570-144">Die Signatur des vom *pchildcontext* -Parameter angegebenen betreffzertifikats muss gültig sein.</span><span class="sxs-lookup"><span data-stu-id="8c570-144">The signature of the subject certificate specified by the *pChildContext* parameter must be valid.</span></span>
-   <span data-ttu-id="8c570-145">Das **rgextension** -Element des **pcertinfo** -Members des *pchildcontext* -Parameters muss eine Zertifikat Zertifizierungsstellen- [**Schlüssel-ID- \_ \_ \_ \_ Informations**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_authority_key_id_info) Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="8c570-145">The **rgExtension** member of the **pCertInfo** member of the *pChildContext* parameter must contain a [**CERT\_AUTHORITY\_KEY\_ID\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_authority_key_id_info) structure.</span></span> <span data-ttu-id="8c570-146">Die Member **CertIssuer** und **certserialmember** dieser Struktur Stimmen stark mit den entsprechenden Membern für das Aussteller Zertifikat überein.</span><span class="sxs-lookup"><span data-stu-id="8c570-146">The **CertIssuer** and **CertSerialMember** members of this structure much match the corresponding members for the issuer certificate.</span></span>
-   <span data-ttu-id="8c570-147">Der Wert des *psftverisyasof* -Parameters muss innerhalb des Gültigkeits Zeitraums des Antragsteller Zertifikats liegen.</span><span class="sxs-lookup"><span data-stu-id="8c570-147">The value of the *psftVerifyAsOf* parameter must be within the period of validity of the subject certificate.</span></span>
-   <span data-ttu-id="8c570-148">Der Gültigkeits Zeitraum des Antragsteller Zertifikats muss innerhalb des Gültigkeits Zeitraums des Aussteller Zertifikats liegen.</span><span class="sxs-lookup"><span data-stu-id="8c570-148">The period of validity of the subject certificate must be within the period of validity of the issuer certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c570-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8c570-149">Requirements</span></span>



| <span data-ttu-id="8c570-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8c570-150">Requirement</span></span> | <span data-ttu-id="8c570-151">Wert</span><span class="sxs-lookup"><span data-stu-id="8c570-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c570-152">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8c570-152">Minimum supported client</span></span><br/> | <span data-ttu-id="8c570-153">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8c570-153">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="8c570-154">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8c570-154">Minimum supported server</span></span><br/> | <span data-ttu-id="8c570-155">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8c570-155">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8c570-156">DLL</span><span class="sxs-lookup"><span data-stu-id="8c570-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c570-157"><dt>Wintrust.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c570-157"><dt>Wintrust.dll</dt></span></span> </dl> |



 

 

---
description: Gibt ein Signaturzertifikat an (wird auch als Registrierungs-Agent-Zertifikat bezeichnet).
ms.assetid: db2437a9-46f6-48c3-9630-82ec556df645
title: 'Iscrdenr:: setsigningcertificate-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setSigningCertificate
- SCrdEnr.setSigningCertificate
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: dd00ba19872cb0ba2b21981c79e8f7be03aa4937
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350172"
---
# <a name="iscrdenrsetsigningcertificate-method"></a><span data-ttu-id="59225-103">Iscrdenr:: setsigningcertificate-Methode</span><span class="sxs-lookup"><span data-stu-id="59225-103">ISCrdEnr::setSigningCertificate method</span></span>

<span data-ttu-id="59225-104">Mit der **setsigningcertificate** -Methode wird ein Signaturzertifikat (auch als Registrierungs- *Agent-Zertifikat* bezeichnet) angegeben.</span><span class="sxs-lookup"><span data-stu-id="59225-104">The **setSigningCertificate** method specifies a signing certificate (also known as the *enrollment agent certificate*).</span></span>

<span data-ttu-id="59225-105">Vor der Registrierung im Namen von Benutzern müssen Sie ein Signaturzertifikat auswählen oder festlegen.</span><span class="sxs-lookup"><span data-stu-id="59225-105">Before enrolling on behalf of users, you must select or set a signing certificate.</span></span> <span data-ttu-id="59225-106">Der diesem Signaturzertifikat zugeordnete [*private Schlüssel*](../secgloss/p-gly.md) wird verwendet, um eine PKCS 7-Anforderung zu signieren \# .</span><span class="sxs-lookup"><span data-stu-id="59225-106">The [*private key*](../secgloss/p-gly.md) associated with this signing certificate is used to sign a PKCS \#7 request.</span></span> <span data-ttu-id="59225-107">Die PKCS \# 7 enthält wiederum die PKCS 10-Anforderung des Benutzers \# (die mit dem privaten Schlüssel des Benutzers signiert ist).</span><span class="sxs-lookup"><span data-stu-id="59225-107">The PKCS \#7, in turn, contains the user's PKCS \#10 request (which is signed with the user's private key).</span></span>

## <a name="syntax"></a><span data-ttu-id="59225-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="59225-108">Syntax</span></span>


```C++
HRESULT setSigningCertificate(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName
);
```


```VB

SCrdEnr.setSigningCertificate( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName _
)
```





## <a name="parameters"></a><span data-ttu-id="59225-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="59225-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59225-110">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59225-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59225-111">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="59225-111">Reserved for future use.</span></span> <span data-ttu-id="59225-112">Legen Sie diesen Wert auf NULL fest.</span><span class="sxs-lookup"><span data-stu-id="59225-112">Set this value to zero.</span></span>

</dd> <dt>

<span data-ttu-id="59225-113">*bstraucerttemplatename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59225-113">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59225-114">Der Name der Zertifikat Vorlage für das Signaturzertifikat.</span><span class="sxs-lookup"><span data-stu-id="59225-114">Name of the certificate template for the signing certificate.</span></span> <span data-ttu-id="59225-115">Sie können den Wert "anmelmentagent" verwenden, wenn Sie ein Registrierungs Agent-Zertifikat erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="59225-115">You can use the value "EnrollmentAgent" if you have obtained an EnrollmentAgent certificate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59225-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="59225-116">Return value</span></span>

### <a name="vb"></a><span data-ttu-id="59225-117">VB</span><span class="sxs-lookup"><span data-stu-id="59225-117">VB</span></span>

<span data-ttu-id="59225-118">Wenn die Methode erfolgreich ausgeführt wird, gibt die Methode S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="59225-118">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="59225-119">Wenn die Methode fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="59225-119">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="59225-120">Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="59225-120">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="59225-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="59225-121">Remarks</span></span>

<span data-ttu-id="59225-122">Vor der Registrierung im Namen eines Benutzers müssen Sie zuerst ein Signaturzertifikat abrufen.</span><span class="sxs-lookup"><span data-stu-id="59225-122">Before enrolling on behalf of a user, you must first obtain a signing certificate.</span></span> <span data-ttu-id="59225-123">Sie können ein Signaturzertifikat mit dem Zertifikat-Manager-MMC-Snap-in abrufen.</span><span class="sxs-lookup"><span data-stu-id="59225-123">You can obtain a signing certificate by using the Certificate Manager MMC snap-in.</span></span> <span data-ttu-id="59225-124">Die **setsigningcertificate** -Methode erhält nicht das Signaturzertifikat, sondern informiert die Smartcard-Registrierungs Steuerung, die zuvor das zu verwendende Signaturzertifikat abgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="59225-124">The **setSigningCertificate** method does not obtain the signing certificate but informs the Smart Card Enrollment Control which previously obtained signing certificate to use.</span></span> <span data-ttu-id="59225-125">Die **setsigningcertificate** -Methode durchsucht den "My"-Speicher des Aufrufers nach dem neuesten Signaturzertifikat, das der von *bstrincerttemplatename* angegebenen Zertifikat Vorlage entspricht.</span><span class="sxs-lookup"><span data-stu-id="59225-125">The **setSigningCertificate** method searches the caller's "My" store for the most recent signing certificate corresponding to the certificate template specified by *bstrCertTemplateName*.</span></span>

<span data-ttu-id="59225-126">Eine Alternative zu **setsigningcertificate** ist **iscrdenr:: setsigningcertificate**.</span><span class="sxs-lookup"><span data-stu-id="59225-126">An alternative to **setSigningCertificate** is **ISCrdEnr::setSigningCertificate**.</span></span>

<span data-ttu-id="59225-127">Nachdem ein Signaturzertifikat festgelegt wurde, kann der zugehörige Name durch Aufrufen von [**iscrdenr:: getsigningcertifikatename**](iscrdenr-getsigningcertificatename.md)abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="59225-127">After a signing certificate is set, its name can be retrieved by calling [**ISCrdEnr::getSigningCertificateName**](iscrdenr-getsigningcertificatename.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="59225-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="59225-128">Requirements</span></span>



| <span data-ttu-id="59225-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="59225-129">Requirement</span></span> | <span data-ttu-id="59225-130">Wert</span><span class="sxs-lookup"><span data-stu-id="59225-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="59225-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="59225-131">Minimum supported client</span></span><br/> | <span data-ttu-id="59225-132">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="59225-132">None supported</span></span><br/>                                                               |
| <span data-ttu-id="59225-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="59225-133">Minimum supported server</span></span><br/> | <span data-ttu-id="59225-134">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="59225-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="59225-135">DLL</span><span class="sxs-lookup"><span data-stu-id="59225-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59225-136"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59225-136"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="59225-137">IID</span><span class="sxs-lookup"><span data-stu-id="59225-137">IID</span></span><br/>                      | <span data-ttu-id="59225-138">IID \_ iscrdenr ist definiert als 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="59225-138">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="59225-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="59225-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59225-140">**Iscrdenr**</span><span class="sxs-lookup"><span data-stu-id="59225-140">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="59225-141">**Iscrdenr:: getsigningcertificename**</span><span class="sxs-lookup"><span data-stu-id="59225-141">**ISCrdEnr::getSigningCertificateName**</span></span>](iscrdenr-getsigningcertificatename.md)
</dt> </dl>

 

 

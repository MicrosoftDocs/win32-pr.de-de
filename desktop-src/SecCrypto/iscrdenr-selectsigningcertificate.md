---
description: Zeigt das Dialogfeld Zertifikat auswählen an, in dem ein Signaturzertifikat (auch als Registrierungs-Agent-Zertifikat bezeichnet) ausgewählt werden kann.
ms.assetid: b8198f65-4ffb-4dfa-8286-e62ef483ab16
title: 'Iscrdenr:: selectsigningcertificate-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.selectSigningCertificate
- SCrdEnr.selectSigningCertificate
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: a4ef3be0ef16797597f57c12e90736ba50109601
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868207"
---
# <a name="iscrdenrselectsigningcertificate-method"></a><span data-ttu-id="417d8-103">Iscrdenr:: selectsigningcertificate-Methode</span><span class="sxs-lookup"><span data-stu-id="417d8-103">ISCrdEnr::selectSigningCertificate method</span></span>

<span data-ttu-id="417d8-104">Die **selectsigningcertificate** -Methode zeigt das Dialogfeld **Zertifikat auswählen** an, in dem ein Signaturzertifikat (auch als Registrierungs- *Agent-Zertifikat* bezeichnet) ausgewählt werden kann.</span><span class="sxs-lookup"><span data-stu-id="417d8-104">The **selectSigningCertificate** method displays a **Select Certificate** dialog box, allowing a signing certificate (also known as the *enrollment agent certificate*) to be selected.</span></span>

<span data-ttu-id="417d8-105">Vor der Registrierung im Namen von Benutzern müssen Sie ein Signaturzertifikat auswählen.</span><span class="sxs-lookup"><span data-stu-id="417d8-105">Before enrolling on behalf of users, you must select a signing certificate.</span></span> <span data-ttu-id="417d8-106">Der diesem Signaturzertifikat zugeordnete [*private Schlüssel*](../secgloss/p-gly.md) wird verwendet, um eine PKCS 7-Anforderung zu signieren \# .</span><span class="sxs-lookup"><span data-stu-id="417d8-106">The [*private key*](../secgloss/p-gly.md) associated with this signing certificate is used to sign a PKCS \#7 request.</span></span> <span data-ttu-id="417d8-107">Die PKCS \# 7 enthält wiederum die PKCS 10-Anforderung des Benutzers \# (die mit dem privaten Schlüssel des Benutzers signiert ist).</span><span class="sxs-lookup"><span data-stu-id="417d8-107">The PKCS \#7, in turn, contains the user's PKCS \#10 request (which is signed with the user's private key).</span></span>

## <a name="syntax"></a><span data-ttu-id="417d8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="417d8-108">Syntax</span></span>


```C++
HRESULT selectSigningCertificate(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName
);
```


```VB

SCrdEnr.selectSigningCertificate( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName _
)
```





## <a name="parameters"></a><span data-ttu-id="417d8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="417d8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="417d8-110">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="417d8-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="417d8-111">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="417d8-111">Reserved for future use.</span></span> <span data-ttu-id="417d8-112">Legen Sie diesen Wert auf NULL fest.</span><span class="sxs-lookup"><span data-stu-id="417d8-112">Set this value to zero.</span></span>

</dd> <dt>

<span data-ttu-id="417d8-113">*bstraucerttemplatename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="417d8-113">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="417d8-114">Eine Zeichenfolge, die den Namen der Zertifikat Vorlage für das Signaturzertifikat darstellt.</span><span class="sxs-lookup"><span data-stu-id="417d8-114">A string that represents the name of the certificate template for the signing certificate.</span></span> <span data-ttu-id="417d8-115">Sie können den Wert "anmelmentagent" verwenden, wenn Sie ein Registrierungs Agent-Zertifikat erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="417d8-115">You can use the value "EnrollmentAgent" if you have obtained an EnrollmentAgent certificate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="417d8-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="417d8-116">Return value</span></span>

### <a name="vb"></a><span data-ttu-id="417d8-117">VB</span><span class="sxs-lookup"><span data-stu-id="417d8-117">VB</span></span>

<span data-ttu-id="417d8-118">Wenn die Methode erfolgreich ausgeführt wird, gibt die Methode **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="417d8-118">If the method succeeds, the method returns **S\_OK**.</span></span>

<span data-ttu-id="417d8-119">Wenn die Methode fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="417d8-119">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="417d8-120">Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="417d8-120">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="417d8-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="417d8-121">Remarks</span></span>

<span data-ttu-id="417d8-122">Vor der Registrierung im Namen eines Benutzers müssen Sie zuerst ein Signaturzertifikat abrufen.</span><span class="sxs-lookup"><span data-stu-id="417d8-122">Before enrolling on behalf of a user, you must first obtain a signing certificate.</span></span> <span data-ttu-id="417d8-123">Sie können ein Signaturzertifikat mit dem Zertifikat-Manager-MMC-Snap-in abrufen.</span><span class="sxs-lookup"><span data-stu-id="417d8-123">You can obtain a signing certificate by using the Certificate Manager MMC snap-in.</span></span> <span data-ttu-id="417d8-124">Von der **selectsigningcertificate** -Methode wird das Signaturzertifikat nicht abgerufen, aber es wird ein Dialogfeld mit zuvor abzurufenden Signatur Zertifikaten angezeigt, sodass Sie auswählen können, welches Zertifikat zum Signieren der Anforderungen zum Registrieren im Auftrag verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="417d8-124">The **selectSigningCertificate** method does not obtain the signing certificate but displays a dialog box of previously obtained signing certificates, allowing you to choose which certificate will be used to sign the enroll-on-behalf requests.</span></span>

<span data-ttu-id="417d8-125">Eine Alternative zu **selectsigningcertificate** ist [**iscrdenr:: setsigningcertificate**](iscrdenr-setsigningcertificate.md).</span><span class="sxs-lookup"><span data-stu-id="417d8-125">An alternative to **selectSigningCertificate** is [**ISCrdEnr::setSigningCertificate**](iscrdenr-setsigningcertificate.md).</span></span>

<span data-ttu-id="417d8-126">Nachdem ein Signaturzertifikat ausgewählt wurde, kann der zugehörige Name durch Aufrufen von [**iscrdenr:: getsigningcertifikatename**](iscrdenr-getsigningcertificatename.md)abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="417d8-126">After a signing certificate is selected, its name can be retrieved by calling [**ISCrdEnr::getSigningCertificateName**](iscrdenr-getsigningcertificatename.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="417d8-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="417d8-127">Requirements</span></span>



| <span data-ttu-id="417d8-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="417d8-128">Requirement</span></span> | <span data-ttu-id="417d8-129">Wert</span><span class="sxs-lookup"><span data-stu-id="417d8-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="417d8-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="417d8-130">Minimum supported client</span></span><br/> | <span data-ttu-id="417d8-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="417d8-131">None supported</span></span><br/>                                                               |
| <span data-ttu-id="417d8-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="417d8-132">Minimum supported server</span></span><br/> | <span data-ttu-id="417d8-133">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="417d8-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="417d8-134">DLL</span><span class="sxs-lookup"><span data-stu-id="417d8-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="417d8-135"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="417d8-135"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="417d8-136">IID</span><span class="sxs-lookup"><span data-stu-id="417d8-136">IID</span></span><br/>                      | <span data-ttu-id="417d8-137">IID \_ iscrdenr ist definiert als 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="417d8-137">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="417d8-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="417d8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="417d8-139">**Iscrdenr**</span><span class="sxs-lookup"><span data-stu-id="417d8-139">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="417d8-140">**Iscrdenr:: getsigningcertificename**</span><span class="sxs-lookup"><span data-stu-id="417d8-140">**ISCrdEnr::getSigningCertificateName**</span></span>](iscrdenr-getsigningcertificatename.md)
</dt> </dl>

 

 

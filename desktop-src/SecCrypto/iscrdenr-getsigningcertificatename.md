---
description: Ruft den Antragsteller Namen aus dem Signaturzertifikat ab.
ms.assetid: e50b1e12-ec89-4d58-aa57-dc24aa2409ef
title: 'Iscrdenr:: getsigningcertifitorename-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getSigningCertificateName
- SCrdEnr.getSigningCertificateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 8d9a8a84067e82a18e5066721f3e7f39d075c339
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393693"
---
# <a name="iscrdenrgetsigningcertificatename-method"></a><span data-ttu-id="fe30d-103">Iscrdenr:: getsigningcertifitorename-Methode</span><span class="sxs-lookup"><span data-stu-id="fe30d-103">ISCrdEnr::getSigningCertificateName method</span></span>

<span data-ttu-id="fe30d-104">Die **getsigningcertifikatename** -Methode ruft den Antragsteller Namen aus dem Signaturzertifikat ab.</span><span class="sxs-lookup"><span data-stu-id="fe30d-104">The **getSigningCertificateName** method retrieves the subject name from the signing certificate.</span></span>

<span data-ttu-id="fe30d-105">Diese Methode kann auch verwendet werden, um das Zertifikat in einem Dialogfeld anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="fe30d-105">This method can also be used to display the certificate in a dialog box.</span></span> <span data-ttu-id="fe30d-106">Diese Methode ruft die [*CryptoAPI*](../secgloss/c-gly.md) -Funktion [**certgetnamestring**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa)auf.</span><span class="sxs-lookup"><span data-stu-id="fe30d-106">This method calls the [*CryptoAPI*](../secgloss/c-gly.md) function [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa).</span></span>

## <a name="syntax"></a><span data-ttu-id="fe30d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe30d-107">Syntax</span></span>


```C++
HRESULT getSigningCertificateName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrSigningCertName
);
```


```VB

SCrdEnr.getSigningCertificateName( _
  ByVal dwFlags, _
  ByRef pbstrSigningCertName _
)
```





## <a name="parameters"></a><span data-ttu-id="fe30d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe30d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe30d-109">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe30d-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe30d-110">Ein-Wert, der bestimmt, ob das Zertifikat in einem Dialogfeld angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="fe30d-110">A value that determines whether the certificate is displayed in a dialog box.</span></span> <span data-ttu-id="fe30d-111">Wenn dieser Wert "SCard \_ ENROLL \_ No \_ Display \_ CERT (als 0x01 definiert)" lautet, wird das Signaturzertifikat nicht angezeigt. alle anderen Werte führen dazu, dass das Signaturzertifikat im Dialogfeld " **Zertifikat** " angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="fe30d-111">If this value is SCARD\_ENROLL\_NO\_DISPLAY\_CERT (defined as 0x01), the signing certificate is not displayed; any other values result in the signing certificate being displayed in the **Certificate** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="fe30d-112">*pbstrausigningcertname* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="fe30d-112">*pbstrSigningCertName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe30d-113">Ein Zeiger auf eine Zeichenfolge, die den Namen des Signatur Zertifikats zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="fe30d-113">A pointer to a string that returns the name of the signing certificate.</span></span> <span data-ttu-id="fe30d-114">Das Signaturzertifikat wird verwendet, um die [*Zertifikat Anforderung*](../secgloss/c-gly.md)zu signieren.</span><span class="sxs-lookup"><span data-stu-id="fe30d-114">The signing certificate will be used to sign the [*certificate request*](../secgloss/c-gly.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe30d-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fe30d-115">Return value</span></span>

### <a name="c"></a><span data-ttu-id="fe30d-116">C++</span><span class="sxs-lookup"><span data-stu-id="fe30d-116">C++</span></span>

<span data-ttu-id="fe30d-117">Wenn die Methode erfolgreich ausgeführt wird, gibt die Methode S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="fe30d-117">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="fe30d-118">Wenn die Methode fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="fe30d-118">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="fe30d-119">Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="fe30d-119">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="fe30d-120">VB</span><span class="sxs-lookup"><span data-stu-id="fe30d-120">VB</span></span>

<span data-ttu-id="fe30d-121">Eine Zeichenfolge, die den Namen des Signatur Zertifikats darstellt.</span><span class="sxs-lookup"><span data-stu-id="fe30d-121">A string that represents the name of the signing certificate.</span></span> <span data-ttu-id="fe30d-122">Das Signaturzertifikat wird verwendet, um die [*Zertifikat Anforderung*](../secgloss/c-gly.md)zu signieren.</span><span class="sxs-lookup"><span data-stu-id="fe30d-122">The signing certificate will be used to sign the [*certificate request*](../secgloss/c-gly.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fe30d-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fe30d-123">Remarks</span></span>

<span data-ttu-id="fe30d-124">Die **getsigningcertifikatename** -Methode gibt den Antragsteller Namen des Zertifikats, das Sie (oder ein anderer Administrator) ausgewählt haben, in einem vorherigen erfolgreichen [**iscrdenr:: selectsigningcertificate**](iscrdenr-selectsigningcertificate.md) -oder [**iscrdenr:: setsigningcertificate**](iscrdenr-setsigningcertificate.md)-Vorgang zurück.</span><span class="sxs-lookup"><span data-stu-id="fe30d-124">The **getSigningCertificateName** method returns the subject name of the certificate you (or another administrator) have selected in a previous successful call to [**ISCrdEnr::selectSigningCertificate**](iscrdenr-selectsigningcertificate.md) or [**ISCrdEnr::setSigningCertificate**](iscrdenr-setsigningcertificate.md).</span></span> <span data-ttu-id="fe30d-125">Diese Methode ruft die [**certgetnamestring**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa) -Funktion auf, um den Antragsteller Namen entsprechend der für den "CERT \_ Name \_ Simple \_ Display Type" \_ -Wert des *dwType* -Parameters von **certgetnamestring** beschriebenen Sequenz abzurufen.</span><span class="sxs-lookup"><span data-stu-id="fe30d-125">This method calls the [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa) function to retrieve the subject name according to the sequence described for the CERT\_NAME\_SIMPLE\_DISPLAY\_TYPE value of **CertGetNameString**'s *dwType* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe30d-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe30d-126">Requirements</span></span>



| <span data-ttu-id="fe30d-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fe30d-127">Requirement</span></span> | <span data-ttu-id="fe30d-128">Wert</span><span class="sxs-lookup"><span data-stu-id="fe30d-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe30d-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fe30d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="fe30d-130">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="fe30d-130">None supported</span></span><br/>                                                               |
| <span data-ttu-id="fe30d-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fe30d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="fe30d-132">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fe30d-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fe30d-133">DLL</span><span class="sxs-lookup"><span data-stu-id="fe30d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe30d-134"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe30d-134"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="fe30d-135">IID</span><span class="sxs-lookup"><span data-stu-id="fe30d-135">IID</span></span><br/>                      | <span data-ttu-id="fe30d-136">IID \_ iscrdenr ist definiert als 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="fe30d-136">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="fe30d-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fe30d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe30d-138">**Iscrdenr**</span><span class="sxs-lookup"><span data-stu-id="fe30d-138">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="fe30d-139">**Iscrdenr:: selectsigningcertificate**</span><span class="sxs-lookup"><span data-stu-id="fe30d-139">**ISCrdEnr::selectSigningCertificate**</span></span>](iscrdenr-selectsigningcertificate.md)
</dt> </dl>

 

 

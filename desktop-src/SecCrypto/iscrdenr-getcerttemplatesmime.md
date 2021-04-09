---
description: Wird verwendet, um zu bestimmen, ob eine Zertifikat Vorlage die \_ \_ \_ Verwendung der e-Mail- \_ Schutz Schlüssel für den szoid-PKIX
ms.assetid: 1f0512e0-68b6-4b79-84bd-614babb4151d
title: 'Iscrdenr:: getcerttemplatesmime-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCertTemplateSMIME
- SCrdEnr.getCertTemplateSMIME
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 4ed66af6a8a91855fbfc5a972a8bf00358314663
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867399"
---
# <a name="iscrdenrgetcerttemplatesmime-method"></a><span data-ttu-id="54edd-103">Iscrdenr:: getcerttemplatesmime-Methode</span><span class="sxs-lookup"><span data-stu-id="54edd-103">ISCrdEnr::getCertTemplateSMIME method</span></span>

<span data-ttu-id="54edd-104">Die **getcerttemplatesmime** -Methode wird verwendet, um zu bestimmen, ob eine Zertifikat Vorlage die \_ \_ \_ Verwendung des e-Mail-Schutzes für den szoomid PKIX KP- \_ Schlüssel enthält</span><span class="sxs-lookup"><span data-stu-id="54edd-104">The **getCertTemplateSMIME** method is used to determine whether a certificate template contains the szOID\_PKIX\_KP\_EMAIL\_PROTECTION key usage.</span></span>

<span data-ttu-id="54edd-105">Wenn diese Schlüssel Verwendung Teil der Zertifikat Vorlage ist, werden von der Zertifikat Vorlage [*sichere/Multipurpose Internet Mail Extensions*](../secgloss/s-gly.md) Vorgänge (S/MIME) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="54edd-105">If this key usage is part of the certificate template, the certificate template supports [*Secure/Multipurpose Internet Mail Extensions*](../secgloss/s-gly.md) (S/MIME) operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="54edd-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="54edd-106">Syntax</span></span>


```C++
HRESULT getCertTemplateSMIME(
  [in]  BSTR      bstrCertTemplateName,
  [out] DWORD *pdwCertTemplateSMIME
);
```


```VB

SCrdEnr.getCertTemplateSMIME( _
  ByVal bstrCertTemplateName, _
  ByRef pdwCertTemplateSMIME _
)
```





## <a name="parameters"></a><span data-ttu-id="54edd-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="54edd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54edd-108">*bstraucerttemplatename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="54edd-108">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54edd-109">Der Name des Zertifikats, das für die Verwendung von S/MIME-Schlüsseln abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="54edd-109">The name of the certificate being queried for the S/MIME key usage.</span></span>

</dd> <dt>

<span data-ttu-id="54edd-110">*pdwcerttemplatesmime* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="54edd-110">*pdwCertTemplateSMIME* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="54edd-111">Ein Zeiger auf ein **DWORD** , das den Wert 1 zurückgibt, wenn *bstrincerttemplatename* S/MIME unterstützt. Andernfalls wird NULL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="54edd-111">A pointer to a **DWORD** that returns a value of one if *bstrCertTemplateName* supports S/MIME; otherwise it returns zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54edd-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="54edd-112">Return value</span></span>

### <a name="c"></a><span data-ttu-id="54edd-113">C++</span><span class="sxs-lookup"><span data-stu-id="54edd-113">C++</span></span>

<span data-ttu-id="54edd-114">Wenn die Methode erfolgreich ausgeführt wird, gibt die Methode S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="54edd-114">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="54edd-115">Wenn die Methode fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="54edd-115">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="54edd-116">Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="54edd-116">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="54edd-117">VB</span><span class="sxs-lookup"><span data-stu-id="54edd-117">VB</span></span>

<span data-ttu-id="54edd-118">Der **lange** Wert 1, wenn *bstrincerttemplatename* S/MIME unterstützt. andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="54edd-118">**Long** value of one if *bstrCertTemplateName* supports S/MIME; otherwise zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="54edd-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="54edd-119">Remarks</span></span>

<span data-ttu-id="54edd-120">Die Konstante für szoid \_ PKIX \_ KP \_ -e-Mail- \_ Schutz ist in Wincrypt. h definiert.</span><span class="sxs-lookup"><span data-stu-id="54edd-120">The constant for szOID\_PKIX\_KP\_EMAIL\_PROTECTION is defined in Wincrypt.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="54edd-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="54edd-121">Requirements</span></span>



| <span data-ttu-id="54edd-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="54edd-122">Requirement</span></span> | <span data-ttu-id="54edd-123">Wert</span><span class="sxs-lookup"><span data-stu-id="54edd-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="54edd-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="54edd-124">Minimum supported client</span></span><br/> | <span data-ttu-id="54edd-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="54edd-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="54edd-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="54edd-126">Minimum supported server</span></span><br/> | <span data-ttu-id="54edd-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="54edd-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="54edd-128">DLL</span><span class="sxs-lookup"><span data-stu-id="54edd-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54edd-129"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54edd-129"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="54edd-130">IID</span><span class="sxs-lookup"><span data-stu-id="54edd-130">IID</span></span><br/>                      | <span data-ttu-id="54edd-131">IID \_ iscrdenr ist definiert als 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="54edd-131">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="54edd-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54edd-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54edd-133">**Iscrdenr**</span><span class="sxs-lookup"><span data-stu-id="54edd-133">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

<span data-ttu-id="54edd-134">[**Iscrdenr:: Enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="54edd-134">[**ISCrdEnr::enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))</span></span>
</dt> </dl>

 

 

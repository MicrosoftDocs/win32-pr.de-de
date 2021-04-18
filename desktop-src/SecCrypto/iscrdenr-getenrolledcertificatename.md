---
description: 'Ruft den Namen des Zertifikats ab, das sich aus einem früheren erfolgreichen Aufrufen von "iscrdenr:: Enroll" ergibt.'
ms.assetid: e33b217a-b717-49bd-b0f3-3ba9229a0696
title: 'Iscrdenr:: getenrolledcertifitorename-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getEnrolledCertificateName
- SCrdEnr.getEnrolledCertificateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: e3c9640e7719d2b5ac0e576384246cda5e1b2bfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351426"
---
# <a name="iscrdenrgetenrolledcertificatename-method"></a><span data-ttu-id="48b14-103">Iscrdenr:: getenrolledcertifitorename-Methode</span><span class="sxs-lookup"><span data-stu-id="48b14-103">ISCrdEnr::getEnrolledCertificateName method</span></span>

<span data-ttu-id="48b14-104">Die **getenrolledcertifitorename** -Methode ruft den Namen des Zertifikats ab, das sich aus einem früheren erfolgreichen Aufrufen von [**iscrdenr:: Enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))ergibt.</span><span class="sxs-lookup"><span data-stu-id="48b14-104">The **getEnrolledCertificateName** method retrieves the name of the certificate resulting from an earlier successful call to [**ISCrdEnr::enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85)).</span></span>

<span data-ttu-id="48b14-105">Diese Methode kann auch verwendet werden, um das Zertifikat in einem Dialogfeld anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="48b14-105">This method can also be used to display the certificate in a dialog box.</span></span> <span data-ttu-id="48b14-106">Diese Methode ruft die [*CryptoAPI*](../secgloss/c-gly.md) -Funktion [**certgetnamestring**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa)auf.</span><span class="sxs-lookup"><span data-stu-id="48b14-106">This method calls the [*CryptoAPI*](../secgloss/c-gly.md) function [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa).</span></span>

## <a name="syntax"></a><span data-ttu-id="48b14-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="48b14-107">Syntax</span></span>


```C++
HRESULT getEnrolledCertificateName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pBstrCertName
);
```


```VB

SCrdEnr.getEnrolledCertificateName( _
  ByVal dwFlags, _
  ByRef pBstrCertName _
)
```





## <a name="parameters"></a><span data-ttu-id="48b14-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="48b14-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48b14-109">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="48b14-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48b14-110">Ein-Wert, der bestimmt, ob das Zertifikat in einem Dialogfeld angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="48b14-110">A value that determines whether the certificate is displayed in a dialog box.</span></span> <span data-ttu-id="48b14-111">Wenn dieser Wert "SCard \_ ENROLL \_ No \_ Display \_ CERT (als 0x01 definiert)" lautet, wird das registrierte Zertifikat nicht angezeigt. alle anderen Werte bewirken, dass das registrierte Zertifikat im Dialogfeld " **Zertifikat** " angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="48b14-111">If this value is SCARD\_ENROLL\_NO\_DISPLAY\_CERT (defined as 0x01), the enrolled certificate is not displayed; any other values cause the enrolled certificate to be displayed in the **Certificate** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="48b14-112">*pbstraucertname* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="48b14-112">*pBstrCertName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="48b14-113">Ein Zeiger auf eine Zeichenfolge, die den abgerufenen Zertifikats Namen zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="48b14-113">A pointer to a string that returns the retrieved certificate name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48b14-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="48b14-114">Return value</span></span>

### <a name="c"></a><span data-ttu-id="48b14-115">C++</span><span class="sxs-lookup"><span data-stu-id="48b14-115">C++</span></span>

<span data-ttu-id="48b14-116">Wenn die Methode erfolgreich ausgeführt wird, gibt die Methode S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="48b14-116">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="48b14-117">Wenn die Methode fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="48b14-117">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="48b14-118">Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="48b14-118">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="48b14-119">VB</span><span class="sxs-lookup"><span data-stu-id="48b14-119">VB</span></span>

<span data-ttu-id="48b14-120">Eine Zeichenfolge, die den abgerufenen Zertifikats Namen darstellt.</span><span class="sxs-lookup"><span data-stu-id="48b14-120">A string that represents the retrieved certificate name.</span></span>

## <a name="remarks"></a><span data-ttu-id="48b14-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="48b14-121">Remarks</span></span>

<span data-ttu-id="48b14-122">Da diese Methode für ein vorhandenes Zertifikat funktioniert, müssen Sie [**iscrdenr:: Enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85)) erfolgreich aufrufen, bevor Sie **getenrolledcertifikatename** aufrufen können.</span><span class="sxs-lookup"><span data-stu-id="48b14-122">Because this method operates on an existing certificate, you must have successfully called [**ISCrdEnr::enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85)) before you can call **getEnrolledCertificateName**.</span></span>

<span data-ttu-id="48b14-123">Die **getenrolledcertifitorename** -Methode ruft die [**certgetnamestring**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa) -Funktion auf, um den Zertifikat Namen entsprechend der für den "CERT \_ Name \_ Simple \_ Display Type" \_ -Wert des *dwType* -Parameters von **certgetnamestring** beschriebenen Sequenz abzurufen.</span><span class="sxs-lookup"><span data-stu-id="48b14-123">The **getEnrolledCertificateName** method calls the [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa) function to retrieve the certificate name according to the sequence described for the CERT\_NAME\_SIMPLE\_DISPLAY\_TYPE value of **CertGetNameString**'s *dwType* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="48b14-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="48b14-124">Requirements</span></span>



| <span data-ttu-id="48b14-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="48b14-125">Requirement</span></span> | <span data-ttu-id="48b14-126">Wert</span><span class="sxs-lookup"><span data-stu-id="48b14-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="48b14-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="48b14-127">Minimum supported client</span></span><br/> | <span data-ttu-id="48b14-128">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="48b14-128">None supported</span></span><br/>                                                               |
| <span data-ttu-id="48b14-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="48b14-129">Minimum supported server</span></span><br/> | <span data-ttu-id="48b14-130">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48b14-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="48b14-131">DLL</span><span class="sxs-lookup"><span data-stu-id="48b14-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48b14-132"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48b14-132"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="48b14-133">IID</span><span class="sxs-lookup"><span data-stu-id="48b14-133">IID</span></span><br/>                      | <span data-ttu-id="48b14-134">IID \_ iscrdenr ist definiert als 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="48b14-134">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="48b14-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48b14-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48b14-136">**Iscrdenr**</span><span class="sxs-lookup"><span data-stu-id="48b14-136">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

<span data-ttu-id="48b14-137">[**Iscrdenr:: Enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="48b14-137">[**ISCrdEnr::enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))</span></span>
</dt> </dl>

 

 

---
description: Ruft die Anzahl der Zertifikat Vorlagen ab.
ms.assetid: f56e6e72-1562-4c53-b0da-b4bc69511559
title: 'Iscrdenr:: getcerttemplatecount-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCertTemplateCount
- SCrdEnr.getCertTemplateCount
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 86a78f03929bc6cdcfc7b611944b81c59a1c9fc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868208"
---
# <a name="iscrdenrgetcerttemplatecount-method"></a><span data-ttu-id="2b651-103">Iscrdenr:: getcerttemplatecount-Methode</span><span class="sxs-lookup"><span data-stu-id="2b651-103">ISCrdEnr::getCertTemplateCount method</span></span>

<span data-ttu-id="2b651-104">Die **getcerttemplatecount** -Methode ruft die Anzahl der Zertifikat Vorlagen ab.</span><span class="sxs-lookup"><span data-stu-id="2b651-104">The **getCertTemplateCount** method retrieves the number of certificate templates.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b651-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b651-105">Syntax</span></span>


```C++
HRESULT getCertTemplateCount(
  [in]  DWORD     dwFlags,
  [out] LONG *pdwCertTemplateCount
);
```


```VB

SCrdEnr.getCertTemplateCount( _
  ByVal dwFlags, _
  ByRef pdwCertTemplateCount _
)
```





## <a name="parameters"></a><span data-ttu-id="2b651-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b651-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b651-107">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2b651-107">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b651-108">Ein-Wert, der bestimmt, ob die Vorlage für Benutzer-oder Computer Zertifikate bestimmt ist.</span><span class="sxs-lookup"><span data-stu-id="2b651-108">A value that determines whether the template is for user or machine certificates.</span></span> <span data-ttu-id="2b651-109">Wenn dieser Wert "SCard \_ ENROLL \_ User \_ CERT \_ Template" (definiert als 1) ist, wird die zurückgegebene Anzahl für Benutzerzertifikat Vorlagen verwendet.</span><span class="sxs-lookup"><span data-stu-id="2b651-109">If this value is SCARD\_ENROLL\_USER\_CERT\_TEMPLATE (defined as 1) then the returned count will be for user certificate templates.</span></span> <span data-ttu-id="2b651-110">Wenn dieser Wert "SCard \_ ENROLL \_ Computer \_ CERT \_ Template" (definiert als 2) ist, wird die zurückgegebene Anzahl für Computer Zertifikat Vorlagen verwendet.</span><span class="sxs-lookup"><span data-stu-id="2b651-110">If this value is SCARD\_ENROLL\_MACHINE\_CERT\_TEMPLATE (defined as 2) then the returned count will be for machine certificate templates.</span></span>

</dd> <dt>

<span data-ttu-id="2b651-111">*pdwcerttemplatecount* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2b651-111">*pdwCertTemplateCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b651-112">Ein Zeiger auf einen **Long** -Wert, der die Anzahl der Zertifikat Vorlagen zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="2b651-112">A pointer to a **LONG** that returns the number of certificate templates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b651-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2b651-113">Return value</span></span>

### <a name="c"></a><span data-ttu-id="2b651-114">C++</span><span class="sxs-lookup"><span data-stu-id="2b651-114">C++</span></span>

<span data-ttu-id="2b651-115">Wenn die Methode erfolgreich ausgeführt wird, gibt die Methode S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="2b651-115">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="2b651-116">Wenn die Methode fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="2b651-116">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="2b651-117">Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="2b651-117">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="2b651-118">VB</span><span class="sxs-lookup"><span data-stu-id="2b651-118">VB</span></span>

<span data-ttu-id="2b651-119">Ein **Long** -Wert, der die Anzahl der Zertifikat Vorlagen darstellt.</span><span class="sxs-lookup"><span data-stu-id="2b651-119">A **Long** value that represents the number of certificate templates.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b651-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2b651-120">Requirements</span></span>



| <span data-ttu-id="2b651-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2b651-121">Requirement</span></span> | <span data-ttu-id="2b651-122">Wert</span><span class="sxs-lookup"><span data-stu-id="2b651-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b651-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2b651-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2b651-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2b651-124">None supported</span></span><br/>                                                               |
| <span data-ttu-id="2b651-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2b651-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2b651-126">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2b651-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2b651-127">DLL</span><span class="sxs-lookup"><span data-stu-id="2b651-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b651-128"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b651-128"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="2b651-129">IID</span><span class="sxs-lookup"><span data-stu-id="2b651-129">IID</span></span><br/>                      | <span data-ttu-id="2b651-130">IID \_ iscrdenr ist definiert als 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="2b651-130">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="2b651-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b651-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b651-132">**Iscrdenr**</span><span class="sxs-lookup"><span data-stu-id="2b651-132">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="2b651-133">**Iscrdenr:: enumcerttemplatename**</span><span class="sxs-lookup"><span data-stu-id="2b651-133">**ISCrdEnr::enumCertTemplateName**</span></span>](iscrdenr-enumcerttemplatename.md)
</dt> </dl>

 

 





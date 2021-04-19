---
description: Listet die Namen der Zertifikat Vorlagen auf.
ms.assetid: 4741eb0d-b8e0-468c-8a00-9ccacb52a9a7
title: 'Iscrdenr:: enumcerttemplatename-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.enumCertTemplateName
- SCrdEnr.enumCertTemplateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: a0a4850143cac48ef9b9b853f99153d4daeb4366
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362687"
---
# <a name="iscrdenrenumcerttemplatename-method"></a><span data-ttu-id="f55e8-103">Iscrdenr:: enumcerttemplatename-Methode</span><span class="sxs-lookup"><span data-stu-id="f55e8-103">ISCrdEnr::enumCertTemplateName method</span></span>

<span data-ttu-id="f55e8-104">Die **enumcerttemplatename** -Methode listet die Namen der Zertifikat Vorlagen auf.</span><span class="sxs-lookup"><span data-stu-id="f55e8-104">The **enumCertTemplateName** method enumerates the certificate template names.</span></span>

## <a name="syntax"></a><span data-ttu-id="f55e8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f55e8-105">Syntax</span></span>


```C++
HRESULT enumCertTemplateName(
  [in]  DWORD     dwIndex,
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrCertTemplateName
);
```


```VB

SCrdEnr.enumCertTemplateName( _
  ByVal dwIndex, _
  ByVal dwFlags, _
  ByRef pbstrCertTemplateName _
)
```





## <a name="parameters"></a><span data-ttu-id="f55e8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f55e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f55e8-107">*dwIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f55e8-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f55e8-108">Der null basierte Index für die enumerationssequenz.</span><span class="sxs-lookup"><span data-stu-id="f55e8-108">The zero-based index for the enumeration sequence.</span></span>

</dd> <dt>

<span data-ttu-id="f55e8-109">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f55e8-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f55e8-110">Ein-Wert, der bestimmt, ob die aufgelistete Zertifikat Vorlage auf Benutzer-oder Computer Zertifikate angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="f55e8-110">A value that determines whether the enumerated certificate template applies to user or machine certificates.</span></span> <span data-ttu-id="f55e8-111">Wenn dieser Wert "SCard \_ ENROLL \_ User \_ CERT \_ Template" (definiert als 1) ist, gilt die Enumeration für Benutzerzertifikat Vorlagen.</span><span class="sxs-lookup"><span data-stu-id="f55e8-111">If this value is SCARD\_ENROLL\_USER\_CERT\_TEMPLATE (defined as 1), the enumeration applies to user certificate templates.</span></span> <span data-ttu-id="f55e8-112">Wenn dieser Wert "SCard \_ ENROLL \_ Computer \_ CERT \_ Template" (definiert als 2) ist, gilt die Enumeration für Computer Zertifikat Vorlagen.</span><span class="sxs-lookup"><span data-stu-id="f55e8-112">If this value is SCARD\_ENROLL\_MACHINE\_CERT\_TEMPLATE (defined as 2), the enumeration applies to machine certificate templates.</span></span>

</dd> <dt>

<span data-ttu-id="f55e8-113">*pbstraucerttemplatename* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f55e8-113">*pbstrCertTemplateName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f55e8-114">Ein Zeiger auf eine Zeichenfolge, die den Namen der aufgelisteten Zertifikat Vorlage zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="f55e8-114">A pointer to a string that returns the name of the enumerated certificate template.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f55e8-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f55e8-115">Return value</span></span>

### <a name="c"></a><span data-ttu-id="f55e8-116">C++</span><span class="sxs-lookup"><span data-stu-id="f55e8-116">C++</span></span>

<span data-ttu-id="f55e8-117">Wenn die Methode erfolgreich ausgeführt wird, gibt die Methode S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="f55e8-117">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="f55e8-118">Wenn die Methode fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="f55e8-118">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="f55e8-119">Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="f55e8-119">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="f55e8-120">VB</span><span class="sxs-lookup"><span data-stu-id="f55e8-120">VB</span></span>

<span data-ttu-id="f55e8-121">Eine Zeichenfolge, die den Namen der aufgelisteten Zertifikat Vorlage enthält.</span><span class="sxs-lookup"><span data-stu-id="f55e8-121">A string that contains the name of the enumerated certificate template.</span></span>

## <a name="requirements"></a><span data-ttu-id="f55e8-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f55e8-122">Requirements</span></span>



| <span data-ttu-id="f55e8-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f55e8-123">Requirement</span></span> | <span data-ttu-id="f55e8-124">Wert</span><span class="sxs-lookup"><span data-stu-id="f55e8-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f55e8-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f55e8-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f55e8-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f55e8-126">None supported</span></span><br/>                                                               |
| <span data-ttu-id="f55e8-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f55e8-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f55e8-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f55e8-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f55e8-129">DLL</span><span class="sxs-lookup"><span data-stu-id="f55e8-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f55e8-130"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f55e8-130"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="f55e8-131">IID</span><span class="sxs-lookup"><span data-stu-id="f55e8-131">IID</span></span><br/>                      | <span data-ttu-id="f55e8-132">IID \_ iscrdenr ist definiert als 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="f55e8-132">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="f55e8-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f55e8-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f55e8-134">**Iscrdenr**</span><span class="sxs-lookup"><span data-stu-id="f55e8-134">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="f55e8-135">**Iscrdenr:: getcerttemplatecount**</span><span class="sxs-lookup"><span data-stu-id="f55e8-135">**ISCrdEnr::getCertTemplateCount**</span></span>](iscrdenr-getcerttemplatecount.md)
</dt> <dt>

[<span data-ttu-id="f55e8-136">**Iscrdenr:: getcerttemplatename**</span><span class="sxs-lookup"><span data-stu-id="f55e8-136">**ISCrdEnr::getCertTemplateName**</span></span>](iscrdenr-getcerttemplatename.md)
</dt> <dt>

[<span data-ttu-id="f55e8-137">**Iscrdenr:: setcerttemplatename**</span><span class="sxs-lookup"><span data-stu-id="f55e8-137">**ISCrdEnr::setCertTemplateName**</span></span>](iscrdenr-setcerttemplatename.md)
</dt> </dl>

 

 





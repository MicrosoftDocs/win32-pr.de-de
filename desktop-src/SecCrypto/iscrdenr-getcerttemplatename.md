---
description: Ruft den Namen der Zertifikat Vorlage ab.
ms.assetid: 26fd758a-b348-4efb-841b-c8f2ab88efea
title: 'Iscrdenr:: getcerttemplatename-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCertTemplateName
- SCrdEnr.getCertTemplateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 4eee84140e0a23b8a0dd5d26099ca61b868a90fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217995"
---
# <a name="iscrdenrgetcerttemplatename-method"></a><span data-ttu-id="e371e-103">Iscrdenr:: getcerttemplatename-Methode</span><span class="sxs-lookup"><span data-stu-id="e371e-103">ISCrdEnr::getCertTemplateName method</span></span>

<span data-ttu-id="e371e-104">Die **getcerttemplatename** -Methode ruft den Namen der Zertifikat Vorlage ab.</span><span class="sxs-lookup"><span data-stu-id="e371e-104">The **getCertTemplateName** method retrieves the name of the certificate template.</span></span>

## <a name="syntax"></a><span data-ttu-id="e371e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e371e-105">Syntax</span></span>


```C++
HRESULT getCertTemplateName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrCertTemplateName
);
```


```VB

SCrdEnr.getCertTemplateName( _
  ByVal dwFlags, _
  ByRef pbstrCertTemplateName _
)
```





## <a name="parameters"></a><span data-ttu-id="e371e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e371e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e371e-107">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e371e-107">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e371e-108">Ein-Wert, der bestimmt, ob der tatsächliche Name oder der Anzeige Name der Zertifikat Vorlage zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e371e-108">A value that determines whether the certificate template's real name or display name is returned.</span></span> <span data-ttu-id="e371e-109">Wenn *dwFlags* den \_ \_ \_ \_ anzeigen Amen "Name der Zertifikat Vorlage" aufweisen \_ , wird der Anzeige Name der Zertifikat Vorlage abgerufen. andernfalls wird der tatsächliche Name der Zertifikat Vorlage angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e371e-109">If *dwFlags* has the value SCARD\_ENROLL\_CERT\_TEMPLATE\_DISPLAY\_NAME, the certificate template's display name is retrieved; otherwise, the real name of the certificate template is displayed.</span></span>

</dd> <dt>

<span data-ttu-id="e371e-110">*pbstraucerttemplatename* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e371e-110">*pbstrCertTemplateName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e371e-111">Ein Zeiger auf eine Zeichenfolge, die den Namen der Zertifikat Vorlage zurückgibt, die in der [*Zertifikat Anforderung*](../secgloss/c-gly.md)verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e371e-111">A pointer to a string that returns the name of the certificate template which will be used in the [*certificate request*](../secgloss/c-gly.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e371e-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e371e-112">Return value</span></span>

### <a name="c"></a><span data-ttu-id="e371e-113">C++</span><span class="sxs-lookup"><span data-stu-id="e371e-113">C++</span></span>

<span data-ttu-id="e371e-114">Wenn die Methode erfolgreich ausgeführt wird, gibt die Methode S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="e371e-114">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="e371e-115">Wenn die Methode fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="e371e-115">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="e371e-116">Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="e371e-116">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="e371e-117">VB</span><span class="sxs-lookup"><span data-stu-id="e371e-117">VB</span></span>

<span data-ttu-id="e371e-118">Eine Zeichenfolge, die den Namen der Zertifikat Vorlage darstellt, die in der [*Zertifikat Anforderung*](../secgloss/c-gly.md)verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e371e-118">A string that represents the name of the certificate template which will be used in the [*certificate request*](../secgloss/c-gly.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e371e-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e371e-119">Remarks</span></span>

<span data-ttu-id="e371e-120">Wenn Sie den Namen der Zertifikat Vorlage nicht durch Aufrufen von [**iscrdenr:: setcerttemplatename**](iscrdenr-setcerttemplatename.md)festlegen, wird der Name standardmäßig auf den Vornamen in der Liste der verfügbaren Zertifikat Vorlagen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e371e-120">If you do not set the certificate template name by calling [**ISCrdEnr::setCertTemplateName**](iscrdenr-setcerttemplatename.md), the name defaults to the first name in the list of available certificate templates.</span></span>

## <a name="requirements"></a><span data-ttu-id="e371e-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e371e-121">Requirements</span></span>



| <span data-ttu-id="e371e-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e371e-122">Requirement</span></span> | <span data-ttu-id="e371e-123">Wert</span><span class="sxs-lookup"><span data-stu-id="e371e-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e371e-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e371e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e371e-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e371e-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="e371e-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e371e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e371e-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e371e-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e371e-128">DLL</span><span class="sxs-lookup"><span data-stu-id="e371e-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e371e-129"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e371e-129"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="e371e-130">IID</span><span class="sxs-lookup"><span data-stu-id="e371e-130">IID</span></span><br/>                      | <span data-ttu-id="e371e-131">IID \_ iscrdenr ist definiert als 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="e371e-131">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="e371e-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e371e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e371e-133">**Iscrdenr**</span><span class="sxs-lookup"><span data-stu-id="e371e-133">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="e371e-134">**Iscrdenr:: setcerttemplatename**</span><span class="sxs-lookup"><span data-stu-id="e371e-134">**ISCrdEnr::setCertTemplateName**</span></span>](iscrdenr-setcerttemplatename.md)
</dt> </dl>

 

 

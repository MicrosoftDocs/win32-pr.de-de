---
description: Gibt den Namen der Zertifikat Vorlage an.
ms.assetid: 15d22130-e614-4505-94e8-83c2efbf6d87
title: 'Iscrdenr:: setcerttemplatename-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setCertTemplateName
- SCrdEnr.setCertTemplateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 53ba18626a7d2bb703ed4d11953fb4872cf9257c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348641"
---
# <a name="iscrdenrsetcerttemplatename-method"></a><span data-ttu-id="fff8e-103">Iscrdenr:: setcerttemplatename-Methode</span><span class="sxs-lookup"><span data-stu-id="fff8e-103">ISCrdEnr::setCertTemplateName method</span></span>

<span data-ttu-id="fff8e-104">Die **setcerttemplatename** -Methode gibt den Namen der Zertifikat Vorlage an.</span><span class="sxs-lookup"><span data-stu-id="fff8e-104">The **setCertTemplateName** method specifies the name of the certificate template.</span></span>

## <a name="syntax"></a><span data-ttu-id="fff8e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fff8e-105">Syntax</span></span>


```C++
HRESULT setCertTemplateName(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName
);
```


```VB

SCrdEnr.setCertTemplateName( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName _
)
```





## <a name="parameters"></a><span data-ttu-id="fff8e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fff8e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fff8e-107">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fff8e-107">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fff8e-108">Ein Wert, der bestimmt, ob der echte Name oder der Anzeige Name der Zertifikat Vorlage festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="fff8e-108">Value which determines if the certificate template's real name or display name is being set.</span></span> <span data-ttu-id="fff8e-109">Wenn *dwFlags* den \_ \_ \_ \_ anzeigen Amen "Name der Zertifikat Vorlage" aufweisen \_ , wird der Anzeige Name der Zertifikat Vorlage festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fff8e-109">If *dwFlags* has the value SCARD\_ENROLL\_CERT\_TEMPLATE\_DISPLAY\_NAME, the certificate template's display name is set.</span></span> <span data-ttu-id="fff8e-110">Andernfalls wird der echte Name der Zertifikat Vorlage festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fff8e-110">Otherwise, the real name of the certificate template is set.</span></span>

</dd> <dt>

<span data-ttu-id="fff8e-111">*bstraucerttemplatename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fff8e-111">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fff8e-112">Der Name der Zertifikat Vorlage, die in der Zertifikat Anforderung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fff8e-112">Name of the certificate template which will be used in the certificate request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fff8e-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fff8e-113">Return value</span></span>

### <a name="vb"></a><span data-ttu-id="fff8e-114">VB</span><span class="sxs-lookup"><span data-stu-id="fff8e-114">VB</span></span>

<span data-ttu-id="fff8e-115">Wenn die Methode erfolgreich ausgeführt wird, gibt die Methode S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="fff8e-115">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="fff8e-116">Wenn die Methode fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="fff8e-116">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="fff8e-117">Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="fff8e-117">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fff8e-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fff8e-118">Remarks</span></span>

<span data-ttu-id="fff8e-119">Wenn Sie den Namen der Zertifikat Vorlage nicht durch Aufrufen von **iscrdenr:: setcerttemplatename** festlegen, wird der Name standardmäßig auf den Vornamen in der Liste der verfügbaren Zertifikat Vorlagen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fff8e-119">If you do not set the certificate template name by calling **ISCrdEnr::setCertTemplateName**, the name defaults to the first name in the list of available certificate templates.</span></span>

## <a name="requirements"></a><span data-ttu-id="fff8e-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fff8e-120">Requirements</span></span>



| <span data-ttu-id="fff8e-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fff8e-121">Requirement</span></span> | <span data-ttu-id="fff8e-122">Wert</span><span class="sxs-lookup"><span data-stu-id="fff8e-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fff8e-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fff8e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="fff8e-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="fff8e-124">None supported</span></span><br/>                                                               |
| <span data-ttu-id="fff8e-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fff8e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="fff8e-126">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fff8e-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fff8e-127">DLL</span><span class="sxs-lookup"><span data-stu-id="fff8e-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fff8e-128"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fff8e-128"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="fff8e-129">IID</span><span class="sxs-lookup"><span data-stu-id="fff8e-129">IID</span></span><br/>                      | <span data-ttu-id="fff8e-130">IID \_ iscrdenr ist definiert als 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="fff8e-130">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="fff8e-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fff8e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fff8e-132">**Iscrdenr**</span><span class="sxs-lookup"><span data-stu-id="fff8e-132">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="fff8e-133">**Iscrdenr:: getcerttemplatename**</span><span class="sxs-lookup"><span data-stu-id="fff8e-133">**ISCrdEnr::getCertTemplateName**</span></span>](iscrdenr-getcerttemplatename.md)
</dt> </dl>

 

 





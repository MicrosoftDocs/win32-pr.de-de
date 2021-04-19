---
description: Gibt die Anzahl der Zertifizierungsstellen (CAS) zurück, die bereit sind, ein Zertifikat basierend auf der angegebenen Zertifikat Vorlage auszustellen.
ms.assetid: 377121a8-3895-4308-a803-4a62580c6de0
title: 'Iscrdenr:: getcacount-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCACount
- SCrdEnr.getCACount
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: eb33f6c7345862dedf6c909054d811ff4da470ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364222"
---
# <a name="iscrdenrgetcacount-method"></a><span data-ttu-id="94d33-103">Iscrdenr:: getcacount-Methode</span><span class="sxs-lookup"><span data-stu-id="94d33-103">ISCrdEnr::getCACount method</span></span>

<span data-ttu-id="94d33-104">Die **getcacount** -Methode gibt die Anzahl der [*Zertifizierungs*](../secgloss/c-gly.md) stellen (CAS) zurück, die bereit sind, ein Zertifikat basierend auf der angegebenen Zertifikat Vorlage auszustellen.</span><span class="sxs-lookup"><span data-stu-id="94d33-104">The **getCACount** method returns the number of [*certification authorities*](../secgloss/c-gly.md) (CAs) willing to issue a certificate based on the specified certificate template.</span></span>

## <a name="syntax"></a><span data-ttu-id="94d33-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="94d33-105">Syntax</span></span>


```C++
HRESULT getCACount(
  [in]  BSTR     bstrCertTemplateName,
  [out] LONG *pdwCACount
);
```


```VB

SCrdEnr.getCACount( _
  ByVal bstrCertTemplateName, _
  ByRef pdwCACount _
)
```





## <a name="parameters"></a><span data-ttu-id="94d33-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="94d33-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94d33-107">*bstraucerttemplatename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="94d33-107">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94d33-108">Eine Zeichenfolge, die den Namen der Zertifikat Vorlage darstellt.</span><span class="sxs-lookup"><span data-stu-id="94d33-108">A string that represents the name of the certificate template.</span></span>

</dd> <dt>

<span data-ttu-id="94d33-109">*pdwcacount* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="94d33-109">*pdwCACount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="94d33-110">Ein Zeiger auf einen **Long** -Wert, der die Anzahl der verfügbaren CAS zurückgibt, die ein Zertifikat für die in *bstrincerttemplatename* angegebene Zertifikat Vorlage ausstellen.</span><span class="sxs-lookup"><span data-stu-id="94d33-110">A pointer to a **LONG** that returns the number of available CAs that will issue a certificate for the certificate template specified in *bstrCertTemplateName*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94d33-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="94d33-111">Return value</span></span>

### <a name="c"></a><span data-ttu-id="94d33-112">C++</span><span class="sxs-lookup"><span data-stu-id="94d33-112">C++</span></span>

<span data-ttu-id="94d33-113">Wenn die Methode erfolgreich ausgeführt wird, gibt die Methode S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="94d33-113">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="94d33-114">Wenn die Methode fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="94d33-114">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="94d33-115">Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="94d33-115">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="94d33-116">VB</span><span class="sxs-lookup"><span data-stu-id="94d33-116">VB</span></span>

<span data-ttu-id="94d33-117">Ein **langer** Wert, der die Anzahl der verfügbaren Zertifizierungsstellen darstellt, die ein Zertifikat für die in *bstrincerttemplatename* angegebene Zertifikat Vorlage ausstellen.</span><span class="sxs-lookup"><span data-stu-id="94d33-117">A **Long** value that represents the number of available CAs that will issue a certificate for the certificate template specified in *bstrCertTemplateName*.</span></span>

## <a name="requirements"></a><span data-ttu-id="94d33-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="94d33-118">Requirements</span></span>



| <span data-ttu-id="94d33-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="94d33-119">Requirement</span></span> | <span data-ttu-id="94d33-120">Wert</span><span class="sxs-lookup"><span data-stu-id="94d33-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="94d33-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="94d33-121">Minimum supported client</span></span><br/> | <span data-ttu-id="94d33-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="94d33-122">None supported</span></span><br/>                                                               |
| <span data-ttu-id="94d33-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="94d33-123">Minimum supported server</span></span><br/> | <span data-ttu-id="94d33-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="94d33-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="94d33-125">DLL</span><span class="sxs-lookup"><span data-stu-id="94d33-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94d33-126"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94d33-126"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="94d33-127">IID</span><span class="sxs-lookup"><span data-stu-id="94d33-127">IID</span></span><br/>                      | <span data-ttu-id="94d33-128">IID \_ iscrdenr ist definiert als 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="94d33-128">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="94d33-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="94d33-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94d33-130">**Iscrdenr**</span><span class="sxs-lookup"><span data-stu-id="94d33-130">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="94d33-131">**Iscrdenr:: enumcaname**</span><span class="sxs-lookup"><span data-stu-id="94d33-131">**ISCrdEnr::enumCAName**</span></span>](iscrdenr-enumcaname.md)
</dt> <dt>

[<span data-ttu-id="94d33-132">**Iscrdenr:: getcaname**</span><span class="sxs-lookup"><span data-stu-id="94d33-132">**ISCrdEnr::getCAName**</span></span>](iscrdenr-getcaname.md)
</dt> </dl>

 

 

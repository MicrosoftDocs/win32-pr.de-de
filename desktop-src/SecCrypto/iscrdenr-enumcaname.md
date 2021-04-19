---
description: Listet den Namen der Zertifizierungsstellen (CAS) für einen angegebenen Namen für die Zertifikat Vorlage auf.
ms.assetid: 82cc3346-a8b9-4abd-933a-c212a37a373e
title: 'Iscrdenr:: enumcaname-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.enumCAName
- SCrdEnr.enumCAName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: c23df2f74cdf3791f1280e38cbff8ddd48f924b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349658"
---
# <a name="iscrdenrenumcaname-method"></a><span data-ttu-id="46aeb-103">Iscrdenr:: enumcaname-Methode</span><span class="sxs-lookup"><span data-stu-id="46aeb-103">ISCrdEnr::enumCAName method</span></span>

<span data-ttu-id="46aeb-104">Mit der **enumcaname** -Methode wird der Name der [*Zertifizierungs*](../secgloss/c-gly.md) stellen (CAS) für einen angegebenen Zertifikat Vorlagen Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="46aeb-104">The **enumCAName** method enumerates the name of the [*certification authorities*](../secgloss/c-gly.md) (CAs) for a given certificate template name.</span></span>

## <a name="syntax"></a><span data-ttu-id="46aeb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="46aeb-105">Syntax</span></span>


```C++
HRESULT enumCAName(
  [in]  DWORD     dwIndex,
  [in]  DWORD     dwFlags,
  [in]  BSTR     bstrCertTemplateName,
  [out] BSTR *pbstrCAName
);
```


```VB

SCrdEnr.enumCAName( _
  ByVal dwIndex, _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName, _
  ByRef pbstrCAName _
)
```





## <a name="parameters"></a><span data-ttu-id="46aeb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="46aeb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46aeb-107">*dwIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46aeb-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46aeb-108">Der null basierte Index für die enumerationssequenz.</span><span class="sxs-lookup"><span data-stu-id="46aeb-108">The zero-based index for the enumeration sequence.</span></span>

</dd> <dt>

<span data-ttu-id="46aeb-109">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46aeb-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46aeb-110">Ein-Wert, der bestimmt, ob der Name auf den ZS-Namen oder den Computernamen der Zertifizierungsstelle verweist.</span><span class="sxs-lookup"><span data-stu-id="46aeb-110">A value that determines whether the name refers to the CA name or the CA's machine name.</span></span> <span data-ttu-id="46aeb-111">Wenn es sich bei diesem Wert um den Computer \_ \_ Namen der Zertifizierungsstelle \_ \_ (definiert als 0x01) handelt, bezieht sich der Name auf den Computernamen der Zertifizierungsstelle.</span><span class="sxs-lookup"><span data-stu-id="46aeb-111">If this value is SCARD\_ENROLL\_CA\_MACHINE\_NAME (defined as 0x01), the name refers to the CA's machine name.</span></span> <span data-ttu-id="46aeb-112">Andernfalls bezieht sich der Name auf den Zertifizierungsstellen Namen.</span><span class="sxs-lookup"><span data-stu-id="46aeb-112">Otherwise the name refers to the CA name.</span></span>

</dd> <dt>

<span data-ttu-id="46aeb-113">*bstraucerttemplatename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46aeb-113">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46aeb-114">Der Name der Zertifikat Vorlage.</span><span class="sxs-lookup"><span data-stu-id="46aeb-114">The name of the certificate template.</span></span>

</dd> <dt>

<span data-ttu-id="46aeb-115">*pbstraucaname* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="46aeb-115">*pbstrCAName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46aeb-116">Ein Zeiger auf eine Zeichenfolge, die den Namen der Zertifizierungsstelle zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="46aeb-116">A pointer to a string that returns the name of the CA.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46aeb-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="46aeb-117">Return value</span></span>

### <a name="c"></a><span data-ttu-id="46aeb-118">C++</span><span class="sxs-lookup"><span data-stu-id="46aeb-118">C++</span></span>

<span data-ttu-id="46aeb-119">Wenn die Methode erfolgreich ausgeführt wird, gibt die Methode S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="46aeb-119">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="46aeb-120">Wenn die Methode fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="46aeb-120">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="46aeb-121">Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="46aeb-121">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="46aeb-122">VB</span><span class="sxs-lookup"><span data-stu-id="46aeb-122">VB</span></span>

<span data-ttu-id="46aeb-123">Eine Zeichenfolge, die den Namen der Zertifizierungsstelle darstellt.</span><span class="sxs-lookup"><span data-stu-id="46aeb-123">A string that represents the name of the CA.</span></span>

## <a name="requirements"></a><span data-ttu-id="46aeb-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="46aeb-124">Requirements</span></span>



| <span data-ttu-id="46aeb-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="46aeb-125">Requirement</span></span> | <span data-ttu-id="46aeb-126">Wert</span><span class="sxs-lookup"><span data-stu-id="46aeb-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46aeb-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="46aeb-127">Minimum supported client</span></span><br/> | <span data-ttu-id="46aeb-128">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="46aeb-128">None supported</span></span><br/>                                                               |
| <span data-ttu-id="46aeb-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="46aeb-129">Minimum supported server</span></span><br/> | <span data-ttu-id="46aeb-130">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="46aeb-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="46aeb-131">DLL</span><span class="sxs-lookup"><span data-stu-id="46aeb-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46aeb-132"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46aeb-132"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="46aeb-133">IID</span><span class="sxs-lookup"><span data-stu-id="46aeb-133">IID</span></span><br/>                      | <span data-ttu-id="46aeb-134">IID \_ iscrdenr ist definiert als 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="46aeb-134">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="46aeb-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46aeb-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46aeb-136">**Iscrdenr**</span><span class="sxs-lookup"><span data-stu-id="46aeb-136">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="46aeb-137">**Iscrdenr:: getcacount**</span><span class="sxs-lookup"><span data-stu-id="46aeb-137">**ISCrdEnr::getCACount**</span></span>](iscrdenr-getcacount.md)
</dt> <dt>

[<span data-ttu-id="46aeb-138">**Iscrdenr:: getcaname**</span><span class="sxs-lookup"><span data-stu-id="46aeb-138">**ISCrdEnr::getCAName**</span></span>](iscrdenr-getcaname.md)
</dt> <dt>

[<span data-ttu-id="46aeb-139">**Iscrdenr:: setcaname**</span><span class="sxs-lookup"><span data-stu-id="46aeb-139">**ISCrdEnr::setCAName**</span></span>](iscrdenr-setcaname.md)
</dt> </dl>

 

 

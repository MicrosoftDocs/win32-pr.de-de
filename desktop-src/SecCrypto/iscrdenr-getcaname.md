---
description: Ruft den Namen der angegebenen Zertifizierungsstelle (Certification Authority, ca) für eine angegebene Zertifikat Vorlage ab.
ms.assetid: e921710a-7c74-4fda-91e1-fbad45889984
title: 'Iscrdenr:: getcaname-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCAName
- SCrdEnr.getCAName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: b62b0a7e871a29ff0a8edd28eb8cd5e18e97c1a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217997"
---
# <a name="iscrdenrgetcaname-method"></a><span data-ttu-id="105ae-103">Iscrdenr:: getcaname-Methode</span><span class="sxs-lookup"><span data-stu-id="105ae-103">ISCrdEnr::getCAName method</span></span>

<span data-ttu-id="105ae-104">Die **getcaname** -Methode ruft den Namen der angegebenen Zertifizierungsstelle ( [*Certification Authority*](../secgloss/c-gly.md) , ca) für eine angegebene Zertifikat Vorlage ab.</span><span class="sxs-lookup"><span data-stu-id="105ae-104">The **getCAName** method retrieves the name of the specified [*certification authority*](../secgloss/c-gly.md) (CA) for a given certificate template.</span></span>

## <a name="syntax"></a><span data-ttu-id="105ae-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="105ae-105">Syntax</span></span>


```C++
HRESULT getCAName(
  [in]  DWORD     dwFlags,
  [in]  BSTR     bstrCertTemplateName,
  [out] BSTR *pbstrCAName
);
```


```VB

SCrdEnr.getCAName( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName, _
  ByRef pbstrCAName _
)
```





## <a name="parameters"></a><span data-ttu-id="105ae-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="105ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="105ae-107">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="105ae-107">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="105ae-108">Ein-Wert, der bestimmt, ob der Name auf den ZS-Namen oder den Computernamen der Zertifizierungsstelle verweist.</span><span class="sxs-lookup"><span data-stu-id="105ae-108">A value that determines whether the name refers to the CA name or the CA's machine name.</span></span> <span data-ttu-id="105ae-109">Wenn es sich bei diesem Wert um den Computer \_ \_ Namen der Zertifizierungsstelle \_ \_ (definiert als 0x01) handelt, verweist der Name auf den Computernamen der Zertifizierungsstelle; andernfalls bezieht sich der Name auf den Namen der Zertifizierungsstelle.</span><span class="sxs-lookup"><span data-stu-id="105ae-109">If this value is SCARD\_ENROLL\_CA\_MACHINE\_NAME (defined as 0x01) then the name refers to the CA's machine name; otherwise the name refers to the CA name.</span></span>

</dd> <dt>

<span data-ttu-id="105ae-110">*bstraucerttemplatename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="105ae-110">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="105ae-111">Der Name der Zertifikat Vorlage.</span><span class="sxs-lookup"><span data-stu-id="105ae-111">The name of the certificate template.</span></span>

</dd> <dt>

<span data-ttu-id="105ae-112">*pbstraucaname* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="105ae-112">*pbstrCAName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="105ae-113">Ein Zeiger auf eine Zeichenfolge, die den Namen der Zertifizierungsstelle zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="105ae-113">A pointer to a string that returns the name of the CA.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="105ae-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="105ae-114">Return value</span></span>

### <a name="c"></a><span data-ttu-id="105ae-115">C++</span><span class="sxs-lookup"><span data-stu-id="105ae-115">C++</span></span>

<span data-ttu-id="105ae-116">Wenn die Methode erfolgreich ausgeführt wird, gibt die Methode S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="105ae-116">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="105ae-117">Wenn die Methode fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="105ae-117">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="105ae-118">Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="105ae-118">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="105ae-119">VB</span><span class="sxs-lookup"><span data-stu-id="105ae-119">VB</span></span>

<span data-ttu-id="105ae-120">Eine Zeichenfolge, die den Namen der Zertifizierungsstelle darstellt.</span><span class="sxs-lookup"><span data-stu-id="105ae-120">A string that represents the name of the CA.</span></span>

## <a name="remarks"></a><span data-ttu-id="105ae-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="105ae-121">Remarks</span></span>

<span data-ttu-id="105ae-122">Der Standardname der Zertifizierungsstelle ist der Vorname in der Liste der verfügbaren Zertifizierungsstellen.</span><span class="sxs-lookup"><span data-stu-id="105ae-122">The default CA name is the first name in the available list of CAs.</span></span>

## <a name="requirements"></a><span data-ttu-id="105ae-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="105ae-123">Requirements</span></span>



| <span data-ttu-id="105ae-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="105ae-124">Requirement</span></span> | <span data-ttu-id="105ae-125">Wert</span><span class="sxs-lookup"><span data-stu-id="105ae-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="105ae-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="105ae-126">Minimum supported client</span></span><br/> | <span data-ttu-id="105ae-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="105ae-127">None supported</span></span><br/>                                                               |
| <span data-ttu-id="105ae-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="105ae-128">Minimum supported server</span></span><br/> | <span data-ttu-id="105ae-129">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="105ae-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="105ae-130">DLL</span><span class="sxs-lookup"><span data-stu-id="105ae-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="105ae-131"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="105ae-131"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="105ae-132">IID</span><span class="sxs-lookup"><span data-stu-id="105ae-132">IID</span></span><br/>                      | <span data-ttu-id="105ae-133">IID \_ iscrdenr ist definiert als 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="105ae-133">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="105ae-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="105ae-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="105ae-135">**Iscrdenr**</span><span class="sxs-lookup"><span data-stu-id="105ae-135">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="105ae-136">**Iscrdenr:: enumcaname**</span><span class="sxs-lookup"><span data-stu-id="105ae-136">**ISCrdEnr::enumCAName**</span></span>](iscrdenr-enumcaname.md)
</dt> <dt>

[<span data-ttu-id="105ae-137">**Iscrdenr:: getcacount**</span><span class="sxs-lookup"><span data-stu-id="105ae-137">**ISCrdEnr::getCACount**</span></span>](iscrdenr-getcacount.md)
</dt> <dt>

[<span data-ttu-id="105ae-138">**Iscrdenr:: setcaname**</span><span class="sxs-lookup"><span data-stu-id="105ae-138">**ISCrdEnr::setCAName**</span></span>](iscrdenr-setcaname.md)
</dt> </dl>

 

 

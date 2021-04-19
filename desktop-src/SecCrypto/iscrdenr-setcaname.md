---
description: Gibt den Namen der Zertifizierungsstelle an.
ms.assetid: 224c2a51-8a25-4b66-b86b-c87531475145
title: 'Iscrdenr:: setcaname-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setCAName
- SCrdEnr.setCAName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 46dcd9294337c088b9e1b0ab68bddefe4308ed27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350048"
---
# <a name="iscrdenrsetcaname-method"></a><span data-ttu-id="544ce-103">Iscrdenr:: setcaname-Methode</span><span class="sxs-lookup"><span data-stu-id="544ce-103">ISCrdEnr::setCAName method</span></span>

<span data-ttu-id="544ce-104">Die **setcaname** -Methode gibt den Namen der [*Zertifizierungs*](../secgloss/c-gly.md) Stelle an.</span><span class="sxs-lookup"><span data-stu-id="544ce-104">The **setCAName** method specifies the name of the [*certification authority*](../secgloss/c-gly.md) (CA).</span></span>

## <a name="syntax"></a><span data-ttu-id="544ce-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="544ce-105">Syntax</span></span>


```C++
HRESULT setCAName(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName,
  [in] BSTR bstrCAName
);
```


```VB

SCrdEnr.setCAName( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName, _
  ByVal bstrCAName _
)
```





## <a name="parameters"></a><span data-ttu-id="544ce-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="544ce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="544ce-107">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="544ce-107">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="544ce-108">Ein Wert, der angibt, ob der Name auf den ZS-Namen oder den Computernamen der Zertifizierungsstelle verweist.</span><span class="sxs-lookup"><span data-stu-id="544ce-108">Value that specifies whether the name refers to the CA name or the CA's machine name.</span></span> <span data-ttu-id="544ce-109">Wenn es sich bei diesem Wert um den Computer \_ \_ Namen der Zertifizierungsstelle \_ \_ (definiert als 0x01) handelt, bezieht sich der Name auf den Computernamen der Zertifizierungsstelle.</span><span class="sxs-lookup"><span data-stu-id="544ce-109">If this value is SCARD\_ENROLL\_CA\_MACHINE\_NAME (defined as 0x01), the name refers to the CA's machine name.</span></span> <span data-ttu-id="544ce-110">Andernfalls bezieht sich der Name auf den Zertifizierungsstellen Namen.</span><span class="sxs-lookup"><span data-stu-id="544ce-110">Otherwise, the name refers to the CA name.</span></span>

</dd> <dt>

<span data-ttu-id="544ce-111">*bstraucerttemplatename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="544ce-111">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="544ce-112">Name der Zertifikat Vorlage.</span><span class="sxs-lookup"><span data-stu-id="544ce-112">Name of the certificate template.</span></span>

</dd> <dt>

<span data-ttu-id="544ce-113">*bstraucaname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="544ce-113">*bstrCAName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="544ce-114">Der ZS-Name, der mit der von *bstrincerttemplatename* angegebenen Zertifikat Vorlage verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="544ce-114">CA name to be used with the certificate template specified by *bstrCertTemplateName*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="544ce-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="544ce-115">Return value</span></span>

### <a name="vb"></a><span data-ttu-id="544ce-116">VB</span><span class="sxs-lookup"><span data-stu-id="544ce-116">VB</span></span>

<span data-ttu-id="544ce-117">Der Rückgabewert ist ein **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="544ce-117">The return value is an **HRESULT**.</span></span> <span data-ttu-id="544ce-118">Der Wert S \_ OK gibt an, dass der-Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="544ce-118">A value of S\_OK indicates that the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="544ce-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="544ce-119">Remarks</span></span>

<span data-ttu-id="544ce-120">Verwenden Sie diese Methode, um eine Zertifizierungsstelle für eine Zertifikat Vorlage anzugeben.</span><span class="sxs-lookup"><span data-stu-id="544ce-120">Use this method to specify a CA for a certificate template.</span></span>

## <a name="requirements"></a><span data-ttu-id="544ce-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="544ce-121">Requirements</span></span>



| <span data-ttu-id="544ce-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="544ce-122">Requirement</span></span> | <span data-ttu-id="544ce-123">Wert</span><span class="sxs-lookup"><span data-stu-id="544ce-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="544ce-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="544ce-124">Minimum supported client</span></span><br/> | <span data-ttu-id="544ce-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="544ce-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="544ce-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="544ce-126">Minimum supported server</span></span><br/> | <span data-ttu-id="544ce-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="544ce-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="544ce-128">DLL</span><span class="sxs-lookup"><span data-stu-id="544ce-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="544ce-129"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="544ce-129"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="544ce-130">IID</span><span class="sxs-lookup"><span data-stu-id="544ce-130">IID</span></span><br/>                      | <span data-ttu-id="544ce-131">IID \_ iscrdenr ist definiert als 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="544ce-131">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="544ce-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="544ce-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="544ce-133">**Iscrdenr**</span><span class="sxs-lookup"><span data-stu-id="544ce-133">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="544ce-134">**Iscrdenr:: enumcaname**</span><span class="sxs-lookup"><span data-stu-id="544ce-134">**ISCrdEnr::enumCAName**</span></span>](iscrdenr-enumcaname.md)
</dt> <dt>

[<span data-ttu-id="544ce-135">**Iscrdenr:: getcaname**</span><span class="sxs-lookup"><span data-stu-id="544ce-135">**ISCrdEnr::getCAName**</span></span>](iscrdenr-getcaname.md)
</dt> </dl>

 

 

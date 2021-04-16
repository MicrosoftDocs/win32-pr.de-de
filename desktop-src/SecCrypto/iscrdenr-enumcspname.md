---
description: Listet den Namen der verfügbaren Kryptografiedienstanbieter (CSPs) auf.
ms.assetid: d0dc8a8a-afff-4ccc-96e0-2c52913c3322
title: 'Iscrdenr:: enumcspname-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.enumCSPName
- SCrdEnr.enumCSPName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: e7bba587b56300cd02efd81758288d3b77c65a66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529993"
---
# <a name="iscrdenrenumcspname-method"></a><span data-ttu-id="b2993-103">Iscrdenr:: enumcspname-Methode</span><span class="sxs-lookup"><span data-stu-id="b2993-103">ISCrdEnr::enumCSPName method</span></span>

<span data-ttu-id="b2993-104">Die **enumcspname** -Methode listet den Namen der verfügbaren [*Kryptografiedienstanbieter*](../secgloss/c-gly.md) (CSPs) auf.</span><span class="sxs-lookup"><span data-stu-id="b2993-104">The **enumCSPName** method enumerates the name of the available [*cryptographic service providers*](../secgloss/c-gly.md) (CSPs).</span></span>

## <a name="syntax"></a><span data-ttu-id="b2993-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2993-105">Syntax</span></span>


```C++
HRESULT enumCSPName(
  [in]  DWORD     dwIndex,
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrCSPName
);
```


```VB

SCrdEnr.enumCSPName( _
  ByVal dwIndex, _
  ByVal dwFlags, _
  ByRef pbstrCSPName _
)
```





## <a name="parameters"></a><span data-ttu-id="b2993-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2993-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2993-107">*dwIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b2993-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2993-108">Der null basierte Index für die enumerationssequenz.</span><span class="sxs-lookup"><span data-stu-id="b2993-108">The zero-based index for the enumeration sequence.</span></span>

</dd> <dt>

<span data-ttu-id="b2993-109">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b2993-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2993-110">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="b2993-110">Reserved for future use.</span></span> <span data-ttu-id="b2993-111">Legen Sie diesen Wert auf NULL fest.</span><span class="sxs-lookup"><span data-stu-id="b2993-111">Set this value to zero.</span></span>

</dd> <dt>

<span data-ttu-id="b2993-112">*pbstrincspname* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b2993-112">*pbstrCSPName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2993-113">Ein Zeiger auf eine Zeichenfolge, die den Namen des enumerierten CSP zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="b2993-113">A pointer to a string that returns the name of the enumerated CSP.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2993-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b2993-114">Return value</span></span>

### <a name="c"></a><span data-ttu-id="b2993-115">C++</span><span class="sxs-lookup"><span data-stu-id="b2993-115">C++</span></span>

<span data-ttu-id="b2993-116">Wenn die Methode erfolgreich ausgeführt wird, gibt die Methode S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="b2993-116">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="b2993-117">Wenn die Methode fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="b2993-117">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="b2993-118">Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="b2993-118">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="b2993-119">VB</span><span class="sxs-lookup"><span data-stu-id="b2993-119">VB</span></span>

<span data-ttu-id="b2993-120">Eine Zeichenfolge, die den Namen des enumerierten CSP darstellt.</span><span class="sxs-lookup"><span data-stu-id="b2993-120">A string that represents the name of the enumerated CSP.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2993-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b2993-121">Requirements</span></span>



| <span data-ttu-id="b2993-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b2993-122">Requirement</span></span> | <span data-ttu-id="b2993-123">Wert</span><span class="sxs-lookup"><span data-stu-id="b2993-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2993-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b2993-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b2993-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b2993-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="b2993-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b2993-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b2993-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b2993-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b2993-128">DLL</span><span class="sxs-lookup"><span data-stu-id="b2993-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2993-129"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2993-129"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="b2993-130">IID</span><span class="sxs-lookup"><span data-stu-id="b2993-130">IID</span></span><br/>                      | <span data-ttu-id="b2993-131">IID \_ iscrdenr ist definiert als 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="b2993-131">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="b2993-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b2993-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2993-133">**Iscrdenr**</span><span class="sxs-lookup"><span data-stu-id="b2993-133">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="b2993-134">**Iscrdenr:: cspcount**</span><span class="sxs-lookup"><span data-stu-id="b2993-134">**ISCrdEnr::CSPCount**</span></span>](iscrdenr-cspcount.md)
</dt> <dt>

[<span data-ttu-id="b2993-135">**Iscrdenr:: cspname**</span><span class="sxs-lookup"><span data-stu-id="b2993-135">**ISCrdEnr::CSPName**</span></span>](iscrdenr-cspname.md)
</dt> </dl>

 

 

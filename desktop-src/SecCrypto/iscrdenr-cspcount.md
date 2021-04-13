---
description: Ruft die Anzahl der Kryptografiedienstanbieter (CSPs) ab.
ms.assetid: 7e0c1613-85ad-4f25-837e-d7b0f11e654a
title: 'Iscrdenr:: cspcount-Eigenschaft'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.CSPCount
- ISCrdEnr.get_CSPCount
- SCrdEnr.CSPCount
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: b2aea22db3c804ae4808996002b68efdcb6cf9a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348518"
---
# <a name="iscrdenrcspcount-property"></a><span data-ttu-id="194e6-103">Iscrdenr:: cspcount-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="194e6-103">ISCrdEnr::CSPCount property</span></span>

<span data-ttu-id="194e6-104">Die **cspcount** -Eigenschaft ruft die Anzahl der [*Kryptografiedienstanbieter*](../secgloss/c-gly.md) (CSPs) ab.</span><span class="sxs-lookup"><span data-stu-id="194e6-104">The **CSPCount** property retrieves the number of [*cryptographic service providers*](../secgloss/c-gly.md) (CSPs).</span></span>

<span data-ttu-id="194e6-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="194e6-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="194e6-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="194e6-106">Syntax</span></span>


```C++
HRESULT get_CSPCount(
   LONG *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="194e6-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="194e6-107">Property value</span></span>

<span data-ttu-id="194e6-108">Die Anzahl der CSPs.</span><span class="sxs-lookup"><span data-stu-id="194e6-108">The number of CSPs.</span></span>

## <a name="error-codes"></a><span data-ttu-id="194e6-109">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="194e6-109">Error codes</span></span>

<span data-ttu-id="194e6-110">Wenn die Methode erfolgreich ausgeführt wird, gibt die Methode S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="194e6-110">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="194e6-111">Wenn die Methode fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="194e6-111">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="194e6-112">Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="194e6-112">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="194e6-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="194e6-113">Requirements</span></span>



| <span data-ttu-id="194e6-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="194e6-114">Requirement</span></span> | <span data-ttu-id="194e6-115">Wert</span><span class="sxs-lookup"><span data-stu-id="194e6-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="194e6-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="194e6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="194e6-117">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="194e6-117">None supported</span></span><br/>                                                               |
| <span data-ttu-id="194e6-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="194e6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="194e6-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="194e6-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="194e6-120">DLL</span><span class="sxs-lookup"><span data-stu-id="194e6-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="194e6-121"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="194e6-121"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="194e6-122">IID</span><span class="sxs-lookup"><span data-stu-id="194e6-122">IID</span></span><br/>                      | <span data-ttu-id="194e6-123">IID \_ iscrdenr ist definiert als 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="194e6-123">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="194e6-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="194e6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="194e6-125">**Iscrdenr**</span><span class="sxs-lookup"><span data-stu-id="194e6-125">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="194e6-126">**Iscrdenr:: cspname**</span><span class="sxs-lookup"><span data-stu-id="194e6-126">**ISCrdEnr::CSPName**</span></span>](iscrdenr-cspname.md)
</dt> <dt>

[<span data-ttu-id="194e6-127">**Iscrdenr:: enumcspname**</span><span class="sxs-lookup"><span data-stu-id="194e6-127">**ISCrdEnr::enumCSPName**</span></span>](iscrdenr-enumcspname.md)
</dt> </dl>

 

 

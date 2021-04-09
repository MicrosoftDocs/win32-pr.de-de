---
description: Legt den Namen des Kryptografiedienstanbieters (CSP) fest oder ruft ihn ab.
ms.assetid: 34fde7b0-747d-4592-a89a-207f82369f52
title: 'Iscrdenr:: cspname-Eigenschaft'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.CSPName
- ISCrdEnr.get_CSPName
- ISCrdEnr.put_CSPName
- SCrdEnr.CSPName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 363f2f9120d3b0a202335d0e8e450464cbc1f118
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050430"
---
# <a name="iscrdenrcspname-property"></a><span data-ttu-id="32de2-103">Iscrdenr:: cspname-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="32de2-103">ISCrdEnr::CSPName property</span></span>

<span data-ttu-id="32de2-104">Die **cspname** -Eigenschaft legt den Namen des [*Kryptografiedienstanbieters*](../secgloss/c-gly.md) (CSP) fest oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="32de2-104">The **CSPName** property sets or retrieves the name of the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

<span data-ttu-id="32de2-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="32de2-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="32de2-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="32de2-106">Syntax</span></span>


```C++
HRESULT put_CSPName(
   BSTR newVal
);

HRESULT get_CSPName(
   BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="32de2-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="32de2-107">Property value</span></span>

<span data-ttu-id="32de2-108">Der Name des CSP.</span><span class="sxs-lookup"><span data-stu-id="32de2-108">The name of the CSP.</span></span>

## <a name="error-codes"></a><span data-ttu-id="32de2-109">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="32de2-109">Error codes</span></span>

<span data-ttu-id="32de2-110">Wenn die Methode erfolgreich ausgeführt wird, gibt die Methode S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="32de2-110">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="32de2-111">Wenn die Methode fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="32de2-111">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="32de2-112">Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="32de2-112">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="32de2-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="32de2-113">Remarks</span></span>

<span data-ttu-id="32de2-114">Legen Sie diese Eigenschaft fest, um den Namen des CSP anzugeben, der mit der Smartcard-Registrierungs Steuerung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="32de2-114">Set this property to specify the name of the CSP to use with the Smart Card Enrollment Control.</span></span> <span data-ttu-id="32de2-115">Rufen Sie diese Eigenschaft ab, um den Namen des angegebenen CSP abzurufen.</span><span class="sxs-lookup"><span data-stu-id="32de2-115">Get this property to retrieve the name of the specified CSP.</span></span> <span data-ttu-id="32de2-116">Wenn Sie für diese Eigenschaft keinen Wert angeben, wird die **cspname** -Eigenschaft standardmäßig auf den Vornamen in der Liste verfügbarer CSPs-Objekte festgelegt.</span><span class="sxs-lookup"><span data-stu-id="32de2-116">If you do not specify a value for this property, the **CSPName** property defaults to the first name in the available list of CSPs.</span></span>

## <a name="requirements"></a><span data-ttu-id="32de2-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="32de2-117">Requirements</span></span>



| <span data-ttu-id="32de2-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="32de2-118">Requirement</span></span> | <span data-ttu-id="32de2-119">Wert</span><span class="sxs-lookup"><span data-stu-id="32de2-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="32de2-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="32de2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="32de2-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="32de2-121">None supported</span></span><br/>                                                               |
| <span data-ttu-id="32de2-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="32de2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="32de2-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="32de2-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="32de2-124">DLL</span><span class="sxs-lookup"><span data-stu-id="32de2-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32de2-125"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32de2-125"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="32de2-126">IID</span><span class="sxs-lookup"><span data-stu-id="32de2-126">IID</span></span><br/>                      | <span data-ttu-id="32de2-127">IID \_ iscrdenr ist definiert als 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="32de2-127">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="32de2-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="32de2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32de2-129">**Iscrdenr**</span><span class="sxs-lookup"><span data-stu-id="32de2-129">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="32de2-130">**Iscrdenr:: cspcount**</span><span class="sxs-lookup"><span data-stu-id="32de2-130">**ISCrdEnr::CSPCount**</span></span>](iscrdenr-cspcount.md)
</dt> <dt>

[<span data-ttu-id="32de2-131">**Iscrdenr:: enumcspname**</span><span class="sxs-lookup"><span data-stu-id="32de2-131">**ISCrdEnr::enumCSPName**</span></span>](iscrdenr-enumcspname.md)
</dt> </dl>

 

 

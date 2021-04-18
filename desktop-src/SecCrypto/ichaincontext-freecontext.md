---
description: Gibt einen pccert- \_ Ketten kontextfrei, \_ der über die ChainContext-Eigenschaft abgerufen wurde.
ms.assetid: fa9a6171-58ff-400f-bdcc-ba32a0ae0441
title: 'Ichaincontext:: freecontext-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChainContext.FreeContext
- ChainContext.FreeContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 413b119f250bfbd061301391fee7741362979f65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368578"
---
# <a name="ichaincontextfreecontext-method"></a><span data-ttu-id="2fe59-103">Ichaincontext:: freecontext-Methode</span><span class="sxs-lookup"><span data-stu-id="2fe59-103">IChainContext::FreeContext method</span></span>

<span data-ttu-id="2fe59-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="2fe59-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="2fe59-105">Die **freecontext** -Methode gibt einen pccert- \_ Ketten kontextfrei, \_ der über die [**chainContext**](ichaincontext-chaincontext.md) -Eigenschaft abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="2fe59-105">The **FreeContext** method releases a PCCERT\_CHAIN\_CONTEXT acquired through the [**ChainContext**](ichaincontext-chaincontext.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fe59-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="2fe59-106">Syntax</span></span>


```VB
ChainContext.FreeContext()
```



## <a name="parameters"></a><span data-ttu-id="2fe59-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="2fe59-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fe59-108">*pchaincontext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2fe59-108">*pChainContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fe59-109">Der zu veröffentlichende pccert- \_ Ketten \_ Kontext.</span><span class="sxs-lookup"><span data-stu-id="2fe59-109">The PCCERT\_CHAIN\_CONTEXT to be released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fe59-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2fe59-110">Return value</span></span>

<span data-ttu-id="2fe59-111">Der Rückgabewert ist ein **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="2fe59-111">The return value is an **HRESULT**.</span></span> <span data-ttu-id="2fe59-112">Der Wert S \_ OK weist auf Erfolg hin.</span><span class="sxs-lookup"><span data-stu-id="2fe59-112">A value of S\_OK indicates success.</span></span> <span data-ttu-id="2fe59-113">Jeder andere Wert gibt an, dass der Vorgang fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="2fe59-113">Any other value indicates that the operation failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="2fe59-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2fe59-114">Remarks</span></span>

<span data-ttu-id="2fe59-115">Diese Methode gibt nicht den \_ \_ in einem [**Ketten**](chain.md) Objekt enthaltenen pccert-Ketten kontextfrei.</span><span class="sxs-lookup"><span data-stu-id="2fe59-115">This method does not release the PCCERT\_CHAIN\_CONTEXT contained within a [**Chain**](chain.md) object.</span></span> <span data-ttu-id="2fe59-116">Es sollte nur verwendet werden, um einen mit \_ \_ der [**chainContext**](ichaincontext-chaincontext.md) -Eigenschaft erworbenen pccert-Ketten kontextfrei zugeben.</span><span class="sxs-lookup"><span data-stu-id="2fe59-116">It should be used only to release a PCCERT\_CHAIN\_CONTEXT acquired through the [**ChainContext**](ichaincontext-chaincontext.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fe59-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2fe59-117">Requirements</span></span>



| <span data-ttu-id="2fe59-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2fe59-118">Requirement</span></span> | <span data-ttu-id="2fe59-119">Wert</span><span class="sxs-lookup"><span data-stu-id="2fe59-119">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2fe59-120">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="2fe59-120">Redistributable</span></span><br/> | <span data-ttu-id="2fe59-121">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="2fe59-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="2fe59-122">DLL</span><span class="sxs-lookup"><span data-stu-id="2fe59-122">DLL</span></span><br/>             | <dl> <span data-ttu-id="2fe59-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2fe59-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fe59-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2fe59-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fe59-125">**Ichaincontext**</span><span class="sxs-lookup"><span data-stu-id="2fe59-125">**IChainContext**</span></span>](ichaincontext.md)
</dt> </dl>

 

 





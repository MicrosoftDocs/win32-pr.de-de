---
description: Ruft ggf. den Transaktions-oder Transaktions Proxy ab, der dem aktuellen Kontext zugeordnet ist.
ms.assetid: 2f85f395-3ec5-4c5a-a6db-c902cb8f8486
title: 'Icontexttransaktioninfo:: fetchtransaction-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo.FetchTransaction
api_type:
- COM
api_location: ''
ms.openlocfilehash: 0e753974f93539f051465f13a1ea92d7e0e3bfa1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127032"
---
# <a name="icontexttransactioninfofetchtransaction-method"></a><span data-ttu-id="8f1e0-103">Icontexttransaktioninfo:: fetchtransaction-Methode</span><span class="sxs-lookup"><span data-stu-id="8f1e0-103">IContextTransactionInfo::FetchTransaction method</span></span>

<span data-ttu-id="8f1e0-104">Ruft ggf. den Transaktions-oder Transaktions Proxy ab, der dem aktuellen Kontext zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="8f1e0-104">Retrieves the transaction or transaction proxy that is associated with the current context, if any.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f1e0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f1e0-105">Syntax</span></span>


```C++
HRESULT FetchTransaction(
  [out, retval] IUnknown **pUnk
);
```



## <a name="parameters"></a><span data-ttu-id="8f1e0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f1e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f1e0-107">*Punk* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="8f1e0-107">*pUnk* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="8f1e0-108">Der Transaktions-oder Transaktions Proxy, der dem aktuellen Kontext zugeordnet ist. andernfalls **null**.</span><span class="sxs-lookup"><span data-stu-id="8f1e0-108">The transaction or transaction proxy that is associated with the current context; otherwise, **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f1e0-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8f1e0-109">Return value</span></span>

<span data-ttu-id="8f1e0-110">Diese Methode kann die Standard Rückgabewerte e \_ invalidArg, e \_ oudef Memory, e \_ unerwartet und S OK zurückgeben \_ .</span><span class="sxs-lookup"><span data-stu-id="8f1e0-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f1e0-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8f1e0-111">Requirements</span></span>



| <span data-ttu-id="8f1e0-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8f1e0-112">Requirement</span></span> | <span data-ttu-id="8f1e0-113">Wert</span><span class="sxs-lookup"><span data-stu-id="8f1e0-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="8f1e0-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8f1e0-114">Minimum supported client</span></span><br/> | <span data-ttu-id="8f1e0-115">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8f1e0-115">Windows XP with SP2 \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="8f1e0-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8f1e0-116">Minimum supported server</span></span><br/> | <span data-ttu-id="8f1e0-117">Windows Server 2003 mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8f1e0-117">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8f1e0-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8f1e0-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f1e0-119">**Icontexttransaktioninfo**</span><span class="sxs-lookup"><span data-stu-id="8f1e0-119">**IContextTransactionInfo**</span></span>](icontexttransactioninfo.md)
</dt> </dl>

 

 





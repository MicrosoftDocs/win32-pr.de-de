---
description: Ruft die Isolationsstufe und den Timeout Wert einer Transaktion ab, die im Stamm Transaktionskontext gehostet wird.
ms.assetid: bb3ff03e-e69e-4a50-af36-4938eb4323df
title: 'Icontexttransaktioninfo:: gettxisolationlevelandtimeout-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo.GetTxIsolationLevelAndTimeout
api_type:
- COM
api_location: ''
ms.openlocfilehash: b8545a697e672af7206a69ffa19618d5b70e055c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344847"
---
# <a name="icontexttransactioninfogettxisolationlevelandtimeout-method"></a><span data-ttu-id="5426a-103">Icontexttransaktioninfo:: gettxisolationlevelandtimeout-Methode</span><span class="sxs-lookup"><span data-stu-id="5426a-103">IContextTransactionInfo::GetTxIsolationLevelAndTimeout method</span></span>

<span data-ttu-id="5426a-104">Ruft die Isolationsstufe und den Timeout Wert einer Transaktion ab, die im Stamm Transaktionskontext gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="5426a-104">Retrieves the isolation level and timeout value of a transaction that is hosted in the root transaction context.</span></span>

## <a name="syntax"></a><span data-ttu-id="5426a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5426a-105">Syntax</span></span>


```C++
HRESULT GetTxIsolationLevelAndTimeout(
  [out] ISOLEVEL *pIsoLevel,
  [out] DWORD    *dwTime
);
```



## <a name="parameters"></a><span data-ttu-id="5426a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5426a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5426a-107">*pisolevel* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5426a-107">*pIsoLevel* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5426a-108">Der [IsolationLevel](/previous-versions/windows/desktop/ms679234(v=vs.85)) -Wert für die Transaktion.</span><span class="sxs-lookup"><span data-stu-id="5426a-108">The [ISOLATIONLEVEL](/previous-versions/windows/desktop/ms679234(v=vs.85)) value for the transaction.</span></span>

</dd> <dt>

<span data-ttu-id="5426a-109">*dwTime* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5426a-109">*dwTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5426a-110">Das Timeout der Transaktion in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="5426a-110">The timeout of the transaction, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5426a-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5426a-111">Return value</span></span>

<span data-ttu-id="5426a-112">Diese Methode kann die Standard Rückgabewerte e \_ invalidArg, e \_ oudef Memory, e \_ unerwartet und S OK zurückgeben \_ .</span><span class="sxs-lookup"><span data-stu-id="5426a-112">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="5426a-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5426a-113">Requirements</span></span>



| <span data-ttu-id="5426a-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5426a-114">Requirement</span></span> | <span data-ttu-id="5426a-115">Wert</span><span class="sxs-lookup"><span data-stu-id="5426a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="5426a-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5426a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5426a-117">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5426a-117">Windows XP with SP2 \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="5426a-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5426a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5426a-119">Windows Server 2003 mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5426a-119">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5426a-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5426a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5426a-121">**Icontexttransaktioninfo**</span><span class="sxs-lookup"><span data-stu-id="5426a-121">**IContextTransactionInfo**</span></span>](icontexttransactioninfo.md)
</dt> </dl>

 


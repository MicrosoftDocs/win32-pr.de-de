---
description: Ordnet eine itransaktionproxy-Implementierung dem aktuellen Kontext zu.
ms.assetid: 64009632-b536-41fb-95ac-b23e2cbf18da
title: 'Icontexttransaktioninfo:: registertransaktionproxy-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo.RegisterTransactionProxy
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7b559453b0d4ed75f92f7a421be4c3a47e07fdf7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342389"
---
# <a name="icontexttransactioninforegistertransactionproxy-method"></a><span data-ttu-id="7b9c7-103">Icontexttransaktioninfo:: registertransaktionproxy-Methode</span><span class="sxs-lookup"><span data-stu-id="7b9c7-103">IContextTransactionInfo::RegisterTransactionProxy method</span></span>

<span data-ttu-id="7b9c7-104">Ordnet eine [**itransaktionproxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) -Implementierung dem aktuellen Kontext zu.</span><span class="sxs-lookup"><span data-stu-id="7b9c7-104">Associates an [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) implementation with the current context.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b9c7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b9c7-105">Syntax</span></span>


```C++
HRESULT RegisterTransactionProxy(
  [in]  ITransactionProxy *pProxy,
  [out] GUID              *pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="7b9c7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b9c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b9c7-107">*pproxy* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b9c7-107">*pProxy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b9c7-108">Eine [**itransaktionproxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) -Implementierung, die dem aktuellen Kontext zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7b9c7-108">An [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) implementation to associate with the current context.</span></span>

</dd> <dt>

<span data-ttu-id="7b9c7-109">*pguid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7b9c7-109">*pGuid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7b9c7-110">Eine GUID zum Identifizieren des Transaktions Proxys.</span><span class="sxs-lookup"><span data-stu-id="7b9c7-110">A GUID that identifies the transaction proxy.</span></span> <span data-ttu-id="7b9c7-111">Com+ verwendet diese GUID beim Aufrufen von [**itransaktionproxy:: Commit**](/windows/desktop/api/ComSvcs/nf-comsvcs-itransactionproxy-commit) für den Transaktions Proxy.</span><span class="sxs-lookup"><span data-stu-id="7b9c7-111">COM+ uses this GUID when calling [**ITransactionProxy::Commit**](/windows/desktop/api/ComSvcs/nf-comsvcs-itransactionproxy-commit) on the transaction proxy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b9c7-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7b9c7-112">Return value</span></span>

<span data-ttu-id="7b9c7-113">Diese Methode kann die Standard Rückgabewerte e \_ invalidArg, e \_ oudef Memory und e sowie \_ die folgenden Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="7b9c7-113">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, and E\_UNEXPECTED, as well as the following values.</span></span>



| <span data-ttu-id="7b9c7-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="7b9c7-114">Return code</span></span>                                                                                                     | <span data-ttu-id="7b9c7-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7b9c7-115">Description</span></span>                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7b9c7-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7b9c7-116"><dt>**S\_OK**</dt></span></span> </dl>                            | <span data-ttu-id="7b9c7-117">Die Methode wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="7b9c7-117">The method completed successfully.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="7b9c7-118"><dt>**Kontext \_ E \_ alleseryintransaction**</dt></span><span class="sxs-lookup"><span data-stu-id="7b9c7-118"><dt>**CONTEXT\_E\_ALREADYINTRANSACTION**</dt></span></span> </dl> | <span data-ttu-id="7b9c7-119">Dem aktuellen Kontext ist bereits eine [**itransaktionproxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) -Implementierung zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="7b9c7-119">The current context already has an associated [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) implementation.</span></span><br/> |
| <dl> <span data-ttu-id="7b9c7-120"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="7b9c7-120"><dt>**E\_NOTIMPL**</dt></span></span> </dl>                       | <span data-ttu-id="7b9c7-121">Der aktuelle Kontext gehostet eine Bring Your Own Transaction (BYOT)-Transaktion oder eine nicht-root-Transaktion.</span><span class="sxs-lookup"><span data-stu-id="7b9c7-121">The current context is hosting a Bring Your Own Transaction (BYOT) transaction or a non-root transaction.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="7b9c7-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7b9c7-122">Remarks</span></span>

<span data-ttu-id="7b9c7-123">Die **registertransaktionproxy** -Methode kann nur aufgerufen werden, wenn der aktuelle Kontext ein Stamm Transaktionskontext ist.</span><span class="sxs-lookup"><span data-stu-id="7b9c7-123">The **RegisterTransactionProxy** method can only be called if the current context is a root transaction context.</span></span> <span data-ttu-id="7b9c7-124">Er kann nicht aufgerufen werden, wenn der Kontext eine BYOT-Transaktion oder eine nicht-root-Transaktion gehostet.</span><span class="sxs-lookup"><span data-stu-id="7b9c7-124">It cannot be called if the context is hosting a BYOT transaction or a non-root transaction.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b9c7-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7b9c7-125">Requirements</span></span>



| <span data-ttu-id="7b9c7-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7b9c7-126">Requirement</span></span> | <span data-ttu-id="7b9c7-127">Wert</span><span class="sxs-lookup"><span data-stu-id="7b9c7-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="7b9c7-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7b9c7-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7b9c7-129">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7b9c7-129">Windows XP with SP2 \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="7b9c7-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7b9c7-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7b9c7-131">Windows Server 2003 mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7b9c7-131">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7b9c7-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b9c7-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b9c7-133">**Icontexttransaktioninfo**</span><span class="sxs-lookup"><span data-stu-id="7b9c7-133">**IContextTransactionInfo**</span></span>](icontexttransactioninfo.md)
</dt> </dl>

 

 





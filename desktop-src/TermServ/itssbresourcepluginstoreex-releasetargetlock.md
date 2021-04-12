---
title: Itssbresourcepluginstoreex releasetargetlock-Methode
description: Gibt eine Sperre für ein Ziel frei.
ms.assetid: ab2ae9f3-2d38-4b31-9889-58297c574bd4
ms.tgt_platform: multiple
keywords:
- Releasetargetlock-Methode Remotedesktopdienste
- Releasetargetlock-Methode Remotedesktopdienste, itssbresourcepluginstoreex-Schnittstelle
- Itssbresourcepluginstoreex-Schnittstelle Remotedesktopdienste, releasetargetlock-Methode
topic_type:
- apiref
api_name:
- ITsSbResourcePluginStoreEx.ReleaseTargetLock
api_location:
- SbTsV.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fbc34bdb27e40316ea1271bf0faa5d8c6b0abfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104300"
---
# <a name="itssbresourcepluginstoreexreleasetargetlock-method"></a><span data-ttu-id="9e5eb-106">Itssbresourcepluginstoreex:: releasetargetlock-Methode</span><span class="sxs-lookup"><span data-stu-id="9e5eb-106">ITsSbResourcePluginStoreEx::ReleaseTargetLock method</span></span>

<span data-ttu-id="9e5eb-107">Gibt eine Sperre für ein Ziel frei.</span><span class="sxs-lookup"><span data-stu-id="9e5eb-107">Releases a lock on a target.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e5eb-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e5eb-108">Syntax</span></span>


```C++
HRESULT ReleaseTargetLock(
  [in] IUnknown *pContext
);
```



## <a name="parameters"></a><span data-ttu-id="9e5eb-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e5eb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e5eb-110">*pContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9e5eb-110">*pContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e5eb-111">Ein Zeiger auf den Kontext, der von der [**acquiretargetlock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock) -Methode zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9e5eb-111">A pointer to the context returned by the [**AcquireTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e5eb-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9e5eb-112">Return value</span></span>

<span data-ttu-id="9e5eb-113">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="9e5eb-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9e5eb-114">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9e5eb-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e5eb-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9e5eb-115">Remarks</span></span>

<span data-ttu-id="9e5eb-116">Diese Methode ist nur unter Windows Server 2012 R2 mit installiertem [KB3091411](https://support.microsoft.com/kb/3091411) in der [**itssbresourcepluginstoreex**](itssbresourcepluginstoreex.md) -Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9e5eb-116">This method is only available on Windows Server 2012 R2 with [KB3091411](https://support.microsoft.com/kb/3091411) installed in the [**ITsSbResourcePluginStoreEx**](itssbresourcepluginstoreex.md) interface.</span></span> <span data-ttu-id="9e5eb-117">Diese Methode ist in der [**itssbresourcepluginstore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) -Schnittstelle ab Windows Server 2016 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9e5eb-117">This method is available on the [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) interface starting with Windows Server 2016.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e5eb-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9e5eb-118">Requirements</span></span>



| <span data-ttu-id="9e5eb-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9e5eb-119">Requirement</span></span> | <span data-ttu-id="9e5eb-120">Wert</span><span class="sxs-lookup"><span data-stu-id="9e5eb-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e5eb-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9e5eb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9e5eb-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9e5eb-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="9e5eb-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9e5eb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9e5eb-124">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="9e5eb-124">Windows Server 2012 R2</span></span><br/>                                                             |
| <span data-ttu-id="9e5eb-125">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="9e5eb-125">End of server support</span></span><br/>    | <span data-ttu-id="9e5eb-126">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="9e5eb-126">Windows Server 2012 R2</span></span><br/>                                                             |
| <span data-ttu-id="9e5eb-127">IDL</span><span class="sxs-lookup"><span data-stu-id="9e5eb-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9e5eb-128"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9e5eb-128"><dt>SbTsV.idl</dt></span></span> </dl>          |
| <span data-ttu-id="9e5eb-129">IID</span><span class="sxs-lookup"><span data-stu-id="9e5eb-129">IID</span></span><br/>                      | <span data-ttu-id="9e5eb-130">IID \_ itssbresourcepluginstoreex ist als 80b83ffd-625d-11e5-bea1-a0481c7e9064 definiert</span><span class="sxs-lookup"><span data-stu-id="9e5eb-130">IID\_ITsSbResourcePluginStoreEx is defined as 80b83ffd-625d-11e5-bea1-a0481c7e9064</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9e5eb-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9e5eb-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e5eb-132">**Itssbresourcepluginstoreex**</span><span class="sxs-lookup"><span data-stu-id="9e5eb-132">**ITsSbResourcePluginStoreEx**</span></span>](itssbresourcepluginstoreex.md)
</dt> </dl>

 

 






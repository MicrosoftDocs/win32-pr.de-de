---
title: Ienumf siitems RemoteNext-Methode
description: Unterstützt einen Remote Client, der eine angegebene Anzahl von Elementen in der enumerationssequenz abrufen möchte. | Ienumf siitems RemoteNext-Methode
ms.assetid: a5ae59ed-08d7-4225-9aec-91049789e8fe
keywords:
- RemoteNext-Methode IMAPI
- RemoteNext-Methode IMAPI, ienumssiitems-Schnittstelle
- Ienumf siitems Interface IMAPI, RemoteNext-Methode
topic_type:
- apiref
api_name:
- IEnumFsiItems.RemoteNext
api_location:
- Imapi2fs.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e29d3f75cd8e2f83fcd21236661d0d1fa0dabef
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104530713"
---
# <a name="ienumfsiitemsremotenext-method"></a><span data-ttu-id="cecf1-107">Ienumf siitems:: RemoteNext-Methode</span><span class="sxs-lookup"><span data-stu-id="cecf1-107">IEnumFsiItems::RemoteNext method</span></span>

<span data-ttu-id="cecf1-108">Unterstützt einen Remote Client, der eine angegebene Anzahl von Elementen in der enumerationssequenz abrufen möchte.</span><span class="sxs-lookup"><span data-stu-id="cecf1-108">Supports a remote client that wants to retrieve a specified number of items in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="cecf1-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="cecf1-109">Syntax</span></span>


```C++
HRESULT RemoteNext(
  [in]  ULONG    celt,
  [out] IFsiItem **rgelt,
  [out] ULONG    *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="cecf1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="cecf1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cecf1-111">*celt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cecf1-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cecf1-112">Anzahl der abzurufenden Elemente.</span><span class="sxs-lookup"><span data-stu-id="cecf1-112">Number of items to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="cecf1-113">*rgelt* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="cecf1-113">*rgelt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cecf1-114">Array von [**ifsiitem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem) -Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="cecf1-114">Array of [**IFsiItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem) interfaces.</span></span> <span data-ttu-id="cecf1-115">Wenn Sie den Vorgang abgeschlossen haben, müssen Sie jede Schnittstelle in rgelt freigeben</span><span class="sxs-lookup"><span data-stu-id="cecf1-115">You must release each interface in rgelt when done.</span></span>

</dd> <dt>

<span data-ttu-id="cecf1-116">*pceltfetch* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="cecf1-116">*pceltFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cecf1-117">Anzahl der Elemente, die in rgelt zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="cecf1-117">Number of elements returned in rgelt.</span></span> <span data-ttu-id="cecf1-118">Sie können *pceltfetch* auf **null** festlegen, wenn es sich um ein *celt* handelt.</span><span class="sxs-lookup"><span data-stu-id="cecf1-118">You can set *pceltFetched* to **NULL** if *celt* is one.</span></span> <span data-ttu-id="cecf1-119">Initialisieren Sie andernfalls den Wert von *pceltfetch* auf 0, bevor Sie diese Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="cecf1-119">Otherwise, initialize the value of *pceltFetched* to 0 before calling this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cecf1-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cecf1-120">Return value</span></span>

<span data-ttu-id="cecf1-121">S \_ OK wird zurückgegeben, wenn die Anzahl der angeforderten Elemente (*celt*) erfolgreich zurückgegeben wurde oder wenn die Anzahl der zurückgegebenen Elemente (*pceltfetch*) kleiner als die Anzahl der angeforderten Elemente ist.</span><span class="sxs-lookup"><span data-stu-id="cecf1-121">S\_OK is returned when the number of requested elements (*celt*) are returned successfully or the number of returned items (*pceltFetched*) is less than the number of requested elements.</span></span>

<span data-ttu-id="cecf1-122">Andere Erfolgs Codes können als Ergebnis der-Implementierung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="cecf1-122">Other success codes may be returned as a result of implementation.</span></span> <span data-ttu-id="cecf1-123">Die folgenden Fehlercodes werden häufig bei einem Vorgangs Fehler zurückgegeben. Sie stellen jedoch nicht die einzigen möglichen Fehler Werte dar:</span><span class="sxs-lookup"><span data-stu-id="cecf1-123">The following error codes are commonly returned on operation failure, but do not represent the only possible error values:</span></span>



| <span data-ttu-id="cecf1-124">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="cecf1-124">Return code</span></span>                                                                                   | <span data-ttu-id="cecf1-125">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cecf1-125">Description</span></span>                                                                     |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cecf1-126"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="cecf1-126"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="cecf1-127">Der Zeiger ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="cecf1-127">Pointer is not valid.</span></span><br/> <span data-ttu-id="cecf1-128">Wert: 0x80004003</span><span class="sxs-lookup"><span data-stu-id="cecf1-128">Value: 0x80004003</span></span><br/>                   |
| <dl> <span data-ttu-id="cecf1-129"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="cecf1-129"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="cecf1-130">Der erforderliche Arbeitsspeicher konnte nicht belegt werden.</span><span class="sxs-lookup"><span data-stu-id="cecf1-130">Failed to allocate the required memory.</span></span><br/> <span data-ttu-id="cecf1-131">Wert: 0x8007000E</span><span class="sxs-lookup"><span data-stu-id="cecf1-131">Value: 0x8007000E</span></span><br/> |
| <dl> <span data-ttu-id="cecf1-132"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="cecf1-132"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="cecf1-133">Mindestens ein Argument ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="cecf1-133">One or more arguments are not valid.</span></span><br/> <span data-ttu-id="cecf1-134">Wert: 0x80070057</span><span class="sxs-lookup"><span data-stu-id="cecf1-134">Value: 0x80070057</span></span><br/>    |



 

## <a name="requirements"></a><span data-ttu-id="cecf1-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cecf1-135">Requirements</span></span>



| <span data-ttu-id="cecf1-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cecf1-136">Requirement</span></span> | <span data-ttu-id="cecf1-137">Wert</span><span class="sxs-lookup"><span data-stu-id="cecf1-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cecf1-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cecf1-138">Minimum supported client</span></span><br/> | <span data-ttu-id="cecf1-139">Windows Vista, Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cecf1-139">Windows Vista, Windows XP with SP2 \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="cecf1-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cecf1-140">Minimum supported server</span></span><br/> | <span data-ttu-id="cecf1-141">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cecf1-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cecf1-142">IDL</span><span class="sxs-lookup"><span data-stu-id="cecf1-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cecf1-143"><dt>Imapi2fs. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cecf1-143"><dt>Imapi2fs.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cecf1-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cecf1-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cecf1-145">**Ienumssiitems**</span><span class="sxs-lookup"><span data-stu-id="cecf1-145">**IEnumFsiItems**</span></span>](/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumfsiitems)
</dt> <dt>

[<span data-ttu-id="cecf1-146">Ienumssiitems:: Next</span><span class="sxs-lookup"><span data-stu-id="cecf1-146">IEnumFsiItems::Next</span></span>](/windows/desktop/api/imapi2fs/nf-imapi2fs-ienumfsiitems-next)
</dt> </dl>

 

 






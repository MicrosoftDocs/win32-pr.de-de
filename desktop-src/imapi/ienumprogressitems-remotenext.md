---
title: Ienumprogressitems RemoteNext-Methode
description: Unterstützt einen Remote Client, der eine angegebene Anzahl von Elementen in der enumerationssequenz abrufen möchte. | Ienumprogressitems RemoteNext-Methode
ms.assetid: c5f85ca3-1bad-49fd-9e67-d41135cd837d
keywords:
- RemoteNext-Methode IMAPI
- RemoteNext-Methode IMAPI, ienumprogressitems-Schnittstelle
- Ienumprogressitems Interface IMAPI, RemoteNext-Methode
topic_type:
- apiref
api_name:
- IEnumProgressItems.RemoteNext
api_location:
- Imapi2fs.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a088a1be640c6653a8a8ccd8b00cf21bd027ecd7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106354321"
---
# <a name="ienumprogressitemsremotenext-method"></a><span data-ttu-id="d481b-107">Ienumprogressitems:: RemoteNext-Methode</span><span class="sxs-lookup"><span data-stu-id="d481b-107">IEnumProgressItems::RemoteNext method</span></span>

<span data-ttu-id="d481b-108">Unterstützt einen Remote Client, der eine angegebene Anzahl von Elementen in der enumerationssequenz abrufen möchte</span><span class="sxs-lookup"><span data-stu-id="d481b-108">Supports a remote client that wants to retrieve a specified number of items in the enumeration sequence</span></span>

## <a name="syntax"></a><span data-ttu-id="d481b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="d481b-109">Syntax</span></span>


```C++
HRESULT RemoteNext(
  [in]  ULONG         celt,
  [out] IProgressItem **rgelt,
  [out] ULONG         *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="d481b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d481b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d481b-111">*celt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d481b-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d481b-112">Anzahl der abzurufenden Elemente.</span><span class="sxs-lookup"><span data-stu-id="d481b-112">Number of items to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="d481b-113">*rgelt* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d481b-113">*rgelt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d481b-114">Array von [**iprogressitem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem) -Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="d481b-114">Array of [**IProgressItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem) interfaces.</span></span> <span data-ttu-id="d481b-115">Wenn Sie den Vorgang abgeschlossen haben, müssen Sie jede Schnittstelle in rgelt freigeben</span><span class="sxs-lookup"><span data-stu-id="d481b-115">You must release each interface in rgelt when done.</span></span>

</dd> <dt>

<span data-ttu-id="d481b-116">*pceltfetch* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d481b-116">*pceltFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d481b-117">Anzahl der Elemente, die in rgelt zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d481b-117">Number of elements returned in rgelt.</span></span> <span data-ttu-id="d481b-118">Sie können *pceltfetch* auf **null** festlegen, wenn es sich um ein *celt* handelt.</span><span class="sxs-lookup"><span data-stu-id="d481b-118">You can set *pceltFetched* to **NULL** if *celt* is one.</span></span> <span data-ttu-id="d481b-119">Initialisieren Sie andernfalls den Wert von *pceltfetch* auf 0, bevor Sie diese Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d481b-119">Otherwise, initialize the value of *pceltFetched* to 0 before calling this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d481b-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d481b-120">Return value</span></span>

<span data-ttu-id="d481b-121">S \_ OK wird zurückgegeben, wenn die Anzahl der angeforderten Elemente (*celt*) erfolgreich zurückgegeben wurde oder wenn die Anzahl der zurückgegebenen Elemente (*pceltfetch*) kleiner als die Anzahl der angeforderten Elemente ist.</span><span class="sxs-lookup"><span data-stu-id="d481b-121">S\_OK is returned when the number of requested elements (*celt*) are returned successfully or the number of returned items (*pceltFetched*) is less than the number of requested elements.</span></span>

<span data-ttu-id="d481b-122">Andere Erfolgs Codes können als Ergebnis der-Implementierung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d481b-122">Other success codes may be returned as a result of implementation.</span></span> <span data-ttu-id="d481b-123">Die folgenden Fehlercodes werden häufig bei einem Vorgangs Fehler zurückgegeben. Sie stellen jedoch nicht die einzigen möglichen Fehler Werte dar:</span><span class="sxs-lookup"><span data-stu-id="d481b-123">The following error codes are commonly returned on operation failure, but do not represent the only possible error values:</span></span>



| <span data-ttu-id="d481b-124">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="d481b-124">Return code</span></span>                                                                                   | <span data-ttu-id="d481b-125">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d481b-125">Description</span></span>                                                                     |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d481b-126"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="d481b-126"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="d481b-127">Der Zeiger ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="d481b-127">Pointer is not valid.</span></span><br/> <span data-ttu-id="d481b-128">Wert: 0x80004003</span><span class="sxs-lookup"><span data-stu-id="d481b-128">Value: 0x80004003</span></span><br/>                   |
| <dl> <span data-ttu-id="d481b-129"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="d481b-129"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d481b-130">Der erforderliche Arbeitsspeicher konnte nicht belegt werden.</span><span class="sxs-lookup"><span data-stu-id="d481b-130">Failed to allocate the required memory.</span></span><br/> <span data-ttu-id="d481b-131">Wert: 0x8007000E</span><span class="sxs-lookup"><span data-stu-id="d481b-131">Value: 0x8007000E</span></span><br/> |
| <dl> <span data-ttu-id="d481b-132"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="d481b-132"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="d481b-133">Mindestens ein Argument ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="d481b-133">One or more arguments are not valid.</span></span><br/> <span data-ttu-id="d481b-134">Wert: 0x80070057</span><span class="sxs-lookup"><span data-stu-id="d481b-134">Value: 0x80070057</span></span><br/>    |
| <dl> <span data-ttu-id="d481b-135"><dt>**E \_ Unerwartete**</dt></span><span class="sxs-lookup"><span data-stu-id="d481b-135"><dt> **E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="d481b-136">Unerwarteter Fehler.</span><span class="sxs-lookup"><span data-stu-id="d481b-136">An unexpected failure occurred.</span></span><br/> <span data-ttu-id="d481b-137">Wert: 0x8000ffff</span><span class="sxs-lookup"><span data-stu-id="d481b-137">Value: 0x8000FFFF</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="d481b-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d481b-138">Remarks</span></span>

<span data-ttu-id="d481b-139">Wenn weniger als die angeforderte Anzahl von Elementen in der Sequenz vorhanden sind, werden die restlichen Elemente abgerufen.</span><span class="sxs-lookup"><span data-stu-id="d481b-139">If there are fewer than the requested number of elements left in the sequence, it retrieves the remaining elements.</span></span>

## <a name="requirements"></a><span data-ttu-id="d481b-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d481b-140">Requirements</span></span>



| <span data-ttu-id="d481b-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d481b-141">Requirement</span></span> | <span data-ttu-id="d481b-142">Wert</span><span class="sxs-lookup"><span data-stu-id="d481b-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d481b-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d481b-143">Minimum supported client</span></span><br/> | <span data-ttu-id="d481b-144">Windows Vista, Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d481b-144">Windows Vista, Windows XP with SP2 \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="d481b-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d481b-145">Minimum supported server</span></span><br/> | <span data-ttu-id="d481b-146">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d481b-146">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d481b-147">IDL</span><span class="sxs-lookup"><span data-stu-id="d481b-147">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d481b-148"><dt>Imapi2fs. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d481b-148"><dt>Imapi2fs.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d481b-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d481b-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d481b-150">**Ienumprogressitems**</span><span class="sxs-lookup"><span data-stu-id="d481b-150">**IEnumProgressItems**</span></span>](/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumprogressitems)
</dt> <dt>

[<span data-ttu-id="d481b-151">Ienumprogressitems:: Next</span><span class="sxs-lookup"><span data-stu-id="d481b-151">IEnumProgressItems::Next</span></span>](/windows/desktop/api/imapi2fs/nf-imapi2fs-ienumprogressitems-next)
</dt> </dl>

 

 






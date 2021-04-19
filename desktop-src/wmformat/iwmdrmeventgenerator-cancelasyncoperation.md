---
title: Iwmdrmeventgenerator cancelasyncoperation-Methode (wmdrmsdk. h)
description: Die cancelasyncoperation-Methode bricht einen asynchronen Vorgang ab.
ms.assetid: 95c59e03-b6c8-40c2-b1dc-381cb6d8d558
keywords:
- Cancelasyncoperation-Methode, Windows Media-Format
- Cancelasyncoperation-Methode, Windows Media-Format, iwmdrmeventgenerator-Schnittstelle
- Iwmdrmeventgenerator-Schnittstelle Windows Media-Format, cancelasyncoperation-Methode
topic_type:
- apiref
api_name:
- IWMDRMEventGenerator.CancelAsyncOperation
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1223f56e820eb5927eeb972f28056baa14824774
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367044"
---
# <a name="iwmdrmeventgeneratorcancelasyncoperation-method"></a><span data-ttu-id="34652-106">Iwmdrmeventgenerator:: cancelasyncoperation-Methode</span><span class="sxs-lookup"><span data-stu-id="34652-106">IWMDRMEventGenerator::CancelAsyncOperation method</span></span>

<span data-ttu-id="34652-107">Die **cancelasyncoperation** -Methode bricht einen asynchronen Vorgang ab.</span><span class="sxs-lookup"><span data-stu-id="34652-107">The **CancelAsyncOperation** method cancels an asynchronous operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="34652-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="34652-108">Syntax</span></span>


```C++
HRESULT CancelAsyncOperation(
  [in] IUnknown *punkCancelationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="34652-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="34652-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34652-110">*punkcancelationcookie* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="34652-110">*punkCancelationCookie* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34652-111">Zeiger auf das Abbruch Cookie, das den asynchronen Vorgang identifiziert, der abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="34652-111">Pointer to the cancellation cookie that identifies the asynchronous operation to be canceled.</span></span> <span data-ttu-id="34652-112">Dieses Cookie wird von der-Methode bereitgestellt, mit der der Vorgang gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="34652-112">This cookie is provided by the method used to start the operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34652-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="34652-113">Return value</span></span>

<span data-ttu-id="34652-114">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="34652-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="34652-115">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="34652-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="34652-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="34652-116">Return code</span></span>                                                                          | <span data-ttu-id="34652-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="34652-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="34652-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="34652-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="34652-119">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="34652-119">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="34652-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="34652-120">Remarks</span></span>

<span data-ttu-id="34652-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="34652-121">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="34652-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="34652-122">Requirements</span></span>



| <span data-ttu-id="34652-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="34652-123">Requirement</span></span> | <span data-ttu-id="34652-124">Wert</span><span class="sxs-lookup"><span data-stu-id="34652-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="34652-125">Header</span><span class="sxs-lookup"><span data-stu-id="34652-125">Header</span></span><br/>  | <dl> <span data-ttu-id="34652-126"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="34652-126"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="34652-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="34652-127">Library</span></span><br/> | <dl> <span data-ttu-id="34652-128"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="34652-128"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34652-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="34652-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34652-130">**Iwmdrmeventgenerator-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="34652-130">**IWMDRMEventGenerator Interface**</span></span>](iwmdrmeventgenerator.md)
</dt> </dl>

 

 






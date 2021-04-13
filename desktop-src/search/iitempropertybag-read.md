---
description: Bewirkt, dass eine oder mehrere Eigenschaften aus dem Eigenschaften Behälter gelesen werden. Die iitempropertybag-Schnittstelle wird nur unter Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.
ms.assetid: 78a63ef0-1b79-4b07-9121-a6fbd1116c4b
title: 'Iitempropertybag:: Read-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag.Read
api_type:
- COM
api_location: ''
ms.openlocfilehash: ef7af13dc42239a2823d7e7ca9b8def4748519fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342939"
---
# <a name="iitempropertybagread-method"></a><span data-ttu-id="e7bfc-104">Iitempropertybag:: Read-Methode</span><span class="sxs-lookup"><span data-stu-id="e7bfc-104">IItemPropertyBag::Read method</span></span>

<span data-ttu-id="e7bfc-105">Bewirkt, dass eine oder mehrere Eigenschaften aus dem Eigenschaften Behälter gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-105">Causes one or more properties to be read from the property bag.</span></span> <span data-ttu-id="e7bfc-106">Die [**iitempropertybag**](iitempropertybag.md) -Schnittstelle wird nur unter Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-106">The [**IItemPropertyBag**](iitempropertybag.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7bfc-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7bfc-107">Syntax</span></span>


```C++
HRESULT Read(
  [in]  ULONG    cProperties,
  [in]  ITEMPROP *pPropBag,
  [out] VARIANT  *pvarValue,
  [out] HRESULT  *phrError
);
```



## <a name="parameters"></a><span data-ttu-id="e7bfc-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7bfc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7bfc-109">*cproperties* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e7bfc-109">*cProperties* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7bfc-110">Die Anzahl der zu lesenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-110">The number of properties to read.</span></span> <span data-ttu-id="e7bfc-111">Dieses Argument gibt die Anzahl der Elemente in den Arrays bei *ppropbag*, *pvarvalue* und *phrerror* an.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-111">This argument specifies the number of elements in the arrays at *pPropBag*, *pvarValue*, and *phrError*.</span></span>

</dd> <dt>

<span data-ttu-id="e7bfc-112">*ppropbag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e7bfc-112">*pPropBag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7bfc-113">Ein Zeiger auf ein Array von [**ItemProp**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) -Strukturen, das die angeforderten Eigenschaften angibt.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-113">Pointer to an array of [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) structures that specifies the properties that are requested.</span></span>

</dd> <dt>

<span data-ttu-id="e7bfc-114">*pvarvalue* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e7bfc-114">*pvarValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7bfc-115">Empfängt einen Zeiger, der ein Array von **Variant** -Strukturen zurückgibt, das die Eigenschaftswerte empfängt.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-115">Receives a pointer that returns an array of **VARIANT** structures that receives the property values.</span></span>

</dd> <dt>

<span data-ttu-id="e7bfc-116">*phrerror* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e7bfc-116">*phrError* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7bfc-117">Ein Zeiger auf ein Array von **HRESULT** -Werten, die das Ergebnis der einzelnen gelesenen Eigenschaften empfangen.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-117">Pointer to an array of **HRESULT** values that receives the result of each property read.</span></span> <span data-ttu-id="e7bfc-118">Es müssen mindestens *cproperties* -Elemente in diesem Array vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-118">There must be at least *cProperties* elements in this array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7bfc-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e7bfc-119">Return value</span></span>

<span data-ttu-id="e7bfc-120">Wenn die Methode erfolgreich ausgeführt wird, gibt Sie S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-120">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="e7bfc-121">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7bfc-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e7bfc-122">Remarks</span></span>

<span data-ttu-id="e7bfc-123">Die [**iitempropertybag**](iitempropertybag.md) -Schnittstelle wird nur unter Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-123">The [**IItemPropertyBag**](iitempropertybag.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="e7bfc-124">Zum Anzeigen einer Vorschau von Anlagen mit einem Protokollhandler eines Drittanbieters auf Computern, auf denen Windows XP oder Windows Server 2003 ausgeführt wird, ist es möglicherweise erforderlich, die [**iitempropertybag**](iitempropertybag.md) -Schnittstelle und die folgenden APIs zu verwenden: die Schnittstellen [**isearchprotocolui**](-search-isearchprotocolui.md), [**iitempreviewerext**](-search-iitempreviewerext.md) und [**isearchitem**](-search-isearchitem.md) [**, die-und**](-search-linkinfo.md) [**linktype**](-search-linktype.md) [**-**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) Enumeration.</span><span class="sxs-lookup"><span data-stu-id="e7bfc-124">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**IItemPropertyBag**](iitempropertybag.md) interface and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) and [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) structures, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7bfc-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e7bfc-125">Requirements</span></span>



| <span data-ttu-id="e7bfc-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e7bfc-126">Requirement</span></span> | <span data-ttu-id="e7bfc-127">Wert</span><span class="sxs-lookup"><span data-stu-id="e7bfc-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e7bfc-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e7bfc-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e7bfc-129">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e7bfc-129">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e7bfc-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e7bfc-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e7bfc-131">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e7bfc-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e7bfc-132">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="e7bfc-132">Redistributable</span></span><br/>          | <span data-ttu-id="e7bfc-133">Windows-Desktop Suche (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="e7bfc-133">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="e7bfc-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7bfc-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7bfc-135">**Iitempropertybag**</span><span class="sxs-lookup"><span data-stu-id="e7bfc-135">**IItemPropertyBag**</span></span>](iitempropertybag.md)
</dt> </dl>

 

 





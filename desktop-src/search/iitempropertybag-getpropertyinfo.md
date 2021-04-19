---
description: Ruft die Informationen ab, die erforderlich sind, um die Eigenschaften in der Eigenschaften Sammlung zu lesen oder zu speichern. Die iitempropertybag-Schnittstelle wird nur unter Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.
ms.assetid: 1667b67d-9dd2-48a6-81dd-c8b06834cef0
title: 'Iitempropertybag:: GetPropertyInfo-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag.GetPropertyInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: a64b064c6c6d3708edc353db136fcad599d14adb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346496"
---
# <a name="iitempropertybaggetpropertyinfo-method"></a><span data-ttu-id="89f88-104">Iitempropertybag:: GetPropertyInfo-Methode</span><span class="sxs-lookup"><span data-stu-id="89f88-104">IItemPropertyBag::GetPropertyInfo method</span></span>

<span data-ttu-id="89f88-105">Ruft die Informationen ab, die erforderlich sind, um die Eigenschaften in der Eigenschaften Sammlung zu lesen oder zu speichern.</span><span class="sxs-lookup"><span data-stu-id="89f88-105">Gets the information required to read or save the properties in the property bag.</span></span> <span data-ttu-id="89f88-106">Die [**iitempropertybag**](iitempropertybag.md) -Schnittstelle wird nur unter Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="89f88-106">The [**IItemPropertyBag**](iitempropertybag.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

## <a name="syntax"></a><span data-ttu-id="89f88-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="89f88-107">Syntax</span></span>


```C++
HRESULT GetPropertyInfo(
  [in]  ULONG    iProperty,
  [in]  ULONG    cProperties,
  [out] ITEMPROP *pPropBag,
  [out] ULONG    *pcProperties
);
```



## <a name="parameters"></a><span data-ttu-id="89f88-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="89f88-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89f88-109">*IProperty* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="89f88-109">*iProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89f88-110">Der null basierte Index der ersten Eigenschaft, für die Informationen angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="89f88-110">The zero-based index of the first property for which information is requested.</span></span>

</dd> <dt>

<span data-ttu-id="89f88-111">*cproperties* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="89f88-111">*cProperties* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89f88-112">Die Anzahl der Eigenschaften, für die Informationen zu erhalten sind.</span><span class="sxs-lookup"><span data-stu-id="89f88-112">The number of properties to get information for.</span></span> <span data-ttu-id="89f88-113">Dieses Argument gibt die Anzahl der Array Elemente in *ppropbag* an.</span><span class="sxs-lookup"><span data-stu-id="89f88-113">This argument specifies the number of array elements in *pPropBag*.</span></span>

</dd> <dt>

<span data-ttu-id="89f88-114">*ppropbag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="89f88-114">*pPropBag* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="89f88-115">Ein Zeiger auf ein Array von [**ItemProp**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) -Strukturen, das die Informationen für die Eigenschaften empfängt.</span><span class="sxs-lookup"><span data-stu-id="89f88-115">Pointer to an array of [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) structures that receives the information for the properties.</span></span>

</dd> <dt>

<span data-ttu-id="89f88-116">*pcProperties* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="89f88-116">*pcProperties* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="89f88-117">Empfängt einen Zeiger auf eine **ulong** -Variable, die die Anzahl der Eigenschaften empfängt, für die Informationen abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="89f88-117">Receives a pointer to a **ULONG** variable that receives the number of properties for which information was retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89f88-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="89f88-118">Return value</span></span>

<span data-ttu-id="89f88-119">Wenn die Methode erfolgreich ausgeführt wird, gibt Sie S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="89f88-119">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="89f88-120">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="89f88-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="89f88-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="89f88-121">Remarks</span></span>

<span data-ttu-id="89f88-122">Die [**iitempropertybag**](iitempropertybag.md) -Schnittstelle wird nur unter Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="89f88-122">The [**IItemPropertyBag**](iitempropertybag.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="89f88-123">Zum Anzeigen einer Vorschau von Anlagen mit einem Protokollhandler eines Drittanbieters auf Computern, auf denen Windows XP oder Windows Server 2003 ausgeführt wird, ist es möglicherweise erforderlich, die [**iitempropertybag**](iitempropertybag.md) -Schnittstelle und die folgenden APIs zu verwenden: die Schnittstellen [**isearchprotocolui**](-search-isearchprotocolui.md), [**iitempreviewerext**](-search-iitempreviewerext.md) und [**isearchitem**](-search-isearchitem.md) [**, die-und**](-search-linkinfo.md) [**linktype**](-search-linktype.md) [**-**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) Enumeration.</span><span class="sxs-lookup"><span data-stu-id="89f88-123">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**IItemPropertyBag**](iitempropertybag.md) interface and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) and [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) structures, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="89f88-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="89f88-124">Requirements</span></span>



| <span data-ttu-id="89f88-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="89f88-125">Requirement</span></span> | <span data-ttu-id="89f88-126">Wert</span><span class="sxs-lookup"><span data-stu-id="89f88-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="89f88-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="89f88-127">Minimum supported client</span></span><br/> | <span data-ttu-id="89f88-128">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="89f88-128">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="89f88-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="89f88-129">Minimum supported server</span></span><br/> | <span data-ttu-id="89f88-130">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="89f88-130">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="89f88-131">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="89f88-131">Redistributable</span></span><br/>          | <span data-ttu-id="89f88-132">Windows-Desktop Suche (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="89f88-132">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="89f88-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="89f88-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89f88-134">**Iitempropertybag**</span><span class="sxs-lookup"><span data-stu-id="89f88-134">**IItemPropertyBag**</span></span>](iitempropertybag.md)
</dt> </dl>

 

 





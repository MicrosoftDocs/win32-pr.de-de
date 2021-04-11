---
description: Bewirkt, dass eine oder mehrere Eigenschaften im Eigenschaften Behälter gespeichert werden. Die iitempropertybag-Schnittstelle wird nur unter Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.
ms.assetid: 35491fbc-fb1c-4bad-86e8-9f19856ed7cb
title: 'Iitempropertybag:: Write-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag.Write
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7df66487bba0c2bbef40cf3642754dff56f65835
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128508"
---
# <a name="iitempropertybagwrite-method"></a><span data-ttu-id="ed0a1-104">Iitempropertybag:: Write-Methode</span><span class="sxs-lookup"><span data-stu-id="ed0a1-104">IItemPropertyBag::Write method</span></span>

<span data-ttu-id="ed0a1-105">Bewirkt, dass eine oder mehrere Eigenschaften im Eigenschaften Behälter gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="ed0a1-105">Causes one or more properties to be saved into the property bag.</span></span> <span data-ttu-id="ed0a1-106">Die [**iitempropertybag**](iitempropertybag.md) -Schnittstelle wird nur unter Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ed0a1-106">The [**IItemPropertyBag**](iitempropertybag.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed0a1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed0a1-107">Syntax</span></span>


```C++
HRESULT Write(
  [in] ULONG    cProperties,
  [in] ITEMPROP *pPropBag,
  [in] VARIANT  *pvarValue
);
```



## <a name="parameters"></a><span data-ttu-id="ed0a1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed0a1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed0a1-109">*cproperties* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed0a1-109">*cProperties* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed0a1-110">Die Anzahl der zu speichernden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ed0a1-110">The number of properties to save.</span></span> <span data-ttu-id="ed0a1-111">Dieses Argument gibt die Anzahl der Elemente in den Arrays bei *ppropbag* und *pvarvalue* an.</span><span class="sxs-lookup"><span data-stu-id="ed0a1-111">This argument specifies the number of elements in the arrays at *pPropBag* and *pvarValue*.</span></span>

</dd> <dt>

<span data-ttu-id="ed0a1-112">*ppropbag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed0a1-112">*pPropBag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed0a1-113">Ein Zeiger auf ein Array von [**ItemProp**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) -Strukturen, das die zu speichernden Eigenschaften angibt.</span><span class="sxs-lookup"><span data-stu-id="ed0a1-113">Pointer to an array of [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) structures that specifies the properties to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="ed0a1-114">*pvarvalue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed0a1-114">*pvarValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed0a1-115">Ein Zeiger auf eine **Variante** , deren Typ vom Datentyp der darin enthaltenen Eigenschafts Informationen abhängt.</span><span class="sxs-lookup"><span data-stu-id="ed0a1-115">Pointer to a **VARIANT** whose type depends on the data type of the property information that it contains.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed0a1-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ed0a1-116">Return value</span></span>

<span data-ttu-id="ed0a1-117">Wenn die Methode erfolgreich ausgeführt wird, gibt Sie S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="ed0a1-117">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="ed0a1-118">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ed0a1-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed0a1-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ed0a1-119">Remarks</span></span>

<span data-ttu-id="ed0a1-120">Die [**iitempropertybag**](iitempropertybag.md) -Schnittstelle wird nur unter Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ed0a1-120">The [**IItemPropertyBag**](iitempropertybag.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="ed0a1-121">Zum Anzeigen einer Vorschau von Anlagen mit einem Protokollhandler eines Drittanbieters auf Computern, auf denen Windows XP oder Windows Server 2003 ausgeführt wird, ist es möglicherweise erforderlich, die [**iitempropertybag**](iitempropertybag.md) -Schnittstelle und die folgenden APIs zu verwenden: die Schnittstellen [**isearchprotocolui**](-search-isearchprotocolui.md), [**iitempreviewerext**](-search-iitempreviewerext.md) und [**isearchitem**](-search-isearchitem.md) [**, die-und**](-search-linkinfo.md) [**linktype**](-search-linktype.md) [**-**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) Enumeration.</span><span class="sxs-lookup"><span data-stu-id="ed0a1-121">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**IItemPropertyBag**](iitempropertybag.md) interface and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) and [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) structures, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed0a1-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ed0a1-122">Requirements</span></span>



| <span data-ttu-id="ed0a1-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ed0a1-123">Requirement</span></span> | <span data-ttu-id="ed0a1-124">Wert</span><span class="sxs-lookup"><span data-stu-id="ed0a1-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ed0a1-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ed0a1-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ed0a1-126">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ed0a1-126">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="ed0a1-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ed0a1-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ed0a1-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ed0a1-128">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="ed0a1-129">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="ed0a1-129">Redistributable</span></span><br/>          | <span data-ttu-id="ed0a1-130">Windows-Desktop Suche (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="ed0a1-130">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="ed0a1-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed0a1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed0a1-132">**Iitempropertybag**</span><span class="sxs-lookup"><span data-stu-id="ed0a1-132">**IItemPropertyBag**</span></span>](iitempropertybag.md)
</dt> </dl>

 

 





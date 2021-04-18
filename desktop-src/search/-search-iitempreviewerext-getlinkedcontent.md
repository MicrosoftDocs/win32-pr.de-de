---
description: Ermöglicht der Erweiterung den umfangreichen Inhalt für eine Eigenschaft.
ms.assetid: d1b09ea0-7263-4b7c-8c59-25251bb6b285
title: 'Iitempreviewerext:: getlinkedcontent-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.GetLinkedContent
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7d450bbda2ac7c24b49d1ca5032fd1c59754652e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345490"
---
# <a name="iitempreviewerextgetlinkedcontent-method"></a><span data-ttu-id="c8978-103">Iitempreviewerext:: getlinkedcontent-Methode</span><span class="sxs-lookup"><span data-stu-id="c8978-103">IItemPreviewerExt::GetLinkedContent method</span></span>

<span data-ttu-id="c8978-104">Ermöglicht der Erweiterung den umfangreichen Inhalt für eine Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="c8978-104">Permits the extension to rich content for a property.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8978-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8978-105">Syntax</span></span>


```C++
HRESULT GetLinkedContent(
  [in]          DWORD     dwContext,
  [in]          LPCOLESTR pwszProp,
  [out, retval] LINKINFO  *pInfo
);
```



## <a name="parameters"></a><span data-ttu-id="c8978-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8978-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8978-107">*dwcontext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c8978-107">*dwContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8978-108">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="c8978-108">Type: **DWORD**</span></span>

<span data-ttu-id="c8978-109">Der Kontext Bezeichner für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="c8978-109">The context identifier for the operation.</span></span> <span data-ttu-id="c8978-110">Überschreiben Sie den *dwcontext* -Standard, um den Kontext Bezeichner auf einen Wert Ihrer Wahl festzulegen.</span><span class="sxs-lookup"><span data-stu-id="c8978-110">Override the *dwContext* default to set the context identifier to a value of your choosing.</span></span>

</dd> <dt>

<span data-ttu-id="c8978-111">*pwszprop* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c8978-111">*pwszProp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8978-112">Typ: **lpcolestr**</span><span class="sxs-lookup"><span data-stu-id="c8978-112">Type: **LPCOLESTR**</span></span>

<span data-ttu-id="c8978-113">Ein Zeiger auf die-Eigenschaft des verknüpften Inhalts als Unicode-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="c8978-113">A pointer to the property of the linked content as a Unicode string.</span></span>

</dd> <dt>

<span data-ttu-id="c8978-114">*pinfo* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="c8978-114">*pInfo* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="c8978-115">Typ: \**[**linkinfo**](-search-linkinfo.md) \** _</span><span class="sxs-lookup"><span data-stu-id="c8978-115">Type: \**[**LINKINFO**](-search-linkinfo.md)\** _</span></span>

<span data-ttu-id="c8978-116">Empfängt einen Zeiger auf die [_ *linkinfo* \*](-search-linkinfo.md) -Struktur, in der die-Methode Informationen über die Transaktion zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="c8978-116">Receives a pointer to the [_ *LINKINFO*\*](-search-linkinfo.md) structure in which the method returns information about the transaction.</span></span> <span data-ttu-id="c8978-117">*pinfo* darf kein **null** -Zeiger sein.</span><span class="sxs-lookup"><span data-stu-id="c8978-117">*pInfo* must not be a **NULL** pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8978-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c8978-118">Return value</span></span>

<span data-ttu-id="c8978-119">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c8978-119">Type: **HRESULT**</span></span>

<span data-ttu-id="c8978-120">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="c8978-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c8978-121">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c8978-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8978-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c8978-122">Remarks</span></span>

<span data-ttu-id="c8978-123">Die [**iitempreviewerext**](-search-iitempreviewerext.md) -Schnittstelle wird nur unter Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c8978-123">The [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="c8978-124">Zum Anzeigen einer Vorschau von Anlagen mit einem Protokollhandler eines Drittanbieters auf Computern, auf denen Windows XP oder Windows Server 2003 ausgeführt wird, ist es möglicherweise erforderlich, die [**iitempreviewerext**](-search-iitempreviewerext.md) -Schnittstelle und die folgenden APIs zu verwenden: die Schnittstellen [**isearchprotocolui**](-search-isearchprotocolui.md), [**iitempropertybag**](iitempropertybag.md) und [**isearchitem**](-search-isearchitem.md) , die [**linkinfo**](-search-linkinfo.md) -Struktur und die [**linktype**](-search-linktype.md)</span><span class="sxs-lookup"><span data-stu-id="c8978-124">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface, and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8978-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c8978-125">Requirements</span></span>



| <span data-ttu-id="c8978-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c8978-126">Requirement</span></span> | <span data-ttu-id="c8978-127">Wert</span><span class="sxs-lookup"><span data-stu-id="c8978-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c8978-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c8978-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c8978-129">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c8978-129">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c8978-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c8978-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c8978-131">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c8978-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c8978-132">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="c8978-132">Redistributable</span></span><br/>          | <span data-ttu-id="c8978-133">Windows-Desktop Suche (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="c8978-133">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="c8978-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c8978-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8978-135">**Iitempreviewerext**</span><span class="sxs-lookup"><span data-stu-id="c8978-135">**IItemPreviewerExt**</span></span>](-search-iitempreviewerext.md)
</dt> </dl>

 

 





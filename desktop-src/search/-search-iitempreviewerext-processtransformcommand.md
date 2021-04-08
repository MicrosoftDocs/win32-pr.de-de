---
description: Ermöglicht die Verarbeitung eines Transformations Befehls, der in einer Vorschau Vorlage gefunden wurde.
ms.assetid: 0b81b780-8bd1-4667-a0a1-65319f209603
title: Iitempreviewerext::P rocesstransformcommand-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.ProcessTransformCommand
api_type:
- COM
api_location: ''
ms.openlocfilehash: 384294aac177679ea7445edb880198d250310625
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862172"
---
# <a name="iitempreviewerextprocesstransformcommand-method"></a><span data-ttu-id="f005c-103">Iitempreviewerext::P rocesstransformcommand-Methode</span><span class="sxs-lookup"><span data-stu-id="f005c-103">IItemPreviewerExt::ProcessTransformCommand method</span></span>

<span data-ttu-id="f005c-104">Ermöglicht die Verarbeitung eines Transformations Befehls, der in einer Vorschau Vorlage gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="f005c-104">Permits processing of a transformation command encountered in a preview template.</span></span>

## <a name="syntax"></a><span data-ttu-id="f005c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f005c-105">Syntax</span></span>


```C++
HRESULT ProcessTransformCommand(
  [in]          DWORD     dwContext,
  [in]          LPCOLESTR pwszName,
  [in]          LPCOLESTR pwszArg,
  [out, retval] VARIANT   *pvarResult
);
```



## <a name="parameters"></a><span data-ttu-id="f005c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f005c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f005c-107">*dwcontext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f005c-107">*dwContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f005c-108">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="f005c-108">Type: **DWORD**</span></span>

<span data-ttu-id="f005c-109">Der Kontext Bezeichner für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="f005c-109">The context identifier for the operation.</span></span> <span data-ttu-id="f005c-110">Überschreiben Sie den *dwcontext* -Standard, um den Kontext Bezeichner auf einen Wert Ihrer Wahl festzulegen.</span><span class="sxs-lookup"><span data-stu-id="f005c-110">Override the *dwContext* default to set the context identifier to a value of your choosing.</span></span>

</dd> <dt>

<span data-ttu-id="f005c-111">*pwszName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f005c-111">*pwszName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f005c-112">Typ: **lpcolestr**</span><span class="sxs-lookup"><span data-stu-id="f005c-112">Type: **LPCOLESTR**</span></span>

<span data-ttu-id="f005c-113">Ein Zeiger auf den Namen des Transformations Befehls als Unicode-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="f005c-113">A pointer to the name of the transformation command as a Unicode string.</span></span>

</dd> <dt>

<span data-ttu-id="f005c-114">*pwszarg* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f005c-114">*pwszArg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f005c-115">Typ: **lpcolestr**</span><span class="sxs-lookup"><span data-stu-id="f005c-115">Type: **LPCOLESTR**</span></span>

<span data-ttu-id="f005c-116">Ein Zeiger auf das Argument als Unicode-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="f005c-116">A pointer to the argument as a Unicode string.</span></span>

</dd> <dt>

<span data-ttu-id="f005c-117">*pVarResult* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="f005c-117">*pvarResult* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="f005c-118">Typ: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="f005c-118">Type: \**VARIANT\** _</span></span>

<span data-ttu-id="f005c-119">Ein Zeiger auf die Ergebnis Variante.</span><span class="sxs-lookup"><span data-stu-id="f005c-119">A pointer to the result variant.</span></span> <span data-ttu-id="f005c-120">_pvarResult \* darf kein **null** -Zeiger sein.</span><span class="sxs-lookup"><span data-stu-id="f005c-120">_pvarResult\* must not be a **NULL** pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f005c-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f005c-121">Return value</span></span>

<span data-ttu-id="f005c-122">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f005c-122">Type: **HRESULT**</span></span>

<span data-ttu-id="f005c-123">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="f005c-123">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f005c-124">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f005c-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f005c-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f005c-125">Remarks</span></span>

<span data-ttu-id="f005c-126">Die [**iitempreviewerext**](-search-iitempreviewerext.md) -Schnittstelle wird nur unter Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f005c-126">The [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="f005c-127">Zum Anzeigen einer Vorschau von Anlagen mit einem Protokollhandler eines Drittanbieters auf Computern, auf denen Windows XP oder Windows Server 2003 ausgeführt wird, ist es möglicherweise erforderlich, die [**iitempreviewerext**](-search-iitempreviewerext.md) -Schnittstelle und die folgenden APIs zu verwenden: die Schnittstellen [**isearchprotocolui**](-search-isearchprotocolui.md), [**iitempropertybag**](iitempropertybag.md) und [**isearchitem**](-search-isearchitem.md) , die [**linkinfo**](-search-linkinfo.md) -Struktur und die [**linktype**](-search-linktype.md)</span><span class="sxs-lookup"><span data-stu-id="f005c-127">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface, and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="f005c-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f005c-128">Requirements</span></span>



| <span data-ttu-id="f005c-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f005c-129">Requirement</span></span> | <span data-ttu-id="f005c-130">Wert</span><span class="sxs-lookup"><span data-stu-id="f005c-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f005c-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f005c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="f005c-132">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f005c-132">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f005c-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f005c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="f005c-134">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f005c-134">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f005c-135">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="f005c-135">Redistributable</span></span><br/>          | <span data-ttu-id="f005c-136">Windows-Desktop Suche (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="f005c-136">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="f005c-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f005c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f005c-138">**Iitempreviewerext**</span><span class="sxs-lookup"><span data-stu-id="f005c-138">**IItemPreviewerExt**</span></span>](-search-iitempreviewerext.md)
</dt> </dl>

 

 





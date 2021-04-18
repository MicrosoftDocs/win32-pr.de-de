---
description: Ruft einen zugehörigen Textteil zum Einbetten in den MHTML-Ausgabedatenstrom ab.
ms.assetid: 7810568b-5fb7-4814-aa9f-d7ae805c97e1
title: 'Iitempreviewerext:: getrelatedpart-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.GetRelatedPart
api_type:
- COM
api_location: ''
ms.openlocfilehash: 281d91b1679b2a944996bb1c85060d16c4e0b966
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106339760"
---
# <a name="iitempreviewerextgetrelatedpart-method"></a><span data-ttu-id="b9ed5-103">Iitempreviewerext:: getrelatedpart-Methode</span><span class="sxs-lookup"><span data-stu-id="b9ed5-103">IItemPreviewerExt::GetRelatedPart method</span></span>

<span data-ttu-id="b9ed5-104">Ruft einen zugehörigen Textteil zum Einbetten in den MHTML-Ausgabedatenstrom ab.</span><span class="sxs-lookup"><span data-stu-id="b9ed5-104">Gets a related body part for embedding into the output MHTML stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9ed5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9ed5-105">Syntax</span></span>


```C++
HRESULT GetRelatedPart(
  [in]          DWORD     dwContext,
  [in]          LPCOLESTR pwszProp,
  [in]          DWORD     dwIndex,
  [out, retval] LINKINFO  *pInfo
);
```



## <a name="parameters"></a><span data-ttu-id="b9ed5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b9ed5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9ed5-107">*dwcontext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b9ed5-107">*dwContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9ed5-108">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="b9ed5-108">Type: **DWORD**</span></span>

<span data-ttu-id="b9ed5-109">Der Kontext Bezeichner für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="b9ed5-109">The context identifier for the operation.</span></span> <span data-ttu-id="b9ed5-110">Überschreiben Sie den **dwcontext** -Standard, um den Kontext Bezeichner auf einen Wert Ihrer Wahl festzulegen.</span><span class="sxs-lookup"><span data-stu-id="b9ed5-110">Override the **dwContext** default to set the context identifier to a value of your choosing.</span></span>

</dd> <dt>

<span data-ttu-id="b9ed5-111">*pwszprop* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b9ed5-111">*pwszProp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9ed5-112">Typ: **lpcolestr**</span><span class="sxs-lookup"><span data-stu-id="b9ed5-112">Type: **LPCOLESTR**</span></span>

<span data-ttu-id="b9ed5-113">Ein Zeiger auf die-Eigenschaft des verknüpften Inhalts als Unicode-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="b9ed5-113">A pointer to the property of the linked content as a Unicode string.</span></span>

</dd> <dt>

<span data-ttu-id="b9ed5-114">*dwIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b9ed5-114">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9ed5-115">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="b9ed5-115">Type: **DWORD**</span></span>

<span data-ttu-id="b9ed5-116">Der Wert einer langen ganzen Zahl ohne Vorzeichen, der den NULL basierten Index des zugehörigen Textteils enthält.</span><span class="sxs-lookup"><span data-stu-id="b9ed5-116">An unsigned long integer value that contains the zero-based index of the related body part.</span></span>

</dd> <dt>

<span data-ttu-id="b9ed5-117">*pinfo* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="b9ed5-117">*pInfo* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="b9ed5-118">Typ: \**[**linkinfo**](-search-linkinfo.md) \** _</span><span class="sxs-lookup"><span data-stu-id="b9ed5-118">Type: \**[**LINKINFO**](-search-linkinfo.md)\** _</span></span>

<span data-ttu-id="b9ed5-119">Empfängt einen Zeiger auf die [_ *linkinfo* \*](-search-linkinfo.md) -Struktur, in der die-Methode Informationen über die Transaktion zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="b9ed5-119">Receives a pointer to the [_ *LINKINFO*\*](-search-linkinfo.md) structure in which the method returns information about the transaction.</span></span> <span data-ttu-id="b9ed5-120">*pinfo* darf kein **null** -Zeiger sein.</span><span class="sxs-lookup"><span data-stu-id="b9ed5-120">*pInfo* must not be a **NULL** pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9ed5-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b9ed5-121">Return value</span></span>

<span data-ttu-id="b9ed5-122">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b9ed5-122">Type: **HRESULT**</span></span>

<span data-ttu-id="b9ed5-123">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="b9ed5-123">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b9ed5-124">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b9ed5-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9ed5-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b9ed5-125">Remarks</span></span>

<span data-ttu-id="b9ed5-126">Die [**iitempreviewerext**](-search-iitempreviewerext.md) -Schnittstelle wird nur unter Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b9ed5-126">The [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="b9ed5-127">Zum Anzeigen einer Vorschau von Anlagen mit einem Protokollhandler eines Drittanbieters auf Computern, auf denen Windows XP oder Windows Server 2003 ausgeführt wird, ist es möglicherweise erforderlich, die [**iitempreviewerext**](-search-iitempreviewerext.md) -Schnittstelle und die folgenden APIs zu verwenden: die Schnittstellen [**isearchprotocolui**](-search-isearchprotocolui.md), [**iitempropertybag**](iitempropertybag.md) und [**isearchitem**](-search-isearchitem.md) , die [**linkinfo**](-search-linkinfo.md) -Struktur und die [**linktype**](-search-linktype.md)</span><span class="sxs-lookup"><span data-stu-id="b9ed5-127">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface, and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9ed5-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b9ed5-128">Requirements</span></span>



| <span data-ttu-id="b9ed5-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b9ed5-129">Requirement</span></span> | <span data-ttu-id="b9ed5-130">Wert</span><span class="sxs-lookup"><span data-stu-id="b9ed5-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b9ed5-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b9ed5-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b9ed5-132">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b9ed5-132">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b9ed5-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b9ed5-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b9ed5-134">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b9ed5-134">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b9ed5-135">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="b9ed5-135">Redistributable</span></span><br/>          | <span data-ttu-id="b9ed5-136">Windows-Desktop Suche (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="b9ed5-136">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="b9ed5-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b9ed5-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9ed5-138">**Iitempreviewerext**</span><span class="sxs-lookup"><span data-stu-id="b9ed5-138">**IItemPreviewerExt**</span></span>](-search-iitempreviewerext.md)
</dt> </dl>

 

 





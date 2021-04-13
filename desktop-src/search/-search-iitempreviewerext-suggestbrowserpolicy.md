---
description: Schlägt die Sicherheitsrichtlinie vor, die auf den Browser angewendet werden soll.
ms.assetid: 73541611-2024-4c33-ab03-e3204244c46c
title: 'Iitempreviewerext:: Vorschlags-browserpolicy-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.SuggestBrowserPolicy
api_type:
- COM
api_location: ''
ms.openlocfilehash: 0a4f248edbfa4a1779016e40d73051d8c1d9acac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484427"
---
# <a name="iitempreviewerextsuggestbrowserpolicy-method"></a><span data-ttu-id="547bb-103">Iitempreviewerext:: Vorschlags-browserpolicy-Methode</span><span class="sxs-lookup"><span data-stu-id="547bb-103">IItemPreviewerExt::SuggestBrowserPolicy method</span></span>

<span data-ttu-id="547bb-104">Schlägt die Sicherheitsrichtlinie vor, die auf den Browser angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="547bb-104">Suggests the security policy to be applied to the browser.</span></span>

## <a name="syntax"></a><span data-ttu-id="547bb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="547bb-105">Syntax</span></span>


```C++
HRESULT SuggestBrowserPolicy(
  [in]          DWORD dwContext,
  [out, retval] DWORD *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="547bb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="547bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="547bb-107">*dwcontext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="547bb-107">*dwContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="547bb-108">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="547bb-108">Type: **DWORD**</span></span>

<span data-ttu-id="547bb-109">Der Kontext Bezeichner für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="547bb-109">The context identifier for the operation.</span></span> <span data-ttu-id="547bb-110">Überschreiben Sie den *dwcontext* -Standard, um den Kontext Bezeichner auf einen Wert Ihrer Wahl festzulegen.</span><span class="sxs-lookup"><span data-stu-id="547bb-110">Override the *dwContext* default to set the context identifier to a value of your choosing.</span></span>

</dd> <dt>

<span data-ttu-id="547bb-111">*pdwflags* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="547bb-111">*pdwFlags* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="547bb-112">Typ: \**DWORD \** _</span><span class="sxs-lookup"><span data-stu-id="547bb-112">Type: \**DWORD\** _</span></span>

<span data-ttu-id="547bb-113">Ein Zeiger auf einen DWORD-Wert, der Überprüfungs Prüfungs Flags enthält.</span><span class="sxs-lookup"><span data-stu-id="547bb-113">A pointer to a DWORD value containing verification check flags.</span></span> <span data-ttu-id="547bb-114">Das Flag _ *browserpolicy \_ nicht vertrauenswürdiges \_ Content*\* deaktiviert jede Möglichkeit, dass die Vorschau das Skript oder ActiveX ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="547bb-114">The _ *BROWSERPOLICY\_UNTRUSTED\_CONTENT*\* flag disables any possibility of the preview being able to run script or ActiveX.</span></span> <span data-ttu-id="547bb-115">Der *pdwflags* -Parameter darf kein **null** -Zeiger sein.</span><span class="sxs-lookup"><span data-stu-id="547bb-115">The parameter *pdwFlags* must not be a **NULL** pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="547bb-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="547bb-116">Return value</span></span>

<span data-ttu-id="547bb-117">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="547bb-117">Type: **HRESULT**</span></span>

<span data-ttu-id="547bb-118">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="547bb-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="547bb-119">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="547bb-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="547bb-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="547bb-120">Remarks</span></span>

<span data-ttu-id="547bb-121">Die [**iitempreviewerext**](-search-iitempreviewerext.md) -Schnittstelle wird nur unter Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="547bb-121">The [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="547bb-122">Zum Anzeigen einer Vorschau von Anlagen mit einem Protokollhandler eines Drittanbieters auf Computern, auf denen Windows XP oder Windows Server 2003 ausgeführt wird, ist es möglicherweise erforderlich, die [**iitempreviewerext**](-search-iitempreviewerext.md) -Schnittstelle und die folgenden APIs zu verwenden: die Schnittstellen [**isearchprotocolui**](-search-isearchprotocolui.md), [**iitempropertybag**](iitempropertybag.md) und [**isearchitem**](-search-isearchitem.md) , die [**linkinfo**](-search-linkinfo.md) -Struktur und die [**linktype**](-search-linktype.md)</span><span class="sxs-lookup"><span data-stu-id="547bb-122">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface, and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

<span data-ttu-id="547bb-123">Die Verwendung des Flags " **browserpolicy \_ nicht vertrauenswürdiger \_ Inhalt** " wird dringend empfohlen, um die Möglichkeit zu deaktivieren, dass die Vorschau Skripts oder ActiveX ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="547bb-123">Using the **BROWSERPOLICY\_UNTRUSTED\_CONTENT** flag is strongly recommended to disable any possibility of the preview being able to run script or ActiveX.</span></span> <span data-ttu-id="547bb-124">Die **iitempreviewerext:: Vorschlags-browserpolicy** -Methode kann Informationen darüber zurückgeben, ob das Element, das in der Vorschau angezeigt wird, vertrauenswürdig ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="547bb-124">The **IItemPreviewerExt::SuggestBrowserPolicy** method can return information on whether the item being previewed is trusted or not.</span></span> <span data-ttu-id="547bb-125">Dies ermöglicht es dem Vorschau-Steuerelement, das Skript und sogar ActiveX-Steuerelemente auszuführen.</span><span class="sxs-lookup"><span data-stu-id="547bb-125">This will allow the previewer trident control to execute script, and even ActiveX controls.</span></span> <span data-ttu-id="547bb-126">Da der Vorschau häufig temporäre Dateien verwendet, um die Vorschau zu generieren, kann dies dazu führen, dass in der lokalen Computer Zone unerwartete Skript-und Code Ausführungen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="547bb-126">Because the previewer often uses temporary files to generate the preview, doing so can result in unexpected script and code execution in the Local Computer zone.</span></span>

## <a name="requirements"></a><span data-ttu-id="547bb-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="547bb-127">Requirements</span></span>



| <span data-ttu-id="547bb-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="547bb-128">Requirement</span></span> | <span data-ttu-id="547bb-129">Wert</span><span class="sxs-lookup"><span data-stu-id="547bb-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="547bb-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="547bb-130">Minimum supported client</span></span><br/> | <span data-ttu-id="547bb-131">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="547bb-131">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="547bb-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="547bb-132">Minimum supported server</span></span><br/> | <span data-ttu-id="547bb-133">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="547bb-133">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="547bb-134">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="547bb-134">Redistributable</span></span><br/>          | <span data-ttu-id="547bb-135">Windows-Desktop Suche (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="547bb-135">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="547bb-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="547bb-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="547bb-137">**Iitempreviewerext**</span><span class="sxs-lookup"><span data-stu-id="547bb-137">**IItemPreviewerExt**</span></span>](-search-iitempreviewerext.md)
</dt> </dl>

 

 





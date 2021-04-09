---
description: Ruft das Suchelement für die angegebenen Daten ab. Diese Methode wird einmal für jede URL aufgerufen, die vom Gatherer verarbeitet wird, und Ruft einen Zeiger auf das isearchitem-Objekt ab.
ms.assetid: 35893bc9-8327-44f9-a9fc-7855c5c063e3
title: 'Isearchprotocolui:: getsearchitemforurl-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchProtocolUI.GetSearchItemForUrl
api_type:
- COM
api_location: ''
ms.openlocfilehash: f8a9bbe3459109946b7a4789d9b9f0fb7473ff05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750400"
---
# <a name="isearchprotocoluigetsearchitemforurl-method"></a><span data-ttu-id="d2488-104">Isearchprotocolui:: getsearchitemforurl-Methode</span><span class="sxs-lookup"><span data-stu-id="d2488-104">ISearchProtocolUI::GetSearchItemForUrl method</span></span>

<span data-ttu-id="d2488-105">Ruft das Suchelement für die angegebenen Daten ab.</span><span class="sxs-lookup"><span data-stu-id="d2488-105">Gets the search item for the data specified.</span></span> <span data-ttu-id="d2488-106">Diese Methode wird einmal für jede URL aufgerufen, die vom Gatherer verarbeitet wird, und Ruft einen Zeiger auf das [**isearchitem**](-search-isearchitem.md) -Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="d2488-106">This method is called once for every URL processed by the gatherer, and retrieves a pointer to the [**ISearchItem**](-search-isearchitem.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2488-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2488-107">Syntax</span></span>


```C++
HRESULT GetSearchItemForUrl(
  [in]          LPCOLESTR        pcwszURL,
  [in]          IItemPropertyBag *pPropertyBag,
  [out, retval] ISearchItem      **ppSearchItem
);
```



## <a name="parameters"></a><span data-ttu-id="d2488-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2488-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2488-109">*pcwszurl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d2488-109">*pcwszURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2488-110">Typ: **lpcolestr**</span><span class="sxs-lookup"><span data-stu-id="d2488-110">Type: **LPCOLESTR**</span></span>

<span data-ttu-id="d2488-111">Zeiger auf eine Unicode-Zeichenfolge mit NULL-Daten, die das Suchelement für die URL enthält, auf die zugegriffen wird</span><span class="sxs-lookup"><span data-stu-id="d2488-111">Pointer to a null data terminated Unicode string containing the search item for the URL being accessed.</span></span>

</dd> <dt>

<span data-ttu-id="d2488-112">*ppropertybag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d2488-112">*pPropertyBag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2488-113">Geben Sie Folgendes ein: \**iitempropertybag \** _</span><span class="sxs-lookup"><span data-stu-id="d2488-113">Type: \**IItemPropertyBag\** _</span></span>

<span data-ttu-id="d2488-114">Zeiger auf ein [_ *iitempropertybag* \*](iitempropertybag.md) -Objekt, das Informationen über das Suchelement enthält, einschließlich der Eigenschaften des Elements.</span><span class="sxs-lookup"><span data-stu-id="d2488-114">Pointer to an [_ *IItemPropertyBag*\*](iitempropertybag.md) object that contains information about the search item, including the properties of the item.</span></span>

</dd> <dt>

<span data-ttu-id="d2488-115">*ppsearchitem* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="d2488-115">*ppSearchItem* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="d2488-116">Typ: **[ **isearchitem**](-search-isearchitem.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="d2488-116">Type: **[**ISearchItem**](-search-isearchitem.md)\*\***</span></span>

<span data-ttu-id="d2488-117">Empfängt die Adresse eines Zeigers auf das [**isearchitem**](-search-isearchitem.md) -Objekt, das mit dieser Methode erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="d2488-117">Receives the address of a pointer to the [**ISearchItem**](-search-isearchitem.md) object created by this method.</span></span> <span data-ttu-id="d2488-118">Dieses Objekt enthält Informationen über das Suchelement, z. b. den Dateinamen des Elements.</span><span class="sxs-lookup"><span data-stu-id="d2488-118">This object contains information about the search item, such as the item's file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2488-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d2488-119">Return value</span></span>

<span data-ttu-id="d2488-120">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d2488-120">Type: **HRESULT**</span></span>

<span data-ttu-id="d2488-121">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="d2488-121">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d2488-122">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d2488-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2488-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d2488-123">Remarks</span></span>

<span data-ttu-id="d2488-124">Die **isearchprotocolui:: getsearchitemforurl** -Methode wird nur unter Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d2488-124">The **ISearchProtocolUI::GetSearchItemForUrl** method is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="d2488-125">Zum Anzeigen einer Vorschau von Anlagen mit einem Protokollhandler von Drittanbietern auf Computern, auf denen Windows XP oder Windows Server 2003 ausgeführt wird, kann es erforderlich sein, die [**isearchprotocolui**](-search-isearchprotocolui.md) -Schnittstelle und die folgenden APIs zu verwenden: die Schnittstellen [**iitempreviewerext**](-search-iitempreviewerext.md), [**iitempropertybag**](iitempropertybag.md) und [**isearchitem**](-search-isearchitem.md) , die [**linkinfo**](-search-linkinfo.md) -Struktur und die [**linktype**](-search-linktype.md)</span><span class="sxs-lookup"><span data-stu-id="d2488-125">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**ISearchProtocolUI**](-search-isearchprotocolui.md) interface, and the following APIs: the [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2488-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d2488-126">Requirements</span></span>



| <span data-ttu-id="d2488-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d2488-127">Requirement</span></span> | <span data-ttu-id="d2488-128">Wert</span><span class="sxs-lookup"><span data-stu-id="d2488-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d2488-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d2488-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d2488-130">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d2488-130">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d2488-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d2488-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d2488-132">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d2488-132">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d2488-133">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="d2488-133">Redistributable</span></span><br/>          | <span data-ttu-id="d2488-134">Windows-Desktop Suche (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="d2488-134">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="d2488-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d2488-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2488-136">**Isearchprotocolui**</span><span class="sxs-lookup"><span data-stu-id="d2488-136">**ISearchProtocolUI**</span></span>](-search-isearchprotocolui.md)
</dt> </dl>

 

 





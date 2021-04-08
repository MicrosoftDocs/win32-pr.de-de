---
title: TS_ATTRID (textstor. h)
description: Der TS \_ Atre-Datentyp wird verwendet, um ein Text Attribut zu identifizieren.
ms.assetid: 5e375609-3d3c-4c12-ae05-dcaa70779162
keywords:
- TS_ATTRID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ea3823a95c123fe9942f69a2a133fd94a8567a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739784"
---
# <a name="ts_attrid"></a><span data-ttu-id="c199c-104">TS \_ -attrd</span><span class="sxs-lookup"><span data-stu-id="c199c-104">TS\_ATTRID</span></span>

<span data-ttu-id="c199c-105">Der **TS \_ Atre-** Datentyp wird verwendet, um ein Text Attribut zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="c199c-105">The **TS\_ATTRID** data type is used to identify a text attribute.</span></span>


```C++
typedef GUID TS_ATTRID;
```



## <a name="remarks"></a><span data-ttu-id="c199c-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c199c-106">Remarks</span></span>

<span data-ttu-id="c199c-107">Eine Liste vordefinierter GUIDs für TS \_ atdid ist in der Spalte ". h" enthalten.</span><span class="sxs-lookup"><span data-stu-id="c199c-107">A list of predefined GUIDs for TS\_ATTRID is in tsattrs.h.</span></span>

<span data-ttu-id="c199c-108">Der GUIDs-Text " \_ \_ -Text verticalwriting" und die \_ Textausrichtung "-Text" \_ sind nützlich für Anwendungen, um den zu korrigierenden Eingabe Text abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="c199c-108">The GUIDs TSATTRID\_Text\_VerticalWriting and TSATTRID\_Text\_Orientation are useful for applications to match input text that is to be corrected.</span></span> <span data-ttu-id="c199c-109">Es können zusätzliche benutzerdefinierte GUIDs erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="c199c-109">Additional user-defined GUIDs can be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="c199c-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c199c-110">Requirements</span></span>



| <span data-ttu-id="c199c-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c199c-111">Requirement</span></span> | <span data-ttu-id="c199c-112">Wert</span><span class="sxs-lookup"><span data-stu-id="c199c-112">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c199c-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c199c-113">Minimum supported client</span></span><br/> | <span data-ttu-id="c199c-114">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="c199c-114">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                       |
| <span data-ttu-id="c199c-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c199c-115">Minimum supported server</span></span><br/> | <span data-ttu-id="c199c-116">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="c199c-116">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                             |
| <span data-ttu-id="c199c-117">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="c199c-117">Redistributable</span></span><br/>          | <span data-ttu-id="c199c-118">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c199c-118">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="c199c-119">Header</span><span class="sxs-lookup"><span data-stu-id="c199c-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="c199c-120"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="c199c-120"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="c199c-121">IDL</span><span class="sxs-lookup"><span data-stu-id="c199c-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c199c-122"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c199c-122"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c199c-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c199c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c199c-124">**ITextStoreACP:: findnextattrtransition**</span><span class="sxs-lookup"><span data-stu-id="c199c-124">**ITextStoreACP::FindNextAttrTransition**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-findnextattrtransition)
</dt> <dt>

[<span data-ttu-id="c199c-125">**ITextStoreACP:: requestatus-satposition**</span><span class="sxs-lookup"><span data-stu-id="c199c-125">**ITextStoreACP::RequestAttrsAtPosition**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrsatposition)
</dt> <dt>

[<span data-ttu-id="c199c-126">**ITextStoreACP:: requestatus-stransitioningatposition**</span><span class="sxs-lookup"><span data-stu-id="c199c-126">**ITextStoreACP::RequestAttrsTransitioningAtPosition**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition)
</dt> <dt>

[<span data-ttu-id="c199c-127">**ITextStoreACP:: requestsupportedattrs**</span><span class="sxs-lookup"><span data-stu-id="c199c-127">**ITextStoreACP::RequestSupportedAttrs**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestsupportedattrs)
</dt> <dt>

[<span data-ttu-id="c199c-128">**ITextStoreACPSink:: onattrschange**</span><span class="sxs-lookup"><span data-stu-id="c199c-128">**ITextStoreACPSink::OnAttrsChange**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onattrschange)
</dt> <dt>

[<span data-ttu-id="c199c-129">**Itextstoreanchor:: findnextattrtransition**</span><span class="sxs-lookup"><span data-stu-id="c199c-129">**ITextStoreAnchor::FindNextAttrTransition**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition)
</dt> <dt>

[<span data-ttu-id="c199c-130">**Itextstoreanchor:: requestatus-satposition**</span><span class="sxs-lookup"><span data-stu-id="c199c-130">**ITextStoreAnchor::RequestAttrsAtPosition**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrsatposition)
</dt> <dt>

[<span data-ttu-id="c199c-131">**Itextstoreanchor:: requestatus-stransitioningatposition**</span><span class="sxs-lookup"><span data-stu-id="c199c-131">**ITextStoreAnchor::RequestAttrsTransitioningAtPosition**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition)
</dt> <dt>

[<span data-ttu-id="c199c-132">**Itextstoreanchor:: requestsupportedattrs**</span><span class="sxs-lookup"><span data-stu-id="c199c-132">**ITextStoreAnchor::RequestSupportedAttrs**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestsupportedattrs)
</dt> <dt>

[<span data-ttu-id="c199c-133">**Itextstoreanchorsink:: onattrschange**</span><span class="sxs-lookup"><span data-stu-id="c199c-133">**ITextStoreAnchorSink::OnAttrsChange**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onattrschange)
</dt> <dt>

[<span data-ttu-id="c199c-134">**TS- \_ attrval**</span><span class="sxs-lookup"><span data-stu-id="c199c-134">**TS\_ATTRVAL**</span></span>](/windows/desktop/api/Textstor/ns-textstor-ts_attrval)
</dt> </dl>

 

 






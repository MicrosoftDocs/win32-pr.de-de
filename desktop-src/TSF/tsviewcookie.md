---
title: "\"Tviewcookie\" (textstor. h)"
description: Der Datentyp "tviewcookie" identifiziert eine Kontextansicht.
ms.assetid: e649b799-d0d6-4f2d-b9f1-28070eea9b16
keywords:
- "\"T\""
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb43f888f76410e83e89d037f39ea665ca548ec9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338128"
---
# <a name="tsviewcookie"></a><span data-ttu-id="2e2fa-104">"T"</span><span class="sxs-lookup"><span data-stu-id="2e2fa-104">TsViewCookie</span></span>

<span data-ttu-id="2e2fa-105">Der Datentyp " **tviewcookie** " identifiziert eine Kontextansicht.</span><span class="sxs-lookup"><span data-stu-id="2e2fa-105">The **TsViewCookie** data type identifies a context view.</span></span>


```C++
typedef DWORD TsViewCookie;
```



## <a name="remarks"></a><span data-ttu-id="2e2fa-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2e2fa-106">Remarks</span></span>

<span data-ttu-id="2e2fa-107">Eine Anwendung muss für jede erstellte Ansicht **einen eindeutigen Wert** für den Wert von "Wert" angeben.</span><span class="sxs-lookup"><span data-stu-id="2e2fa-107">An application must supply a unique **TsViewCookie** value for each view it creates.</span></span>

<span data-ttu-id="2e2fa-108">Der TSF-Manager erhält diesen Wert aus der Anwendung durch Aufrufen von [ITextStoreACP:: GetActiveView](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getactiveview) oder [itextstoreanchor:: GetActiveView](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getactiveview).</span><span class="sxs-lookup"><span data-stu-id="2e2fa-108">The TSF manager obtains this value from the application by calling [ITextStoreACP::GetActiveView](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getactiveview) or [ITextStoreAnchor::GetActiveView](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getactiveview).</span></span> <span data-ttu-id="2e2fa-109">Der TSF-Manager verwendet diesen Wert, um die Sicht zu identifizieren, wenn verschiedene [ITextStoreACP-](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) oder [itextstoreanchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) -Methoden aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="2e2fa-109">The TSF manager uses this value to identify the view when calling various [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) or [ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e2fa-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2e2fa-110">Requirements</span></span>



| <span data-ttu-id="2e2fa-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2e2fa-111">Requirement</span></span> | <span data-ttu-id="2e2fa-112">Wert</span><span class="sxs-lookup"><span data-stu-id="2e2fa-112">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e2fa-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2e2fa-113">Minimum supported client</span></span><br/> | <span data-ttu-id="2e2fa-114">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="2e2fa-114">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                       |
| <span data-ttu-id="2e2fa-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2e2fa-115">Minimum supported server</span></span><br/> | <span data-ttu-id="2e2fa-116">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="2e2fa-116">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                             |
| <span data-ttu-id="2e2fa-117">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="2e2fa-117">Redistributable</span></span><br/>          | <span data-ttu-id="2e2fa-118">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2e2fa-118">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="2e2fa-119">Header</span><span class="sxs-lookup"><span data-stu-id="2e2fa-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e2fa-120"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e2fa-120"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="2e2fa-121">IDL</span><span class="sxs-lookup"><span data-stu-id="2e2fa-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2e2fa-122"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2e2fa-122"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e2fa-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2e2fa-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e2fa-124">**ITextStoreACP**</span><span class="sxs-lookup"><span data-stu-id="2e2fa-124">**ITextStoreACP**</span></span>](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp)
</dt> <dt>

[<span data-ttu-id="2e2fa-125">**ITextStoreACP:: GetActiveView**</span><span class="sxs-lookup"><span data-stu-id="2e2fa-125">**ITextStoreACP::GetActiveView**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getactiveview)
</dt> <dt>

[<span data-ttu-id="2e2fa-126">**Itextstoreanchor:: GetActiveView**</span><span class="sxs-lookup"><span data-stu-id="2e2fa-126">**ITextStoreAnchor::GetActiveView**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getactiveview)
</dt> </dl>

 

 






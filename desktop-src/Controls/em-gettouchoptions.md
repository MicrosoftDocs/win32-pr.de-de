---
title: EM_GETTOUCHOPTIONS Meldung (RichEdit. h)
description: Ruft die Berührungs Optionen ab, die einem Rich-Edit-Steuerelement zugeordnet sind.
ms.assetid: 1D367818-5625-4A5A-A7A1-330FED516990
keywords:
- Windows-Steuerelemente für EM_GETTOUCHOPTIONS Meldung
topic_type:
- apiref
api_name:
- EM_GETTOUCHOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 812d37de1972c6da205944d9913dc3fa046c205d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040847"
---
# <a name="em_gettouchoptions-message"></a><span data-ttu-id="12b90-104">EM \_ gettouchoptions-Meldung</span><span class="sxs-lookup"><span data-stu-id="12b90-104">EM\_GETTOUCHOPTIONS message</span></span>

<span data-ttu-id="12b90-105">Ruft die Berührungs Optionen ab, die einem Rich-Edit-Steuerelement zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="12b90-105">Retrieves the touch options that are associated with a rich edit control.</span></span>


```C++
#define EM_GETTOUCHOPTIONS       (WM_USER + 310)
```



## <a name="parameters"></a><span data-ttu-id="12b90-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="12b90-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12b90-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="12b90-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="12b90-108">Die Abruf Optionen, die abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="12b90-108">The touch options to retrieve.</span></span> <span data-ttu-id="12b90-109">Dieses Argument einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="12b90-109">It can be one of the following values.</span></span>



| <span data-ttu-id="12b90-110">Wert</span><span class="sxs-lookup"><span data-stu-id="12b90-110">Value</span></span>                                                                                                                                                                        | <span data-ttu-id="12b90-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="12b90-111">Meaning</span></span>                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="RTO_SHOWHANDLES"></span><span id="rto_showhandles"></span><dl> <span data-ttu-id="12b90-112"><dt>**RTO- \_ showhandles**</dt></span><span class="sxs-lookup"><span data-stu-id="12b90-112"><dt>**RTO\_SHOWHANDLES**</dt></span></span> </dl>          | <span data-ttu-id="12b90-113">Ruft ab, ob die Fingerabdruck Zieh Geräte sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="12b90-113">Retrieves whether the touch grippers are visible.</span></span><br/> |
| <span id="RTO_DISABLEHANDLES"></span><span id="rto_disablehandles"></span><dl> <span data-ttu-id="12b90-114"><dt>**RTO- \_ disablehandles**</dt></span><span class="sxs-lookup"><span data-stu-id="12b90-114"><dt>**RTO\_DISABLEHANDLES**</dt></span></span> </dl> | <span data-ttu-id="12b90-115">Das Abrufen dieses Flags ist nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="12b90-115">Retrieving this flag is not implemented.</span></span><br/>          |



 

</dd> <dt>

<span data-ttu-id="12b90-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="12b90-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="12b90-117">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="12b90-117">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12b90-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="12b90-118">Return value</span></span>

<span data-ttu-id="12b90-119">Gibt den Wert der Option zurück, die vom *wParam* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="12b90-119">Returns the value of the option specified by the *wParam* parameter.</span></span> <span data-ttu-id="12b90-120">Der Wert ist ungleich 0 (null), wenn *wParam* eine **RTO \_ showhandles** hat und die Fingerabdruck Zieh Zeichen sichtbar sind; andernfalls 0 (null).</span><span class="sxs-lookup"><span data-stu-id="12b90-120">It is nonzero if *wParam* is **RTO\_SHOWHANDLES** and the touch grippers are visible; zero, otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="12b90-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="12b90-121">Requirements</span></span>



| <span data-ttu-id="12b90-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="12b90-122">Requirement</span></span> | <span data-ttu-id="12b90-123">Wert</span><span class="sxs-lookup"><span data-stu-id="12b90-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="12b90-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="12b90-124">Minimum supported client</span></span><br/> | <span data-ttu-id="12b90-125">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="12b90-125">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="12b90-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="12b90-126">Minimum supported server</span></span><br/> | <span data-ttu-id="12b90-127">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="12b90-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="12b90-128">Header</span><span class="sxs-lookup"><span data-stu-id="12b90-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="12b90-129"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="12b90-129"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12b90-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="12b90-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12b90-131">**EM \_ settouchoptions**</span><span class="sxs-lookup"><span data-stu-id="12b90-131">**EM\_SETTOUCHOPTIONS**</span></span>](em-settouchoptions.md)
</dt> </dl>

 

 






---
title: TTN_LINKCLICK Benachrichtigungs Code (kommctrl. h)
description: Wird gesendet, wenn auf einen Textlink in einer QuickInfo-Sprechblase geklickt wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: d3e76431-5b5f-4d67-8528-db21fd939917
keywords:
- Windows-Steuerelemente für TTN_LINKCLICK Benachrichtigungs
topic_type:
- apiref
api_name:
- TTN_LINKCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c90be24910c2739b4495b651abf97156342d955b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344681"
---
# <a name="ttn_linkclick-notification-code"></a><span data-ttu-id="4df0b-105">TTN- \_ linkclick-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="4df0b-105">TTN\_LINKCLICK notification code</span></span>

<span data-ttu-id="4df0b-106">Wird gesendet, wenn auf einen Textlink in einer QuickInfo-Sprechblase geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="4df0b-106">Sent when a text link inside a balloon tooltip is clicked.</span></span> <span data-ttu-id="4df0b-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="4df0b-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TTN_LINKCLICK
```



## <a name="parameters"></a><span data-ttu-id="4df0b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4df0b-108">Parameters</span></span>

<span data-ttu-id="4df0b-109">Dieser Benachrichtigungs Code weist keine Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="4df0b-109">This notification code has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4df0b-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4df0b-110">Return value</span></span>

<span data-ttu-id="4df0b-111">Der Rückgabewert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4df0b-111">Return value not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="4df0b-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4df0b-112">Remarks</span></span>

<span data-ttu-id="4df0b-113">Im folgenden finden Sie ein Beispiel für den Fall, dass diese Benachrichtigung gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="4df0b-113">Following is an example of when this notification is sent.</span></span> <span data-ttu-id="4df0b-114">Angenommen, die QuickInfo-QuickInfo enthält den folgenden Text: "This is a <A>Link</A>".</span><span class="sxs-lookup"><span data-stu-id="4df0b-114">Assume that your balloon tooltip contains the following text, "This is a <A>link</A>".</span></span> <span data-ttu-id="4df0b-115">Wenn auf "Link" geklickt wird, sendet das ToolTip-Steuerelement einen TTN- \_ linkclick-Benachrichtigungs Code.</span><span class="sxs-lookup"><span data-stu-id="4df0b-115">When "link" is clicked, the tooltip control sends a TTN\_LINKCLICK notification code.</span></span>

> [!Note]  
> <span data-ttu-id="4df0b-116">Zur Verwendung dieses Benachrichtigungs Codes müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="4df0b-116">To use this notification code, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="4df0b-117">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="4df0b-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4df0b-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4df0b-118">Requirements</span></span>



| <span data-ttu-id="4df0b-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4df0b-119">Requirement</span></span> | <span data-ttu-id="4df0b-120">Wert</span><span class="sxs-lookup"><span data-stu-id="4df0b-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4df0b-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4df0b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4df0b-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4df0b-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4df0b-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4df0b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4df0b-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4df0b-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4df0b-125">Header</span><span class="sxs-lookup"><span data-stu-id="4df0b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4df0b-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="4df0b-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






---
title: RBN_CHILDSIZE Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Grund leisten-Steuerelement gesendet, wenn die Größe des untergeordneten Fensters eines Bands geändert wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: ba64d21a-e568-4894-8007-be644ae4f54a
keywords:
- Windows-Steuerelemente für RBN_CHILDSIZE Benachrichtigungs
topic_type:
- apiref
api_name:
- RBN_CHILDSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d505d13048d96783d53b9b1a821d80712597da4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859002"
---
# <a name="rbn_childsize-notification-code"></a><span data-ttu-id="a4150-105">RBN \_ childsize-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="a4150-105">RBN\_CHILDSIZE notification code</span></span>

<span data-ttu-id="a4150-106">Wird von einem Grund leisten-Steuerelement gesendet, wenn die Größe des untergeordneten Fensters eines Bands geändert wird.</span><span class="sxs-lookup"><span data-stu-id="a4150-106">Sent by a rebar control when a band's child window is resized.</span></span> <span data-ttu-id="a4150-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="a4150-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_CHILDSIZE

    lprbcs = (LPNMREBARCHILDSIZE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="a4150-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4150-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4150-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a4150-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a4150-110">Zeiger auf eine [**nmrebarchildsize**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchildsize) -Struktur, die Informationen über den Benachrichtigungs Code enthält.</span><span class="sxs-lookup"><span data-stu-id="a4150-110">Pointer to an [**NMREBARCHILDSIZE**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchildsize) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4150-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a4150-111">Return value</span></span>

<span data-ttu-id="a4150-112">Der Rückgabewert für diese Benachrichtigung wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a4150-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4150-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a4150-113">Requirements</span></span>



| <span data-ttu-id="a4150-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a4150-114">Requirement</span></span> | <span data-ttu-id="a4150-115">Wert</span><span class="sxs-lookup"><span data-stu-id="a4150-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a4150-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a4150-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a4150-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a4150-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a4150-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a4150-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a4150-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a4150-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a4150-120">Header</span><span class="sxs-lookup"><span data-stu-id="a4150-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4150-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4150-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






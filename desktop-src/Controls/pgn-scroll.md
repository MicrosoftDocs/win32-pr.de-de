---
title: PGN_SCROLL Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Pager-Steuer Elements, dass für das enthaltene Fenster ein Rollup durchgeführt wird. Diese Benachrichtigung wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 3d40e75e-c445-4885-b807-8cfcb92cb2d9
keywords:
- Windows-Steuerelemente für PGN_SCROLL Benachrichtigungs
topic_type:
- apiref
api_name:
- PGN_SCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62bc964b1a820fb0d5cd341e8909f36d5f6312ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103471"
---
# <a name="pgn_scroll-notification-code"></a><span data-ttu-id="ed8d0-105">PGN- \_ scrollbenachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="ed8d0-105">PGN\_SCROLL notification code</span></span>

<span data-ttu-id="ed8d0-106">Benachrichtigt das übergeordnete Fenster eines Pager-Steuer Elements, dass für das enthaltene Fenster ein Rollup durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ed8d0-106">Notifies a pager control's parent window that the contained window is about to be scrolled.</span></span> <span data-ttu-id="ed8d0-107">Diese Benachrichtigung wird in Form einer WM-Benachrichtigungs Meldung gesendet. [**\_**](wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="ed8d0-107">This notification is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PGN_SCROLL

    lpnms = (LPNMPGSCROLL) lParam;
```



## <a name="parameters"></a><span data-ttu-id="ed8d0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed8d0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed8d0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ed8d0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ed8d0-110">Ein Zeiger auf eine [**nmpgscroll**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgscroll) -Struktur, die Informationen über den Benachrichtigungs Code enthält und empfängt.</span><span class="sxs-lookup"><span data-stu-id="ed8d0-110">Pointer to an [**NMPGSCROLL**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgscroll) structure that contains and receives information about the notification code.</span></span> <span data-ttu-id="ed8d0-111">Der **Idir** -Member dieser Struktur gibt die Richtung des Bildlaufs an.</span><span class="sxs-lookup"><span data-stu-id="ed8d0-111">The **iDir** member of this structure indicates the direction of the scroll.</span></span> <span data-ttu-id="ed8d0-112">Die Elemente **IXPOS** und **iypos** enthalten die horizontale und vertikale Position des enthaltenen Fensters vor dem Bildlauf.</span><span class="sxs-lookup"><span data-stu-id="ed8d0-112">The **iXpos** and **iYpos** members contain the horizontal and vertical position of the contained window prior to the scroll.</span></span> <span data-ttu-id="ed8d0-113">Der **iscroll** -Member enthält den Standardwert für das Schiebe Delta.</span><span class="sxs-lookup"><span data-stu-id="ed8d0-113">The **iScroll** member contains the default scroll delta amount.</span></span> <span data-ttu-id="ed8d0-114">Wenn gewünscht, können Sie diesen Member in einen anderen Bild Lauf Betrag ändern.</span><span class="sxs-lookup"><span data-stu-id="ed8d0-114">You can modify this member to a different scroll amount if desired.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed8d0-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ed8d0-115">Return value</span></span>

<span data-ttu-id="ed8d0-116">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="ed8d0-116">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed8d0-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ed8d0-117">Requirements</span></span>



| <span data-ttu-id="ed8d0-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ed8d0-118">Requirement</span></span> | <span data-ttu-id="ed8d0-119">Wert</span><span class="sxs-lookup"><span data-stu-id="ed8d0-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ed8d0-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ed8d0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ed8d0-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ed8d0-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ed8d0-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ed8d0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ed8d0-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ed8d0-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ed8d0-124">Header</span><span class="sxs-lookup"><span data-stu-id="ed8d0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed8d0-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed8d0-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






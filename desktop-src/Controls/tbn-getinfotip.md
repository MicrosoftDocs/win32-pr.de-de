---
title: TBN_GETINFOTIP Benachrichtigungs Code (kommctrl. h)
description: Ruft Infotipp-Informationen für ein Symbolleisten Element ab. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 877de60c-f6e1-440a-81f0-d66ab443c985
keywords:
- Windows-Steuerelemente für TBN_GETINFOTIP Benachrichtigungs
topic_type:
- apiref
api_name:
- TBN_GETINFOTIP
- TBN_GETINFOTIPA
- TBN_GETINFOTIPW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fda2c1b181ebea1840b153b8b2df8328b3f2cc8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040353"
---
# <a name="tbn_getinfotip-notification-code"></a><span data-ttu-id="a2b31-105">TBN- \_ getinfotip-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="a2b31-105">TBN\_GETINFOTIP notification code</span></span>

<span data-ttu-id="a2b31-106">Ruft Infotipp-Informationen für ein Symbolleisten Element ab.</span><span class="sxs-lookup"><span data-stu-id="a2b31-106">Retrieves infotip information for a toolbar item.</span></span> <span data-ttu-id="a2b31-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="a2b31-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_GETINFOTIP

    lptbgit = (LPNMTBGETINFOTIP) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="a2b31-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2b31-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2b31-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a2b31-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a2b31-110">Ein Zeiger auf eine [**nmtbgetinfotip**](/windows/win32/api/commctrl/ns-commctrl-nmtbgetinfotipa) -Struktur, die Element Informationen enthält und Infotipp-Informationen empfängt.</span><span class="sxs-lookup"><span data-stu-id="a2b31-110">Pointer to an [**NMTBGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmtbgetinfotipa) structure that contains item information and receives infotip information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2b31-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a2b31-111">Return value</span></span>

<span data-ttu-id="a2b31-112">Der Rückgabewert wird vom-Steuerelement ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a2b31-112">The return value is ignored by the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2b31-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a2b31-113">Remarks</span></span>

<span data-ttu-id="a2b31-114">Die Infotipp-Unterstützung auf der Symbolleiste ermöglicht der Symbolleiste das Anzeigen von Quick Infos für Elemente, die so groß wie infotipsize-Zeichen sind.</span><span class="sxs-lookup"><span data-stu-id="a2b31-114">The infotip support in the toolbar allows the toolbar to display tooltips for items that are as large as INFOTIPSIZE characters.</span></span> <span data-ttu-id="a2b31-115">Wenn dieser Benachrichtigungs Code nicht verarbeitet wird, verwendet die Symbolleiste den Text des Elements für den infotip.</span><span class="sxs-lookup"><span data-stu-id="a2b31-115">If this notification code is not processed, the toolbar will use the item's text for the infotip.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2b31-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a2b31-116">Requirements</span></span>



| <span data-ttu-id="a2b31-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a2b31-117">Requirement</span></span> | <span data-ttu-id="a2b31-118">Wert</span><span class="sxs-lookup"><span data-stu-id="a2b31-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a2b31-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a2b31-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a2b31-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a2b31-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a2b31-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a2b31-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a2b31-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a2b31-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a2b31-123">Header</span><span class="sxs-lookup"><span data-stu-id="a2b31-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2b31-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2b31-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="a2b31-125">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="a2b31-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a2b31-126">**TBN \_ Getinfotipw** (Unicode) und **TBN \_ getinfotipa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="a2b31-126">**TBN\_GETINFOTIPW** (Unicode) and **TBN\_GETINFOTIPA** (ANSI)</span></span><br/>             |



 

 






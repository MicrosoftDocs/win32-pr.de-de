---
title: HDN_DIVIDERDBLCLICK Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Header Steuer Elements, dass der Benutzer auf den unter Teiler des-Steuer Elements Doppel geklickt hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: b722196a-23ae-49c3-b0a2-8fe0d1e33b26
keywords:
- Windows-Steuerelemente für HDN_DIVIDERDBLCLICK Benachrichtigungs
topic_type:
- apiref
api_name:
- HDN_DIVIDERDBLCLICK
- HDN_DIVIDERDBLCLICKA
- HDN_DIVIDERDBLCLICKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0129096139a4d698f25de543a2628b473bfd66e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104041020"
---
# <a name="hdn_dividerdblclick-notification-code"></a><span data-ttu-id="bc43c-105">Hdn \_ dividerdblclick-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="bc43c-105">HDN\_DIVIDERDBLCLICK notification code</span></span>

<span data-ttu-id="bc43c-106">Benachrichtigt das übergeordnete Fenster eines Header Steuer Elements, dass der Benutzer auf den unter Teiler des-Steuer Elements Doppel geklickt hat.</span><span class="sxs-lookup"><span data-stu-id="bc43c-106">Notifies a header control's parent window that the user double-clicked the divider area of the control.</span></span> <span data-ttu-id="bc43c-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="bc43c-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_DIVIDERDBLCLICK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="bc43c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc43c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc43c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bc43c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bc43c-110">Ein Zeiger auf eine [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) -Struktur, die Informationen über das Header Steuerelement und das Element enthält, auf das Doppel geklickt wurde.</span><span class="sxs-lookup"><span data-stu-id="bc43c-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about the header control and the item whose divider was double-clicked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc43c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bc43c-111">Return value</span></span>

<span data-ttu-id="bc43c-112">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="bc43c-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc43c-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc43c-113">Requirements</span></span>



| <span data-ttu-id="bc43c-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bc43c-114">Requirement</span></span> | <span data-ttu-id="bc43c-115">Wert</span><span class="sxs-lookup"><span data-stu-id="bc43c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bc43c-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bc43c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bc43c-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc43c-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bc43c-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bc43c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bc43c-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc43c-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bc43c-120">Header</span><span class="sxs-lookup"><span data-stu-id="bc43c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc43c-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc43c-121"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="bc43c-122">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="bc43c-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="bc43c-123">**Hdn \_ Dividerdblclickw** (Unicode) und **Hdn \_ dividerdblclicka** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="bc43c-123">**HDN\_DIVIDERDBLCLICKW** (Unicode) and **HDN\_DIVIDERDBLCLICKA** (ANSI)</span></span><br/>   |



 

 






---
title: NM_CHAR (Symbolleisten-) Benachrichtigungs Code (kommstrg. h)
description: Wird von einer Symbolleiste gesendet, wenn Sie eine WM- \_ char-Nachricht empfängt. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 7bf0b046-da8e-448f-94e1-62ba0989f7ba
keywords:
- NM_CHAR (Symbolleiste) Benachrichtigungs Code Windows-Steuerelemente
topic_type:
- apiref
api_name:
- NM_CHAR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5a68cb85130f22c8cda63920ada974453a36991
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859342"
---
# <a name="nm_char-toolbar-notification-code"></a><span data-ttu-id="0b811-105">NM \_ char (Toolbar)-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="0b811-105">NM\_CHAR (toolbar) notification code</span></span>

<span data-ttu-id="0b811-106">Wird von einer Symbolleiste gesendet, wenn Sie eine [**WM- \_ char**](/windows/desktop/inputdev/wm-char) -Nachricht empfängt.</span><span class="sxs-lookup"><span data-stu-id="0b811-106">Sent by a toolbar when it receives a [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message.</span></span> <span data-ttu-id="0b811-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="0b811-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CHAR

    lpnmc = (LPNMCHAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="0b811-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b811-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b811-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0b811-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0b811-110">Ein Zeiger auf eine [**nmchar**](/windows/win32/api/commctrl/ns-commctrl-nmchar) -Struktur, die zusätzliche Informationen über das Zeichen enthält, das den Benachrichtigungs Code verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="0b811-110">Pointer to an [**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) structure that contains additional information about the character that caused the notification code.</span></span> <span data-ttu-id="0b811-111">Der **dwitemprev** -Member dieser Struktur enthält den Befehls Bezeichner des aktuell aktiven Elements oder-1, wenn derzeit kein Element aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="0b811-111">The **dwItemPrev** member of this structure contains the command identifier of the item that is currently hot or -1 if no item is currently hot.</span></span> <span data-ttu-id="0b811-112">Der **dwitemnext** -Member dieser Struktur enthält den Befehls Bezeichner des Elements, das heiß wird, oder-1, wenn der Schlüssel nicht mit der Zugriffstaste eines Elements übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="0b811-112">The **dwItemNext** member of this structure contains the command identifier of the item that will become hot or -1 if the key does not match any item's accelerator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b811-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0b811-113">Return value</span></span>

<span data-ttu-id="0b811-114">Gibt **true** zurück, um anzugeben, dass die Symbolleiste das Zeichen nicht verarbeiten soll, und **false** , damit von der Symbolleiste das Zeichen verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="0b811-114">Returns **TRUE** to indicate that the toolbar should not process the character and **FALSE** to have the toolbar process the character.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b811-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0b811-115">Requirements</span></span>



| <span data-ttu-id="0b811-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0b811-116">Requirement</span></span> | <span data-ttu-id="0b811-117">Wert</span><span class="sxs-lookup"><span data-stu-id="0b811-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0b811-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0b811-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0b811-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0b811-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0b811-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0b811-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0b811-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0b811-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0b811-122">Header</span><span class="sxs-lookup"><span data-stu-id="0b811-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b811-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b811-123"><dt>Commctrl.h</dt></span></span> </dl> |



 


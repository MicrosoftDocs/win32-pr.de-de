---
title: HDN_ITEMSTATEICONCLICK Meldung (kommstrg. h)
description: Benachrichtigt das übergeordnete Fenster eines Header Steuer Elements, dass der Benutzer auf das Zustands Symbol eines Elements geklickt hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: a1969579-3a69-49ff-b06e-4b7450146a92
keywords:
- Windows-Steuerelemente für HDN_ITEMSTATEICONCLICK Meldung
topic_type:
- apiref
api_name:
- HDN_ITEMSTATEICONCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95e5e162b78c829e60494f6e8ff81af3ca97eee4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479161"
---
# <a name="hdn_itemstateiconclick-message"></a><span data-ttu-id="bfd23-105">Hdn \_ itemstateideclick-Nachricht</span><span class="sxs-lookup"><span data-stu-id="bfd23-105">HDN\_ITEMSTATEICONCLICK message</span></span>

<span data-ttu-id="bfd23-106">Benachrichtigt das übergeordnete Fenster eines Header Steuer Elements, dass der Benutzer auf das Zustands Symbol eines Elements geklickt hat.</span><span class="sxs-lookup"><span data-stu-id="bfd23-106">Notifies a header control's parent window that the user clicked an item's state icon.</span></span> <span data-ttu-id="bfd23-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="bfd23-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_ITEMSTATEICONCLICK

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="bfd23-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bfd23-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfd23-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bfd23-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bfd23-110">Ein Zeiger auf eine [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) -Struktur, die zusätzliche Informationen über das Statussymbol enthält, auf das geklickt wurde.</span><span class="sxs-lookup"><span data-stu-id="bfd23-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains additional information about the state icon that was clicked on.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfd23-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bfd23-111">Return value</span></span>

<span data-ttu-id="bfd23-112">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="bfd23-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfd23-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bfd23-113">Requirements</span></span>



| <span data-ttu-id="bfd23-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bfd23-114">Requirement</span></span> | <span data-ttu-id="bfd23-115">Wert</span><span class="sxs-lookup"><span data-stu-id="bfd23-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bfd23-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bfd23-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bfd23-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bfd23-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bfd23-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bfd23-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bfd23-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bfd23-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bfd23-120">Header</span><span class="sxs-lookup"><span data-stu-id="bfd23-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfd23-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfd23-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






---
title: HDN_ITEMCHANGING Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Header Steuer Elements, dass sich die Attribute eines Header Elements ändern. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: c3361f88-69d4-425f-b548-0ad3b2a00af4
keywords:
- Windows-Steuerelemente für HDN_ITEMCHANGING Benachrichtigungs
topic_type:
- apiref
api_name:
- HDN_ITEMCHANGING
- HDN_ITEMCHANGINGA
- HDN_ITEMCHANGINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c803f9bde466b524b2ca1cb89062f5fc89d6865f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858682"
---
# <a name="hdn_itemchanging-notification-code"></a><span data-ttu-id="cb717-105">Hdn \_ ItemChanging-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="cb717-105">HDN\_ITEMCHANGING notification code</span></span>

<span data-ttu-id="cb717-106">Benachrichtigt das übergeordnete Fenster eines Header Steuer Elements, dass sich die Attribute eines Header Elements ändern.</span><span class="sxs-lookup"><span data-stu-id="cb717-106">Notifies a header control's parent window that the attributes of a header item are about to change.</span></span> <span data-ttu-id="cb717-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="cb717-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_ITEMCHANGING

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="cb717-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb717-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb717-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cb717-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cb717-110">Ein Zeiger auf eine [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) -Struktur, die Informationen über das Header Steuerelement und das Header Element enthält, einschließlich der Attribute, die gerade geändert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cb717-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about the header control and the header item, including the attributes that are about to change.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb717-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cb717-111">Return value</span></span>

<span data-ttu-id="cb717-112">Gibt **false** zurück, um die Änderungen zuzulassen, oder **true** , um Sie zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="cb717-112">Returns **FALSE** to allow the changes, or **TRUE** to prevent them.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb717-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cb717-113">Requirements</span></span>



| <span data-ttu-id="cb717-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cb717-114">Requirement</span></span> | <span data-ttu-id="cb717-115">Wert</span><span class="sxs-lookup"><span data-stu-id="cb717-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cb717-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cb717-116">Minimum supported client</span></span><br/> | <span data-ttu-id="cb717-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cb717-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cb717-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cb717-118">Minimum supported server</span></span><br/> | <span data-ttu-id="cb717-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cb717-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cb717-120">Header</span><span class="sxs-lookup"><span data-stu-id="cb717-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb717-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb717-121"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="cb717-122">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="cb717-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="cb717-123">**Hdn \_ Itemchangingw** (Unicode) und **Hdn \_ itemchanginga** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="cb717-123">**HDN\_ITEMCHANGINGW** (Unicode) and **HDN\_ITEMCHANGINGA** (ANSI)</span></span><br/>         |



 

 






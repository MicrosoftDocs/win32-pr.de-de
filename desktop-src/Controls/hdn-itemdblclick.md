---
title: HDN_ITEMDBLCLICK Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Header Steuer Elements, dass der Benutzer auf das-Steuerelement Doppel geklickt hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet. Nur Header Steuerelemente, die auf den HDS-Schaltflächen Stil festgelegt sind, \_ senden diesen Benachrichtigungs Code.
ms.assetid: 72bb00b9-226f-4409-b788-b623868f78b6
keywords:
- Windows-Steuerelemente für HDN_ITEMDBLCLICK Benachrichtigungs
topic_type:
- apiref
api_name:
- HDN_ITEMDBLCLICK
- HDN_ITEMDBLCLICKA
- HDN_ITEMDBLCLICKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e61117303ecc478a998da8799867988dbc1ca08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104213741"
---
# <a name="hdn_itemdblclick-notification-code"></a><span data-ttu-id="40df1-106">Hdn \_ itemdblclick-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="40df1-106">HDN\_ITEMDBLCLICK notification code</span></span>

<span data-ttu-id="40df1-107">Benachrichtigt das übergeordnete Fenster eines Header Steuer Elements, dass der Benutzer auf das-Steuerelement Doppel geklickt hat.</span><span class="sxs-lookup"><span data-stu-id="40df1-107">Notifies a header control's parent window that the user double-clicked the control.</span></span> <span data-ttu-id="40df1-108">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="40df1-108">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <span data-ttu-id="40df1-109">Nur Header Steuerelemente, die auf den [**HDS- \_ Schalt**](header-control-styles.md) Flächen Stil festgelegt sind, senden diesen Benachrichtigungs Code.</span><span class="sxs-lookup"><span data-stu-id="40df1-109">Only header controls that are set to the [**HDS\_BUTTONS**](header-control-styles.md) style send this notification code.</span></span>


```C++
HDN_ITEMDBLCLICK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="40df1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="40df1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40df1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="40df1-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="40df1-112">Ein Zeiger auf eine [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) -Struktur, die Informationen zu diesem Benachrichtigungs Code enthält.</span><span class="sxs-lookup"><span data-stu-id="40df1-112">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40df1-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="40df1-113">Return value</span></span>

<span data-ttu-id="40df1-114">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="40df1-114">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="40df1-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="40df1-115">Requirements</span></span>



| <span data-ttu-id="40df1-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="40df1-116">Requirement</span></span> | <span data-ttu-id="40df1-117">Wert</span><span class="sxs-lookup"><span data-stu-id="40df1-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="40df1-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="40df1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="40df1-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="40df1-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="40df1-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="40df1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="40df1-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="40df1-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="40df1-122">Header</span><span class="sxs-lookup"><span data-stu-id="40df1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="40df1-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="40df1-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="40df1-124">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="40df1-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="40df1-125">**Hdn \_ Itemdblclickw** (Unicode) und **Hdn \_ itemdblclicka** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="40df1-125">**HDN\_ITEMDBLCLICKW** (Unicode) and **HDN\_ITEMDBLCLICKA** (ANSI)</span></span><br/>         |



 

 






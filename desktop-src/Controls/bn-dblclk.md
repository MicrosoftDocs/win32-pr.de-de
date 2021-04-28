---
title: BN_DBLCLK Benachrichtigungscode (Winuser.h)
description: 'BN_DBLCLK Benachrichtigungscode: Wird gesendet, wenn der Benutzer auf eine Schaltfläche doppelklickt.'
ms.assetid: 60cc033f-8b84-4aa5-b625-fdee9deb4757
keywords:
- windows-Steuerelemente für BN_DBLCLK Benachrichtigungscode
topic_type:
- apiref
api_name:
- BN_DBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdb403f37b8fee9ea36023a7cd2511bbaaa2af81
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096848"
---
# <a name="bn_dblclk-notification-code"></a><span data-ttu-id="9e565-104">BN \_ DBLCLK-Benachrichtigungscode</span><span class="sxs-lookup"><span data-stu-id="9e565-104">BN\_DBLCLK notification code</span></span>

<span data-ttu-id="9e565-105">Wird gesendet, wenn der Benutzer auf eine Schaltfläche doppelklickt.</span><span class="sxs-lookup"><span data-stu-id="9e565-105">Sent when the user double-clicks a button.</span></span> <span data-ttu-id="9e565-106">Dieser Benachrichtigungscode wird automatisch für die Schaltflächen [**BS \_ USERBUTTON,**](button-styles.md) [**BS \_ RADIOBUTTON**](button-styles.md)und [**BS \_ OWNERDRAW**](button-styles.md) gesendet.</span><span class="sxs-lookup"><span data-stu-id="9e565-106">This notification code is sent automatically for [**BS\_USERBUTTON**](button-styles.md), [**BS\_RADIOBUTTON**](button-styles.md), and [**BS\_OWNERDRAW**](button-styles.md) buttons.</span></span> <span data-ttu-id="9e565-107">Andere Schaltflächentypen senden BN \_ DBLCLK nur, wenn sie den [**BS \_ NOTIFY-Stil**](button-styles.md) aufweisen.</span><span class="sxs-lookup"><span data-stu-id="9e565-107">Other button types send BN\_DBLCLK only if they have the [**BS\_NOTIFY**](button-styles.md) style.</span></span>

<span data-ttu-id="9e565-108">Das übergeordnete Fenster der Schaltfläche empfängt diesen Benachrichtigungscode über die [**WM \_ COMMAND-Meldung.**](/windows/desktop/menurc/wm-command)</span><span class="sxs-lookup"><span data-stu-id="9e565-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_DBLCLK

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="9e565-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e565-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e565-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9e565-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9e565-111">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Steuerelementbezeichner der Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="9e565-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="9e565-112">[**Hiword**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungscode an.</span><span class="sxs-lookup"><span data-stu-id="9e565-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="9e565-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9e565-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9e565-114">Ein Handle für die Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="9e565-114">A handle to the button.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9e565-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9e565-115">Remarks</span></span>

<span data-ttu-id="9e565-116">BN \_ DBLCLK ist identisch mit dem [BN DOUBLECLICKED-Benachrichtigungscode. \_ ](bn-doubleclicked.md)</span><span class="sxs-lookup"><span data-stu-id="9e565-116">BN\_DBLCLK is the same as the [BN\_DOUBLECLICKED](bn-doubleclicked.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e565-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9e565-117">Requirements</span></span>



| <span data-ttu-id="9e565-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9e565-118">Requirement</span></span> | <span data-ttu-id="9e565-119">Wert</span><span class="sxs-lookup"><span data-stu-id="9e565-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e565-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9e565-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9e565-121">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9e565-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9e565-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9e565-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9e565-123">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9e565-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9e565-124">Header</span><span class="sxs-lookup"><span data-stu-id="9e565-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e565-125"><dt>Winuser.h (windows.h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="9e565-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e565-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9e565-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="9e565-127">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="9e565-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9e565-128">BN \_ GEKLICKT</span><span class="sxs-lookup"><span data-stu-id="9e565-128">BN\_CLICKED</span></span>](bn-clicked.md)
</dt> <dt>

[<span data-ttu-id="9e565-129">BN \_ DOUBLECLICKED</span><span class="sxs-lookup"><span data-stu-id="9e565-129">BN\_DOUBLECLICKED</span></span>](bn-doubleclicked.md)
</dt> <dt>

<span data-ttu-id="9e565-130">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="9e565-130">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="9e565-131">**\_WM-BEFEHL**</span><span class="sxs-lookup"><span data-stu-id="9e565-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


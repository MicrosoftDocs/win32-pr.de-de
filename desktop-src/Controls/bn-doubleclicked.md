---
title: BN_DOUBLECLICKED Benachrichtigungscode (Winuser.h)
description: 'BN_DOUBLECLICKED Benachrichtigungscode: Wird gesendet, wenn der Benutzer auf eine Schaltfläche doppelklickt.'
ms.assetid: 2fd7363a-5a02-453c-bfab-df5cbf8e42a5
keywords:
- BN_DOUBLECLICKED Benachrichtigungscode Windows-Steuerelemente
topic_type:
- apiref
api_name:
- BN_DOUBLECLICKED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64a11a4dec91a7a2f1d200c4c86c6989d846604a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104188"
---
# <a name="bn_doubleclicked-notification-code"></a><span data-ttu-id="fbb12-104">BN \_ DOUBLECLICKED-Benachrichtigungscode</span><span class="sxs-lookup"><span data-stu-id="fbb12-104">BN\_DOUBLECLICKED notification code</span></span>

<span data-ttu-id="fbb12-105">Wird gesendet, wenn der Benutzer auf eine Schaltfläche doppelklickt.</span><span class="sxs-lookup"><span data-stu-id="fbb12-105">Sent when the user double-clicks a button.</span></span> <span data-ttu-id="fbb12-106">Dieser Benachrichtigungscode wird automatisch für [**die Schaltflächen BS \_ USERBUTTON,**](button-styles.md) [**BS \_ RADIOBUTTON**](button-styles.md)und [**BS \_ OWNERDRAW**](button-styles.md) gesendet.</span><span class="sxs-lookup"><span data-stu-id="fbb12-106">This notification code is sent automatically for [**BS\_USERBUTTON**](button-styles.md), [**BS\_RADIOBUTTON**](button-styles.md), and [**BS\_OWNERDRAW**](button-styles.md) buttons.</span></span> <span data-ttu-id="fbb12-107">Andere Schaltflächentypen senden BN \_ DOUBLECLICKED nur, wenn sie den [**Stil BS \_ NOTIFY**](button-styles.md) haben.</span><span class="sxs-lookup"><span data-stu-id="fbb12-107">Other button types send BN\_DOUBLECLICKED only if they have the [**BS\_NOTIFY**](button-styles.md) style.</span></span>

<span data-ttu-id="fbb12-108">Das übergeordnete Fenster der Schaltfläche empfängt diesen Benachrichtigungscode über die [**WM \_ COMMAND-Meldung.**](/windows/desktop/menurc/wm-command)</span><span class="sxs-lookup"><span data-stu-id="fbb12-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_DOUBLECLICKED

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="fbb12-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="fbb12-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbb12-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fbb12-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fbb12-111">Das [**LOWORD enthält**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) den Steuerelementbezeichner der Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="fbb12-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="fbb12-112">Das [**HIWORD gibt**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) den Benachrichtigungscode an.</span><span class="sxs-lookup"><span data-stu-id="fbb12-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="fbb12-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fbb12-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fbb12-114">Ein Handle für die Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="fbb12-114">A handle to the button.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fbb12-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fbb12-115">Remarks</span></span>

<span data-ttu-id="fbb12-116">BN \_ DOUBLECLICKED ist mit dem [BN \_ DBLCLK-Benachrichtigungscode](bn-dblclk.md) identisch.</span><span class="sxs-lookup"><span data-stu-id="fbb12-116">BN\_DOUBLECLICKED is the same as the [BN\_DBLCLK](bn-dblclk.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbb12-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fbb12-117">Requirements</span></span>



| <span data-ttu-id="fbb12-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fbb12-118">Requirement</span></span> | <span data-ttu-id="fbb12-119">Wert</span><span class="sxs-lookup"><span data-stu-id="fbb12-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbb12-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fbb12-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fbb12-121">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fbb12-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fbb12-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fbb12-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fbb12-123">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fbb12-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fbb12-124">Header</span><span class="sxs-lookup"><span data-stu-id="fbb12-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fbb12-125"><dt>Winuser.h (einschließlich Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="fbb12-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 


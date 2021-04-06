---
title: BN_DOUBLECLICKED Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, wenn der Benutzer auf eine Schaltfläche doppelklickt.
ms.assetid: 2fd7363a-5a02-453c-bfab-df5cbf8e42a5
keywords:
- Windows-Steuerelemente für BN_DOUBLECLICKED Benachrichtigungs
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
ms.openlocfilehash: 018df4387b026d68e3f4e9a6c259fb19efd4a0f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858758"
---
# <a name="bn_doubleclicked-notification-code"></a><span data-ttu-id="a5e0c-104">Milliarde- \_ Benachrichtigungs Code mit doppelten Klicks</span><span class="sxs-lookup"><span data-stu-id="a5e0c-104">BN\_DOUBLECLICKED notification code</span></span>

<span data-ttu-id="a5e0c-105">Wird gesendet, wenn der Benutzer auf eine Schaltfläche doppelklickt.</span><span class="sxs-lookup"><span data-stu-id="a5e0c-105">Sent when the user double-clicks a button.</span></span> <span data-ttu-id="a5e0c-106">Dieser Benachrichtigungs Code wird automatisch für die Schaltflächen " [**\_ Benutzer Schaltfläche**](button-styles.md)", " [**SB \_ RadioButton**](button-styles.md)" und " [**b \_**](button-styles.md)</span><span class="sxs-lookup"><span data-stu-id="a5e0c-106">This notification code is sent automatically for [**BS\_USERBUTTON**](button-styles.md), [**BS\_RADIOBUTTON**](button-styles.md), and [**BS\_OWNERDRAW**](button-styles.md) buttons.</span></span> <span data-ttu-id="a5e0c-107">Bei anderen Schaltflächen Typen \_ wird nur der Typ "bn doublegeklickt" gesendet, wenn Sie über die Art der [**\_**](button-styles.md) "</span><span class="sxs-lookup"><span data-stu-id="a5e0c-107">Other button types send BN\_DOUBLECLICKED only if they have the [**BS\_NOTIFY**](button-styles.md) style.</span></span>

<span data-ttu-id="a5e0c-108">Das übergeordnete Fenster der Schaltfläche empfängt diesen Benachrichtigungs Code über die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.</span><span class="sxs-lookup"><span data-stu-id="a5e0c-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_DOUBLECLICKED

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="a5e0c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5e0c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5e0c-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a5e0c-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a5e0c-111">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Steuerelement Bezeichner der Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="a5e0c-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="a5e0c-112">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.</span><span class="sxs-lookup"><span data-stu-id="a5e0c-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="a5e0c-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a5e0c-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a5e0c-114">Ein Handle für die Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="a5e0c-114">A handle to the button.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a5e0c-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a5e0c-115">Remarks</span></span>

<span data-ttu-id="a5e0c-116">Der Wert für "bn doublegeklickt" ist mit dem Datenbankadministrator- \_ Benachrichtigungs Code [ \_ ](bn-dblclk.md) identisch.</span><span class="sxs-lookup"><span data-stu-id="a5e0c-116">BN\_DOUBLECLICKED is the same as the [BN\_DBLCLK](bn-dblclk.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5e0c-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a5e0c-117">Requirements</span></span>



| <span data-ttu-id="a5e0c-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a5e0c-118">Requirement</span></span> | <span data-ttu-id="a5e0c-119">Wert</span><span class="sxs-lookup"><span data-stu-id="a5e0c-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5e0c-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a5e0c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a5e0c-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a5e0c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a5e0c-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a5e0c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a5e0c-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a5e0c-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a5e0c-124">Header</span><span class="sxs-lookup"><span data-stu-id="a5e0c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5e0c-125"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="a5e0c-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 


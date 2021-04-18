---
title: RBN_AUTOSIZE Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Grund leisten-Steuerelement gesendet, das mit der automatischen Größenanpassung von RB erstellt wird, \_ Wenn sich der grundbalken automatisch ändert. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: d174fe99-13cc-404c-9dc5-d5a93e9807a2
keywords:
- Windows-Steuerelemente für RBN_AUTOSIZE Benachrichtigungs
topic_type:
- apiref
api_name:
- RBN_AUTOSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ecfac5a4f84d69d444c25a24956cb911fd90a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340376"
---
# <a name="rbn_autosize-notification-code"></a><span data-ttu-id="576ff-105">RBN- \_ Benachrichtigungs Code für automatische Größe</span><span class="sxs-lookup"><span data-stu-id="576ff-105">RBN\_AUTOSIZE notification code</span></span>

<span data-ttu-id="576ff-106">Wird von einem Grund leisten-Steuerelement gesendet, das mit der automatischen [**\_ Größenanpassung von RB**](rebar-control-styles.md) erstellt wird, wenn sich der grundbalken automatisch ändert.</span><span class="sxs-lookup"><span data-stu-id="576ff-106">Sent by a rebar control created with the [**RBS\_AUTOSIZE**](rebar-control-styles.md) style when the rebar automatically resizes itself.</span></span> <span data-ttu-id="576ff-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="576ff-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_AUTOSIZE

    lpnmas = (LPNMRBAUTOSIZE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="576ff-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="576ff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="576ff-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="576ff-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="576ff-110">Zeiger auf eine [**nmrbauumsize**](/windows/win32/api/commctrl/ns-commctrl-nmrbautosize) -Struktur, die Informationen über den Vorgang zum Ändern der Größe enthält.</span><span class="sxs-lookup"><span data-stu-id="576ff-110">Pointer to an [**NMRBAUTOSIZE**](/windows/win32/api/commctrl/ns-commctrl-nmrbautosize) structure that contains information about the resize operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="576ff-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="576ff-111">Return value</span></span>

<span data-ttu-id="576ff-112">Der Rückgabewert für diese Benachrichtigung wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="576ff-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="576ff-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="576ff-113">Requirements</span></span>



| <span data-ttu-id="576ff-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="576ff-114">Requirement</span></span> | <span data-ttu-id="576ff-115">Wert</span><span class="sxs-lookup"><span data-stu-id="576ff-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="576ff-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="576ff-116">Minimum supported client</span></span><br/> | <span data-ttu-id="576ff-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="576ff-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="576ff-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="576ff-118">Minimum supported server</span></span><br/> | <span data-ttu-id="576ff-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="576ff-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="576ff-120">Header</span><span class="sxs-lookup"><span data-stu-id="576ff-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="576ff-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="576ff-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






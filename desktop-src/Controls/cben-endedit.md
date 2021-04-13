---
title: CBEN_ENDEDIT Benachrichtigungs Code (kommctrl. h)
description: Wird gesendet, wenn der Benutzer einen Vorgang innerhalb des Bearbeitungs Felds abgeschlossen hat oder ein Element aus der Dropdown Liste des Steuer Elements ausgewählt hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: b6b50951-7304-4499-b57b-a5b592de2190
keywords:
- Windows-Steuerelemente für CBEN_ENDEDIT Benachrichtigungs
topic_type:
- apiref
api_name:
- CBEN_ENDEDIT
- CBEN_ENDEDITA
- CBEN_ENDEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 679b9f878dbd8f7f374b461ee548f9ce2c62e281
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391550"
---
# <a name="cben_endedit-notification-code"></a><span data-ttu-id="5a324-105">Cben \_ EndEdit-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="5a324-105">CBEN\_ENDEDIT notification code</span></span>

<span data-ttu-id="5a324-106">Wird gesendet, wenn der Benutzer einen Vorgang innerhalb des Bearbeitungs Felds abgeschlossen hat oder ein Element aus der Dropdown Liste des Steuer Elements ausgewählt hat.</span><span class="sxs-lookup"><span data-stu-id="5a324-106">Sent when the user has concluded an operation within the edit box or has selected an item from the control's drop-down list.</span></span> <span data-ttu-id="5a324-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="5a324-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
CBEN_ENDEDIT

    pnmEditInfo = (PNMCBEENDEDIT) lParam;
```



## <a name="parameters"></a><span data-ttu-id="5a324-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a324-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a324-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5a324-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5a324-110">Ein Zeiger auf eine [**nmcbeendedit**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbeendedita) -Struktur, die Informationen darüber enthält, wie der Benutzer den Bearbeitungsvorgang abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="5a324-110">A pointer to an [**NMCBEENDEDIT**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbeendedita) structure that contains information about how the user concluded the edit operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a324-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5a324-111">Return value</span></span>

<span data-ttu-id="5a324-112">**False** , um den Benachrichtigungs Code zu akzeptieren und dem Steuerelement das Anzeigen des ausgewählten Elements zu ermöglichen. andernfalls **true**.</span><span class="sxs-lookup"><span data-stu-id="5a324-112">**FALSE** to accept the notification code and allow the control to display the selected item; otherwise, **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a324-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5a324-113">Requirements</span></span>



| <span data-ttu-id="5a324-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5a324-114">Requirement</span></span> | <span data-ttu-id="5a324-115">Wert</span><span class="sxs-lookup"><span data-stu-id="5a324-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5a324-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5a324-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5a324-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5a324-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5a324-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5a324-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5a324-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5a324-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5a324-120">Header</span><span class="sxs-lookup"><span data-stu-id="5a324-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a324-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a324-121"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="5a324-122">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="5a324-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5a324-123">**Cben \_ "Dededitw** (Unicode)" und " **cben \_** " (ANSI)</span><span class="sxs-lookup"><span data-stu-id="5a324-123">**CBEN\_ENDEDITW** (Unicode) and **CBEN\_ENDEDITA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="5a324-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5a324-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a324-125">Informationen zu ComboBoxEx-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="5a324-125">About ComboBoxEx Controls</span></span>](comboboxex-controls.md)
</dt> </dl>

 

 






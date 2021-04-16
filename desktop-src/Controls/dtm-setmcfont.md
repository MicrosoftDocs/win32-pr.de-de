---
title: DTM_SETMCFONT Meldung (kommstrg. h)
description: Legt die Schriftart fest, die vom untergeordneten Monatskalender-Steuerelement des Steuer Elements für die Datums-und Uhrzeit Auswahl verwendet werden soll. Sie können diese Nachricht explizit senden oder das DateTime- \_ SetMonthCalFont-Makro verwenden.
ms.assetid: 5033e975-9b68-438a-99c3-80ca02cd59e7
keywords:
- Windows-Steuerelemente für DTM_SETMCFONT Meldung
topic_type:
- apiref
api_name:
- DTM_SETMCFONT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b148ffb95acd82257265bf0bab53000b10803793
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477931"
---
# <a name="dtm_setmcfont-message"></a><span data-ttu-id="cd9a3-105">DTM- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="cd9a3-105">DTM\_SETMCFONT message</span></span>

<span data-ttu-id="cd9a3-106">Legt die Schriftart fest, die vom untergeordneten Monatskalender-Steuerelement des Steuer Elements für die Datums-und Uhrzeit Auswahl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cd9a3-106">Sets the font to be used by the date and time picker (DTP) control's child month calendar control.</span></span> <span data-ttu-id="cd9a3-107">Sie können diese Nachricht explizit senden oder das [**DateTime- \_ SetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalfont) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="cd9a3-107">You can send this message explicitly or use the [**DateTime\_SetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalfont) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="cd9a3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="cd9a3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd9a3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cd9a3-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cd9a3-110">Ein Handle für die Schriftart, die festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="cd9a3-110">A handle to the font that will be set.</span></span>

</dd> <dt>

<span data-ttu-id="cd9a3-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cd9a3-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cd9a3-112">Gibt an, ob das Steuerelement sofort nach dem Festlegen der Schriftart neu gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cd9a3-112">Specifies whether the control should be redrawn immediately upon setting the font.</span></span> <span data-ttu-id="cd9a3-113">Wenn Sie diesen Parameter auf " **true** " festlegen, wird das Steuerelement neu gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="cd9a3-113">Setting this parameter to **TRUE** causes the control to redraw itself.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd9a3-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cd9a3-114">Return value</span></span>

<span data-ttu-id="cd9a3-115">Der Rückgabewert für diese Nachricht wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="cd9a3-115">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd9a3-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cd9a3-116">Requirements</span></span>



| <span data-ttu-id="cd9a3-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cd9a3-117">Requirement</span></span> | <span data-ttu-id="cd9a3-118">Wert</span><span class="sxs-lookup"><span data-stu-id="cd9a3-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cd9a3-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cd9a3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cd9a3-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cd9a3-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cd9a3-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cd9a3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cd9a3-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cd9a3-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cd9a3-123">Header</span><span class="sxs-lookup"><span data-stu-id="cd9a3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd9a3-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd9a3-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






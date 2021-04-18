---
title: TCM_SETPADDING Meldung (kommstrg. h)
description: Legt den Leerraum (Padding) um das Symbol und die Bezeichnung der einzelnen Registerkarten in einem Registerkarten-Steuerelement fest. Sie können diese Nachricht explizit oder mithilfe des tabstrg- \_ setPadding-Makros senden.
ms.assetid: c7f84c0d-8bf4-429a-b403-a0019575e72e
keywords:
- Windows-Steuerelemente für TCM_SETPADDING Meldung
topic_type:
- apiref
api_name:
- TCM_SETPADDING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 353cde946944bda7dc8d285f863d976e29353996
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338318"
---
# <a name="tcm_setpadding-message"></a><span data-ttu-id="1c989-105">TCM- \_ setPadding-Meldung</span><span class="sxs-lookup"><span data-stu-id="1c989-105">TCM\_SETPADDING message</span></span>

<span data-ttu-id="1c989-106">Legt den Leerraum (Padding) um das Symbol und die Bezeichnung der einzelnen Registerkarten in einem Registerkarten-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="1c989-106">Sets the amount of space (padding) around each tab's icon and label in a tab control.</span></span> <span data-ttu-id="1c989-107">Sie können diese Nachricht explizit oder mithilfe des [**tabstrg- \_ setPadding**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setpadding) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="1c989-107">You can send this message explicitly or by using the [**TabCtrl\_SetPadding**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setpadding) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="1c989-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c989-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c989-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1c989-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1c989-110">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ist ein **int** -Wert, der die horizontale Auffüll Menge in Pixel angibt.</span><span class="sxs-lookup"><span data-stu-id="1c989-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is an **INT** value that specifies the amount of horizontal padding, in pixels.</span></span> <span data-ttu-id="1c989-111">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) ist ein **int** -Wert, der die Menge der vertikalen Auffüll Zeichen in Pixel angibt.</span><span class="sxs-lookup"><span data-stu-id="1c989-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is an **INT** value that specifies the amount of vertical padding, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c989-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1c989-112">Return value</span></span>

<span data-ttu-id="1c989-113">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="1c989-113">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c989-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1c989-114">Requirements</span></span>



| <span data-ttu-id="1c989-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1c989-115">Requirement</span></span> | <span data-ttu-id="1c989-116">Wert</span><span class="sxs-lookup"><span data-stu-id="1c989-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1c989-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1c989-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1c989-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1c989-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1c989-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1c989-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1c989-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1c989-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1c989-121">Header</span><span class="sxs-lookup"><span data-stu-id="1c989-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c989-122"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c989-122"><dt>Commctrl.h</dt></span></span> </dl> |



 


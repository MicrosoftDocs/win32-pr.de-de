---
title: MCM_SIZERECTTOMIN Meldung (kommstrg. h)
description: Berechnet, wie viele Kalender in das angegebene Rechteck passen, und gibt dann die Mindestgröße zurück, die ein Rechteck aufweisen muss, um dieser Anzahl von Kalendern gerecht zu werden. Sie können diese Nachricht explizit oder mit dem monthcal \_ sizerecttomin-Makro senden.
ms.assetid: d52a7f68-e0c9-4646-a4aa-97129dffeb5d
keywords:
- Windows-Steuerelemente für MCM_SIZERECTTOMIN Meldung
topic_type:
- apiref
api_name:
- MCM_SIZERECTTOMIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f525f4cca9280b92fab0b9b86aa1d950ed990ef4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105981"
---
# <a name="mcm_sizerecttomin-message"></a><span data-ttu-id="60dde-105">MCM \_ sizerecttomin-Meldung</span><span class="sxs-lookup"><span data-stu-id="60dde-105">MCM\_SIZERECTTOMIN message</span></span>

<span data-ttu-id="60dde-106">Berechnet, wie viele Kalender in das angegebene Rechteck passen, und gibt dann die Mindestgröße zurück, die ein Rechteck aufweisen muss, um dieser Anzahl von Kalendern gerecht zu werden.</span><span class="sxs-lookup"><span data-stu-id="60dde-106">Calculates how many calendars will fit in the given rectangle, and then returns the minimum size that a rectangle needs to be to fit that number of calendars.</span></span> <span data-ttu-id="60dde-107">Sie können diese Nachricht explizit oder mit dem [**monthcal \_ sizerecttomin**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_sizerecttomin) -Makro senden.</span><span class="sxs-lookup"><span data-stu-id="60dde-107">You can send this message explicitly or by using the [**MonthCal\_SizeRectToMin**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_sizerecttomin) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="60dde-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="60dde-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60dde-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="60dde-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="60dde-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="60dde-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="60dde-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="60dde-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="60dde-112">Enthält bei einem Eintrag einen Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die einen Bereich beschreibt, der größer oder gleich der Größe ist, die für die gewünschte Anzahl von Kalendern erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="60dde-112">On entry, contains a pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that describes a region that is greater than or equal to the size necessary to fit the desired number of calendars.</span></span> <span data-ttu-id="60dde-113">Wenn diese Funktion zurückgegeben wird, enthält Sie die minimale **Rect** -Struktur, die dieser Anzahl von Kalendern entspricht.</span><span class="sxs-lookup"><span data-stu-id="60dde-113">When this function returns, contains the minimum **RECT** structure that fits this number of calendars.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60dde-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="60dde-114">Return value</span></span>

<span data-ttu-id="60dde-115">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="60dde-115">Unused.</span></span>

## <a name="requirements"></a><span data-ttu-id="60dde-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="60dde-116">Requirements</span></span>



| <span data-ttu-id="60dde-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="60dde-117">Requirement</span></span> | <span data-ttu-id="60dde-118">Wert</span><span class="sxs-lookup"><span data-stu-id="60dde-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="60dde-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="60dde-119">Minimum supported client</span></span><br/> | <span data-ttu-id="60dde-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="60dde-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="60dde-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="60dde-121">Minimum supported server</span></span><br/> | <span data-ttu-id="60dde-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="60dde-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="60dde-123">Header</span><span class="sxs-lookup"><span data-stu-id="60dde-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="60dde-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="60dde-124"><dt>Commctrl.h</dt></span></span> </dl> |



 


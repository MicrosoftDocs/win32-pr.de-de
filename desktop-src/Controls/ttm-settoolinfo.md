---
title: TTM_SETTOOLINFO Meldung (kommstrg. h)
description: Legt die Informationen fest, die ein QuickInfo-Steuerelement für ein Tool verwaltet.
ms.assetid: ba18f651-2e52-46e2-871b-c1760e94ab59
keywords:
- Windows-Steuerelemente für TTM_SETTOOLINFO Meldung
topic_type:
- apiref
api_name:
- TTM_SETTOOLINFO
- TTM_SETTOOLINFOA
- TTM_SETTOOLINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 327dd853e3304f8233b95c947a890c4f49298cc7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478951"
---
# <a name="ttm_settoolinfo-message"></a><span data-ttu-id="cf04e-104">TTM- \_ SetToolInfo-Meldung</span><span class="sxs-lookup"><span data-stu-id="cf04e-104">TTM\_SETTOOLINFO message</span></span>

<span data-ttu-id="cf04e-105">Legt die Informationen fest, die ein QuickInfo-Steuerelement für ein Tool verwaltet.</span><span class="sxs-lookup"><span data-stu-id="cf04e-105">Sets the information that a tooltip control maintains for a tool.</span></span>

## <a name="parameters"></a><span data-ttu-id="cf04e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf04e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf04e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cf04e-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="cf04e-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="cf04e-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="cf04e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cf04e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cf04e-110">Ein Zeiger auf eine [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur, die die festzulegenden Informationen angibt.</span><span class="sxs-lookup"><span data-stu-id="cf04e-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure that specifies the information to set.</span></span> <span data-ttu-id="cf04e-111">Der **CBSIZE** -Member dieser Struktur muss vor dem Senden dieser Nachricht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="cf04e-111">The **cbSize** member of this structure must be set before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf04e-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cf04e-112">Return value</span></span>

<span data-ttu-id="cf04e-113">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="cf04e-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf04e-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf04e-114">Remarks</span></span>

<span data-ttu-id="cf04e-115">Einige interne Eigenschaften eines Tools werden erstellt, wenn das Tool erstellt wird, und werden nicht neu berechnet, wenn eine **TTM- \_ SetToolInfo** -Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="cf04e-115">Some internal properties of a tool are established when the tool is created, and are not recomputed when a **TTM\_SETTOOLINFO** message is sent.</span></span> <span data-ttu-id="cf04e-116">Wenn Sie einer [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur einfach Werte zuweisen und Sie mit einer **TTM- \_ SetToolInfo** -Meldung an das QuickInfo-Steuerelement übergeben, gehen diese Eigenschaften möglicherweise verloren.</span><span class="sxs-lookup"><span data-stu-id="cf04e-116">If you simply assign values to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure and pass it to the tooltip control with a **TTM\_SETTOOLINFO** message, these properties may be lost.</span></span> <span data-ttu-id="cf04e-117">Stattdessen sollte die Anwendung zuerst die aktuelle **toolinfo** -Struktur des Tools anfordern, indem das QuickInfo-Steuerelement eine [**TTM \_ gettoolinfo**](ttm-gettoolinfo.md) -Nachricht sendet.</span><span class="sxs-lookup"><span data-stu-id="cf04e-117">Instead, your application should first request the tool's current **TOOLINFO** structure by sending the tooltip control a [**TTM\_GETTOOLINFO**](ttm-gettoolinfo.md) message.</span></span> <span data-ttu-id="cf04e-118">Ändern Sie dann die Elemente dieser Struktur nach Bedarf, und übergeben Sie Sie mit **TTM \_ SetToolInfo** zurück an das QuickInfo-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="cf04e-118">Then, modify the members of this structure as needed and pass it back to the tooltip control with **TTM\_SETTOOLINFO**.</span></span>

<span data-ttu-id="cf04e-119">Beim Aufrufen von **TTM \_ SetToolInfo** darf die Zeichenfolge, auf die der **lpszText** -Member der [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur verweist, nicht länger als 80 **tchars** sein, einschließlich des abschließenden **null**-Werts.</span><span class="sxs-lookup"><span data-stu-id="cf04e-119">When calling **TTM\_SETTOOLINFO**, the string pointed to by the **lpszText** member of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure must not exceed 80 **TCHARs** in length, including the terminating **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf04e-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf04e-120">Requirements</span></span>



| <span data-ttu-id="cf04e-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cf04e-121">Requirement</span></span> | <span data-ttu-id="cf04e-122">Wert</span><span class="sxs-lookup"><span data-stu-id="cf04e-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cf04e-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cf04e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="cf04e-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf04e-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cf04e-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cf04e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="cf04e-126">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf04e-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cf04e-127">Header</span><span class="sxs-lookup"><span data-stu-id="cf04e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf04e-128"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf04e-128"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="cf04e-129">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="cf04e-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="cf04e-130">**TTM \_ Settoolinfow** (Unicode) und **TTM \_ settoolinfoa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="cf04e-130">**TTM\_SETTOOLINFOW** (Unicode) and **TTM\_SETTOOLINFOA** (ANSI)</span></span><br/>           |



 

 






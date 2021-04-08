---
title: RB_GETBANDBORDERS Meldung (kommstrg. h)
description: Ruft die Rahmen eines Bands ab. Das Ergebnis dieser Nachricht kann verwendet werden, um den nutzbaren Bereich in einem Band zu berechnen.
ms.assetid: 45f2ae7e-636e-474b-a0d0-5235c6401e6a
keywords:
- Windows-Steuerelemente für RB_GETBANDBORDERS Meldung
topic_type:
- apiref
api_name:
- RB_GETBANDBORDERS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 521dfecaf5e2573b30f606b7b4d7ecdec9bd896d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956800"
---
# <a name="rb_getbandborders-message"></a><span data-ttu-id="cd76e-105">RB \_ getBandBorders-Meldung</span><span class="sxs-lookup"><span data-stu-id="cd76e-105">RB\_GETBANDBORDERS message</span></span>

<span data-ttu-id="cd76e-106">Ruft die Rahmen eines Bands ab.</span><span class="sxs-lookup"><span data-stu-id="cd76e-106">Retrieves the borders of a band.</span></span> <span data-ttu-id="cd76e-107">Das Ergebnis dieser Nachricht kann verwendet werden, um den nutzbaren Bereich in einem Band zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="cd76e-107">The result of this message can be used to calculate the usable area in a band.</span></span>

## <a name="parameters"></a><span data-ttu-id="cd76e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="cd76e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd76e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cd76e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cd76e-110">Der null basierte Index des Bands, für das die Rahmen abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="cd76e-110">Zero-based index of the band for which the borders will be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="cd76e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cd76e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cd76e-112">Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die die Band Rahmen empfängt.</span><span class="sxs-lookup"><span data-stu-id="cd76e-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that will receive the band borders.</span></span> <span data-ttu-id="cd76e-113">Wenn das Grund leisten-Steuerelement den [**RSB- \_ bandborder**](rebar-control-styles.md) -Stil hat, erhält jedes Element dieser Struktur die Anzahl der Pixel auf der entsprechenden Seite des Bands, die den Rahmen bilden.</span><span class="sxs-lookup"><span data-stu-id="cd76e-113">If the rebar control has the [**RBS\_BANDBORDERS**](rebar-control-styles.md) style, each member of this structure will receive the number of pixels, on the corresponding side of the band, that constitute the border.</span></span> <span data-ttu-id="cd76e-114">Wenn das Grund leisten-Steuerelement nicht den **RSB- \_ bandrahmenstil** hat, erhält nur das **linke** Element dieser Struktur gültige Informationen.</span><span class="sxs-lookup"><span data-stu-id="cd76e-114">If the rebar control does not have the **RBS\_BANDBORDERS** style, only the **left** member of this structure receives valid information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd76e-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cd76e-115">Return value</span></span>

<span data-ttu-id="cd76e-116">Der Rückgabewert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="cd76e-116">The return value is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd76e-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cd76e-117">Requirements</span></span>



| <span data-ttu-id="cd76e-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cd76e-118">Requirement</span></span> | <span data-ttu-id="cd76e-119">Wert</span><span class="sxs-lookup"><span data-stu-id="cd76e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cd76e-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cd76e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cd76e-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cd76e-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cd76e-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cd76e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cd76e-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cd76e-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cd76e-124">Header</span><span class="sxs-lookup"><span data-stu-id="cd76e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd76e-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd76e-125"><dt>Commctrl.h</dt></span></span> </dl> |



 


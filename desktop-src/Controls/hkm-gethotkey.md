---
title: HKM_GETHOTKEY Meldung (kommstrg. h)
description: Ruft den Code des virtuellen Schlüssels und die Modifiziererflags eines Abkürzungs Schlüssels von einem Steuerelement für den Hot Key ab.
ms.assetid: 8b061411-604d-46ea-a082-3eca2d47d992
keywords:
- Windows-Steuerelemente für HKM_GETHOTKEY Meldung
topic_type:
- apiref
api_name:
- HKM_GETHOTKEY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16e23e02f32a4dd6f82f61fd735688353f48ec19
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476320"
---
# <a name="hkm_gethotkey-message"></a><span data-ttu-id="c2a56-104">HKM- \_ GetHotKey-Nachricht</span><span class="sxs-lookup"><span data-stu-id="c2a56-104">HKM\_GETHOTKEY message</span></span>

<span data-ttu-id="c2a56-105">Ruft den Code des virtuellen Schlüssels und die Modifiziererflags eines Abkürzungs Schlüssels von einem Steuerelement für den Hot Key ab.</span><span class="sxs-lookup"><span data-stu-id="c2a56-105">Gets the virtual key code and modifier flags of a hot key from a hot key control.</span></span>

## <a name="parameters"></a><span data-ttu-id="c2a56-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2a56-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2a56-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c2a56-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c2a56-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="c2a56-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c2a56-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c2a56-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c2a56-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="c2a56-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2a56-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c2a56-111">Return value</span></span>

<span data-ttu-id="c2a56-112">Gibt den Code und die Modifiziererflags des virtuellen Schlüssels zurück.</span><span class="sxs-lookup"><span data-stu-id="c2a56-112">Returns the virtual key code and modifier flags.</span></span> <span data-ttu-id="c2a56-113">Das [**lobyzeichen**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) von [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ist der virtuelle Schlüsselcode der "Hot"-Taste.</span><span class="sxs-lookup"><span data-stu-id="c2a56-113">The [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) of the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is the virtual key code of the hot key.</span></span> <span data-ttu-id="c2a56-114">Das [**Hibyte**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) des **loworts** ist der schlüsselmodifizierer, der die Schlüssel angibt, die eine Kombination aus der Tastenkombination definieren.</span><span class="sxs-lookup"><span data-stu-id="c2a56-114">The [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) of the **LOWORD** is the key modifier that specifies the keys that define a hot key combination.</span></span> <span data-ttu-id="c2a56-115">Die Modifiziererflags können eine Kombination der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="c2a56-115">The modifier flags can be a combination of the following values.</span></span>



| <span data-ttu-id="c2a56-116">Wert</span><span class="sxs-lookup"><span data-stu-id="c2a56-116">Value</span></span>            | <span data-ttu-id="c2a56-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c2a56-117">Meaning</span></span>      |
|------------------|--------------|
| <span data-ttu-id="c2a56-118">hotkeyf \_ alt</span><span class="sxs-lookup"><span data-stu-id="c2a56-118">HOTKEYF\_ALT</span></span>     | <span data-ttu-id="c2a56-119">ALT-TASTE</span><span class="sxs-lookup"><span data-stu-id="c2a56-119">ALT key</span></span>      |
| <span data-ttu-id="c2a56-120">hotkeyf- \_ Steuerelement</span><span class="sxs-lookup"><span data-stu-id="c2a56-120">HOTKEYF\_CONTROL</span></span> | <span data-ttu-id="c2a56-121">Steuerelement Taste</span><span class="sxs-lookup"><span data-stu-id="c2a56-121">CONTROL key</span></span>  |
| <span data-ttu-id="c2a56-122">hotkeyf \_ ext</span><span class="sxs-lookup"><span data-stu-id="c2a56-122">HOTKEYF\_EXT</span></span>     | <span data-ttu-id="c2a56-123">Erweiterter Schlüssel</span><span class="sxs-lookup"><span data-stu-id="c2a56-123">Extended key</span></span> |
| <span data-ttu-id="c2a56-124">hotkeyf- \_ Verschiebung</span><span class="sxs-lookup"><span data-stu-id="c2a56-124">HOTKEYF\_SHIFT</span></span>   | <span data-ttu-id="c2a56-125">Umschalttaste</span><span class="sxs-lookup"><span data-stu-id="c2a56-125">SHIFT key</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="c2a56-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c2a56-126">Remarks</span></span>

<span data-ttu-id="c2a56-127">Der 16-Bit-Wert, der von dieser Nachricht zurückgegeben wird, kann als *wParam* -Parameter in der [**WM \_ -**](/windows/desktop/inputdev/wm-sethotkey) Nachricht "\*" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c2a56-127">The 16-bit value returned by this message can be used as the *wParam* parameter in the [**WM\_SETHOTKEY**](/windows/desktop/inputdev/wm-sethotkey) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2a56-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2a56-128">Requirements</span></span>



| <span data-ttu-id="c2a56-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c2a56-129">Requirement</span></span> | <span data-ttu-id="c2a56-130">Wert</span><span class="sxs-lookup"><span data-stu-id="c2a56-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c2a56-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c2a56-131">Minimum supported client</span></span><br/> | <span data-ttu-id="c2a56-132">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c2a56-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c2a56-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c2a56-133">Minimum supported server</span></span><br/> | <span data-ttu-id="c2a56-134">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c2a56-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c2a56-135">Header</span><span class="sxs-lookup"><span data-stu-id="c2a56-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2a56-136"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2a56-136"><dt>Commctrl.h</dt></span></span> </dl> |



 


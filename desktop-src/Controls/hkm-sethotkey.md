---
title: HKM_SETHOTKEY Meldung (kommstrg. h)
description: Legt die Tastenkombination für ein Hot Key-Steuerelement fest.
ms.assetid: 372a7b2f-d9d5-43a8-9c06-730f2f5dc56e
keywords:
- Windows-Steuerelemente für HKM_SETHOTKEY Meldung
topic_type:
- apiref
api_name:
- HKM_SETHOTKEY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3672136c44c0268e218e7f87cbbeb3373b76b39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517651"
---
# <a name="hkm_sethotkey-message"></a><span data-ttu-id="0261b-104">HKM-Nachricht für " \_ abkthotkey"</span><span class="sxs-lookup"><span data-stu-id="0261b-104">HKM\_SETHOTKEY message</span></span>

<span data-ttu-id="0261b-105">Legt die Tastenkombination für ein Hot Key-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="0261b-105">Sets the hot key combination for a hot key control.</span></span>

## <a name="parameters"></a><span data-ttu-id="0261b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0261b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0261b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0261b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0261b-108">Das [**lobyzeichen**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) von [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ist der virtuelle Schlüsselcode der "Hot"-Taste.</span><span class="sxs-lookup"><span data-stu-id="0261b-108">The [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) of the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is the virtual key code of the hot key.</span></span> <span data-ttu-id="0261b-109">Das [**Hibyte**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) des **loworts** ist der schlüsselmodifizierer, der die Schlüssel angibt, die eine Kombination aus der Tastenkombination definieren.</span><span class="sxs-lookup"><span data-stu-id="0261b-109">The [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) of the **LOWORD** is the key modifier that indicates the keys that define a hot key combination.</span></span> <span data-ttu-id="0261b-110">Eine Liste der modifiziererflagwerte finden Sie in der Beschreibung der [**HKM \_ GetHotKey**](hkm-gethotkey.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="0261b-110">For a list of modifier flag values, see the description of the [**HKM\_GETHOTKEY**](hkm-gethotkey.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="0261b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0261b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0261b-112">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="0261b-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0261b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0261b-113">Return value</span></span>

<span data-ttu-id="0261b-114">Es wird immer NULL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0261b-114">Always returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="0261b-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0261b-115">Requirements</span></span>



| <span data-ttu-id="0261b-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0261b-116">Requirement</span></span> | <span data-ttu-id="0261b-117">Wert</span><span class="sxs-lookup"><span data-stu-id="0261b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0261b-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0261b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0261b-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0261b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0261b-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0261b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0261b-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0261b-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0261b-122">Header</span><span class="sxs-lookup"><span data-stu-id="0261b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0261b-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="0261b-123"><dt>Commctrl.h</dt></span></span> </dl> |



 


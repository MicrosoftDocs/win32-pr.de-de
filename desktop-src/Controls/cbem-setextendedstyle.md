---
title: CBEM_SETEXTENDEDSTYLE Meldung (kommstrg. h)
description: Legt erweiterte Stile innerhalb eines ComboBoxEx-Steuer Elements fest.
ms.assetid: 00848bd0-5a2f-4bfb-ae1f-ee3aa88ac57a
keywords:
- Windows-Steuerelemente für CBEM_SETEXTENDEDSTYLE Meldung
topic_type:
- apiref
api_name:
- CBEM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0a60518d2f6130c2c89e379125308fc2e647c6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339371"
---
# <a name="cbem_setextendedstyle-message"></a><span data-ttu-id="b7840-104">CBEM- \_ textendedstyle-Meldung</span><span class="sxs-lookup"><span data-stu-id="b7840-104">CBEM\_SETEXTENDEDSTYLE message</span></span>

<span data-ttu-id="b7840-105">Legt erweiterte Stile innerhalb eines ComboBoxEx-Steuer Elements fest.</span><span class="sxs-lookup"><span data-stu-id="b7840-105">Sets extended styles within a ComboBoxEx control.</span></span>

## <a name="parameters"></a><span data-ttu-id="b7840-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7840-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7840-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b7840-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b7840-108">Ein **DWORD** -Wert, der angibt, welche Stile in *LPARAM* betroffen sein sollen.</span><span class="sxs-lookup"><span data-stu-id="b7840-108">A **DWORD** value that indicates which styles in *lParam* are to be affected.</span></span> <span data-ttu-id="b7840-109">Nur die erweiterten Stile in *wParam* werden geändert.</span><span class="sxs-lookup"><span data-stu-id="b7840-109">Only the extended styles in *wParam* will be changed.</span></span> <span data-ttu-id="b7840-110">Wenn dieser Parameter 0 (null) ist, werden alle Stile in *LPARAM* beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="b7840-110">If this parameter is zero, then all of the styles in *lParam* will be affected.</span></span>

</dd> <dt>

<span data-ttu-id="b7840-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b7840-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b7840-112">Ein **DWORD** -Wert, der das [ComboBoxEx-Steuer](comboboxex-control-extended-styles.md) Element enthält, das für das Steuerelement festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b7840-112">A **DWORD** value that contains the [ComboBoxEx Control Extended Styles](comboboxex-control-extended-styles.md) to set for the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7840-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b7840-113">Return value</span></span>

<span data-ttu-id="b7840-114">Gibt einen **DWORD** -Wert zurück, der die erweiterten Stile enthält, die zuvor für das Steuerelement verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="b7840-114">Returns a **DWORD** value that contains the extended styles previously used for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7840-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b7840-115">Remarks</span></span>

<span data-ttu-id="b7840-116">mit *wParam* können Sie einen oder mehrere erweiterte Stile ändern, ohne zuerst die vorhandenen Stile abrufen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="b7840-116">*wParam* enables you to modify one or more extended styles without having to retrieve the existing styles first.</span></span> <span data-ttu-id="b7840-117">Wenn Sie z. b. [**CBEs \_ Ex \_ noeditimage**](comboboxex-control-extended-styles.md) für *wParam* und 0 für *LPARAM* übergeben, wird der Stil **CBEs \_ Ex \_ noeditimage** gelöscht, aber alle anderen Stile bleiben unverändert.</span><span class="sxs-lookup"><span data-stu-id="b7840-117">For example, if you pass [**CBES\_EX\_NOEDITIMAGE**](comboboxex-control-extended-styles.md) for *wParam* and 0 for *lParam*, the **CBES\_EX\_NOEDITIMAGE** style will be cleared, but all other styles will remain the same.</span></span>

<span data-ttu-id="b7840-118">Wenn Sie versuchen, einen erweiterten Stil für ein ComboBoxEx-Steuerelement festzulegen, das mit dem [**\_ einfachen CBS**](combo-box-styles.md) -Stil erstellt wurde, wird es möglicherweise nicht ordnungsgemäß neu gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="b7840-118">If you try to set an extended style for a ComboBoxEx control created with the [**CBS\_SIMPLE**](combo-box-styles.md) style, it may not repaint properly.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7840-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b7840-119">Requirements</span></span>



| <span data-ttu-id="b7840-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b7840-120">Requirement</span></span> | <span data-ttu-id="b7840-121">Wert</span><span class="sxs-lookup"><span data-stu-id="b7840-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b7840-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b7840-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b7840-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b7840-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b7840-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b7840-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b7840-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b7840-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b7840-126">Header</span><span class="sxs-lookup"><span data-stu-id="b7840-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7840-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7840-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






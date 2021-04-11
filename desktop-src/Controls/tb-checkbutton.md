---
title: TB_CHECKBUTTON Meldung (kommstrg. h)
description: Überprüft oder überprüft eine angegebene Schaltfläche in einer Symbolleiste.
ms.assetid: e67734a9-851c-41ab-8ad7-15d434f58e5a
keywords:
- Windows-Steuerelemente für TB_CHECKBUTTON Meldung
topic_type:
- apiref
api_name:
- TB_CHECKBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7734b37da44db38d9ca09b34ad9e666cc90eb5b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104041014"
---
# <a name="tb_checkbutton-message"></a><span data-ttu-id="328f5-104">TB \_ checkbutton-Meldung</span><span class="sxs-lookup"><span data-stu-id="328f5-104">TB\_CHECKBUTTON message</span></span>

<span data-ttu-id="328f5-105">Überprüft oder überprüft eine angegebene Schaltfläche in einer Symbolleiste.</span><span class="sxs-lookup"><span data-stu-id="328f5-105">Checks or unchecks a given button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="328f5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="328f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="328f5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="328f5-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="328f5-108">Der Befehls Bezeichner der zu Überprüfung enden Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="328f5-108">Command identifier of the button to check.</span></span>

</dd> <dt>

<span data-ttu-id="328f5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="328f5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="328f5-110">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ist ein **boolescher** Wert, der angibt, ob die angegebene Schaltfläche überprüft oder nicht überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="328f5-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **BOOL** that indicates whether to check or uncheck the specified button.</span></span> <span data-ttu-id="328f5-111">**True** gibt an, dass die Überprüfung hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="328f5-111">If **TRUE**, the check is added.</span></span> <span data-ttu-id="328f5-112">Wenn der Wert **false** ist, wird die Überprüfung entfernt.</span><span class="sxs-lookup"><span data-stu-id="328f5-112">If **FALSE**, the check is removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="328f5-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="328f5-113">Return value</span></span>

<span data-ttu-id="328f5-114">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="328f5-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="328f5-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="328f5-115">Remarks</span></span>

<span data-ttu-id="328f5-116">Wenn eine Schaltfläche aktiviert ist, wird Sie im gedrückten Zustand angezeigt.</span><span class="sxs-lookup"><span data-stu-id="328f5-116">When a button is checked, it is displayed in the pressed state.</span></span>

## <a name="requirements"></a><span data-ttu-id="328f5-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="328f5-117">Requirements</span></span>



| <span data-ttu-id="328f5-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="328f5-118">Requirement</span></span> | <span data-ttu-id="328f5-119">Wert</span><span class="sxs-lookup"><span data-stu-id="328f5-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="328f5-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="328f5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="328f5-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="328f5-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="328f5-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="328f5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="328f5-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="328f5-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="328f5-124">Header</span><span class="sxs-lookup"><span data-stu-id="328f5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="328f5-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="328f5-125"><dt>Commctrl.h</dt></span></span> </dl> |



 


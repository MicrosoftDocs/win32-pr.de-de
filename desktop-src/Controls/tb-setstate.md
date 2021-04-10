---
title: TB_SETSTATE Meldung (kommstrg. h)
description: Legt den Zustand für die angegebene Schaltfläche in einer Symbolleiste fest.
ms.assetid: 68633b58-8d21-4931-b01f-32a66bda37b1
keywords:
- Windows-Steuerelemente für TB_SETSTATE Meldung
topic_type:
- apiref
api_name:
- TB_SETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7aa46dc68d9af5559e580e697bf6893b15051cff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106587"
---
# <a name="tb_setstate-message"></a><span data-ttu-id="7e258-104">TB- \_ SetState-Meldung</span><span class="sxs-lookup"><span data-stu-id="7e258-104">TB\_SETSTATE message</span></span>

<span data-ttu-id="7e258-105">Legt den Zustand für die angegebene Schaltfläche in einer Symbolleiste fest.</span><span class="sxs-lookup"><span data-stu-id="7e258-105">Sets the state for the specified button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="7e258-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e258-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e258-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7e258-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7e258-108">Der Befehls Bezeichner der Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="7e258-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="7e258-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7e258-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7e258-110">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ist eine Kombination von Werten, die in den Status der Symbolleisten- [Schalt](toolbar-button-states.md)Flächen</span><span class="sxs-lookup"><span data-stu-id="7e258-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a combination of values listed in [Toolbar Button States](toolbar-button-states.md).</span></span> <span data-ttu-id="7e258-111">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="7e258-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e258-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7e258-112">Return value</span></span>

<span data-ttu-id="7e258-113">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="7e258-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e258-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7e258-114">Requirements</span></span>



| <span data-ttu-id="7e258-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7e258-115">Requirement</span></span> | <span data-ttu-id="7e258-116">Wert</span><span class="sxs-lookup"><span data-stu-id="7e258-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7e258-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7e258-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7e258-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7e258-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7e258-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7e258-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7e258-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7e258-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7e258-121">Header</span><span class="sxs-lookup"><span data-stu-id="7e258-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e258-122"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e258-122"><dt>Commctrl.h</dt></span></span> </dl> |



 


---
title: LVM_SETCOLUMNORDERARRAY Meldung (kommstrg. h)
description: Legt die Reihenfolge der Spalten in einem Listenansicht-Steuerelement von links nach rechts fest. Sie können diese Nachricht explizit senden oder das ListView \_ setcolumnorderarray-Makro verwenden.
ms.assetid: 9b491832-42cc-4262-8f6c-23cbc2c889bf
keywords:
- Windows-Steuerelemente für LVM_SETCOLUMNORDERARRAY Meldung
topic_type:
- apiref
api_name:
- LVM_SETCOLUMNORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94fdeb27074a3f6762e7fb3788fd7ccc0a2dcc5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040099"
---
# <a name="lvm_setcolumnorderarray-message"></a><span data-ttu-id="b8c99-105">LVM- \_ setcolumnorderarray-Meldung</span><span class="sxs-lookup"><span data-stu-id="b8c99-105">LVM\_SETCOLUMNORDERARRAY message</span></span>

<span data-ttu-id="b8c99-106">Legt die Reihenfolge der Spalten in einem Listenansicht-Steuerelement von links nach rechts fest.</span><span class="sxs-lookup"><span data-stu-id="b8c99-106">Sets the left-to-right order of columns in a list-view control.</span></span> <span data-ttu-id="b8c99-107">Sie können diese Nachricht explizit senden oder das [**ListView \_ setcolumnorderarray**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumnorderarray) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="b8c99-107">You can send this message explicitly or use the [**ListView\_SetColumnOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumnorderarray) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b8c99-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b8c99-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8c99-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b8c99-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b8c99-110">Größe des Puffers in *LPARAM* in-Elementen.</span><span class="sxs-lookup"><span data-stu-id="b8c99-110">Size, in elements, of the buffer at *lParam*.</span></span>

</dd> <dt>

<span data-ttu-id="b8c99-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b8c99-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b8c99-112">Zeiger auf ein Array, das die Reihenfolge angibt, in der Spalten von links nach rechts angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b8c99-112">Pointer to an array that specifies the order in which columns should be displayed, from left to right.</span></span> <span data-ttu-id="b8c99-113">Wenn der Inhalt des Arrays beispielsweise {2,0,1} ist, zeigt das Steuerelement Spalte 2, Spalte 0 und Spalte 1 in dieser Reihenfolge an.</span><span class="sxs-lookup"><span data-stu-id="b8c99-113">For example, if the contents of the array are {2,0,1}, the control displays column 2, column 0, and column 1 in that order.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8c99-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b8c99-114">Return value</span></span>

<span data-ttu-id="b8c99-115">Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="b8c99-115">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8c99-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b8c99-116">Requirements</span></span>



| <span data-ttu-id="b8c99-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b8c99-117">Requirement</span></span> | <span data-ttu-id="b8c99-118">Wert</span><span class="sxs-lookup"><span data-stu-id="b8c99-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b8c99-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b8c99-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b8c99-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b8c99-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b8c99-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b8c99-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b8c99-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b8c99-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b8c99-123">Header</span><span class="sxs-lookup"><span data-stu-id="b8c99-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8c99-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8c99-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






---
title: LVM_GETCOLUMNWIDTH Meldung (kommstrg. h)
description: Ruft die Breite einer Spalte in der Berichts-oder Listenansicht ab. Sie können diese Nachricht explizit oder mithilfe des ListView \_ getColumnWidth-Makros senden.
ms.assetid: 06e8ec36-3bc5-4516-ac29-17c36fb6d962
keywords:
- Windows-Steuerelemente für LVM_GETCOLUMNWIDTH Meldung
topic_type:
- apiref
api_name:
- LVM_GETCOLUMNWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0577e7cb2a589c432d4b5ca62f640de61d67dc75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102899"
---
# <a name="lvm_getcolumnwidth-message"></a><span data-ttu-id="f0a93-105">LVM \_ getColumnWidth-Nachricht</span><span class="sxs-lookup"><span data-stu-id="f0a93-105">LVM\_GETCOLUMNWIDTH message</span></span>

<span data-ttu-id="f0a93-106">Ruft die Breite einer Spalte in der Berichts-oder Listenansicht ab.</span><span class="sxs-lookup"><span data-stu-id="f0a93-106">Gets the width of a column in report or list view.</span></span> <span data-ttu-id="f0a93-107">Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ getColumnWidth**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumnwidth) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="f0a93-107">You can send this message explicitly or by using the [**ListView\_GetColumnWidth**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumnwidth) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f0a93-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0a93-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0a93-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f0a93-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f0a93-110">Der Index der Spalte.</span><span class="sxs-lookup"><span data-stu-id="f0a93-110">The index of the column.</span></span> <span data-ttu-id="f0a93-111">Dieser Parameter wird in der Listenansicht ignoriert.</span><span class="sxs-lookup"><span data-stu-id="f0a93-111">This parameter is ignored in list view.</span></span>

</dd> <dt>

<span data-ttu-id="f0a93-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f0a93-112">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f0a93-113">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="f0a93-113">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0a93-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f0a93-114">Return value</span></span>

<span data-ttu-id="f0a93-115">Gibt die Spaltenbreite zurück, wenn erfolgreich, andernfalls 0 (null).</span><span class="sxs-lookup"><span data-stu-id="f0a93-115">Returns the column width if successful, or zero otherwise.</span></span> <span data-ttu-id="f0a93-116">Wenn diese Nachricht an ein Listenansicht-Steuerelement mit dem [**LVS- \_ Berichts**](list-view-window-styles.md) Stil gesendet wird und die angegebene Spalte nicht vorhanden ist, ist der Rückgabewert nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="f0a93-116">If this message is sent to a list-view control with the [**LVS\_REPORT**](list-view-window-styles.md) style and the specified column does not exist, the return value is undefined.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0a93-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f0a93-117">Requirements</span></span>



| <span data-ttu-id="f0a93-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f0a93-118">Requirement</span></span> | <span data-ttu-id="f0a93-119">Wert</span><span class="sxs-lookup"><span data-stu-id="f0a93-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f0a93-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f0a93-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f0a93-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f0a93-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f0a93-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f0a93-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f0a93-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f0a93-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f0a93-124">Header</span><span class="sxs-lookup"><span data-stu-id="f0a93-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0a93-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0a93-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






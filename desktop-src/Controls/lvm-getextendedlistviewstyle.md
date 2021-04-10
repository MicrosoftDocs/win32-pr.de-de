---
title: LVM_GETEXTENDEDLISTVIEWSTYLE Meldung (kommstrg. h)
description: Ruft die erweiterten Stile ab, die zurzeit für ein angegebenes Listenansicht-Steuerelement verwendet werden. Sie können diese Nachricht explizit senden oder das ListView \_ getextendedlistviewstyle-Makro verwenden.
ms.assetid: 5cfccdb8-a81c-4fa9-a4fa-19cf49bd6ce0
keywords:
- Windows-Steuerelemente für LVM_GETEXTENDEDLISTVIEWSTYLE Meldung
topic_type:
- apiref
api_name:
- LVM_GETEXTENDEDLISTVIEWSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 273da9e7eac85475b90ad05dc5fdd7f70d524562
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040103"
---
# <a name="lvm_getextendedlistviewstyle-message"></a><span data-ttu-id="8d516-105">LVM \_ getextendedlistviewstyle-Meldung</span><span class="sxs-lookup"><span data-stu-id="8d516-105">LVM\_GETEXTENDEDLISTVIEWSTYLE message</span></span>

<span data-ttu-id="8d516-106">Ruft die erweiterten Stile ab, die zurzeit für ein angegebenes Listenansicht-Steuerelement verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8d516-106">Gets the extended styles that are currently in use for a given list-view control.</span></span> <span data-ttu-id="8d516-107">Sie können diese Nachricht explizit senden oder das [**ListView \_ getextendedlistviewstyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getextendedlistviewstyle) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="8d516-107">You can send this message explicitly or use the [**ListView\_GetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getextendedlistviewstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8d516-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d516-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d516-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8d516-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8d516-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="8d516-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8d516-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8d516-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="8d516-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="8d516-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d516-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8d516-113">Return value</span></span>

<span data-ttu-id="8d516-114">Gibt ein **DWORD** zurück, das die derzeit für ein angegebenes Listenansicht-Steuerelement verwendeten Stile darstellt.</span><span class="sxs-lookup"><span data-stu-id="8d516-114">Returns a **DWORD** that represents the styles currently in use for a given list-view control.</span></span> <span data-ttu-id="8d516-115">Bei diesem Wert kann es sich um eine Kombination aus [erweiterten List-View Stilen](extended-list-view-styles.md)handeln.</span><span class="sxs-lookup"><span data-stu-id="8d516-115">This value can be a combination of [Extended List-View Styles](extended-list-view-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8d516-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8d516-116">Requirements</span></span>



| <span data-ttu-id="8d516-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8d516-117">Requirement</span></span> | <span data-ttu-id="8d516-118">Wert</span><span class="sxs-lookup"><span data-stu-id="8d516-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8d516-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8d516-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8d516-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8d516-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8d516-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8d516-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8d516-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8d516-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8d516-123">Header</span><span class="sxs-lookup"><span data-stu-id="8d516-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d516-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d516-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






---
title: HDM_GETITEMRECT Meldung (kommstrg. h)
description: Ruft das umgebende Rechteck für ein angegebenes Element in einem Header Steuerelement ab. Sie können diese Nachricht explizit senden oder das-Header \_ GetItemRect-Makro verwenden.
ms.assetid: b483ef97-3700-425b-8160-81c673850f68
keywords:
- Windows-Steuerelemente für HDM_GETITEMRECT Meldung
topic_type:
- apiref
api_name:
- HDM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4baec72bd914a9d2dad72556a5444c0059452cf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477583"
---
# <a name="hdm_getitemrect-message"></a><span data-ttu-id="6b019-105">HDM- \_ GetItemRect-Nachricht</span><span class="sxs-lookup"><span data-stu-id="6b019-105">HDM\_GETITEMRECT message</span></span>

<span data-ttu-id="6b019-106">Ruft das umgebende Rechteck für ein angegebenes Element in einem Header Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="6b019-106">Gets the bounding rectangle for a given item in a header control.</span></span> <span data-ttu-id="6b019-107">Sie können diese Nachricht explizit senden oder das- [**Header \_ GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemrect) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="6b019-107">You can send this message explicitly or use the [**Header\_GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6b019-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b019-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b019-109">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b019-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b019-110">Der null basierte Index des Header Steuerelement Elements, für das das umgebende Rechteck abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="6b019-110">The zero-based index of the header control item for which to retrieve the bounding rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="6b019-111">*LPARAM* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6b019-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b019-112">Ein Zeiger auf eine [**Rect**](/windows/win32/api/windef/ns-windef-rect) -Struktur, die die umschließenden Rechteck Informationen empfängt.</span><span class="sxs-lookup"><span data-stu-id="6b019-112">A pointer to a [**RECT**](/windows/win32/api/windef/ns-windef-rect) structure that receives the bounding rectangle information.</span></span> <span data-ttu-id="6b019-113">Der Absender der Nachricht ist für die Zuordnung dieser Struktur verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="6b019-113">The message sender is responsible for allocating this structure.</span></span> <span data-ttu-id="6b019-114">Die in der Rect-Struktur zurückgegebenen Koordinaten werden relativ zum übergeordneten Header Steuerelement ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="6b019-114">The coordinates returned in the RECT structure are expressed relative to the header control parent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b019-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6b019-115">Return value</span></span>

<span data-ttu-id="6b019-116">Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="6b019-116">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b019-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b019-117">Requirements</span></span>



| <span data-ttu-id="6b019-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b019-118">Requirement</span></span> | <span data-ttu-id="6b019-119">Wert</span><span class="sxs-lookup"><span data-stu-id="6b019-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6b019-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6b019-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6b019-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b019-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6b019-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6b019-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6b019-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b019-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6b019-124">Header</span><span class="sxs-lookup"><span data-stu-id="6b019-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b019-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b019-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






---
title: CB_SETHORIZONTALEXTENT Meldung (Winuser. h)
description: Eine Anwendung sendet die CB \_ sethorizontalblock-Nachricht, um die Breite (in Pixel) festzulegen, um die ein Listenfeld Horizontal (die Bild lauffähigen Breite) gescrollt werden kann.
ms.assetid: 85e8ff4f-ad9a-451c-b791-bd442b32d716
keywords:
- Windows-Steuerelemente für CB_SETHORIZONTALEXTENT Meldung
topic_type:
- apiref
api_name:
- CB_SETHORIZONTALEXTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f51e505f36f7cfd3fa47644a288db4a97ba89ca4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476629"
---
# <a name="cb_sethorizontalextent-message"></a><span data-ttu-id="a84b9-104">CB- \_ Nachricht "logthorizontalblock"</span><span class="sxs-lookup"><span data-stu-id="a84b9-104">CB\_SETHORIZONTALEXTENT message</span></span>

<span data-ttu-id="a84b9-105">Eine Anwendung sendet die **CB \_ sethorizontalblock** -Nachricht, um die Breite (in Pixel) festzulegen, um die ein Listenfeld Horizontal (die Bild lauffähigen Breite) gescrollt werden kann.</span><span class="sxs-lookup"><span data-stu-id="a84b9-105">An application sends the **CB\_SETHORIZONTALEXTENT** message to set the width, in pixels, by which a list box can be scrolled horizontally (the scrollable width).</span></span> <span data-ttu-id="a84b9-106">Wenn die Breite des Listen Felds kleiner als dieser Wert ist, führt die horizontale Schiebe Leiste einen horizontalen Bildlauf durch Elemente im Listenfeld aus.</span><span class="sxs-lookup"><span data-stu-id="a84b9-106">If the width of the list box is smaller than this value, the horizontal scroll bar horizontally scrolls items in the list box.</span></span> <span data-ttu-id="a84b9-107">Wenn die Breite des Listen Felds gleich oder größer als dieser Wert ist, wird die horizontale Schiebe Leiste ausgeblendet, oder, wenn das Kombinations Feld den Wert für die [**CBS- \_ Deaktivierung**](combo-box-styles.md) hat, deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="a84b9-107">If the width of the list box is equal to or greater than this value, the horizontal scroll bar is hidden or, if the combo box has the [**CBS\_DISABLENOSCROLL**](combo-box-styles.md) style, disabled.</span></span>

## <a name="parameters"></a><span data-ttu-id="a84b9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a84b9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a84b9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a84b9-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a84b9-110">Gibt die scrollbare Breite des Listen Felds in Pixel an.</span><span class="sxs-lookup"><span data-stu-id="a84b9-110">Specifies the scrollable width of the list box, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="a84b9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a84b9-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a84b9-112">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a84b9-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a84b9-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a84b9-113">Requirements</span></span>



| <span data-ttu-id="a84b9-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a84b9-114">Requirement</span></span> | <span data-ttu-id="a84b9-115">Wert</span><span class="sxs-lookup"><span data-stu-id="a84b9-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a84b9-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a84b9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a84b9-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a84b9-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a84b9-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a84b9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a84b9-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a84b9-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a84b9-120">Header</span><span class="sxs-lookup"><span data-stu-id="a84b9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a84b9-121"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="a84b9-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a84b9-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a84b9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a84b9-123">**CB- \_ gethorizontalblock**</span><span class="sxs-lookup"><span data-stu-id="a84b9-123">**CB\_GETHORIZONTALEXTENT**</span></span>](cb-gethorizontalextent.md)
</dt> </dl>

 

 






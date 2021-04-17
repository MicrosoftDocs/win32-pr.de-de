---
title: TB_SETBITMAPSIZE Meldung (kommstrg. h)
description: Legt die Größe der bitzugeordneten Bilder fest, die einer Symbolleiste hinzugefügt werden sollen.
ms.assetid: 20b99cd8-6ef1-4037-92d2-c64a1003b5fe
keywords:
- Windows-Steuerelemente für TB_SETBITMAPSIZE Meldung
topic_type:
- apiref
api_name:
- TB_SETBITMAPSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d9c8a717151041fb83b7a0206acf570a6ad7f76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475138"
---
# <a name="tb_setbitmapsize-message"></a><span data-ttu-id="0ad67-104">TB \_ setbitmapsize-Meldung</span><span class="sxs-lookup"><span data-stu-id="0ad67-104">TB\_SETBITMAPSIZE message</span></span>

<span data-ttu-id="0ad67-105">Legt die Größe der bitzugeordneten Bilder fest, die einer Symbolleiste hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0ad67-105">Sets the size of the bitmapped images to be added to a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="0ad67-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ad67-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ad67-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0ad67-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0ad67-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="0ad67-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="0ad67-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0ad67-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0ad67-110">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt die Breite der bitzugeordneten Bilder in Pixel an.</span><span class="sxs-lookup"><span data-stu-id="0ad67-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the width, in pixels, of the bitmapped images.</span></span> <span data-ttu-id="0ad67-111">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt die Höhe der bitzugeordneten Bilder in Pixel an.</span><span class="sxs-lookup"><span data-stu-id="0ad67-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the height, in pixels, of the bitmapped images.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ad67-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0ad67-112">Return value</span></span>

<span data-ttu-id="0ad67-113">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="0ad67-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ad67-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0ad67-114">Remarks</span></span>

<span data-ttu-id="0ad67-115">Die Größe kann nur festgelegt werden, bevor der Symbolleiste Bitmaps hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="0ad67-115">The size can be set only before adding any bitmaps to the toolbar.</span></span> <span data-ttu-id="0ad67-116">Wenn eine Anwendung die Bitmapgröße nicht explizit festlegt, ist die Größe standardmäßig 16 x 15 Pixel.</span><span class="sxs-lookup"><span data-stu-id="0ad67-116">If an application does not explicitly set the bitmap size, the size defaults to 16 by 15 pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ad67-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0ad67-117">Requirements</span></span>



| <span data-ttu-id="0ad67-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0ad67-118">Requirement</span></span> | <span data-ttu-id="0ad67-119">Wert</span><span class="sxs-lookup"><span data-stu-id="0ad67-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0ad67-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0ad67-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0ad67-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0ad67-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0ad67-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0ad67-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0ad67-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0ad67-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0ad67-124">Header</span><span class="sxs-lookup"><span data-stu-id="0ad67-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ad67-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ad67-125"><dt>Commctrl.h</dt></span></span> </dl> |



 


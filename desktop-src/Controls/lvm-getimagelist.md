---
title: LVM_GETIMAGELIST Meldung (kommstrg. h)
description: Ruft das Handle für eine Bildliste ab, die zum Zeichnen von Listen Ansichts Elementen verwendet wird. Sie können diese Nachricht explizit oder mithilfe des ListView \_ GetImageList-Makros senden.
ms.assetid: dd48d8b5-6dbd-48ab-95c3-0fcf1e8c24f0
keywords:
- Windows-Steuerelemente für LVM_GETIMAGELIST Meldung
topic_type:
- apiref
api_name:
- LVM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0abc68c5e5dd9a18c3ec203ad7fe3db97a542845
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104451"
---
# <a name="lvm_getimagelist-message"></a><span data-ttu-id="47b6e-105">LVM \_ GetImageList-Meldung</span><span class="sxs-lookup"><span data-stu-id="47b6e-105">LVM\_GETIMAGELIST message</span></span>

<span data-ttu-id="47b6e-106">Ruft das Handle für eine Bildliste ab, die zum Zeichnen von Listen Ansichts Elementen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="47b6e-106">Retrieves the handle to an image list used for drawing list-view items.</span></span> <span data-ttu-id="47b6e-107">Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getimagelist) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="47b6e-107">You can send this message explicitly or by using the [**ListView\_GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="47b6e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="47b6e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47b6e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="47b6e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="47b6e-110">Abzurufende Bildliste.</span><span class="sxs-lookup"><span data-stu-id="47b6e-110">Image list to retrieve.</span></span> <span data-ttu-id="47b6e-111">Dieser Parameter kann einen der folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="47b6e-111">This parameter can be one of the following values:</span></span>



| <span data-ttu-id="47b6e-112">Wert</span><span class="sxs-lookup"><span data-stu-id="47b6e-112">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="47b6e-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="47b6e-113">Meaning</span></span>                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span id="LVSIL_NORMAL"></span><span id="lvsil_normal"></span><dl> <span data-ttu-id="47b6e-114"><dt>**lvsil \_ Normal**</dt></span><span class="sxs-lookup"><span data-stu-id="47b6e-114"><dt>**LVSIL\_NORMAL**</dt></span></span> </dl>                | <span data-ttu-id="47b6e-115">Bildliste mit großen Symbolen.</span><span class="sxs-lookup"><span data-stu-id="47b6e-115">Image list with large icons.</span></span><br/>  |
| <span id="LVSIL_SMALL"></span><span id="lvsil_small"></span><dl> <span data-ttu-id="47b6e-116"><dt>**lvsil \_ Small**</dt></span><span class="sxs-lookup"><span data-stu-id="47b6e-116"><dt>**LVSIL\_SMALL**</dt></span></span> </dl>                   | <span data-ttu-id="47b6e-117">Bildliste mit kleinen Symbolen.</span><span class="sxs-lookup"><span data-stu-id="47b6e-117">Image list with small icons.</span></span><br/>  |
| <span id="LVSIL_STATE"></span><span id="lvsil_state"></span><dl> <span data-ttu-id="47b6e-118"><dt>**Zustand "lvsil" \_**</dt></span><span class="sxs-lookup"><span data-stu-id="47b6e-118"><dt>**LVSIL\_STATE**</dt></span></span> </dl>                   | <span data-ttu-id="47b6e-119">Bildliste mit Zustands Bildern.</span><span class="sxs-lookup"><span data-stu-id="47b6e-119">Image list with state images.</span></span><br/> |
| <span id="LVSIL_GROUPHEADER"></span><span id="lvsil_groupheader"></span><dl> <span data-ttu-id="47b6e-120"><dt>**lvsil- \_ GroupHeader**</dt></span><span class="sxs-lookup"><span data-stu-id="47b6e-120"><dt>**LVSIL\_GROUPHEADER**</dt></span></span> </dl> | <span data-ttu-id="47b6e-121">Bildliste für Gruppen Kopfzeile.</span><span class="sxs-lookup"><span data-stu-id="47b6e-121">Image list for group header.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="47b6e-122">*lParam*</span><span class="sxs-lookup"><span data-stu-id="47b6e-122">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="47b6e-123">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="47b6e-123">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47b6e-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="47b6e-124">Return value</span></span>

<span data-ttu-id="47b6e-125">Gibt das Handle für die angegebene Bildliste zurück, wenn erfolgreich, andernfalls **null** .</span><span class="sxs-lookup"><span data-stu-id="47b6e-125">Returns the handle to the specified image list if successful, or **NULL** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="47b6e-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="47b6e-126">Requirements</span></span>



| <span data-ttu-id="47b6e-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="47b6e-127">Requirement</span></span> | <span data-ttu-id="47b6e-128">Wert</span><span class="sxs-lookup"><span data-stu-id="47b6e-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="47b6e-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="47b6e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="47b6e-130">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="47b6e-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="47b6e-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="47b6e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="47b6e-132">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="47b6e-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="47b6e-133">Header</span><span class="sxs-lookup"><span data-stu-id="47b6e-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="47b6e-134"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="47b6e-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






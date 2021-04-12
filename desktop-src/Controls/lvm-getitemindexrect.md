---
title: LVM_GETITEMINDEXRECT Meldung (kommstrg. h)
description: Ruft das umgebende Rechteck für den gesamten oder einen Teil eines unter Elements in der aktuellen Ansicht eines Listenansicht-Steuer Elements ab. Senden Sie diese Nachricht explizit oder mithilfe des ListView \_ getitemindexrect-Makros.
ms.assetid: 17704d24-c029-4d41-b198-04d1e78698e0
keywords:
- Windows-Steuerelemente für LVM_GETITEMINDEXRECT Meldung
topic_type:
- apiref
api_name:
- LVM_GETITEMINDEXRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31ccd114713326c4796ca69f56fc2c38daf145db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478522"
---
# <a name="lvm_getitemindexrect-message"></a><span data-ttu-id="b8997-105">LVM- \_ getitemindexrect-Nachricht</span><span class="sxs-lookup"><span data-stu-id="b8997-105">LVM\_GETITEMINDEXRECT message</span></span>

<span data-ttu-id="b8997-106">Ruft das umgebende Rechteck für den gesamten oder einen Teil eines unter Elements in der aktuellen Ansicht eines Listenansicht-Steuer Elements ab.</span><span class="sxs-lookup"><span data-stu-id="b8997-106">Retrieves the bounding rectangle for all or part of a subitem in the current view of a list-view control.</span></span> <span data-ttu-id="b8997-107">Senden Sie diese Nachricht explizit oder mithilfe des [**ListView \_ getitemindexrect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemindexrect) -Makros.</span><span class="sxs-lookup"><span data-stu-id="b8997-107">Send this message explicitly or by using the [**ListView\_GetItemIndexRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemindexrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b8997-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b8997-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8997-109">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b8997-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8997-110">Ein Zeiger auf eine [**lvitemindex**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) -Struktur für das übergeordnete Element des unter Elements.</span><span class="sxs-lookup"><span data-stu-id="b8997-110">A pointer to a [**LVITEMINDEX**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) structure for the parent item of the subitem.</span></span> <span data-ttu-id="b8997-111">Der Aufrufprozess ist dafür verantwortlich, diese Struktur zuzuordnen und deren Member festzulegen.</span><span class="sxs-lookup"><span data-stu-id="b8997-111">The calling process is responsible for allocating this structure and setting its members.</span></span> <span data-ttu-id="b8997-112">*wParam* darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="b8997-112">*wParam* must not be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b8997-113">*LPARAM* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b8997-113">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b8997-114">Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die die Koordinaten empfängt.</span><span class="sxs-lookup"><span data-stu-id="b8997-114">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to receive the coordinates.</span></span> <span data-ttu-id="b8997-115">Der Aufrufprozess ist für die Zuordnung dieser Struktur verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="b8997-115">The calling process is responsible for allocating this structure.</span></span> <span data-ttu-id="b8997-116">*LPARAM* darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="b8997-116">*lParam* must not be **NULL**.</span></span> <span data-ttu-id="b8997-117">Legen Sie den **obersten** Member auf den Index des unter Elements fest.</span><span class="sxs-lookup"><span data-stu-id="b8997-117">Set the **top** member to the index of the subitem.</span></span> <span data-ttu-id="b8997-118">Legen Sie den **linken** Member auf einen der folgenden Werte fest, um den Teil des unter Elements anzugeben, für das das umgebende Rechteck abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b8997-118">Set the **left** member to one of the following values, indicating the part of the subitem for which the bounding rectangle is to be retrieved.</span></span>



| <span data-ttu-id="b8997-119">Wert</span><span class="sxs-lookup"><span data-stu-id="b8997-119">Value</span></span>                                                                                                                                                   | <span data-ttu-id="b8997-120">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b8997-120">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="LVIR_BOUNDS"></span><span id="lvir_bounds"></span><dl> <span data-ttu-id="b8997-121"><dt>**lvir- \_ Begrenzungen**</dt></span><span class="sxs-lookup"><span data-stu-id="b8997-121"><dt>**LVIR\_BOUNDS**</dt></span></span> </dl> | <span data-ttu-id="b8997-122">Gibt das umgebende Rechteck des gesamten unter Elements zurück, einschließlich des Symbols und der Bezeichnung.</span><span class="sxs-lookup"><span data-stu-id="b8997-122">Returns the bounding rectangle of the entire subitem, including the icon and label.</span></span><br/> |
| <span id="LVIR_ICON"></span><span id="lvir_icon"></span><dl> <span data-ttu-id="b8997-123"><dt>**lvir- \_ Symbol**</dt></span><span class="sxs-lookup"><span data-stu-id="b8997-123"><dt>**LVIR\_ICON**</dt></span></span> </dl>       | <span data-ttu-id="b8997-124">Gibt das umgebende Rechteck des Symbols oder des kleinen Symbols des unter Elements zurück.</span><span class="sxs-lookup"><span data-stu-id="b8997-124">Returns the bounding rectangle of the icon or small icon of the subitem.</span></span><br/>            |
| <span id="LVIR_LABEL"></span><span id="lvir_label"></span><dl> <span data-ttu-id="b8997-125"><dt>**lvir- \_ Bezeichnung**</dt></span><span class="sxs-lookup"><span data-stu-id="b8997-125"><dt>**LVIR\_LABEL**</dt></span></span> </dl>    | <span data-ttu-id="b8997-126">Gibt das umgebende Rechteck des Unterelement Texts zurück.</span><span class="sxs-lookup"><span data-stu-id="b8997-126">Returns the bounding rectangle of the subitem text.</span></span><br/>                                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8997-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b8997-127">Return value</span></span>

<span data-ttu-id="b8997-128">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="b8997-128">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8997-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b8997-129">Requirements</span></span>



| <span data-ttu-id="b8997-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b8997-130">Requirement</span></span> | <span data-ttu-id="b8997-131">Wert</span><span class="sxs-lookup"><span data-stu-id="b8997-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b8997-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b8997-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b8997-133">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b8997-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b8997-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b8997-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b8997-135">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b8997-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b8997-136">Header</span><span class="sxs-lookup"><span data-stu-id="b8997-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8997-137"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8997-137"><dt>Commctrl.h</dt></span></span> </dl> |



 


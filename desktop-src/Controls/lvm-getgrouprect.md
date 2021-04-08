---
title: LVM_GETGROUPRECT Meldung (kommstrg. h)
description: Ruft das Rechteck für eine angegebene Gruppe ab. Senden Sie diese Nachricht explizit oder mithilfe des ListView \_ getgrouprect-Makros.
ms.assetid: 9441a6c5-11d8-4f52-80dd-1b60befd9b9d
keywords:
- Windows-Steuerelemente für LVM_GETGROUPRECT Meldung
topic_type:
- apiref
api_name:
- LVM_GETGROUPRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab2cbdfb1ec6e670e7b5d333694f3a1ca56d287b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949463"
---
# <a name="lvm_getgrouprect-message"></a><span data-ttu-id="0db02-105">LVM \_ getgrouprect-Nachricht</span><span class="sxs-lookup"><span data-stu-id="0db02-105">LVM\_GETGROUPRECT message</span></span>

<span data-ttu-id="0db02-106">Ruft das Rechteck für eine angegebene Gruppe ab.</span><span class="sxs-lookup"><span data-stu-id="0db02-106">Gets the rectangle for a specified group.</span></span> <span data-ttu-id="0db02-107">Senden Sie diese Nachricht explizit oder mithilfe des [**ListView \_ getgrouprect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgrouprect) -Makros.</span><span class="sxs-lookup"><span data-stu-id="0db02-107">Send this message explicitly or by using the [**ListView\_GetGroupRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgrouprect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0db02-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0db02-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0db02-109">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0db02-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0db02-110">Gibt die Group by **igroupid** an (siehe Struktur von " [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) ").</span><span class="sxs-lookup"><span data-stu-id="0db02-110">Specifies the group by **iGroupId** (see [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) structure).</span></span>

</dd> <dt>

<span data-ttu-id="0db02-111">*LPARAM* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0db02-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0db02-112">Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die Informationen über die von *wParam* angegebene Gruppe empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="0db02-112">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to receive information on the group specified by *wParam*.</span></span> <span data-ttu-id="0db02-113">Der Nachrichtenempfänger ist dafür verantwortlich, die Strukturmember mit Informationen für die von *wParam* angegebene Gruppe festzulegen.</span><span class="sxs-lookup"><span data-stu-id="0db02-113">The message receiver is responsible for setting the structure members with information for the group specified by *wParam*.</span></span>

<span data-ttu-id="0db02-114">Der Aufrufprozess ist für die Zuordnung von Arbeitsspeicher für die Struktur verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="0db02-114">The calling process is responsible for allocating memory for the structure.</span></span> <span data-ttu-id="0db02-115">Legen Sie den **obersten** Member des [**Rect**](/previous-versions//dd162897(v=vs.85)) auf eines der folgenden Flags fest, um die Koordinaten des Rechtecks anzugeben, das Sie erhalten möchten.</span><span class="sxs-lookup"><span data-stu-id="0db02-115">Set the **top** member of the [**RECT**](/previous-versions//dd162897(v=vs.85)) to one of the following flags to specify the coordinates of the rectangle to get.</span></span>



| <span data-ttu-id="0db02-116">Wert</span><span class="sxs-lookup"><span data-stu-id="0db02-116">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="0db02-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0db02-117">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVGGR_GROUP"></span><span id="lvggr_group"></span><dl> <span data-ttu-id="0db02-118"><dt>**Gruppe "lvggr" \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0db02-118"><dt>**LVGGR\_GROUP**</dt></span></span> </dl>                | <span data-ttu-id="0db02-119">Koordinaten der gesamten erweiterten Gruppe.</span><span class="sxs-lookup"><span data-stu-id="0db02-119">Coordinates of the entire expanded group.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="LVGGR_HEADER"></span><span id="lvggr_header"></span><dl> <span data-ttu-id="0db02-120"><dt>**lvggr- \_ Header**</dt></span><span class="sxs-lookup"><span data-stu-id="0db02-120"><dt>**LVGGR\_HEADER**</dt></span></span> </dl>             | <span data-ttu-id="0db02-121">Nur Koordinaten des Headers (reduzierte Gruppe).</span><span class="sxs-lookup"><span data-stu-id="0db02-121">Coordinates of the header only (collapsed group).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="LVGGR_LABEL"></span><span id="lvggr_label"></span><dl> <span data-ttu-id="0db02-122"><dt>**Bezeichnung "lvggr" \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0db02-122"><dt>**LVGGR\_LABEL**</dt></span></span> </dl>                | <span data-ttu-id="0db02-123">Nur Koordinaten der Bezeichnung.</span><span class="sxs-lookup"><span data-stu-id="0db02-123">Coordinates of the label only.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="LVGGR_SUBSETLINK"></span><span id="lvggr_subsetlink"></span><dl> <span data-ttu-id="0db02-124"><dt>**subsetlink für "lvggr" \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0db02-124"><dt>**LVGGR\_SUBSETLINK**</dt></span></span> </dl> | <span data-ttu-id="0db02-125">Nur Koordinaten der Teilmenge (Markup Teilmenge).</span><span class="sxs-lookup"><span data-stu-id="0db02-125">Coordinates of the subset link only (markup subset).</span></span> <span data-ttu-id="0db02-126">Ein Listenansicht-Steuerelement kann die Anzahl der sichtbaren Elemente einschränken, die in jeder Gruppe angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="0db02-126">A list-view control can limit the number of visible items displayed in each group.</span></span> <span data-ttu-id="0db02-127">Dem Benutzer wird ein Link angezeigt, mit dem der Benutzer die Gruppe erweitern kann.</span><span class="sxs-lookup"><span data-stu-id="0db02-127">A link is presented to the user to allow the user to expand the group.</span></span> <span data-ttu-id="0db02-128">Dieses Flag gibt das umgebende Rechteck der Teilmenge zurück, wenn es sich bei der Gruppe um eine Teilmenge handelt (Gruppenstatus der \_ untergeordneten Gruppen. [](/windows/win32/api/commctrl/ns-commctrl-lvgroup) </span><span class="sxs-lookup"><span data-stu-id="0db02-128">This flag will return the bounding rectangle of the subset link if the group is a subset (group state of LVGS\_SUBSETED, see structure [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup), member **state**).</span></span> <span data-ttu-id="0db02-129">Dieses Flag wird bereitgestellt, damit Barrierefreiheits Anwendungen den Link finden können.</span><span class="sxs-lookup"><span data-stu-id="0db02-129">This flag is provided so that accessibility applications can located the link.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0db02-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0db02-130">Return value</span></span>

<span data-ttu-id="0db02-131">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="0db02-131">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="0db02-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0db02-132">Requirements</span></span>



| <span data-ttu-id="0db02-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0db02-133">Requirement</span></span> | <span data-ttu-id="0db02-134">Wert</span><span class="sxs-lookup"><span data-stu-id="0db02-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0db02-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0db02-135">Minimum supported client</span></span><br/> | <span data-ttu-id="0db02-136">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0db02-136">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0db02-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0db02-137">Minimum supported server</span></span><br/> | <span data-ttu-id="0db02-138">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0db02-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0db02-139">Header</span><span class="sxs-lookup"><span data-stu-id="0db02-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="0db02-140"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="0db02-140"><dt>Commctrl.h</dt></span></span> </dl> |



 


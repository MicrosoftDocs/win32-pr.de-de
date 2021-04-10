---
title: LVM_SETGROUPINFO Meldung (kommstrg. h)
description: Legt Gruppeninformationen fest.
ms.assetid: f79bd235-e2de-4055-be3e-76eb2744e1ee
keywords:
- Windows-Steuerelemente für LVM_SETGROUPINFO Meldung
topic_type:
- apiref
api_name:
- LVM_SETGROUPINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 688c5b56a57a579e5955fa62a9b44d88258b7afb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040098"
---
# <a name="lvm_setgroupinfo-message"></a><span data-ttu-id="253c0-104">LVM- \_ setgroupinfo-Meldung</span><span class="sxs-lookup"><span data-stu-id="253c0-104">LVM\_SETGROUPINFO message</span></span>

<span data-ttu-id="253c0-105">Legt Gruppeninformationen fest.</span><span class="sxs-lookup"><span data-stu-id="253c0-105">Sets group information.</span></span> <span data-ttu-id="253c0-106">Senden Sie diese Nachricht explizit oder mithilfe des [**ListView \_ setgroupinfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setgroupinfo) -Makros.</span><span class="sxs-lookup"><span data-stu-id="253c0-106">Send this message explicitly or by using the [**ListView\_SetGroupInfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setgroupinfo) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="253c0-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="253c0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="253c0-108">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="253c0-108">*wParam* \[in\]</span></span>
</dt> <dd><span data-ttu-id="253c0-109">ID, die die Gruppe angibt, deren Informationen festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="253c0-109">ID that specifies the group whose information is to be set.</span></span></dd> <dt>

<span data-ttu-id="253c0-110">*LPARAM* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="253c0-110">*lParam* \[in, out\]</span></span>
</dt> <dd><span data-ttu-id="253c0-111">Ein Zeiger auf eine [**orgroup**](windows/win32/api/commctrl/ns-commctrl-lvgroup) -Struktur, die die festzulegenden Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="253c0-111">Pointer to a [**LVGROUP**](windows/win32/api/commctrl/ns-commctrl-lvgroup) structure that contains the information to set.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="253c0-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="253c0-112">Return value</span></span>

<span data-ttu-id="253c0-113">Gibt die ID der Gruppe zurück, wenn erfolgreich, andernfalls-1.</span><span class="sxs-lookup"><span data-stu-id="253c0-113">Returns the ID of the group if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="253c0-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="253c0-114">Remarks</span></span>

<span data-ttu-id="253c0-115">Fügen Sie zum Ändern der Gruppen-ID einer vorhandenen Gruppe <b>LVGF_GROUPID</b> zu " <b>LVGROUP. Mask</b> " hinzu, und legen Sie " <b>LVGROUP. igroupid</b> " auf die neue ID fest.</span><span class="sxs-lookup"><span data-stu-id="253c0-115">To change a group ID of an existing group add <b>LVGF_GROUPID</b> to <b>LVGROUP.mask</b> and set <b>LVGROUP.iGroupId</b> to the new ID.</span></span> <span data-ttu-id="253c0-116">Der-Rückruf schlägt fehl, wenn " <b>LVGROUP. igroupid</b> " die ID einer vorhandenen Gruppe enthält.</span><span class="sxs-lookup"><span data-stu-id="253c0-116">The call will fail if <b>LVGROUP.iGroupId</b> contains ID of an existing group.</span></span>

<span data-ttu-id="253c0-117">Um andere Eigenschaften einer vorhandenen Gruppe zu aktualisieren (z. b. das Aktualisieren einer Ausrichtung des Kopf-oder Fußzeilen Texts für die Gruppe, die <b>ualign</b>), darf " <b>LVGROUP. Mask</b> " keine <b>LVGF_GROUPID</b>enthalten. andernfalls schlägt das Update fehl.</span><span class="sxs-lookup"><span data-stu-id="253c0-117">To update other properties of an existing group (e.g. update an alignment of the header or footer text for the group, <b>uAlign</b>) <b>LVGROUP.mask</b> must not contain <b>LVGF_GROUPID</b>, else the update will fail.</span></span>

> [!Note]  
> <span data-ttu-id="253c0-118">Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="253c0-118">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="253c0-119">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="253c0-119">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="253c0-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="253c0-120">Requirements</span></span>



| <span data-ttu-id="253c0-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="253c0-121">Requirement</span></span> | <span data-ttu-id="253c0-122">Wert</span><span class="sxs-lookup"><span data-stu-id="253c0-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="253c0-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="253c0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="253c0-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="253c0-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="253c0-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="253c0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="253c0-126">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="253c0-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="253c0-127">Header</span><span class="sxs-lookup"><span data-stu-id="253c0-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="253c0-128"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="253c0-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






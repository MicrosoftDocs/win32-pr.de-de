---
title: LVM_GETGROUPINFO Meldung (kommstrg. h)
description: Ruft Gruppeninformationen ab.
ms.assetid: 72d84e0b-121e-473b-a34d-874234c598b6
keywords:
- Windows-Steuerelemente für LVM_GETGROUPINFO Meldung
topic_type:
- apiref
api_name:
- LVM_GETGROUPINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b55d5b1d781e7749df97bd0c9f7782f56545dbee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040441"
---
# <a name="lvm_getgroupinfo-message"></a><span data-ttu-id="e9f95-104">LVM \_ getgroupinfo-Meldung</span><span class="sxs-lookup"><span data-stu-id="e9f95-104">LVM\_GETGROUPINFO message</span></span>

<span data-ttu-id="e9f95-105">Ruft Gruppeninformationen ab.</span><span class="sxs-lookup"><span data-stu-id="e9f95-105">Gets group information.</span></span>

## <a name="parameters"></a><span data-ttu-id="e9f95-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9f95-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9f95-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e9f95-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e9f95-108">Eine ID, die die Gruppe angibt, deren Informationen abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e9f95-108">An ID that specifies the group whose information is retrieved.</span></span></dd> <dt>

<span data-ttu-id="e9f95-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e9f95-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="e9f95-110">Ein Zeiger auf eine <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroup">**orgroup**</a> -Struktur, die die abgerufenen Informationen empfängt.</span><span class="sxs-lookup"><span data-stu-id="e9f95-110">A pointer an <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroup">**LVGROUP**</a> structure that receives the retrieved information.</span></span> <span data-ttu-id="e9f95-111">Legen Sie den **CBSIZE** -Member dieser Struktur auf sizeof (LVGROUP) fest.</span><span class="sxs-lookup"><span data-stu-id="e9f95-111">Set the **cbSize** member of this structure to sizeof(LVGROUP).</span></span> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9f95-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e9f95-112">Return value</span></span>

<span data-ttu-id="e9f95-113">Gibt die ID der Gruppe zurück, wenn erfolgreich, andernfalls-1.</span><span class="sxs-lookup"><span data-stu-id="e9f95-113">Returns the ID of the group if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9f95-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e9f95-114">Remarks</span></span>

<span data-ttu-id="e9f95-115">Bevor Sie versuchen, die Kopfzeile für eine Gruppe abzurufen, stellen Sie zunächst sicher, dass die Gruppe nicht über den lbgs- \_ noheader-Stil verfügt.</span><span class="sxs-lookup"><span data-stu-id="e9f95-115">Before attempting to retrieve the header for a group, first ensure that the group does not have the LBGS\_NOHEADER style.</span></span>

> [!Note]  
> <span data-ttu-id="e9f95-116">Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="e9f95-116">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="e9f95-117">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e9f95-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e9f95-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e9f95-118">Requirements</span></span>



| <span data-ttu-id="e9f95-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e9f95-119">Requirement</span></span> | <span data-ttu-id="e9f95-120">Wert</span><span class="sxs-lookup"><span data-stu-id="e9f95-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e9f95-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e9f95-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e9f95-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e9f95-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e9f95-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e9f95-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e9f95-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e9f95-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e9f95-125">Header</span><span class="sxs-lookup"><span data-stu-id="e9f95-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9f95-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9f95-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






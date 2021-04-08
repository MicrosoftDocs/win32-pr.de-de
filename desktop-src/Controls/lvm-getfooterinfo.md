---
title: LVM_GETFOOTERINFO Meldung (kommstrg. h)
description: Ruft Informationen über die Fußzeile eines Listenansicht-Steuer Elements ab. Senden Sie diese Nachricht explizit oder mithilfe des ListView \_ getfooterinfo-Makros.
ms.assetid: 5734e151-50c0-46df-8f2c-220c4910a590
keywords:
- Windows-Steuerelemente für LVM_GETFOOTERINFO Meldung
topic_type:
- apiref
api_name:
- LVM_GETFOOTERINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 718e6c165985981190b5a1d4c52e851d1a2d504d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949425"
---
# <a name="lvm_getfooterinfo-message"></a><span data-ttu-id="768d4-105">LVM- \_ getfooterinfo-Meldung</span><span class="sxs-lookup"><span data-stu-id="768d4-105">LVM\_GETFOOTERINFO message</span></span>

<span data-ttu-id="768d4-106">Ruft Informationen über die Fußzeile eines Listenansicht-Steuer Elements ab.</span><span class="sxs-lookup"><span data-stu-id="768d4-106">Gets information about the footer of a list-view control.</span></span> <span data-ttu-id="768d4-107">Senden Sie diese Nachricht explizit oder mithilfe des [**ListView \_ getfooterinfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooterinfo) -Makros.</span><span class="sxs-lookup"><span data-stu-id="768d4-107">Send this message explicitly or by using the [**ListView\_GetFooterInfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooterinfo) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="768d4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="768d4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="768d4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="768d4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="768d4-110">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="768d4-110">Not used.</span></span> <span data-ttu-id="768d4-111">Muss den Wert 0 (null) haben.</span><span class="sxs-lookup"><span data-stu-id="768d4-111">Must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="768d4-112">*LPARAM* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="768d4-112">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="768d4-113">Ein Zeiger auf eine " [**lvfooterinfo**](/windows/win32/api/commctrl/ns-commctrl-lvfooterinfo) "-Struktur, die Informationen abhängig vom Wert des **Masken** Elements empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="768d4-113">A pointer to a [**LVFOOTERINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfooterinfo) structure to receive information depending on the value of the **mask** member.</span></span> <span data-ttu-id="768d4-114">Der Aufrufprozess ist dafür verantwortlich, diese Struktur zuzuordnen und das **Masken** Element festzulegen.</span><span class="sxs-lookup"><span data-stu-id="768d4-114">The calling process is responsible for allocating this structure and setting the **mask** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="768d4-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="768d4-115">Return value</span></span>

<span data-ttu-id="768d4-116">Gibt **true** zurück.</span><span class="sxs-lookup"><span data-stu-id="768d4-116">Returns **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="768d4-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="768d4-117">Requirements</span></span>



| <span data-ttu-id="768d4-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="768d4-118">Requirement</span></span> | <span data-ttu-id="768d4-119">Wert</span><span class="sxs-lookup"><span data-stu-id="768d4-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="768d4-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="768d4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="768d4-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="768d4-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="768d4-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="768d4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="768d4-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="768d4-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="768d4-124">Header</span><span class="sxs-lookup"><span data-stu-id="768d4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="768d4-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="768d4-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






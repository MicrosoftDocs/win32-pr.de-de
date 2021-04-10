---
title: LVM_SETITEMINDEXSTATE Meldung (kommstrg. h)
description: Legt den Zustand eines Listen Ansichts Elements fest. Senden Sie diese Nachricht explizit oder mithilfe des ListView-Makros "" \_ .
ms.assetid: 9fea6420-320a-4d2a-84b5-7923fbb14655
keywords:
- Windows-Steuerelemente für LVM_SETITEMINDEXSTATE Meldung
topic_type:
- apiref
api_name:
- LVM_SETITEMINDEXSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01ce8f6847c733127053e2162dd785d52fb77cfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040367"
---
# <a name="lvm_setitemindexstate-message"></a><span data-ttu-id="b2231-105">LVM- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="b2231-105">LVM\_SETITEMINDEXSTATE message</span></span>

<span data-ttu-id="b2231-106">Legt den Zustand eines Listen Ansichts Elements fest.</span><span class="sxs-lookup"><span data-stu-id="b2231-106">Sets the state of a list-view item.</span></span> <span data-ttu-id="b2231-107">Senden Sie diese Nachricht explizit oder mithilfe des [**ListView \_**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemindexstate) -Makros "".</span><span class="sxs-lookup"><span data-stu-id="b2231-107">Send this message explicitly or by using the [**ListView\_SetItemIndexState**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemindexstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b2231-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2231-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2231-109">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b2231-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2231-110">Ein Zeiger auf eine [**lvitemindex**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) -Struktur für das Element.</span><span class="sxs-lookup"><span data-stu-id="b2231-110">A pointer to an [**LVITEMINDEX**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) structure for the item.</span></span> <span data-ttu-id="b2231-111">Der Aufrufprozess ist dafür verantwortlich, diese Struktur zuzuordnen und die Elemente festzulegen.</span><span class="sxs-lookup"><span data-stu-id="b2231-111">The calling process is responsible for allocating this structure and setting the members.</span></span>

</dd> <dt>

<span data-ttu-id="b2231-112">*LPARAM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b2231-112">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2231-113">Ein Zeiger auf eine [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="b2231-113">A pointer to an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure.</span></span> <span data-ttu-id="b2231-114">Der Aufrufprozess ist für die Zuordnung von Arbeitsspeicher für die Struktur verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="b2231-114">The calling process is responsible for allocating memory for the structure.</span></span> <span data-ttu-id="b2231-115">Legen Sie **das** statusmember auf eine oder mehrere (als bitweise Kombination) der [Listen Ansichts elementstatusflags](list-view-item-states.md) fest.</span><span class="sxs-lookup"><span data-stu-id="b2231-115">Set the **state** member to one or more (as a bitwise combination) of the [List-View Item States](list-view-item-states.md) flags.</span></span> <span data-ttu-id="b2231-116">Legen Sie den **statemask** -Member der Struktur so fest, dass er die gültigen Bits des **Zustands** Members angibt.</span><span class="sxs-lookup"><span data-stu-id="b2231-116">Set the **stateMask** member of the structure to indicate the valid bits of the **state** member.</span></span> <span data-ttu-id="b2231-117">Weitere Informationen finden Sie unter dem **Status Ask** -Member der **lvitem** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="b2231-117">For more information, see the **stateMask** member of the **LVITEM** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2231-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b2231-118">Return value</span></span>

<span data-ttu-id="b2231-119">Gibt einen der folgenden Werte vom Typ **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="b2231-119">Returns one of the following values of type **HRESULT**.</span></span>



| <span data-ttu-id="b2231-120">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="b2231-120">Return code</span></span>                                                                                  | <span data-ttu-id="b2231-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b2231-121">Description</span></span>                                                       |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="b2231-122"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="b2231-122"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="b2231-123">Der Zustand konnte nicht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="b2231-123">The state could not be set.</span></span><br/>                            |
| <dl> <span data-ttu-id="b2231-124"><dt>**E \_ unerwartet**</dt></span><span class="sxs-lookup"><span data-stu-id="b2231-124"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="b2231-125">Das Listenansicht-Steuerelement war für den Vorgang nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="b2231-125">The list-view control was not ready for the operation.</span></span><br/> |
| <dl> <span data-ttu-id="b2231-126"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b2231-126"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="b2231-127">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="b2231-127">The operation was successful.</span></span><br/>                          |



 

## <a name="requirements"></a><span data-ttu-id="b2231-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b2231-128">Requirements</span></span>



| <span data-ttu-id="b2231-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b2231-129">Requirement</span></span> | <span data-ttu-id="b2231-130">Wert</span><span class="sxs-lookup"><span data-stu-id="b2231-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b2231-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b2231-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b2231-132">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b2231-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b2231-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b2231-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b2231-134">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b2231-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b2231-135">Header</span><span class="sxs-lookup"><span data-stu-id="b2231-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2231-136"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2231-136"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






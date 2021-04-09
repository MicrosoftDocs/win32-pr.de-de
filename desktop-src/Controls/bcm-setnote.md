---
title: BCM_SETNOTE Meldung (kommstrg. h)
description: Legt den Text des Hinweises fest, der einer Befehls Link Schaltfläche zugeordnet ist. Sie können diese Nachricht explizit senden oder das Schaltflächen- \_ setnote-Makro verwenden.
ms.assetid: c167072a-8207-4744-ac66-247141d726ab
keywords:
- Windows-Steuerelemente für BCM_SETNOTE Meldung
topic_type:
- apiref
api_name:
- BCM_SETNOTE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f544a7fb9dd89346cc2aa9725d36122746a8f608
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956456"
---
# <a name="bcm_setnote-message"></a><span data-ttu-id="0af79-105">BCM- \_ setnote-Meldung</span><span class="sxs-lookup"><span data-stu-id="0af79-105">BCM\_SETNOTE message</span></span>

<span data-ttu-id="0af79-106">Legt den Text des Hinweises fest, der einer Befehls Link Schaltfläche zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0af79-106">Sets the text of the note associated with a command link button.</span></span> <span data-ttu-id="0af79-107">Sie können diese Nachricht explizit senden oder das Schaltflächen- [**\_ setnote**](/windows/desktop/api/Commctrl/nf-commctrl-button_setnote) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="0af79-107">You can send this message explicitly or use the [**Button\_SetNote**](/windows/desktop/api/Commctrl/nf-commctrl-button_setnote) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0af79-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0af79-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0af79-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0af79-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0af79-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="0af79-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="0af79-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0af79-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0af79-112">Ein Zeiger auf eine NULL terminierte **WCHAR** -Zeichenfolge, die den Hinweis enthält.</span><span class="sxs-lookup"><span data-stu-id="0af79-112">A pointer to a null-terminated **WCHAR** string that contains the note.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0af79-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0af79-113">Return value</span></span>

<span data-ttu-id="0af79-114">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="0af79-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0af79-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0af79-115">Remarks</span></span>

<span data-ttu-id="0af79-116">Ab ComCtl32 dll, Version 6,01, können Befehls Link Schaltflächen einen Hinweis enthalten.</span><span class="sxs-lookup"><span data-stu-id="0af79-116">Beginning with comctl32 DLL version 6.01, command link buttons may have a note.</span></span>

<span data-ttu-id="0af79-117">Die **BCM- \_ setnote** -Nachricht funktioniert nur mit den Schaltflächen Formaten " [**SB \_ CommandLink**](button-styles.md) " und " [**b" \_ defcommandlink**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="0af79-117">The **BCM\_SETNOTE** message works only with the [**BS\_COMMANDLINK**](button-styles.md) and [**BS\_DEFCOMMANDLINK**](button-styles.md) button styles.</span></span>

## <a name="requirements"></a><span data-ttu-id="0af79-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0af79-118">Requirements</span></span>



| <span data-ttu-id="0af79-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0af79-119">Requirement</span></span> | <span data-ttu-id="0af79-120">Wert</span><span class="sxs-lookup"><span data-stu-id="0af79-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0af79-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0af79-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0af79-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0af79-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0af79-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0af79-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0af79-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0af79-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0af79-125">Header</span><span class="sxs-lookup"><span data-stu-id="0af79-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0af79-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="0af79-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0af79-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0af79-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="0af79-128">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="0af79-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0af79-129">Schaltflächenstile</span><span class="sxs-lookup"><span data-stu-id="0af79-129">Button Styles</span></span>](button-styles.md)
</dt> <dt>

<span data-ttu-id="0af79-130">**Licher**</span><span class="sxs-lookup"><span data-stu-id="0af79-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0af79-131">Schaltflächentypen</span><span class="sxs-lookup"><span data-stu-id="0af79-131">Button Types</span></span>](button-types-and-styles.md)
</dt> </dl>

 

 






---
title: BCM_GETNOTELENGTH Meldung (kommstrg. h)
description: Ruft die Länge des Notiz Texts ab, der in der Beschreibung für eine Befehls Link Schaltfläche angezeigt werden kann. Senden Sie diese Nachricht explizit oder mithilfe der Schaltfläche \_ getnotelength-Makro.
ms.assetid: 62385485-b553-47e9-9f15-696cc4694752
keywords:
- Windows-Steuerelemente für BCM_GETNOTELENGTH Meldung
topic_type:
- apiref
api_name:
- BCM_GETNOTELENGTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b33c5245778481033bd97326c3d66a40bf03210
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040511"
---
# <a name="bcm_getnotelength-message"></a><span data-ttu-id="18adc-105">BCM \_ getnotelength-Meldung</span><span class="sxs-lookup"><span data-stu-id="18adc-105">BCM\_GETNOTELENGTH message</span></span>

<span data-ttu-id="18adc-106">Ruft die Länge des Notiz Texts ab, der in der Beschreibung für eine Befehls Link Schaltfläche angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="18adc-106">Gets the length of the note text that may be displayed in the description for a command link button.</span></span> <span data-ttu-id="18adc-107">Senden Sie diese Nachricht explizit oder mithilfe der [**Schaltfläche \_ getnotelength**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnotelength) -Makro.</span><span class="sxs-lookup"><span data-stu-id="18adc-107">Send this message explicitly or by using the [**Button\_GetNoteLength**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnotelength) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="18adc-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="18adc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18adc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="18adc-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="18adc-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="18adc-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="18adc-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="18adc-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="18adc-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="18adc-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18adc-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="18adc-113">Return value</span></span>

<span data-ttu-id="18adc-114">Gibt die Länge des Notiz Texts in **WCHARs** zurück, ohne abschließende **null**-Werte, oder 0 (null), wenn kein Hinweis Text vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="18adc-114">Returns the length of the note text in **WCHARs**, not including any terminating **NULL**, or zero if there is no note text.</span></span>

## <a name="remarks"></a><span data-ttu-id="18adc-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="18adc-115">Remarks</span></span>

<span data-ttu-id="18adc-116">Ab ComCtl32 dll, Version 6,01, können Befehls Link Schaltflächen einen Hinweis enthalten.</span><span class="sxs-lookup"><span data-stu-id="18adc-116">Beginning with comctl32 DLL version 6.01, command link buttons may have a note.</span></span> <span data-ttu-id="18adc-117">Weitere Informationen zu DLL-Versionen finden Sie unter [allgemeine Steuerelement Versionen](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="18adc-117">For information on DLL versions, see [Common Control Versions](common-control-versions.md).</span></span>

<span data-ttu-id="18adc-118">Die **BCM \_ getnotelength** -Nachricht funktioniert nur mit den Schaltflächen Stilen " [**SB \_ CommandLink**](button-styles.md) " und " [**SB \_ defcommandlink**](button-styles.md) ".</span><span class="sxs-lookup"><span data-stu-id="18adc-118">The **BCM\_GETNOTELENGTH** message works only with the [**BS\_COMMANDLINK**](button-styles.md) and [**BS\_DEFCOMMANDLINK**](button-styles.md) button styles.</span></span>

## <a name="requirements"></a><span data-ttu-id="18adc-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="18adc-119">Requirements</span></span>



| <span data-ttu-id="18adc-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="18adc-120">Requirement</span></span> | <span data-ttu-id="18adc-121">Wert</span><span class="sxs-lookup"><span data-stu-id="18adc-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="18adc-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="18adc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="18adc-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="18adc-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="18adc-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="18adc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="18adc-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="18adc-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="18adc-126">Header</span><span class="sxs-lookup"><span data-stu-id="18adc-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="18adc-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="18adc-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18adc-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18adc-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="18adc-129">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="18adc-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="18adc-130">Schaltflächenstile</span><span class="sxs-lookup"><span data-stu-id="18adc-130">Button Styles</span></span>](button-styles.md)
</dt> <dt>

<span data-ttu-id="18adc-131">**Licher**</span><span class="sxs-lookup"><span data-stu-id="18adc-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="18adc-132">Schaltflächentypen</span><span class="sxs-lookup"><span data-stu-id="18adc-132">Button Types</span></span>](button-types-and-styles.md)
</dt> </dl>

 

 






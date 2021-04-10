---
title: EM_SETHANDLE Meldung (Winuser. h)
description: Legt das Handle des Arbeitsspeichers fest, der von einem mehrzeiligen Bearbeitungs Steuerelement verwendet wird.
ms.assetid: 0eae9365-62af-4040-8a51-273997a00b81
keywords:
- Windows-Steuerelemente für EM_SETHANDLE Meldung
topic_type:
- apiref
api_name:
- EM_SETHANDLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac8f918d056db1000c6018f55d89095a73a15109
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105573"
---
# <a name="em_sethandle-message"></a><span data-ttu-id="86370-104">EM- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="86370-104">EM\_SETHANDLE message</span></span>

<span data-ttu-id="86370-105">Legt das Handle des Arbeitsspeichers fest, der von einem mehrzeiligen Bearbeitungs Steuerelement verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="86370-105">Sets the handle of the memory that will be used by a multiline edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="86370-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="86370-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86370-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="86370-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="86370-108">Ein Handle für den Arbeitsspeicher Puffer, den das Bearbeitungs Steuerelement verwendet, um den aktuell angezeigten Text zu speichern, anstatt seinen eigenen Arbeitsspeicher zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="86370-108">A handle to the memory buffer the edit control uses to store the currently displayed text instead of allocating its own memory.</span></span> <span data-ttu-id="86370-109">Falls erforderlich, ordnet das-Steuerelement diesen Arbeitsspeicher neu zu.</span><span class="sxs-lookup"><span data-stu-id="86370-109">If necessary, the control reallocates this memory.</span></span>

</dd> <dt>

<span data-ttu-id="86370-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="86370-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="86370-111">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="86370-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86370-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="86370-112">Return value</span></span>

<span data-ttu-id="86370-113">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="86370-113">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="86370-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="86370-114">Remarks</span></span>

<span data-ttu-id="86370-115">Bevor eine Anwendung ein neues Speicher handle festlegt, sollte Sie eine [**EM \_ GetHandle**](em-gethandle.md) -Nachricht senden, um das Handle des aktuellen Speicherpuffers abzurufen, und diesen Arbeitsspeicher freigeben.</span><span class="sxs-lookup"><span data-stu-id="86370-115">Before an application sets a new memory handle, it should send an [**EM\_GETHANDLE**](em-gethandle.md) message to retrieve the handle of the current memory buffer and should free that memory.</span></span>

<span data-ttu-id="86370-116">Ein Bearbeitungs Steuerelement ordnet den angegebenen Puffer automatisch neu zu, wenn ein zusätzlicher Platz für Text benötigt wird, oder er entfernt ausreichend Text, sodass zusätzlicher Speicherplatz nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="86370-116">An edit control automatically reallocates the given buffer whenever it needs additional space for text, or it removes enough text so that additional space is no longer needed.</span></span>

<span data-ttu-id="86370-117">Beim Senden einer **EM- \_ SetHandle** -Nachricht wird der Rückgängig-Puffer gelöscht ([**EM \_ CanUndo**](em-canundo.md) gibt NULL zurück), und das Flag für die interne Änderung ([**EM \_ getmodify**](em-getmodify.md) gibt NULL zurück).</span><span class="sxs-lookup"><span data-stu-id="86370-117">Sending an **EM\_SETHANDLE** message clears the undo buffer ([**EM\_CANUNDO**](em-canundo.md) returns zero) and the internal modification flag ([**EM\_GETMODIFY**](em-getmodify.md) returns zero).</span></span> <span data-ttu-id="86370-118">Das Bearbeitungs Steuerelement-Fenster wird neu gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="86370-118">The edit control window is redrawn.</span></span>

<span data-ttu-id="86370-119">Umfassende **Bearbeitung:** Die **EM \_** -Abmeldung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="86370-119">**Rich Edit:** The **EM\_SETHANDLE** message is not supported.</span></span> <span data-ttu-id="86370-120">Rich Edit-Steuerelemente speichern Text nicht als einfaches Zeichen Array.</span><span class="sxs-lookup"><span data-stu-id="86370-120">Rich edit controls do not store text as a simple array of characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="86370-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="86370-121">Requirements</span></span>



| <span data-ttu-id="86370-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="86370-122">Requirement</span></span> | <span data-ttu-id="86370-123">Wert</span><span class="sxs-lookup"><span data-stu-id="86370-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86370-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="86370-124">Minimum supported client</span></span><br/> | <span data-ttu-id="86370-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="86370-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="86370-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="86370-126">Minimum supported server</span></span><br/> | <span data-ttu-id="86370-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="86370-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="86370-128">Header</span><span class="sxs-lookup"><span data-stu-id="86370-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="86370-129"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="86370-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86370-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="86370-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="86370-131">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="86370-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="86370-132">**EM \_ CanUndo**</span><span class="sxs-lookup"><span data-stu-id="86370-132">**EM\_CANUNDO**</span></span>](em-canundo.md)
</dt> <dt>

[<span data-ttu-id="86370-133">**EM \_ GetHandle**</span><span class="sxs-lookup"><span data-stu-id="86370-133">**EM\_GETHANDLE**</span></span>](em-gethandle.md)
</dt> <dt>

[<span data-ttu-id="86370-134">**EM \_ getmodify**</span><span class="sxs-lookup"><span data-stu-id="86370-134">**EM\_GETMODIFY**</span></span>](em-getmodify.md)
</dt> </dl>

 

 






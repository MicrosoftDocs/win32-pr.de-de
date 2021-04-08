---
title: TDM_NAVIGATE_PAGE Meldung (kommstrg. h)
description: Erstellt ein Aufgaben Dialogfeld mit neuen Inhalten neu und simuliert die Funktionalität eines Assistenten für mehrere Seiten.
ms.assetid: e0eefd08-e279-47db-97e9-7ca86b41e22f
keywords:
- Windows-Steuerelemente für TDM_NAVIGATE_PAGE Meldung
topic_type:
- apiref
api_name:
- TDM_NAVIGATE_PAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56fc86e0e4fe457a43e035ed5d568e91303c7fcd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957097"
---
# <a name="tdm_navigate_page-message"></a><span data-ttu-id="9657a-104">TDM- \_ Navigations \_ Seite (Meldung)</span><span class="sxs-lookup"><span data-stu-id="9657a-104">TDM\_NAVIGATE\_PAGE message</span></span>

<span data-ttu-id="9657a-105">Erstellt ein Aufgaben Dialogfeld mit neuen Inhalten neu und simuliert die Funktionalität eines Assistenten für mehrere Seiten.</span><span class="sxs-lookup"><span data-stu-id="9657a-105">Recreates a task dialog with new contents, simulating the functionality of a multi-page wizard.</span></span>

## <a name="parameters"></a><span data-ttu-id="9657a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9657a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9657a-107">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9657a-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9657a-108">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="9657a-108">Not used.</span></span> <span data-ttu-id="9657a-109">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="9657a-109">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="9657a-110">*LPARAM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9657a-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9657a-111">Ein Zeiger auf eine [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) -Struktur, die das zu Erstell gende Aufgaben Dialogfeld beschreibt.</span><span class="sxs-lookup"><span data-stu-id="9657a-111">A pointer to a [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure that describes the task dialog to create.</span></span> <span data-ttu-id="9657a-112">Die aufrufenden Anwendung muss diese Struktur zuordnen und deren Member festlegen.</span><span class="sxs-lookup"><span data-stu-id="9657a-112">The calling application must allocate this structure and set its members.</span></span> <span data-ttu-id="9657a-113">Die Werte der Elemente variieren abhängig von der Art der Seite, zu der der Benutzer navigiert.</span><span class="sxs-lookup"><span data-stu-id="9657a-113">The values of the members vary depending on the kind of page the user navigates to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9657a-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9657a-114">Return value</span></span>

<span data-ttu-id="9657a-115">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="9657a-115">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="9657a-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9657a-116">Remarks</span></span>

<span data-ttu-id="9657a-117">Verwenden Sie die [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) -Funktion, um ein Aufgaben Dialogfeld für den Assistenten zu starten.</span><span class="sxs-lookup"><span data-stu-id="9657a-117">To launch a wizard task dialog, use the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) function.</span></span> <span data-ttu-id="9657a-118">Wenn der Benutzer mithilfe des Assistenten navigiert, senden Sie diese Meldung an das Aufgaben Dialogfeld, um die nächste Seite anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9657a-118">As the user navigates using the wizard, send this message to the task dialog to display the next page.</span></span> <span data-ttu-id="9657a-119">Ein neues Aufgaben Dialogfeld (wie eine neue Seite) wird mit den in der Struktur angegebenen Elementen erstellt, auf die von *LPARAM* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="9657a-119">A new task dialog (looks like a new page) is created with the elements specified in the structure pointed to by *lParam*.</span></span> <span data-ttu-id="9657a-120">Bei der Erstellung wird der gesamte Inhalt des dialograhmens zerstört und rekonstruiert.</span><span class="sxs-lookup"><span data-stu-id="9657a-120">At creation, the entire contents of the dialog frame are destroyed and reconstructed.</span></span> <span data-ttu-id="9657a-121">Dadurch gehen alle Zustandsinformationen, die von Steuerelementen (z. b. Statusanzeige, expando-Schaltfläche oder Überprüfungs Kästchen) im Dialogfeld gespeichert werden, verloren.</span><span class="sxs-lookup"><span data-stu-id="9657a-121">As a result, any state information held by controls (for example, a progress bar, expando button, or verification checkbox) in the dialog is lost.</span></span>

<span data-ttu-id="9657a-122">Das Layout des Aufgaben Dialogfelds schlägt möglicherweise fehl, und dies wird möglicherweise nicht im Rückgabewert berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="9657a-122">The layout of the task dialog may fail and this may not be reflected in the return value.</span></span> <span data-ttu-id="9657a-123">Der Rückgabewert S \_ OK gibt nur an, dass das Aufgaben Dialogfeld die Nachricht empfangen und versucht hat, Sie zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="9657a-123">A return value of S\_OK reflects only that the task dialog received the message and attempted to process it.</span></span> <span data-ttu-id="9657a-124">Wenn das Layout des Aufgaben Dialogfelds fehlschlägt (das Aufgaben Dialogfeld kann nicht angezeigt werden), wird das Dialogfeld geschlossen, und ein **HRESULT** -Code wird bei der registrierten Rückruffunktion zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9657a-124">If the layout of the task dialog fails (the task dialog cannot be displayed), the dialog will close and an **HRESULT** code is returned at the registered callback function.</span></span> <span data-ttu-id="9657a-125">Weitere Informationen zur Syntax der Rückruffunktion finden Sie unter [*taskdialogcallbackproc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback).</span><span class="sxs-lookup"><span data-stu-id="9657a-125">For more information on the callback function syntax, see [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback).</span></span>

## <a name="requirements"></a><span data-ttu-id="9657a-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9657a-126">Requirements</span></span>



| <span data-ttu-id="9657a-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9657a-127">Requirement</span></span> | <span data-ttu-id="9657a-128">Wert</span><span class="sxs-lookup"><span data-stu-id="9657a-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9657a-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9657a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9657a-130">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9657a-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9657a-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9657a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9657a-132">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9657a-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9657a-133">Header</span><span class="sxs-lookup"><span data-stu-id="9657a-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="9657a-134"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="9657a-134"><dt>Commctrl.h</dt></span></span> </dl> |



 


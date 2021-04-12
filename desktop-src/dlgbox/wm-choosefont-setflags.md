---
title: WM_CHOOSEFONT_SETFLAGS Meldung (kommdlg. h)
description: Eine Anwendung sendet die WM \_ choosefont- \_ setFlags-Nachricht an ein Schriftart Dialogfeld, um die Anzeigeoptionen für das Dialogfeld festzulegen.
ms.assetid: 945ebc07-440d-4466-8255-ad344bdc568a
keywords:
- Dialog Felder WM_CHOOSEFONT_SETFLAGS Meldung
topic_type:
- apiref
api_name:
- WM_CHOOSEFONT_SETFLAGS
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f7abf436311f8a3868b1471c2a10a7ee2e4a3b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104882"
---
# <a name="wm_choosefont_setflags-message"></a><span data-ttu-id="3709e-104">WM \_ choosefont \_ setFlags-Nachricht</span><span class="sxs-lookup"><span data-stu-id="3709e-104">WM\_CHOOSEFONT\_SETFLAGS message</span></span>

<span data-ttu-id="3709e-105">Eine Anwendung sendet die **WM \_ choosefont- \_ setFlags** -Nachricht an ein **Schriftart** Dialogfeld, um die Anzeigeoptionen für das Dialogfeld festzulegen.</span><span class="sxs-lookup"><span data-stu-id="3709e-105">An application sends the **WM\_CHOOSEFONT\_SETFLAGS** message to a **Font** dialog box to set the display options for the dialog box.</span></span>


```C++
#define WM_USER                        0x0400
#define WM_CHOOSEFONT_SETFLAGS        (WM_USER + 102)
```



## <a name="parameters"></a><span data-ttu-id="3709e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3709e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3709e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3709e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3709e-108">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="3709e-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3709e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3709e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3709e-110">Ein Zeiger auf eine [**Auswahl Schriftart**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) Struktur, die neue Einstellungen im **Flags** -Member enthält.</span><span class="sxs-lookup"><span data-stu-id="3709e-110">A pointer to a [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure that contains new settings in the **Flags** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3709e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3709e-111">Return value</span></span>

<span data-ttu-id="3709e-112">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="3709e-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3709e-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3709e-113">Remarks</span></span>

<span data-ttu-id="3709e-114">Die [**Auswahl Schriftart**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) erstellt ein Dialogfeld **Schriftart** und verwendet eine [**Auswahl Schriftart**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) , um die Anfangswerte für den **Flags** -Member anzugeben.</span><span class="sxs-lookup"><span data-stu-id="3709e-114">The [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) function creates a **Font** dialog box and uses a [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure to specify the initial values for the **Flags** member.</span></span> <span data-ttu-id="3709e-115">Verwenden Sie die " **WM \_ choosefont \_ setFlags** "-Meldung, um unterschiedliche Werte für den **Flags** -Member anzugeben, während das Dialogfeld **Schriftart** geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="3709e-115">Use the **WM\_CHOOSEFONT\_SETFLAGS** message to specify different values for the **Flags** member while the **Font** dialog box is open.</span></span>

<span data-ttu-id="3709e-116">Normalerweise sollten Sie die **WM \_ choosefont- \_ setFlags** -Nachricht von einer [**cfhuokproc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) -Hook-Prozedur senden.</span><span class="sxs-lookup"><span data-stu-id="3709e-116">Typically, you should send the **WM\_CHOOSEFONT\_SETFLAGS** message from a [**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) hook procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="3709e-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3709e-117">Requirements</span></span>



| <span data-ttu-id="3709e-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3709e-118">Requirement</span></span> | <span data-ttu-id="3709e-119">Wert</span><span class="sxs-lookup"><span data-stu-id="3709e-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3709e-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3709e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3709e-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3709e-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3709e-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3709e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3709e-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3709e-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3709e-124">Header</span><span class="sxs-lookup"><span data-stu-id="3709e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3709e-125"><dt>Kommdlg. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3709e-125"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3709e-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3709e-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="3709e-127">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="3709e-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3709e-128">**Cfhuokproc**</span><span class="sxs-lookup"><span data-stu-id="3709e-128">**CFHookProc**</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)
</dt> <dt>

[<span data-ttu-id="3709e-129">**Auswahl Schriftart**</span><span class="sxs-lookup"><span data-stu-id="3709e-129">**ChooseFont**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[<span data-ttu-id="3709e-130">**Auswahl Schriftart**</span><span class="sxs-lookup"><span data-stu-id="3709e-130">**CHOOSEFONT**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

<span data-ttu-id="3709e-131">**Licher**</span><span class="sxs-lookup"><span data-stu-id="3709e-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3709e-132">Allgemeine Dialog Feld Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3709e-132">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 


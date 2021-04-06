---
title: WM_CHOOSEFONT_SETLOGFONT Meldung (kommdlg. h)
description: Eine Anwendung sendet die Meldung "WM \_ choosefont \_ setlogfont" an ein Schriftart Dialogfeld, um die aktuellen Informationen zur logischen Schriftart festzulegen.
ms.assetid: ad169eca-a3ae-45bd-90df-821a93a7a764
keywords:
- Dialog Felder WM_CHOOSEFONT_SETLOGFONT Meldung
topic_type:
- apiref
api_name:
- WM_CHOOSEFONT_SETLOGFONT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6a588ebff7c8e56bb559a2cc9faa1d6290fbd8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742584"
---
# <a name="wm_choosefont_setlogfont-message"></a><span data-ttu-id="81370-104">WM \_ choosefont- \_ setlogfont-Meldung</span><span class="sxs-lookup"><span data-stu-id="81370-104">WM\_CHOOSEFONT\_SETLOGFONT message</span></span>

<span data-ttu-id="81370-105">Eine Anwendung sendet die Meldung " **WM \_ choosefont \_ setlogfont** " an ein **Schriftart** Dialogfeld, um die aktuellen Informationen zur logischen Schriftart festzulegen.</span><span class="sxs-lookup"><span data-stu-id="81370-105">An application sends the **WM\_CHOOSEFONT\_SETLOGFONT** message to a **Font** dialog box to set the current logical font information.</span></span>


```C++
#define WM_USER                        0x0400
#define WM_CHOOSEFONT_SETLOGFONT      (WM_USER + 101)
```



## <a name="parameters"></a><span data-ttu-id="81370-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="81370-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81370-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="81370-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="81370-108">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="81370-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="81370-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="81370-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="81370-110">Ein Zeiger auf eine [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur, die Informationen über die aktuelle logische Schriftart enthält.</span><span class="sxs-lookup"><span data-stu-id="81370-110">A pointer to a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure that contains information about the current logical font.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81370-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="81370-111">Return value</span></span>

<span data-ttu-id="81370-112">Diese Nachricht weist keinen Rückgabewert auf.</span><span class="sxs-lookup"><span data-stu-id="81370-112">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="81370-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="81370-113">Remarks</span></span>

<span data-ttu-id="81370-114">Wenn Sie zum Erstellen eines **Schriftart** Dialogfelds die [**choolfont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) -Funktion aufzurufen, können Sie den **lplogfont** -Member der [**chooonfont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) -Struktur verwenden, um eine [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur anzugeben, die Anfangswerte für das Dialogfeld enthält.</span><span class="sxs-lookup"><span data-stu-id="81370-114">When you call the [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) function to create a **Font** dialog box, you can use the **lpLogFont** member of the [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure to specify a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure containing initial values for the dialog box.</span></span> <span data-ttu-id="81370-115">Verwenden Sie die " **WM \_ choosefont \_ setlogfont** "-Meldung, um eine **LOGFONT** -Struktur mit unterschiedlichen Werten anzugeben, während das Dialogfeld **Schriftart** geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="81370-115">Use the **WM\_CHOOSEFONT\_SETLOGFONT** message to specify a **LOGFONT** structure with different values while the **Font** dialog box is open.</span></span>

<span data-ttu-id="81370-116">In der Regel würden Sie die **WM \_ choosefont- \_ setlogfont** -Nachricht von einer [**cfhuokproc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) -Hook-Prozedur senden.</span><span class="sxs-lookup"><span data-stu-id="81370-116">Typically, you would send the **WM\_CHOOSEFONT\_SETLOGFONT** message from a [**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) hook procedure.</span></span> <span data-ttu-id="81370-117">Die Hook-Prozedur kann auch die Nachrichten [**WM \_ choosefont \_ getlogfont**](wm-choosefont-getlogfont.md) und [**WM \_ choosefont \_ setFlags**](wm-choosefont-setflags.md) senden.</span><span class="sxs-lookup"><span data-stu-id="81370-117">The hook procedure can also send the [**WM\_CHOOSEFONT\_GETLOGFONT**](wm-choosefont-getlogfont.md) and [**WM\_CHOOSEFONT\_SETFLAGS**](wm-choosefont-setflags.md) messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="81370-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="81370-118">Requirements</span></span>



| <span data-ttu-id="81370-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="81370-119">Requirement</span></span> | <span data-ttu-id="81370-120">Wert</span><span class="sxs-lookup"><span data-stu-id="81370-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81370-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="81370-121">Minimum supported client</span></span><br/> | <span data-ttu-id="81370-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="81370-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="81370-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="81370-123">Minimum supported server</span></span><br/> | <span data-ttu-id="81370-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="81370-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="81370-125">Header</span><span class="sxs-lookup"><span data-stu-id="81370-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="81370-126"><dt>Kommdlg. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="81370-126"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81370-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="81370-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="81370-128">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="81370-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="81370-129">**Cfhuokproc**</span><span class="sxs-lookup"><span data-stu-id="81370-129">**CFHookProc**</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)
</dt> <dt>

[<span data-ttu-id="81370-130">**Auswahl Schriftart**</span><span class="sxs-lookup"><span data-stu-id="81370-130">**ChooseFont**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[<span data-ttu-id="81370-131">**Auswahl Schriftart**</span><span class="sxs-lookup"><span data-stu-id="81370-131">**CHOOSEFONT**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[<span data-ttu-id="81370-132">**WM- \_ Auswahl Schriftart \_ getlogfont**</span><span class="sxs-lookup"><span data-stu-id="81370-132">**WM\_CHOOSEFONT\_GETLOGFONT**</span></span>](wm-choosefont-getlogfont.md)
</dt> <dt>

[<span data-ttu-id="81370-133">**WM \_ choosefont- \_ setFlags**</span><span class="sxs-lookup"><span data-stu-id="81370-133">**WM\_CHOOSEFONT\_SETFLAGS**</span></span>](wm-choosefont-setflags.md)
</dt> <dt>

<span data-ttu-id="81370-134">**Licher**</span><span class="sxs-lookup"><span data-stu-id="81370-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="81370-135">Allgemeine Dialog Feld Bibliothek</span><span class="sxs-lookup"><span data-stu-id="81370-135">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> <dt>

<span data-ttu-id="81370-136">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="81370-136">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="81370-137">**"LogFont"**</span><span class="sxs-lookup"><span data-stu-id="81370-137">**LOGFONT**</span></span>](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> </dl>

 


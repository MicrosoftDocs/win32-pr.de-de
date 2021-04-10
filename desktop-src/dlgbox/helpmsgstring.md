---
title: Helpmsgstring-Nachricht (kommdlg. h)
description: Ein häufig verwendeter Dialogfeld sendet die registrierte helpmsgstring-Meldung an die Fenster Prozedur des Besitzer Fensters, wenn der Benutzer auf die Schaltfläche Hilfe klickt.
ms.assetid: 21c0fcf5-785b-4005-8133-e48347f991a8
keywords:
- Helpmsgstring-Meldungs Dialogfelder
topic_type:
- apiref
api_name:
- HELPMSGSTRING
- HELPMSGSTRINGA
- HELPMSGSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac3f7a883f50b06c8d142cb83bedf0bfa2920191
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106011"
---
# <a name="helpmsgstring-message"></a><span data-ttu-id="d63ad-104">Helpmsgstring-Meldung</span><span class="sxs-lookup"><span data-stu-id="d63ad-104">HELPMSGSTRING message</span></span>

<span data-ttu-id="d63ad-105">Ein häufig verwendeter Dialogfeld sendet die registrierte **helpmsgstring** -Meldung an die Fenster Prozedur des Besitzer Fensters, wenn der Benutzer auf die Schaltfläche **Hilfe** klickt.</span><span class="sxs-lookup"><span data-stu-id="d63ad-105">A common dialog box sends the **HELPMSGSTRING** registered message to the window procedure of its owner window when the user clicks the **Help** button.</span></span>


```C++
#define HELPMSGSTRING TEXT("commdlg_help")
```



## <a name="parameters"></a><span data-ttu-id="d63ad-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d63ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d63ad-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d63ad-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d63ad-108">Ein Handle für das allgemeine Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="d63ad-108">A handle to the common dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="d63ad-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d63ad-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d63ad-110">Ein Zeiger auf die Initialisierungs Struktur für das allgemeine Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="d63ad-110">A pointer to the initialization structure for the common dialog box.</span></span> <span data-ttu-id="d63ad-111">Bei [**dieser Struktur kann**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) es sich um eine " [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)"-, " [**choosefont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)"-, " [**FindReplace**](/windows/win32/api/commdlg/ns-commdlg-findreplacea)"-, " [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)"-, " [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) "-</span><span class="sxs-lookup"><span data-stu-id="d63ad-111">This structure can be a [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1), [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta), [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea), [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea), [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) or [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d63ad-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d63ad-112">Return value</span></span>

<span data-ttu-id="d63ad-113">Diese Nachricht weist keinen Rückgabewert auf.</span><span class="sxs-lookup"><span data-stu-id="d63ad-113">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d63ad-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d63ad-114">Remarks</span></span>

<span data-ttu-id="d63ad-115">Sie müssen die **helpmsgstring** -Konstante in einem Aufrufen der [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) -Funktion angeben, um den Bezeichner für die vom Dialogfeld gesendete Nachricht abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d63ad-115">You must specify the **HELPMSGSTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier for the message sent by the dialog box.</span></span>

<span data-ttu-id="d63ad-116">Wenn Sie das Dialogfeld erstellen, verwenden Sie den **hwndOwner** -Member der Initialisierungs Struktur, um das Fenster für den Empfang von **helpmsgstring** -Nachrichten zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="d63ad-116">When you create the dialog box, use the **hwndOwner** member of the initialization structure to identify the window to receive **HELPMSGSTRING** messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="d63ad-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d63ad-117">Requirements</span></span>



| <span data-ttu-id="d63ad-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d63ad-118">Requirement</span></span> | <span data-ttu-id="d63ad-119">Wert</span><span class="sxs-lookup"><span data-stu-id="d63ad-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d63ad-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d63ad-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d63ad-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d63ad-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d63ad-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d63ad-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d63ad-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d63ad-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d63ad-124">Header</span><span class="sxs-lookup"><span data-stu-id="d63ad-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d63ad-125"><dt>Kommdlg. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d63ad-125"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="d63ad-126">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="d63ad-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d63ad-127">**Helpmsgstringw** (Unicode) und **helpmsgstrauinga** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d63ad-127">**HELPMSGSTRINGW** (Unicode) and **HELPMSGSTRINGA** (ANSI)</span></span><br/>                                    |



## <a name="see-also"></a><span data-ttu-id="d63ad-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d63ad-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="d63ad-129">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="d63ad-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d63ad-130">**CDN- \_ Hilfe**</span><span class="sxs-lookup"><span data-stu-id="d63ad-130">**CDN\_HELP**</span></span>](cdn-help.md)
</dt> <dt>

[<span data-ttu-id="d63ad-131">**CHOOSECOLOR**</span><span class="sxs-lookup"><span data-stu-id="d63ad-131">**CHOOSECOLOR**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)
</dt> <dt>

[<span data-ttu-id="d63ad-132">**Auswahl Schriftart**</span><span class="sxs-lookup"><span data-stu-id="d63ad-132">**CHOOSEFONT**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[<span data-ttu-id="d63ad-133">**FindReplace**</span><span class="sxs-lookup"><span data-stu-id="d63ad-133">**FINDREPLACE**</span></span>](/windows/win32/api/commdlg/ns-commdlg-findreplacea)
</dt> <dt>

[<span data-ttu-id="d63ad-134">**OpenFileName**</span><span class="sxs-lookup"><span data-stu-id="d63ad-134">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[<span data-ttu-id="d63ad-135">**PRINTDLG**</span><span class="sxs-lookup"><span data-stu-id="d63ad-135">**PRINTDLG**</span></span>](/windows/win32/api/commdlg/ns-commdlg-printdlga)
</dt> <dt>

[<span data-ttu-id="d63ad-136">**Pagesetupdlg**</span><span class="sxs-lookup"><span data-stu-id="d63ad-136">**PAGESETUPDLG**</span></span>](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)
</dt> <dt>

[<span data-ttu-id="d63ad-137">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="d63ad-137">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="d63ad-138">**Licher**</span><span class="sxs-lookup"><span data-stu-id="d63ad-138">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d63ad-139">Allgemeine Dialog Feld Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d63ad-139">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 


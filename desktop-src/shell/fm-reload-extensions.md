---
description: Wird von einer Datei-Manager-Erweiterung (oder einer anderen Anwendung) gesendet, damit der Datei-Manager alle Erweiterungs-DLLs erneut lädt, die im \[ Abschnitt "Addons" \] der Winfile.ini Datei aufgeführt sind.
ms.assetid: 5103a986-5f45-4deb-aaae-c6e87cb60051
title: FM_RELOAD_EXTENSIONS Meldung (WF. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_RELOAD_EXTENSIONS
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.openlocfilehash: 9e82ec9ec638cb70cc7b571ed9e5e76d604cd4da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979713"
---
# <a name="fm_reload_extensions-message"></a><span data-ttu-id="fcd19-103">FM-Nachricht zum erneuten \_ Laden \_</span><span class="sxs-lookup"><span data-stu-id="fcd19-103">FM\_RELOAD\_EXTENSIONS message</span></span>

<span data-ttu-id="fcd19-104">Wird von einer Datei-Manager-Erweiterung (oder einer anderen Anwendung) gesendet, damit der Datei-Manager alle Erweiterungs-DLLs erneut lädt, die im \[ Abschnitt "Addons" \] der Winfile.ini Datei aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="fcd19-104">Sent by a File Manager extension (or another application) to cause File Manager to reload all extension DLLs listed in the \[AddOns\] section of the Winfile.ini file.</span></span>

## <a name="parameters"></a><span data-ttu-id="fcd19-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="fcd19-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcd19-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fcd19-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fcd19-107">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="fcd19-107">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="fcd19-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fcd19-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fcd19-109">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="fcd19-109">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcd19-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fcd19-110">Return value</span></span>

<span data-ttu-id="fcd19-111">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="fcd19-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcd19-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fcd19-112">Remarks</span></span>

<span data-ttu-id="fcd19-113">Andere Anwendungen können die [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) -Funktion verwenden, um diese Nachricht an den Datei-Manager zu senden.</span><span class="sxs-lookup"><span data-stu-id="fcd19-113">Other applications can use the [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) function to send this message to File Manager.</span></span> <span data-ttu-id="fcd19-114">Zum Abrufen des entsprechenden Datei-Manager-Fenster Handles kann eine Anwendung \_ in einem Aufrufen der [**FindWindow**](/windows/win32/api/winuser/nf-winuser-findwindowa) -Funktion als *lpszClassName* -Parameter "WFS-Frame" angeben.</span><span class="sxs-lookup"><span data-stu-id="fcd19-114">To obtain the appropriate File Manager window handle, an application can specify "WFS\_Frame" as the *lpszClassName* parameter in a call to the [**FindWindow**](/windows/win32/api/winuser/nf-winuser-findwindowa) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcd19-115">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="fcd19-115">Requirements</span></span>



| <span data-ttu-id="fcd19-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fcd19-116">Requirement</span></span> | <span data-ttu-id="fcd19-117">Wert</span><span class="sxs-lookup"><span data-stu-id="fcd19-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fcd19-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fcd19-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fcd19-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fcd19-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="fcd19-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fcd19-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fcd19-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fcd19-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fcd19-122">Header</span><span class="sxs-lookup"><span data-stu-id="fcd19-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="fcd19-123"><dt>WF. h</dt></span><span class="sxs-lookup"><span data-stu-id="fcd19-123"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fcd19-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="fcd19-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcd19-125">**"F"**</span><span class="sxs-lookup"><span data-stu-id="fcd19-125">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 

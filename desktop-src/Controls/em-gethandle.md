---
title: EM_GETHANDLE Meldung (Winuser. h)
description: Ruft ein Handle des Speichers ab, der dem Text eines mehrzeiligen Bearbeitungs Steuer Elements zugeordnet ist.
ms.assetid: 74271812-9715-4a46-96b3-0788134f8143
keywords:
- Windows-Steuerelemente für EM_GETHANDLE Meldung
topic_type:
- apiref
api_name:
- EM_GETHANDLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88a466394b48d2d726621e50a7e2c5df2f747f08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518299"
---
# <a name="em_gethandle-message"></a><span data-ttu-id="a118a-104">\_GetHandle-Nachricht</span><span class="sxs-lookup"><span data-stu-id="a118a-104">EM\_GETHANDLE message</span></span>

<span data-ttu-id="a118a-105">Ruft ein Handle des Speichers ab, der dem Text eines mehrzeiligen Bearbeitungs Steuer Elements zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a118a-105">Gets a handle of the memory currently allocated for a multiline edit control's text.</span></span>

## <a name="parameters"></a><span data-ttu-id="a118a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a118a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a118a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a118a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a118a-108">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="a118a-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a118a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a118a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a118a-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="a118a-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a118a-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a118a-111">Return value</span></span>

<span data-ttu-id="a118a-112">Der Rückgabewert ist ein Speicher handle, das den Puffer identifiziert, der den Inhalt des Bearbeitungs Steuer Elements enthält.</span><span class="sxs-lookup"><span data-stu-id="a118a-112">The return value is a memory handle identifying the buffer that holds the content of the edit control.</span></span> <span data-ttu-id="a118a-113">Wenn ein Fehler auftritt, z. b. das Senden der Nachricht an ein einzeilige Bearbeitungs Steuerelement, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="a118a-113">If an error occurs, such as sending the message to a single-line edit control, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="a118a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a118a-114">Remarks</span></span>

<span data-ttu-id="a118a-115">Wenn die Funktion erfolgreich ausgeführt wird, kann die Anwendung auf den Inhalt des Bearbeitungs Steuer Elements zugreifen, indem Sie den Rückgabewert in [**hlocal**](/windows/desktop/WinProg/windows-data-types) umwandeln und an [**loczuweisung**](/windows/desktop/api/winbase/nf-winbase-locallock)übergibt.</span><span class="sxs-lookup"><span data-stu-id="a118a-115">If the function succeeds, the application can access the contents of the edit control by casting the return value to [**HLOCAL**](/windows/desktop/WinProg/windows-data-types) and passing it to [**LocalLock**](/windows/desktop/api/winbase/nf-winbase-locallock).</span></span> <span data-ttu-id="a118a-116">**Loczuweisung** gibt einen Zeiger auf einen Puffer zurück, der ein mit Null endendes Array von **char** s oder **WCHAR** s ist, je nachdem, ob eine ANSI-oder Unicode-Funktion das Steuerelement erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="a118a-116">**LocalLock** returns a pointer to a buffer that is a null-terminated array of **CHAR** s or **WCHAR** s, depending on whether an ANSI or Unicode function created the control.</span></span> <span data-ttu-id="a118a-117">Wenn z. b. " [**featewindowexa**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " verwendet wurde, ist der Puffer ein Array von " **char** s", aber wenn " **featewindowexw** " verwendet wurde, ist der Puffer ein Array von **WCHAR** s.</span><span class="sxs-lookup"><span data-stu-id="a118a-117">For example, if [**CreateWindowExA**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) was used the buffer is an array of **CHAR** s, but if **CreateWindowExW** was used the buffer is an array of **WCHAR** s.</span></span> <span data-ttu-id="a118a-118">Der Inhalt des Puffers wird möglicherweise nicht von der Anwendung geändert.</span><span class="sxs-lookup"><span data-stu-id="a118a-118">The application may not change the contents of the buffer.</span></span> <span data-ttu-id="a118a-119">Um den Puffer zu entsperren, ruft die Anwendung [**localunlock**](/windows/desktop/api/winbase/nf-winbase-localunlock) auf, bevor das Bearbeitungs Steuerelement neue Nachrichten empfangen kann.</span><span class="sxs-lookup"><span data-stu-id="a118a-119">To unlock the buffer, the application calls [**LocalUnlock**](/windows/desktop/api/winbase/nf-winbase-localunlock) before allowing the edit control to receive new messages.</span></span>

> [!Note]  
> <span data-ttu-id="a118a-120">Für Comctl32.dll Version 6 enthält der Puffer immer ein Array von **WCHAR** s, unabhängig davon, ob eine ANSI-oder Unicode-Funktion das Bearbeitungs Steuerelement erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="a118a-120">For Comctl32.dll version 6, the buffer always contains an array of **WCHAR** s, regardless of whether an ANSI or Unicode function created the edit control.</span></span> <span data-ttu-id="a118a-121">Weitere Informationen zu DLL-Versionen finden Sie unter [allgemeine Steuerelement Versionen](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="a118a-121">For more information on DLL versions, see [Common Control Versions](common-control-versions.md).</span></span>

 

<span data-ttu-id="a118a-122">Wenn Ihre Anwendung die von **EM \_ GetHandle** vorgegebenen Einschränkungen nicht einhalten kann, verwenden Sie die Funktionen [**getwindowtextlength**](/windows/desktop/api/winuser/nf-winuser-getwindowtextlengtha) und [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) , um den Inhalt des Bearbeitungs Steuer Elements in einen von der Anwendung bereitgestellten Puffer zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="a118a-122">If your application cannot abide by the restrictions imposed by **EM\_GETHANDLE**, use the [**GetWindowTextLength**](/windows/desktop/api/winuser/nf-winuser-getwindowtextlengtha) and [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) functions to copy the contents of the edit control into an application-provided buffer.</span></span>

<span data-ttu-id="a118a-123">Umfassende **Bearbeitung:** Die **\_ GetHandle** -Nachricht wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a118a-123">**Rich Edit:** The **EM\_GETHANDLE** message is not supported.</span></span> <span data-ttu-id="a118a-124">Rich Edit-Steuerelemente speichern Text nicht als einfaches Zeichen Array.</span><span class="sxs-lookup"><span data-stu-id="a118a-124">Rich edit controls do not store text as a simple array of characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="a118a-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a118a-125">Requirements</span></span>



| <span data-ttu-id="a118a-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a118a-126">Requirement</span></span> | <span data-ttu-id="a118a-127">Wert</span><span class="sxs-lookup"><span data-stu-id="a118a-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a118a-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a118a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a118a-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a118a-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a118a-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a118a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a118a-131">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a118a-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a118a-132">Header</span><span class="sxs-lookup"><span data-stu-id="a118a-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="a118a-133"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="a118a-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a118a-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a118a-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="a118a-135">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="a118a-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a118a-136">**EM- \_ andle**</span><span class="sxs-lookup"><span data-stu-id="a118a-136">**EM\_SETHANDLE**</span></span>](em-sethandle.md)
</dt> <dt>

<span data-ttu-id="a118a-137">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="a118a-137">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="a118a-138">**GetWindowText**</span><span class="sxs-lookup"><span data-stu-id="a118a-138">**GetWindowText**</span></span>](/windows/desktop/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[<span data-ttu-id="a118a-139">**Getwindowtextlength**</span><span class="sxs-lookup"><span data-stu-id="a118a-139">**GetWindowTextLength**</span></span>](/windows/desktop/api/winuser/nf-winuser-getwindowtextlengtha)
</dt> <dt>

[<span data-ttu-id="a118a-140">**Loczuweisung**</span><span class="sxs-lookup"><span data-stu-id="a118a-140">**LocalLock**</span></span>](/windows/desktop/api/winbase/nf-winbase-locallock)
</dt> <dt>

[<span data-ttu-id="a118a-141">**Localunlock**</span><span class="sxs-lookup"><span data-stu-id="a118a-141">**LocalUnlock**</span></span>](/windows/desktop/api/winbase/nf-winbase-localunlock)
</dt> </dl>

 


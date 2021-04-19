---
description: Wird verwendet, um private Nachrichten für die Verwendung durch private Fenster Klassen zu definieren, in der Regel in der Form OCM \_ \_ Base + x, wobei x ein ganzzahliger Wert ist.
ms.assetid: b1a9c0ca-349d-49d2-9b8b-ae7d3bf94c10
title: OCM__BASE (OLECTL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bc79cc842a7f25ba66dc8d807c5ab355fc04547
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356179"
---
# <a name="ocm__base"></a><span data-ttu-id="646bb-103">OCM- \_ \_ Basis</span><span class="sxs-lookup"><span data-stu-id="646bb-103">OCM\_\_BASE</span></span>

<span data-ttu-id="646bb-104">Wird verwendet, um private Nachrichten für die Verwendung durch private Fenster Klassen zu definieren, in der Regel in der Form **OCM \_ \_ Base** + *x*, wobei *x* ein ganzzahliger Wert ist.</span><span class="sxs-lookup"><span data-stu-id="646bb-104">Used to define private messages for use by private window classes, usually of the form **OCM\_\_BASE**+*x*, where *x* is an integer value.</span></span>

``` syntax
#define WM_USER                   0x0400
#define OCM__BASE                (WM_USER+0x1c00)
```

## <a name="remarks"></a><span data-ttu-id="646bb-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="646bb-105">Remarks</span></span>

<span data-ttu-id="646bb-106">Im folgenden finden Sie die Bereiche der Nachrichtennummern.</span><span class="sxs-lookup"><span data-stu-id="646bb-106">The following are the ranges of message numbers.</span></span>



| <span data-ttu-id="646bb-107">Range</span><span class="sxs-lookup"><span data-stu-id="646bb-107">Range</span></span>                                                 | <span data-ttu-id="646bb-108">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="646bb-108">Meaning</span></span>                                                        |
|-------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="646bb-109">0 bis [**WM \_ Benutzer**](wm-user.md)  1</span><span class="sxs-lookup"><span data-stu-id="646bb-109">0 through [**WM\_USER**](wm-user.md)  1</span></span><br/>   | <span data-ttu-id="646bb-110">Nachrichten, die für die Verwendung durch das System reserviert sind</span><span class="sxs-lookup"><span data-stu-id="646bb-110">Messages reserved for use by the system.</span></span><br/>            |
| <span data-ttu-id="646bb-111">[**WM \_ Benutzer**](wm-user.md) über 0x7FFF</span><span class="sxs-lookup"><span data-stu-id="646bb-111">[**WM\_USER**](wm-user.md) through 0x7FFF</span></span><br/> | <span data-ttu-id="646bb-112">Ganzzahlige Nachrichten, die von privaten Fenster Klassen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="646bb-112">Integer messages for use by private window classes.</span></span><br/> |
| <span data-ttu-id="646bb-113">[**WM \_ App**](wm-app.md) über 0xbfff</span><span class="sxs-lookup"><span data-stu-id="646bb-113">[**WM\_APP**](wm-app.md) through 0xBFFF</span></span><br/>   | <span data-ttu-id="646bb-114">Nachrichten, die für die Verwendung durch Anwendungen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="646bb-114">Messages available for use by applications.</span></span><br/>         |
| <span data-ttu-id="646bb-115">0xc000 bis 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="646bb-115">0xC000 through 0xFFFF</span></span><br/>                      | <span data-ttu-id="646bb-116">Zeichen folgen Nachrichten zur Verwendung durch Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="646bb-116">String messages for use by applications.</span></span><br/>            |
| <span data-ttu-id="646bb-117">Größer als 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="646bb-117">Greater than 0xFFFF</span></span><br/>                        | <span data-ttu-id="646bb-118">Vom System reserviert.</span><span class="sxs-lookup"><span data-stu-id="646bb-118">Reserved by the system.</span></span><br/>                             |



 

<span data-ttu-id="646bb-119">Die Nachrichtennummern im ersten Bereich (0 bis [**WM \_ Benutzer**](wm-user.md)  1) werden vom System definiert.</span><span class="sxs-lookup"><span data-stu-id="646bb-119">Message numbers in the first range (0 through [**WM\_USER**](wm-user.md)  1) are defined by the system.</span></span> <span data-ttu-id="646bb-120">Werte in diesem Bereich, die nicht explizit definiert sind, werden vom System reserviert.</span><span class="sxs-lookup"><span data-stu-id="646bb-120">Values in this range that are not explicitly defined are reserved by the system.</span></span>

<span data-ttu-id="646bb-121">Nachrichtennummern im zweiten Bereich ([**WM- \_ Benutzer**](wm-user.md) bis 0x7FFF) können definiert und von einer Anwendung verwendet werden, um Nachrichten innerhalb einer privaten Fenster Klasse zu senden.</span><span class="sxs-lookup"><span data-stu-id="646bb-121">Message numbers in the second range ([**WM\_USER**](wm-user.md) through 0x7FFF) can be defined and used by an application to send messages within a private window class.</span></span> <span data-ttu-id="646bb-122">Diese Werte können nicht verwendet werden, um Nachrichten zu definieren, die in einer Anwendung sinnvoll sind, da einige vordefinierte Fenster Klassen bereits Werte in diesem Bereich definieren.</span><span class="sxs-lookup"><span data-stu-id="646bb-122">These values cannot be used to define messages that are meaningful throughout an application because some predefined window classes already define values in this range.</span></span> <span data-ttu-id="646bb-123">Beispielsweise können von vordefinierten Steuerelement Klassen wie **Button**, **Edit**, **ListBox** und **ComboBox** diese Werte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="646bb-123">For example, predefined control classes such as **BUTTON**, **EDIT**, **LISTBOX**, and **COMBOBOX** may use these values.</span></span> <span data-ttu-id="646bb-124">Nachrichten in diesem Bereich sollten nicht an andere Anwendungen gesendet werden, es sei denn, die Anwendungen wurden zum Austauschen von Nachrichten und zum Anfügen derselben Bedeutung an die Nachrichtennummern entwickelt.</span><span class="sxs-lookup"><span data-stu-id="646bb-124">Messages in this range should not be sent to other applications unless the applications have been designed to exchange messages and to attach the same meaning to the message numbers.</span></span>

<span data-ttu-id="646bb-125">Die Nachrichtennummern im dritten Bereich (0X8000 bis 0xbfff) sind für Anwendungen verfügbar, die als private Nachrichten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="646bb-125">Message numbers in the third range (0x8000 through 0xBFFF) are available for applications to use as private messages.</span></span> <span data-ttu-id="646bb-126">Nachrichten in diesem Bereich stehen nicht in Konflikt mit Systemmeldungen.</span><span class="sxs-lookup"><span data-stu-id="646bb-126">Messages in this range do not conflict with system messages.</span></span>

<span data-ttu-id="646bb-127">Die Nachrichtennummern im vierten Bereich (0xc000 bis 0xFFFF) werden zur Laufzeit definiert, wenn eine Anwendung die [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) -Funktion aufruft, um eine Nachrichtennummer für eine Zeichenfolge abzurufen.</span><span class="sxs-lookup"><span data-stu-id="646bb-127">Message numbers in the fourth range (0xC000 through 0xFFFF) are defined at run time when an application calls the [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) function to retrieve a message number for a string.</span></span> <span data-ttu-id="646bb-128">Alle Anwendungen, die dieselbe Zeichenfolge registrieren, können die zugeordnete Nachrichtennummer zum Austauschen von Nachrichten verwenden.</span><span class="sxs-lookup"><span data-stu-id="646bb-128">All applications that register the same string can use the associated message number for exchanging messages.</span></span> <span data-ttu-id="646bb-129">Die tatsächliche Nachrichtennummer ist jedoch keine Konstante und kann nicht davon ausgegangen werden, dass Sie zwischen verschiedenen Sitzungen identisch ist.</span><span class="sxs-lookup"><span data-stu-id="646bb-129">The actual message number, however, is not a constant and cannot be assumed to be the same between different sessions.</span></span>

<span data-ttu-id="646bb-130">Die Nachrichtennummern im fünften Bereich (größer als 0xFFFF) werden vom System reserviert.</span><span class="sxs-lookup"><span data-stu-id="646bb-130">Message numbers in the fifth range (greater than 0xFFFF) are reserved by the system.</span></span>

## <a name="requirements"></a><span data-ttu-id="646bb-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="646bb-131">Requirements</span></span>



| <span data-ttu-id="646bb-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="646bb-132">Requirement</span></span> | <span data-ttu-id="646bb-133">Wert</span><span class="sxs-lookup"><span data-stu-id="646bb-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="646bb-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="646bb-134">Minimum supported client</span></span><br/> | <span data-ttu-id="646bb-135">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="646bb-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="646bb-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="646bb-136">Minimum supported server</span></span><br/> | <span data-ttu-id="646bb-137">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="646bb-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="646bb-138">Header</span><span class="sxs-lookup"><span data-stu-id="646bb-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="646bb-139"><dt>OLECTL. h</dt></span><span class="sxs-lookup"><span data-stu-id="646bb-139"><dt>Olectl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="646bb-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="646bb-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="646bb-141">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="646bb-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="646bb-142">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="646bb-142">**RegisterWindowMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

[<span data-ttu-id="646bb-143">**WM- \_ App**</span><span class="sxs-lookup"><span data-stu-id="646bb-143">**WM\_APP**</span></span>](wm-app.md)
</dt> <dt>

<span data-ttu-id="646bb-144">**Licher**</span><span class="sxs-lookup"><span data-stu-id="646bb-144">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="646bb-145">Nachrichten und Nachrichten Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="646bb-145">Messages and Message Queues</span></span>](messages-and-message-queues.md)
</dt> </dl>

 


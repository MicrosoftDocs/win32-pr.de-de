---
description: Wird verwendet, um private Nachrichten für die Verwendung durch private Fenster Klassen zu definieren, in der Regel im Format WM \_ User + x, wobei x ein ganzzahliger Wert ist.
ms.assetid: 4115c587-fcb4-4170-9948-fe33bcb8742a
title: WM_USER (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1efd6f2e79180b7dc627281829539d20f5fa74d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041697"
---
# <a name="wm_user"></a><span data-ttu-id="eac62-103">WM- \_ Benutzer</span><span class="sxs-lookup"><span data-stu-id="eac62-103">WM\_USER</span></span>

<span data-ttu-id="eac62-104">Wird verwendet, um private Nachrichten für die Verwendung durch private Fenster Klassen zu definieren, in der Regel im Format **WM \_ User** + *x*, wobei *x* ein ganzzahliger Wert ist.</span><span class="sxs-lookup"><span data-stu-id="eac62-104">Used to define private messages for use by private window classes, usually of the form **WM\_USER**+*x*, where *x* is an integer value.</span></span>

``` syntax
#define WM_USER                         0x0400
```

## <a name="remarks"></a><span data-ttu-id="eac62-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eac62-105">Remarks</span></span>

<span data-ttu-id="eac62-106">Im folgenden finden Sie die Bereiche der Nachrichtennummern.</span><span class="sxs-lookup"><span data-stu-id="eac62-106">The following are the ranges of message numbers.</span></span>



| <span data-ttu-id="eac62-107">Range</span><span class="sxs-lookup"><span data-stu-id="eac62-107">Range</span></span>                                                        | <span data-ttu-id="eac62-108">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="eac62-108">Meaning</span></span>                                                        |
|--------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="eac62-109">0 bis **WM \_ Benutzer** – 1</span><span class="sxs-lookup"><span data-stu-id="eac62-109">0 through **WM\_USER** –1</span></span><br/>                         | <span data-ttu-id="eac62-110">Nachrichten, die für die Verwendung durch das System reserviert sind</span><span class="sxs-lookup"><span data-stu-id="eac62-110">Messages reserved for use by the system.</span></span><br/>            |
| <span data-ttu-id="eac62-111">**WM \_ Benutzer** über 0x7FFF</span><span class="sxs-lookup"><span data-stu-id="eac62-111">**WM\_USER** through 0x7FFF</span></span><br/>                       | <span data-ttu-id="eac62-112">Ganzzahlige Nachrichten, die von privaten Fenster Klassen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eac62-112">Integer messages for use by private window classes.</span></span><br/> |
| <span data-ttu-id="eac62-113">[**WM \_ App**](wm-app.md) (0X8000) bis 0xbfff</span><span class="sxs-lookup"><span data-stu-id="eac62-113">[**WM\_APP**](wm-app.md) (0x8000) through 0xBFFF</span></span><br/> | <span data-ttu-id="eac62-114">Nachrichten, die für die Verwendung durch Anwendungen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="eac62-114">Messages available for use by applications.</span></span><br/>         |
| <span data-ttu-id="eac62-115">0xc000 bis 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="eac62-115">0xC000 through 0xFFFF</span></span><br/>                             | <span data-ttu-id="eac62-116">Zeichen folgen Nachrichten zur Verwendung durch Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="eac62-116">String messages for use by applications.</span></span><br/>            |
| <span data-ttu-id="eac62-117">Größer als 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="eac62-117">Greater than 0xFFFF</span></span><br/>                               | <span data-ttu-id="eac62-118">Vom System reserviert.</span><span class="sxs-lookup"><span data-stu-id="eac62-118">Reserved by the system.</span></span><br/>                             |



 

<span data-ttu-id="eac62-119">Die Nachrichtennummern im ersten Bereich (0 bis **WM \_** – 1) werden vom System definiert.</span><span class="sxs-lookup"><span data-stu-id="eac62-119">Message numbers in the first range (0 through **WM\_USER** –1) are defined by the system.</span></span> <span data-ttu-id="eac62-120">Werte in diesem Bereich, die nicht explizit definiert sind, werden vom System reserviert.</span><span class="sxs-lookup"><span data-stu-id="eac62-120">Values in this range that are not explicitly defined are reserved by the system.</span></span>

<span data-ttu-id="eac62-121">Nachrichtennummern im zweiten Bereich (**WM- \_ Benutzer** bis 0x7FFF) können definiert und von einer Anwendung verwendet werden, um Nachrichten innerhalb einer privaten Fenster Klasse zu senden.</span><span class="sxs-lookup"><span data-stu-id="eac62-121">Message numbers in the second range (**WM\_USER** through 0x7FFF) can be defined and used by an application to send messages within a private window class.</span></span> <span data-ttu-id="eac62-122">Diese Werte können nicht verwendet werden, um Nachrichten zu definieren, die in einer Anwendung sinnvoll sind, da einige vordefinierte Fenster Klassen bereits Werte in diesem Bereich definieren.</span><span class="sxs-lookup"><span data-stu-id="eac62-122">These values cannot be used to define messages that are meaningful throughout an application because some predefined window classes already define values in this range.</span></span> <span data-ttu-id="eac62-123">Beispielsweise können von vordefinierten Steuerelement Klassen wie **Button**, **Edit**, **ListBox** und **ComboBox** diese Werte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eac62-123">For example, predefined control classes such as **BUTTON**, **EDIT**, **LISTBOX**, and **COMBOBOX** may use these values.</span></span> <span data-ttu-id="eac62-124">Nachrichten in diesem Bereich sollten nicht an andere Anwendungen gesendet werden, es sei denn, die Anwendungen wurden zum Austauschen von Nachrichten und zum Anfügen derselben Bedeutung an die Nachrichtennummern entwickelt.</span><span class="sxs-lookup"><span data-stu-id="eac62-124">Messages in this range should not be sent to other applications unless the applications have been designed to exchange messages and to attach the same meaning to the message numbers.</span></span>

<span data-ttu-id="eac62-125">Die Nachrichtennummern im dritten Bereich (0X8000 bis 0xbfff) sind für Anwendungen verfügbar, die als private Nachrichten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eac62-125">Message numbers in the third range (0x8000 through 0xBFFF) are available for applications to use as private messages.</span></span> <span data-ttu-id="eac62-126">Nachrichten in diesem Bereich stehen nicht in Konflikt mit Systemmeldungen.</span><span class="sxs-lookup"><span data-stu-id="eac62-126">Messages in this range do not conflict with system messages.</span></span>

<span data-ttu-id="eac62-127">Die Nachrichtennummern im vierten Bereich (0xc000 bis 0xFFFF) werden zur Laufzeit definiert, wenn eine Anwendung die [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) -Funktion aufruft, um eine Nachrichtennummer für eine Zeichenfolge abzurufen.</span><span class="sxs-lookup"><span data-stu-id="eac62-127">Message numbers in the fourth range (0xC000 through 0xFFFF) are defined at run time when an application calls the [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) function to retrieve a message number for a string.</span></span> <span data-ttu-id="eac62-128">Alle Anwendungen, die dieselbe Zeichenfolge registrieren, können die zugeordnete Nachrichtennummer zum Austauschen von Nachrichten verwenden.</span><span class="sxs-lookup"><span data-stu-id="eac62-128">All applications that register the same string can use the associated message number for exchanging messages.</span></span> <span data-ttu-id="eac62-129">Die tatsächliche Nachrichtennummer ist jedoch keine Konstante und kann nicht davon ausgegangen werden, dass Sie zwischen verschiedenen Sitzungen identisch ist.</span><span class="sxs-lookup"><span data-stu-id="eac62-129">The actual message number, however, is not a constant and cannot be assumed to be the same between different sessions.</span></span>

<span data-ttu-id="eac62-130">Die Nachrichtennummern im fünften Bereich (größer als 0xFFFF) werden vom System reserviert.</span><span class="sxs-lookup"><span data-stu-id="eac62-130">Message numbers in the fifth range (greater than 0xFFFF) are reserved by the system.</span></span>

## <a name="requirements"></a><span data-ttu-id="eac62-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eac62-131">Requirements</span></span>



| <span data-ttu-id="eac62-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eac62-132">Requirement</span></span> | <span data-ttu-id="eac62-133">Wert</span><span class="sxs-lookup"><span data-stu-id="eac62-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eac62-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eac62-134">Minimum supported client</span></span><br/> | <span data-ttu-id="eac62-135">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eac62-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="eac62-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eac62-136">Minimum supported server</span></span><br/> | <span data-ttu-id="eac62-137">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eac62-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="eac62-138">Header</span><span class="sxs-lookup"><span data-stu-id="eac62-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="eac62-139"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="eac62-139"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eac62-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eac62-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="eac62-141">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="eac62-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="eac62-142">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="eac62-142">**RegisterWindowMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

[<span data-ttu-id="eac62-143">**WM- \_ App**</span><span class="sxs-lookup"><span data-stu-id="eac62-143">**WM\_APP**</span></span>](wm-app.md)
</dt> <dt>

<span data-ttu-id="eac62-144">**Licher**</span><span class="sxs-lookup"><span data-stu-id="eac62-144">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="eac62-145">Nachrichten und Nachrichten Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="eac62-145">Messages and Message Queues</span></span>](messages-and-message-queues.md)
</dt> </dl>

 

 

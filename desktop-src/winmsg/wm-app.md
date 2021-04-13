---
description: Wird verwendet, um private Nachrichten zu definieren, in der Regel in der Form WM \_ app + x, wobei x ein ganzzahliger Wert ist.
ms.assetid: fdb549df-426f-4af5-9c17-6e8730e4abc0
title: WM_APP (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4998f8240b08d248a75b375bb813ba02cd02344e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216963"
---
# <a name="wm_app"></a><span data-ttu-id="e6885-103">WM- \_ App</span><span class="sxs-lookup"><span data-stu-id="e6885-103">WM\_APP</span></span>

<span data-ttu-id="e6885-104">Wird verwendet, um private Nachrichten zu definieren, in der Regel in der Form **WM \_ App** + *x*, wobei *x* ein ganzzahliger Wert ist.</span><span class="sxs-lookup"><span data-stu-id="e6885-104">Used to define private messages, usually of the form **WM\_APP**+*x*, where *x* is an integer value.</span></span>

``` syntax
#define WM_APP                          0x8000
```

## <a name="remarks"></a><span data-ttu-id="e6885-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e6885-105">Remarks</span></span>

<span data-ttu-id="e6885-106">Die **\_ App** -Konstante der WM wird verwendet, um zwischen Nachrichten Werten zu unterscheiden, die für die Verwendung durch das System reserviert sind, und Werte, die von einer Anwendung verwendet werden können, um Nachrichten innerhalb einer privaten Fenster Klasse zu senden.</span><span class="sxs-lookup"><span data-stu-id="e6885-106">The **WM\_APP** constant is used to distinguish between message values that are reserved for use by the system and values that can be used by an application to send messages within a private window class.</span></span> <span data-ttu-id="e6885-107">Im folgenden finden Sie die verfügbaren Bereiche der Nachrichtennummern.</span><span class="sxs-lookup"><span data-stu-id="e6885-107">The following are the ranges of message numbers available.</span></span>



| <span data-ttu-id="e6885-108">Range</span><span class="sxs-lookup"><span data-stu-id="e6885-108">Range</span></span>                                                 | <span data-ttu-id="e6885-109">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e6885-109">Meaning</span></span>                                                        |
|-------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="e6885-110">0 bis [**WM \_ Benutzer**](wm-user.md) – 1</span><span class="sxs-lookup"><span data-stu-id="e6885-110">0 through [**WM\_USER**](wm-user.md) –1</span></span><br/>   | <span data-ttu-id="e6885-111">Nachrichten, die für die Verwendung durch das System reserviert sind</span><span class="sxs-lookup"><span data-stu-id="e6885-111">Messages reserved for use by the system.</span></span><br/>            |
| <span data-ttu-id="e6885-112">[**WM \_ Benutzer**](wm-user.md) über 0x7FFF</span><span class="sxs-lookup"><span data-stu-id="e6885-112">[**WM\_USER**](wm-user.md) through 0x7FFF</span></span><br/> | <span data-ttu-id="e6885-113">Ganzzahlige Nachrichten, die von privaten Fenster Klassen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e6885-113">Integer messages for use by private window classes.</span></span><br/> |
| <span data-ttu-id="e6885-114">**WM \_ App** über 0xbfff</span><span class="sxs-lookup"><span data-stu-id="e6885-114">**WM\_APP** through 0xBFFF</span></span><br/>                 | <span data-ttu-id="e6885-115">Nachrichten, die für die Verwendung durch Anwendungen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="e6885-115">Messages available for use by applications.</span></span><br/>         |
| <span data-ttu-id="e6885-116">0xc000 bis 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="e6885-116">0xC000 through 0xFFFF</span></span><br/>                      | <span data-ttu-id="e6885-117">Zeichen folgen Nachrichten zur Verwendung durch Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="e6885-117">String messages for use by applications.</span></span><br/>            |
| <span data-ttu-id="e6885-118">Größer als 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="e6885-118">Greater than 0xFFFF</span></span><br/>                        | <span data-ttu-id="e6885-119">Vom System reserviert.</span><span class="sxs-lookup"><span data-stu-id="e6885-119">Reserved by the system.</span></span><br/>                             |



 

<span data-ttu-id="e6885-120">Die Nachrichtennummern im ersten Bereich (0 bis [**WM \_**](wm-user.md) – 1) werden vom System definiert.</span><span class="sxs-lookup"><span data-stu-id="e6885-120">Message numbers in the first range (0 through [**WM\_USER**](wm-user.md) –1) are defined by the system.</span></span> <span data-ttu-id="e6885-121">Werte in diesem Bereich, die nicht explizit definiert sind, werden vom System reserviert.</span><span class="sxs-lookup"><span data-stu-id="e6885-121">Values in this range that are not explicitly defined are reserved by the system.</span></span>

<span data-ttu-id="e6885-122">Nachrichtennummern im zweiten Bereich ([**WM- \_ Benutzer**](wm-user.md) bis 0x7FFF) können definiert und von einer Anwendung verwendet werden, um Nachrichten innerhalb einer privaten Fenster Klasse zu senden.</span><span class="sxs-lookup"><span data-stu-id="e6885-122">Message numbers in the second range ([**WM\_USER**](wm-user.md) through 0x7FFF) can be defined and used by an application to send messages within a private window class.</span></span> <span data-ttu-id="e6885-123">Diese Werte können nicht verwendet werden, um Nachrichten zu definieren, die in einer Anwendung sinnvoll sind, da einige vordefinierte Fenster Klassen bereits Werte in diesem Bereich definieren.</span><span class="sxs-lookup"><span data-stu-id="e6885-123">These values cannot be used to define messages that are meaningful throughout an application because some predefined window classes already define values in this range.</span></span> <span data-ttu-id="e6885-124">Beispielsweise können von vordefinierten Steuerelement Klassen wie **Button**, **Edit**, **ListBox** und **ComboBox** diese Werte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e6885-124">For example, predefined control classes such as **BUTTON**, **EDIT**, **LISTBOX**, and **COMBOBOX** may use these values.</span></span> <span data-ttu-id="e6885-125">Nachrichten in diesem Bereich sollten nicht an andere Anwendungen gesendet werden, es sei denn, die Anwendungen wurden zum Austauschen von Nachrichten und zum Anfügen derselben Bedeutung an die Nachrichtennummern entwickelt.</span><span class="sxs-lookup"><span data-stu-id="e6885-125">Messages in this range should not be sent to other applications unless the applications have been designed to exchange messages and to attach the same meaning to the message numbers.</span></span>

<span data-ttu-id="e6885-126">Die Nachrichtennummern im dritten Bereich (0X8000 bis 0xbfff) sind für Anwendungen verfügbar, die als private Nachrichten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e6885-126">Message numbers in the third range (0x8000 through 0xBFFF) are available for applications to use as private messages.</span></span> <span data-ttu-id="e6885-127">Nachrichten in diesem Bereich stehen nicht in Konflikt mit Systemmeldungen.</span><span class="sxs-lookup"><span data-stu-id="e6885-127">Messages in this range do not conflict with system messages.</span></span>

<span data-ttu-id="e6885-128">Die Nachrichtennummern im vierten Bereich (0xc000 bis 0xFFFF) werden zur Laufzeit definiert, wenn eine Anwendung die [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) -Funktion aufruft, um eine Nachrichtennummer für eine Zeichenfolge abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e6885-128">Message numbers in the fourth range (0xC000 through 0xFFFF) are defined at run time when an application calls the [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) function to retrieve a message number for a string.</span></span> <span data-ttu-id="e6885-129">Alle Anwendungen, die dieselbe Zeichenfolge registrieren, können die zugeordnete Nachrichtennummer zum Austauschen von Nachrichten verwenden.</span><span class="sxs-lookup"><span data-stu-id="e6885-129">All applications that register the same string can use the associated message number for exchanging messages.</span></span> <span data-ttu-id="e6885-130">Die tatsächliche Nachrichtennummer ist jedoch keine Konstante und kann nicht davon ausgegangen werden, dass Sie zwischen verschiedenen Sitzungen identisch ist.</span><span class="sxs-lookup"><span data-stu-id="e6885-130">The actual message number, however, is not a constant and cannot be assumed to be the same between different sessions.</span></span>

<span data-ttu-id="e6885-131">Die Nachrichtennummern im fünften Bereich (größer als 0xFFFF) werden vom System reserviert.</span><span class="sxs-lookup"><span data-stu-id="e6885-131">Message numbers in the fifth range (greater than 0xFFFF) are reserved by the system.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6885-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e6885-132">Requirements</span></span>



| <span data-ttu-id="e6885-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e6885-133">Requirement</span></span> | <span data-ttu-id="e6885-134">Wert</span><span class="sxs-lookup"><span data-stu-id="e6885-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6885-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e6885-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e6885-136">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e6885-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e6885-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e6885-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e6885-138">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e6885-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e6885-139">Header</span><span class="sxs-lookup"><span data-stu-id="e6885-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6885-140"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="e6885-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6885-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6885-141">See also</span></span>

<dl> <dt>

<span data-ttu-id="e6885-142">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="e6885-142">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e6885-143">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="e6885-143">**RegisterWindowMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

[<span data-ttu-id="e6885-144">**WM- \_ Benutzer**</span><span class="sxs-lookup"><span data-stu-id="e6885-144">**WM\_USER**</span></span>](wm-user.md)
</dt> <dt>

<span data-ttu-id="e6885-145">**Licher**</span><span class="sxs-lookup"><span data-stu-id="e6885-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e6885-146">Nachrichten und Nachrichten Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="e6885-146">Messages and Message Queues</span></span>](messages-and-message-queues.md)
</dt> </dl>

 

 

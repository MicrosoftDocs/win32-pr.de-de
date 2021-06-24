---
description: Wird verwendet, um private Nachrichten für die Verwendung durch private Fensterklassen zu definieren, in der Regel im Format OCM \_ \_ BASE+x, wobei x ein ganzzahliger Wert ist.
ms.assetid: b1a9c0ca-349d-49d2-9b8b-ae7d3bf94c10
title: OCM__BASE (Olectl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa3713d8a7b7447430e914e2582089244a417b1c
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2021
ms.locfileid: "112588057"
---
# <a name="ocm__base"></a><span data-ttu-id="a104a-103">OCM \_ \_ BASE</span><span class="sxs-lookup"><span data-stu-id="a104a-103">OCM\_\_BASE</span></span>

<span data-ttu-id="a104a-104">Wird verwendet, um private Nachrichten für die Verwendung durch private Fensterklassen zu definieren, in der Regel im Format **OCM \_ \_ BASE** + *x*, wobei *x* ein ganzzahliger Wert ist.</span><span class="sxs-lookup"><span data-stu-id="a104a-104">Used to define private messages for use by private window classes, usually of the form **OCM\_\_BASE**+*x*, where *x* is an integer value.</span></span>

``` syntax
#define WM_USER                   0x0400
#define OCM__BASE                (WM_USER+0x1c00)
```

## <a name="remarks"></a><span data-ttu-id="a104a-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a104a-105">Remarks</span></span>

<span data-ttu-id="a104a-106">Im Folgenden werden die Bereiche von Nachrichtennummern angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a104a-106">The following are the ranges of message numbers.</span></span>



| <span data-ttu-id="a104a-107">Range</span><span class="sxs-lookup"><span data-stu-id="a104a-107">Range</span></span>                                                 | <span data-ttu-id="a104a-108">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a104a-108">Meaning</span></span>                                                        |
|-------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="a104a-109">0 bis [**WM \_ USER**](wm-user.md)-1</span><span class="sxs-lookup"><span data-stu-id="a104a-109">0 through [**WM\_USER**](wm-user.md)-1</span></span><br/>   | <span data-ttu-id="a104a-110">Nachrichten, die für die Verwendung durch das System reserviert sind.</span><span class="sxs-lookup"><span data-stu-id="a104a-110">Messages reserved for use by the system.</span></span><br/>            |
| <span data-ttu-id="a104a-111">[**WM \_ USER**](wm-user.md) über 0x7FFF</span><span class="sxs-lookup"><span data-stu-id="a104a-111">[**WM\_USER**](wm-user.md) through 0x7FFF</span></span><br/> | <span data-ttu-id="a104a-112">Ganzzahlige Nachrichten für die Verwendung durch private Fensterklassen.</span><span class="sxs-lookup"><span data-stu-id="a104a-112">Integer messages for use by private window classes.</span></span><br/> |
| <span data-ttu-id="a104a-113">[**WM \_ APP**](wm-app.md) über 0xBFFF</span><span class="sxs-lookup"><span data-stu-id="a104a-113">[**WM\_APP**](wm-app.md) through 0xBFFF</span></span><br/>   | <span data-ttu-id="a104a-114">Nachrichten, die für die Verwendung durch Anwendungen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="a104a-114">Messages available for use by applications.</span></span><br/>         |
| <span data-ttu-id="a104a-115">0xC000 über 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="a104a-115">0xC000 through 0xFFFF</span></span><br/>                      | <span data-ttu-id="a104a-116">Zeichenfolgenmeldungen zur Verwendung durch Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="a104a-116">String messages for use by applications.</span></span><br/>            |
| <span data-ttu-id="a104a-117">Größer als 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="a104a-117">Greater than 0xFFFF</span></span><br/>                        | <span data-ttu-id="a104a-118">Vom System reserviert.</span><span class="sxs-lookup"><span data-stu-id="a104a-118">Reserved by the system.</span></span><br/>                             |



 

<span data-ttu-id="a104a-119">Nachrichtennummern im ersten Bereich (0 bis [**WM \_ USER**](wm-user.md)  1) werden vom System definiert.</span><span class="sxs-lookup"><span data-stu-id="a104a-119">Message numbers in the first range (0 through [**WM\_USER**](wm-user.md)  1) are defined by the system.</span></span> <span data-ttu-id="a104a-120">Werte in diesem Bereich, die nicht explizit definiert sind, werden vom System reserviert.</span><span class="sxs-lookup"><span data-stu-id="a104a-120">Values in this range that are not explicitly defined are reserved by the system.</span></span>

<span data-ttu-id="a104a-121">Nachrichtennummern im zweiten Bereich [**(WM \_ USER**](wm-user.md) bis 0x7FFF) können von einer Anwendung definiert und verwendet werden, um Nachrichten innerhalb einer privaten Fensterklasse zu senden.</span><span class="sxs-lookup"><span data-stu-id="a104a-121">Message numbers in the second range ([**WM\_USER**](wm-user.md) through 0x7FFF) can be defined and used by an application to send messages within a private window class.</span></span> <span data-ttu-id="a104a-122">Diese Werte können nicht verwendet werden, um Nachrichten zu definieren, die in einer Anwendung sinnvoll sind, da einige vordefinierte Fensterklassen bereits Werte in diesem Bereich definieren.</span><span class="sxs-lookup"><span data-stu-id="a104a-122">These values cannot be used to define messages that are meaningful throughout an application because some predefined window classes already define values in this range.</span></span> <span data-ttu-id="a104a-123">Vordefinierte Steuerelementklassen wie **BUTTON,** **EDIT,** **LISTBOX** und **COMBOBOX** können diese Werte beispielsweise verwenden.</span><span class="sxs-lookup"><span data-stu-id="a104a-123">For example, predefined control classes such as **BUTTON**, **EDIT**, **LISTBOX**, and **COMBOBOX** may use these values.</span></span> <span data-ttu-id="a104a-124">Nachrichten in diesem Bereich sollten nicht an andere Anwendungen gesendet werden, es sei denn, die Anwendungen wurden zum Austauschen von Nachrichten und zum Anfügen der gleichen Bedeutung an die Nachrichtennummern entwickelt.</span><span class="sxs-lookup"><span data-stu-id="a104a-124">Messages in this range should not be sent to other applications unless the applications have been designed to exchange messages and to attach the same meaning to the message numbers.</span></span>

<span data-ttu-id="a104a-125">Nachrichtennummern im dritten Bereich (0x8000 bis 0xBFFF) sind für Anwendungen verfügbar, die als private Nachrichten verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="a104a-125">Message numbers in the third range (0x8000 through 0xBFFF) are available for applications to use as private messages.</span></span> <span data-ttu-id="a104a-126">Nachrichten in diesem Bereich verursachen keinen Konflikt mit Systemmeldungen.</span><span class="sxs-lookup"><span data-stu-id="a104a-126">Messages in this range do not conflict with system messages.</span></span>

<span data-ttu-id="a104a-127">Nachrichtennummern im vierten Bereich (0xC000 bis 0xFFFF) werden zur Laufzeit definiert, wenn eine Anwendung die [**RegisterWindowMessage-Funktion**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) aufruft, um eine Nachrichtennummer für eine Zeichenfolge abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a104a-127">Message numbers in the fourth range (0xC000 through 0xFFFF) are defined at run time when an application calls the [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) function to retrieve a message number for a string.</span></span> <span data-ttu-id="a104a-128">Alle Anwendungen, die dieselbe Zeichenfolge registrieren, können die zugeordnete Nachrichtennummer zum Austauschen von Nachrichten verwenden.</span><span class="sxs-lookup"><span data-stu-id="a104a-128">All applications that register the same string can use the associated message number for exchanging messages.</span></span> <span data-ttu-id="a104a-129">Die tatsächliche Nachrichtennummer ist jedoch keine Konstante und kann nicht davon ausgegangen werden, dass sie zwischen verschiedenen Sitzungen identisch ist.</span><span class="sxs-lookup"><span data-stu-id="a104a-129">The actual message number, however, is not a constant and cannot be assumed to be the same between different sessions.</span></span>

<span data-ttu-id="a104a-130">Nachrichtennummern im fünften Bereich (größer als 0xFFFF) werden vom System reserviert.</span><span class="sxs-lookup"><span data-stu-id="a104a-130">Message numbers in the fifth range (greater than 0xFFFF) are reserved by the system.</span></span>

## <a name="requirements"></a><span data-ttu-id="a104a-131">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="a104a-131">Requirements</span></span>



| <span data-ttu-id="a104a-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a104a-132">Requirement</span></span> | <span data-ttu-id="a104a-133">Wert</span><span class="sxs-lookup"><span data-stu-id="a104a-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a104a-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a104a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="a104a-135">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a104a-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a104a-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a104a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="a104a-137">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a104a-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a104a-138">Header</span><span class="sxs-lookup"><span data-stu-id="a104a-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="a104a-139"><dt>Olectl.h</dt></span><span class="sxs-lookup"><span data-stu-id="a104a-139"><dt>Olectl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a104a-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a104a-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="a104a-141">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="a104a-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a104a-142">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="a104a-142">**RegisterWindowMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

[<span data-ttu-id="a104a-143">**\_WM-APP**</span><span class="sxs-lookup"><span data-stu-id="a104a-143">**WM\_APP**</span></span>](wm-app.md)
</dt> <dt>

<span data-ttu-id="a104a-144">**Konzeptionellen**</span><span class="sxs-lookup"><span data-stu-id="a104a-144">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a104a-145">Nachrichten und Nachrichtenwarteschlangen</span><span class="sxs-lookup"><span data-stu-id="a104a-145">Messages and Message Queues</span></span>](messages-and-message-queues.md)
</dt> </dl>

 


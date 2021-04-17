---
description: Benachrichtigt eine appbar, wenn ein Ereignis aufgetreten ist, das sich auf die Größe und Position der appbar auswirken kann.
ms.assetid: 1016a362-4d2b-410e-aec9-c1cc8f497778
title: ABN_POSCHANGED Meldung (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24b0a800b1c112cba18fbadbba79a999ec83c77e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977425"
---
# <a name="abn_poschanged-message"></a><span data-ttu-id="a8328-103">ABN- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="a8328-103">ABN\_POSCHANGED message</span></span>

<span data-ttu-id="a8328-104">Benachrichtigt eine appbar, wenn ein Ereignis aufgetreten ist, das sich auf die Größe und Position der appbar auswirken kann.</span><span class="sxs-lookup"><span data-stu-id="a8328-104">Notifies an appbar when an event has occurred that may affect the appbar's size and position.</span></span> <span data-ttu-id="a8328-105">Zu den Ereignissen zählen Änderungen in der Größe, Position und Sichtbarkeit der Taskleiste sowie das Hinzufügen, entfernen oder Ändern der Größe einer anderen appbar auf der gleichen Seite des Bildschirms.</span><span class="sxs-lookup"><span data-stu-id="a8328-105">Events include changes in the taskbar's size, position, and visibility state, as well as the addition, removal, or resizing of another appbar on the same side of the screen.</span></span>


```C++
ABN_POSCHANGED
```



## <a name="parameters"></a><span data-ttu-id="a8328-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8328-106">Parameters</span></span>

<span data-ttu-id="a8328-107">Diese Nachricht weist keine Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="a8328-107">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a8328-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a8328-108">Return value</span></span>

<span data-ttu-id="a8328-109">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="a8328-109">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8328-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a8328-110">Remarks</span></span>

<span data-ttu-id="a8328-111">Eine appbar sollte auf diese Benachrichtigungs Meldung reagieren, indem die [**ABM- \_ querypos**](abm-querypos.md) -und [**ABM- \_ SetPos**](abm-setpos.md) -Nachrichten gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="a8328-111">An appbar should respond to this notification message by sending the [**ABM\_QUERYPOS**](abm-querypos.md) and [**ABM\_SETPOS**](abm-setpos.md) messages.</span></span> <span data-ttu-id="a8328-112">Wenn sich die Position geändert hat, sollte die appbar die [**MoveWindow**](/windows/desktop/api/winuser/nf-winuser-movewindow) -Funktion zum Verschieben an die neue Position aufruft.</span><span class="sxs-lookup"><span data-stu-id="a8328-112">If its position has changed, the appbar should call the [**MoveWindow**](/windows/desktop/api/winuser/nf-winuser-movewindow) function to move itself to the new position.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8328-113">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="a8328-113">Requirements</span></span>



| <span data-ttu-id="a8328-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a8328-114">Requirement</span></span> | <span data-ttu-id="a8328-115">Wert</span><span class="sxs-lookup"><span data-stu-id="a8328-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a8328-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a8328-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a8328-117">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a8328-117">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a8328-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a8328-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a8328-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a8328-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a8328-120">Header</span><span class="sxs-lookup"><span data-stu-id="a8328-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8328-121"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8328-121"><dt>Shellapi.h</dt></span></span> </dl> |



 


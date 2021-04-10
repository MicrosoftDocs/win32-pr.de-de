---
description: Wird gesendet, wenn ein Benutzer einen Stift Flick ausführt. Ein Fenster empfängt diese Meldung über seine WindowProc-Funktion.
ms.assetid: 9433aadf-3440-4249-8f2c-3e22ebc949fb
title: WM_TABLET_FLICK Meldung (tpcshrd. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98c95598ac23f37918c67eec70c2ed205f8a4fe3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214552"
---
# <a name="wm_tablet_flick-message"></a><span data-ttu-id="31d65-104">WM- \_ Tablet \_ Flick-Nachricht</span><span class="sxs-lookup"><span data-stu-id="31d65-104">WM\_TABLET\_FLICK message</span></span>

<span data-ttu-id="31d65-105">Wird gesendet, wenn ein Benutzer einen Stift Flick ausführt.</span><span class="sxs-lookup"><span data-stu-id="31d65-105">Sent when a user performs a pen flick.</span></span> <span data-ttu-id="31d65-106">Ein Fenster empfängt diese Meldung über seine [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="31d65-106">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_TABLET_DEFBASE  0x02C0
#define WM_TABLET_FLICK    (WM_TABLET_DEFBASE + 11)     
```



## <a name="parameters"></a><span data-ttu-id="31d65-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="31d65-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31d65-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="31d65-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="31d65-109">Eine [**Flick \_ Datenstruktur**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_data) , die Informationen über den aufgetretenen Stift Flick enthält.</span><span class="sxs-lookup"><span data-stu-id="31d65-109">A [**FLICK\_DATA Structure**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_data) that contains information about the pen flick that occurred.</span></span>

</dd> <dt>

<span data-ttu-id="31d65-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="31d65-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="31d65-111">Die [**flimapointstruktur \_**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_point) , die angibt, wo der Stift flicke aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="31d65-111">The [**FLICK\_POINT Structure**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_point) that specifies where the pen flick occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="31d65-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="31d65-112">Remarks</span></span>

<span data-ttu-id="31d65-113">Bei einem Stift-Flick handelt es sich um eine unidirektionale Stift Bewegung, bei der der Benutzer sich bei einer schnellen, geraden Bewegung an den Digitalisierer wenden muss.</span><span class="sxs-lookup"><span data-stu-id="31d65-113">A pen flick is a unidirectional pen gesture that requires the user to contact the digitizer in a quick, straight flicking motion.</span></span> <span data-ttu-id="31d65-114">Ein Flick ist durch hohe Geschwindigkeit und einen hohen Grad an Genauigkeit gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="31d65-114">A flick is characterized by high speed and a high degree of straightness.</span></span> <span data-ttu-id="31d65-115">Ein Flick wird durch seine Richtung identifiziert.</span><span class="sxs-lookup"><span data-stu-id="31d65-115">A flick is identified by its direction.</span></span> <span data-ttu-id="31d65-116">Flicks können in acht Richtungen erstellt werden, die den Haupt-und sekundären Kompass Richtungen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="31d65-116">Flicks can be made in eight directions corresponding to the cardinal and secondary compass directions.</span></span>

<span data-ttu-id="31d65-117">Wenn ein Stift-Flick auftritt, benachrichtigt Windows zunächst eine Anwendung, indem er eine **WM- \_ Tablet- \_** Pass-Nachricht sendet, die ein Fenster über seine [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion empfängt.</span><span class="sxs-lookup"><span data-stu-id="31d65-117">When a pen flick occurs, Windows first notifies an application by sending a **WM\_TABLET\_FLICK** message, which a window receives through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <span data-ttu-id="31d65-118">Gibt die in [Flicks-Konstanten](flicks-constants.md)beschriebene **Maske-Maske- \_ \_ \_ Maske** zurück, die angibt, dass die Anwendung auf die **WM- \_ Tablet \_** -Nachricht geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="31d65-118">Return the **FLICK\_WM\_HANDLED\_MASK** constant, described in [Flicks Constants](flicks-constants.md), to indicate that the application responded to the **WM\_TABLET\_FLICK** message.</span></span> <span data-ttu-id="31d65-119">Wenn die Anwendung keine " **Flick- \_ WM \_ behandelte \_ Maske**" zurückgibt, führt Windows die in der schnelle Stift Bewegungen-Systemsteuerung angegebene Standardaktion aus, indem eine nach Verfolgungs Benachrichtigung gesendet wird, wie z. b. [**WM \_ appcommand**](../inputdev/wm-appcommand.md), [**WM \_ VScroll**](../controls/wm-vscroll.md)oder [**WM \_ KeyDown**](../inputdev/wm-keydown.md), je nachdem, welche Aktion dem Stift Flick zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="31d65-119">If the application does not return **FLICK\_WM\_HANDLED\_MASK**, Windows performs the default action specified in the flicks control panel by sending a follow-up notification, such as [**WM\_APPCOMMAND**](../inputdev/wm-appcommand.md), [**WM\_VSCROLL**](../controls/wm-vscroll.md), or [**WM\_KEYDOWN**](../inputdev/wm-keydown.md), depending on which action is associated with the pen flick.</span></span>

<span data-ttu-id="31d65-120">Gehen Sie bei der Behandlung der **WM- \_ Tablet \_ Flick** -Nachricht vorsichtig vor.</span><span class="sxs-lookup"><span data-stu-id="31d65-120">Use caution when handling the **WM\_TABLET\_FLICK** message.</span></span> <span data-ttu-id="31d65-121">**WM \_ Tablet \_ Flick** wird über die [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) -Funktion übergeben.</span><span class="sxs-lookup"><span data-stu-id="31d65-121">**WM\_TABLET\_FLICK** is passed via the [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) function.</span></span> <span data-ttu-id="31d65-122">Wenn Sie Methoden für eine COM-Schnittstelle aufzurufen, muss sich dieses Objekt innerhalb desselben Prozesses befinden.</span><span class="sxs-lookup"><span data-stu-id="31d65-122">If you call methods on a COM interface, that object must be within the same process.</span></span> <span data-ttu-id="31d65-123">Andernfalls löst com eine Ausnahme aus.</span><span class="sxs-lookup"><span data-stu-id="31d65-123">If not, COM throws an exception.</span></span>

## <a name="requirements"></a><span data-ttu-id="31d65-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="31d65-124">Requirements</span></span>



| <span data-ttu-id="31d65-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="31d65-125">Requirement</span></span> | <span data-ttu-id="31d65-126">Wert</span><span class="sxs-lookup"><span data-stu-id="31d65-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="31d65-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="31d65-127">Minimum supported client</span></span><br/> | <span data-ttu-id="31d65-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="31d65-128">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="31d65-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="31d65-129">Minimum supported server</span></span><br/> | <span data-ttu-id="31d65-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="31d65-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="31d65-131">Header</span><span class="sxs-lookup"><span data-stu-id="31d65-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="31d65-132"><dt>Tpcshrd. h</dt></span><span class="sxs-lookup"><span data-stu-id="31d65-132"><dt>Tpcshrd.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31d65-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="31d65-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31d65-134">**Flick \_ Datenstruktur**</span><span class="sxs-lookup"><span data-stu-id="31d65-134">**flick\_data structure**</span></span>](/windows/desktop/api/tabflicks/ns-tabflicks-flick_data)
</dt> <dt>

[<span data-ttu-id="31d65-135">**WM- \_ Tablet \_ Flick-Nachricht**</span><span class="sxs-lookup"><span data-stu-id="31d65-135">**wm\_tablet\_flick message**</span></span>](wm-tablet-flick-message.md)
</dt> <dt>

[<span data-ttu-id="31d65-136">Gesten schnelle Stift Bewegungen</span><span class="sxs-lookup"><span data-stu-id="31d65-136">flicks gestures</span></span>](flicks-gestures.md)
</dt> <dt>

<span data-ttu-id="31d65-137">[reagieren auf Pen-schnelle Stift Bewegungen](/previous-versions/windows/desktop/ms703447(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="31d65-137">[responding to pen flicks](/previous-versions/windows/desktop/ms703447(v=vs.85))</span></span>
</dt> </dl>

 

 

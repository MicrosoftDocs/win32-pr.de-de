---
title: WM_RASDIALEVENT Meldung (RAS. h)
description: Das Betriebssystem sendet eine WM- \_ rasdialereignisnachricht an eine Fenster Prozedur, wenn während eines RAS-Verbindungsprozesses eine Änderung des Zustands Ereignisses auftritt.
ms.assetid: 4526da20-04e7-47b2-b576-8dc36c08b053
keywords:
- WM_RASDIALEVENT-Message-RAS
topic_type:
- apiref
api_name:
- WM_RASDIALEVENT
api_location:
- Ras.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 470fe3915c9f672c4663971159386e529ea60db4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339119"
---
# <a name="wm_rasdialevent-message"></a><span data-ttu-id="3d9f9-104">WM- \_ rasdialereignismeldung</span><span class="sxs-lookup"><span data-stu-id="3d9f9-104">WM\_RASDIALEVENT message</span></span>

<span data-ttu-id="3d9f9-105">Das Betriebssystem sendet eine **WM- \_ rasdialereignisnachricht** an eine Fenster Prozedur, wenn während eines RAS-Verbindungsprozesses eine Änderung des Zustands Ereignisses auftritt.</span><span class="sxs-lookup"><span data-stu-id="3d9f9-105">The operating system sends a **WM\_RASDIALEVENT** message to a window procedure when a change of state event occurs during a RAS connection process.</span></span> <span data-ttu-id="3d9f9-106">Dies ist der Fall, wenn ein Fenster angegeben wurde, das Benachrichtigungen über solche Ereignisse mithilfe des *Benachrichtigung* -Parameters von [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala)behandelt.</span><span class="sxs-lookup"><span data-stu-id="3d9f9-106">This happens when a window has been specified to handle notifications of such events by using the *notifier* parameter of [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala).</span></span>

<span data-ttu-id="3d9f9-107">Die beiden Nachrichten Parameter entsprechen den Parametern mit denselben Namen, die mit den Rückruf Funktionen von " [**rasdialfunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) " und " [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) " verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3d9f9-107">The two message parameters are equivalent to the parameters of the same names that are used with [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) and [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) callback functions.</span></span>


```C++
WM_RASDIALEVENT 
rasconnstate = (RASCONNSTATE) wParam; 
dwError = (DWORD) lParam;
            
```



## <a name="parameters"></a><span data-ttu-id="3d9f9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d9f9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d9f9-109">*rasrestate*</span><span class="sxs-lookup"><span data-stu-id="3d9f9-109">*rasconnstate*</span></span> 
</dt> <dd>

<span data-ttu-id="3d9f9-110">Der Wert von *wParam*.</span><span class="sxs-lookup"><span data-stu-id="3d9f9-110">Value of *wParam*.</span></span> <span data-ttu-id="3d9f9-111">Entspricht dem " *rasconfiguration State* "-Parameter der " [**rasdialfunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) "-und " [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) "-Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="3d9f9-111">Equivalent to the *rasconnstate* parameter of the [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) and [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) callback functions.</span></span> <span data-ttu-id="3d9f9-112">Gibt einen " [**rasnetwork State**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) "-Enumeratorwert an, der den Zustand angibt, in den der RAS-RAS-Verbindungsprozess eintritt.</span><span class="sxs-lookup"><span data-stu-id="3d9f9-112">Specifies a [**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) enumerator value that indicates the state the RasDial remote access connection process is about to enter.</span></span>

</dd> <dt>

<span data-ttu-id="3d9f9-113">*dwError*</span><span class="sxs-lookup"><span data-stu-id="3d9f9-113">*dwError*</span></span> 
</dt> <dd>

<span data-ttu-id="3d9f9-114">Der Wert von *LPARAM*.</span><span class="sxs-lookup"><span data-stu-id="3d9f9-114">Value of *lParam*.</span></span> <span data-ttu-id="3d9f9-115">Entspricht dem *dwError* -Parameter der " [**rasdialfunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) "-und " [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) "-Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="3d9f9-115">Equivalent to the *dwError* parameter of the [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) and [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) callback functions.</span></span> <span data-ttu-id="3d9f9-116">Ein Wert ungleich NULL gibt den Fehler an, der aufgetreten ist, oder 0 (null), wenn kein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="3d9f9-116">A nonzero value indicates the error that has occurred, or zero if no error has occurred.</span></span>

<span data-ttu-id="3d9f9-117">Der [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) sendet diese Nachricht mit *dwError* auf NULL festgelegt, wenn für den jeweiligen Verbindungsstatus ein Eintrag festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="3d9f9-117">[**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) sends this message with *dwError* set to zero upon entry to each connection state.</span></span> <span data-ttu-id="3d9f9-118">Wenn ein Fehler innerhalb eines Zustands auftritt, wird die Nachricht erneut für den Zustand gesendet, dieses Mal mit einem *dwError* -Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="3d9f9-118">If an error occurs within a state, the message is sent again for the state, this time with a nonzero *dwError* value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d9f9-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3d9f9-119">Return value</span></span>

<span data-ttu-id="3d9f9-120">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie " **true**" zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="3d9f9-120">If an application processes this message, it should return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d9f9-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3d9f9-121">Requirements</span></span>



| <span data-ttu-id="3d9f9-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3d9f9-122">Requirement</span></span> | <span data-ttu-id="3d9f9-123">Wert</span><span class="sxs-lookup"><span data-stu-id="3d9f9-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3d9f9-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3d9f9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3d9f9-125">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3d9f9-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3d9f9-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3d9f9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3d9f9-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3d9f9-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3d9f9-128">Header</span><span class="sxs-lookup"><span data-stu-id="3d9f9-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d9f9-129"><dt>RAS. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d9f9-129"><dt>Ras.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d9f9-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3d9f9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d9f9-131">Remote Zugriffs Dienst (RAS) (Übersicht)</span><span class="sxs-lookup"><span data-stu-id="3d9f9-131">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="3d9f9-132">Remote Zugriffs Dienst-Meldungen</span><span class="sxs-lookup"><span data-stu-id="3d9f9-132">Remote Access Service Messages</span></span>](remote-access-service-messages.md)
</dt> <dt>

[<span data-ttu-id="3d9f9-133">**Rasdial**</span><span class="sxs-lookup"><span data-stu-id="3d9f9-133">**RasDial**</span></span>](/windows/desktop/api/Ras/nf-ras-rasdiala)
</dt> <dt>

[<span data-ttu-id="3d9f9-134">**Rasdialfunc**</span><span class="sxs-lookup"><span data-stu-id="3d9f9-134">**RasDialFunc**</span></span>](/windows/desktop/api/Ras/nc-ras-rasdialfunc)
</dt> <dt>

[<span data-ttu-id="3d9f9-135">**RasDialFunc1**</span><span class="sxs-lookup"><span data-stu-id="3d9f9-135">**RasDialFunc1**</span></span>](/windows/desktop/api/Ras/nc-ras-rasdialfunc1)
</dt> <dt>

<span data-ttu-id="3d9f9-136">[**Rasrestate**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3d9f9-136">[**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85))</span></span>
</dt> </dl>

 


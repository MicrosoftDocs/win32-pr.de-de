---
description: Das Ereignis des benutzerdefinierten DBT- \_ Geräts identifiziert ein benutzerdefiniertes Ereignis.
ms.assetid: b42feda9-5fe7-4e54-aad9-28c61d2f29b6
title: DBT_USERDEFINED-Ereignis (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d57ed3ebb801da4ae1ed7a7964cb7aac4f411a35
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041431"
---
# <a name="dbt_userdefined-event"></a><span data-ttu-id="9d7e0-103">DBT \_ UserDefined-Ereignis</span><span class="sxs-lookup"><span data-stu-id="9d7e0-103">DBT\_USERDEFINED event</span></span>

<span data-ttu-id="9d7e0-104">Das Ereignis des benutzerdefinierten DBT- \_ Geräts identifiziert ein benutzerdefiniertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="9d7e0-104">The DBT\_USERDEFINED device event identifies a user-defined event.</span></span>

<span data-ttu-id="9d7e0-105">Um dieses Geräte Ereignis zu übertragen, müssen Sie die Funktion [**broadcastsystemmessage**](/windows/desktop/api/winuser/nf-winuser-broadcastsystemmessage) mit der [**WM \_ devicechange**](wm-devicechange.md) -Nachricht abrufen.</span><span class="sxs-lookup"><span data-stu-id="9d7e0-105">To broadcast this device event, call the [**BroadcastSystemMessage**](/windows/desktop/api/winuser/nf-winuser-broadcastsystemmessage) function with the [**WM\_DEVICECHANGE**](wm-devicechange.md) message.</span></span> <span data-ttu-id="9d7e0-106">Legen Sie *wParam* auf DBT \_ UserDefined fest, und legen Sie *LPARAM* wie im folgenden beschrieben fest.</span><span class="sxs-lookup"><span data-stu-id="9d7e0-106">Set *wParam* to DBT\_USERDEFINED and set *lParam* as described following.</span></span>


```C++
LRESULT CALLBACK WindowProc( HWND   hwnd,     // handle to window
                             UINT   uMsg,     // WM_DEVICECHANGE
                             WPARAM wParam,   // DBT_USERDEFINED
                             LPARAM lParam ); // event-specific data
```



## <a name="parameters"></a><span data-ttu-id="9d7e0-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d7e0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d7e0-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="9d7e0-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="9d7e0-109">Das Fensterhandle</span><span class="sxs-lookup"><span data-stu-id="9d7e0-109">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="9d7e0-110">*Umschlag*</span><span class="sxs-lookup"><span data-stu-id="9d7e0-110">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="9d7e0-111">Der [**WM- \_ devicechange**](wm-devicechange.md) -Nachrichten Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="9d7e0-111">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="9d7e0-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9d7e0-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9d7e0-113">Legen Sie auf DBT \_ UserDefined fest.</span><span class="sxs-lookup"><span data-stu-id="9d7e0-113">Set to DBT\_USERDEFINED.</span></span>

</dd> <dt>

<span data-ttu-id="9d7e0-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9d7e0-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9d7e0-115">Ein Zeiger auf eine [**\_ \_ \_ benutzerdefinierte dev Broadcast**](/windows/win32/api/dbt/ns-dbt-_dev_broadcast_userdefined) -Struktur, die die in Bearbeitung befindliche benutzerdefinierte Übertragung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="9d7e0-115">A pointer to a [**\_DEV\_BROADCAST\_USERDEFINED**](/windows/win32/api/dbt/ns-dbt-_dev_broadcast_userdefined) structure which describes the user-defined broadcast in progress.</span></span> <span data-ttu-id="9d7e0-116">Der Member **dbud \_ szName** enthält den Namen der benutzerdefinierten Meldung, gefolgt von benutzerdefinierten Daten.</span><span class="sxs-lookup"><span data-stu-id="9d7e0-116">The **dbud\_szName** member contains the name of the user-defined message, followed by any user-defined data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d7e0-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9d7e0-117">Return value</span></span>

<span data-ttu-id="9d7e0-118">Gibt **true** zurück.</span><span class="sxs-lookup"><span data-stu-id="9d7e0-118">Return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d7e0-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9d7e0-119">Requirements</span></span>



| <span data-ttu-id="9d7e0-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9d7e0-120">Requirement</span></span> | <span data-ttu-id="9d7e0-121">Wert</span><span class="sxs-lookup"><span data-stu-id="9d7e0-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9d7e0-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9d7e0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9d7e0-123">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9d7e0-123">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="9d7e0-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9d7e0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9d7e0-125">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9d7e0-125">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="9d7e0-126">Header</span><span class="sxs-lookup"><span data-stu-id="9d7e0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d7e0-127"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d7e0-127"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d7e0-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d7e0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d7e0-129">Geräte Ereignisse</span><span class="sxs-lookup"><span data-stu-id="9d7e0-129">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="9d7e0-130">Geräte Verwaltungs Ereignisse</span><span class="sxs-lookup"><span data-stu-id="9d7e0-130">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="9d7e0-131">**\_\_ \_ benutzerdefinierter Entwickler-Broadcast**</span><span class="sxs-lookup"><span data-stu-id="9d7e0-131">**\_DEV\_BROADCAST\_USERDEFINED**</span></span>](/windows/win32/api/dbt/ns-dbt-_dev_broadcast_userdefined)
</dt> <dt>

[<span data-ttu-id="9d7e0-132">**WM- \_ devicechange**</span><span class="sxs-lookup"><span data-stu-id="9d7e0-132">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> <dt>

[<span data-ttu-id="9d7e0-133">**Broadcastsystemmessage**</span><span class="sxs-lookup"><span data-stu-id="9d7e0-133">**BroadcastSystemMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-broadcastsystemmessage)
</dt> </dl>

 


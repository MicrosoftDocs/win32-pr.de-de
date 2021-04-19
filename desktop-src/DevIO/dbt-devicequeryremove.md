---
description: Das System überträgt das DBT \_ DeviceQueryRemove-Geräte Ereignis, um die Berechtigung zum Entfernen eines Geräts oder eines Mediums anzufordern.
ms.assetid: a0e9aa57-da0e-4e9c-99d0-5502040d2664
title: DBT_DEVICEQUERYREMOVE-Ereignis (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b8c9dbdee13318f9a664582fdba8f9e3f9bfc5f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345619"
---
# <a name="dbt_devicequeryremove-event"></a><span data-ttu-id="01909-103">DBT \_ DeviceQueryRemove-Ereignis</span><span class="sxs-lookup"><span data-stu-id="01909-103">DBT\_DEVICEQUERYREMOVE event</span></span>

<span data-ttu-id="01909-104">Das System überträgt das DBT \_ DeviceQueryRemove-Geräte Ereignis, um die Berechtigung zum Entfernen eines Geräts oder eines Mediums anzufordern.</span><span class="sxs-lookup"><span data-stu-id="01909-104">The system broadcasts the DBT\_DEVICEQUERYREMOVE device event to request permission to remove a device or piece of media.</span></span> <span data-ttu-id="01909-105">Diese Meldung ist die letzte Chance, dass Anwendungen und Treiber dieses Entfernen vorbereiten können.</span><span class="sxs-lookup"><span data-stu-id="01909-105">This message is the last chance for applications and drivers to prepare for this removal.</span></span> <span data-ttu-id="01909-106">Allerdings kann jede Anwendung diese Anforderung verweigern und den Vorgang abbrechen.</span><span class="sxs-lookup"><span data-stu-id="01909-106">However, any application can deny this request and cancel the operation.</span></span>

<span data-ttu-id="01909-107">Zum übertragen dieses Geräte Ereignisses verwendet das System die [**WM \_ devicechange**](wm-devicechange.md) -Nachricht, wobei *wParam* auf DBT \_ DeviceQueryRemove und *LPARAM* festgelegt ist, wie im folgenden beschrieben.</span><span class="sxs-lookup"><span data-stu-id="01909-107">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_DEVICEQUERYREMOVE and *lParam* set as described following.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="01909-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="01909-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01909-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="01909-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="01909-110">Das Fensterhandle</span><span class="sxs-lookup"><span data-stu-id="01909-110">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="01909-111">*Umschlag*</span><span class="sxs-lookup"><span data-stu-id="01909-111">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="01909-112">Der [**WM- \_ devicechange**](wm-devicechange.md) -Nachrichten Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="01909-112">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="01909-113">*wParam*</span><span class="sxs-lookup"><span data-stu-id="01909-113">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="01909-114">Legen Sie auf DBT \_ DeviceQueryRemove fest.</span><span class="sxs-lookup"><span data-stu-id="01909-114">Set to DBT\_DEVICEQUERYREMOVE.</span></span>

</dd> <dt>

<span data-ttu-id="01909-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="01909-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="01909-116">Ein Zeiger auf eine-Struktur, die das zu entfernende Gerät identifiziert.</span><span class="sxs-lookup"><span data-stu-id="01909-116">A pointer to a structure identifying the device to remove.</span></span> <span data-ttu-id="01909-117">Die Struktur besteht aus einem Ereignis unabhängigen Header, gefolgt von Ereignis abhängigen Membern, die das Gerät beschreiben.</span><span class="sxs-lookup"><span data-stu-id="01909-117">The structure consists of an event-independent header, followed by event-dependent members that describe the device.</span></span> <span data-ttu-id="01909-118">Um diese Struktur zu verwenden, behandeln Sie die Struktur als Entwicklungs [**\_ Broadcast- \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) -Struktur, und überprüfen Sie dann den zugehörigen **dbch \_ den DeviceType "** -Member, um den Gerätetyp zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="01909-118">To use this structure, treat the structure as a [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) structure, then check its **dbch\_devicetype** member to determine the device type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01909-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="01909-119">Return value</span></span>

<span data-ttu-id="01909-120">Geben Sie **true** zurück, um die Berechtigung zum Entfernen eines Geräts zu erteilen.</span><span class="sxs-lookup"><span data-stu-id="01909-120">Return **TRUE** to grant permission to remove a device.</span></span>

<span data-ttu-id="01909-121">Rückgabe der Broadcast \_ Abfrage \_ ablehnen, um die Berechtigung zum Entfernen eines Geräts abzulehnen.</span><span class="sxs-lookup"><span data-stu-id="01909-121">Return BROADCAST\_QUERY\_DENY to deny permission to remove a device.</span></span>

## <a name="remarks"></a><span data-ttu-id="01909-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="01909-122">Remarks</span></span>

<span data-ttu-id="01909-123">Sie müssen alle Handles für das Gerät schließen, andernfalls tritt beim Entfernen des Geräts ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="01909-123">You must close all handles to the device or the device removal will fail.</span></span>

## <a name="examples"></a><span data-ttu-id="01909-124">Beispiele</span><span class="sxs-lookup"><span data-stu-id="01909-124">Examples</span></span>

<span data-ttu-id="01909-125">Ein Beispiel finden Sie unter [Verarbeiten einer Anforderung zum Entfernen eines Geräts](processing-a-request-to-remove-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="01909-125">For an example, see [Processing a Request to Remove a Device](processing-a-request-to-remove-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="01909-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="01909-126">Requirements</span></span>



| <span data-ttu-id="01909-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="01909-127">Requirement</span></span> | <span data-ttu-id="01909-128">Wert</span><span class="sxs-lookup"><span data-stu-id="01909-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="01909-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="01909-129">Minimum supported client</span></span><br/> | <span data-ttu-id="01909-130">Windows XP</span><span class="sxs-lookup"><span data-stu-id="01909-130">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="01909-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="01909-131">Minimum supported server</span></span><br/> | <span data-ttu-id="01909-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="01909-132">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="01909-133">Header</span><span class="sxs-lookup"><span data-stu-id="01909-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="01909-134"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="01909-134"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01909-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="01909-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01909-136">Geräte Ereignisse</span><span class="sxs-lookup"><span data-stu-id="01909-136">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="01909-137">Geräte Verwaltungs Ereignisse</span><span class="sxs-lookup"><span data-stu-id="01909-137">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="01909-138">**Entwickler- \_ Broadcast \_ HDR**</span><span class="sxs-lookup"><span data-stu-id="01909-138">**DEV\_BROADCAST\_HDR**</span></span>](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[<span data-ttu-id="01909-139">**WM- \_ devicechange**</span><span class="sxs-lookup"><span data-stu-id="01909-139">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 





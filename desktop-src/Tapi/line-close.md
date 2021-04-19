---
description: Die TAPI-Zeilen \_ Schließen-Nachricht wird gesendet, wenn das angegebene Zeilen Gerät zwangsweise geschlossen wurde. Das Zeilen Geräte handle oder alle Aufruf Handles für Aufrufe in der Zeile sind nicht mehr gültig, nachdem diese Nachricht gesendet wurde.
ms.assetid: f254e331-d574-4fa7-8447-6e4535d3d773
title: LINE_CLOSE Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7f4fde53d1017b2dcd9fe4ea833803055d9f2dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369673"
---
# <a name="line_close-message"></a><span data-ttu-id="51717-104">Zeilen Schluss \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="51717-104">LINE\_CLOSE message</span></span>

<span data-ttu-id="51717-105">Die TAPI- **Zeilen \_ Schließen** -Nachricht wird gesendet, wenn das angegebene Zeilen Gerät zwangsweise geschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="51717-105">The TAPI **LINE\_CLOSE** message is sent when the specified line device has been forcibly closed.</span></span> <span data-ttu-id="51717-106">Das Zeilen Geräte handle oder alle Aufruf Handles für Aufrufe in der Zeile sind nicht mehr gültig, nachdem diese Nachricht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="51717-106">The line device handle or any call handles for calls on the line are no longer valid once this message has been sent.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="51717-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="51717-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51717-108">*hdevice*</span><span class="sxs-lookup"><span data-stu-id="51717-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="51717-109">Ein Handle für das Zeilen Gerät, das geschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="51717-109">A handle to the line device that was closed.</span></span> <span data-ttu-id="51717-110">Dieses Handle ist nicht mehr gültig.</span><span class="sxs-lookup"><span data-stu-id="51717-110">This handle is no longer valid.</span></span>

</dd> <dt>

<span data-ttu-id="51717-111">*dwcallbackinstance*</span><span class="sxs-lookup"><span data-stu-id="51717-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="51717-112">Die beim Öffnen der Zeile angegebene Rückruf Instanz.</span><span class="sxs-lookup"><span data-stu-id="51717-112">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="51717-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="51717-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="51717-114">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="51717-114">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="51717-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="51717-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="51717-116">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="51717-116">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="51717-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="51717-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="51717-118">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="51717-118">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51717-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="51717-119">Return value</span></span>

<span data-ttu-id="51717-120">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="51717-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="51717-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="51717-121">Remarks</span></span>

<span data-ttu-id="51717-122">Die Meldung zum **\_ Schließen der Zeile** wird nur an jede Anwendung gesendet, nachdem der TAPI-Dienstanbieter (TSP) das Schließen einer geöffneten Zeile erzwungen hat.</span><span class="sxs-lookup"><span data-stu-id="51717-122">The **LINE\_CLOSE** message is sent to any application only after the TAPI service provider (TSP) has forcibly closed an open line.</span></span> <span data-ttu-id="51717-123">Gibt an, ob die Zeile sofort nach einer erzwungenen Schließung wieder geöffnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="51717-123">Whether or not the line can be reopened immediately after a forced close is device-specific.</span></span>

<span data-ttu-id="51717-124">Die Ursache kann eine bedeutende Zustandsänderung, ein Hardwarefehler, ein Verlust der Verbindung zu einem Server oder sogar potenziell verhindern, dass eine einzelne Anwendung ein Zeilen Gerät zu lange monopolisiert.</span><span class="sxs-lookup"><span data-stu-id="51717-124">The causing condition can be a significant change of state, a hardware error, a loss of connection to a server, or even potentially to prevent a single application from monopolizing a line device for too long.</span></span> <span data-ttu-id="51717-125">Ein liniengerät kann auch erzwungen werden, nachdem der Benutzer die Konfiguration dieser Zeile oder seines Treibers geändert hat.</span><span class="sxs-lookup"><span data-stu-id="51717-125">A line device can also be forcibly closed after the user has modified the configuration of that line or its driver.</span></span> <span data-ttu-id="51717-126">Wenn der Benutzer möchte, dass die Konfigurationsänderungen sofort wirksam werden (im Gegensatz zu nach dem nächsten Neustart des Systems), und Sie sich auf die aktuelle Ansicht des Geräts der Anwendung auswirken (z. b. eine Änderung der Gerätefunktionen), kann ein Dienstanbieter zwangsweise das Zeilen Gerät schließen.</span><span class="sxs-lookup"><span data-stu-id="51717-126">If the user wants the configuration changes to be effective immediately (as opposed to after the next system restart), and they affect the application's current view of the device (such as a change in device capabilities), then a service provider can forcibly close the line device.</span></span>

## <a name="requirements"></a><span data-ttu-id="51717-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="51717-127">Requirements</span></span>



| <span data-ttu-id="51717-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="51717-128">Requirement</span></span> | <span data-ttu-id="51717-129">Wert</span><span class="sxs-lookup"><span data-stu-id="51717-129">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="51717-130">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="51717-130">TAPI version</span></span><br/> | <span data-ttu-id="51717-131">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="51717-131">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="51717-132">Header</span><span class="sxs-lookup"><span data-stu-id="51717-132">Header</span></span><br/>       | <dl> <span data-ttu-id="51717-133"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="51717-133"><dt>Tapi.h</dt></span></span> </dl> |



 

 





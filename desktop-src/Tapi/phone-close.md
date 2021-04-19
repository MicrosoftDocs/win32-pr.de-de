---
description: Die TAPI-Telefon \_ Meldung "Schließen" wird gesendet, wenn ein geöffnetes Telefongerät im Rahmen der Ressourcenrückgewinnung zwangsweise geschlossen wurde. Das Geräte Handle ist nicht mehr gültig, nachdem diese Nachricht gesendet wurde.
ms.assetid: 84650abf-235e-4792-a67d-2f0f08b85a32
title: PHONE_CLOSE Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d9a7641b437a10098806fc7ad52aa64200ca015
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367079"
---
# <a name="phone_close-message"></a><span data-ttu-id="41047-104">\_Meldung zum Schließen des Telefons</span><span class="sxs-lookup"><span data-stu-id="41047-104">PHONE\_CLOSE message</span></span>

<span data-ttu-id="41047-105">Die TAPI-Telefon Meldung " **\_ Schließen** " wird gesendet, wenn ein geöffnetes Telefongerät im Rahmen der Ressourcenrückgewinnung zwangsweise geschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="41047-105">The TAPI **PHONE\_CLOSE** message is sent when an open phone device has been forcibly closed as part of resource reclamation.</span></span> <span data-ttu-id="41047-106">Das Geräte Handle ist nicht mehr gültig, nachdem diese Nachricht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="41047-106">The device handle is no longer valid once this message has been sent.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="41047-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="41047-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41047-108">*hphone*</span><span class="sxs-lookup"><span data-stu-id="41047-108">*hPhone*</span></span> 
</dt> <dd>

<span data-ttu-id="41047-109">Ein Handle für das geöffnete Telefongerät, das geschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="41047-109">A handle to the open phone device that was closed.</span></span> <span data-ttu-id="41047-110">Das Handle ist nicht mehr gültig, nachdem diese Nachricht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="41047-110">The handle is no longer valid after this message has been sent.</span></span>

</dd> <dt>

<span data-ttu-id="41047-111">*dwcallbackinstance*</span><span class="sxs-lookup"><span data-stu-id="41047-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="41047-112">Die Rückruf Instanz der Anwendung, die beim Öffnen des Telefon Geräts bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="41047-112">The application's callback instance that provided when opening the phone device.</span></span>

</dd> <dt>

<span data-ttu-id="41047-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="41047-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="41047-114">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="41047-114">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="41047-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="41047-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="41047-116">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="41047-116">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="41047-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="41047-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="41047-118">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="41047-118">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41047-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="41047-119">Return value</span></span>

<span data-ttu-id="41047-120">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="41047-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="41047-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="41047-121">Remarks</span></span>

<span data-ttu-id="41047-122">Die Meldung zum **\_ Schließen des Telefons** wird nur an eine Anwendung gesendet, nachdem ein geöffnetes Telefon zwangsweise geschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="41047-122">The **PHONE\_CLOSE** message is only sent to an application after an open phone has been forcibly closed.</span></span> <span data-ttu-id="41047-123">Dies kann durchgeführt werden, um zu verhindern, dass eine einzelne Anwendung das Telefongerät zu lange monopolisiert.</span><span class="sxs-lookup"><span data-stu-id="41047-123">This can be done to prevent a single application from monopolizing a phone device for too long.</span></span> <span data-ttu-id="41047-124">Gibt an, ob das Telefon sofort nach einer erzwungenen Schließung wieder geöffnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="41047-124">Whether the phone can be reopened immediately after a forced close is device specific.</span></span>

<span data-ttu-id="41047-125">Ein geöffnetes Telefongerät kann auch erzwungen werden, nachdem der Benutzer die Konfiguration dieses Telefons oder seines Treibers geändert hat.</span><span class="sxs-lookup"><span data-stu-id="41047-125">An open phone device can also be forcibly closed after the user has modified the configuration of that phone or its driver.</span></span> <span data-ttu-id="41047-126">Wenn der Benutzer möchte, dass die Konfigurationsänderungen sofort wirksam werden (im Gegensatz zu nach dem nächsten Neustart des Systems), und sich diese Änderungen auf die aktuelle Ansicht des Geräts (z. b. eine Änderung der Gerätefunktionen) auswirken, kann ein Dienstanbieter das Telefongerät schließen.</span><span class="sxs-lookup"><span data-stu-id="41047-126">If the user wants the configuration changes to be effective immediately (as opposed to after the next system restart), and these changes affect the application's current view of the device (such as a change in device capabilities), then a service provider can forcibly close the phone device.</span></span>

## <a name="requirements"></a><span data-ttu-id="41047-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="41047-127">Requirements</span></span>



| <span data-ttu-id="41047-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="41047-128">Requirement</span></span> | <span data-ttu-id="41047-129">Wert</span><span class="sxs-lookup"><span data-stu-id="41047-129">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="41047-130">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="41047-130">TAPI version</span></span><br/> | <span data-ttu-id="41047-131">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="41047-131">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="41047-132">Header</span><span class="sxs-lookup"><span data-stu-id="41047-132">Header</span></span><br/>       | <dl> <span data-ttu-id="41047-133"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="41047-133"><dt>Tapi.h</dt></span></span> </dl> |



 

 





---
description: Die Meldung für die TAPI-Telefon \_ Schaltfläche wird gesendet, um der Anwendung mitzuteilen, dass die Schaltfläche zum Drücken der Schaltfläche aktiviert ist, wenn auf dem lokalen Telefon ein Schaltflächen-
ms.assetid: fe47eed7-89d1-488b-b945-9e1aedc1f63c
title: PHONE_BUTTON Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2da810630a937f8415e070373f359dca06a694e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368478"
---
# <a name="phone_button-message"></a><span data-ttu-id="5c931-103">Telefon \_ Schaltfläche Meldung</span><span class="sxs-lookup"><span data-stu-id="5c931-103">PHONE\_BUTTON message</span></span>

<span data-ttu-id="5c931-104">Die Meldung für die TAPI- **Telefon \_ Schaltfläche** wird gesendet, um der Anwendung mitzuteilen, dass die Schaltfläche zum Drücken der Schaltfläche aktiviert ist, wenn auf dem lokalen Telefon ein Schaltflächen-</span><span class="sxs-lookup"><span data-stu-id="5c931-104">The TAPI **PHONE\_BUTTON** message is sent to notify the application that button press monitoring is enabled if it has detected a button press on the local phone.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="5c931-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c931-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c931-106">*hphone*</span><span class="sxs-lookup"><span data-stu-id="5c931-106">*hPhone*</span></span> 
</dt> <dd>

<span data-ttu-id="5c931-107">Ein Handle für das Telefongerät.</span><span class="sxs-lookup"><span data-stu-id="5c931-107">A handle to the phone device.</span></span>

</dd> <dt>

<span data-ttu-id="5c931-108">*dwcallbackinstance*</span><span class="sxs-lookup"><span data-stu-id="5c931-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="5c931-109">Die Rückruf Instanz der Anwendung, die beim Öffnen des Telefon Geräts bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="5c931-109">The application's callback instance provided when opening the phone device.</span></span>

</dd> <dt>

<span data-ttu-id="5c931-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="5c931-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="5c931-111">Der Schaltflächen-/Lamp-Bezeichner der Schaltfläche, die gedrückt wurde.</span><span class="sxs-lookup"><span data-stu-id="5c931-111">The button/lamp identifier of the button that was pressed.</span></span> <span data-ttu-id="5c931-112">Beachten Sie, dass die Schaltflächen Bezeichner 0 (null) bis 11 immer die Keypad-Schaltflächen sind, wobei "0" den Schaltflächen Bezeichner 0 (null), "1" als Schaltflächen Bezeichner 1 (usw. bis Schaltflächen Bezeichner 9) und "" als Schaltflächen Bezeichner \* \# 11 hat.</span><span class="sxs-lookup"><span data-stu-id="5c931-112">Note that button identifiers zero through 11 are always the KEYPAD buttons, with '0' being button identifier zero, '1' being button identifier 1 (and so on through button identifier 9), and with '\*' being button identifier 10, and '\#' being button identifier 11.</span></span> <span data-ttu-id="5c931-113">Weitere Informationen zu einem Schaltflächen Bezeichner sind mit [**phonegetdevcaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) und [**phonegetbuttoninfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5c931-113">Additional information about a button identifier is available with [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) and [**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo).</span></span>

</dd> <dt>

<span data-ttu-id="5c931-114">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="5c931-114">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="5c931-115">Der Schaltflächen Modus der Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="5c931-115">The button mode of the button.</span></span> <span data-ttu-id="5c931-116">Dieser Parameter verwendet eine der [**phonebuttonmode- \_ Konstanten**](phonebuttonmode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="5c931-116">This parameter uses one of the [**PHONEBUTTONMODE\_ constants**](phonebuttonmode--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c931-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="5c931-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="5c931-118">Gibt an, ob es sich um ein Button-down-Ereignis oder ein Schaltflächen-up-Ereignis handelt.</span><span class="sxs-lookup"><span data-stu-id="5c931-118">Specifies whether this is a button-down event or a button-up event.</span></span> <span data-ttu-id="5c931-119">Dieser Parameter verwendet eine der [**phonebuttonstate- \_ Konstanten**](phonebuttonstate--constants.md).</span><span class="sxs-lookup"><span data-stu-id="5c931-119">This parameter uses one of the [**PHONEBUTTONSTATE\_ constants**](phonebuttonstate--constants.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c931-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5c931-120">Return value</span></span>

<span data-ttu-id="5c931-121">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="5c931-121">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c931-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5c931-122">Remarks</span></span>

<span data-ttu-id="5c931-123">Wenn sich der Zustand einer Schaltfläche ändert, wird eine **Telefon \_ Schaltfläche** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5c931-123">A **PHONE\_BUTTON** message is sent whenever a button changes state.</span></span> <span data-ttu-id="5c931-124">Eine Anwendung ist garantiert, dass Sie für jedes Schaltflächen-nach-unten-Ereignis ein entsprechendes Schaltflächen-up-Ereignis sendet.</span><span class="sxs-lookup"><span data-stu-id="5c931-124">An application is guaranteed that for each button down event, it is eventually sent a corresponding button up event.</span></span> <span data-ttu-id="5c931-125">Ein Dienstanbieter, der nicht in der Lage ist, die tatsächliche Schaltfläche nach oben zu erkennen, ist erforderlich, um die Schaltfläche nach oben zu generieren, die für jede Schaltfläche gedrückt ist.</span><span class="sxs-lookup"><span data-stu-id="5c931-125">A service provider that is incapable of detecting the actual button up is required to generate the button up message shortly after the button down message for each button press.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c931-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5c931-126">Requirements</span></span>



| <span data-ttu-id="5c931-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5c931-127">Requirement</span></span> | <span data-ttu-id="5c931-128">Wert</span><span class="sxs-lookup"><span data-stu-id="5c931-128">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5c931-129">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="5c931-129">TAPI version</span></span><br/> | <span data-ttu-id="5c931-130">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="5c931-130">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="5c931-131">Header</span><span class="sxs-lookup"><span data-stu-id="5c931-131">Header</span></span><br/>       | <dl> <span data-ttu-id="5c931-132"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c931-132"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c931-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5c931-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c931-134">**phonegetbuttoninfo**</span><span class="sxs-lookup"><span data-stu-id="5c931-134">**phoneGetButtonInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo)
</dt> <dt>

[<span data-ttu-id="5c931-135">**phonegetdevcaps**</span><span class="sxs-lookup"><span data-stu-id="5c931-135">**phoneGetDevCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)
</dt> </dl>

 

 





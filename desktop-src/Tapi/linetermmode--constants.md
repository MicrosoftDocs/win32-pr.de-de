---
description: Die \_ Bit-Flag-Konstanten von linetermmode beschreiben verschiedene Arten von Ereignissen in einer Telefonleitung, die an ein Terminal Gerät weitergeleitet werden können.
ms.assetid: 60af1687-8958-4918-be21-a13780c60974
title: LINETERMMODE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e689e2e4e432d6cf804e64babd462e749e7e9e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373716"
---
# <a name="linetermmode_-constants"></a><span data-ttu-id="739d6-103">Linetermmode- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="739d6-103">LINETERMMODE\_ Constants</span></span>

<span data-ttu-id="739d6-104">Die Bit-Flag-Konstanten von **linetermmode \_** beschreiben verschiedene Arten von Ereignissen in einer Telefonleitung, die an ein Terminal Gerät weitergeleitet werden können.</span><span class="sxs-lookup"><span data-stu-id="739d6-104">The **LINETERMMODE\_** bit-flag constants describe different types of events on a phone line that can be routed to a terminal device.</span></span>

<dl> <dt>

<span data-ttu-id="739d6-105"><span id="LINETERMMODE_BUTTONS"></span><span id="linetermmode_buttons"></span>**linetermmode- \_ Schaltflächen**</span><span class="sxs-lookup"><span data-stu-id="739d6-105"><span id="LINETERMMODE_BUTTONS"></span><span id="linetermmode_buttons"></span>**LINETERMMODE\_BUTTONS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="739d6-106">Dabei handelt es sich um Schaltflächen, die vom Terminal an die Zeile gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="739d6-106">These are button-press events sent from the terminal to the line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="739d6-107"><span id="LINETERMMODE_DISPLAY"></span><span id="linetermmode_display"></span>**linetermmode- \_ Anzeige**</span><span class="sxs-lookup"><span data-stu-id="739d6-107"><span id="LINETERMMODE_DISPLAY"></span><span id="linetermmode_display"></span>**LINETERMMODE\_DISPLAY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="739d6-108">Dies sind Anzeigeinformationen, die von der Zeile an das Terminal gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="739d6-108">This is display information sent from the line to the terminal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="739d6-109"><span id="LINETERMMODE_HOOKSWITCH"></span><span id="linetermmode_hookswitch"></span>**linetermmode ( \_ huokswitch)**</span><span class="sxs-lookup"><span data-stu-id="739d6-109"><span id="LINETERMMODE_HOOKSWITCH"></span><span id="linetermmode_hookswitch"></span>**LINETERMMODE\_HOOKSWITCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="739d6-110">Dabei handelt es sich um vom Terminal an die Zeile gesendete Ereignisse vom-Terminal.</span><span class="sxs-lookup"><span data-stu-id="739d6-110">These are hookswitch events sent from the terminal to the line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="739d6-111"><span id="LINETERMMODE_LAMPS"></span><span id="linetermmode_lamps"></span>**linetermmode- \_ Lampen**</span><span class="sxs-lookup"><span data-stu-id="739d6-111"><span id="LINETERMMODE_LAMPS"></span><span id="linetermmode_lamps"></span>**LINETERMMODE\_LAMPS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="739d6-112">Dies sind Lamp-Ereignisse, die von der Zeile an das Terminal gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="739d6-112">These are lamp events sent from the line to the terminal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="739d6-113"><span id="LINETERMMODE_MEDIABIDIRECT"></span><span id="linetermmode_mediabidirect"></span>**linetermmode \_ mediabidirect**</span><span class="sxs-lookup"><span data-stu-id="739d6-113"><span id="LINETERMMODE_MEDIABIDIRECT"></span><span id="linetermmode_mediabidirect"></span>**LINETERMMODE\_MEDIABIDIRECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="739d6-114">Dies ist der bidirektionale Mediendaten Strom, der einem-Befehl in der-Zeile und dem Terminal zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="739d6-114">This is the bidirectional media stream associated with a call on the line and the terminal.</span></span> <span data-ttu-id="739d6-115">Verwenden Sie diesen Wert, wenn das Routing beider unidirektionaler Kanäle des Medien Stroms eines Aufrufes nicht unabhängig voneinander gesteuert werden kann.</span><span class="sxs-lookup"><span data-stu-id="739d6-115">Use this value when the routing of both unidirectional channels of a call's media stream cannot be controlled independently.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="739d6-116"><span id="LINETERMMODE_MEDIAFROMLINE"></span><span id="linetermmode_mediafromline"></span>**linetermmode- \_ mediafromline**</span><span class="sxs-lookup"><span data-stu-id="739d6-116"><span id="LINETERMMODE_MEDIAFROMLINE"></span><span id="linetermmode_mediafromline"></span>**LINETERMMODE\_MEDIAFROMLINE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="739d6-117">Dies ist der unidirektionale Mediendaten Strom von der Zeile bis zum Terminal, das einem-Befehl in der Zeile zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="739d6-117">This is the unidirectional media stream from the line to the terminal associated with a call on the line.</span></span> <span data-ttu-id="739d6-118">Verwenden Sie diesen Wert, wenn das Routing beider unidirektionaler Kanäle des Medien Stroms eines Aufrufens unabhängig voneinander gesteuert werden kann.</span><span class="sxs-lookup"><span data-stu-id="739d6-118">Use this value when the routing of both unidirectional channels of a call's media stream can be controlled independently.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="739d6-119"><span id="LINETERMMODE_MEDIATOLINE"></span><span id="linetermmode_mediatoline"></span>**linetermmode- \_ mediatoline**</span><span class="sxs-lookup"><span data-stu-id="739d6-119"><span id="LINETERMMODE_MEDIATOLINE"></span><span id="linetermmode_mediatoline"></span>**LINETERMMODE\_MEDIATOLINE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="739d6-120">Dies ist der unidirektionale Mediendaten Strom vom Terminal zu der Zeile, die einem-Befehl in der Zeile zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="739d6-120">This is the unidirectional media stream from the terminal to the line associated with a call on the line.</span></span> <span data-ttu-id="739d6-121">Verwenden Sie diesen Wert, wenn das Routing beider unidirektionaler Kanäle des Medien Stroms eines Aufrufens unabhängig voneinander gesteuert werden kann.</span><span class="sxs-lookup"><span data-stu-id="739d6-121">Use this value when the routing of both unidirectional channels of a call's media stream can be controlled independently.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="739d6-122"><span id="LINETERMMODE_RINGER"></span><span id="linetermmode_ringer"></span>**linetermmode- \_ Ringer**</span><span class="sxs-lookup"><span data-stu-id="739d6-122"><span id="LINETERMMODE_RINGER"></span><span id="linetermmode_ringer"></span>**LINETERMMODE\_RINGER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="739d6-123">Dies sind die ruftsteuerinformationen, die vom Switch zum Terminal gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="739d6-123">This is ringer-control information sent from the switch to the terminal.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="739d6-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="739d6-124">Remarks</span></span>

<span data-ttu-id="739d6-125">Keine Erweiterbarkeit.</span><span class="sxs-lookup"><span data-stu-id="739d6-125">No extensibility.</span></span> <span data-ttu-id="739d6-126">Alle 32 Bits sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="739d6-126">All 32 bits are reserved.</span></span>

<span data-ttu-id="739d6-127">Diese Konstanten beschreiben die Klassen von Steuerungs-und Informationsdaten strömen, die direkt zwischen einem Linien Gerät und einem Terminal Gerät (z. b. einem Telefon Satz) weitergeleitet werden können.</span><span class="sxs-lookup"><span data-stu-id="739d6-127">These constants describe the classes of control and information streams that can be routed directly between a line device and a terminal device (such as a phone set).</span></span>

## <a name="requirements"></a><span data-ttu-id="739d6-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="739d6-128">Requirements</span></span>



| <span data-ttu-id="739d6-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="739d6-129">Requirement</span></span> | <span data-ttu-id="739d6-130">Wert</span><span class="sxs-lookup"><span data-stu-id="739d6-130">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="739d6-131">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="739d6-131">TAPI version</span></span><br/> | <span data-ttu-id="739d6-132">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="739d6-132">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="739d6-133">Header</span><span class="sxs-lookup"><span data-stu-id="739d6-133">Header</span></span><br/>       | <dl> <span data-ttu-id="739d6-134"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="739d6-134"><dt>Tapi.h</dt></span></span> </dl> |



 

 





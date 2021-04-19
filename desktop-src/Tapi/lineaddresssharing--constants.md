---
description: Die lineaddresssharing \_ -Bitflag-Konstanten beschreiben verschiedene Methoden, mit denen eine Adresse zwischen Zeilen gemeinsam genutzt werden kann.
ms.assetid: f37ba549-c8dc-4a7c-bfe6-8e5f733d9750
title: LINEADDRESSSHARING_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 785c7e924ffc958d3fe14b739bb2eb28dec322a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359387"
---
# <a name="lineaddresssharing_-constants"></a><span data-ttu-id="c6a58-103">Lineaddresssharing- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="c6a58-103">LINEADDRESSSHARING\_ Constants</span></span>

<span data-ttu-id="c6a58-104">Die **lineaddresssharing \_** -Bitflag-Konstanten beschreiben verschiedene Methoden, mit denen eine Adresse zwischen Zeilen gemeinsam genutzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="c6a58-104">The **LINEADDRESSSHARING\_** bit-flag constants describe various ways an address can be shared between lines.</span></span>

<dl> <dt>

<span data-ttu-id="c6a58-105"><span id="LINEADDRESSSHARING_PRIVATE"></span><span id="lineaddresssharing_private"></span>**lineaddresssharing \_ Privat**</span><span class="sxs-lookup"><span data-stu-id="c6a58-105"><span id="LINEADDRESSSHARING_PRIVATE"></span><span id="lineaddresssharing_private"></span>**LINEADDRESSSHARING\_PRIVATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c6a58-106">Die Adresse ist für die Zeile des Benutzers privat. Sie ist keiner anderen Station zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="c6a58-106">The address is private to the user's line; it is not assigned to any other station.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c6a58-107"><span id="LINEADDRESSSHARING_BRIDGEDEXCL"></span><span id="lineaddresssharing_bridgedexcl"></span>**lineaddresssharing \_ bridgedexcl**</span><span class="sxs-lookup"><span data-stu-id="c6a58-107"><span id="LINEADDRESSSHARING_BRIDGEDEXCL"></span><span id="lineaddresssharing_bridgedexcl"></span>**LINEADDRESSSHARING\_BRIDGEDEXCL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c6a58-108">Die Adresse wird an eine oder mehrere andere Stationen überbrückt.</span><span class="sxs-lookup"><span data-stu-id="c6a58-108">The address is bridged to one or more other stations.</span></span> <span data-ttu-id="c6a58-109">Die erste Zeile zum Aktivieren eines Aufrufs in der Zeile hat exklusiven Zugriff auf die Adresse und die Aufrufe, die möglicherweise vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="c6a58-109">The first line to activate a call on the line will have exclusive access to the address and calls that may exist on it.</span></span> <span data-ttu-id="c6a58-110">Andere Zeilen sind nicht in der Lage, die überbrückt Adresse zu verwenden, während Sie verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c6a58-110">Other lines will not be able to use the bridged address while it is in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c6a58-111"><span id="LINEADDRESSSHARING_BRIDGEDNEW"></span><span id="lineaddresssharing_bridgednew"></span>**lineaddresssharing \_ bridgednew**</span><span class="sxs-lookup"><span data-stu-id="c6a58-111"><span id="LINEADDRESSSHARING_BRIDGEDNEW"></span><span id="lineaddresssharing_bridgednew"></span>**LINEADDRESSSHARING\_BRIDGEDNEW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c6a58-112">Die Adresse wird mit einer oder mehreren anderen Stationen überbrückt.</span><span class="sxs-lookup"><span data-stu-id="c6a58-112">The address is bridged with one or more other stations.</span></span> <span data-ttu-id="c6a58-113">Die erste Zeile zum Aktivieren eines Aufrufes in der Zeile hat exklusiven Zugriff auf den entsprechenden-Befehl.</span><span class="sxs-lookup"><span data-stu-id="c6a58-113">The first line to activate a call on the line will have exclusive access to only the corresponding call.</span></span> <span data-ttu-id="c6a58-114">Andere Anwendungen, die die Adresse verwenden, führen zu neuen und separaten aufrufungen.</span><span class="sxs-lookup"><span data-stu-id="c6a58-114">Other applications that use the address will result in new and separate call appearances.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c6a58-115"><span id="LINEADDRESSSHARING_BRIDGEDSHARED"></span><span id="lineaddresssharing_bridgedshared"></span>**lineaddresssharing \_ bridgedshared**</span><span class="sxs-lookup"><span data-stu-id="c6a58-115"><span id="LINEADDRESSSHARING_BRIDGEDSHARED"></span><span id="lineaddresssharing_bridgedshared"></span>**LINEADDRESSSHARING\_BRIDGEDSHARED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c6a58-116">Die Adresse wird durch eine oder mehrere andere Zeilen überbrückt.</span><span class="sxs-lookup"><span data-stu-id="c6a58-116">The address is bridged with one or more other lines.</span></span> <span data-ttu-id="c6a58-117">Alle überbrückten Parteien können Aufrufe für die Adresse freigeben, die dann als Konferenz fungiert.</span><span class="sxs-lookup"><span data-stu-id="c6a58-117">All bridged parties can share in calls on the address, which then functions as a conference.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c6a58-118"><span id="LINEADDRESSSHARING_MONITORED"></span><span id="lineaddresssharing_monitored"></span>**überwachte lineaddresssharing \_**</span><span class="sxs-lookup"><span data-stu-id="c6a58-118"><span id="LINEADDRESSSHARING_MONITORED"></span><span id="lineaddresssharing_monitored"></span>**LINEADDRESSSHARING\_MONITORED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c6a58-119">Dabei handelt es sich um eine Adresse, deren Status im Leerlauf/ausgelastet für diese Zeile verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="c6a58-119">This is an address whose idle/busy status is made available to this line.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c6a58-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c6a58-120">Remarks</span></span>

<span data-ttu-id="c6a58-121">Keine Erweiterbarkeit.</span><span class="sxs-lookup"><span data-stu-id="c6a58-121">No extensibility.</span></span> <span data-ttu-id="c6a58-122">Alle 32 Bits sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="c6a58-122">All 32 bits are reserved.</span></span>

<span data-ttu-id="c6a58-123">Die Art und Weise, in der eine Adresse Zeilen übergreifend freigegeben wird, kann sich auf das Verhalten dieser Adresse auswirken.</span><span class="sxs-lookup"><span data-stu-id="c6a58-123">The way in which an address is shared across lines can affect the behavior of that address.</span></span> <span data-ttu-id="c6a58-124">[**Zeile \_ CallState**](line-callstate.md) -und [**line \_ addressstate**](line-addressstate.md) -Meldungen werden als Reaktion auf Aktivitäten durch die Bridging-Stationen an die Anwendung gesendet.</span><span class="sxs-lookup"><span data-stu-id="c6a58-124">[**LINE\_CALLSTATE**](line-callstate.md) and [**LINE\_ADDRESSSTATE**](line-addressstate.md) messages are sent to the application in response to activities by the bridging stations.</span></span> <span data-ttu-id="c6a58-125">In diesen Nachrichten kann eine Anwendung den Status der Adresse nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="c6a58-125">It is through these messages that an application can track the status of the address.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6a58-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c6a58-126">Requirements</span></span>



| <span data-ttu-id="c6a58-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c6a58-127">Requirement</span></span> | <span data-ttu-id="c6a58-128">Wert</span><span class="sxs-lookup"><span data-stu-id="c6a58-128">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="c6a58-129">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="c6a58-129">TAPI version</span></span><br/> | <span data-ttu-id="c6a58-130">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="c6a58-130">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="c6a58-131">Header</span><span class="sxs-lookup"><span data-stu-id="c6a58-131">Header</span></span><br/>       | <dl> <span data-ttu-id="c6a58-132"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6a58-132"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6a58-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c6a58-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6a58-134">**Zeile \_ addressstate**</span><span class="sxs-lookup"><span data-stu-id="c6a58-134">**LINE\_ADDRESSSTATE**</span></span>](line-addressstate.md)
</dt> <dt>

[<span data-ttu-id="c6a58-135">**\_liniencallstate**</span><span class="sxs-lookup"><span data-stu-id="c6a58-135">**LINE\_CALLSTATE**</span></span>](line-callstate.md)
</dt> </dl>

 

 





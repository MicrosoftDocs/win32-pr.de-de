---
description: Die \_ Bit-Flag-Konstanten von linedevstatusflags beschreiben eine Auflistung boolescher Zeilen-Gerätestatus Elemente.
ms.assetid: 5fa754d3-07b2-4b75-91ef-1bf961d9fef4
title: LINEDEVSTATUSFLAGS_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70745b1a84119af2305cadabd0a39ab5954e5b7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369563"
---
# <a name="linedevstatusflags_-constants"></a><span data-ttu-id="d2b56-103">Linedevstatus Flags- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="d2b56-103">LINEDEVSTATUSFLAGS\_ Constants</span></span>

<span data-ttu-id="d2b56-104">Die Bit-Flag-Konstanten von **linedevstatusflags \_** beschreiben eine Auflistung boolescher Zeilen-Gerätestatus Elemente.</span><span class="sxs-lookup"><span data-stu-id="d2b56-104">The **LINEDEVSTATUSFLAGS\_** bit-flag constants describe a collection of Boolean line device status items.</span></span>

<dl> <dt>

<span data-ttu-id="d2b56-105"><span id="LINEDEVSTATUSFLAGS_CONNECTED"></span><span id="linedevstatusflags_connected"></span>**verknüpfte linedevstatus \_ -Flags**</span><span class="sxs-lookup"><span data-stu-id="d2b56-105"><span id="LINEDEVSTATUSFLAGS_CONNECTED"></span><span id="linedevstatusflags_connected"></span>**LINEDEVSTATUSFLAGS\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d2b56-106">Gibt an, ob die Linie mit TAPI verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="d2b56-106">Specifies whether the line is connected to TAPI.</span></span> <span data-ttu-id="d2b56-107">**True** gibt an, dass die Linie verbunden ist und TAPI auf dem liniengerät betrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="d2b56-107">If **TRUE**, the line is connected and TAPI is able to operate on the line device.</span></span> <span data-ttu-id="d2b56-108">Wenn der Wert **false** ist, wird die Zeile getrennt, und die Anwendung kann das liniengerät nicht über TAPI steuern.</span><span class="sxs-lookup"><span data-stu-id="d2b56-108">If **FALSE**, the line is disconnected and the application is unable to control the line device through TAPI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d2b56-109"><span id="LINEDEVSTATUSFLAGS_INSERVICE"></span><span id="linedevstatusflags_inservice"></span>**linedevstatus Flags- \_ INService**</span><span class="sxs-lookup"><span data-stu-id="d2b56-109"><span id="LINEDEVSTATUSFLAGS_INSERVICE"></span><span id="linedevstatusflags_inservice"></span>**LINEDEVSTATUSFLAGS\_INSERVICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d2b56-110">Gibt an, ob die Zeile im Dienst ist.</span><span class="sxs-lookup"><span data-stu-id="d2b56-110">Indicates whether the line is in service.</span></span> <span data-ttu-id="d2b56-111">**True** gibt an, dass sich die Zeile im Dienst befindet. Wenn der Wert **false** ist, ist die Zeile nicht mehr Dienst.</span><span class="sxs-lookup"><span data-stu-id="d2b56-111">If **TRUE**, the line is in service; if **FALSE**, the line is out of service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d2b56-112"><span id="LINEDEVSTATUSFLAGS_LOCKED"></span><span id="linedevstatusflags_locked"></span>**linedevstatus-Flags \_ gesperrt**</span><span class="sxs-lookup"><span data-stu-id="d2b56-112"><span id="LINEDEVSTATUSFLAGS_LOCKED"></span><span id="linedevstatusflags_locked"></span>**LINEDEVSTATUSFLAGS\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d2b56-113">Gibt an, ob die Zeile gesperrt oder entsperrt ist.</span><span class="sxs-lookup"><span data-stu-id="d2b56-113">Indicates whether the line is locked or unlocked.</span></span> <span data-ttu-id="d2b56-114">Dieses Bit wird am häufigsten bei Linien Geräten verwendet, die Mobiltelefonen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d2b56-114">This bit is most often used with line devices associated with cellular phones.</span></span> <span data-ttu-id="d2b56-115">Viele Mobiltelefone verfügen über einen Sicherheitsmechanismus, der die Eingabe eines Kennworts erfordert, damit das Telefonanrufe platzieren kann.</span><span class="sxs-lookup"><span data-stu-id="d2b56-115">Many cellular phones have a security mechanism that requires the entry of a password to enable the phone to place calls.</span></span> <span data-ttu-id="d2b56-116">Dieses Bit kann verwendet werden, um Anwendungen mitzuteilen, dass das Telefon gesperrt ist, und kann keine Anrufe platzieren, bis das Kennwort auf der Benutzeroberfläche des Telefons eingegeben wird, damit die Anwendung dem Benutzer eine entsprechende Warnung präsentieren kann.</span><span class="sxs-lookup"><span data-stu-id="d2b56-116">This bit can be used to indicate to applications that the phone is locked and cannot place calls until the password is entered on the user interface of the phone so that the application can present an appropriate alert to the user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d2b56-117"><span id="LINEDEVSTATUSFLAGS_MSGWAIT"></span><span id="linedevstatusflags_msgwait"></span>**linedevstatus Flags \_ msgwait**</span><span class="sxs-lookup"><span data-stu-id="d2b56-117"><span id="LINEDEVSTATUSFLAGS_MSGWAIT"></span><span id="linedevstatusflags_msgwait"></span>**LINEDEVSTATUSFLAGS\_MSGWAIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d2b56-118">Gibt an, ob die Zeile eine Nachricht wartet.</span><span class="sxs-lookup"><span data-stu-id="d2b56-118">Indicates whether the line has a message waiting.</span></span> <span data-ttu-id="d2b56-119">**True** gibt an, dass eine Nachricht wartet. **false** gibt an, dass keine Nachricht wartet.</span><span class="sxs-lookup"><span data-stu-id="d2b56-119">If **TRUE**, a message is waiting; if **FALSE**, no message is waiting.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d2b56-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d2b56-120">Remarks</span></span>

<span data-ttu-id="d2b56-121">Keine Erweiterbarkeit.</span><span class="sxs-lookup"><span data-stu-id="d2b56-121">No extensibility.</span></span> <span data-ttu-id="d2b56-122">Alle 32 Bits sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="d2b56-122">All 32 bits are reserved.</span></span>

<span data-ttu-id="d2b56-123">Linedevstatusflags- \_ Konstanten werden innerhalb des **dwdevstatusflags** -Members der [**linedevstatus**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) -Datenstruktur verwendet.</span><span class="sxs-lookup"><span data-stu-id="d2b56-123">LINEDEVSTATUSFLAGS\_ constants are used within the **dwDevStatusFlags** member of the [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) data structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2b56-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d2b56-124">Requirements</span></span>



| <span data-ttu-id="d2b56-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d2b56-125">Requirement</span></span> | <span data-ttu-id="d2b56-126">Wert</span><span class="sxs-lookup"><span data-stu-id="d2b56-126">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="d2b56-127">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="d2b56-127">TAPI version</span></span><br/> | <span data-ttu-id="d2b56-128">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="d2b56-128">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="d2b56-129">Header</span><span class="sxs-lookup"><span data-stu-id="d2b56-129">Header</span></span><br/>       | <dl> <span data-ttu-id="d2b56-130"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2b56-130"><dt>Tapi.h</dt></span></span> </dl> |



 

 





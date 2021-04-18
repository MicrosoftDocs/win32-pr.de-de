---
description: Die \_ Bit-Flag-Konstanten phoneprivilege beschreiben die verschiedenen Methoden, mit denen ein Telefongerät geöffnet werden kann.
ms.assetid: 1dc2fab9-b044-4ae3-8c16-fa450f9ef714
title: PHONEPRIVILEGE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6d04c074e03d6f0b7f7a6c58e4268e0bd5057a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365857"
---
# <a name="phoneprivilege_-constants"></a><span data-ttu-id="2a825-103">Phoneprivilege- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="2a825-103">PHONEPRIVILEGE\_ Constants</span></span>

<span data-ttu-id="2a825-104">Die Bit-Flag-Konstanten **phoneprivilege \_** beschreiben die verschiedenen Methoden, mit denen ein Telefongerät geöffnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="2a825-104">The **PHONEPRIVILEGE\_** bit-flag constants describe the various ways in which a phone device can be opened.</span></span>

<dl> <dt>

<span data-ttu-id="2a825-105"><span id="PHONEPRIVILEGE_MONITOR"></span><span id="phoneprivilege_monitor"></span>**phoneprivilege- \_ Monitor**</span><span class="sxs-lookup"><span data-stu-id="2a825-105"><span id="PHONEPRIVILEGE_MONITOR"></span><span id="phoneprivilege_monitor"></span>**PHONEPRIVILEGE\_MONITOR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2a825-106">Eine Anwendung, die ein Telefongerät mit der Berechtigung überwachen öffnet, wird über Ereignisse und Zustandsänderungen informiert, die auf dem Telefon stattfinden.</span><span class="sxs-lookup"><span data-stu-id="2a825-106">An application that opens a phone device with the monitor privilege is informed about events and state changes occurring on the phone.</span></span> <span data-ttu-id="2a825-107">Die Anwendung kann keine Vorgänge auf dem Telefongerät aufrufen, die den Zustand ändern, sodass nur Status Vorgänge aufgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="2a825-107">The application cannot invoke any operations on the phone device that would change its state, so only status operations can be invoked.</span></span> <span data-ttu-id="2a825-108">Mehrere Anwendungen können ein Telefongerät zu einem beliebigen Zeitpunkt überwachen.</span><span class="sxs-lookup"><span data-stu-id="2a825-108">Multiple applications can monitor a phone device at any given time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2a825-109"><span id="PHONEPRIVILEGE_OWNER"></span><span id="phoneprivilege_owner"></span>**phoneprivilege- \_ Besitzer**</span><span class="sxs-lookup"><span data-stu-id="2a825-109"><span id="PHONEPRIVILEGE_OWNER"></span><span id="phoneprivilege_owner"></span>**PHONEPRIVILEGE\_OWNER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2a825-110">Eine Anwendung, die ein Telefongerät mit der Berechtigung "Besitzer" öffnet, kann den Status der Lampen, ruftys, Anzeige-, huokswitch-und Datenblöcke des Telefons ändern.</span><span class="sxs-lookup"><span data-stu-id="2a825-110">An application that opens a phone device with the owner privilege is allowed to change the state of the lamps, ringer, display, hookswitch, and data blocks of the phone.</span></span> <span data-ttu-id="2a825-111">Wenn Sie ein Telefongerät im Besitzer Modus öffnen, wird auch die Überwachung des Telefon Geräts ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="2a825-111">Opening a phone device in owner mode also provides monitoring of the phone device.</span></span> <span data-ttu-id="2a825-112">Es ist nur eine Anwendung berechtigt, zu einem beliebigen Zeitpunkt als Besitzer eines Telefon Geräts zu fungieren.</span><span class="sxs-lookup"><span data-stu-id="2a825-112">Only one application is allowed to be the owner of a phone device at any given time.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2a825-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2a825-113">Remarks</span></span>

<span data-ttu-id="2a825-114">Keine Erweiterbarkeit.</span><span class="sxs-lookup"><span data-stu-id="2a825-114">No extensibility.</span></span> <span data-ttu-id="2a825-115">Alle 32 Bits sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="2a825-115">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a825-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2a825-116">Requirements</span></span>



| <span data-ttu-id="2a825-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2a825-117">Requirement</span></span> | <span data-ttu-id="2a825-118">Wert</span><span class="sxs-lookup"><span data-stu-id="2a825-118">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="2a825-119">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="2a825-119">TAPI version</span></span><br/> | <span data-ttu-id="2a825-120">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="2a825-120">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="2a825-121">Header</span><span class="sxs-lookup"><span data-stu-id="2a825-121">Header</span></span><br/>       | <dl> <span data-ttu-id="2a825-122"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a825-122"><dt>Tapi.h</dt></span></span> </dl> |



 

 





---
description: Die untc-Schnittstelle stellt die Methoden bereit, mit denen die NPP mit dem Netzwerk verbunden, Netzwerk Datenverkehr erfasst, Statistiken abgerufen und die Netzwerkverbindung vom Netzwerk getrennt wird.
ms.assetid: 9252a9ba-2c3e-40b9-b8de-84ef5d4831a7
title: Untc-Schnittstelle (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: c937d7d9233b1df063a7cf4a12e57e909145b8c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959384"
---
# <a name="irtc-interface"></a><span data-ttu-id="d4a7e-103">Untc-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="d4a7e-103">IRTC interface</span></span>

<span data-ttu-id="d4a7e-104">Die **untc** -Schnittstelle stellt die Methoden bereit, mit denen die NPP mit dem Netzwerk verbunden, Netzwerk Datenverkehr erfasst, Statistiken abgerufen und die Netzwerkverbindung vom Netzwerk getrennt wird.</span><span class="sxs-lookup"><span data-stu-id="d4a7e-104">The **IRTC** interface provides the methods used to connect the NPP to the network, capture network traffic, retrieve statistics, and disconnect the NPP from the network.</span></span> <span data-ttu-id="d4a7e-105">Bei " **untc** " wird eine Schnittstelle zu lokalen Einstiegspunkten abgerufen, die zum Einbinden der echt Zeiterfassung notwendig sind.</span><span class="sxs-lookup"><span data-stu-id="d4a7e-105">**IRTC** gets an interface to local-only entry points, which are necessary to engage in real-time capture.</span></span> <span data-ttu-id="d4a7e-106">Diese Schnittstelle enthält eine Methode, die einen Rückruf an den NPP übergibt.</span><span class="sxs-lookup"><span data-stu-id="d4a7e-106">This interface includes a method that hands off a callback to the NPP.</span></span>

## <a name="members"></a><span data-ttu-id="d4a7e-107">Member</span><span class="sxs-lookup"><span data-stu-id="d4a7e-107">Members</span></span>

<span data-ttu-id="d4a7e-108">Die Schnittstelle " **iritc** " erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d4a7e-108">The **IRTC** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d4a7e-109">**Außerdem gibt** es die folgenden Arten von Membern:</span><span class="sxs-lookup"><span data-stu-id="d4a7e-109">**IRTC** also has these types of members:</span></span>

-   [<span data-ttu-id="d4a7e-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="d4a7e-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d4a7e-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="d4a7e-111">Methods</span></span>

<span data-ttu-id="d4a7e-112">Die Schnittstelle " **iritc** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="d4a7e-112">The **IRTC** interface has these methods.</span></span>



| <span data-ttu-id="d4a7e-113">Methode</span><span class="sxs-lookup"><span data-stu-id="d4a7e-113">Method</span></span>                                                              | <span data-ttu-id="d4a7e-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d4a7e-114">Description</span></span>                                                                                                                                             |
|:--------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d4a7e-115">**Konfigurieren**</span><span class="sxs-lookup"><span data-stu-id="d4a7e-115">**Configure**</span></span>](irtc-configure.md)                                 | <span data-ttu-id="d4a7e-116">Legt den-, Muster Übereinstimmungs-und Puffergröße der Erfassung fest.</span><span class="sxs-lookup"><span data-stu-id="d4a7e-116">Sets the trigger, pattern match, and buffer size of the capture.</span></span><br/>                                                                             |
| [<span data-ttu-id="d4a7e-117">**Verbinden**</span><span class="sxs-lookup"><span data-stu-id="d4a7e-117">**Connect**</span></span>](irtc-connect.md)                                     | <span data-ttu-id="d4a7e-118">Verbindet den NPP mit dem Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="d4a7e-118">Connects the NPP to the network.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="d4a7e-119">**Trennen**</span><span class="sxs-lookup"><span data-stu-id="d4a7e-119">**Disconnect**</span></span>](irtc-disconnect.md)                               | <span data-ttu-id="d4a7e-120">Trennt die NPP vom Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="d4a7e-120">Disconnects the NPP from the network.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="d4a7e-121">**Getcontrolstate**</span><span class="sxs-lookup"><span data-stu-id="d4a7e-121">**GetControlState**</span></span>](irtc-getcontrolstate.md)                     | <span data-ttu-id="d4a7e-122">Ruft den Zustand der [*Erfassung*](c.md)ab, der angibt, ob die Erfassung ausgeführt wird oder angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="d4a7e-122">Retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span><br/>                      |
| [<span data-ttu-id="d4a7e-123">**Getconversation ationstatistics**</span><span class="sxs-lookup"><span data-stu-id="d4a7e-123">**GetConversationStatistics**</span></span>](irtc-getconversationstatistics.md) | <span data-ttu-id="d4a7e-124">Ruft [*Sitzungs*](s.md) -und [*Stations Informationen*](s.md) für die aktuelle Erfassung ab.</span><span class="sxs-lookup"><span data-stu-id="d4a7e-124">Retrieves [*session*](s.md) and [*station information*](s.md) for the current capture.</span></span><br/> |
| [<span data-ttu-id="d4a7e-125">**Gettotalstatistics**</span><span class="sxs-lookup"><span data-stu-id="d4a7e-125">**GetTotalStatistics**</span></span>](irtc-gettotalstatistics.md)               | <span data-ttu-id="d4a7e-126">Extrahiert Zeit, Puffer, Treiber und andere Netzwerk Statistiken aus der aktuell laufenden Erfassung.</span><span class="sxs-lookup"><span data-stu-id="d4a7e-126">Extracts time, buffer, driver, and other network statistics from the currently running capture.</span></span><br/>                                              |
| [<span data-ttu-id="d4a7e-127">**Anhalten**</span><span class="sxs-lookup"><span data-stu-id="d4a7e-127">**Pause**</span></span>](irtc-pause.md)                                         | <span data-ttu-id="d4a7e-128">Beendet vorübergehend die aktuelle Erfassung.</span><span class="sxs-lookup"><span data-stu-id="d4a7e-128">Temporarily stops the current capture.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="d4a7e-129">**Querystations**</span><span class="sxs-lookup"><span data-stu-id="d4a7e-129">**QueryStations**</span></span>](irtc-querystations.md)                         | <span data-ttu-id="d4a7e-130">Ruft eine Liste aller Computer in einem Subnetz ab, die Netzwerkmonitor zum Erfassen von Netzwerkdaten verwenden.</span><span class="sxs-lookup"><span data-stu-id="d4a7e-130">Retrieves a list of all computers on a subnet that are using Network Monitor to capture network data.</span></span><br/>                                        |
| [<span data-ttu-id="d4a7e-131">**QueryStatus**</span><span class="sxs-lookup"><span data-stu-id="d4a7e-131">**QueryStatus**</span></span>](irtc-querystatus.md)                             | <span data-ttu-id="d4a7e-132">Ruft den Status des NPP ab.</span><span class="sxs-lookup"><span data-stu-id="d4a7e-132">Retrieves the status of the NPP.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="d4a7e-133">**Fortsetzen**</span><span class="sxs-lookup"><span data-stu-id="d4a7e-133">**Resume**</span></span>](irtc-resume.md)                                       | <span data-ttu-id="d4a7e-134">Startet eine angehaltene Erfassung neu.</span><span class="sxs-lookup"><span data-stu-id="d4a7e-134">Restarts a paused capture.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="d4a7e-135">**Start**</span><span class="sxs-lookup"><span data-stu-id="d4a7e-135">**Start**</span></span>](irtc-start.md)                                         | <span data-ttu-id="d4a7e-136">Startet eine Aufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="d4a7e-136">Starts a capture.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="d4a7e-137">**Stop**</span><span class="sxs-lookup"><span data-stu-id="d4a7e-137">**Stop**</span></span>](irtc-stop.md)                                           | <span data-ttu-id="d4a7e-138">Hält die aktuelle Erfassung an.</span><span class="sxs-lookup"><span data-stu-id="d4a7e-138">Stops the current capture.</span></span><br/>                                                                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="d4a7e-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d4a7e-139">Requirements</span></span>



| <span data-ttu-id="d4a7e-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d4a7e-140">Requirement</span></span> | <span data-ttu-id="d4a7e-141">Wert</span><span class="sxs-lookup"><span data-stu-id="d4a7e-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4a7e-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d4a7e-142">Minimum supported client</span></span><br/> | <span data-ttu-id="d4a7e-143">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d4a7e-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="d4a7e-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d4a7e-144">Minimum supported server</span></span><br/> | <span data-ttu-id="d4a7e-145">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d4a7e-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="d4a7e-146">Header</span><span class="sxs-lookup"><span data-stu-id="d4a7e-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4a7e-147"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4a7e-147"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="d4a7e-148">DLL</span><span class="sxs-lookup"><span data-stu-id="d4a7e-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4a7e-149"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4a7e-149"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



 


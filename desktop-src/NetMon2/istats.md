---
description: Die iStats-Schnittstelle stellt die Methoden bereit, die Sie verwenden, um eine NPP mit dem Netzwerk zu verbinden, den Netzwerk Datenverkehr zu erfassen, Statistiken abzurufen und die NPP vom Netzwerk zu trennen. Diese Schnittstelle generiert Statistiken ohne Frames.
ms.assetid: 57cfcdd6-f16c-4a1c-b2ba-ce98f0576862
title: IStats-Schnittstelle (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: b64816589e3d4d0a2e3ace7be5c895e3d2cf22f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353130"
---
# <a name="istats-interface"></a><span data-ttu-id="0b1b5-104">IStats-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="0b1b5-104">IStats interface</span></span>

<span data-ttu-id="0b1b5-105">Die **iStats** -Schnittstelle stellt die Methoden bereit, die Sie verwenden, um eine NPP mit dem Netzwerk zu verbinden, den Netzwerk Datenverkehr zu erfassen, Statistiken abzurufen und die NPP vom Netzwerk zu trennen.</span><span class="sxs-lookup"><span data-stu-id="0b1b5-105">The **IStats** interface provides the methods you use to connect an NPP to the network, capture network traffic, retrieve statistics, and disconnect the NPP from the network.</span></span> <span data-ttu-id="0b1b5-106">Diese Schnittstelle generiert Statistiken ohne Frames.</span><span class="sxs-lookup"><span data-stu-id="0b1b5-106">This interface generates statistics without frames.</span></span>

## <a name="members"></a><span data-ttu-id="0b1b5-107">Member</span><span class="sxs-lookup"><span data-stu-id="0b1b5-107">Members</span></span>

<span data-ttu-id="0b1b5-108">Die **iStats** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="0b1b5-108">The **IStats** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="0b1b5-109">**IStats** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0b1b5-109">**IStats** also has these types of members:</span></span>

-   [<span data-ttu-id="0b1b5-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="0b1b5-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0b1b5-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="0b1b5-111">Methods</span></span>

<span data-ttu-id="0b1b5-112">Die **iStats** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="0b1b5-112">The **IStats** interface has these methods.</span></span>



| <span data-ttu-id="0b1b5-113">Methode</span><span class="sxs-lookup"><span data-stu-id="0b1b5-113">Method</span></span>                                                                | <span data-ttu-id="0b1b5-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0b1b5-114">Description</span></span>                                                                                                                                               |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0b1b5-115">**Konfigurieren**</span><span class="sxs-lookup"><span data-stu-id="0b1b5-115">**Configure**</span></span>](istats-configure.md)                                 | <span data-ttu-id="0b1b5-116">Konfiguriert den-, Muster Übereinstimmungs-und Puffergröße der Erfassungs Datei.</span><span class="sxs-lookup"><span data-stu-id="0b1b5-116">Configures the trigger, pattern match, and buffer size of the capture file.</span></span><br/>                                                                    |
| [<span data-ttu-id="0b1b5-117">**Verbinden**</span><span class="sxs-lookup"><span data-stu-id="0b1b5-117">**Connect**</span></span>](istats-connect.md)                                     | <span data-ttu-id="0b1b5-118">Verbindet den NPP mit dem Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="0b1b5-118">Connects the NPP to the network.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="0b1b5-119">**Trennen**</span><span class="sxs-lookup"><span data-stu-id="0b1b5-119">**Disconnect**</span></span>](istats-disconnect.md)                               | <span data-ttu-id="0b1b5-120">Trennt die NPP vom Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="0b1b5-120">Disconnects the NPP from the network.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="0b1b5-121">**Getcontrolstate**</span><span class="sxs-lookup"><span data-stu-id="0b1b5-121">**GetControlState**</span></span>](istats-getcontrolstate.md)                     | <span data-ttu-id="0b1b5-122">Ruft den Zustand der [*Erfassung*](c.md)ab, der angibt, ob die Erfassung ausgeführt wird oder angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="0b1b5-122">Retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span><br/>                        |
| [<span data-ttu-id="0b1b5-123">**Getconversation ationstatistics**</span><span class="sxs-lookup"><span data-stu-id="0b1b5-123">**GetConversationStatistics**</span></span>](istats-getconversationstatistics.md) | <span data-ttu-id="0b1b5-124">Ruft [*Sitzungs*](s.md) -und [*Stations Informationen*](s.md) zur aktuellen Erfassung ab.</span><span class="sxs-lookup"><span data-stu-id="0b1b5-124">Retrieves [*session*](s.md) and [*station information*](s.md) about the current capture.</span></span><br/> |
| [<span data-ttu-id="0b1b5-125">**Gettotalstatistics**</span><span class="sxs-lookup"><span data-stu-id="0b1b5-125">**GetTotalStatistics**</span></span>](istats-gettotalstatistics.md)               | <span data-ttu-id="0b1b5-126">Extrahiert Zeit, Puffer, Treiber und andere Netzwerk Statistiken aus der aktuell laufenden Erfassung.</span><span class="sxs-lookup"><span data-stu-id="0b1b5-126">Extracts time, buffer, driver, and other network statistics from the currently running capture.</span></span><br/>                                                |
| [<span data-ttu-id="0b1b5-127">**Anhalten**</span><span class="sxs-lookup"><span data-stu-id="0b1b5-127">**Pause**</span></span>](istats-pause.md)                                         | <span data-ttu-id="0b1b5-128">Beendet vorübergehend die aktuelle Erfassung.</span><span class="sxs-lookup"><span data-stu-id="0b1b5-128">Temporarily stops the current capture.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="0b1b5-129">**Querystations**</span><span class="sxs-lookup"><span data-stu-id="0b1b5-129">**QueryStations**</span></span>](istats-querystations.md)                         | <span data-ttu-id="0b1b5-130">Ruft eine Liste aller Computer ab, die Netzwerkmonitor zum Erfassen von Daten in einem Subnetz verwenden.</span><span class="sxs-lookup"><span data-stu-id="0b1b5-130">Retrieves a list of all computers that are using Network Monitor to capture data on a subnet.</span></span><br/>                                                  |
| [<span data-ttu-id="0b1b5-131">**QueryStatus**</span><span class="sxs-lookup"><span data-stu-id="0b1b5-131">**QueryStatus**</span></span>](istats-querystatus.md)                             | <span data-ttu-id="0b1b5-132">Ruft den Status des NPP ab.</span><span class="sxs-lookup"><span data-stu-id="0b1b5-132">Retrieves the status of the NPP.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="0b1b5-133">**Fortsetzen**</span><span class="sxs-lookup"><span data-stu-id="0b1b5-133">**Resume**</span></span>](istats-resume.md)                                       | <span data-ttu-id="0b1b5-134">Startet eine angehaltene Erfassung neu.</span><span class="sxs-lookup"><span data-stu-id="0b1b5-134">Restarts a paused capture.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="0b1b5-135">**Start**</span><span class="sxs-lookup"><span data-stu-id="0b1b5-135">**Start**</span></span>](istats-start.md)                                         | <span data-ttu-id="0b1b5-136">Startet die Erfassung.</span><span class="sxs-lookup"><span data-stu-id="0b1b5-136">Starts the capture.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="0b1b5-137">**Stop**</span><span class="sxs-lookup"><span data-stu-id="0b1b5-137">**Stop**</span></span>](istats-stop.md)                                           | <span data-ttu-id="0b1b5-138">Hält die aktuelle Erfassung an.</span><span class="sxs-lookup"><span data-stu-id="0b1b5-138">Stops the current capture.</span></span><br/>                                                                                                                     |



 

## <a name="requirements"></a><span data-ttu-id="0b1b5-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0b1b5-139">Requirements</span></span>



| <span data-ttu-id="0b1b5-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0b1b5-140">Requirement</span></span> | <span data-ttu-id="0b1b5-141">Wert</span><span class="sxs-lookup"><span data-stu-id="0b1b5-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b1b5-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0b1b5-142">Minimum supported client</span></span><br/> | <span data-ttu-id="0b1b5-143">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0b1b5-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="0b1b5-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0b1b5-144">Minimum supported server</span></span><br/> | <span data-ttu-id="0b1b5-145">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0b1b5-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="0b1b5-146">Header</span><span class="sxs-lookup"><span data-stu-id="0b1b5-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b1b5-147"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b1b5-147"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="0b1b5-148">DLL</span><span class="sxs-lookup"><span data-stu-id="0b1b5-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b1b5-149"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b1b5-149"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



 


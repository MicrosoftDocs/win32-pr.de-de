---
description: Die idelta Interface-Schnittstelle stellt die Methoden bereit, die zum Herstellen einer Verbindung mit dem Netzwerk, zum Erfassen von Netzwerk Datenverkehr für eine Aufzeichnungsdatei, zum Abrufen von Statistiken und zum Trennen der Verbindung mit dem Netzwerk
ms.assetid: ab275653-2377-4af6-a810-48515962c88c
title: Idelta aydc-Schnittstelle (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: cb87bc9f821e758b83a1bc3dee5d81a4b1b771d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372895"
---
# <a name="idelaydc-interface"></a><span data-ttu-id="640b5-103">Idelta aydc-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="640b5-103">IDelaydC interface</span></span>

<span data-ttu-id="640b5-104">Die **idelta** Interface-Schnittstelle stellt die Methoden bereit, die zum Herstellen einer Verbindung mit dem Netzwerk, zum Erfassen von Netzwerk Datenverkehr für eine Aufzeichnungsdatei, zum Abrufen von Statistiken und zum Trennen der Verbindung mit dem Netzwerk</span><span class="sxs-lookup"><span data-stu-id="640b5-104">The **IDelaydC** interface provides the methods used to connect to the network, capture network traffic to a capture file, retrieve statistics, and disconnect from the network.</span></span>

<span data-ttu-id="640b5-105">Diese Schnittstelle erfasst Frames aus dem Netzwerkdaten Strom und kopiert dann die Frames in eine Erfassungs Datei.</span><span class="sxs-lookup"><span data-stu-id="640b5-105">This interface captures frames from the network data stream and then copies the frames to a capture file.</span></span> <span data-ttu-id="640b5-106">Diese Schnittstelle wird von Netzwerkmonitor-und NPP-Anwendungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="640b5-106">This interface is used by Network Monitor and NPP applications.</span></span> <span data-ttu-id="640b5-107">Zum Empfangen der Netzwerkdaten muss die Ziel-NIC den gemischten-Modus unterstützen.</span><span class="sxs-lookup"><span data-stu-id="640b5-107">To receive the network data, the targeted NIC must support promiscuous mode.</span></span>

## <a name="members"></a><span data-ttu-id="640b5-108">Member</span><span class="sxs-lookup"><span data-stu-id="640b5-108">Members</span></span>

<span data-ttu-id="640b5-109">Die **idelta-DC** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="640b5-109">The **IDelaydC** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="640b5-110">**Idelta aydc** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="640b5-110">**IDelaydC** also has these types of members:</span></span>

-   [<span data-ttu-id="640b5-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="640b5-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="640b5-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="640b5-112">Methods</span></span>

<span data-ttu-id="640b5-113">Die **idelta-DC** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="640b5-113">The **IDelaydC** interface has these methods.</span></span>



| <span data-ttu-id="640b5-114">Methode</span><span class="sxs-lookup"><span data-stu-id="640b5-114">Method</span></span>                                                                  | <span data-ttu-id="640b5-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="640b5-115">Description</span></span>                                                                                                                                             |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="640b5-116">**Konfigurieren**</span><span class="sxs-lookup"><span data-stu-id="640b5-116">**Configure**</span></span>](idelaydc-configure.md)                                 | <span data-ttu-id="640b5-117">Übermittelt Konfigurationsinformationen, die für eine Erfassung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="640b5-117">Submits configuration information used for a capture.</span></span><br/>                                                                                        |
| [<span data-ttu-id="640b5-118">**Verbinden**</span><span class="sxs-lookup"><span data-stu-id="640b5-118">**Connect**</span></span>](idelaydc-connect.md)                                     | <span data-ttu-id="640b5-119">Verbindet den NPP mit dem Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="640b5-119">Connects the NPP to the network.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="640b5-120">**Trennen**</span><span class="sxs-lookup"><span data-stu-id="640b5-120">**Disconnect**</span></span>](idelaydc-disconnect.md)                               | <span data-ttu-id="640b5-121">Trennt die NPP vom Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="640b5-121">Disconnects the NPP from the network.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="640b5-122">**Getcontrolstate**</span><span class="sxs-lookup"><span data-stu-id="640b5-122">**GetControlState**</span></span>](idelaydc-getcontrolstate.md)                     | <span data-ttu-id="640b5-123">Ruft den Zustand der [*Erfassung*](c.md)ab, der angibt, ob die Erfassung ausgeführt wird oder angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="640b5-123">Retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span><br/>                      |
| [<span data-ttu-id="640b5-124">**Getconversation ationstatistics**</span><span class="sxs-lookup"><span data-stu-id="640b5-124">**GetConversationStatistics**</span></span>](idelaydc-getconversationstatistics.md) | <span data-ttu-id="640b5-125">Ruft [*Sitzungs*](s.md) -und [*Stations Informationen*](s.md) für die aktuelle Erfassung ab.</span><span class="sxs-lookup"><span data-stu-id="640b5-125">Retrieves [*session*](s.md) and [*station information*](s.md) for the current capture.</span></span><br/> |
| [<span data-ttu-id="640b5-126">**Gettotalstatistics**</span><span class="sxs-lookup"><span data-stu-id="640b5-126">**GetTotalStatistics**</span></span>](idelaydc-gettotalstatistics.md)               | <span data-ttu-id="640b5-127">Extrahiert Zeit, Puffer, Treiber und andere Netzwerk Statistiken aus der aktuell laufenden Erfassung.</span><span class="sxs-lookup"><span data-stu-id="640b5-127">Extracts time, buffer, driver, and other network statistics from the currently running capture.</span></span><br/>                                              |
| [<span data-ttu-id="640b5-128">**Anhalten**</span><span class="sxs-lookup"><span data-stu-id="640b5-128">**Pause**</span></span>](idelaydc-pause.md)                                         | <span data-ttu-id="640b5-129">Beendet vorübergehend die aktuelle Erfassung.</span><span class="sxs-lookup"><span data-stu-id="640b5-129">Temporarily stops the current capture.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="640b5-130">**Querystations**</span><span class="sxs-lookup"><span data-stu-id="640b5-130">**QueryStations**</span></span>](idelaydc-querystations.md)                         | <span data-ttu-id="640b5-131">Ruft eine Liste aller Computer ab, von denen Netzwerkmonitor zum Erfassen von Daten in einem Subnetz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="640b5-131">Retrieves a list of all computers that use Network Monitor to capture data on a subnet.</span></span><br/>                                                      |
| [<span data-ttu-id="640b5-132">**QueryStatus**</span><span class="sxs-lookup"><span data-stu-id="640b5-132">**QueryStatus**</span></span>](idelaydc-querystatus.md)                             | <span data-ttu-id="640b5-133">Ruft den Status des NPP ab.</span><span class="sxs-lookup"><span data-stu-id="640b5-133">Retrieves the status of the NPP.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="640b5-134">**Fortsetzen**</span><span class="sxs-lookup"><span data-stu-id="640b5-134">**Resume**</span></span>](idelaydc-resume.md)                                       | <span data-ttu-id="640b5-135">Setzt eine angehaltene Erfassung fort.</span><span class="sxs-lookup"><span data-stu-id="640b5-135">Resumes a paused capture.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="640b5-136">**Start**</span><span class="sxs-lookup"><span data-stu-id="640b5-136">**Start**</span></span>](idelaydc-start.md)                                         | <span data-ttu-id="640b5-137">Startet eine Erfassung und erstellt die [*Erfassungs Datei*](c.md).</span><span class="sxs-lookup"><span data-stu-id="640b5-137">Starts a capture and creates the [*capture file*](c.md).</span></span><br/>                                                           |
| [<span data-ttu-id="640b5-138">**Stop**</span><span class="sxs-lookup"><span data-stu-id="640b5-138">**Stop**</span></span>](idelaydc-stop.md)                                           | <span data-ttu-id="640b5-139">Beendet die aktuelle Erfassung und schließt die [*Erfassungs Datei*](c.md).</span><span class="sxs-lookup"><span data-stu-id="640b5-139">Stops the current capture and closes the [*capture file*](c.md).</span></span><br/>                                                   |



 

## <a name="requirements"></a><span data-ttu-id="640b5-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="640b5-140">Requirements</span></span>



| <span data-ttu-id="640b5-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="640b5-141">Requirement</span></span> | <span data-ttu-id="640b5-142">Wert</span><span class="sxs-lookup"><span data-stu-id="640b5-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="640b5-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="640b5-143">Minimum supported client</span></span><br/> | <span data-ttu-id="640b5-144">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="640b5-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="640b5-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="640b5-145">Minimum supported server</span></span><br/> | <span data-ttu-id="640b5-146">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="640b5-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="640b5-147">Header</span><span class="sxs-lookup"><span data-stu-id="640b5-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="640b5-148"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="640b5-148"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="640b5-149">DLL</span><span class="sxs-lookup"><span data-stu-id="640b5-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="640b5-150"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="640b5-150"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



 


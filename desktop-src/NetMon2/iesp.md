---
description: Die iESP-Schnittstelle stellt die Methoden bereit, die die NPP mit dem Netzwerk verbinden, den Netzwerk Datenverkehr für eine Erfassungs Datei erfassen, Statistiken abrufen und die Verbindung mit dem NPP vom Netzwerk trennen.
ms.assetid: e483f501-4928-4bfd-b212-e100f2b8f64f
title: IESP-Schnittstelle (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 1a7400bb9a16e6ece5f5f26fe95a0398a7d45e19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128917"
---
# <a name="iesp-interface"></a><span data-ttu-id="dcd07-103">IESP-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="dcd07-103">IESP interface</span></span>

<span data-ttu-id="dcd07-104">Die **iESP** -Schnittstelle stellt die Methoden bereit, die die NPP mit dem Netzwerk verbinden, den Netzwerk Datenverkehr für eine Erfassungs Datei erfassen, Statistiken abrufen und die Verbindung mit dem NPP vom Netzwerk trennen.</span><span class="sxs-lookup"><span data-stu-id="dcd07-104">The **IESP** interface provides the methods that connect the NPP to the network, capture network traffic to a capture file, retrieve statistics, and disconnect the NPP from the network.</span></span> <span data-ttu-id="dcd07-105">Diese Schnittstelle wird hauptsächlich verwendet, wenn Sie [*netzwerkkonversationsstatistiken*](c.md) in einem proprietären ESP-Dateiformat erfassen müssen.</span><span class="sxs-lookup"><span data-stu-id="dcd07-105">This interface is used primarily when you need to collect network [*conversation statistics*](c.md) in a proprietary ESP file format.</span></span>

## <a name="members"></a><span data-ttu-id="dcd07-106">Member</span><span class="sxs-lookup"><span data-stu-id="dcd07-106">Members</span></span>

<span data-ttu-id="dcd07-107">Die **iESP** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="dcd07-107">The **IESP** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="dcd07-108">**IESP** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="dcd07-108">**IESP** also has these types of members:</span></span>

-   [<span data-ttu-id="dcd07-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="dcd07-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="dcd07-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="dcd07-110">Methods</span></span>

<span data-ttu-id="dcd07-111">Die **iESP** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="dcd07-111">The **IESP** interface has these methods.</span></span>



| <span data-ttu-id="dcd07-112">Methode</span><span class="sxs-lookup"><span data-stu-id="dcd07-112">Method</span></span>                                          | <span data-ttu-id="dcd07-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dcd07-113">Description</span></span>                                                                                                                        |
|:------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dcd07-114">**Konfigurieren**</span><span class="sxs-lookup"><span data-stu-id="dcd07-114">**Configure**</span></span>](iesp-configure.md)             | <span data-ttu-id="dcd07-115">Übermittelt Konfigurationsinformationen für eine Erfassung</span><span class="sxs-lookup"><span data-stu-id="dcd07-115">Submits configuration information for a capture</span></span><br/>                                                                         |
| [<span data-ttu-id="dcd07-116">**Verbinden**</span><span class="sxs-lookup"><span data-stu-id="dcd07-116">**Connect**</span></span>](iesp-connect.md)                 | <span data-ttu-id="dcd07-117">Verbindet den NPP mit dem Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="dcd07-117">Connects the NPP to the network.</span></span><br/>                                                                                        |
| [<span data-ttu-id="dcd07-118">**Trennen**</span><span class="sxs-lookup"><span data-stu-id="dcd07-118">**Disconnect**</span></span>](iesp-disconnect.md)           | <span data-ttu-id="dcd07-119">Trennt die NPP vom Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="dcd07-119">Disconnects the NPP from the network.</span></span><br/>                                                                                   |
| [<span data-ttu-id="dcd07-120">**Getcontrolstate**</span><span class="sxs-lookup"><span data-stu-id="dcd07-120">**GetControlState**</span></span>](iesp-getcontrolstate.md) | <span data-ttu-id="dcd07-121">Ruft den Zustand der [*Erfassung*](c.md)ab, der angibt, ob die Erfassung ausgeführt wird oder angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="dcd07-121">Retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span><br/> |
| [<span data-ttu-id="dcd07-122">**Anhalten**</span><span class="sxs-lookup"><span data-stu-id="dcd07-122">**Pause**</span></span>](iesp-pause.md)                     | <span data-ttu-id="dcd07-123">Beendet vorübergehend die aktuelle Erfassung.</span><span class="sxs-lookup"><span data-stu-id="dcd07-123">Temporarily stops the current capture.</span></span><br/>                                                                                  |
| [<span data-ttu-id="dcd07-124">**Querystations**</span><span class="sxs-lookup"><span data-stu-id="dcd07-124">**QueryStations**</span></span>](iesp-querystations.md)     | <span data-ttu-id="dcd07-125">Ruft eine Liste aller Computer ab, die Netzwerkmonitor zum Erfassen von Daten in einem Subnetz verwenden.</span><span class="sxs-lookup"><span data-stu-id="dcd07-125">Retrieves a list of all computers that are using Network Monitor to capture data on a subnet.</span></span><br/>                           |
| [<span data-ttu-id="dcd07-126">**QueryStatus**</span><span class="sxs-lookup"><span data-stu-id="dcd07-126">**QueryStatus**</span></span>](iesp-querystatus.md)         | <span data-ttu-id="dcd07-127">Ruft den Status des NPP ab.</span><span class="sxs-lookup"><span data-stu-id="dcd07-127">Retrieves the status of the NPP.</span></span><br/>                                                                                        |
| [<span data-ttu-id="dcd07-128">**Fortsetzen**</span><span class="sxs-lookup"><span data-stu-id="dcd07-128">**Resume**</span></span>](iesp-resume.md)                   | <span data-ttu-id="dcd07-129">Setzt eine angehaltene Erfassung fort.</span><span class="sxs-lookup"><span data-stu-id="dcd07-129">Resumes a paused capture.</span></span><br/>                                                                                               |
| [<span data-ttu-id="dcd07-130">**Start**</span><span class="sxs-lookup"><span data-stu-id="dcd07-130">**Start**</span></span>](iesp-start.md)                     | <span data-ttu-id="dcd07-131">Startet die Erfassung und erstellt die Erfassungs Datei.</span><span class="sxs-lookup"><span data-stu-id="dcd07-131">Starts the capture and creates the capture file.</span></span><br/>                                                                        |
| [<span data-ttu-id="dcd07-132">**Stop**</span><span class="sxs-lookup"><span data-stu-id="dcd07-132">**Stop**</span></span>](iesp-stop.md)                       | <span data-ttu-id="dcd07-133">Hält die aktuelle Erfassung an.</span><span class="sxs-lookup"><span data-stu-id="dcd07-133">Stops the current capture.</span></span><br/>                                                                                              |



 

## <a name="requirements"></a><span data-ttu-id="dcd07-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dcd07-134">Requirements</span></span>



| <span data-ttu-id="dcd07-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dcd07-135">Requirement</span></span> | <span data-ttu-id="dcd07-136">Wert</span><span class="sxs-lookup"><span data-stu-id="dcd07-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcd07-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dcd07-137">Minimum supported client</span></span><br/> | <span data-ttu-id="dcd07-138">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dcd07-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="dcd07-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dcd07-139">Minimum supported server</span></span><br/> | <span data-ttu-id="dcd07-140">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dcd07-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="dcd07-141">Header</span><span class="sxs-lookup"><span data-stu-id="dcd07-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="dcd07-142"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcd07-142"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="dcd07-143">DLL</span><span class="sxs-lookup"><span data-stu-id="dcd07-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dcd07-144"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dcd07-144"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



 


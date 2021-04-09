---
description: TAPI 3 umfasst eine Reihe von Objekten, die von den fünf Haupt-TAPI-Objekten (TAPI, Address, Callcenter, callhub und Terminal) unabhängig sind.
ms.assetid: 090fa8e5-58a5-46ee-89a3-bd97fcfbf0f0
title: Stand-Alone Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e71fdea9c7ed4b66f57c3c0fe35625f35656555e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865003"
---
# <a name="stand-alone-objects"></a><span data-ttu-id="ab173-103">Stand-Alone Objekte</span><span class="sxs-lookup"><span data-stu-id="ab173-103">Stand-Alone Objects</span></span>

<span data-ttu-id="ab173-104">TAPI 3 umfasst eine Reihe von Objekten, die von den fünf Haupt-TAPI-Objekten (TAPI, Address, Callcenter, callhub und Terminal) unabhängig sind.</span><span class="sxs-lookup"><span data-stu-id="ab173-104">TAPI 3 involves a number of objects that are independent of its five main TAPI objects (TAPI, Address, Call, CallHub, and Terminal).</span></span> <span data-ttu-id="ab173-105">[Ereignis Schnittstellen](./event-interfaces.md) und [Enumeratorschnittstellen](enumerator-interfaces.md) sind eigenständige Objekte und werden separat zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="ab173-105">[Event Interfaces](./event-interfaces.md) and [Enumerator Interfaces](enumerator-interfaces.md) are stand-alone objects, and are summarized separately.</span></span> <span data-ttu-id="ab173-106">Im folgenden werden eigenständige nicht-Ereignis-und nicht-Enumerator-Schnittstellen zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="ab173-106">The following summarizes non-event and non-enumerator stand-alone interfaces.</span></span>



| <span data-ttu-id="ab173-107">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="ab173-107">Interface</span></span>                                             | <span data-ttu-id="ab173-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ab173-108">Description</span></span>                                                                                                                                                                                                   |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ab173-109">**Itcollection**</span><span class="sxs-lookup"><span data-stu-id="ab173-109">**ITCollection**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection)                  | <span data-ttu-id="ab173-110">Stellt Methoden bereit, mit denen Automatisierungs Client Anwendungen, wie z. b. Visual Basic, Sammlungs Informationen abrufen können.</span><span class="sxs-lookup"><span data-stu-id="ab173-110">Provides methods to allow Automation client applications such as Visual Basic to retrieve collection information.</span></span>                                                                                             |
| [<span data-ttu-id="ab173-111">**ITCollection2**</span><span class="sxs-lookup"><span data-stu-id="ab173-111">**ITCollection2**</span></span>](/windows/desktop/api/Tapi3if/nn-tapi3if-itcollection2)                | <span data-ttu-id="ab173-112">Erweitert die [**itcollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) durch Bereitstellen zusätzlicher Methoden zum Ändern von Auflistungen.</span><span class="sxs-lookup"><span data-stu-id="ab173-112">Extends [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) by providing additional methods for modifying collections.</span></span>                                                                                                       |
| [<span data-ttu-id="ab173-113">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="ab173-113">**IDispatch**</span></span>](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) | <span data-ttu-id="ab173-114">Standard-COM-Schnittstelle zum Implementieren von Automation.</span><span class="sxs-lookup"><span data-stu-id="ab173-114">Standard COM interface for implementing Automation.</span></span>                                                                                                                                                           |
| [<span data-ttu-id="ab173-115">**IUnknown**</span><span class="sxs-lookup"><span data-stu-id="ab173-115">**IUnknown**</span></span>](/windows/win32/api/unknwn/nn-unknwn-iunknown)                         | <span data-ttu-id="ab173-116">Standard-COM-Schnittstelle zum erhalten von Zeigern auf Objekt Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="ab173-116">Standard COM interface for getting pointers to object interfaces.</span></span>                                                                                                                                             |
| [<span data-ttu-id="ab173-117">**Itdispatchmapper**</span><span class="sxs-lookup"><span data-stu-id="ab173-117">**ITDispatchMapper**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itdispatchmapper)          | <span data-ttu-id="ab173-118">Ermöglicht es einer Anwendung, den Dispatch-Zeiger einer anderen Schnittstelle für ein Objekt abzurufen, wenn ein aktueller [**IDispatch**](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) -Zeiger angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="ab173-118">Allows an application to retrieve the dispatch pointer of another interface on an object, given a current [**IDispatch**](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) pointer.</span></span> <span data-ttu-id="ab173-119">Nützlich für einige Skriptsprachen.</span><span class="sxs-lookup"><span data-stu-id="ab173-119">Useful for some scripting languages.</span></span> |
| [<span data-ttu-id="ab173-120">**Itrequest**</span><span class="sxs-lookup"><span data-stu-id="ab173-120">**ITRequest**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itrequest)                        | <span data-ttu-id="ab173-121">Stellt Methoden bereit, die es einer TAPI 3-Anwendung ermöglichen, unter [stützte Telefonie](assisted-telephony-overview.md)zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ab173-121">Provides methods that allow a TAPI 3 application to use [Assisted Telephony](assisted-telephony-overview.md).</span></span>                                                                                                |



 



| <span data-ttu-id="ab173-122">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="ab173-122">Interface</span></span>                                  | <span data-ttu-id="ab173-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ab173-123">Description</span></span>                                                                                                                                                                |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ab173-124">**Itmediacontrol**</span><span class="sxs-lookup"><span data-stu-id="ab173-124">**ITMediaControl**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol)   | <span data-ttu-id="ab173-125">Startet, beendet und hält aktuelle Aktionen wie z. b. eine Wiedergabe an.</span><span class="sxs-lookup"><span data-stu-id="ab173-125">Starts, stops, and pauses current actions, such as a playback.</span></span>                                                                                                             |
| [<span data-ttu-id="ab173-126">**Itmediaplayback**</span><span class="sxs-lookup"><span data-stu-id="ab173-126">**ITMediaPlayback**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) | <span data-ttu-id="ab173-127">Stellt Wiedergabe spezifische Methoden bereit, die es einer Anwendung ermöglichen, Vorgänge wie das Festlegen der Liste der wieder zugebende Dateien und das Ändern der Wiedergabegeschwindigkeit auszuführen.</span><span class="sxs-lookup"><span data-stu-id="ab173-127">Provides playback-specific methods that allow an application to perform such operations as setting the list of files to play and changing the playback speed.</span></span>              |
| [<span data-ttu-id="ab173-128">**Itmediarecord**</span><span class="sxs-lookup"><span data-stu-id="ab173-128">**ITMediaRecord**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itmediarecord)     | <span data-ttu-id="ab173-129">Stellt Aufzeichnungs spezifische Methoden bereit, die es einer Anwendung ermöglichen, Vorgänge wie das Festlegen der Namen von Dateien zum Aufzeichnen und Ändern der Dauer einer Aufzeichnung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="ab173-129">Provides recording-specific methods that allow an application to perform such operations as setting the names of files to record and changing the duration of a recording.</span></span> |



 



| <span data-ttu-id="ab173-130">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="ab173-130">Interface</span></span>                                                  | <span data-ttu-id="ab173-131">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ab173-131">Description</span></span>                                                                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ab173-132">**Itscriptableaudioformat**</span><span class="sxs-lookup"><span data-stu-id="ab173-132">**ITScriptableAudioFormat**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itscriptableaudioformat) | <span data-ttu-id="ab173-133">Ruft das Audioformat ab oder legt das Audioformat für, eine Spur, fest.</span><span class="sxs-lookup"><span data-stu-id="ab173-133">Retrieves the audio format from, or sets the audio format for, a track.</span></span>                                                                                             |
| [<span data-ttu-id="ab173-134">**Itstaticaudioterminal**</span><span class="sxs-lookup"><span data-stu-id="ab173-134">**ITStaticAudioTerminal**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itstaticaudioterminal)     | <span data-ttu-id="ab173-135">Stellt Methoden für statische audioterminalobjekte bereit, die zur Unterstützung von Telefongeräten benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="ab173-135">Provides methods on static audio terminal objects that are needed to support phone devices.</span></span> <span data-ttu-id="ab173-136">TAPI 3,1-Msps müssen diese Schnittstelle für alle statischen audioterminals verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="ab173-136">TAPI 3.1 MSPs must expose this interface on all static audio terminals.</span></span> |



 

 

 

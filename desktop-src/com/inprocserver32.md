---
title: InprocServer32
description: Registriert einen 32-Bit-in-Process-Server und gibt das Threading Modell des Apartment an, in dem der Server ausgeführt werden kann.
ms.assetid: 4edbbd9d-7ea1-4476-aee7-eaf30e54db8d
keywords:
- InprocServer32 Registrierungsschlüssel com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0daae9d495ad588e0dc710b63fe7d7ae9f48c11d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515962"
---
# <a name="inprocserver32"></a><span data-ttu-id="08501-104">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="08501-104">InprocServer32</span></span>

<span data-ttu-id="08501-105">Registriert einen 32-Bit-in-Process-Server und gibt das Threading Modell des Apartment an, in dem der Server ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="08501-105">Registers a 32-bit in-process server and specifies the threading model of the apartment the server can run in.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="08501-106">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="08501-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocServer32
         (Default) = path
         ThreadingModel = value
```

## <a name="remarks"></a><span data-ttu-id="08501-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="08501-107">Remarks</span></span>

<span data-ttu-id="08501-108">**ThreadingModel** ist ein **reg \_ SZ** -Wert, der das Threading Modell angibt.</span><span class="sxs-lookup"><span data-stu-id="08501-108">**ThreadingModel** is a **REG\_SZ** value the specifies the threading model.</span></span> <span data-ttu-id="08501-109">Die möglichen Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="08501-109">The possible values are shown in the following table.</span></span>



| <span data-ttu-id="08501-110">Wert</span><span class="sxs-lookup"><span data-stu-id="08501-110">Value</span></span>     | <span data-ttu-id="08501-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="08501-111">Description</span></span>                                |
|-----------|--------------------------------------------|
| <span data-ttu-id="08501-112">Apartment</span><span class="sxs-lookup"><span data-stu-id="08501-112">Apartment</span></span> | <span data-ttu-id="08501-113">Single Thread-Apartment</span><span class="sxs-lookup"><span data-stu-id="08501-113">Single-threaded apartment</span></span>                  |
| <span data-ttu-id="08501-114">Both</span><span class="sxs-lookup"><span data-stu-id="08501-114">Both</span></span>      | <span data-ttu-id="08501-115">Single Thread-oder Multithread-Apartment</span><span class="sxs-lookup"><span data-stu-id="08501-115">Single-threaded or multithreaded apartment</span></span> |
| <span data-ttu-id="08501-116">Kostenlos</span><span class="sxs-lookup"><span data-stu-id="08501-116">Free</span></span>      | <span data-ttu-id="08501-117">Multithread-Apartment</span><span class="sxs-lookup"><span data-stu-id="08501-117">Multithreaded apartment</span></span>                    |
| <span data-ttu-id="08501-118">Neutral</span><span class="sxs-lookup"><span data-stu-id="08501-118">Neutral</span></span>   | <span data-ttu-id="08501-119">Neutrales Apartment</span><span class="sxs-lookup"><span data-stu-id="08501-119">Neutral apartment</span></span>                          |



 

<span data-ttu-id="08501-120">Sie müssen für jedes Objekt, das vom Prozess internen Server bereitgestellt wird, denselben Wert verwenden.</span><span class="sxs-lookup"><span data-stu-id="08501-120">You must use the same value for every object provided by the in-process server.</span></span>

<span data-ttu-id="08501-121">Wenn **ThreadingModel** nicht vorhanden oder nicht auf einen Wert festgelegt ist, wird der Server in das erste Apartment geladen, das im Prozess initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="08501-121">If **ThreadingModel** is not present or is not set to a value, the server is loaded into the first apartment that was initialized in the process.</span></span> <span data-ttu-id="08501-122">Dieses Apartment wird manchmal als Haupt-Single Thread-Apartment (STA) bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="08501-122">This apartment is sometimes referred to as the main single-threaded apartment (STA).</span></span> <span data-ttu-id="08501-123">Wenn der erste STA in einem Prozess durch com initialisiert wird, anstatt durch einen expliziten Aufruf von [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) oder [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex), wird er als Host STA bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="08501-123">If the first STA in a process is initialized by COM, rather than by an explicit call to [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) or [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex), it is called the host STA.</span></span> <span data-ttu-id="08501-124">Beispielsweise erstellt com einen Host-STA, wenn ein in-Process-Server, der geladen werden soll, einen STA erfordert, aber zurzeit kein STA im Prozess vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="08501-124">For example, COM creates a host STA if an in-process server to be loaded requires an STA but there is currently no STA in the process.</span></span>

<span data-ttu-id="08501-125">Wenn möglich, wird der Prozess interne Server in dasselbe Apartment geladen wie der Client, der ihn lädt.</span><span class="sxs-lookup"><span data-stu-id="08501-125">Whenever possible, the in-process server is loaded in the same apartment as the client that loads it.</span></span> <span data-ttu-id="08501-126">Wenn das Threading Modell des Client-Apartment nicht mit dem angegebenen Modell kompatibel ist, wird der Server entsprechend der Angabe in der folgenden Tabelle geladen.</span><span class="sxs-lookup"><span data-stu-id="08501-126">If the threading model of the client apartment is not compatible with the model specified, the server is loaded as indicated in the following table.</span></span>



| <span data-ttu-id="08501-127">Threading Modell des Servers</span><span class="sxs-lookup"><span data-stu-id="08501-127">Threading model of server</span></span> | <span data-ttu-id="08501-128">Apartment Server wird ausgeführt in</span><span class="sxs-lookup"><span data-stu-id="08501-128">Apartment server is run in</span></span> |
|---------------------------|----------------------------|
| <not specified>     | <span data-ttu-id="08501-129">Haupt-STA</span><span class="sxs-lookup"><span data-stu-id="08501-129">Main STA</span></span>                   |
| <span data-ttu-id="08501-130">Both</span><span class="sxs-lookup"><span data-stu-id="08501-130">Both</span></span>                      | <span data-ttu-id="08501-131">Dasselbe Apartment wie der Client</span><span class="sxs-lookup"><span data-stu-id="08501-131">Same apartment as client</span></span>   |
| <span data-ttu-id="08501-132">Kostenlos</span><span class="sxs-lookup"><span data-stu-id="08501-132">Free</span></span>                      | <span data-ttu-id="08501-133">Multithread-Apartment</span><span class="sxs-lookup"><span data-stu-id="08501-133">Multithreaded apartment</span></span>    |
| <span data-ttu-id="08501-134">Neutral</span><span class="sxs-lookup"><span data-stu-id="08501-134">Neutral</span></span>                   | <span data-ttu-id="08501-135">Neutrales Apartment</span><span class="sxs-lookup"><span data-stu-id="08501-135">Neutral apartment</span></span>          |



 

<span data-ttu-id="08501-136">Wenn das Threading Modell des Servers Apartment ist, hängt das Apartment, in das der Server geladen wird, von dem Apartment ab, in dem der Client ausgeführt wird, wie in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="08501-136">If the threading model of the server is Apartment, the apartment the server is loaded in depends on the apartment the client is running in, as indicated in the following table.</span></span>



| <span data-ttu-id="08501-137">Apartment Client wird ausgeführt in</span><span class="sxs-lookup"><span data-stu-id="08501-137">Apartment client is run in</span></span> | <span data-ttu-id="08501-138">Apartment Server wird ausgeführt in</span><span class="sxs-lookup"><span data-stu-id="08501-138">Apartment server is run in</span></span> |
|----------------------------|----------------------------|
| <span data-ttu-id="08501-139">Multithread</span><span class="sxs-lookup"><span data-stu-id="08501-139">Multithreaded</span></span>              | <span data-ttu-id="08501-140">Host-STA</span><span class="sxs-lookup"><span data-stu-id="08501-140">Host STA</span></span>                   |
| <span data-ttu-id="08501-141">Neutral (auf STA-Thread)</span><span class="sxs-lookup"><span data-stu-id="08501-141">Neutral (on STA thread)</span></span>    | <span data-ttu-id="08501-142">Dasselbe Apartment wie der Client</span><span class="sxs-lookup"><span data-stu-id="08501-142">Same apartment as client</span></span>   |
| <span data-ttu-id="08501-143">Neutral (im MTA-Thread)</span><span class="sxs-lookup"><span data-stu-id="08501-143">Neutral (on MTA thread)</span></span>    | <span data-ttu-id="08501-144">Host-STA</span><span class="sxs-lookup"><span data-stu-id="08501-144">Host STA</span></span>                   |



 

<span data-ttu-id="08501-145">COM kann auch einen Host-Multithread-Apartment (MTA) erstellen.</span><span class="sxs-lookup"><span data-stu-id="08501-145">COM can also create a host multithreaded apartment (MTA).</span></span> <span data-ttu-id="08501-146">Wenn ein Client in einem Single Thread-Apartment einen Prozess internen Server anfordert, dessen Threading Modell frei ist, wenn kein MTA im Prozess vorhanden ist, erstellt com einen Host-MTA und lädt ihn in den Server.</span><span class="sxs-lookup"><span data-stu-id="08501-146">If a client in a single-threaded apartment requests an in-process server whose threading model is Free when there is no MTA in the process, COM creates a host MTA and loads the server into it.</span></span>

<span data-ttu-id="08501-147">Bei einem in-Process-32-Bit-Server müssen die Schlüssel [**InprocHandler32**](inprochandler32.md), [**InprocServer**](inprocserver.md), **InProcServer32** und [**Insertable**](insertable.md) registriert werden.</span><span class="sxs-lookup"><span data-stu-id="08501-147">For a 32-bit in-process server, the [**InprocHandler32**](inprochandler32.md), [**InprocServer**](inprocserver.md), **InprocServer32**, and [**Insertable**](insertable.md) keys must be registered.</span></span> <span data-ttu-id="08501-148">Der **InprocServer** -Eintrag wird nur aus Gründen der Abwärtskompatibilität benötigt.</span><span class="sxs-lookup"><span data-stu-id="08501-148">The **InprocServer** entry is needed only for backward compatibility.</span></span> <span data-ttu-id="08501-149">Wenn Sie fehlt, funktioniert die Klasse weiterhin, aber Sie kann nicht in 16-Bit-Anwendungen geladen werden.</span><span class="sxs-lookup"><span data-stu-id="08501-149">If it is missing, the class still works but it cannot be loaded in 16-bit applications.</span></span>

<span data-ttu-id="08501-150">Wenn ein Container die Registrierung nach einem in-Process-Server durchsucht, hat die 16-Bit-Version eine Priorität mit einem 16-Bit-Container, und die 32-Bit-Version hat eine Priorität mit einem 32-Bit-Container.</span><span class="sxs-lookup"><span data-stu-id="08501-150">If a container is searching the registry for an in-process server, the 16-bit version has priority with a 16-bit container and the 32-bit version has priority with a 32-bit container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="08501-151">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="08501-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08501-152">**InprocServer**</span><span class="sxs-lookup"><span data-stu-id="08501-152">**InprocServer**</span></span>](inprocserver.md)
</dt> </dl>

 

 





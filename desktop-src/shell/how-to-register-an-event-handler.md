---
description: Ein Gerät kann potenziell viele Ereignisse generieren, und jedes Ereignis hat die Möglichkeit, von einem von mehreren unterschiedlichen Handlern verarbeitet zu werden.
ms.assetid: C203B5AB-917C-4543-98D6-EDE02E0B5E49
title: Registrieren eines Ereignis Handlers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a3d786111a80cba455dd3480bdc970bc27009d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979521"
---
# <a name="how-to-register-an-event-handler"></a><span data-ttu-id="dfce0-103">Registrieren eines Ereignis Handlers</span><span class="sxs-lookup"><span data-stu-id="dfce0-103">How to Register an Event Handler</span></span>

<span data-ttu-id="dfce0-104">Ein Gerät kann potenziell viele Ereignisse generieren, und jedes Ereignis hat die Möglichkeit, von einem von mehreren unterschiedlichen Handlern verarbeitet zu werden.</span><span class="sxs-lookup"><span data-stu-id="dfce0-104">A device can potentially generate many events, and each event has the option of being handled by one of a number of different handlers.</span></span> <span data-ttu-id="dfce0-105">In Windows XP sind die folgenden Ereignisse definiert:</span><span class="sxs-lookup"><span data-stu-id="dfce0-105">In Windows XP, the following events are defined:</span></span>

-   <span data-ttu-id="dfce0-106">Devicearrival</span><span class="sxs-lookup"><span data-stu-id="dfce0-106">DeviceArrival</span></span>
-   <span data-ttu-id="dfce0-107">Deviceremoval</span><span class="sxs-lookup"><span data-stu-id="dfce0-107">DeviceRemoval</span></span>
-   <span data-ttu-id="dfce0-108">Mediaarrival</span><span class="sxs-lookup"><span data-stu-id="dfce0-108">MediaArrival</span></span>
-   <span data-ttu-id="dfce0-109">Mediaremuval</span><span class="sxs-lookup"><span data-stu-id="dfce0-109">MediaRemoval</span></span>

## <a name="instructions"></a><span data-ttu-id="dfce0-110">Instructions</span><span class="sxs-lookup"><span data-stu-id="dfce0-110">Instructions</span></span>


<span data-ttu-id="dfce0-111">Ereignishandler werden unter dem Schlüssel **Eventhandlers** definiert.</span><span class="sxs-lookup"><span data-stu-id="dfce0-111">Event handlers are defined under the **EventHandlers** key.</span></span> <span data-ttu-id="dfce0-112">Bei den Werten eines ereignishandlerschlüssels handelt es sich um die Namen der einzelnen Handler, aus denen der Benutzer auswählen muss, wenn das Ereignis erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="dfce0-112">An event handler key's values are the names of each handler that the user must choose from when the event is detected.</span></span> <span data-ttu-id="dfce0-113">Diesen Einträgen ist kein Datenwert zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="dfce0-113">There is no data value associated with these entries.</span></span> <span data-ttu-id="dfce0-114">Im folgenden finden Sie eine Beispiel Definition für einen benutzerdefinierten Ereignishandler mit dem Namen **mynewremovaleventhandler, der diese handlermöglichkeiten** für den Benutzer darstellt:</span><span class="sxs-lookup"><span data-stu-id="dfce0-114">Following is an example definition for a custom event handler called **MyNewRemovalEventHandler**, which presents these handler possibilities to the user:</span></span>

-   <span data-ttu-id="dfce0-115">Ein Handler, der verwendet wird, wenn das Ereignis auf einem Gerät erkannt wird, das vom Unternehmen mit dem Namen "c-so, Inc."</span><span class="sxs-lookup"><span data-stu-id="dfce0-115">A handler to use if the event is detected on a device made by the company named Contoso, Inc.</span></span>
-   <span data-ttu-id="dfce0-116">Ein Handler, der verwendet wird, wenn das Ereignis auf einem Gerät erkannt wird, das vom Unternehmen mit dem Namen Fabrikam, Inc.</span><span class="sxs-lookup"><span data-stu-id="dfce0-116">A handler to use if the event is detected on a device made by the company named Fabrikam, Inc.</span></span>
-   <span data-ttu-id="dfce0-117">Ein Handler, der in allen anderen Fällen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="dfce0-117">A handler to use in all other cases.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     EventHandlers
                        MyNewRemovalEventHandler
                           CompanyContosoHandler [REG_SZ]
                           CompanyFabrikamHandler [REG_SZ]
                           MyRemovalHandler [REG_SZ]
```

<span data-ttu-id="dfce0-118">Nachdem ein Ereignishandler definiert wurde, muss er mit einem Geräte Handler für eine der Ereignis Möglichkeiten registriert werden: devicearrival, deviceremoval, mediaarrival oder mediaremoval.</span><span class="sxs-lookup"><span data-stu-id="dfce0-118">After an event handler is defined, it must be registered with a device handler for one of the event possibilities: DeviceArrival, DeviceRemoval, MediaArrival, or MediaRemoval.</span></span> <span data-ttu-id="dfce0-119">Mynewremovaleventhandler, der zuvor definiert wurde, wird für deviceremoval unter einem benutzerdefinierten Geräte Handler mit dem Namen mydevicehandler verwendet und für diesen Zweck im folgenden Beispiel definiert.</span><span class="sxs-lookup"><span data-stu-id="dfce0-119">MyNewRemovalEventHandler, defined earlier, is used for DeviceRemoval under a custom device handler named MyDeviceHandler and is defined for that purpose in the following example.</span></span> <span data-ttu-id="dfce0-120">Auch hier hat der Registrierungs Wert keine Daten Komponente.</span><span class="sxs-lookup"><span data-stu-id="dfce0-120">Again, the registry value has no data component.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     DeviceHandlers
                        EventHandlers
                           DeviceRemoval
                              MyNewRemovalEventHandler
```

<span data-ttu-id="dfce0-121">In Windows XP wird der folgende Satz von EventHandler definiert.</span><span class="sxs-lookup"><span data-stu-id="dfce0-121">Windows XP predefines the following set of EventHandlers.</span></span> 

| <span data-ttu-id="dfce0-122">Eventhandlers-Schlüssel</span><span class="sxs-lookup"><span data-stu-id="dfce0-122">EventHandlers key</span></span>        | <span data-ttu-id="dfce0-123">Medien-oder Dateityp</span><span class="sxs-lookup"><span data-stu-id="dfce0-123">Media or file type</span></span>                             |
|--------------------------|------------------------------------------------|
| <span data-ttu-id="dfce0-124">HandleCDBurningOnArrival</span><span class="sxs-lookup"><span data-stu-id="dfce0-124">HandleCDBurningOnArrival</span></span> | <span data-ttu-id="dfce0-125">Leere CD-R/CD-RW</span><span class="sxs-lookup"><span data-stu-id="dfce0-125">Blank CD-R/CD-RW</span></span>                               |
| <span data-ttu-id="dfce0-126">ShowPicturesOnArrival</span><span class="sxs-lookup"><span data-stu-id="dfce0-126">ShowPicturesOnArrival</span></span>    | <span data-ttu-id="dfce0-127">Bilddateien</span><span class="sxs-lookup"><span data-stu-id="dfce0-127">Picture files</span></span>                                  |
| <span data-ttu-id="dfce0-128">PlayMusicFilesOnArrival</span><span class="sxs-lookup"><span data-stu-id="dfce0-128">PlayMusicFilesOnArrival</span></span>  | <span data-ttu-id="dfce0-129">Musikdateien</span><span class="sxs-lookup"><span data-stu-id="dfce0-129">Music files</span></span>                                    |
| <span data-ttu-id="dfce0-130">PlayVideoFilesOnArrival</span><span class="sxs-lookup"><span data-stu-id="dfce0-130">PlayVideoFilesOnArrival</span></span>  | <span data-ttu-id="dfce0-131">Video Dateien</span><span class="sxs-lookup"><span data-stu-id="dfce0-131">Video files</span></span>                                    |
| <span data-ttu-id="dfce0-132">PlayCDAudioOnArrival</span><span class="sxs-lookup"><span data-stu-id="dfce0-132">PlayCDAudioOnArrival</span></span>     | <span data-ttu-id="dfce0-133">AudioCD (Redbook Format CD mit Audiospuren)</span><span class="sxs-lookup"><span data-stu-id="dfce0-133">Audio CD (REDBOOK format CD with Audio tracks)</span></span> |
| <span data-ttu-id="dfce0-134">PlayDVDMovieOnArrival</span><span class="sxs-lookup"><span data-stu-id="dfce0-134">PlayDVDMovieOnArrival</span></span>    | <span data-ttu-id="dfce0-135">DVD-Filme</span><span class="sxs-lookup"><span data-stu-id="dfce0-135">DVD movies</span></span>                                     |



 

<span data-ttu-id="dfce0-136">In Windows Vista sind zusätzlich zu den oben aufgeführten Event andlers vordefiniert.</span><span class="sxs-lookup"><span data-stu-id="dfce0-136">Windows Vista predefines the following set of EventHandlers in addition to those above.</span></span> 

| <span data-ttu-id="dfce0-137">Eventhandlers-Schlüssel</span><span class="sxs-lookup"><span data-stu-id="dfce0-137">EventHandlers key</span></span>              | <span data-ttu-id="dfce0-138">Medien-oder Dateityp</span><span class="sxs-lookup"><span data-stu-id="dfce0-138">Media or file type</span></span>   |
|--------------------------------|----------------------|
| <span data-ttu-id="dfce0-139">PlaySuperVideoCDMovieOnArrival</span><span class="sxs-lookup"><span data-stu-id="dfce0-139">PlaySuperVideoCDMovieOnArrival</span></span> | <span data-ttu-id="dfce0-140">Super VideoCD-Filme</span><span class="sxs-lookup"><span data-stu-id="dfce0-140">Super VideoCD movies</span></span> |
| <span data-ttu-id="dfce0-141">PlayVideoCDMovieOnArrival</span><span class="sxs-lookup"><span data-stu-id="dfce0-141">PlayVideoCDMovieOnArrival</span></span>      | <span data-ttu-id="dfce0-142">VideoCD-Filme</span><span class="sxs-lookup"><span data-stu-id="dfce0-142">VideoCD movies</span></span>       |



 

 

 




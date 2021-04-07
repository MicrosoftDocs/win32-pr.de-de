---
title: Ereignis Koordinaten Übersetzung
description: Ereignis Koordinaten Übersetzung
ms.assetid: e7de8af1-a409-4140-9e85-e035bd583912
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c40a742ead8fc8d7e431c1caa5210f0978168cb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713218"
---
# <a name="event-coordinate-translation"></a><span data-ttu-id="6dcfc-103">Ereignis Koordinaten Übersetzung</span><span class="sxs-lookup"><span data-stu-id="6dcfc-103">Event Coordinate Translation</span></span>

<span data-ttu-id="6dcfc-104">Die 96-Spezifikation für-Steuerelemente erfordert, dass die Koordinaten, die für Ereignisse, die von der-Steuer Elements ausgelöst werden, von HIMETRIC in als Punkt basiert</span><span class="sxs-lookup"><span data-stu-id="6dcfc-104">The 96 specification for controls requires that coordinates passed for events fired by the control change from being HIMETRIC to being points based.</span></span> <span data-ttu-id="6dcfc-105">Diese Änderung führt dazu, dass das Ereignis das Übergeben von Koordinaten in der Zeile mit den Eigenschaften und Methoden durchführt, sodass die Koordinaten Übersetzung nicht mehr für den Container zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="6dcfc-105">This change brings the event passing of coordinates in line with properties and methods and thus coordinate translation is no longer the responsibility of the container.</span></span> <span data-ttu-id="6dcfc-106">Dies löst bestimmte Kompatibilitätsprobleme aus, bei denen ein Steuerelement Ereignisse mithilfe einer Koordinaten Basis auslöst, die nicht erwartet wird. Dies sollte nur ein Problem sein, bei dem ein 96-Steuerelement Container ein älteres Pre-96-Steuerelement wie folgt gehostet:</span><span class="sxs-lookup"><span data-stu-id="6dcfc-106">This raises certain compatibility issues where a control fires events using a coordinate base that it is not expecting, this should only be an issue where a 96 control container is hosting an older pre-96 control as follows:</span></span>

-   <span data-ttu-id="6dcfc-107">Wenn ein älterer Pre-96-Container ein 96-Steuerelement hostet, stellt das Steuerelement die Ereignis Koordinaten als Punkte dar, sodass der Container keine Probleme verursacht, da der Container den Parametertyp erkennen sollte.</span><span class="sxs-lookup"><span data-stu-id="6dcfc-107">When an older pre-96 container hosts a 96 control the control will present the event coordinates as points, this should not cause the container any problems as the container should recognize the parameter type.</span></span>
-   <span data-ttu-id="6dcfc-108">Wenn ein 96-Container ein Pre-96-Steuerelement hostet, stellt das Steuerelement den Container mit Koordinaten dar und erwartet, dass der Container eine beliebige Übersetzung benötigt.</span><span class="sxs-lookup"><span data-stu-id="6dcfc-108">When a 96 container hosts a pre-96 control the control will present the container with coordinates and expect the container to any translation necessary.</span></span> <span data-ttu-id="6dcfc-109">Allerdings erwartet der 96-Container, dass ein Steuerelement der 96-Steuerelement Spezifikation entspricht und seine Koordinaten als Punkte darstellen.</span><span class="sxs-lookup"><span data-stu-id="6dcfc-109">However the 96 container will be expecting a control to conform to the 96 controls specification and present its coordinates as points.</span></span> <span data-ttu-id="6dcfc-110">Das-Steuerelement verwendet die [**transformcoords**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-transformcoords) -Methode auf der [**iolecontrolsite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) -Schnittstelle, die vom Container bereitgestellt wird, auf die gleiche Weise wie für Eigenschaften und Methoden, um dies zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="6dcfc-110">The control uses the [**TransformCoords**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-transformcoords) method on the [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) interface provided by the container in the same way as it does for properties and methods to achieve this.</span></span>

<span data-ttu-id="6dcfc-111">Daher muss der Benutzer eines 96-Containers, der vor 96-Steuerelementen gehostet wird, beachten, dass eine weitere Übersetzung der Koordinaten erforderlich ist, wenn Ereignisse ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="6dcfc-111">As a result the user of a 96 container hosting pre-96 controls will need to be aware that further translation of coordinates may be necessary when events are fired.</span></span>

 

 





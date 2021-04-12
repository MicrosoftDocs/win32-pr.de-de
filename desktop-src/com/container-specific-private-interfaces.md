---
title: Private Schnittstellen Container-Specific
description: Private Schnittstellen Container-Specific
ms.assetid: 429cf71c-9b9d-4d0b-b5de-91fbe1dde3cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25c6569a79e9f1801c6fd82543bc40408903c780
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311298"
---
# <a name="container-specific-private-interfaces"></a><span data-ttu-id="69ca0-103">Private Schnittstellen Container-Specific</span><span class="sxs-lookup"><span data-stu-id="69ca0-103">Container-Specific Private Interfaces</span></span>

<span data-ttu-id="69ca0-104">Einige Container stellen Container spezifische private Schnittstellen für zusätzliche Funktionen oder eine verbesserte Leistung bereit.</span><span class="sxs-lookup"><span data-stu-id="69ca0-104">Some containers provide container-specific private interfaces for additional functionality or improved performance.</span></span> <span data-ttu-id="69ca0-105">Steuerelemente, die sich auf diese Container spezifischen Schnittstellen stützen, sollten, wenn möglich, ohne diese Container spezifischen Schnittstellen funktionieren, damit das Steuerelement in verschiedenen Containern funktioniert.</span><span class="sxs-lookup"><span data-stu-id="69ca0-105">Controls that rely on those container-specific interfaces should, if possible, work without those container-specific interfaces present so that the control functions in different containers.</span></span> <span data-ttu-id="69ca0-106">Beispielsweise implementiert Visual Basic Private Schnittstellen, die Zeichen folgen Formatierungsfunktionen für Steuerelemente bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="69ca0-106">For example, Visual Basic implements private interfaces that provide string formatting functionality to controls.</span></span> <span data-ttu-id="69ca0-107">Wenn ein Steuerelement diese privaten Formatierungs Schnittstellen nutzt, sollte es in der Lage sein, mit standardmäßiger Formatierungs Unterstützung auszuführen, wenn diese Schnittstellen nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="69ca0-107">If a control makes use of these private formatting interfaces, it should be able to run with default formatting support if these interfaces are not available.</span></span> <span data-ttu-id="69ca0-108">Wenn das Steuerelement ohne die privaten Schnittstellen funktionieren kann, sollte es entsprechende Maßnahmen ergreifen (z. b. den Benutzer vor eingeschränkter Funktionalität warnen), aber weiterhin arbeiten.</span><span class="sxs-lookup"><span data-stu-id="69ca0-108">If the control can function without the private interfaces, it should take appropriate action (such as warn the user of reduced functionality) but continue to work.</span></span> <span data-ttu-id="69ca0-109">Wenn dies nicht möglich ist, sollte eine Komponenten Kategorie bei Bedarf registriert werden, damit nur Container, die diese Funktion unterstützen, diese Steuerelemente hosten können.</span><span class="sxs-lookup"><span data-stu-id="69ca0-109">If this is not an option, a component category should be registered as required so that only containers supporting this functionality can host these controls.</span></span>

 

 





---
title: Was ist das Steuerungspunkt-Objektmodell?
description: In der folgenden Abbildung wird das grundlegende Steuerungspunkt-Objektmodell veranschaulicht.
ms.assetid: 6c5a32a1-932e-4868-b4c6-8701e90a7c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e491d3ec89b1074fb09a9f7632a886fb67b59863
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311363"
---
# <a name="what-is-the-control-point-object-model"></a><span data-ttu-id="d6f79-103">Was ist das Steuerungspunkt-Objektmodell?</span><span class="sxs-lookup"><span data-stu-id="d6f79-103">What is the Control Point Object Model?</span></span>

<span data-ttu-id="d6f79-104">In der folgenden Abbildung wird das grundlegende Steuerungspunkt-Objektmodell veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="d6f79-104">The following illustration shows the basic Control Point object model.</span></span>

![Steuerungspunkt-Objektmodell](images/upnp-object-model.png)

<span data-ttu-id="d6f79-106">Durch die Suche nach Geräten mithilfe der Device Finder-Schnittstelle wird eine Geräte Sammlung erstellt.</span><span class="sxs-lookup"><span data-stu-id="d6f79-106">Searching for devices with the Device Finder interface creates a Devices collection.</span></span> <span data-ttu-id="d6f79-107">Eine Geräte Sammlung enthält 0 (null) oder mehr Geräte Objekte.</span><span class="sxs-lookup"><span data-stu-id="d6f79-107">A Devices collection contains zero or more Device objects.</span></span> <span data-ttu-id="d6f79-108">Anwendungen können mit den verschiedenen Geräte Sammlungs Methoden auf einzelne Geräte Objekte zugreifen.</span><span class="sxs-lookup"><span data-stu-id="d6f79-108">Applications can use the various Devices collection methods to access individual Device objects.</span></span>

<span data-ttu-id="d6f79-109">Geräte Objekte enthalten immer eine Dienste-Sammlung, die ein oder mehrere Dienst Objekte enthält.</span><span class="sxs-lookup"><span data-stu-id="d6f79-109">Device objects always contain a Services collection that contains one or more Service objects.</span></span> <span data-ttu-id="d6f79-110">Diese Dienst Objekte werden von Anwendungen verwendet, um mit Geräten zu kommunizieren und diese zu steuern.</span><span class="sxs-lookup"><span data-stu-id="d6f79-110">These service objects are used by applications to communicate with and control devices.</span></span>

 

 





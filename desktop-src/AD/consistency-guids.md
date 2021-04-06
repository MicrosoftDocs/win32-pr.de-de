---
title: Konsistenz-GUIDs
description: Konsistenz-GUIDs stellen eine Erkennungs Strategie dar, die es einer Anwendung ermöglicht, partielle Updates zu erkennen.
ms.assetid: 3418667f-4d5a-4a4b-b0f5-7744a21608f7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bcfb25d0f04a459217811a2ff0393fac47e3206
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036256"
---
# <a name="consistency-guids"></a><span data-ttu-id="2886d-103">Konsistenz-GUIDs</span><span class="sxs-lookup"><span data-stu-id="2886d-103">Consistency GUIDs</span></span>

<span data-ttu-id="2886d-104">Konsistenz-GUIDs stellen eine Erkennungs Strategie dar, die es einer Anwendung ermöglicht, partielle Updates zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="2886d-104">Consistency GUIDs are a detection strategy that allows an application to detect partial updates.</span></span> <span data-ttu-id="2886d-105">Eine Konsistenz-GUID (Global Unique Identifier) wird auf jedes Objekt in einem verknüpften Satz angewendet.</span><span class="sxs-lookup"><span data-stu-id="2886d-105">A consistency GUID (Globally Unique IDentifier) is applied to each object in a related set.</span></span> <span data-ttu-id="2886d-106">In der Implementierung generiert eine Quell Anwendung eine neue GUID und wendet Sie auf jedes Objekt an, das Sie in der Gruppe verwandter Objekte aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="2886d-106">In implementation, a source application generates a new GUID and applies it to each object it updates in the set of related objects.</span></span> <span data-ttu-id="2886d-107">Anschließend wendet Sie die neue GUID auf die restlichen Objekte in der Menge an und wird beendet, indem die neue GUID auf das "Master"-Objekt angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="2886d-107">It then applies the new GUID to the rest of the objects in the set, and finishes by applying the new GUID to the "master" object.</span></span> <span data-ttu-id="2886d-108">In der Regel handelt es sich bei dem "Master"-Objekt um einen Container, der das übergeordnete Element der anderen Objekte in der Menge ist.</span><span class="sxs-lookup"><span data-stu-id="2886d-108">Typically, the "master" object will be a container that is the parent of the other objects in the set.</span></span>

<span data-ttu-id="2886d-109">Wichtige Hinweise:</span><span class="sxs-lookup"><span data-stu-id="2886d-109">Some important considerations:</span></span>

-   <span data-ttu-id="2886d-110">Konsistenz-GUIDs, die mit Objekt Zählungen oder Prüfsummen kombiniert werden, sind effektiver als Konsistenz-GUIDs, da die Anwendung, die die Objekte liest, möglicherweise nicht weiß, wie viele Objekte mit der GUID vorhanden sein sollten.</span><span class="sxs-lookup"><span data-stu-id="2886d-110">Consistency GUIDs combined with object counts or checksums are more effective than consistency GUIDs alone, because the application reading the objects may not know how many objects with the GUID should be present.</span></span>
-   <span data-ttu-id="2886d-111">Anwendungen müssen eigene GUIDs generieren (eine Microsoft Win32-API, uuidcreate, bietet diese Funktion) und nicht die vom System generierten GUIDs verwenden, die im **objectGUID** -Attribut eines Objekts gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="2886d-111">Applications must generate their own GUIDs (a Microsoft Win32 API, UuidCreate, provides this function), and not use the system-generated GUIDs found in an object's **objectGUID** attribute.</span></span> <span data-ttu-id="2886d-112">Dies liegt daran, dass eine Konsistenz-GUID bei jeder Aktualisierung des Satzes von Objekten geändert werden muss.</span><span class="sxs-lookup"><span data-stu-id="2886d-112">This is because a consistency GUID needs to change each time the set of objects is updated.</span></span> <span data-ttu-id="2886d-113">Objektidentitäts-GUIDs, die in " **objectGUID** " gefunden werden, werden nach dem Erstellen des Objekts nie geändert.</span><span class="sxs-lookup"><span data-stu-id="2886d-113">Object identity GUIDs found in **objectGUID** never change after the object has been created.</span></span>
-   <span data-ttu-id="2886d-114">Bei Konsistenz-GUIDs wird davon ausgegangen, dass kein Objekt von Mengen gemeinsam verwendet wird, sodass jede Menge eine eindeutige Konsistenz-GUID aufweisen kann.</span><span class="sxs-lookup"><span data-stu-id="2886d-114">Consistency GUIDs assume that no object is shared among sets, so each set can have a unique consistency GUID.</span></span>

 

 





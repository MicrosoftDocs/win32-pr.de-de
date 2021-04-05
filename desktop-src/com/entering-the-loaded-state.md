---
title: Eingabe des geladenen Zustands
description: Eingabe des geladenen Zustands
ms.assetid: 841b6f1a-cf9d-4a7e-9732-0701777a9617
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: add74927d107d7f6b9fe2d76856adec6697a00c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709443"
---
# <a name="entering-the-loaded-state"></a><span data-ttu-id="d380c-103">Eingabe des geladenen Zustands</span><span class="sxs-lookup"><span data-stu-id="d380c-103">Entering the Loaded State</span></span>

<span data-ttu-id="d380c-104">Wenn ein Objekt in den geladenen Zustand wechselt, werden die in-Memory-Strukturen erstellt, die das Objekt darstellen, sodass Vorgänge für das Objekt aufgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="d380c-104">When an object enters the loaded state, the in-memory structures representing the object are created so that operations can be invoked on it.</span></span> <span data-ttu-id="d380c-105">Der Handler des-Objekts oder der in-Process-Server wird geladen.</span><span class="sxs-lookup"><span data-stu-id="d380c-105">The object's handler or in-process server is loaded.</span></span> <span data-ttu-id="d380c-106">Dieser Prozess, der als *Instanziierung* bezeichnet wird, tritt auf, wenn ein Objekt aus dem permanenten Speicher geladen wird (ein Übergang von dem passiven in den geladenen Zustand) oder wenn ein Objekt zum ersten Mal erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d380c-106">This process, referred to as *instantiation*, occurs when an object is loaded from persistent storage (a transition from the passive to the loaded state) or when an object is being created for the first time.</span></span>

<span data-ttu-id="d380c-107">Intern handelt es sich bei der Instanziierung um einen zweistufigen Prozess.</span><span class="sxs-lookup"><span data-stu-id="d380c-107">Internally, instantiation is a two-phase process.</span></span> <span data-ttu-id="d380c-108">Ein Objekt der entsprechenden Klasse wird erstellt, nach dem eine Methode für dieses Objekt aufgerufen wird, um die Initialisierung auszuführen und Zugriff auf die Daten des Objekts zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d380c-108">An object of the appropriate class is created, after which a method on that object is called to perform initialization and give access to the object's data.</span></span> <span data-ttu-id="d380c-109">Die Initialisierungs Methode wird in einer der unterstützten Schnittstellen des Objekts definiert.</span><span class="sxs-lookup"><span data-stu-id="d380c-109">The initialization method is defined in one of the object's supported interfaces.</span></span> <span data-ttu-id="d380c-110">Die jeweilige Initialisierungs Methode, die aufgerufen wird, hängt vom Kontext ab, in dem das Objekt instanziiert wird, und vom Speicherort der Initialisierungs Daten.</span><span class="sxs-lookup"><span data-stu-id="d380c-110">The particular initialization method called depends on the context in which the object is being instantiated and the location of the initialization data.</span></span>

 

 





---
description: Ein-Objekt besteht aus einem Standard Header und Objekt spezifischen Attributen. Da alle Objekte dieselbe Struktur aufweisen, gibt es einen einzelnen Objekt-Manager in Windows, der alle Objekte verwaltet.
ms.assetid: 104113f3-bfd1-4ff7-b92f-2f753c0f5185
title: Objekt-Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3a74581650828a77c6423825d3c557a13075a89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960243"
---
# <a name="object-manager"></a><span data-ttu-id="dc482-104">Objekt-Manager</span><span class="sxs-lookup"><span data-stu-id="dc482-104">Object Manager</span></span>

<span data-ttu-id="dc482-105">Ein-Objekt besteht aus einem Standard Header und Objekt spezifischen Attributen.</span><span class="sxs-lookup"><span data-stu-id="dc482-105">An object consists of a standard header and object-specific attributes.</span></span> <span data-ttu-id="dc482-106">Da alle Objekte dieselbe Struktur aufweisen, gibt es einen einzelnen Objekt-Manager in Windows, der alle Objekte verwaltet.</span><span class="sxs-lookup"><span data-stu-id="dc482-106">Because all objects have the same structure, there is a single object manager in Windows that maintains all objects.</span></span>

<span data-ttu-id="dc482-107">Der Objekt Header enthält Elemente, wie z. b. den Objektnamen, sodass andere Prozesse anhand des Namens und einer Sicherheits Beschreibung auf das Objekt verweisen können, sodass der Objekt-Manager steuern kann, welche Prozesse auf die System Ressource zugreifen.</span><span class="sxs-lookup"><span data-stu-id="dc482-107">The object header includes items such as the object name, so that other processes can reference the object by name, and a security descriptor, so that the object manager can control which processes access the system resource.</span></span>

<span data-ttu-id="dc482-108">Die Aufgaben, die der Objekt-Manager ausführt, umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="dc482-108">The tasks that the object manager performs include the following:</span></span>

-   <span data-ttu-id="dc482-109">Erstellen von Objekten</span><span class="sxs-lookup"><span data-stu-id="dc482-109">Creating objects</span></span>
-   <span data-ttu-id="dc482-110">Überprüfen, ob ein Prozess über das Recht zur Verwendung des Objekts verfügt</span><span class="sxs-lookup"><span data-stu-id="dc482-110">Verifying that a process has the right to use the object</span></span>
-   <span data-ttu-id="dc482-111">Erstellen von Objekt Handles und Zurückgeben dieser Objekte an den Aufrufer</span><span class="sxs-lookup"><span data-stu-id="dc482-111">Creating object handles and returning them to the caller</span></span>
-   <span data-ttu-id="dc482-112">Verwalten von Ressourcen Kontingente</span><span class="sxs-lookup"><span data-stu-id="dc482-112">Maintaining resource quotas</span></span>
-   <span data-ttu-id="dc482-113">Erstellen von doppelten Handles</span><span class="sxs-lookup"><span data-stu-id="dc482-113">Creating duplicate handles</span></span>
-   <span data-ttu-id="dc482-114">Schließen von Handles in Objekte</span><span class="sxs-lookup"><span data-stu-id="dc482-114">Closing handles to objects</span></span>

 

 




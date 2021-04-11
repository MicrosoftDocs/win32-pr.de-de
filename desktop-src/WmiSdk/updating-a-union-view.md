---
description: Sie können die Werte der nicht Schlüsseleigenschaften von Union-Ansichts Klassen Instanzen aktualisieren. Die Änderungen, die Sie an der Instanz der Ansichts Klasse vornehmen, werden zurück an die Quell Klassen Instanzen weitergegeben, die die Union-Ansichts Klasse bilden.
ms.assetid: 375c9bc8-9f7b-42b4-a841-cf6af88887de
ms.tgt_platform: multiple
title: Aktualisieren einer Union-Ansicht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b051147ab40aacbf9032c5a0998d5894148985c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130960"
---
# <a name="updating-a-union-view"></a><span data-ttu-id="5f660-104">Aktualisieren einer Union-Ansicht</span><span class="sxs-lookup"><span data-stu-id="5f660-104">Updating a Union View</span></span>

<span data-ttu-id="5f660-105">Sie können die Werte der nicht Schlüsseleigenschaften von Union-Ansichts Klassen Instanzen aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="5f660-105">You can update the values of nonkey properties of union view class instances.</span></span> <span data-ttu-id="5f660-106">Die Änderungen, die Sie an der Instanz der Ansichts Klasse vornehmen, werden zurück an die Quell Klassen Instanzen weitergegeben, die die Union-Ansichts Klasse bilden.</span><span class="sxs-lookup"><span data-stu-id="5f660-106">The changes you make to the view class instance will be propagated back to the source class instances that form the union view class.</span></span>

<span data-ttu-id="5f660-107">Die folgenden Einschränkungen gelten für Änderungen von Ansichts Klassen Instanzen:</span><span class="sxs-lookup"><span data-stu-id="5f660-107">The following restrictions apply to changes to view class instances:</span></span>

-   <span data-ttu-id="5f660-108">Es können keine neuen Instanzen von Ansichts Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="5f660-108">You cannot create new instances of view classes.</span></span>
-   <span data-ttu-id="5f660-109">Updates werden nur von Union-Klassen unterstützt. Verknüpfungs-und Zuordnungs Sichten erstellen schreibgeschützte Ansichts Instanzen.</span><span class="sxs-lookup"><span data-stu-id="5f660-109">Only union classes support updates; join and association views create read-only view instances.</span></span>
-   <span data-ttu-id="5f660-110">Der Erfolg eines Updates hängt davon ab, ob eine Quell Instanz aktualisierbar ist.</span><span class="sxs-lookup"><span data-stu-id="5f660-110">Success of an update depends on whether a source instance is updateable.</span></span> <span data-ttu-id="5f660-111">Wenn eine Ansichts Instanzeigenschaft einer schreibgeschützten Eigenschaft einer Quell Instanz zugeordnet ist, tritt beim Versuch, die Ansichts Eigenschaft zu ändern, ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="5f660-111">If a view instance property maps to a read-only property of a source instance, attempts to modify the view property fail.</span></span>

 

 




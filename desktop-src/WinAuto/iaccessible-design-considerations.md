---
title: Überlegungen zum Entwurf von IAccessible
description: In diesem Abschnitt werden die Probleme erläutert, die Server Entwickler beim Entwerfen von Klassen basierend auf der IAccessible-Schnittstelle haben.
ms.assetid: 240cdff1-a4c3-477a-b146-2ac295d7a148
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ebb8648bd0398117f1d3da895ff4b4288aa5e7c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310320"
---
# <a name="iaccessible-design-considerations"></a><span data-ttu-id="d4fe7-103">Überlegungen zum Entwurf von IAccessible</span><span class="sxs-lookup"><span data-stu-id="d4fe7-103">IAccessible Design Considerations</span></span>

<span data-ttu-id="d4fe7-104">In diesem Abschnitt werden die Probleme erläutert, die Server Entwickler beim Entwerfen von Klassen basierend auf der [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle haben.</span><span class="sxs-lookup"><span data-stu-id="d4fe7-104">This section discusses the issues that server developer face when designing classes based on the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d4fe7-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="d4fe7-105">In this section</span></span>

-   [<span data-ttu-id="d4fe7-106">Auswählen, wann barrierefreie Objekte erstellt werden sollen</span><span class="sxs-lookup"><span data-stu-id="d4fe7-106">Choosing When to Create Accessible Objects</span></span>](choosing-when-to-create-accessible-objects.md)
-   [<span data-ttu-id="d4fe7-107">Auswählen der zu unterstützten Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d4fe7-107">Choosing Which Properties to Support</span></span>](choosing-which-properties-to-support.md)
-   [<span data-ttu-id="d4fe7-108">Auswählen des Inhalts für beschreibende Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d4fe7-108">Choosing the Content for Descriptive Properties</span></span>](choosing-the-content-for-descriptive-properties.md)
-   [<span data-ttu-id="d4fe7-109">Festlegen von Eigenschaften für animierte oder verschiebenden Objekten</span><span class="sxs-lookup"><span data-stu-id="d4fe7-109">Setting Properties for Animated or Moving Objects</span></span>](setting-properties-for-animated-or-moving-objects.md)
-   [<span data-ttu-id="d4fe7-110">Erstellen geeigneter WinEvents</span><span class="sxs-lookup"><span data-stu-id="d4fe7-110">Generating Appropriate WinEvents</span></span>](generating-appropriate-winevents.md)
-   [<span data-ttu-id="d4fe7-111">Verfügbar machen zusätzlicher Informationen, die nicht von der IAccessible-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="d4fe7-111">Exposing Additional Information Not Covered by IAccessible Interface</span></span>](exposing-additional-information-not-covered-by-iaccessible-interface.md)

 

 





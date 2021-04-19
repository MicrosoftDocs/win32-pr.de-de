---
description: WMI-Anbieter sind in der Regel so konzipiert, dass Sie Informationen zu einem bestimmten verwalteten Objekt auf einem einzelnen Computer bereitstellen.
ms.assetid: 9f23d599-ac37-4bfb-a3dc-0cef67e68b05
ms.tgt_platform: multiple
title: Verknüpfen von Klassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89c36956d20d9390462577332e7ac7b644d4ffc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359503"
---
# <a name="linking-classes-together"></a><span data-ttu-id="404b5-103">Verknüpfen von Klassen</span><span class="sxs-lookup"><span data-stu-id="404b5-103">Linking Classes Together</span></span>

<span data-ttu-id="404b5-104">WMI-Anbieter sind in der Regel so konzipiert, dass Sie Informationen zu einem bestimmten verwalteten Objekt auf einem einzelnen Computer bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="404b5-104">WMI providers are usually designed to provide information about a specific managed object on a single computer.</span></span> <span data-ttu-id="404b5-105">Wenn eine gemeinsame Eigenschaft vorhanden ist, die als Schlüssel zur eindeutigen Identifizierung aller verschiedenen Quell Instanzen dienen kann, verwenden Sie den [Ansichts Anbieter](view-provider.md) , um Eigenschaften aus unterschiedlichen Klassen, Namespaces oder Computern zu einer einzigen Klasse zu kombinieren.</span><span class="sxs-lookup"><span data-stu-id="404b5-105">If there is a common property that can serve as a key to uniquely identify all the different source instances, then use the [View Provider](view-provider.md) to combine properties from different classes, namespaces, or computers into a single class.</span></span>

<span data-ttu-id="404b5-106">Sie müssen [den Ansichts Anbieter zunächst registrieren](registering-the-view-provider.md).</span><span class="sxs-lookup"><span data-stu-id="404b5-106">You must first [register the View Provider](registering-the-view-provider.md).</span></span> <span data-ttu-id="404b5-107">Nach der Registrierung können Sie die folgenden Typen von Ansichts Klassen erstellen:</span><span class="sxs-lookup"><span data-stu-id="404b5-107">After registration, you can create the following types of view classes:</span></span>

-   [<span data-ttu-id="404b5-108">Joinansicht</span><span class="sxs-lookup"><span data-stu-id="404b5-108">Join view</span></span>](creating-a-new-instance-from-old-properties.md)

    <span data-ttu-id="404b5-109">Instanzen von verschiedenen Klassen, die durch einen allgemeinen Eigenschafts Wert verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="404b5-109">Instances of different classes connected by a common property value.</span></span>

-   [<span data-ttu-id="404b5-110">Zuordnungs Ansicht</span><span class="sxs-lookup"><span data-stu-id="404b5-110">Association view</span></span>](associating-instances-between-namespaces.md)

    <span data-ttu-id="404b5-111">Sichten vorhandener Zuordnungs Klassen über der Namespace Grenze hinweg.</span><span class="sxs-lookup"><span data-stu-id="404b5-111">Views of existing association classes across the namespace boundary.</span></span>

-   [<span data-ttu-id="404b5-112">Union-Ansicht</span><span class="sxs-lookup"><span data-stu-id="404b5-112">Union view</span></span>](creating-a-union-view-class.md)

    <span data-ttu-id="404b5-113">Union von einer oder mehreren-Instanzen.</span><span class="sxs-lookup"><span data-stu-id="404b5-113">Union of one or more instances.</span></span>

 

 




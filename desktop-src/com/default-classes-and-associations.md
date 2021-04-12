---
title: Standardklassen und-Zuordnungen
description: Für bestimmte Kategorien kann eine einzelne Klasse als Standardklasse zugeordnet werden.
ms.assetid: 9c48615b-ab10-44e4-a032-49d5ee0c9b01
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 871c537535c57da0809effbe3ee8ec086a88fd5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104387981"
---
# <a name="default-classes-and-associations"></a><span data-ttu-id="566a3-103">Standardklassen und-Zuordnungen</span><span class="sxs-lookup"><span data-stu-id="566a3-103">Default Classes and Associations</span></span>

<span data-ttu-id="566a3-104">Für bestimmte Kategorien kann eine einzelne Klasse als Standardklasse zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="566a3-104">For certain categories, a single class can be associated as the default class.</span></span> <span data-ttu-id="566a3-105">Die Standardklasse wird immer dann ausgewählt, wenn eine bestimmte Objekt Kategorie erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="566a3-105">The default class is selected whenever that particular category of object is required.</span></span> <span data-ttu-id="566a3-106">Obwohl dies für alle Komponenten Kategorien nicht nützlich sein kann, kann das Einrichten einer Standardklasse hilfreich sein, wenn eine bestimmte Klasse aus einer Liste möglicher Klassen geladen werden muss, ohne dass ein Benutzereingriff erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="566a3-106">While this may not be useful for all component categories, establishing a default class can be helpful when a particular class must be loaded from a list of possible classes without user intervention.</span></span> <span data-ttu-id="566a3-107">Administratoren definieren, welche Klasse durch die Bearbeitung der Registrierung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="566a3-107">Administrators define which class can be used by manipulating the registry.</span></span>

<span data-ttu-id="566a3-108">Um einer Kategorie eine Standardklasse zuzuordnen, führen Sie einen CLSID-Schlüssel mit der gleichen CLSID wie die CATID der als Standard ausgewählten Komponenten Kategorie ein.</span><span class="sxs-lookup"><span data-stu-id="566a3-108">To associate a default class with a category, introduce a CLSID key with the same CLSID as the CATID of the component category chosen as the default.</span></span> <span data-ttu-id="566a3-109">Fügen Sie diesem Schlüssel dann einen TreatAs-Schlüssel mit dem Wert für die CLSID der Standardklasse für die Kategorie hinzu.</span><span class="sxs-lookup"><span data-stu-id="566a3-109">Then add a TreatAs key to this key, using the value for the CLSID of the default class for the category.</span></span> <span data-ttu-id="566a3-110">Um die Standardklasse für eine Komponenten Kategorie zu verwenden, verwenden Sie [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) oder [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), wobei Sie die CATID für den CLSID-Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="566a3-110">To use the default class for a component category, use [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) or [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), specifying the CATID for the CLSID parameter.</span></span> <span data-ttu-id="566a3-111">Dadurch wird automatisch zur CLSID umgeleitet, die als Standard für diese Kategorie festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="566a3-111">This automatically redirects to the CLSID established as the default for this category.</span></span> <span data-ttu-id="566a3-112">Der Registrierungs Eintrag lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="566a3-112">The registry entry is as follows:</span></span>

```
HKEY_CLASSES_ROOT\CLSID
   {catid}
      TreatAs
          = default clsid
```

<span data-ttu-id="566a3-113">Während der Installation kann eine Komponente überprüfen, ob alle Standardklassen Schlüssel für Ihre Kategorien vorhanden sind, und den Benutzern Optionen zum Überschreiben der aktuellen Einstellungen präsentieren.</span><span class="sxs-lookup"><span data-stu-id="566a3-113">During installation, a component can check for the existence of any default class keys for its categories and present the user with options for overriding the current settings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="566a3-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="566a3-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="566a3-115">Zuordnen von Symbolen zu einer Kategorie</span><span class="sxs-lookup"><span data-stu-id="566a3-115">Associating Icons with a Category</span></span>](associating-icons-with-a-category.md)
</dt> <dt>

[<span data-ttu-id="566a3-116">Kategorisierung nach Komponenten Funktionen</span><span class="sxs-lookup"><span data-stu-id="566a3-116">Categorizing by Component Capabilities</span></span>](categorizing-by-component-capabilities.md)
</dt> <dt>

[<span data-ttu-id="566a3-117">Kategorisierung nach Container Funktionen</span><span class="sxs-lookup"><span data-stu-id="566a3-117">Categorizing by Container Capabilities</span></span>](categorizing-by-container-capabilities.md)
</dt> <dt>

[<span data-ttu-id="566a3-118">Definieren von Komponenten Kategorien</span><span class="sxs-lookup"><span data-stu-id="566a3-118">Defining Component Categories</span></span>](defining-component-categories.md)
</dt> <dt>

[<span data-ttu-id="566a3-119">Der Komponenten Kategorien-Manager</span><span class="sxs-lookup"><span data-stu-id="566a3-119">The Component Categories Manager</span></span>](the-component-categories-manager.md)
</dt> </dl>

 

 





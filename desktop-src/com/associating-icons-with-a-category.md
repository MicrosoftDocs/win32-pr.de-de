---
title: Zuordnen von Symbolen zu einer Kategorie
description: Zuordnen von Symbolen zu einer Kategorie
ms.assetid: 5e5c3c10-07cf-4a34-9822-97ec940b3117
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98c7a662ab3aaf578f037ff246207d03e4fcd688
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036489"
---
# <a name="associating-icons-with-a-category"></a><span data-ttu-id="3a6d5-103">Zuordnen von Symbolen zu einer Kategorie</span><span class="sxs-lookup"><span data-stu-id="3a6d5-103">Associating Icons with a Category</span></span>

<span data-ttu-id="3a6d5-104">Das Entwickeln einer Benutzeroberfläche, die es dem Benutzer ermöglicht, Komponenten Kategorien innerhalb einer Kategorie auszuwählen, erfordert die Möglichkeit, ein aussagekräftiges Bild für eine bestimmte Kategorie anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="3a6d5-104">Building a user interface that allows the user to select component categories within a category requires the ability to display a meaningful image for a particular category.</span></span> <span data-ttu-id="3a6d5-105">Wenn Sie ein Symbol einer Komponenten Kategorie zuordnen möchten, erstellen Sie einen Schlüssel für die CATID der Kategorie, und füllen Sie den Schlüssel mit einem [DefaultIcon](defaulticon.md) -Unterschlüssel auf.</span><span class="sxs-lookup"><span data-stu-id="3a6d5-105">To associate an icon with a component category, create a key for the category's CATID and populate that key with a [DefaultIcon](defaulticon.md) subkey.</span></span> <span data-ttu-id="3a6d5-106">Der Registrierungs Eintrag lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3a6d5-106">The registry entry is as follows:</span></span>

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...catid...}\DefaultIcon = "c:\hello\icons.dll,1"
 
```

<span data-ttu-id="3a6d5-107">Der Dateiname, auf den der DefaultIcon-Schlüssel verweist, kann entweder eine exe-oder DLL-Datei (reine Ressourcen-DLL) sein.</span><span class="sxs-lookup"><span data-stu-id="3a6d5-107">The filename referenced by the DefaultIcon key can be either an EXE or a DLL file (resource-only DLL).</span></span>

<span data-ttu-id="3a6d5-108">Um einer Komponenten Kategorie eine kleine 16x16-"Toolbox Bitmap" zuzuordnen, erstellen Sie einen Schlüssel in der **HKEY-Klassen Stamm- \_ \_ \\ CLSID** für die CATID der Kategorie und füllen den Schlüssel mit einem [ToolBoxBitmap32](toolboxbitmap32.md) -Unterschlüssel auf, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="3a6d5-108">To associate a small 16x16 "toolbox bitmap" with a component category, create a key in **HKEY\_CLASSES\_ROOT\\CLSID** for the category's CATID and populate that key with a [ToolBoxBitmap32](toolboxbitmap32.md) subkey, as shown in the following example:</span></span>

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...catid...}\ToolBoxBitmap32 = "c:\goodbye\mycomponent.dll,42"
 
```

<span data-ttu-id="3a6d5-109">Der Dateiname, auf den der [ToolBoxBitmap32](toolboxbitmap32.md) -Schlüssel verweist, kann auch eine exe-oder DLL-Datei (reine Ressourcen-DLL) sein.</span><span class="sxs-lookup"><span data-stu-id="3a6d5-109">The filename referenced by the [ToolBoxBitmap32](toolboxbitmap32.md) key can also be an EXE or DLL file (resource-only DLL).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3a6d5-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3a6d5-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a6d5-111">Kategorisierung nach Komponenten Funktionen</span><span class="sxs-lookup"><span data-stu-id="3a6d5-111">Categorizing by Component Capabilities</span></span>](categorizing-by-component-capabilities.md)
</dt> <dt>

[<span data-ttu-id="3a6d5-112">Kategorisierung nach Container Funktionen</span><span class="sxs-lookup"><span data-stu-id="3a6d5-112">Categorizing by Container Capabilities</span></span>](categorizing-by-container-capabilities.md)
</dt> <dt>

[<span data-ttu-id="3a6d5-113">Standardklassen und-Zuordnungen</span><span class="sxs-lookup"><span data-stu-id="3a6d5-113">Default Classes and Associations</span></span>](default-classes-and-associations.md)
</dt> <dt>

[<span data-ttu-id="3a6d5-114">Definieren von Komponenten Kategorien</span><span class="sxs-lookup"><span data-stu-id="3a6d5-114">Defining Component Categories</span></span>](defining-component-categories.md)
</dt> <dt>

[<span data-ttu-id="3a6d5-115">**Ialisierungsinformationen**</span><span class="sxs-lookup"><span data-stu-id="3a6d5-115">**ICatInformation**</span></span>](/windows/desktop/api/ComCat/nn-comcat-icatinformation)
</dt> <dt>

[<span data-ttu-id="3a6d5-116">**I-Register**</span><span class="sxs-lookup"><span data-stu-id="3a6d5-116">**ICatRegister**</span></span>](/windows/desktop/api/ComCat/nn-comcat-icatregister)
</dt> <dt>

[<span data-ttu-id="3a6d5-117">Der Komponenten Kategorien-Manager</span><span class="sxs-lookup"><span data-stu-id="3a6d5-117">The Component Categories Manager</span></span>](the-component-categories-manager.md)
</dt> </dl>

 

 





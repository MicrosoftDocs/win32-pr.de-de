---
description: Nachdem Sie den Suchergebnis Modus, den Durchsuchenmodus und die Layoutmuster verstanden haben, können Sie eine benutzerdefinierte Eigenschaften Liste für den Dateityp registrieren. Führen Sie diese Schritte aus, um eine benutzerdefinierte Eigenschaften Liste und ein Layoutmuster für den Dateityp zu registrieren.
ms.assetid: 29B863B3-E5FD-4E0A-B76B-4AFE5A6A76E3
title: Registrieren von benutzerdefinierten Eigenschaften und Layouts für den Dateityp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da55d0a90d4dd0f3ca109a3ca9f628a3c0912520
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994662"
---
# <a name="how-to-register-custom-properties-and-layout-for-your-file-type"></a><span data-ttu-id="c358f-103">Registrieren von benutzerdefinierten Eigenschaften und Layouts für den Dateityp</span><span class="sxs-lookup"><span data-stu-id="c358f-103">How to Register Custom Properties and Layout for Your File Type</span></span>

<span data-ttu-id="c358f-104">Nachdem Sie den Suchergebnis Modus, den Durchsuchenmodus und die Layoutmuster verstanden haben, können Sie eine benutzerdefinierte Eigenschaften Liste für den Dateityp registrieren.</span><span class="sxs-lookup"><span data-stu-id="c358f-104">After you understand the Search Result mode, the Browse mode, and the layout patterns, you can register a custom property list for your file type.</span></span>

<span data-ttu-id="c358f-105">Führen Sie diese Schritte aus, um eine benutzerdefinierte Eigenschaften Liste und ein Layoutmuster für den Dateityp zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="c358f-105">To register a custom property list and layout pattern for your file type, follow these steps.</span></span>

## <a name="instructions"></a><span data-ttu-id="c358f-106">Instructions</span><span class="sxs-lookup"><span data-stu-id="c358f-106">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="c358f-107">Schritt 1:</span><span class="sxs-lookup"><span data-stu-id="c358f-107">Step 1:</span></span>

<span data-ttu-id="c358f-108">Wählen Sie aus den vier layoutmustern: Alpha, Beta, Gamma oder Delta.</span><span class="sxs-lookup"><span data-stu-id="c358f-108">Choose from the four layout patterns: Alpha, Beta, Gamma, or Delta.</span></span>

### <a name="step-2"></a><span data-ttu-id="c358f-109">Schritt 2:</span><span class="sxs-lookup"><span data-stu-id="c358f-109">Step 2:</span></span>

<span data-ttu-id="c358f-110">Berücksichtigen Sie die folgenden Formatierungs Regeln, die gleichermaßen für alle vier Layoutmuster gelten:</span><span class="sxs-lookup"><span data-stu-id="c358f-110">Consider the following formatting rules, which apply equally to all four layout patterns:</span></span>

-   <span data-ttu-id="c358f-111">Eigenschaft 1 wird immer in einer größeren Schriftgröße angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c358f-111">Property 1 is always displayed in a larger font size.</span></span> <span data-ttu-id="c358f-112">Der Umfang der großen Schriftart, der in der Regel für den Elementnamen verwendet wird, aber auch für den Anker oder eine andere Element Eigenschaft verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c358f-112">The large font size usually used for the item name, but can also be used for the anchor or other item property.</span></span>
-   <span data-ttu-id="c358f-113">Eigenschaft 4 ist für Ausschnitte in den Alpha-, Beta-und Gamma layoutmustern vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="c358f-113">Property 4 is intended for excerpts in the Alpha, Beta, and Gamma layout patterns.</span></span> <span data-ttu-id="c358f-114">Dieser Eigenschaft wird mehr Platz in diesen Mustern zugewiesen, und Sie wird in einer grauen Schriftfarbe angezeigt, im Gegensatz zu den anderen Eigenschaften, um Sie zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c358f-114">This property is allotted more space in those patterns and is displayed in a gray font color, as opposed to black like the other properties, to help it stand out.</span></span>
-   <span data-ttu-id="c358f-115">Die unten angegebenen Pixel Messungen liegen in relativen Pixeln vor, und die Größe enthält das Symbol/die Miniaturansicht links neben den Eigenschaften und das Leerzeichen zwischen Symbol/Miniaturansicht und Auswahl Rechteck.</span><span class="sxs-lookup"><span data-stu-id="c358f-115">The pixel measurements below are in relative pixels, and the size includes the icon/thumbnail to the left of the properties and the space between the icon/thumbnail and the selection rectangle.</span></span>
-   <span data-ttu-id="c358f-116">Die meisten Eigenschaften verfügen über eine minimale Anzeige Größe.</span><span class="sxs-lookup"><span data-stu-id="c358f-116">Most properties have a minimum display size.</span></span> <span data-ttu-id="c358f-117">Aus diesem Grund werden Sie nicht angezeigt, wenn auf einer bestimmten Ansichts Größe nicht genügend Speicherplatz vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c358f-117">Therefore, they will not appear if there is not enough space for them at a particular view size.</span></span> <span data-ttu-id="c358f-118">Die minimale Größe ist normalerweise 100 Pixel breit.</span><span class="sxs-lookup"><span data-stu-id="c358f-118">The minimum size is usually 100 pixels wide.</span></span>
-   <span data-ttu-id="c358f-119">Jedes Layoutmuster definiert die Anzahl der Zeilen und die Anzahl der Eigenschaften in jeder Zeile.</span><span class="sxs-lookup"><span data-stu-id="c358f-119">Each layout pattern defines the number of rows and the number of properties in each row.</span></span>

### <a name="step-3"></a><span data-ttu-id="c358f-120">Schritt 3:</span><span class="sxs-lookup"><span data-stu-id="c358f-120">Step 3:</span></span>

<span data-ttu-id="c358f-121">Entscheiden Sie, welche Eigenschaften im Layout angezeigt werden sollen und welche Eigenschaft Sie an jedem Speicherort anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="c358f-121">Decide which properties you want to display in the layout, and which property you want to display in each location.</span></span> <span data-ttu-id="c358f-122">Berücksichtigen Sie bei der Entscheidung, welche Eigenschaft an jeder Position im Layout angezeigt werden soll, die typische Länge der Eigenschaft, ihre Wichtigkeit für den Benutzer und ob Sie gelöscht werden soll, wenn die Fenstergröße zu klein ist, um alle Eigenschaften zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="c358f-122">When deciding which property to display in each position in the layout, consider the typical length of the property, its importance to the user, and whether it should be dropped when the window size is too small to contain all properties.</span></span>

### <a name="step-4"></a><span data-ttu-id="c358f-123">Schritt 4:</span><span class="sxs-lookup"><span data-stu-id="c358f-123">Step 4:</span></span>

<span data-ttu-id="c358f-124">Registrieren Sie ein Layoutmuster und eine Eigenschaften Liste für Ihren Dateityp oder Elementtyp, indem Sie die folgenden Schlüssel unter dem ProgID-Registrierungsschlüssel für den Dateityp oder das Element hinzufügen (in diesem Beispiel für den Dateityp ". xyz").</span><span class="sxs-lookup"><span data-stu-id="c358f-124">Register a layout pattern and a property list for your file type or item type by adding the following keys under the ProgID registry key for the file type or item (in this example, for the .xyz file type).</span></span>

```
HKEY_CLASSES_ROOT\*
   Contoso.xyzfile
      (ContentViewModeForBrowse) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
      (ContentViewModeForSearch) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
      (ContentViewModeLayoutPatternForBrowse) = <PropertyList>
      (ContentViewModeLayoutPatternForSearch) = <PropertyList>
```

### <a name="step-5"></a><span data-ttu-id="c358f-125">Schritt 5:</span><span class="sxs-lookup"><span data-stu-id="c358f-125">Step 5:</span></span>

<span data-ttu-id="c358f-126">Beachten Sie die folgenden Formatierungs Richtlinien zum Registrieren von Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="c358f-126">Observe the following formatting guidelines for registering properties:</span></span>

-   <span data-ttu-id="c358f-127">Jede Registrierung beginnt mit `prop:`</span><span class="sxs-lookup"><span data-stu-id="c358f-127">Each registration starts with `prop:`</span></span>
-   <span data-ttu-id="c358f-128">Jede Eigenschaft erfordert den vollständigen Eigenschaftsnamen.</span><span class="sxs-lookup"><span data-stu-id="c358f-128">Each property requires the full property name.</span></span>
-   <span data-ttu-id="c358f-129">Eigenschaften werden durch ein Semikolon ohne Leerzeichen voneinander getrennt.</span><span class="sxs-lookup"><span data-stu-id="c358f-129">Properties are separated by a semicolon with no space.</span></span>
-   <span data-ttu-id="c358f-130">Eigenschaften werden in der Reihenfolge angezeigt, in der das ausgewählte Layoutmuster definiert ist.</span><span class="sxs-lookup"><span data-stu-id="c358f-130">Properties are displayed in the order defined by the selected layout pattern.</span></span>
-   <span data-ttu-id="c358f-131">`~` Gibt an, dass die Eigenschaften Bezeichnung nicht angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c358f-131">`~` indicates that the property label should not be displayed.</span></span>
-   <span data-ttu-id="c358f-132">`~System.LayoutPattern.PlaceHolder` sollte verwendet werden, wenn Sie eine im Layoutmuster angegebene Eigenschaft leer lassen möchten.</span><span class="sxs-lookup"><span data-stu-id="c358f-132">`~System.LayoutPattern.PlaceHolder` should be used if you want to leave blank a property that is specified in the layout pattern.</span></span>

<span data-ttu-id="c358f-133">Der folgende Beispiel Registrierungsschlüssel veranschaulicht diese Formatierungs Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="c358f-133">The following sample registry key illustrates these formatting guidelines.</span></span>

```
HKEY_CLASSES_ROOT\
   Kind.Document
      (ContentViewModeForBrowse) = <PropertyList>
```

<span data-ttu-id="c358f-134">Mögliche Werte für (contentviewmodeforbrowse) umfassen Folgendes: `prop:~System.ItemNameDisplay;System.Author;System.LayoutPattern.Placeholder;System.Keywords;System.DateModified;~System.Size`</span><span class="sxs-lookup"><span data-stu-id="c358f-134">Possible values for (ContentViewModeForBrowse) include the following: `prop:~System.ItemNameDisplay;System.Author;System.LayoutPattern.Placeholder;System.Keywords;System.DateModified;~System.Size`</span></span>

 

 




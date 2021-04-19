---
description: Erstellen einer Filter Eigenschaften Seite
ms.assetid: 028e2c4e-0241-4057-8514-d3e9b456ab6e
title: Erstellen einer Filter Eigenschaften Seite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cc19bf918ba47c53a04e34f5e5292bfdc716eca
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346397"
---
# <a name="creating-a-filter-property-page"></a><span data-ttu-id="89e0c-103">Erstellen einer Filter Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="89e0c-103">Creating a Filter Property Page</span></span>

<span data-ttu-id="89e0c-104">In diesem Abschnitt wird beschrieben, wie eine Eigenschaften Seite für einen benutzerdefinierten DirectShow-Filter mithilfe der [**cbasepropertypage**](cbasepropertypage.md) -Klasse erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="89e0c-104">This section describes how to create a property page for a custom DirectShow filter, using the [**CBasePropertyPage**](cbasepropertypage.md) class.</span></span> <span data-ttu-id="89e0c-105">Der Beispielcode in diesem Abschnitt zeigt alle Schritte, die erforderlich sind, um eine Eigenschaften Seite zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="89e0c-105">The example code in this section shows all the steps needed to create a property page.</span></span> <span data-ttu-id="89e0c-106">Das Beispiel zeigt eine Eigenschaften Seite für einen hypothetischen Videoeffekt Filter, der eine Sättigung-Eigenschaft unterstützt.</span><span class="sxs-lookup"><span data-stu-id="89e0c-106">The example shows a property page for a hypothetical video effect filter that supports a saturation property.</span></span> <span data-ttu-id="89e0c-107">Die Eigenschaften Seite verfügt über einen Schieberegler, den der Benutzer verschieben kann, um den Sättigungsgrad des Filters anzupassen.</span><span class="sxs-lookup"><span data-stu-id="89e0c-107">The property page has a slider, which the user can move to adjust the filter's saturation level.</span></span>

<span data-ttu-id="89e0c-108">Dieser Abschnitt enthält die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="89e0c-108">This section contains the following topics:</span></span>

-   [<span data-ttu-id="89e0c-109">Schritt 1: Definieren eines Mechanismus zum Festlegen der Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="89e0c-109">Step 1. Define a Mechanism for Setting the Property</span></span>](step-1--define-a-mechanism-for-setting-the-property.md)
-   [<span data-ttu-id="89e0c-110">Schritt 2: Implementieren von ISpecifyPropertyPages</span><span class="sxs-lookup"><span data-stu-id="89e0c-110">Step 2. Implement ISpecifyPropertyPages</span></span>](step-2--implement-ispecifypropertypages.md)
-   [<span data-ttu-id="89e0c-111">Schritt 3. QueryInterface-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="89e0c-111">Step 3. Support QueryInterface</span></span>](step-3--support-queryinterface.md)
-   [<span data-ttu-id="89e0c-112">Schritt 4: Erstellen der Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="89e0c-112">Step 4. Create the Property Page</span></span>](step-4--create-the-property-page.md)
-   [<span data-ttu-id="89e0c-113">Schritt 5: Speichern eines Zeigers auf den Filter</span><span class="sxs-lookup"><span data-stu-id="89e0c-113">Step 5. Store a Pointer to the Filter</span></span>](step-5--store-a-pointer-to-the-filter.md)
-   [<span data-ttu-id="89e0c-114">Schritt 6: Initialisieren des Dialog Felds</span><span class="sxs-lookup"><span data-stu-id="89e0c-114">Step 6. Initialize the Dialog</span></span>](step-6--initialize-the-dialog.md)
-   [<span data-ttu-id="89e0c-115">Schritt 7: Fenster Meldungen behandeln</span><span class="sxs-lookup"><span data-stu-id="89e0c-115">Step 7. Handle Window Messages</span></span>](step-7--handle-window-messages.md)
-   [<span data-ttu-id="89e0c-116">Schritt 8. Anwenden von Eigenschafts Änderungen</span><span class="sxs-lookup"><span data-stu-id="89e0c-116">Step 8. Apply Property Changes</span></span>](step-8--apply-property-changes.md)
-   [<span data-ttu-id="89e0c-117">Schritt 9: Trennen der Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="89e0c-117">Step 9. Disconnect the Property Page</span></span>](step-9--disconnect-the-property-page.md)
-   [<span data-ttu-id="89e0c-118">Schritt 10. COM-Registrierung unterstützen</span><span class="sxs-lookup"><span data-stu-id="89e0c-118">Step 10. Support COM Registration</span></span>](step-10--support-com-registration.md)

## <a name="related-topics"></a><span data-ttu-id="89e0c-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="89e0c-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89e0c-120">Schreiben von DirectShow-Filtern</span><span class="sxs-lookup"><span data-stu-id="89e0c-120">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 




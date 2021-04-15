---
title: Description-Eigenschaft (Windows-Barrierefreiheits Funktionen)
description: Die Description-Eigenschaft eines Objekts stellt eine Textbeschreibung zur visuellen Darstellung eines Objekts bereit.
ms.assetid: 1fe3221f-e1dd-44b2-b749-d00bee1b6b89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34320b2959899d049d959037c0f24299780b54b0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474979"
---
# <a name="description-property-windows-accessibility-features"></a><span data-ttu-id="206a9-103">Description-Eigenschaft (Windows-Barrierefreiheits Funktionen)</span><span class="sxs-lookup"><span data-stu-id="206a9-103">Description Property (Windows Accessibility features)</span></span>

> [!Note]  
> <span data-ttu-id="206a9-104">Die **Description** -Eigenschaft wird häufig falsch verwendet und wird nicht von der Microsoft-Benutzeroberflächen Automatisierung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="206a9-104">The **Description** property is often used incorrectly and is not supported by Microsoft UI Automation.</span></span> <span data-ttu-id="206a9-105">Microsoft Active Accessibility Server-Entwickler sollten diese Eigenschaft nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="206a9-105">Microsoft Active Accessibility server developers should not use this property.</span></span> <span data-ttu-id="206a9-106">Wenn weitere Informationen für Barrierefreiheits-und Automatisierungs Szenarien erforderlich sind, verwenden Sie die Eigenschaften, die von Benutzeroberflächenautomatisierungs-Elementen und Steuerelement Mustern unterstützt</span><span class="sxs-lookup"><span data-stu-id="206a9-106">If more information is needed for accessibility and automation scenarios, use the properties supported by UI Automation elements and control patterns.</span></span>

 

<span data-ttu-id="206a9-107">Die **Description** -Eigenschaft eines Objekts stellt eine Textbeschreibung zur visuellen Darstellung eines Objekts bereit.</span><span class="sxs-lookup"><span data-stu-id="206a9-107">An object's **Description** property provides a textual description about an object's visual appearance.</span></span> <span data-ttu-id="206a9-108">Die Beschreibung wird hauptsächlich verwendet, um einen größeren Kontext für sehorientierte oder Blind Benutzer bereitzustellen, wird jedoch auch für die Kontextsuche oder andere Anwendungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="206a9-108">The description is primarily used to provide greater context for low-vision or blind users, but is also used for context searching or other applications.</span></span> <span data-ttu-id="206a9-109">Mit dieser Eigenschaft können Benutzer ein Symbol oder die visuelle Darstellung in der Gesamtdarstellung verstehen.</span><span class="sxs-lookup"><span data-stu-id="206a9-109">This property can help users understand an icon or the overall visual appearance.</span></span>

<span data-ttu-id="206a9-110">Die **Description** -Eigenschaft wird durch Aufrufen von [**IAccessible:: get \_ accdescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)abgerufen.</span><span class="sxs-lookup"><span data-stu-id="206a9-110">The **Description** property is retrieved by calling [**IAccessible::get\_accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription).</span></span>

## <a name="when-to-support-the-description-property"></a><span data-ttu-id="206a9-111">Unterstützung der Description-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="206a9-111">When to Support the Description Property</span></span>

<span data-ttu-id="206a9-112">Server unterstützen die **Description** -Eigenschaft, wenn die Beschreibung nicht offensichtlich ist, oder wenn Sie auf der Grundlage der [**Eigenschaften Name**](name-property.md), [**Rolle**](role-property.md), [**Zustand**](state-property.md)und [**Wert**](value-property.md) des Objekts nicht redundant ist.</span><span class="sxs-lookup"><span data-stu-id="206a9-112">Servers support the **Description** property if the description is not obvious, or when it is not redundant based on the object's [**Name**](name-property.md), [**Role**](role-property.md), [**State**](state-property.md), and [**Value**](value-property.md) properties.</span></span> <span data-ttu-id="206a9-113">Eine Schaltfläche mit der Bezeichnung "OK" benötigt z. b. keine zusätzlichen Informationen, wohingegen eine Schaltfläche, die ein Bild eines Kakteen anzeigt, wäre.</span><span class="sxs-lookup"><span data-stu-id="206a9-113">For example, a button labeled "OK" would not need additional information, whereas a button that shows a picture of a cactus would.</span></span> <span data-ttu-id="206a9-114">Die Eigenschaften " **Name**", " **Role**" und " [**Help**](help-property.md) " für eine solche Schaltfläche beschreiben den Zweck, aber die **Description** -Eigenschaft vermittelt weniger spürbare Informationen. Beispiel: "diese Schaltfläche zeigt ein Bild eines Kakteen an."</span><span class="sxs-lookup"><span data-stu-id="206a9-114">The **Name**, **Role**, and [**Help**](help-property.md) properties for such a button describe its purpose, but the **Description** property conveys information that is less tangible; for example, "This button shows a picture of a cactus."</span></span>

<span data-ttu-id="206a9-115">Ein Microsoft Active Accessibility Server kann die Unterstützung für die Benutzeroberflächen Automatisierung mithilfe der [direkten Anmerkung](direct-annotation.md), mithilfe der [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Schnittstelle oder durch die parallele Implementierung von Microsoft Active Accessibility und UI-Automatisierung mit beiden Implementierungen hinzufügen, die die [**WM- \_ GetObject**](wm-getobject.md) -Nachricht verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="206a9-115">A Microsoft Active Accessibility server can add support for UI Automation by using [Direct Annotation](direct-annotation.md), using the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface, or by implementing Microsoft Active Accessibility and UI Automation side-by-side with both implementations handling the [**WM\_GETOBJECT**](wm-getobject.md) message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="206a9-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="206a9-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="206a9-117">Verwenden der direkten Anmerkung</span><span class="sxs-lookup"><span data-stu-id="206a9-117">Using Direct Annotation</span></span>](using-direct-annotation.md)
</dt> <dt>

[<span data-ttu-id="206a9-118">Die iaccessibleex-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="206a9-118">The IAccessibleEx Interface</span></span>](iaccessibleex.md)
</dt> </dl>

 

 





---
description: Abhängigkeiten zwischen Eigenschaften
ms.assetid: 1c7c7c76-ec27-4ee4-a860-24244843a1e5
title: Abhängigkeiten zwischen Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6df8015c3fc49e35f5079315f6c056f680ebcc12
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958420"
---
# <a name="interdependencies-between-properties"></a><span data-ttu-id="34598-103">Abhängigkeiten zwischen Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="34598-103">Interdependencies Between Properties</span></span>

<span data-ttu-id="34598-104">Wenn Sie Eigenschaften festlegen, erzwingt der com+-Katalog einige Konsistenz Logik, um sicherzustellen, dass Sie Elemente auf sinnvolle Weise konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="34598-104">When you set properties, the COM+ catalog enforces some coherency logic to ensure that you configure elements in a reasonable way.</span></span> <span data-ttu-id="34598-105">Diese Logik kann auf zwei Arten implementiert werden, wie im folgenden dargestellt:</span><span class="sxs-lookup"><span data-stu-id="34598-105">This logic can be implemented in two ways, as follows:</span></span>

-   <span data-ttu-id="34598-106">**Abhängigkeiten:**</span><span class="sxs-lookup"><span data-stu-id="34598-106">**Dependencies.**</span></span> <span data-ttu-id="34598-107">Sie werden möglicherweise daran gehindert, Änderungen vorzunehmen, weil eine andere Eigenschaft von einer bestimmten Einstellung für eine Eigenschaft abhängt, die Sie festlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="34598-107">You might be blocked from making some changes because another property depends on a particular setting for a property you attempt to set.</span></span> <span data-ttu-id="34598-108">Wenn eine Komponente z. b. mit den erforderlichen Attribut Transaktionen festgelegt ist und Sie dann versuchen, die Synchronisierungs Einstellung in keine zu ändern, wird beim Versuch, [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) aufzurufen, ein Fehler generiert, da die Transaktionen von der Synchronisierung abhängen.</span><span class="sxs-lookup"><span data-stu-id="34598-108">For example, if a component is set with the attribute Transactions Required and if you then attempt to change the Synchronization setting to None, an error is generated when you attempt to call [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) because transactions depend on synchronization.</span></span>
-   <span data-ttu-id="34598-109">**Nebeneffekte.**</span><span class="sxs-lookup"><span data-stu-id="34598-109">**Side effects.**</span></span> <span data-ttu-id="34598-110">Einige Eigenschaften werden möglicherweise geändert, ohne dass Sie explizit festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="34598-110">Some properties might be changed for you without your explicitly setting them.</span></span> <span data-ttu-id="34598-111">Wenn Sie z. b. eine Komponente mit den erforderlichen Attribut Transaktionen festgelegt haben, wird die Synchronisierung auch auf Required festgelegt.</span><span class="sxs-lookup"><span data-stu-id="34598-111">For example, if you set a component with the attribute Transactions Required, Synchronization will be set to Required as well.</span></span> <span data-ttu-id="34598-112">Dies ist wirklich die Kehrseite der Abhängigkeiten – eine Eigenschaft hat Vorrang vor einer anderen Eigenschaft, und ihre Abhängigkeit wird durch das erste Festlegen der sekundären Eigenschaft und das anschließende Blockieren von Änderungen an der Eigenschaft ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="34598-112">This is really the flip side of dependencies—one property takes precedence over another, and its dependency is expressed through first setting the secondary property and then blocking changes to it.</span></span>

<span data-ttu-id="34598-113">In der Liste der Eigenschaften, die von Elementen in einer Sammlung verfügbar gemacht werden und die in [com+-Administrations Sammlungen](com--administration-collections.md)aufgeführt sind, werden die Abhängigkeiten und Nebeneffekte für jede Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="34598-113">In the list of properties exposed by items in a collection, all listed in [COM+ Administration Collections](com--administration-collections.md), the dependencies and side effects are stated for each property.</span></span> <span data-ttu-id="34598-114">Wenn Sie com+-Anwendungen und-Komponenten konfigurieren, sollten Sie wissen, welche Einschränkungen für Konfigurationen gelten.</span><span class="sxs-lookup"><span data-stu-id="34598-114">When you configure COM+ applications and components, you should be aware of what constraints are imposed on configurations.</span></span>

## <a name="related-topics"></a><span data-ttu-id="34598-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="34598-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34598-116">Eigenschaften werden erhalten und festgelegt</span><span class="sxs-lookup"><span data-stu-id="34598-116">Getting and Setting Properties</span></span>](getting-and-setting-properties.md)
</dt> <dt>

[<span data-ttu-id="34598-117">Abfragen von verfügbaren Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="34598-117">Querying for Available Properties</span></span>](querying-for-available-properties.md)
</dt> <dt>

[<span data-ttu-id="34598-118">Speichern oder Verwerfen von Änderungen</span><span class="sxs-lookup"><span data-stu-id="34598-118">Saving or Discarding Changes</span></span>](saving-or-discarding-changes.md)
</dt> </dl>

 

 




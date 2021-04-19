---
description: Ressourcen, die für die Anpassung einer Anwendung benötigt werden, z. b. Unternehmens Vorlagen, können mit der Anwendung bereitgestellt werden, indem eine Transformation mit dem Installationspaket der Anwendung eingeschlossen wird.
ms.assetid: 3d9328d0-4d95-449c-bf2b-5487f7ba5971
title: Verwenden von Transformationen zum Hinzufügen von Ressourcen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c11fac7ad65601286fb550abd950bf5ac49af1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356175"
---
# <a name="using-transforms-to-add-resources"></a><span data-ttu-id="0e6df-103">Verwenden von Transformationen zum Hinzufügen von Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0e6df-103">Using Transforms to Add Resources</span></span>

<span data-ttu-id="0e6df-104">Ressourcen, die für die Anpassung einer Anwendung benötigt werden, z. b. Unternehmens Vorlagen, können mit der Anwendung bereitgestellt werden, indem eine Transformation mit dem Installationspaket der Anwendung eingeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="0e6df-104">Resources that are needed for the customization of an application, such as corporate templates, can be deployed with the application by including a transform with the application's installation package.</span></span> <span data-ttu-id="0e6df-105">Beim Bereitstellen von Ressourcen, wie z. b. Dateien, Registrierungs Schlüsseln oder Verknüpfungen, mithilfe einer Transformation müssen folgende Regeln befolgt werden.</span><span class="sxs-lookup"><span data-stu-id="0e6df-105">The following rules should be followed when deploying resources, such as files, registry keys, or shortcuts, using a transform.</span></span>

-   <span data-ttu-id="0e6df-106">Die Transformation sollte der Installations Datenbank eine oder mehrere neue Komponenten hinzufügen, um die zusätzlichen Ressourcen zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="0e6df-106">The transform should add one or more new components to the installation database to contain the additional resources.</span></span> <span data-ttu-id="0e6df-107">Die Transformation sollte einer Komponente, die bereits in der Installation vorhanden ist, keine Ressourcen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0e6df-107">The transform should not add resources to a component that already exists in the installation.</span></span>
-   <span data-ttu-id="0e6df-108">Die Transformation sollte der Installations Datenbank eine oder mehrere neue Funktionen hinzufügen, um diese neuen Komponenten zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="0e6df-108">The transform should add one or more new features to the installation database to contain these new components.</span></span> <span data-ttu-id="0e6df-109">Diese neuen Features sollten nicht die übergeordneten Elemente vorhandener Funktionen sein, aber es können auch neue über-und untergeordnete Funktionen integriert werden.</span><span class="sxs-lookup"><span data-stu-id="0e6df-109">These new features should not be the parents of any existing features, but new parent and child features may be introduced together.</span></span> <span data-ttu-id="0e6df-110">Neuen Features sollten Namen zugewiesen werden, die für alle anderen Transformationen für dieses Produkt eindeutig sind.</span><span class="sxs-lookup"><span data-stu-id="0e6df-110">New features should be given names that are unique across all other transforms for this product.</span></span> <span data-ttu-id="0e6df-111">Zwei Transformationen sollten dem Produkt, das in der featurespalte der [Featuretabelle](feature-table.md) mit dem gleichen Namen aufgeführt ist und verschiedene Komponenten oder Ressourcen enthält, nie eine Funktion hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0e6df-111">No two transforms should ever add a feature to this product that has the same name listed in the Feature column of the [Feature table](feature-table.md) and containing different components or resources.</span></span>

 

 




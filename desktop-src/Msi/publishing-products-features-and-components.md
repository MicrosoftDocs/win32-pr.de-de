---
description: Verwenden Sie zum Veröffentlichen eines Produkts, einer Komponente oder eines Features eine der Veröffentlichungs Aktionen.
ms.assetid: 2c395d81-4f46-444e-a275-7a5d806e473c
title: Veröffentlichen von Produkten, Features und Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cdd8c8445491646399c7d118a69ae497d27faff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215905"
---
# <a name="publishing-products-features-and-components"></a><span data-ttu-id="865ee-103">Veröffentlichen von Produkten, Features und Komponenten</span><span class="sxs-lookup"><span data-stu-id="865ee-103">Publishing Products, Features, and Components</span></span>

<span data-ttu-id="865ee-104">Verwenden Sie zum [veröffentlichen](components-and-features.md) eines Produkts, einer Komponente oder eines Features eine der Veröffentlichungs Aktionen.</span><span class="sxs-lookup"><span data-stu-id="865ee-104">To [publish](components-and-features.md) a product, component, or feature, use one of the publishing actions.</span></span> <span data-ttu-id="865ee-105">Die [publishproduct-Aktion](publishproduct-action.md) registriert die Produktinformationen beim System.</span><span class="sxs-lookup"><span data-stu-id="865ee-105">The [PublishProduct action](publishproduct-action.md) registers the product information with the system.</span></span> <span data-ttu-id="865ee-106">Nachdem Sie die publishproduct-Aktion ausgeführt haben, veröffentlichen Sie die Komponenten mit der [PublishComponents-Aktion](publishcomponents-action.md), die wiederum die [PublishComponent-Tabelle](publishcomponent-table.md) verwendet, um die Komponenten zu ermitteln, die als angekündigt festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="865ee-106">After executing the PublishProduct action, publish the components with the [PublishComponents action](publishcomponents-action.md), which in turn uses the [PublishComponent table](publishcomponent-table.md) to determine the components that are set as advertised.</span></span> <span data-ttu-id="865ee-107">Zum Veröffentlichen auf featurebasis rufen Sie die [publishfeatures-Aktion](publishfeatures-action.md)auf.</span><span class="sxs-lookup"><span data-stu-id="865ee-107">To publish on a per-feature basis, invoke the [PublishFeatures action](publishfeatures-action.md).</span></span> <span data-ttu-id="865ee-108">Bei dieser Aktion wird die [FeatureComponents-Tabelle](featurecomponents-table.md) als Daten verwendet, um aufzulösen, welche Features angekündigt werden.</span><span class="sxs-lookup"><span data-stu-id="865ee-108">This action uses the [FeatureComponents table](featurecomponents-table.md) as data to resolve which features are advertised.</span></span>

<span data-ttu-id="865ee-109">Es gibt auch zwei Aktionen, die die Veröffentlichung eines Features oder einer Komponente aufheben: die [unpublishcomponents-Aktion](unpublishcomponents-action.md) und die [unpublishfeatures-Aktion](unpublishfeatures-action.md).</span><span class="sxs-lookup"><span data-stu-id="865ee-109">There are also two corresponding actions that unpublish a feature or a component: the [UnpublishComponents action](unpublishcomponents-action.md) and the [UnpublishFeatures action](unpublishfeatures-action.md).</span></span>

 

 




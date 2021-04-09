---
description: Im folgenden Verfahren wird ein Szenario zum Generieren einer Transformation beschrieben, die eine Funktion dauerhaft verbirgt.
ms.assetid: 43f36866-a9df-4035-a8ae-5ccbcb628a90
title: Erstellen einer Transformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0543ae74f71155e6fcd504ebee677558f21bbfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042541"
---
# <a name="generating-a-transform"></a><span data-ttu-id="7a645-103">Erstellen einer Transformation</span><span class="sxs-lookup"><span data-stu-id="7a645-103">Generating a Transform</span></span>

<span data-ttu-id="7a645-104">Im folgenden Verfahren wird ein Szenario zum Generieren einer Transformation beschrieben, die eine Funktion dauerhaft verbirgt.</span><span class="sxs-lookup"><span data-stu-id="7a645-104">The following procedure describes a scenario to generate a transform that permanently hides a feature.</span></span>

<span data-ttu-id="7a645-105">**So blenden Sie eine Produkt Funktion dauerhaft aus**</span><span class="sxs-lookup"><span data-stu-id="7a645-105">**To permanently hide a product feature**</span></span>

1.  <span data-ttu-id="7a645-106">Kopieren Sie das ursprüngliche Installationspaket.</span><span class="sxs-lookup"><span data-stu-id="7a645-106">Copy the original installation package.</span></span>
2.  <span data-ttu-id="7a645-107">Ändern Sie die Kopie, indem Sie den Wert der Anzeige Spalte in der [Featuretabelle](feature-table.md) auf NULL festlegen.</span><span class="sxs-lookup"><span data-stu-id="7a645-107">Alter the copy by setting the value of the Display column in the [Feature table](feature-table.md) to zero.</span></span> <span data-ttu-id="7a645-108">Dies gibt das Ausblenden des Features an.</span><span class="sxs-lookup"><span data-stu-id="7a645-108">This specifies hiding the feature.</span></span>
3.  <span data-ttu-id="7a645-109">Erstellen Sie eine Transformation vom ursprünglichen Installationspaket zu den neuen Installationspaketen, indem Sie [**msidatabasegeneratetransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7a645-109">Create a transform from the original installation package to the new installation packages by calling [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma).</span></span>
4.  <span data-ttu-id="7a645-110">Erstellen Sie die Zusammenfassungs Informationen in der Transformation, indem Sie [**msicreatetransformsummaryinfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7a645-110">Create the summary information in the transform by calling [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).</span></span>

<span data-ttu-id="7a645-111">Die Transformation kann dann während der Installation angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="7a645-111">The transform is then ready to be applied during installation.</span></span> <span data-ttu-id="7a645-112">Weitere Informationen finden Sie unter [Anwenden von Transformationen](applying-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="7a645-112">For more information, see [Applying Transforms](applying-transforms.md).</span></span>

 

 




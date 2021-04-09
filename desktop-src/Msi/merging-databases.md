---
description: Sie können das Installationsprogramm verwenden, um die Informationen in einer Datenbank in einer anderen Datenbank hinzuzufügen, indem Sie eine Zusammenführung ausführen.
ms.assetid: c53ef3d2-b3dc-4cd1-bd98-a856a223917f
title: Daten Bank Zusammenführung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8212355f37a12aa3b92bc10e6e3e41abdcf361dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960345"
---
# <a name="merging-databases"></a><span data-ttu-id="2b092-103">Daten Bank Zusammenführung</span><span class="sxs-lookup"><span data-stu-id="2b092-103">Merging Databases</span></span>

<span data-ttu-id="2b092-104">Sie können das Installationsprogramm verwenden, um die Informationen in einer Datenbank in einer anderen Datenbank hinzuzufügen, indem Sie eine Zusammenführung ausführen.</span><span class="sxs-lookup"><span data-stu-id="2b092-104">You can use the installer to add the information in one database into another database by performing a merge.</span></span> <span data-ttu-id="2b092-105">Zusammenführungen [und Transformationen](merges-and-transforms.md) arbeiten mit einer gesamten Datenbank, und ein Merge kombiniert zwei Datenbanken zu einer Datenbank.</span><span class="sxs-lookup"><span data-stu-id="2b092-105">[Merges and Transforms](merges-and-transforms.md) operate on an entire database, and a merge combines two databases into one.</span></span> <span data-ttu-id="2b092-106">Zusammenführungen sind für Entwicklungsteams nützlich, da Sie es ermöglichen, dass die Installations Datenbank der großen Anwendung in kleinere Teile aufgeteilt und anschließend später in der kompletten Installations Datenbank kombiniert werden kann.</span><span class="sxs-lookup"><span data-stu-id="2b092-106">Merges are useful to development teams because they allow the installation database of large application to be divided into smaller parts and then recombined into the complete installation database later.</span></span>

<span data-ttu-id="2b092-107">**So führen Sie mehrere Komponenten Datenbanken zu einer einzelnen, kompletten Datenbank zusammen**</span><span class="sxs-lookup"><span data-stu-id="2b092-107">**To merge several component databases into a single complete database**</span></span>

1.  <span data-ttu-id="2b092-108">Entwickeln Sie die partiellen Komponenten Datenbanken separat.</span><span class="sxs-lookup"><span data-stu-id="2b092-108">Develop the partial component databases separately.</span></span>
2.  <span data-ttu-id="2b092-109">Führen Sie die einzelnen Komponenten Datenbanken durch Aufrufen der Funktion [**msidatabasemerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) in der Hauptprodukt Datenbank zusammen.</span><span class="sxs-lookup"><span data-stu-id="2b092-109">Merge each component database into the main product database by calling the [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) function.</span></span>

 

 




---
description: In diesem Beispiel wird veranschaulicht, wie ein Patchpaket erstellt wird, das ein kleines Update auf das Beispiel Installationspaket anwendet, das in einem Installations Beispiel erläutert wird.
ms.assetid: 17dadd64-6e81-444a-985e-1b340e4f2ee5
title: Beispiel für ein kleines Update-Patching
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36d4997a326e8fea33086a75c9cf40ecef8cb997
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349368"
---
# <a name="a-small-update-patching-example"></a><span data-ttu-id="ed363-103">Beispiel für ein kleines Update-Patching</span><span class="sxs-lookup"><span data-stu-id="ed363-103">A Small Update Patching Example</span></span>

<span data-ttu-id="ed363-104">In diesem Beispiel wird veranschaulicht, wie ein [Patchpaket](patch-packages.md) erstellt wird, das ein [kleines Update](small-updates.md) auf das Beispiel Installationspaket anwendet, das in [einem Installations Beispiel](an-installation-example.md)erläutert wird.</span><span class="sxs-lookup"><span data-stu-id="ed363-104">This example illustrates how to create a [patch package](patch-packages.md) that applies a [small update](small-updates.md) to the sample installation package discussed in [An Installation Example](an-installation-example.md).</span></span> <span data-ttu-id="ed363-105">Ein kleines Update nimmt Änderungen an einer oder mehreren Anwendungs Dateien vor, die als zu gering eingestuft werden, um das Ändern des Produktcodes zu rechtfertigen.</span><span class="sxs-lookup"><span data-stu-id="ed363-105">A small update makes changes to one or more application files that are judged to be too minor to warrant changing the product code.</span></span> <span data-ttu-id="ed363-106">Weitere Informationen finden Sie unter [Patching und Upgrades](patching-and-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="ed363-106">For more information see [Patching and Upgrades](patching-and-upgrades.md).</span></span>

<span data-ttu-id="ed363-107">In diesem Beispiel wird veranschaulicht, wie ein Windows Installer Patch-Paket erstellt wird, mit dem die Konzert Funktion des hypothetischen Product MNP2000 aktualisiert wird, um einen Fehler im ursprünglichen Produkt zu beheben.</span><span class="sxs-lookup"><span data-stu-id="ed363-107">This example illustrates how to create a Windows Installer patch package that updates the Concert feature of the hypothetical product MNP2000 to fix an error in the original product.</span></span> <span data-ttu-id="ed363-108">Das Patchpaket für das Beispiel wendet ein kleines Update auf das Produkt an, das keine Änderung des Produktcodes erfordert.</span><span class="sxs-lookup"><span data-stu-id="ed363-108">The example patch package applies a small update to the product that does not require changing the product code.</span></span> <span data-ttu-id="ed363-109">Weitere Informationen zu wichtigen Upgrades finden Sie im Abschnitt zu den [wichtigsten Upgrades](major-upgrades.md) im Abschnitt " [Patching und Upgrades](patching-and-upgrades.md) ".</span><span class="sxs-lookup"><span data-stu-id="ed363-109">See the topic on [Major Upgrades](major-upgrades.md) in the [Patching and Upgrades](patching-and-upgrades.md) section for more information about major upgrades.</span></span>

<span data-ttu-id="ed363-110">Das Beispiel Aktualisierungs Paket verfügt über die folgenden Spezifikationen:</span><span class="sxs-lookup"><span data-stu-id="ed363-110">The sample upgrade package has the following specifications:</span></span>

-   <span data-ttu-id="ed363-111">Es korrigiert einen geringfügigen Fehler in dem Konzert Zeitplan, der durch das Konzert Feature angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ed363-111">It corrects a minor error in the Concert schedule displayed by the Concert feature.</span></span>
-   <span data-ttu-id="ed363-112">Der Paket Code wird aktualisiert, um widerzuspiegeln, dass sich das Installationspaket geändert hat.</span><span class="sxs-lookup"><span data-stu-id="ed363-112">It updates the package code to reflect the installation package has changed.</span></span>
-   <span data-ttu-id="ed363-113">Das kleine Update kann durch Patchen der lokalen Installation des Produkts angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="ed363-113">The small update can be applied by patching the local installation of the product.</span></span>

[<span data-ttu-id="ed363-114">Fortsetzen</span><span class="sxs-lookup"><span data-stu-id="ed363-114">Continue</span></span>](planning-a-small-update-patch.md)

 

 




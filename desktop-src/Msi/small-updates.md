---
description: Ein kleines Update nimmt Änderungen an einer oder mehreren Anwendungs Dateien vor, die zu gering sind, um das Ändern des Produktcodes zu rechtfertigen.
ms.assetid: c74ef2bd-9cf5-4ec0-bfff-1fad0e17ba98
title: Kleine Updates
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ca87e825f462a98cc7fc80ad42d2b09b7931d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128372"
---
# <a name="small-updates"></a><span data-ttu-id="df404-103">Kleine Updates</span><span class="sxs-lookup"><span data-stu-id="df404-103">Small Updates</span></span>

<span data-ttu-id="df404-104">Ein kleines Update nimmt Änderungen an einer oder mehreren Anwendungs Dateien vor, die zu gering sind, um das Ändern des Produktcodes zu rechtfertigen.</span><span class="sxs-lookup"><span data-stu-id="df404-104">A small update makes changes to one or more application files that are too minor to warrant changing the product code.</span></span> <span data-ttu-id="df404-105">Ein kleines Update wird häufig auch als QFE-Update (Quick Fix Engineering) bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="df404-105">A small update is also commonly referred to as a quick fix engineering (QFE) update.</span></span> <span data-ttu-id="df404-106">Bei einem kleinen Update ist die Neuorganisation der Funktionskomponenten Struktur nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="df404-106">A small update does not permit reorganization of the feature-component tree.</span></span>

<span data-ttu-id="df404-107">Bei einem typischen kleinen Update werden nur eine oder zwei Dateien oder ein Registrierungsschlüssel geändert.</span><span class="sxs-lookup"><span data-stu-id="df404-107">A typical small update changes only one or two files or a registry key.</span></span> <span data-ttu-id="df404-108">Da ein kleines Update die Informationen in der MSI-Datei ändert, muss der Installationspaket Code geändert werden.</span><span class="sxs-lookup"><span data-stu-id="df404-108">Because a small update changes the information in the .msi file, the installation package code must be changed.</span></span> <span data-ttu-id="df404-109">Der Paketcode wird in der [**Zusammenfassungs Eigenschaft "Revisionsnummer**](revision-number-summary.md) " des [Zusammenfassungs Informationsdaten Stroms](summary-information-stream.md)gespeichert.</span><span class="sxs-lookup"><span data-stu-id="df404-109">The package code is stored in the [**Revision Number Summary**](revision-number-summary.md) property of the [Summary Information Stream](summary-information-stream.md).</span></span>

<span data-ttu-id="df404-110">Der Produktcode wird nie mit einem kleinen Update geändert, sodass alle Änderungen, die durch ein kleines Update eingeführt wurden, mit den in [Ändern des Produktcodes](changing-the-product-code.md)beschriebenen Richtlinien übereinstimmen müssen.</span><span class="sxs-lookup"><span data-stu-id="df404-110">The product code is never changed with a small update, so all of the changes introduced by a small update have to be consistent with the guidelines described in [Changing the Product Code](changing-the-product-code.md).</span></span> <span data-ttu-id="df404-111">Ein Update erfordert ein [großes Upgrade](major-upgrades.md) , um [**ProductCode**](productcode.md)zu ändern.</span><span class="sxs-lookup"><span data-stu-id="df404-111">An update requires a [major upgrade](major-upgrades.md) to change the [**ProductCode**](productcode.md).</span></span> <span data-ttu-id="df404-112">Wenn es erforderlich ist, zwischen Produkten zu unterscheiden, ohne den Produktcode zu ändern, verwenden Sie ein [kleineres Upgrade](minor-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="df404-112">If it is necessary to differentiate between products without changing the product code, use a [minor upgrade](minor-upgrades.md).</span></span>

<span data-ttu-id="df404-113">Informationen zum Anwenden eines kleinen Update-Patch-Pakets auf ein Windows Installer Paket finden Sie unter [Erstellen eines kleinen Update Patches](creating-a-small-update-patch.md), [anwenden kleiner Updates durch Patchen der lokalen Installation des Produkts](applying-small-updates-by-patching-the-local-installation-of-the-product.md), [anwenden kleiner Updates durch erneutes Installieren des Produkts](applying-small-updates-by-reinstalling-the-product.md)und [anwenden kleiner Updates durch Patchen eines administrativen Abbilds](applying-small-updates-by-patching-an-administrative-image.md).</span><span class="sxs-lookup"><span data-stu-id="df404-113">For information on how to apply a small update patch package to a Windows Installer package, see [Creating a Small Update Patch](creating-a-small-update-patch.md), [Applying Small Updates by Patching the Local Installation of the Product](applying-small-updates-by-patching-the-local-installation-of-the-product.md), [Applying Small Updates by Reinstalling the Product](applying-small-updates-by-reinstalling-the-product.md), and [Applying Small Updates by Patching an Administrative Image](applying-small-updates-by-patching-an-administrative-image.md).</span></span>

 

 




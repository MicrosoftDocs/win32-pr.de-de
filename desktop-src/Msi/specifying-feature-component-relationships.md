---
description: Jede Windows Installer Funktion verwendet eine oder mehrere Windows Installer Komponenten, und Features können Komponenten gemeinsam verwenden.
ms.assetid: 7ab4b359-e729-4ca5-8ef3-fa8e988be6da
title: Angeben von Feature-Component Beziehungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a05ff15f4c735ac7d081c16f49f1aafe555a96db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372862"
---
# <a name="specifying-feature-component-relationships"></a><span data-ttu-id="027a3-103">Angeben von Feature-Component Beziehungen</span><span class="sxs-lookup"><span data-stu-id="027a3-103">Specifying Feature-Component Relationships</span></span>

<span data-ttu-id="027a3-104">Jede [Windows Installer Funktion](windows-installer-features.md) verwendet eine oder mehrere [Windows Installer Komponenten](windows-installer-components.md), und Features können Komponenten gemeinsam verwenden.</span><span class="sxs-lookup"><span data-stu-id="027a3-104">Each [Windows Installer Feature](windows-installer-features.md) uses one or more [Windows Installer Components](windows-installer-components.md), and features may share components.</span></span> <span data-ttu-id="027a3-105">Die [FeatureComponents-Tabelle](featurecomponents-table.md) definiert die Beziehung zwischen Features und Komponenten.</span><span class="sxs-lookup"><span data-stu-id="027a3-105">The [FeatureComponents table](featurecomponents-table.md) defines the relationship between features and components.</span></span> <span data-ttu-id="027a3-106">Weitere Informationen finden Sie in der Übersicht über die [Kern Tabellen](core-tables-group.md) und [Komponenten und Features](components-and-features.md) in der Windows Installer Übersicht.</span><span class="sxs-lookup"><span data-stu-id="027a3-106">See the [Core Tables Group](core-tables-group.md) and [Components and Features](components-and-features.md) in the Windows Installer overview.</span></span> <span data-ttu-id="027a3-107">In diesem Abschnitt fügen Sie der Tabelle "FeatureComponents" des Notepad-Beispiels Informationen hinzu.</span><span class="sxs-lookup"><span data-stu-id="027a3-107">In this section you add information to the FeatureComponents table of the Notepad sample.</span></span>

<span data-ttu-id="027a3-108">Öffnen Sie MNP2000.msi mit dem Datenbank-Editor, und geben Sie die folgenden Daten in die leere FeatureComponents-Tabelle ein.</span><span class="sxs-lookup"><span data-stu-id="027a3-108">Use your database editor to open MNP2000.msi and enter the following data into the empty FeatureComponents table.</span></span>

[<span data-ttu-id="027a3-109">FeatureComponents-Tabelle</span><span class="sxs-lookup"><span data-stu-id="027a3-109">FeatureComponents Table</span></span>](featurecomponents-table.md)



| <span data-ttu-id="027a3-110">Funktion\_</span><span class="sxs-lookup"><span data-stu-id="027a3-110">Feature\_</span></span> | <span data-ttu-id="027a3-111">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="027a3-111">Component\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="027a3-112">Ball</span><span class="sxs-lookup"><span data-stu-id="027a3-112">Baseball</span></span>  | <span data-ttu-id="027a3-113">Ball</span><span class="sxs-lookup"><span data-stu-id="027a3-113">Baseball</span></span>    |
| <span data-ttu-id="027a3-114">Konzert</span><span class="sxs-lookup"><span data-stu-id="027a3-114">Concert</span></span>   | <span data-ttu-id="027a3-115">Konzert</span><span class="sxs-lookup"><span data-stu-id="027a3-115">Concert</span></span>     |
| <span data-ttu-id="027a3-116">Abhängigkeit</span><span class="sxs-lookup"><span data-stu-id="027a3-116">Dance</span></span>     | <span data-ttu-id="027a3-117">Abhängigkeit</span><span class="sxs-lookup"><span data-stu-id="027a3-117">Dance</span></span>       |
| <span data-ttu-id="027a3-118">Verbandes</span><span class="sxs-lookup"><span data-stu-id="027a3-118">Football</span></span>  | <span data-ttu-id="027a3-119">Verbandes</span><span class="sxs-lookup"><span data-stu-id="027a3-119">Football</span></span>    |
| <span data-ttu-id="027a3-120">Hilfe</span><span class="sxs-lookup"><span data-stu-id="027a3-120">Help</span></span>      | <span data-ttu-id="027a3-121">Hilfe</span><span class="sxs-lookup"><span data-stu-id="027a3-121">Help</span></span>        |
| <span data-ttu-id="027a3-122">January</span><span class="sxs-lookup"><span data-stu-id="027a3-122">January</span></span>   | <span data-ttu-id="027a3-123">January</span><span class="sxs-lookup"><span data-stu-id="027a3-123">January</span></span>     |
| <span data-ttu-id="027a3-124">Newyears</span><span class="sxs-lookup"><span data-stu-id="027a3-124">NewYears</span></span>  | <span data-ttu-id="027a3-125">Newyears</span><span class="sxs-lookup"><span data-stu-id="027a3-125">NewYears</span></span>    |
| <span data-ttu-id="027a3-126">Editor</span><span class="sxs-lookup"><span data-stu-id="027a3-126">Notepad</span></span>   | <span data-ttu-id="027a3-127">Editor</span><span class="sxs-lookup"><span data-stu-id="027a3-127">Notepad</span></span>     |
| <span data-ttu-id="027a3-128">Infodatei</span><span class="sxs-lookup"><span data-stu-id="027a3-128">Readme</span></span>    | <span data-ttu-id="027a3-129">Editor</span><span class="sxs-lookup"><span data-stu-id="027a3-129">Notepad</span></span>     |



 

[<span data-ttu-id="027a3-130">Fortsetzen</span><span class="sxs-lookup"><span data-stu-id="027a3-130">Continue</span></span>](adding-registry-information.md)

 

 




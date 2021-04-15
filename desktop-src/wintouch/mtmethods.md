---
title: Methoden (IManipulationProcessor)
description: Dieser Abschnitt enthält die Methoden für die IManipulationProcessor-Schnittstelle.
ms.assetid: 33736f79-cb61-449c-80b9-1358db2621e9
keywords:
- Windows-Berührungs-, IManipulationProcessor-Schnittstelle
- Windows-Berührungs Schnittstellen Methoden
- Manipulationen, IManipulationProcessor-Schnittstelle
- IManipulationProcessor-Schnittstelle, Methoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 995a848e18b8308d46ceda717bf7eec291953505
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104391427"
---
# <a name="methods-imanipulationprocessor"></a><span data-ttu-id="737c3-107">Methoden (IManipulationProcessor)</span><span class="sxs-lookup"><span data-stu-id="737c3-107">Methods (IManipulationProcessor)</span></span>

<span data-ttu-id="737c3-108">Dieser Abschnitt enthält die Methoden für die [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="737c3-108">This section contains the methods for the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interface.</span></span>

<span data-ttu-id="737c3-109">Die folgenden Methoden werden von der [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) -Schnittstelle verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="737c3-109">The following methods are exposed by the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interface.</span></span>



| <span data-ttu-id="737c3-110">Methode</span><span class="sxs-lookup"><span data-stu-id="737c3-110">Method</span></span>                                                                      | <span data-ttu-id="737c3-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="737c3-111">Description</span></span>                                                                              |
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="737c3-112">**CompleteManipulation**</span><span class="sxs-lookup"><span data-stu-id="737c3-112">**CompleteManipulation**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-completemanipulation) | <span data-ttu-id="737c3-113">Diese Methode wird aufgerufen, wenn der Entwickler entscheidet, die Bearbeitung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="737c3-113">This method is called when the developer chooses to end the manipulation.</span></span>                |
| [<span data-ttu-id="737c3-114">**Getangularvelocity**</span><span class="sxs-lookup"><span data-stu-id="737c3-114">**GetAngularVelocity**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-getangularvelocity)     | <span data-ttu-id="737c3-115">Berechnet die Rotationsgeschwindigkeit, in der das Zielobjekt bewegt wird.</span><span class="sxs-lookup"><span data-stu-id="737c3-115">Calculates the rotational velocity that the target object is moving at.</span></span>                  |
| [<span data-ttu-id="737c3-116">**Getexpansionvelocity**</span><span class="sxs-lookup"><span data-stu-id="737c3-116">**GetExpansionVelocity**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-getexpansionvelocity) | <span data-ttu-id="737c3-117">Berechnet die Rate, um die das Zielobjekt erweitert wird.</span><span class="sxs-lookup"><span data-stu-id="737c3-117">Calculates the rate that the target object is expanding at.</span></span>                              |
| [<span data-ttu-id="737c3-118">**Getvelocityx**</span><span class="sxs-lookup"><span data-stu-id="737c3-118">**GetVelocityX**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-getvelocityx)                 | <span data-ttu-id="737c3-119">Berechnet die horizontale Geschwindigkeit für das Zielobjekt und gibt Sie zurück.</span><span class="sxs-lookup"><span data-stu-id="737c3-119">Calculates and returns the horizontal velocity for the target object.</span></span>                    |
| [<span data-ttu-id="737c3-120">**Getvelocityy**</span><span class="sxs-lookup"><span data-stu-id="737c3-120">**GetVelocityY**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-getvelocityy)                 | <span data-ttu-id="737c3-121">Berechnet die vertikale Geschwindigkeit und gibt Sie zurück.</span><span class="sxs-lookup"><span data-stu-id="737c3-121">Calculates and returns the vertical velocity.</span></span>                                            |
| [<span data-ttu-id="737c3-122">**Processdown**</span><span class="sxs-lookup"><span data-stu-id="737c3-122">**ProcessDown**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processdown)                   | <span data-ttu-id="737c3-123">Feeds von Daten an den Manipulations Prozessor, der einem Ziel zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="737c3-123">Feeds data to the manipulation processor associated with a target.</span></span>                       |
| [<span data-ttu-id="737c3-124">**Processmove**</span><span class="sxs-lookup"><span data-stu-id="737c3-124">**ProcessMove**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processmove)                   | <span data-ttu-id="737c3-125">Feeds von Daten an den Manipulations Prozessor, der einem Ziel zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="737c3-125">Feeds data to the manipulation processor associated with a target.</span></span>                       |
| [<span data-ttu-id="737c3-126">**Processup**</span><span class="sxs-lookup"><span data-stu-id="737c3-126">**ProcessUp**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processup)                       | <span data-ttu-id="737c3-127">Feeds von Daten an den Manipulations Prozessor, der einem Ziel zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="737c3-127">Feeds data to the manipulation processor associated with a target.</span></span>                       |
| [<span data-ttu-id="737c3-128">**Processdownwithtime**</span><span class="sxs-lookup"><span data-stu-id="737c3-128">**ProcessDownWithTime**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processdownwithtime)   | <span data-ttu-id="737c3-129">Feeds von Daten, einschließlich eines Zeitstempels, auf den einem Ziel zugeordneten Bearbeitungs Prozessor.</span><span class="sxs-lookup"><span data-stu-id="737c3-129">Feeds data including a timestamp to the manipulation processor associated with a target.</span></span> |
| [<span data-ttu-id="737c3-130">**Processmuvewithtime**</span><span class="sxs-lookup"><span data-stu-id="737c3-130">**ProcessMoveWithTime**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processmovewithtime)   | <span data-ttu-id="737c3-131">Feeds von Daten, einschließlich eines Zeitstempels, auf den einem Ziel zugeordneten Bearbeitungs Prozessor.</span><span class="sxs-lookup"><span data-stu-id="737c3-131">Feeds data including a timestamp to the manipulation processor associated with a target.</span></span> |
| [<span data-ttu-id="737c3-132">**Processupwithtime**</span><span class="sxs-lookup"><span data-stu-id="737c3-132">**ProcessUpWithTime**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processupwithtime)       | <span data-ttu-id="737c3-133">Feeds von Daten, einschließlich eines Zeitstempels, auf den einem Ziel zugeordneten Bearbeitungs Prozessor.</span><span class="sxs-lookup"><span data-stu-id="737c3-133">Feeds data including a timestamp to the manipulation processor associated with a target.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="737c3-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="737c3-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="737c3-135">**IManipulationProcessor**</span><span class="sxs-lookup"><span data-stu-id="737c3-135">**IManipulationProcessor**</span></span>](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor)
</dt> </dl>

 

 





---
description: Die vorgeschlagenen Aktions Sequenzen für eine grundlegende instaluisequence-Tabelle in einer Windows Installer-Datenbank.
ms.assetid: f1ddad1e-c075-4054-aa24-f1acdc72da96
title: Vorgeschlagene InstallUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1accfc889d51cb75b3928df60931c848b30bcad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348068"
---
# <a name="suggested-installuisequence"></a><span data-ttu-id="4a482-103">Vorgeschlagene InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="4a482-103">Suggested InstallUISequence</span></span>



| <span data-ttu-id="4a482-104">Aktion</span><span class="sxs-lookup"><span data-stu-id="4a482-104">Action</span></span>                                          | <span data-ttu-id="4a482-105">Bedingung</span><span class="sxs-lookup"><span data-stu-id="4a482-105">Condition</span></span>                                                                                                  | <span data-ttu-id="4a482-106">Sequenz</span><span class="sxs-lookup"><span data-stu-id="4a482-106">Sequence</span></span> |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------|----------|
| <span data-ttu-id="4a482-107">Fatalerrordlg</span><span class="sxs-lookup"><span data-stu-id="4a482-107">FatalErrorDlg</span></span>                                   |                                                                                                            | <span data-ttu-id="4a482-108">-3</span><span class="sxs-lookup"><span data-stu-id="4a482-108">-3</span></span>       |
| <span data-ttu-id="4a482-109">Userexitdlg</span><span class="sxs-lookup"><span data-stu-id="4a482-109">UserExitDlg</span></span>                                     |                                                                                                            | <span data-ttu-id="4a482-110">-2</span><span class="sxs-lookup"><span data-stu-id="4a482-110">-2</span></span>       |
| <span data-ttu-id="4a482-111">Exitdlg</span><span class="sxs-lookup"><span data-stu-id="4a482-111">ExitDlg</span></span>                                         |                                                                                                            | <span data-ttu-id="4a482-112">-1</span><span class="sxs-lookup"><span data-stu-id="4a482-112">-1</span></span>       |
| [<span data-ttu-id="4a482-113">LaunchConditions</span><span class="sxs-lookup"><span data-stu-id="4a482-113">LaunchConditions</span></span>](launchconditions-action.md) |                                                                                                            | <span data-ttu-id="4a482-114">100</span><span class="sxs-lookup"><span data-stu-id="4a482-114">100</span></span>      |
| <span data-ttu-id="4a482-115">Preparedlg</span><span class="sxs-lookup"><span data-stu-id="4a482-115">PrepareDlg</span></span>                                      |                                                                                                            | <span data-ttu-id="4a482-116">140</span><span class="sxs-lookup"><span data-stu-id="4a482-116">140</span></span>      |
| [<span data-ttu-id="4a482-117">AppSearch</span><span class="sxs-lookup"><span data-stu-id="4a482-117">AppSearch</span></span>](appsearch-action.md)               |                                                                                                            | <span data-ttu-id="4a482-118">400</span><span class="sxs-lookup"><span data-stu-id="4a482-118">400</span></span>      |
| [<span data-ttu-id="4a482-119">Ccpsearch</span><span class="sxs-lookup"><span data-stu-id="4a482-119">CCPSearch</span></span>](ccpsearch-action.md)               | <span data-ttu-id="4a482-120">Nicht [ **installiert**](installed.md)</span><span class="sxs-lookup"><span data-stu-id="4a482-120">NOT [**Installed**](installed.md)</span></span>                                                                         | <span data-ttu-id="4a482-121">500</span><span class="sxs-lookup"><span data-stu-id="4a482-121">500</span></span>      |
| [<span data-ttu-id="4a482-122">RMCCPSEARCH</span><span class="sxs-lookup"><span data-stu-id="4a482-122">RMCCPSearch</span></span>](rmccpsearch-action.md)           | <span data-ttu-id="4a482-123">Nicht [ **installiert**](installed.md)</span><span class="sxs-lookup"><span data-stu-id="4a482-123">NOT [**Installed**](installed.md)</span></span>                                                                         | <span data-ttu-id="4a482-124">600</span><span class="sxs-lookup"><span data-stu-id="4a482-124">600</span></span>      |
| [<span data-ttu-id="4a482-125">Costinitialize</span><span class="sxs-lookup"><span data-stu-id="4a482-125">CostInitialize</span></span>](costinitialize-action.md)     |                                                                                                            | <span data-ttu-id="4a482-126">800</span><span class="sxs-lookup"><span data-stu-id="4a482-126">800</span></span>      |
| [<span data-ttu-id="4a482-127">Datei Kosten</span><span class="sxs-lookup"><span data-stu-id="4a482-127">FileCost</span></span>](filecost-action.md)                 |                                                                                                            | <span data-ttu-id="4a482-128">900</span><span class="sxs-lookup"><span data-stu-id="4a482-128">900</span></span>      |
| [<span data-ttu-id="4a482-129">Costfinalize</span><span class="sxs-lookup"><span data-stu-id="4a482-129">CostFinalize</span></span>](costfinalize-action.md)         |                                                                                                            | <span data-ttu-id="4a482-130">1000</span><span class="sxs-lookup"><span data-stu-id="4a482-130">1000</span></span>     |
| <span data-ttu-id="4a482-131">Welcomedlg</span><span class="sxs-lookup"><span data-stu-id="4a482-131">WelcomeDlg</span></span>                                      | <span data-ttu-id="4a482-132">Nicht [ **installiert**](installed.md)</span><span class="sxs-lookup"><span data-stu-id="4a482-132">NOT [**Installed**](installed.md)</span></span>                                                                         | <span data-ttu-id="4a482-133">1230</span><span class="sxs-lookup"><span data-stu-id="4a482-133">1230</span></span>     |
| <span data-ttu-id="4a482-134">Resumedlg</span><span class="sxs-lookup"><span data-stu-id="4a482-134">ResumeDlg</span></span>                                       | <span data-ttu-id="4a482-135">[**Installiert**](installed.md) Und ( [**fort**](resume.md) setzen oder [**vorab ausgewählt**](preselected.md))</span><span class="sxs-lookup"><span data-stu-id="4a482-135">[**Installed**](installed.md) AND ( [**RESUME**](resume.md) OR [**Preselected**](preselected.md))</span></span>       | <span data-ttu-id="4a482-136">1240</span><span class="sxs-lookup"><span data-stu-id="4a482-136">1240</span></span>     |
| <span data-ttu-id="4a482-137">Maintenancewelcomedlg</span><span class="sxs-lookup"><span data-stu-id="4a482-137">MaintenanceWelcomeDlg</span></span>                           | <span data-ttu-id="4a482-138">[**Installiert**](installed.md) Und nicht [**fortsetzen und nicht**](resume.md) [**vorab ausgewählt**](preselected.md)</span><span class="sxs-lookup"><span data-stu-id="4a482-138">[**Installed**](installed.md) AND NOT [**RESUME**](resume.md) AND NOT [**Preselected**](preselected.md)</span></span> | <span data-ttu-id="4a482-139">1250</span><span class="sxs-lookup"><span data-stu-id="4a482-139">1250</span></span>     |
| <span data-ttu-id="4a482-140">ProgressDlg</span><span class="sxs-lookup"><span data-stu-id="4a482-140">ProgressDlg</span></span>                                     |                                                                                                            | <span data-ttu-id="4a482-141">1280</span><span class="sxs-lookup"><span data-stu-id="4a482-141">1280</span></span>     |
| [<span data-ttu-id="4a482-142">ExecuteAction</span><span class="sxs-lookup"><span data-stu-id="4a482-142">ExecuteAction</span></span>](executeaction-action.md)       |                                                                                                            | <span data-ttu-id="4a482-143">1300</span><span class="sxs-lookup"><span data-stu-id="4a482-143">1300</span></span>     |



 

 

 




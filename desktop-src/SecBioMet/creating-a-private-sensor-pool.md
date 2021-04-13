---
title: Erstellen eines privaten Sensor Pools
description: Verwenden der Windows-Biometrieframework-API zum Erstellen eines privaten Sensor Pools.
ms.assetid: 79944E30-A3D4-411D-A551-3B309DEA6FEA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8eda88f8a9bd0befcbf5527e52d572ec7ca55ce2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388606"
---
# <a name="creating-a-private-sensor-pool"></a><span data-ttu-id="769c5-103">Erstellen eines privaten Sensor Pools</span><span class="sxs-lookup"><span data-stu-id="769c5-103">Creating a Private Sensor Pool</span></span>

<span data-ttu-id="769c5-104">Ein privater Sensor Pool ist eine Sammlung von biometrischen Einheiten, die für die ausschließliche Verwendung durch eine Client Anwendung reserviert sind.</span><span class="sxs-lookup"><span data-stu-id="769c5-104">A private sensor pool is a collection of biometric units reserved for exclusive use by a client application.</span></span> <span data-ttu-id="769c5-105">Private Pools unterstützen proprietäre Authentifizierungsmethoden und ermöglichen es einer Client Anwendung, mithilfe von vom Hersteller angegebenen Steuerungs Befehlen auf eine biometrische Einheit zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="769c5-105">Private pools support proprietary authentication methods and enable a client application to access a biometric unit by using vendor-specified control commands.</span></span>

<span data-ttu-id="769c5-106">Die folgenden Themen enthalten Codebeispiele, die zeigen, wie ein privater Sensor Pool erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="769c5-106">The following topics contain code examples that show how to create a private sensor pool.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="769c5-107">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="769c5-107">In this section</span></span>



| <span data-ttu-id="769c5-108">Thema</span><span class="sxs-lookup"><span data-stu-id="769c5-108">Topic</span></span>                                                                         | <span data-ttu-id="769c5-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="769c5-109">Description</span></span>                                                                                          |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="769c5-110">Sensor Pools</span><span class="sxs-lookup"><span data-stu-id="769c5-110">Sensor Pools</span></span>](sensor-pools.md)<br/>                                   | <span data-ttu-id="769c5-111">Beschreibt drei mögliche Sensor Pools: "System", "private" und "nicht zugewiesen".</span><span class="sxs-lookup"><span data-stu-id="769c5-111">Describes three possible sensor pools: system, private, and unassigned.</span></span><br/>                   |
| [<span data-ttu-id="769c5-112">Einrichtung des privaten Pools</span><span class="sxs-lookup"><span data-stu-id="769c5-112">Private Pool Setup</span></span>](private-pool-setup.md)<br/>                       | <span data-ttu-id="769c5-113">Enthält das Setup Konsolen Projekt.</span><span class="sxs-lookup"><span data-stu-id="769c5-113">Contains the setup console project.</span></span><br/>                                                       |
| [<span data-ttu-id="769c5-114">Identität des privaten Pools</span><span class="sxs-lookup"><span data-stu-id="769c5-114">Private Pool Identity</span></span>](private-pool-identity.md)<br/>                 | <span data-ttu-id="769c5-115">Enthält das Identifikations Konsolen Projekt.</span><span class="sxs-lookup"><span data-stu-id="769c5-115">Contains the identification console project.</span></span><br/>                                              |
| [<span data-ttu-id="769c5-116">Private Pool Registrierung</span><span class="sxs-lookup"><span data-stu-id="769c5-116">Private Pool Enrollment</span></span>](private-pool-enrollment.md)<br/>             | <span data-ttu-id="769c5-117">Enthält das Registrierungs Konsolen Projekt.</span><span class="sxs-lookup"><span data-stu-id="769c5-117">Contains the enrollment console project.</span></span><br/>                                                  |
| [<span data-ttu-id="769c5-118">Hilfsfunktionen für private Pools</span><span class="sxs-lookup"><span data-stu-id="769c5-118">Private Pool Helper Functions</span></span>](private-pool-helper-functions.md)<br/> | <span data-ttu-id="769c5-119">Enthält Hilfsfunktionen für die Setup-, Identifizierungs-und Registrierungs Konsolen Projekte.</span><span class="sxs-lookup"><span data-stu-id="769c5-119">Contains helper functions for the setup, identification, and enrollment console projects.</span></span><br/> |
| [<span data-ttu-id="769c5-120">Erstellen von Client Anwendungen</span><span class="sxs-lookup"><span data-stu-id="769c5-120">Create client applications</span></span>](creating-client-applications.md)<br/>     | <span data-ttu-id="769c5-121">Verwenden der Windows-Biometrieframework-API zum Erstellen von Client Anwendungen</span><span class="sxs-lookup"><span data-stu-id="769c5-121">How to use the Windows Biometric Framework API to create client applications.</span></span><br/>             |



 

 

 






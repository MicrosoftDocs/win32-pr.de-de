---
description: Die folgenden Schnittstellen können zum Abrufen von Informationen zu Kryptografieanbietern verwendet werden.
ms.assetid: f4f6a763-707d-48a2-acb9-2a0c3530cf6b
title: Kryptografieanbieterschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1fa42a9a2704849552fadeb79933d85df9e9f78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129888"
---
# <a name="cryptographic-provider-interfaces"></a><span data-ttu-id="f6a4f-103">Kryptografieanbieterschnittstellen</span><span class="sxs-lookup"><span data-stu-id="f6a4f-103">Cryptographic Provider Interfaces</span></span>

<span data-ttu-id="f6a4f-104">Die folgenden Schnittstellen können zum Abrufen von Informationen zu Kryptografieanbietern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f6a4f-104">The following interfaces can be used to retrieve information about cryptographic providers.</span></span>



| <span data-ttu-id="f6a4f-105">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f6a4f-105">Interface</span></span>                                    | <span data-ttu-id="f6a4f-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f6a4f-106">Description</span></span>                                                                  |
|----------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="f6a4f-107">**Icspalgorithmus**</span><span class="sxs-lookup"><span data-stu-id="f6a4f-107">**ICspAlgorithm**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icspalgorithm)       | <span data-ttu-id="f6a4f-108">Stellt einen von einem Kryptografieanbieter implementierten Algorithmus dar.</span><span class="sxs-lookup"><span data-stu-id="f6a4f-108">Represents an algorithm implemented by a cryptographic provider.</span></span>             |
| [<span data-ttu-id="f6a4f-109">**Icspalgorithmen**</span><span class="sxs-lookup"><span data-stu-id="f6a4f-109">**ICspAlgorithms**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icspalgorithms)     | <span data-ttu-id="f6a4f-110">Verwaltet eine Auflistung von [**icspalgorithmusobjekten**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) .</span><span class="sxs-lookup"><span data-stu-id="f6a4f-110">Manages a collection of [**ICspAlgorithm**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) objects.</span></span> |
| [<span data-ttu-id="f6a4f-111">**Icspinformation**</span><span class="sxs-lookup"><span data-stu-id="f6a4f-111">**ICspInformation**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation)   | <span data-ttu-id="f6a4f-112">Bietet Zugriff auf allgemeine Informationen zu einem Kryptografieanbieter.</span><span class="sxs-lookup"><span data-stu-id="f6a4f-112">Provides access to general information about a cryptographic provider.</span></span>       |
| [<span data-ttu-id="f6a4f-113">**Icspinformation**</span><span class="sxs-lookup"><span data-stu-id="f6a4f-113">**ICspInformations**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations) | <span data-ttu-id="f6a4f-114">Verwaltet eine Auflistung von [**icspinformation**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation) -Objekten.</span><span class="sxs-lookup"><span data-stu-id="f6a4f-114">Manages a collection of [**ICspInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation) objects.</span></span>  |
| [<span data-ttu-id="f6a4f-115">**Icspstatus**</span><span class="sxs-lookup"><span data-stu-id="f6a4f-115">**ICspStatus**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus)             | <span data-ttu-id="f6a4f-116">Enthält Informationen zu einem Kryptografieanbieter-/algorithmuspaar.</span><span class="sxs-lookup"><span data-stu-id="f6a4f-116">Contains information about a cryptographic provider/algorithm pair.</span></span>          |
| [<span data-ttu-id="f6a4f-117">**Icspstatus**</span><span class="sxs-lookup"><span data-stu-id="f6a4f-117">**ICspStatuses**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatuses)         | <span data-ttu-id="f6a4f-118">Verwaltet eine Auflistung von [**icspstatus**](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus) -Objekten.</span><span class="sxs-lookup"><span data-stu-id="f6a4f-118">Manages a collection of [**ICspStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus) objects.</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="f6a4f-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f6a4f-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6a4f-120">CertEnroll-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="f6a4f-120">CertEnroll Interfaces</span></span>](certenroll-interfaces.md)
</dt> </dl>

 

 




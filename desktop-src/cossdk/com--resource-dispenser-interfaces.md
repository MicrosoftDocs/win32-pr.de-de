---
description: Com+-Ressourcen Verteiler Schnittstellen
ms.assetid: 66ee4dd6-15d2-49e8-89a3-6fbb5770cabf
title: Com+-Ressourcen Verteiler Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a6ea5c5c09f67f86b42ebf5b881f1d19ad1501
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860856"
---
# <a name="com-resource-dispenser-interfaces"></a><span data-ttu-id="0067b-103">Com+-Ressourcen Verteiler Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="0067b-103">COM+ Resource Dispenser Interfaces</span></span>

<span data-ttu-id="0067b-104">Anwendungskomponenten verwenden Ressourcen Spender, um auf freigegebene Informationen zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="0067b-104">Application components use resource dispensers to access shared information.</span></span> <span data-ttu-id="0067b-105">Die in der folgenden Tabelle beschriebenen Schnittstellen enthalten ausführliche Referenzinformationen für Entwickler von Ressourcen Spendern.</span><span class="sxs-lookup"><span data-stu-id="0067b-105">The interfaces described in the following table provide detailed reference information for developers of resource dispensers.</span></span>



| <span data-ttu-id="0067b-106">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="0067b-106">Interfaces</span></span>                                                | <span data-ttu-id="0067b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0067b-107">Description</span></span>                                                                                                               |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0067b-108">**Idispenser-Treiber**</span><span class="sxs-lookup"><span data-stu-id="0067b-108">**IDispenserDriver**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver)<br/>   | <span data-ttu-id="0067b-109">Diese Schnittstelle wird vom Ressourcen Verteiler-Inhaber aufgerufen, um eine Ressource zu erstellen, aufzulisten, auszuwerten und zu zerstören.</span><span class="sxs-lookup"><span data-stu-id="0067b-109">This interface is called by the resource dispenser holder to create, enlist, evaluate, and destroy a resource.</span></span><br/> |
| [<span data-ttu-id="0067b-110">**Idispenser Server-Manager**</span><span class="sxs-lookup"><span data-stu-id="0067b-110">**IDispenserManager**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager)<br/> | <span data-ttu-id="0067b-111">Ressourcen Spender verwenden diese Schnittstelle, um eine Verbindung mit dem Dispenser-Manager herzustellen.</span><span class="sxs-lookup"><span data-stu-id="0067b-111">Resource dispensers use this interface to connect to the dispenser manager.</span></span><br/>                                    |
| [<span data-ttu-id="0067b-112">**Ihälter**</span><span class="sxs-lookup"><span data-stu-id="0067b-112">**IHolder**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iholder)<br/>                     | <span data-ttu-id="0067b-113">Diese Schnittstelle wird verwendet, um Ressourcen vorzubereiten und zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="0067b-113">This interface is used to prepare and handle resources.</span></span><br/>                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="0067b-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0067b-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0067b-115">Konzepte des com+-Ressourcen Verteilers</span><span class="sxs-lookup"><span data-stu-id="0067b-115">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> <dt>

[<span data-ttu-id="0067b-116">In com+-ressourcendispenser-Schnittstellen verwendete Typen</span><span class="sxs-lookup"><span data-stu-id="0067b-116">Types Used in COM+ Resource Dispenser Interfaces</span></span>](types-used-in-com--resource-dispenser-interfaces.md)
</dt> </dl>

 

 





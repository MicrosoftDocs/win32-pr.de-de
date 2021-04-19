---
description: CRM-Komponenten können entweder in einer COM+-Serveranwendung oder in einer COM+-Bibliotheks Anwendung installiert werden.
ms.assetid: d1ce3a0c-1278-498c-b5dc-4e14b26b4fc2
title: Com+ CRM-Komponenten werden konfiguriert.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f3614c2c34d36cb140f08529c05b31bcc5a4c7f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342780"
---
# <a name="configuring-com-crm-components"></a><span data-ttu-id="853c8-103">Com+ CRM-Komponenten werden konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="853c8-103">Configuring COM+ CRM Components</span></span>

<span data-ttu-id="853c8-104">CRM-Komponenten können entweder in einer COM+-Serveranwendung oder in einer COM+-Bibliotheks Anwendung installiert werden.</span><span class="sxs-lookup"><span data-stu-id="853c8-104">CRM components can be installed into either a COM+ server application or a COM+ library application.</span></span> <span data-ttu-id="853c8-105">Allerdings müssen Sie immer in einer COM+-Serveranwendung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="853c8-105">However, they must always run in a COM+ server application.</span></span> <span data-ttu-id="853c8-106">Wenn Sie in einer COM+-Bibliotheks Anwendung installiert sind, sind Sie nicht für die Verwendung in Client Prozessen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="853c8-106">If they are installed in a COM+ library application, they are not available for use in client processes.</span></span>

<span data-ttu-id="853c8-107">Wenn die CRM-Komponenten in einer Bibliotheks Anwendung installiert sind, sind Sie für mehr als eine Serveranwendung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="853c8-107">If the CRM components they are installed in a library application, they are available to more than one server application.</span></span> <span data-ttu-id="853c8-108">Wenn Sie in einer bestimmten Serveranwendung installiert sind, sind Sie nur für die jeweilige Serveranwendung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="853c8-108">If installed in a specific server application, they are available only to that specific server application.</span></span>

<span data-ttu-id="853c8-109">Um die Verwendung eines CRM in einer Serveranwendung zu aktivieren, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="853c8-109">To enable use of a CRM in a server application, use the following steps:</span></span>

1.  <span data-ttu-id="853c8-110">Klicken Sie unter Komponenten Dienste auf der Seite Server Anwendungseigenschaften auf die Registerkarte **erweitert** .</span><span class="sxs-lookup"><span data-stu-id="853c8-110">From Component Services, under the server application properties page, click the **Advanced** tab.</span></span>

2.  <span data-ttu-id="853c8-111">Wählen Sie die Option **kompensierende Ressourcen-Manager aktivieren** für die Serveranwendung aus.</span><span class="sxs-lookup"><span data-stu-id="853c8-111">Select the **Enable compensating Resource Managers** option for that server application.</span></span> <span data-ttu-id="853c8-112">Wenn diese Option nicht ausgewählt ist, können Versuche, ein CRM innerhalb dieser Serveranwendung zu verwenden, nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="853c8-112">If this option is not selected, attempts to use a CRM within this server application will fail.</span></span>

    > [!Note]  
    > <span data-ttu-id="853c8-113">Wenn Sie in einer Bibliotheks Anwendung installiert sind, ist es nicht erforderlich, die Option **kompensierende Ressourcen-Manager aktivieren** für diese Bibliotheks Anwendung auszuwählen. diese Option muss jedoch für die Serveranwendung ausgewählt werden, in der das CRM ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="853c8-113">If installed in a library application, it is not necessary to select the **Enable compensating Resource Managers** option for that library application, but this option must be selected for the server application in which the CRM is intended to run.</span></span>

     

<span data-ttu-id="853c8-114">Es wird empfohlen, die CRM-Worker-und CRM-kompenatorkomponenten für ein bestimmtes CRM in derselben Anwendung zu installieren.</span><span class="sxs-lookup"><span data-stu-id="853c8-114">It is recommended that the CRM Worker and CRM Compensator components for a specific CRM be installed in the same application.</span></span>

<span data-ttu-id="853c8-115">Die empfohlenen Einstellungen für CRM-Komponenten lauten wie folgt.</span><span class="sxs-lookup"><span data-stu-id="853c8-115">The recommended settings for CRM components are as follows.</span></span>



| <span data-ttu-id="853c8-116">Komponente</span><span class="sxs-lookup"><span data-stu-id="853c8-116">Component</span></span>           | <span data-ttu-id="853c8-117">Einstellungen</span><span class="sxs-lookup"><span data-stu-id="853c8-117">Settings</span></span>                                                                                             |
|---------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="853c8-118">**CRM-Worker**</span><span class="sxs-lookup"><span data-stu-id="853c8-118">**CRM Worker**</span></span>      | <span data-ttu-id="853c8-119">Transaction = Requirements dsync = yesjit = yesthreading Model = both (oder Threading Model = Apartment)</span><span class="sxs-lookup"><span data-stu-id="853c8-119">transaction = requiredsync = yesJIT = yesthreading model = Both (or threading model = Apartment)</span></span>     |
| <span data-ttu-id="853c8-120">**CRM-kompenator**</span><span class="sxs-lookup"><span data-stu-id="853c8-120">**CRM Compensator**</span></span> | <span data-ttu-id="853c8-121">Transaction = disabledsync = disabledjit = nothreading Model = both (oder Threading Model = Apartment)</span><span class="sxs-lookup"><span data-stu-id="853c8-121">transaction = disabledsync = disabledJIT = nothreading model = Both (or threading model = Apartment)</span></span> |



 

> [!Note]  
> <span data-ttu-id="853c8-122">Komponenten, die das CRM verwenden, müssen beim Registrieren explizit ein Threading Modell angeben.</span><span class="sxs-lookup"><span data-stu-id="853c8-122">Components that use the CRM must explicitly specify a threading model when they are registered.</span></span> <span data-ttu-id="853c8-123">Der Standardwert "Hauptthread-Apartment" wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="853c8-123">The default, 'Main Thread Apartment,' is not supported.</span></span> <span data-ttu-id="853c8-124">Die einzigen beiden unterstützten Threading Modelle sind Apartment und beides.</span><span class="sxs-lookup"><span data-stu-id="853c8-124">The only two threading models supported are Apartment and Both.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="853c8-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="853c8-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="853c8-126">Kompensierende com+-Ressourcen-Manager Konzepte</span><span class="sxs-lookup"><span data-stu-id="853c8-126">COM+ Compensating Resource Manager Concepts</span></span>](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 




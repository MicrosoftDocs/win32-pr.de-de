---
description: Com+ stellt ein einfaches Programmiermodell für die Verwendung der automatischen Dienste bereit.
ms.assetid: 2d616b56-4b6a-4c3b-bbd8-d5ca03c4911f
title: Einführung in COM+-Dienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9fd9d256b0213d3b1c58cae7d9670f87e4f4423
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342339"
---
# <a name="com-services-primer"></a><span data-ttu-id="374ee-103">Einführung in COM+-Dienste</span><span class="sxs-lookup"><span data-stu-id="374ee-103">COM+ Services Primer</span></span>

<span data-ttu-id="374ee-104">Com+ stellt ein einfaches Programmiermodell für die Verwendung der automatischen Dienste bereit.</span><span class="sxs-lookup"><span data-stu-id="374ee-104">COM+ provides a simple programming model for using its automatic services.</span></span> <span data-ttu-id="374ee-105">Sie können diese Dienste einfach als deklarative Attribute für Komponenten und deren Methoden festlegen.</span><span class="sxs-lookup"><span data-stu-id="374ee-105">You can simply set these services as declarative attributes on components and their methods.</span></span> <span data-ttu-id="374ee-106">Wenn Sie diese Attribute festlegen, übergibt com+ die angeforderten Dienste automatisch nach Bedarf an das Objekt.</span><span class="sxs-lookup"><span data-stu-id="374ee-106">When you set these attributes, COM+ automatically delivers the requested services to the object as required.</span></span>

<span data-ttu-id="374ee-107">Diese Einführung zeigt com+-Dienste in Aktion, indem Sie den Beispiel Komponenten Code in drei definierten Schritten durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="374ee-107">This primer shows COM+ services in action by walking through sample component code in three defined steps.</span></span> <span data-ttu-id="374ee-108">Die Komplexität der Informationen wird im Verlauf der Schritte erstellt.</span><span class="sxs-lookup"><span data-stu-id="374ee-108">The complexity of the information builds as the steps progress.</span></span> <span data-ttu-id="374ee-109">Der Code konzentriert sich auf das vereinfachte Programmiermodell, wobei die Transaktionsverarbeitung verwendet wird, um grundlegende com+-Prinzipien zu veranschaulichen.</span><span class="sxs-lookup"><span data-stu-id="374ee-109">The code focuses on the simplified programming model, using transaction processing to demonstrate basic COM+ principles.</span></span>

<span data-ttu-id="374ee-110">Jeder der folgenden Schritte veranschaulicht einen grundlegenden Aspekt der com+-Dienste:</span><span class="sxs-lookup"><span data-stu-id="374ee-110">Each of the following steps illustrates a fundamental aspect of COM+ services:</span></span>

-   [<span data-ttu-id="374ee-111">Schritt 1: Erstellen einer transaktionalen Komponente</span><span class="sxs-lookup"><span data-stu-id="374ee-111">Step 1: Creating a Transactional Component</span></span>](step-1--creating-a-transactional-component.md)
-   [<span data-ttu-id="374ee-112">Schritt 2: Erweitern einer Transaktion über mehrere Komponenten hinweg</span><span class="sxs-lookup"><span data-stu-id="374ee-112">Step 2: Extending a Transaction Across Multiple Components</span></span>](step-2--extending-a-transaction-across-multiple-components.md)
-   [<span data-ttu-id="374ee-113">Schritt 3: wieder verwenden von Komponenten</span><span class="sxs-lookup"><span data-stu-id="374ee-113">Step 3: Reusing Components</span></span>](step-3--reusing-components.md)

## <a name="related-topics"></a><span data-ttu-id="374ee-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="374ee-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="374ee-115">Übersicht über die COM+-Programmierung</span><span class="sxs-lookup"><span data-stu-id="374ee-115">COM+ Programming Overview</span></span>](com--programming-overview.md)
</dt> <dt>

[<span data-ttu-id="374ee-116">Übersicht über die COM+-Anwendung</span><span class="sxs-lookup"><span data-stu-id="374ee-116">COM+ Application Overview</span></span>](com--application-overview.md)
</dt> <dt>

[<span data-ttu-id="374ee-117">Com+-Anwendungen werden konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="374ee-117">Configuring COM+ Applications</span></span>](configuring-com--applications.md)
</dt> <dt>

[<span data-ttu-id="374ee-118">Com+-Kontexte und Threading Modelle</span><span class="sxs-lookup"><span data-stu-id="374ee-118">COM+ Contexts and Threading Models</span></span>](com--contexts-and-threading-models.md)
</dt> <dt>

[<span data-ttu-id="374ee-119">Com+-Anwendungen werden erstellt.</span><span class="sxs-lookup"><span data-stu-id="374ee-119">Creating COM+ Applications</span></span>](creating-com--applications.md)
</dt> <dt>

[<span data-ttu-id="374ee-120">Entwerfen von com+-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="374ee-120">Designing COM+ Applications</span></span>](designing-com--applications.md)
</dt> </dl>

 

 




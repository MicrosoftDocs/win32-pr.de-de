---
description: Com+-Dienste ohne Komponenten
ms.assetid: 5ef67411-334b-476e-b9b7-3677b24ab7df
title: Com+-Dienste ohne Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1eeed5a9af96e241d137714d151cc632dd0f20e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127041"
---
# <a name="com-services-without-components"></a><span data-ttu-id="758aa-103">Com+-Dienste ohne Komponenten</span><span class="sxs-lookup"><span data-stu-id="758aa-103">COM+ Services Without Components</span></span>

<span data-ttu-id="758aa-104">Mit com+ 1,5 können Sie die von com+ bereitgestellten Dienste verwenden, ohne eine-Komponente zu erstellen, die die Methoden enthält, mit denen diese Dienste aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="758aa-104">With COM+ 1.5, you can use the services provided by COM+ without needing to build a component to contain the methods that call those services.</span></span> <span data-ttu-id="758aa-105">Dadurch profitieren Sie von Entwicklern, die normalerweise keine Komponenten verwenden, aber com+-Dienste wie Transaktionen oder com+-Tracker verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="758aa-105">This greatly benefits developers who do not normally use components but want to use COM+ services such as transactions or the COM+ Tracker.</span></span> <span data-ttu-id="758aa-106">Durch die Verwendung von COM+-Diensten ohne Komponenten können Entwickler den Aufwand vermeiden, mit dem eine Komponente erstellt wird, die nur für den Zugriff auf die benötigten com+-Dienste verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="758aa-106">By using COM+ services without components, developers can avoid the overhead of creating a component that is used to access only the COM+ services they need.</span></span>

<span data-ttu-id="758aa-107">Beispielsweise waren Skript Umgebungen üblicherweise die größten Verbraucher von COM+-Diensten, Sie waren jedoch nie in der Lage, diese Dienste effizient zu nutzen, da die Dienste innerhalb einer COM+-Komponente gebündelt werden mussten.</span><span class="sxs-lookup"><span data-stu-id="758aa-107">For example, script environments traditionally have been the largest consumers of COM+ services but they were never able to use those services efficiently because the services needed to be bundled within a COM+ component.</span></span> <span data-ttu-id="758aa-108">Diese Bündelung erfordert aufgrund der verstärkten Kommunikation und Duplizierung von Daten, die für die Interaktion der Skript Umgebung mit der Komponente erforderlich sind, zu Leistungseinbußen.</span><span class="sxs-lookup"><span data-stu-id="758aa-108">This bundling requirement increased performance costs because of the increased communication and duplication of data necessary for the scripting environment to interact with the component.</span></span> <span data-ttu-id="758aa-109">Durch die Verwendung von Diensten ohne Komponenten werden solche Kosten minimiert.</span><span class="sxs-lookup"><span data-stu-id="758aa-109">By using services without components, such costs are minimized.</span></span>

<span data-ttu-id="758aa-110">Die in der folgenden Tabelle beschriebenen Themen enthalten Hintergrundinformationen und Aufgabeninformationen zur Verwendung von COM+-Diensten ohne Komponenten.</span><span class="sxs-lookup"><span data-stu-id="758aa-110">The topics described in the following table provide background and task information about using COM+ services without components.</span></span> <span data-ttu-id="758aa-111">Diese Funktion ist für erweiterte Visual C++ Entwickler gedacht, die sich Gedanken über die Leistung machen.</span><span class="sxs-lookup"><span data-stu-id="758aa-111">This feature is intended for advanced Visual C++ developers who are concerned about performance.</span></span>



| <span data-ttu-id="758aa-112">Thema</span><span class="sxs-lookup"><span data-stu-id="758aa-112">Topic</span></span>                                                                                                 | <span data-ttu-id="758aa-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="758aa-113">Description</span></span>                                                                                    |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="758aa-114">Konzepte der com+-Dienste ohne Komponenten</span><span class="sxs-lookup"><span data-stu-id="758aa-114">COM+ Services Without Components Concepts</span></span>](com--services-without-components-concepts.md)<br/> | <span data-ttu-id="758aa-115">Bietet einen Überblick über die Verwendung von COM+-Diensten ohne Komponenten.</span><span class="sxs-lookup"><span data-stu-id="758aa-115">Provides an overview of using COM+ services without components.</span></span><br/>                     |
| [<span data-ttu-id="758aa-116">Com+-Dienste ohne Komponenten Aufgaben</span><span class="sxs-lookup"><span data-stu-id="758aa-116">COM+ Services Without Components Tasks</span></span>](com--services-without-components-tasks.md)<br/>       | <span data-ttu-id="758aa-117">Stellt Anweisungen für die Verwendung von com+ zum Erstellen und Verwenden von-Diensten ohne Komponenten bereit.</span><span class="sxs-lookup"><span data-stu-id="758aa-117">Provides instructions for using COM+ to create and use services without components.</span></span><br/> |



 

 

 





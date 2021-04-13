---
description: Konzepte der COM+-Partitionen
ms.assetid: 9fc35bef-ecc1-4764-bf69-ec89560daff4
title: Konzepte der COM+-Partitionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 483a34e6186cda8978c1882ed1fdfbe8732f7ec8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483078"
---
# <a name="com-partitions-concepts"></a><span data-ttu-id="860f9-103">Konzepte der COM+-Partitionen</span><span class="sxs-lookup"><span data-stu-id="860f9-103">COM+ Partitions Concepts</span></span>

<span data-ttu-id="860f9-104">In Computerumgebungen, in denen es erforderlich ist, unterschiedliche Versionen oder Konfigurationen einer Anwendung auf demselben Computer zu verwenden, können Konflikte auftreten, wenn eine Version der Anwendung andere Komponenten als die andere benötigt oder wenn eine Version eine Komponente auf dem Computer erfordert, die nicht mit der anderen Version der Anwendung kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="860f9-104">In computing environments where it's necessary to use different versions or configurations of an application on the same computer, conflicts can arise when one version of the application requires different components than the other or when one version requires a component on the computer that is incompatible with the other version of the application.</span></span> <span data-ttu-id="860f9-105">In der Vergangenheit bestand die einzige Möglichkeit zur Lösung dieses Problems darin, mehrere Computer beizubehalten und auf jedem Computer eine andere Version der Anwendung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="860f9-105">In the past, the only way to solve this problem was to maintain multiple computers and run a different version of the application on each computer.</span></span> <span data-ttu-id="860f9-106">Ein solcher Ansatz ist kostspielig und ineffizient, da dadurch die Hardwarekosten und der Verwaltungsaufwand erhöht werden.</span><span class="sxs-lookup"><span data-stu-id="860f9-106">Such an approach is costly and inefficient because it increases hardware costs and administrative overhead.</span></span>

<span data-ttu-id="860f9-107">Com+ löst dieses Problem durch Bereitstellen der com+-Partitions Funktion.</span><span class="sxs-lookup"><span data-stu-id="860f9-107">COM+ solves this problem by providing the COM+ partitions feature.</span></span> <span data-ttu-id="860f9-108">Sie können COM+-Partitionen verwenden, um unterschiedliche Versionen einer COM+-Anwendung auf einem Computer zu installieren und diese gleichzeitig auszuführen.</span><span class="sxs-lookup"><span data-stu-id="860f9-108">You can use COM+ partitions to install different versions of a COM+ application on a computer and run them simultaneously.</span></span>

<span data-ttu-id="860f9-109">Informationen zum Verständnis und zur Verwendung dieses Features finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="860f9-109">To understand and use this feature, see the following topics:</span></span>

-   [<span data-ttu-id="860f9-110">Was sind COM+-Partitionen?</span><span class="sxs-lookup"><span data-stu-id="860f9-110">What Are COM+ Partitions?</span></span>](what-are-com--partitions-.md)
-   [<span data-ttu-id="860f9-111">Partitions Implementierung</span><span class="sxs-lookup"><span data-stu-id="860f9-111">Partition Implementation</span></span>](partition-implementation.md)
-   [<span data-ttu-id="860f9-112">Registrieren und Aktivieren von Komponenten in Partitionen</span><span class="sxs-lookup"><span data-stu-id="860f9-112">Registering and Activating Components in Partitions</span></span>](registering-and-activating-components-in-partitions.md)
-   [<span data-ttu-id="860f9-113">Komponenten und Partitionen in der com+-Warteschlange</span><span class="sxs-lookup"><span data-stu-id="860f9-113">COM+ Queued Components and Partitions</span></span>](com--queued-components-and-partitions.md)
-   [<span data-ttu-id="860f9-114">Einschränkungen beim Anwendungs Entwurf</span><span class="sxs-lookup"><span data-stu-id="860f9-114">Application Design Restrictions</span></span>](application-design-restrictions.md)

## <a name="related-topics"></a><span data-ttu-id="860f9-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="860f9-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="860f9-116">Aufgaben für COM+-Partitionen</span><span class="sxs-lookup"><span data-stu-id="860f9-116">COM+ Partitions Tasks</span></span>](com--partitions-tasks.md)
</dt> </dl>

 

 




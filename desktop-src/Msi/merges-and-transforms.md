---
description: Der Windows Installer speichert alle Informationen zur Installation in einer relationalen Datenbank. Sie können diese Datenbank und somit die Installation mithilfe von Transformationen und Zusammenführungen ändern.
ms.assetid: 32163e06-d03d-4b65-b744-62f306f2100d
title: Zusammenführungen und Transformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aec6314e81afb5afa9d74346b64fe3129ba5ed30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349694"
---
# <a name="merges-and-transforms"></a><span data-ttu-id="9aa95-104">Zusammenführungen und Transformationen</span><span class="sxs-lookup"><span data-stu-id="9aa95-104">Merges and Transforms</span></span>

<span data-ttu-id="9aa95-105">Der Windows Installer speichert alle Informationen zur Installation in einer relationalen Datenbank.</span><span class="sxs-lookup"><span data-stu-id="9aa95-105">The Windows Installer keeps all information about the installation in a relational database.</span></span> <span data-ttu-id="9aa95-106">Sie können diese Datenbank und somit die Installation mithilfe von Transformationen und Zusammenführungen ändern.</span><span class="sxs-lookup"><span data-stu-id="9aa95-106">You can modify this database, and therefore the installation, by using transforms and merges.</span></span>

## <a name="transforms"></a><span data-ttu-id="9aa95-107">Transformationen</span><span class="sxs-lookup"><span data-stu-id="9aa95-107">Transforms</span></span>

<span data-ttu-id="9aa95-108">Eine [Daten Bank Transformation](database-transforms.md) fügt Elemente in der ursprünglichen Datenbank hinzu oder ersetzt Sie.</span><span class="sxs-lookup"><span data-stu-id="9aa95-108">A [database transform](database-transforms.md) adds or replaces elements in the original database.</span></span> <span data-ttu-id="9aa95-109">Eine Transformation kann z. b. den gesamten Text in der Benutzeroberfläche einer Anwendung von Französisch in Englisch ändern.</span><span class="sxs-lookup"><span data-stu-id="9aa95-109">For example, a transform can change all of the text in an application's user interface from French to English.</span></span>

<span data-ttu-id="9aa95-110">Zu den Haupt Verwendungsmöglichkeiten von Transformationen gehören:</span><span class="sxs-lookup"><span data-stu-id="9aa95-110">Primary uses for transforms include:</span></span>

-   <span data-ttu-id="9aa95-111">Anpassung der Basis Installationspakete für bestimmte Gruppen von Benutzern.</span><span class="sxs-lookup"><span data-stu-id="9aa95-111">Customization of base installation packages for particular groups of users.</span></span>

    <span data-ttu-id="9aa95-112">Transformationen können verwendet werden, um die verschiedenen Anpassungen eines einzelnen Basispakets zu kapseln, die von verschiedenen Benutzergruppen benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="9aa95-112">Transforms can be used to encapsulate the various customizations of a single base package that are required by different groups of users.</span></span> <span data-ttu-id="9aa95-113">Dies ist z. b. in Organisationen hilfreich, in denen die Support Abteilung für Finanzabteilung und Personal verschiedene Installationen eines bestimmten Produkts erfordert.</span><span class="sxs-lookup"><span data-stu-id="9aa95-113">For example, this is useful in organizations where the finance and staff support departments require different installations of a particular product.</span></span> <span data-ttu-id="9aa95-114">Das Basispaket eines Produkts kann allen Benutzern an einem administrativen Installations Punkt zur Verfügung gestellt werden, wobei die entsprechenden Anpassungen separat an jede Benutzergruppe verteilt werden.</span><span class="sxs-lookup"><span data-stu-id="9aa95-114">A product's base package can be available to everyone at one administrative installation point with appropriate customizations distributed to each group of users separately.</span></span>

-   <span data-ttu-id="9aa95-115">Sprachübergreifende Synchronisierung von Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="9aa95-115">Synchronization of applications across languages.</span></span>

    <span data-ttu-id="9aa95-116">Transformationen sind nützlich, um Pakete, die an weit verbreiteten Positionen erstellt wurden, während der Erstellung synchronisiert zu halten.</span><span class="sxs-lookup"><span data-stu-id="9aa95-116">Transforms are useful for keeping packages authored at widely separated locations synchronized during authoring.</span></span> <span data-ttu-id="9aa95-117">Wenn beispielsweise ein Upgrade zuerst für eine englische Version einer Anwendung entwickelt wird, die auf Englisch und Französisch vorhanden ist, kann eine Transformation auf die aktualisierte englische Version angewendet werden, die Sie in eine aktualisierte französische Version konvertiert.</span><span class="sxs-lookup"><span data-stu-id="9aa95-117">For example, if an upgrade is first developed for an English version of an application that exists in English and French, a transform can be applied to the upgraded English version that converts it into an upgraded French version.</span></span>

    <span data-ttu-id="9aa95-118">Mehrere Transformationen können auf ein Basispaket angewendet und dann während der Installation dynamisch angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="9aa95-118">Multiple transforms can be applied to a base package and then applied on-the-fly during installation.</span></span> <span data-ttu-id="9aa95-119">Dies erweitert die Funktionen des Installers zum Erstellen von benutzerdefinierten Paketen und bietet einen Mechanismus, mit dem die am besten geeigneten Installationen den verschiedenen Benutzergruppen effizient zugewiesen werden können.</span><span class="sxs-lookup"><span data-stu-id="9aa95-119">This extends the capabilities of the installer to create custom packages and provides a mechanism for efficiently assigning the most appropriate installations to different groups of users.</span></span>

-   <span data-ttu-id="9aa95-120">Patchen von Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="9aa95-120">Patching applications.</span></span>

    <span data-ttu-id="9aa95-121">Transformationen können verwendet werden, um eine geringfügige Korrektur für eine Anwendung anzuwenden, die kein großes Upgrade rechtfertigt.</span><span class="sxs-lookup"><span data-stu-id="9aa95-121">Transforms can be used to apply a minor fix to an application that does not warrant a major upgrade.</span></span> <span data-ttu-id="9aa95-122">Weitere Informationen zu Patches finden Sie unter [Patch-Pakete](patch-packages.md).</span><span class="sxs-lookup"><span data-stu-id="9aa95-122">For more information about patches, see [Patch Packages](patch-packages.md).</span></span>

## <a name="merges"></a><span data-ttu-id="9aa95-123">Merges</span><span class="sxs-lookup"><span data-stu-id="9aa95-123">Merges</span></span>

<span data-ttu-id="9aa95-124">Ein Merge kombiniert zwei Datenbanken zu einer Datenbank und fügt Informationen hinzu, anstatt Sie zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="9aa95-124">A merge combines two databases into one database, and adds, rather than replaces, information.</span></span> <span data-ttu-id="9aa95-125">Wenn die gleichen Informationen in beiden Datenbanken vorhanden sind, tritt ein Mergekonflikt auf.</span><span class="sxs-lookup"><span data-stu-id="9aa95-125">If the same information exists in both databases, a merge conflict occurs.</span></span> <span data-ttu-id="9aa95-126">Zusammenführungen sind für Entwicklungsteams nützlich, da Sie es ermöglichen, eine große Anwendung in Teile zu unterteilen, die später erneut kombiniert werden können.</span><span class="sxs-lookup"><span data-stu-id="9aa95-126">Merges are useful to development teams because they allow a large application to be divided into parts that can be recombined later.</span></span> <span data-ttu-id="9aa95-127">Beispielsweise können die Datenbankelemente für die Installation einer neuen Komponente separat und später in der Haupt Installations Datenbank zusammengeführt werden.</span><span class="sxs-lookup"><span data-stu-id="9aa95-127">For example, the database elements for the installation of a new component can be developed separately and later merged into the main installation database.</span></span> <span data-ttu-id="9aa95-128">Weitere Informationen finden Sie unter zusammen [führen von Modulen](merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="9aa95-128">For more information, see [Merge Modules](merge-modules.md).</span></span>

<span data-ttu-id="9aa95-129">Ein Entwicklungsteam kann einen Zusammenarbeits Vorgang folgendermaßen anwenden:</span><span class="sxs-lookup"><span data-stu-id="9aa95-129">A development team might apply a merge operation in the following way:</span></span>

1.  <span data-ttu-id="9aa95-130">Trennen Sie die Gruppen, und arbeiten Sie gleichzeitig an verschiedenen Komponenten einer großen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="9aa95-130">Separate into groups and work simultaneously on different components of a large application.</span></span>
2.  <span data-ttu-id="9aa95-131">Jede Entwicklungsgruppe füllt dann eine Datenbank mit Installationsinformationen für die eigene Komponente auf, ohne dass Sie sich mit den anderen Komponenten der Anwendung beschäftigt.</span><span class="sxs-lookup"><span data-stu-id="9aa95-131">Each development group then populates a database with installation information for its own component, without being concerned with the other components of the application.</span></span>
3.  <span data-ttu-id="9aa95-132">Nachdem die Entwicklung einer Komponente vollständig ist, kann die Datenbank dieser Komponente in der Haupt Installations Datenbank für die gesamte Anwendung zusammengeführt werden.</span><span class="sxs-lookup"><span data-stu-id="9aa95-132">After the development of a component is complete, that component's database can be merged into the main installation database for the entire application.</span></span>

 

 




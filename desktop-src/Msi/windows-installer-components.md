---
description: Eine Komponente ist ein Teil der zu installierenden Anwendung oder des Produkts.
ms.assetid: f1c9696d-3267-44be-a904-ab26250fae2e
title: Windows Installer Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad90f2fb576d0333a26fc92f9cf951e4da06bab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960031"
---
# <a name="windows-installer-components"></a><span data-ttu-id="c7abd-103">Windows Installer Komponenten</span><span class="sxs-lookup"><span data-stu-id="c7abd-103">Windows Installer Components</span></span>

<span data-ttu-id="c7abd-104">Eine Komponente ist ein Teil der zu installierenden Anwendung oder des Produkts.</span><span class="sxs-lookup"><span data-stu-id="c7abd-104">A component is a piece of the application or product to be installed.</span></span> <span data-ttu-id="c7abd-105">Beispiele für Komponenten sind einzelne Dateien, eine Gruppe verwandter Dateien, com-Objekte, Registrierungen, Registrierungsschlüssel, Verknüpfungen, Ressourcen, in einem Verzeichnis gruppierte Bibliotheken oder freigegebene Code Elemente wie MFC oder DAO.</span><span class="sxs-lookup"><span data-stu-id="c7abd-105">Examples of components include single files, a group of related files, COM objects, registration, registry keys, shortcuts, resources, libraries grouped into a directory, or shared pieces of code such as MFC or DAO.</span></span>

<span data-ttu-id="c7abd-106">Der Installer-Dienst installiert oder entfernt eine Komponente als einzelner zusammenhängendes Element.</span><span class="sxs-lookup"><span data-stu-id="c7abd-106">The installer service installs or removes a component as a single coherent piece.</span></span> <span data-ttu-id="c7abd-107">Alle Komponenten werden nach der jeweiligen Komponenten-ID-GUID, die in der ComponentID-Spalte der [Component-Tabelle](component-table.md)angegeben ist, nachverfolgt.</span><span class="sxs-lookup"><span data-stu-id="c7abd-107">It tracks every component by the respective component ID GUID specified in the ComponentId column of the [Component table](component-table.md).</span></span>

> [!Note]  
> <span data-ttu-id="c7abd-108">Zwei Komponenten, die dieselbe Komponenten-ID verwenden, werden unabhängig von Ihrem tatsächlichen Inhalt als mehrere Instanzen derselben Komponente behandelt.</span><span class="sxs-lookup"><span data-stu-id="c7abd-108">Two components that share the same component ID are treated as multiple instances of the same component regardless of their actual content.</span></span> <span data-ttu-id="c7abd-109">Auf dem Computer eines Benutzers ist nur eine einzelne Instanz einer Komponente installiert.</span><span class="sxs-lookup"><span data-stu-id="c7abd-109">Only a single instance of any component is installed on a user's computer.</span></span> <span data-ttu-id="c7abd-110">Mehrere Features oder Anwendungen können daher einige Komponenten gemeinsam nutzen.</span><span class="sxs-lookup"><span data-stu-id="c7abd-110">Several features or applications may therefore share some components.</span></span>

 

<span data-ttu-id="c7abd-111">Da Komponenten im allgemeinen gemeinsam genutzt werden, muss der Autor eines Installationspakets strenge Regeln befolgen, wenn die Komponenten eines Features oder einer Anwendung angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c7abd-111">Because components are commonly shared, the author of an installation package must follow strict rules when specifying the components of a feature or application.</span></span> <span data-ttu-id="c7abd-112">Dies ist für den ordnungsgemäßen Betrieb des Windows Installer Verweis Zählmechanismus entscheidend.</span><span class="sxs-lookup"><span data-stu-id="c7abd-112">This is essential for the correct operation of the Windows Installer reference-counting mechanism.</span></span> <span data-ttu-id="c7abd-113">Weitere Informationen finden Sie unter [Organisieren von Anwendungen in Komponenten](organizing-applications-into-components.md).</span><span class="sxs-lookup"><span data-stu-id="c7abd-113">For more information, see [Organizing Applications into Components](organizing-applications-into-components.md).</span></span>

<span data-ttu-id="c7abd-114">Diese Regeln sind:</span><span class="sxs-lookup"><span data-stu-id="c7abd-114">In brief, these rules are:</span></span>

-   <span data-ttu-id="c7abd-115">Jede Komponente muss in einem einzelnen Ordner gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="c7abd-115">Each component must be stored in a single folder.</span></span>
-   <span data-ttu-id="c7abd-116">Es sollten nie Dateien, Registrierungseinträge, Verknüpfungen oder andere Ressourcen als Mitglied von mehr als einer Komponente ausgeliefert werden.</span><span class="sxs-lookup"><span data-stu-id="c7abd-116">No file, registry entry, shortcut, or other resources should ever be shipped as a member of more than one component.</span></span> <span data-ttu-id="c7abd-117">Dies gilt für Produkte, Produktversionen und Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="c7abd-117">This applies across products, product versions, and companies.</span></span>

<span data-ttu-id="c7abd-118">Weitere Informationen zur Verwendung von-Komponenten finden Sie unter.</span><span class="sxs-lookup"><span data-stu-id="c7abd-118">For more information about using components, see</span></span>

-   [<span data-ttu-id="c7abd-119">Installieren einer fehlenden Komponente</span><span class="sxs-lookup"><span data-stu-id="c7abd-119">Installing a Missing Component</span></span>](installing-a-missing-component.md)
-   [<span data-ttu-id="c7abd-120">Installieren von permanenten Komponenten, Dateien, Schriftarten, Registrierungs Schlüsseln</span><span class="sxs-lookup"><span data-stu-id="c7abd-120">Installing Permanent Components, Files, Fonts, Registry Keys</span></span>](installing-permanent-components-files-fonts-registry-keys.md)
-   [<span data-ttu-id="c7abd-121">Verwenden qualifizierter Komponenten</span><span class="sxs-lookup"><span data-stu-id="c7abd-121">Using Qualified Components</span></span>](using-qualified-components.md)
-   [<span data-ttu-id="c7abd-122">Verwenden transitiv Komponenten</span><span class="sxs-lookup"><span data-stu-id="c7abd-122">Using Transitive Components</span></span>](using-transitive-components.md)
-   [<span data-ttu-id="c7abd-123">Arbeiten mit Features und Komponenten</span><span class="sxs-lookup"><span data-stu-id="c7abd-123">Working with Features and Components</span></span>](working-with-features-and-components.md)
-   [<span data-ttu-id="c7abd-124">Erstellen eines großen Pakets</span><span class="sxs-lookup"><span data-stu-id="c7abd-124">Authoring a Large Package</span></span>](authoring-a-large-package.md)
-   [<span data-ttu-id="c7abd-125">Überprüfen der Installation von Features, Komponenten, Dateien</span><span class="sxs-lookup"><span data-stu-id="c7abd-125">Checking the Installation of Features, Components, Files</span></span>](checking-the-installation-of-features-components-files.md)
-   [<span data-ttu-id="c7abd-126">Suchen nach einer unterbrochenen Funktion oder Komponente</span><span class="sxs-lookup"><span data-stu-id="c7abd-126">Searching for a Broken Feature or Component</span></span>](searching-for-a-broken-feature-or-component.md)
-   [<span data-ttu-id="c7abd-127">Veröffentlichen von Produkten, Features und Komponenten</span><span class="sxs-lookup"><span data-stu-id="c7abd-127">Publishing Products, Features, and Components</span></span>](publishing-products-features-and-components.md)

 

 




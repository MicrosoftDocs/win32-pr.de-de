---
description: Installationspakete für COM+-Anwendungen werden erstellt.
ms.assetid: 3ef7b280-b521-4cd2-9906-013c9dfe16ab
title: Installationspakete für COM+-Anwendungen werden erstellt.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ec34852ab405d965fa1ad8f8fb5892616d1347
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346641"
---
# <a name="creating-installation-packages-for-com-applications"></a><span data-ttu-id="0c2cc-103">Installationspakete für COM+-Anwendungen werden erstellt.</span><span class="sxs-lookup"><span data-stu-id="0c2cc-103">Creating Installation Packages for COM+ Applications</span></span>

<span data-ttu-id="0c2cc-104">Mit dem Verwaltungs Programmkomponenten Dienste oder der com+-Verwaltungs Bibliothek können Sie Installationspakete für COM+-Anwendungen und Anwendungs Proxys erstellen.</span><span class="sxs-lookup"><span data-stu-id="0c2cc-104">You can use the Component Services administrative tool or the COM+ Administration Library to create installation packages for COM+ applications and application proxies.</span></span>

<span data-ttu-id="0c2cc-105">Com+ generiert Windows Installer Installationspakete, die in einer einzigen Datei alle erforderlichen Komponenten zum Installieren einer COM+-Anwendung auf einem anderen Computer enthalten.</span><span class="sxs-lookup"><span data-stu-id="0c2cc-105">COM+ generates Windows Installer installation packages, which in a single file contain all the necessary pieces to install a COM+ application on another computer.</span></span>

<span data-ttu-id="0c2cc-106">Beim Exportieren einer COM+-Anwendung bestimmt das Verwaltungs Programmkomponenten Dienste den Satz von Klassen, Komponenten und deren Attributen der Anwendung sowie Attribute auf Anwendungsebene.</span><span class="sxs-lookup"><span data-stu-id="0c2cc-106">When exporting a COM+ application, the Component Services administrative tool determines the application's set of classes, components, and their attributes, as well as application-level attributes.</span></span> <span data-ttu-id="0c2cc-107">Aus diesen Informationen generiert das Verwaltungs Programmkomponenten Dienste eine einzelne MSI-Datei, die Folgendes enthält:</span><span class="sxs-lookup"><span data-stu-id="0c2cc-107">From this information, the Component Services administrative tool generates a single .msi file, which contains the following:</span></span>

-   <span data-ttu-id="0c2cc-108">Windows Installer Tabellen mit com-Registrierungsinformationen (Weitere Informationen finden Sie in der Windows Installer Dokumentation).</span><span class="sxs-lookup"><span data-stu-id="0c2cc-108">Windows Installer tables with COM registration information (see the Windows Installer documentation for details).</span></span>
-   <span data-ttu-id="0c2cc-109">Eine APL-Datei, die die Attribute der Anwendung enthält.</span><span class="sxs-lookup"><span data-stu-id="0c2cc-109">An .apl file containing the application's attributes.</span></span> <span data-ttu-id="0c2cc-110">(Hierbei handelt es sich um eine interne Datei; das Format dieser Datei ist nicht dokumentiert.)</span><span class="sxs-lookup"><span data-stu-id="0c2cc-110">(This is an internal file; the format of this file is not documented.)</span></span>
-   <span data-ttu-id="0c2cc-111">DLLs und Typbibliotheken, die die Schnittstellen beschreiben, die von den Klassen der com+-Anwendung implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="0c2cc-111">DLLs and type libraries that describe the interfaces implemented by the COM+ application's classes.</span></span>

<span data-ttu-id="0c2cc-112">Neben der MSI-Datei generiert das Verwaltungs Programmkomponenten Dienste eine CAB-Datei.</span><span class="sxs-lookup"><span data-stu-id="0c2cc-112">In addition to the .msi file, the Component Services administrative tool generates a cabinet (.cab) file.</span></span> <span data-ttu-id="0c2cc-113">Diese Datei dient als Wrapper für die MSI-Datei und ermöglicht dem Entwickler die Bereitstellung der com+-Anwendung über Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="0c2cc-113">This file wraps the .msi file, allowing the developer to deploy the COM+ application through Microsoft Internet Explorer.</span></span>

> [!Note]  
> <span data-ttu-id="0c2cc-114">Beim Exportieren einer COM+-Anwendung verpackt das Verwaltungs Programmkomponenten Dienste nur die com+-Standardteile der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="0c2cc-114">When exporting a COM+ application, the Component Services administrative tool packages only the standard COM+ parts of the application.</span></span> <span data-ttu-id="0c2cc-115">Es werden z. b. keine abhängigen DLL-Dateien oder Datendateien paketieren.</span><span class="sxs-lookup"><span data-stu-id="0c2cc-115">It does not package, for example, any dependent DLL or data files.</span></span> <span data-ttu-id="0c2cc-116">Vor der Installation der com+-Anwendung müssen die abhängigen DLL-Dateien zuerst auf einem Computer installiert werden.</span><span class="sxs-lookup"><span data-stu-id="0c2cc-116">The dependent DLL files must first be installed on a computer prior to installing the COM+ application.</span></span> <span data-ttu-id="0c2cc-117">Alternativ können Sie das Windows Installer Authoring Tool verwenden, um diese abhängigen Dateien der MSI-Datei hinzuzufügen, die vom Verwaltungs Programmkomponenten Dienste generiert wird.</span><span class="sxs-lookup"><span data-stu-id="0c2cc-117">Alternatively, you can use the Windows Installer authoring tool to add these dependent files to the .msi file generated by the Component Services administrative tool.</span></span> <span data-ttu-id="0c2cc-118">(Ausführliche Informationen finden Sie in der Windows Installer-Dokumentation.)</span><span class="sxs-lookup"><span data-stu-id="0c2cc-118">(See the Windows Installer documentation for details.)</span></span>

 

## <a name="installing-com-applications-on-other-computers"></a><span data-ttu-id="0c2cc-119">Installieren von com+-Anwendungen auf anderen Computern</span><span class="sxs-lookup"><span data-stu-id="0c2cc-119">Installing COM+ Applications on Other Computers</span></span>

<span data-ttu-id="0c2cc-120">Die vom Verwaltungs Programmkomponenten Dienste generierte Windows Installer Datei (. msi) kann verwendet werden, um die COM+-Anwendung auf einem anderen Computer zu installieren.</span><span class="sxs-lookup"><span data-stu-id="0c2cc-120">The Windows Installer (.msi) file generated by the Component Services administrative tool can be used to install the COM+ application on another computer.</span></span> <span data-ttu-id="0c2cc-121">Die MSI-Datei, die eine COM+-Anwendung enthält, kann nur auf Computern installiert werden, die com+-Dienste unterstützen.</span><span class="sxs-lookup"><span data-stu-id="0c2cc-121">The .msi file containing a COM+ application can be installed only on computers that support COM+ services.</span></span> <span data-ttu-id="0c2cc-122">Ausführliche Verfahren zum Bereitstellen von com+-Anwendungen finden Sie unter "Installieren von com+-Anwendungen" in der Hilfe zur Verwaltung von Komponenten Diensten.</span><span class="sxs-lookup"><span data-stu-id="0c2cc-122">For detailed procedures on deploying COM+ applications, see "Installing COM+ Applications," in the Component Services Administration Help.</span></span>

<span data-ttu-id="0c2cc-123">Wenn die MSI-Datei nicht mit einem Windows Installer Authoring Tool geändert wird, werden mithilfe der Windows Installer installierte COM+-Anwendungen in der Systemsteuerung Software angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0c2cc-123">Unless the .msi file is modified using a Windows Installer authoring tool, COM+ applications installed by using the Windows Installer appear in the Add/Remove Programs control panel.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0c2cc-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0c2cc-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c2cc-125">Anwendungs Proxys</span><span class="sxs-lookup"><span data-stu-id="0c2cc-125">Deploying Application Proxies</span></span>](deploying-application-proxies.md)
</dt> <dt>

[<span data-ttu-id="0c2cc-126">Der com+-Katalog</span><span class="sxs-lookup"><span data-stu-id="0c2cc-126">The COM+ Catalog</span></span>](the-com--catalog.md)
</dt> </dl>

 

 




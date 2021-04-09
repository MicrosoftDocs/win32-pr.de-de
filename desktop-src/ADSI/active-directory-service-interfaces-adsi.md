---
title: Active Directory Service Interfaces
description: Einführung in Active Directory Services-Schnittstellen mit Links zu verschiedenen Handbüchern.
ms.assetid: b24f9789-b9f5-49c4-9812-298bae8b28a9
ms.tgt_platform: multiple
keywords:
- ADSI ADSI
- Active Directory Dienst Schnittstellen (siehe ADSI)
- ADSI ADSI, Startseite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15cc702fec86f1202f1fbd00ba575fd848e4ab74
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039605"
---
# <a name="active-directory-service-interfaces"></a><span data-ttu-id="6b7df-106">Active Directory Service Interfaces</span><span class="sxs-lookup"><span data-stu-id="6b7df-106">Active Directory Service Interfaces</span></span>

## <a name="purpose"></a><span data-ttu-id="6b7df-107">Zweck</span><span class="sxs-lookup"><span data-stu-id="6b7df-107">Purpose</span></span>

<span data-ttu-id="6b7df-108">Active Directory Service Interfaces (ADSI) ist ein Satz von COM-Schnittstellen, die für den Zugriff auf die Funktionen der Verzeichnisdienste von unterschiedlichen Netzwerkanbietern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6b7df-108">Active Directory Service Interfaces (ADSI) is a set of COM interfaces used to access the features of directory services from different network providers.</span></span> <span data-ttu-id="6b7df-109">ADSI wird in einer verteilten Computerumgebung verwendet, um einen einzelnen Satz von Verzeichnisdienst Schnittstellen für die Verwaltung von Netzwerkressourcen zu präsentieren.</span><span class="sxs-lookup"><span data-stu-id="6b7df-109">ADSI is used in a distributed computing environment to present a single set of directory service interfaces for managing network resources.</span></span> <span data-ttu-id="6b7df-110">Administratoren und Entwickler können ADSI-Dienste verwenden, um die Ressourcen in einem Verzeichnisdienst aufzulisten und zu verwalten, unabhängig davon, welche Netzwerkumgebung die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="6b7df-110">Administrators and developers can use ADSI services to enumerate and manage the resources in a directory service, no matter which network environment contains the resource.</span></span>

<span data-ttu-id="6b7df-111">ADSI ermöglicht allgemeine Verwaltungsaufgaben, z. b. das Hinzufügen neuer Benutzer, das Verwalten von Druckern und das Auffinden von Ressourcen in einer verteilten Computerumgebung.</span><span class="sxs-lookup"><span data-stu-id="6b7df-111">ADSI enables common administrative tasks, such as adding new users, managing printers, and locating resources in a distributed computing environment.</span></span>

> [!Note]  
> <span data-ttu-id="6b7df-112">Die folgende Dokumentation ist für Computerprogrammierer vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="6b7df-112">The following documentation is for computer programmers.</span></span> <span data-ttu-id="6b7df-113">Wenn Sie ein Endbenutzer versuchen, ein Druckfehler oder ein Problem mit dem Heimnetzwerk zu debuggen, finden Sie weitere Informationen in den [Microsoft Community-Foren](https://answers.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="6b7df-113">If you are an end-user trying to debug a printing error or home network issue, see the [Microsoft community forums](https://answers.microsoft.com).</span></span>

 

## <a name="where-applicable"></a><span data-ttu-id="6b7df-114">Anwendungsbereich</span><span class="sxs-lookup"><span data-stu-id="6b7df-114">Where applicable</span></span>

<span data-ttu-id="6b7df-115">Netzwerkadministratoren können mit ADSI häufige Aufgaben automatisieren, z. b. das Hinzufügen von Benutzern und Gruppen, das Verwalten von Druckern und das Festlegen von Berechtigungen für Netzwerkressourcen.</span><span class="sxs-lookup"><span data-stu-id="6b7df-115">Network Administrators can use ADSI to automate common tasks, such as adding users and groups, managing printers, and setting permissions on network resources.</span></span>

<span data-ttu-id="6b7df-116">Unabhängige Software Hersteller und Entwickler von Endbenutzern können ADSI als "Verzeichnis Aktivierung" für Ihre Produkte und Anwendungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="6b7df-116">Independent Software Vendors and end-user developers can use ADSI to "directory enable" their products and applications.</span></span> <span data-ttu-id="6b7df-117">Dienste können sich selbst in einem Verzeichnis veröffentlichen, Clients können das Verzeichnis zum Suchen der Dienste verwenden, und beide können das Verzeichnis verwenden, um andere Objekte zu suchen und zu bearbeiten, die von Interesse sind.</span><span class="sxs-lookup"><span data-stu-id="6b7df-117">Services can publish themselves in a directory, clients can use the directory to find the services, and both can use the directory to find and manipulate other objects of interest.</span></span> <span data-ttu-id="6b7df-118">Da Active Directory Dienst Schnittstellen unabhängig von den zugrunde liegenden Verzeichnisdiensten sind, können Verzeichnis aktivierte Produkte und Anwendungen in mehreren Netzwerk-und Verzeichnis Umgebungen erfolgreich ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6b7df-118">Because Active Directory Service Interfaces are independent of the underlying directory service(s), directory-enabled products and applications can operate successfully in multiple network and directory environments.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="6b7df-119">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="6b7df-119">Developer audience</span></span>

<span data-ttu-id="6b7df-120">Sie können in vielen Sprachen ADSI-Client Anwendungen schreiben.</span><span class="sxs-lookup"><span data-stu-id="6b7df-120">You can write ADSI client applications in many languages.</span></span> <span data-ttu-id="6b7df-121">Für die meisten administrativen Aufgaben definiert ADSI Schnittstellen und Objekte, auf die von Automatisierungs kompatiblen Sprachen wie Microsoft Visual Basic, Microsoft Visual Basic Scripting Edition (VBScript) und Java aus zugegriffen werden kann, um die leistungsstärker und effizientere Sprache wie C und C++ zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6b7df-121">For most administrative tasks, ADSI defines interfaces and objects accessible from Automation-compliant languages like Microsoft Visual Basic, Microsoft Visual Basic Scripting Edition (VBScript), and Java to the more performance and efficiency-conscious languages such as C and C++.</span></span> <span data-ttu-id="6b7df-122">Eine gute Grundlage bei der com-Programmierung ist für den ADSI-Programmierer von nutzen.</span><span class="sxs-lookup"><span data-stu-id="6b7df-122">A good foundation in COM programming is useful to the ADSI programmer.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="6b7df-123">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="6b7df-123">Run-time requirements</span></span>

<span data-ttu-id="6b7df-124">Active Directory wird auf Windows Server-Domänen Controllern ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6b7df-124">Active Directory runs on Windows Server domain controllers.</span></span> <span data-ttu-id="6b7df-125">Allerdings können Client Anwendungen mit ADSI in Windows geschrieben und ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6b7df-125">However, client applications using ADSI may be written and run on Windows.</span></span> <span data-ttu-id="6b7df-126">Außerdem benötigen Entwickler das Platform Software Development Kit (SDK), das auch auf der MSDN-Website verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="6b7df-126">In addition, developers will want the Platform Software Development Kit (SDK), also available on the MSDN website.</span></span> <span data-ttu-id="6b7df-127">Verwenden Sie das MMC-Snap-in "Active Directory-Benutzer und-Computer", um den Inhalt Active Directory zu untersuchen.</span><span class="sxs-lookup"><span data-stu-id="6b7df-127">To investigate the contents of Active Directory, use the Active Directory Users and Computers MMC snap-in.</span></span> <span data-ttu-id="6b7df-128">Dieses Snap-in ersetzt das adsvw-Tool, das für vorherige Versionen von Windows verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="6b7df-128">This snap-in replaces the Adsvw tool that was available for previous versions of Windows.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6b7df-129">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="6b7df-129">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="6b7df-130">Informationen zu ADSI</span><span class="sxs-lookup"><span data-stu-id="6b7df-130">About ADSI</span></span>](about-adsi.md)
</dt> <dd>

<span data-ttu-id="6b7df-131">Allgemeine Informationen zu ADSI.</span><span class="sxs-lookup"><span data-stu-id="6b7df-131">General information about ADSI.</span></span>

</dd> <dt>

[<span data-ttu-id="6b7df-132">Verwenden von ADSI</span><span class="sxs-lookup"><span data-stu-id="6b7df-132">Using ADSI</span></span>](using-adsi.md)
</dt> <dd>

<span data-ttu-id="6b7df-133">Programmier Handbuch für die Verwendung von ADSI.</span><span class="sxs-lookup"><span data-stu-id="6b7df-133">Programmer's Guide to using ADSI.</span></span>

</dd> <dt>

[<span data-ttu-id="6b7df-134">ADSI-Schnellstart-Tutorials</span><span class="sxs-lookup"><span data-stu-id="6b7df-134">ADSI Quick-start Tutorials</span></span>](adsi-quick-start-tutorials.md)
</dt> <dd>

<span data-ttu-id="6b7df-135">Verwenden von ADSI mit Automation zum Verwalten von Verzeichnissen.</span><span class="sxs-lookup"><span data-stu-id="6b7df-135">Using ADSI with Automation to manage directories.</span></span>

</dd> <dt>

[<span data-ttu-id="6b7df-136">ADSI-Referenz</span><span class="sxs-lookup"><span data-stu-id="6b7df-136">ADSI Reference</span></span>](adsi-reference.md)
</dt> <dd>

<span data-ttu-id="6b7df-137">Dokumentation zu ADSI-Schnittstellen und-Methoden.</span><span class="sxs-lookup"><span data-stu-id="6b7df-137">Documentation of ADSI interfaces and methods.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="6b7df-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6b7df-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b7df-139">Das Component Object Model</span><span class="sxs-lookup"><span data-stu-id="6b7df-139">The Component Object Model</span></span>](../com/the-component-object-model.md)
</dt> <dt>

[<span data-ttu-id="6b7df-140">COM-Clients und-Server</span><span class="sxs-lookup"><span data-stu-id="6b7df-140">COM Clients and Servers</span></span>](../com/com-clients-and-servers.md)
</dt> <dt>

[<span data-ttu-id="6b7df-141">Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="6b7df-141">Active Directory Domain Services</span></span>](../ad/active-directory-domain-services.md)
</dt> </dl>

 

 
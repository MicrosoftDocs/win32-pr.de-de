---
title: Informationen zu Active Directory Dienst Schnittstellen
description: Active Directory Service Interfaces (ADSI) abstrahiert die Funktionen der Verzeichnisdienste von unterschiedlichen Netzwerkanbietern in einer verteilten Computerumgebung, um eine einzelne Gruppe von Verzeichnisdienst Schnittstellen für die Verwaltung von Netzwerkressourcen bereitzustellen.
ms.assetid: 6d601af5-7470-42c2-b99e-21174ea008b1
ms.tgt_platform: multiple
keywords:
- Informationen zu Active Directory Dienst Schnittstellen ADSI
- ADSI ADSI, Informationen zu
- Active Directory Dienst Schnittstellen ADSI, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc083b33a633335da12915257fcddff1174a6858
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100586"
---
# <a name="about-active-directory-service-interfaces"></a><span data-ttu-id="9442c-106">Informationen zu Active Directory Dienst Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="9442c-106">About Active Directory Service Interfaces</span></span>

<span data-ttu-id="9442c-107">Active Directory Service Interfaces (ADSI) abstrahiert die Funktionen der Verzeichnisdienste von unterschiedlichen Netzwerkanbietern in einer verteilten Computerumgebung, um eine einzelne Gruppe von Verzeichnisdienst Schnittstellen für die Verwaltung von Netzwerkressourcen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9442c-107">Active Directory Service Interfaces (ADSI) abstracts the capabilities of directory services from different network providers in a distributed computing environment to present a single set of directory service interfaces for managing network resources.</span></span> <span data-ttu-id="9442c-108">Administratoren und Entwickler können ADSI-Dienste verwenden, um die Ressourcen in einem Verzeichnisdienst aufzulisten und zu verwalten, unabhängig davon, welche Netzwerkumgebung die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="9442c-108">Administrators and developers can use ADSI services to enumerate and manage the resources in a directory service, no matter which network environment contains the resource.</span></span>

<span data-ttu-id="9442c-109">ADSI vereinfacht das Ausführen allgemeiner Verwaltungsaufgaben, z. b. das Hinzufügen neuer Benutzer, das Verwalten von Druckern und das Auffinden von Ressourcen in der verteilten Computerumgebung.</span><span class="sxs-lookup"><span data-stu-id="9442c-109">ADSI makes it easier to perform common administrative tasks, such as adding new users, managing printers, and locating resources throughout the distributed computing environment.</span></span>

<span data-ttu-id="9442c-110">ADSI erleichtert Entwicklern das "Verzeichnis aktivieren" Ihrer Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="9442c-110">ADSI makes it easy for developers to "directory enable" their applications.</span></span> <span data-ttu-id="9442c-111">Administratoren und Entwickler verarbeiten einen einzelnen Satz von Verzeichnisdienst Schnittstellen, unabhängig davon, welche Verzeichnisdienste installiert sind.</span><span class="sxs-lookup"><span data-stu-id="9442c-111">Administrators and developers handle a single set of directory service interfaces, regardless of which directory services are installed.</span></span>

<span data-ttu-id="9442c-112">In dieser Einführung werden die folgenden Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="9442c-112">The following topics are discussed in this introduction:</span></span>

-   [<span data-ttu-id="9442c-113">Mehrere Verzeichnisdienste</span><span class="sxs-lookup"><span data-stu-id="9442c-113">Multiple Directory Services</span></span>](multiple-directory-services.md)
-   [<span data-ttu-id="9442c-114">Wer wird Active Directory Dienst Schnittstellen verwenden?</span><span class="sxs-lookup"><span data-stu-id="9442c-114">Who Will Use Active Directory Service Interfaces?</span></span>](who-will-use-active-directory-service-interfaces.md)
-   [<span data-ttu-id="9442c-115">Verzeichnisdienste heute</span><span class="sxs-lookup"><span data-stu-id="9442c-115">Directory Services Today</span></span>](directory-services-today.md)
-   [<span data-ttu-id="9442c-116">Vorteile der Verwendung von Active Directory Dienst Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="9442c-116">Benefits of Using Active Directory Service Interfaces</span></span>](benefits-of-using-active-directory-service-interfaces.md)
-   [<span data-ttu-id="9442c-117">Architektur von Active Directory-Dienst Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="9442c-117">Active Directory Service Interfaces Architecture</span></span>](active-directory-service-interfaces-architecture.md)
-   [<span data-ttu-id="9442c-118">Unterstützung für Programmiersprachen</span><span class="sxs-lookup"><span data-stu-id="9442c-118">Programming Language Support</span></span>](programming-language-support.md)
-   [<span data-ttu-id="9442c-119">ADSI-Eigenschaften und-Attribute</span><span class="sxs-lookup"><span data-stu-id="9442c-119">ADSI Properties and Attributes</span></span>](adsi-properties-and-attributes.md)

## <a name="what-you-should-know-before-reading-this-guide"></a><span data-ttu-id="9442c-120">Was Sie vor dem Lesen dieses Handbuchs wissen sollten</span><span class="sxs-lookup"><span data-stu-id="9442c-120">What You Should Know Before Reading This Guide</span></span>

<span data-ttu-id="9442c-121">In diesem Leitfaden wird davon ausgegangen, dass Sie mit dem Component Object Model (com) und der Automatisierung vertraut sind und dass Sie wissen, wie Sie in Visual Basic oder C/C++ programmieren können.</span><span class="sxs-lookup"><span data-stu-id="9442c-121">This guide assumes that you are familiar with the Component Object Model (COM) and Automation, and that you know how to program in either Visual Basic or C/C++.</span></span>

<span data-ttu-id="9442c-122">Einige der in diesem Handbuch verwendeten Begriffe sind entweder für ADSI oder die Verzeichnisdienst Umgebung eindeutig.</span><span class="sxs-lookup"><span data-stu-id="9442c-122">Some of the terms used in this guide are unique to either ADSI or the directory services environment.</span></span> <span data-ttu-id="9442c-123">Andere Begriffe sind zwar vertraut, haben aber möglicherweise eine etwas andere Bedeutung in diesen Umgebungen.</span><span class="sxs-lookup"><span data-stu-id="9442c-123">Other terms will be familiar but may have slightly different meanings in these environments.</span></span>

## <a name="further-reading-about-adsi-and-related-topics"></a><span data-ttu-id="9442c-124">Weitere Informationen zu ADSI und verwandten Themen</span><span class="sxs-lookup"><span data-stu-id="9442c-124">Further Reading about ADSI and Related Topics</span></span>

<span data-ttu-id="9442c-125">Weitere Informationen zu Active Directory-Dienst Schnittstellen und den Technologien, auf denen Sie basieren, finden Sie möglicherweise in den folgenden Quellen.</span><span class="sxs-lookup"><span data-stu-id="9442c-125">For more information about Active Directory Service Interfaces and the technologies on which they are based, you may find the following sources helpful.</span></span>

<span data-ttu-id="9442c-126">Brockschmidt, Kraig.</span><span class="sxs-lookup"><span data-stu-id="9442c-126">Brockschmidt, Kraig.</span></span> <span data-ttu-id="9442c-127">*Innerhalb von OLE*, 2. Edition.</span><span class="sxs-lookup"><span data-stu-id="9442c-127">*Inside OLE*, 2nd edition.</span></span> <span data-ttu-id="9442c-128">Redmond, WA: Microsoft Press, 1995.</span><span class="sxs-lookup"><span data-stu-id="9442c-128">Redmond, WA: Microsoft Press, 1995.</span></span>

<span data-ttu-id="9442c-129">Chappell, David.</span><span class="sxs-lookup"><span data-stu-id="9442c-129">Chappell, David.</span></span> <span data-ttu-id="9442c-130">Grundlegendes *zu ActiveX und OLE*.</span><span class="sxs-lookup"><span data-stu-id="9442c-130">*Understanding ActiveX and OLE*.</span></span> <span data-ttu-id="9442c-131">Redmond, WA: Microsoft Press, 1996.</span><span class="sxs-lookup"><span data-stu-id="9442c-131">Redmond, WA: Microsoft Press, 1996.</span></span>

<span data-ttu-id="9442c-132">Hahn, Steven.</span><span class="sxs-lookup"><span data-stu-id="9442c-132">Hahn, Steven.</span></span> <span data-ttu-id="9442c-133">*ADSI ASP-Programmier Referenz*.</span><span class="sxs-lookup"><span data-stu-id="9442c-133">*ADSI ASP Programmer's Reference*.</span></span> <span data-ttu-id="9442c-134">Wrox Press Ltd., 1998.</span><span class="sxs-lookup"><span data-stu-id="9442c-134">Wrox Press Ltd., 1998.</span></span>

<span data-ttu-id="9442c-135">Harrison, Richard.</span><span class="sxs-lookup"><span data-stu-id="9442c-135">Harrison, Richard.</span></span> <span data-ttu-id="9442c-136">*ASP/MTS/ADSI-Websicherheit*.</span><span class="sxs-lookup"><span data-stu-id="9442c-136">*ASP/MTS/ADSI Web Security*.</span></span> <span data-ttu-id="9442c-137">Prentice Hall, 1999.</span><span class="sxs-lookup"><span data-stu-id="9442c-137">Prentice Hall, 1999.</span></span>

<span data-ttu-id="9442c-138">Die Microsoft-OLE DB Programmierer-Referenz Version 1,0, 1996.</span><span class="sxs-lookup"><span data-stu-id="9442c-138">Microsoft's OLE DB Programmer's Reference Version 1.0, 1996.</span></span>

<span data-ttu-id="9442c-139">*OLE 2-Programmier Referenz, Volume 2*.</span><span class="sxs-lookup"><span data-stu-id="9442c-139">*OLE 2 Programmer's Reference, Volume Two*.</span></span> <span data-ttu-id="9442c-140">Redmond, WA: Microsoft Press, 1994.</span><span class="sxs-lookup"><span data-stu-id="9442c-140">Redmond, WA: Microsoft Press, 1994.</span></span>

<span data-ttu-id="9442c-141">Rogerson, Dale.</span><span class="sxs-lookup"><span data-stu-id="9442c-141">Rogerson, Dale.</span></span> <span data-ttu-id="9442c-142">*Innerhalb von com*.</span><span class="sxs-lookup"><span data-stu-id="9442c-142">*Inside COM*.</span></span> <span data-ttu-id="9442c-143">Redmond, WA: Microsoft Press, 1997.</span><span class="sxs-lookup"><span data-stu-id="9442c-143">Redmond, WA: Microsoft Press, 1997.</span></span>

<span data-ttu-id="9442c-144">*Die Active Directory Service-Entwurfs Spezifikation, Version 2,0*.</span><span class="sxs-lookup"><span data-stu-id="9442c-144">*The Active Directory Service Design Specification Version 2.0*.</span></span>

<span data-ttu-id="9442c-145">*Die Component Object Model Spezifikation*.</span><span class="sxs-lookup"><span data-stu-id="9442c-145">*The Component Object Model Specification*.</span></span>

<span data-ttu-id="9442c-146">(Diese Ressourcen sind in einigen Sprachen und Ländern bzw. Regionen möglicherweise nicht verfügbar.)</span><span class="sxs-lookup"><span data-stu-id="9442c-146">(These resources may not be available in some languages and countries/regions.)</span></span>

 

 





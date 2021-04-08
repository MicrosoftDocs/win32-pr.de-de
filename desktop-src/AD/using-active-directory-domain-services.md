---
title: Verwenden von Active Directory-Domänendiensten
description: Dieser Abschnitt enthält Richtlinien zum Schreiben von Anwendungen, die Daten in einem Active Directory Verzeichnisdienst verwenden oder veröffentlichen.
ms.assetid: 2ae20169-08a5-4e15-8430-ea99a917725f
ms.tgt_platform: multiple
keywords:
- Active Directory Active Directory mit
- Active Directory Domain Services Active Directory mit
- Active Directory Beispiele Active Directory
- Active Directory Domain Services Beispiele Active Directory
- Beispiele Active Directory
- Active Directory Active Directory finden Sie in den Beispielen Active Directory Domain Services Beispiele
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 540b9004311db320decbd15c4f0a29e52ec1302a
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "103734545"
---
# <a name="using-active-directory-domain-services"></a><span data-ttu-id="e60b0-109">Verwenden von Active Directory-Domänendiensten</span><span class="sxs-lookup"><span data-stu-id="e60b0-109">Using Active Directory Domain Services</span></span>

<span data-ttu-id="e60b0-110">Dieser Abschnitt enthält Richtlinien zum Schreiben von Anwendungen, die Daten in einem Active Directory Verzeichnisdienst verwenden oder veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="e60b0-110">This section provides guidelines for writing applications that use or publish data in an Active Directory directory service.</span></span>

> [!Note]  
> <span data-ttu-id="e60b0-111">Die folgende Dokumentation ist für Computerprogrammierer vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="e60b0-111">The following documentation is for computer programmers.</span></span> <span data-ttu-id="e60b0-112">Wenn Sie versuchen, einen Active Directory Druckfehler zu beheben, lesen Sie den [folgenden Vorschlag](https://answers.microsoft.com/windows/forum/all/clicking-find-printer-shows-error-the-active/52bfd961-ff62-4397-b8cf-a0708f0cb3d2) auf den Microsoft Community-Seiten. Wenn dies nicht hilfreich ist, testen Sie diese Empfehlungen von [TechNet](https://social.technet.microsoft.com/Forums/windowsserver/d6212275-24d6-4168-830a-9441f861cb76/error-message-when-attempting-to-print-active-directory-domain-service-is-currently-unavailable?forum=winserverprint).</span><span class="sxs-lookup"><span data-stu-id="e60b0-112">If you are trying to resolve an Active Directory home printing error, see the [following suggestion](https://answers.microsoft.com/windows/forum/all/clicking-find-printer-shows-error-the-active/52bfd961-ff62-4397-b8cf-a0708f0cb3d2) from the Microsoft community pages; if that doesn't help, try these recommendations from [TechNet](https://social.technet.microsoft.com/Forums/windowsserver/d6212275-24d6-4168-830a-9441f861cb76/error-message-when-attempting-to-print-active-directory-domain-service-is-currently-unavailable?forum=winserverprint).</span></span>

 

<span data-ttu-id="e60b0-113">Active Directory Domain Services sind mit dem Lightweight Directory Access Protocol 3,0 kompatibel, das von RFC 2251 und anderen RFCs definiert wird.</span><span class="sxs-lookup"><span data-stu-id="e60b0-113">Active Directory Domain Services are compliant with Lightweight Directory Access Protocol 3.0, which is defined by RFC 2251 and other RFCs.</span></span> <span data-ttu-id="e60b0-114">Alle folgenden API-Sätze können für den Zugriff auf Active Directory Domain Services verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e60b0-114">Any of the following API sets can be used to access Active Directory Domain Services.</span></span> <span data-ttu-id="e60b0-115">Jeder API-Satz hat vor-und Nachteile, die von der Programmiersprache, der Programmierumgebung und der vorgesehenen Ausführungs Methode abhängen.</span><span class="sxs-lookup"><span data-stu-id="e60b0-115">Each API set has advantages and disadvantages that depend on the programming language, programming environment, and intended method of execution.</span></span> <span data-ttu-id="e60b0-116">Die Mehrzahl der Beispiele in dieser Anleitung verwenden ADSI, das von Sprachen wie C und C++ unterstützt wird, sowie von Automatisierungs kompatiblen Sprachen wie Microsoft Visual Basic und Visual Basic Scripting Edition.</span><span class="sxs-lookup"><span data-stu-id="e60b0-116">The majority of the examples in this guide use ADSI, which is supported by languages such as C and C++, as well as automation-compliant languages such as Microsoft Visual Basic and Visual Basic Scripting Edition.</span></span>

<span data-ttu-id="e60b0-117">Weitere Informationen zu bestimmten Active Directory Domain Services Technologien finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="e60b0-117">For more information about specific Active Directory Domain Services technologies, see:</span></span>

-   [<span data-ttu-id="e60b0-118">Lightweight Directory Access Protocol</span><span class="sxs-lookup"><span data-stu-id="e60b0-118">Lightweight Directory Access Protocol</span></span>](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api)
-   [<span data-ttu-id="e60b0-119">Active Directory Service Interfaces</span><span class="sxs-lookup"><span data-stu-id="e60b0-119">Active Directory Service Interfaces</span></span>](../adsi/active-directory-service-interfaces-adsi.md)
-   [<span data-ttu-id="e60b0-120">System.DirectoryServices</span><span class="sxs-lookup"><span data-stu-id="e60b0-120">System.DirectoryServices</span></span>](/dotnet/api/system.directoryservices)

<span data-ttu-id="e60b0-121">In diesem Abschnitt werden die folgenden Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="e60b0-121">This section discusses the following topics:</span></span>

-   [<span data-ttu-id="e60b0-122">Binden an Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="e60b0-122">Binding to Active Directory Domain Services</span></span>](binding-to-active-directory-domain-services.md)
-   [<span data-ttu-id="e60b0-123">Suchen in Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="e60b0-123">Searching in Active Directory Domain Services</span></span>](searching-in-active-directory-domain-services.md)
-   [<span data-ttu-id="e60b0-124">Erstellen und Löschen von Objekten in Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="e60b0-124">Creating and Deleting Objects in Active Directory Domain Services</span></span>](creating-and-deleting-objects-in-active-directory-domain-services.md)
-   [<span data-ttu-id="e60b0-125">Verschieben von Objekten</span><span class="sxs-lookup"><span data-stu-id="e60b0-125">Moving Objects</span></span>](moving-objects.md)
-   [<span data-ttu-id="e60b0-126">Lesen und Schreiben von Attributen von Objekten in Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="e60b0-126">Reading and Writing Attributes of Objects in Active Directory Domain Services</span></span>](reading-and-writing-attributes-of-objects-in-active-directory-domain-services.md)
-   [<span data-ttu-id="e60b0-127">Steuern des Zugriffs auf Objekte in Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="e60b0-127">Controlling Access to Objects in Active Directory Domain Services</span></span>](controlling-access-to-objects-in-active-directory-domain-services.md)
-   [<span data-ttu-id="e60b0-128">Erweitern des Schemas</span><span class="sxs-lookup"><span data-stu-id="e60b0-128">Extending the Schema</span></span>](extending-the-schema.md)
-   [<span data-ttu-id="e60b0-129">Erweitern der Benutzeroberfläche für Verzeichnisobjekte</span><span class="sxs-lookup"><span data-stu-id="e60b0-129">Extending the User Interface for Directory Objects</span></span>](extending-the-user-interface-for-directory-objects.md)
-   [<span data-ttu-id="e60b0-130">Verwalten von Benutzern</span><span class="sxs-lookup"><span data-stu-id="e60b0-130">Managing Users</span></span>](managing-users.md)
-   [<span data-ttu-id="e60b0-131">Verwalten von Gruppen</span><span class="sxs-lookup"><span data-stu-id="e60b0-131">Managing Groups</span></span>](managing-groups.md)
-   [<span data-ttu-id="e60b0-132">Nachverfolgen von Änderungen</span><span class="sxs-lookup"><span data-stu-id="e60b0-132">Tracking Changes</span></span>](tracking-changes.md)
-   [<span data-ttu-id="e60b0-133">Dienstveröffentlichung</span><span class="sxs-lookup"><span data-stu-id="e60b0-133">Service Publication</span></span>](service-publication.md)
-   [<span data-ttu-id="e60b0-134">Dienst Anmeldekonten</span><span class="sxs-lookup"><span data-stu-id="e60b0-134">Service Logon Accounts</span></span>](service-logon-accounts.md)
-   [<span data-ttu-id="e60b0-135">Gegenseitige Authentifizierung mithilfe von Kerberos</span><span class="sxs-lookup"><span data-stu-id="e60b0-135">Mutual Authentication Using Kerberos</span></span>](mutual-authentication-using-kerberos.md)
-   [<span data-ttu-id="e60b0-136">Sichern und Wiederherstellen von Active Directory</span><span class="sxs-lookup"><span data-stu-id="e60b0-136">Backing Up and Restoring Active Directory</span></span>](backing-up-and-restoring-an-active-directory-server.md)
-   [<span data-ttu-id="e60b0-137">Speichern von dynamische Daten</span><span class="sxs-lookup"><span data-stu-id="e60b0-137">Storing Dynamic Data</span></span>](storing-dynamic-data.md)
-   [<span data-ttu-id="e60b0-138">Anwendungsverzeichnis Partitionen</span><span class="sxs-lookup"><span data-stu-id="e60b0-138">Application Directory Partitions</span></span>](application-directory-partitions.md)
-   [<span data-ttu-id="e60b0-139">Erkennen des Betriebsmodus einer Domäne</span><span class="sxs-lookup"><span data-stu-id="e60b0-139">Detecting the Operation Mode of a Domain</span></span>](detecting-the-operation-mode-of-a-domain.md)

 

 
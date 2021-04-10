---
title: Informationen zu Active Directory Domain Services
description: Dieses Handbuch enthält wichtige Informationen zur Integration von Microsoft Active Directory in verteilte Anwendungen, die für Betriebssysteme entwickelt wurden, die Active Directory unterstützen.
ms.assetid: cc6c63dd-ae22-40a7-8312-0a4648bb92bd
ms.tgt_platform: multiple
keywords:
- Active Directory Active Directory, Informationen zu
- Active Directory Domain Services Active Directory, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d8dafb89533d796f0651ad08b913eacda1d0fe9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039034"
---
# <a name="about-active-directory-domain-services"></a><span data-ttu-id="d3701-105">Informationen zu Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="d3701-105">About Active Directory Domain Services</span></span>

## <a name="writing-powerful-applications-that-use-active-directory-domain-services"></a><span data-ttu-id="d3701-106">Schreiben leistungsfähiger Anwendungen, die Active Directory Domain Services verwenden</span><span class="sxs-lookup"><span data-stu-id="d3701-106">Writing Powerful Applications that Use Active Directory Domain Services</span></span>

<span data-ttu-id="d3701-107">Dieses Handbuch enthält wichtige Informationen zur Integration von Active Directory Domain Services in verteilten Anwendungen, die für Betriebssysteme entwickelt wurden, die Active Directory Domain Services unterstützen, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="d3701-107">This guide provides essential information for integrating Active Directory Domain Services in distributed applications designed for operating systems that support Active Directory Domain Services, including:</span></span>

-   <span data-ttu-id="d3701-108">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d3701-108">Windows Server 2008</span></span>
-   <span data-ttu-id="d3701-109">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d3701-109">Windows Server 2008 R2</span></span>
-   <span data-ttu-id="d3701-110">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d3701-110">Windows Server 2012</span></span>
-   <span data-ttu-id="d3701-111">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="d3701-111">Windows Server 2012 R2</span></span>
-   <span data-ttu-id="d3701-112">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="d3701-112">Windows Server 2016</span></span>

> [!Note]  
> <span data-ttu-id="d3701-113">Diese Themen gelten für Softwareentwickler.</span><span class="sxs-lookup"><span data-stu-id="d3701-113">These topics are for software developers.</span></span> <span data-ttu-id="d3701-114">Informationen zu Problemen bei der Unterstützung finden Sie unter [Microsoft-Support](https://windows.microsoft.com/windows/support#1tc).</span><span class="sxs-lookup"><span data-stu-id="d3701-114">For support issues, see [Microsoft Support](https://windows.microsoft.com/windows/support#1tc).</span></span> <span data-ttu-id="d3701-115">Weitere Informationen zum Verwalten von Active Directory finden Sie unter [Active Directory Domain Services](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc770946(v=ws.10)) auf TechNet.</span><span class="sxs-lookup"><span data-stu-id="d3701-115">For information about administering Active Directory, see [Active Directory Domain Services](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc770946(v=ws.10)) at TechNet.</span></span>

 

## <a name="fundamental-directory-features"></a><span data-ttu-id="d3701-116">Grundlegende Verzeichnis Features</span><span class="sxs-lookup"><span data-stu-id="d3701-116">Fundamental Directory Features</span></span>

<span data-ttu-id="d3701-117">Ein Verzeichnisdienst ist ein grundlegender Dienst für verteilte Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="d3701-117">A directory service is a fundamental service for distributed applications.</span></span> <span data-ttu-id="d3701-118">Ein Verzeichnisdienst muss die in der folgenden Tabelle aufgeführten Funktionen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d3701-118">A directory service must provide the features listed in the following table.</span></span>



| <span data-ttu-id="d3701-119">Funktion</span><span class="sxs-lookup"><span data-stu-id="d3701-119">Feature</span></span>               | <span data-ttu-id="d3701-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d3701-120">Description</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3701-121">Standort Transparenz</span><span class="sxs-lookup"><span data-stu-id="d3701-121">Location transparency</span></span> | <span data-ttu-id="d3701-122">Suchen von Benutzern, Gruppen, vernetzten Diensten oder Ressourcen, Daten ohne die Objekt Adresse</span><span class="sxs-lookup"><span data-stu-id="d3701-122">Able to find user, group, networked service, or resource, data without the object address</span></span>           |
| <span data-ttu-id="d3701-123">Objektdaten</span><span class="sxs-lookup"><span data-stu-id="d3701-123">Object data</span></span>           | <span data-ttu-id="d3701-124">Speichern von Benutzer-, Gruppen-, Organisations-und Dienst Daten in einer hierarchischen Struktur</span><span class="sxs-lookup"><span data-stu-id="d3701-124">Able to store user, group, organization, and service data in a hierarchical tree</span></span>                    |
| <span data-ttu-id="d3701-125">Umfassende Abfrage</span><span class="sxs-lookup"><span data-stu-id="d3701-125">Rich query</span></span>            | <span data-ttu-id="d3701-126">Ein Objekt kann durch Abfragen von Objekteigenschaften gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="d3701-126">Able to locate an object by querying for object properties</span></span>                                          |
| <span data-ttu-id="d3701-127">Hochverfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="d3701-127">High availability</span></span>     | <span data-ttu-id="d3701-128">Auffinden eines Replikats des Verzeichnisses an einem Speicherort, der für Lese-/Schreibvorgänge effizient ist</span><span class="sxs-lookup"><span data-stu-id="d3701-128">Able to locate a replica of the directory at a location that is efficient for read/write operations</span></span> |



 

## <a name="advanced-features-of-active-directory-domain-services"></a><span data-ttu-id="d3701-129">Erweiterte Features von Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="d3701-129">Advanced Features of Active Directory Domain Services</span></span>

<span data-ttu-id="d3701-130">Active Directory Domain Services stellt die Funktionen bereit, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="d3701-130">Active Directory Domain Services provides the features listed in the following table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d3701-131">Funktion</span><span class="sxs-lookup"><span data-stu-id="d3701-131">Feature</span></span></th>
<th><span data-ttu-id="d3701-132">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d3701-132">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d3701-133">Unterstützung für Internet Standards</span><span class="sxs-lookup"><span data-stu-id="d3701-133">Support for Internet standards</span></span></td>
<td><span data-ttu-id="d3701-134">Active Directory Domain Services implementiert seine Features gemäß den veröffentlichten Internet Standards wie z. b. LDAP und DNS.</span><span class="sxs-lookup"><span data-stu-id="d3701-134">Active Directory Domain Services implements its features in accordance with published Internet standards such as LDAP and DNS.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3701-135">Eng integrierte und flexible Sicherheit</span><span class="sxs-lookup"><span data-stu-id="d3701-135">Tightly integrated and flexible security</span></span></td>
<td><span data-ttu-id="d3701-136">Einige Vorteile:</span><span class="sxs-lookup"><span data-stu-id="d3701-136">Advantages include:</span></span><br/>
<ul>
<li><span data-ttu-id="d3701-137">Auswahl der Authentifizierungs Pakete.</span><span class="sxs-lookup"><span data-stu-id="d3701-137">Choice of authentication packages.</span></span> <span data-ttu-id="d3701-138">Kerberos, Secure Sockets Layer (SSL) oder eine Kombination richten Sie z. b. einen SSL-Kanal für die Verschlüsselung ein, und verwenden Sie Kerberos für die Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="d3701-138">Kerberos, Secure Sockets Layer (SSL), or a combination; for example, establish an SSL channel for encryption and then use Kerberos for authentication.</span></span></li>
<li><span data-ttu-id="d3701-139">Zentrale Verwaltung des Dienst-und Ressourcen Zugriffs mithilfe der Benutzer und Gruppen in Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="d3701-139">Central management of service and resource access by using the users and groups in Active Directory Domain Services.</span></span></li>
<li><span data-ttu-id="d3701-140">Delegierung der Verwaltung, damit zentrale Administratoren administrative Aufgaben wie das Ändern von Kenn Wörtern oder das Erstellen und Löschen bestimmter Objekte delegieren können.</span><span class="sxs-lookup"><span data-stu-id="d3701-140">Delegation of administration so that central administrators can delegate administrative tasks such as password changing or specific object creation and deletion.</span></span></li>
<li><span data-ttu-id="d3701-141">Der Active Directory Server verwendet die gleichen Zugriffs Steuerungsmechanismen, die für Dateisysteme in den Windows-Betriebssystemen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d3701-141">The Active Directory server uses the same access control mechanisms used on file systems in the Windows operating systems.</span></span> <span data-ttu-id="d3701-142">Folglich funktionieren die gleichen Tools, mit denen die Zugriffs Steuerung in einem Dateisystem verwaltet wird, für Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="d3701-142">Thus, the same tools that manage access control on a file system work for Active Directory Domain Services.</span></span></li>
<li><span data-ttu-id="d3701-143">Umfassende Public Key-Infrastruktur</span><span class="sxs-lookup"><span data-stu-id="d3701-143">Comprehensive Public Key infrastructure.</span></span> <span data-ttu-id="d3701-144">Der Microsoft-Zertifikat Server und die Smartcard-Unterstützung sind in Active Directory Domain Services integriert, um die Smartcard-Anmeldung und Zertifikat Verwaltung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="d3701-144">The Microsoft Certificate Server and Smart Card support are integrated with Active Directory Domain Services to provide Smart Card logon and Certificate management.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d3701-145">Leicht programmierbar</span><span class="sxs-lookup"><span data-stu-id="d3701-145">Easily programmable</span></span></td>
<td><span data-ttu-id="d3701-146">Auf den Active Directory Server kann Programm gesteuert zugegriffen werden, und er kann über die <a href="/windows/desktop/ADSI/active-directory-service-interfaces-adsi">Active Directory Dienst Schnittstellen</a> -API, die <a href="/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api">Lightweight Directory Access Protocol</a> -API oder den <a href="/dotnet/api/system.directoryservices">System. DirectoryServices</a> -Namespace verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="d3701-146">The Active Directory server can be programmatically accessed and administered using the <a href="/windows/desktop/ADSI/active-directory-service-interfaces-adsi">Active Directory Service Interfaces</a> API, <a href="/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api">Lightweight Directory Access Protocol</a> API, or the <a href="/dotnet/api/system.directoryservices">System.DirectoryServices</a> namespace.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3701-147">Verzeichnis aktivierte Systemdienste</span><span class="sxs-lookup"><span data-stu-id="d3701-147">Directory enabled system services</span></span></td>
<td><span data-ttu-id="d3701-148">Die Client Anwendung kann auf einfache Weise auf verteilten Desktops bereitgestellt werden, indem ein Windows Installer Paket erstellt und das in den Windows-Betriebssystemen verfügbare Anwendungs Bereitstellungs Feature verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d3701-148">Your client application can be easily deployed to distributed desktops by creating a Windows Installer package and using the application deployment feature available in the Windows operating systems.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d3701-149">Schlüssel Anwendungsintegration</span><span class="sxs-lookup"><span data-stu-id="d3701-149">Key application integration</span></span></td>
<td><span data-ttu-id="d3701-150">Wichtige verteilte Anwendungen, wie z. b. Exchange, sind in Active Directory Domain Services integriert.</span><span class="sxs-lookup"><span data-stu-id="d3701-150">Key distributed applications, such as Exchange, are integrated with Active Directory Domain Services.</span></span> <span data-ttu-id="d3701-151">Daher können Unternehmen die Anzahl der zu verwaltenden Verzeichnisdienste reduzieren.</span><span class="sxs-lookup"><span data-stu-id="d3701-151">Thus, companies can reduce the number of directory services to be managed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3701-152">Umfassendes und erweiterbares Schema</span><span class="sxs-lookup"><span data-stu-id="d3701-152">Rich and extensible schema</span></span></td>
<td><span data-ttu-id="d3701-153">Das Schema definiert, welche Objekte und Eigenschaften von einem Verzeichnisdienst geschrieben und gelesen werden können.</span><span class="sxs-lookup"><span data-stu-id="d3701-153">The schema defines what objects and properties can be written and read from a directory service.</span></span> <span data-ttu-id="d3701-154">Das Active Directory Schema ist umfangreich.</span><span class="sxs-lookup"><span data-stu-id="d3701-154">The Active Directory Schema is rich.</span></span> <span data-ttu-id="d3701-155">Die meisten Objekte und Eigenschaften, die ein Dienst benötigt, sind verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d3701-155">Most of the objects and properties a service requires are available.</span></span> <span data-ttu-id="d3701-156">Andernfalls kann eine verteilte Anwendung das Schema so erweitern, dass die Anwendungsanforderungen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="d3701-156">If not, a distributed application can extend the schema to support the application requirements.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d3701-157">Weitere Informationen zu Active Directory Domain Services finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="d3701-157">For more information about Active Directory Domain Services, see:</span></span>

-   [<span data-ttu-id="d3701-158">Grundlegende Konzepte von Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="d3701-158">Core Concepts of Active Directory Domain Services</span></span>](core-concepts-of-active-directory-domain-services.md)
-   [<span data-ttu-id="d3701-159">Active Directory-Architektur</span><span class="sxs-lookup"><span data-stu-id="d3701-159">Active Directory Architecture</span></span>](active-directory-domain-services-architecture.md)
-   [<span data-ttu-id="d3701-160">Active Directory-Schema</span><span class="sxs-lookup"><span data-stu-id="d3701-160">Active Directory Schema</span></span>](active-directory-schema.md)


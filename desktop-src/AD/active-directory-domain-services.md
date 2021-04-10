---
title: Active Directory-Domänendienste (AD DS)
description: Microsoft Active Directory Domain Services sind die Grundlage für verteilte Netzwerke, die auf den Betriebssystemen Windows 2000 Server, Windows Server 2003 und Microsoft Windows Server 2008 erstellt werden, die Domänen Controller verwenden.
ms.assetid: 9fc78c72-c59c-4c4d-ace5-00a431645c4b
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services Active Directory
- Active Directory Active Directory, Startseite
- Active Directory Domain Services Active Directory, Startseite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0270f331a68d23ad89a8e5a999f8cabd95487020
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "104039810"
---
# <a name="active-directory-domain-services"></a><span data-ttu-id="11b9d-106">Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="11b9d-106">Active Directory Domain Services</span></span>

## <a name="purpose"></a><span data-ttu-id="11b9d-107">Zweck</span><span class="sxs-lookup"><span data-stu-id="11b9d-107">Purpose</span></span>

<span data-ttu-id="11b9d-108">Microsoft Active Directory Domain Services sind die Grundlage für verteilte Netzwerke, die auf den Betriebssystemen Windows 2000 Server, Windows Server 2003 und Microsoft Windows Server 2008 erstellt werden, die Domänen Controller verwenden.</span><span class="sxs-lookup"><span data-stu-id="11b9d-108">Microsoft Active Directory Domain Services are the foundation for distributed networks built on Windows 2000 Server, Windows Server 2003 and Microsoft Windows Server 2008 operating systems that use domain controllers.</span></span> <span data-ttu-id="11b9d-109">Active Directory Domain Services einen sicheren, strukturierten, hierarchischen Datenspeicher für Objekte in einem Netzwerk wie z. b. Benutzer, Computer, Drucker und Dienste bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="11b9d-109">Active Directory Domain Services provide secure, structured, hierarchical data storage for objects in a network such as users, computers, printers, and services.</span></span> <span data-ttu-id="11b9d-110">Active Directory Domain Services Unterstützung für die Suche nach und die Arbeit mit diesen Objekten bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="11b9d-110">Active Directory Domain Services provide support for locating and working with these objects.</span></span>

<span data-ttu-id="11b9d-111">Dieses Handbuch bietet eine Übersicht über Active Directory Domain Services und Beispielcode für grundlegende Aufgaben, z. b. das Suchen nach Objekten und das Lesen von Eigenschaften, zu erweiterten Aufgaben wie der Dienst Veröffentlichung.</span><span class="sxs-lookup"><span data-stu-id="11b9d-111">This guide provides an overview of Active Directory Domain Services and sample code for basic tasks, such as searching for objects and reading properties, to more advanced tasks such as service publication.</span></span>

<span data-ttu-id="11b9d-112">Windows 2000 Server und spätere Betriebssysteme stellen eine Benutzeroberfläche bereit, mit der Benutzer und Administratoren mit den Objekten und Daten in Active Directory Domain Services arbeiten können.</span><span class="sxs-lookup"><span data-stu-id="11b9d-112">Windows 2000 Server and later operating systems provide a user interface for users and administrators to work with the objects and data in Active Directory Domain Services.</span></span> <span data-ttu-id="11b9d-113">In diesem Leitfaden wird beschrieben, wie Sie diese Benutzeroberfläche erweitern und anpassen.</span><span class="sxs-lookup"><span data-stu-id="11b9d-113">This guide describes how to extend and customize that user interface.</span></span> <span data-ttu-id="11b9d-114">Außerdem wird beschrieben, wie Active Directory Domain Services erweitert wird, indem neue Objektklassen und Attribute definiert werden.</span><span class="sxs-lookup"><span data-stu-id="11b9d-114">It also describes how to extend Active Directory Domain Services by defining new object classes and attributes.</span></span>

> [!Note]  
> <span data-ttu-id="11b9d-115">Die folgende Dokumentation ist für Computerprogrammierer vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="11b9d-115">The following documentation is for computer programmers.</span></span> <span data-ttu-id="11b9d-116">Wenn Sie ein Endbenutzer versuchen, ein Druckfehler oder ein Problem mit dem Heimnetzwerk zu debuggen, finden Sie weitere Informationen in den [Microsoft Community-Foren](https://answers.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="11b9d-116">If you are an end-user trying to debug a printing error or home network issue, see the [Microsoft community forums](https://answers.microsoft.com).</span></span>

 

## <a name="where-applicable"></a><span data-ttu-id="11b9d-117">Anwendungsbereich</span><span class="sxs-lookup"><span data-stu-id="11b9d-117">Where applicable</span></span>

<span data-ttu-id="11b9d-118">Netzwerkadministratoren schreiben Skripts und Anwendungen, die auf Active Directory Domain Services zugreifen, um allgemeine administrative Aufgaben zu automatisieren, z. b. das Hinzufügen von Benutzern und Gruppen, das Verwalten von Druckern und das Festlegen von Berechtigungen für Netzwerk</span><span class="sxs-lookup"><span data-stu-id="11b9d-118">Network administrators write scripts and applications that access Active Directory Domain Services to automate common administrative tasks, such as adding users and groups, managing printers, and setting permissions for network resources.</span></span>

<span data-ttu-id="11b9d-119">Unabhängige Softwarehersteller und Entwickler von Endbenutzern können Active Directory Domain Services programmieren, um Ihre Produkte und Anwendungen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="11b9d-119">Independent software vendors and end-user developers can use Active Directory Domain Services programming to directory-enable their products and applications.</span></span> <span data-ttu-id="11b9d-120">Dienste können sich selbst in Active Directory Domain Services veröffentlichen. Clients können Active Directory Domain Services verwenden, um Dienste zu suchen, und beide können Active Directory Domain Services verwenden, um andere Objekte in einem Netzwerk zu suchen und mit Ihnen zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="11b9d-120">Services can publish themselves in Active Directory Domain Services; clients can use Active Directory Domain Services to find services, and both can use Active Directory Domain Services to locate and work with other objects on a network.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="11b9d-121">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="11b9d-121">Developer audience</span></span>

<span data-ttu-id="11b9d-122">Anwendungen, die auf Daten in Active Directory Domain Services zugreifen, können mit der [Active Directory Dienst Schnittstellen](../adsi/active-directory-service-interfaces-adsi.md) -API, der [Lightweight Directory Access Protocol](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) -API oder dem [System. DirectoryServices](/dotnet/api/system.directoryservices) -Namespace geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="11b9d-122">Applications that access data in Active Directory Domain Services can be written using the [Active Directory Service Interfaces](../adsi/active-directory-service-interfaces-adsi.md) API, [Lightweight Directory Access Protocol](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) API, or the [System.DirectoryServices](/dotnet/api/system.directoryservices) namespace.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="11b9d-123">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="11b9d-123">Run-time requirements</span></span>

<span data-ttu-id="11b9d-124">Active Directory Domain Services auf Domänen Controllern unter Windows 2000 und höher ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="11b9d-124">Active Directory Domain Services run on Windows 2000 and later domain controllers.</span></span> <span data-ttu-id="11b9d-125">Client Anwendungen können jedoch für Windows Vista, Windows Server 2003, Windows XP, Windows 2000, Windows NT 4,0, Windows 98 und Windows 95 geschrieben und ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="11b9d-125">However, client applications can be written for and run on Windows Vista, Windows Server 2003, Windows XP, Windows 2000, Windows NT 4.0, Windows 98, and Windows 95.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="11b9d-126">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="11b9d-126">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="11b9d-127">Informationen zu Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="11b9d-127">About Active Directory Domain Services</span></span>](about-active-directory-domain-services.md)
</dt> <dd>

<span data-ttu-id="11b9d-128">Allgemeine Informationen zu Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="11b9d-128">General information about Active Directory Domain Services.</span></span>

</dd> <dt>

[<span data-ttu-id="11b9d-129">Verwenden von Active Directory-Domänendiensten</span><span class="sxs-lookup"><span data-stu-id="11b9d-129">Using Active Directory Domain Services</span></span>](using-active-directory-domain-services.md)
</dt> <dd>

<span data-ttu-id="11b9d-130">Active Directory Domain Services-Programmier Handbuch.</span><span class="sxs-lookup"><span data-stu-id="11b9d-130">Active Directory Domain Services programming guide.</span></span>

</dd> <dt>

[<span data-ttu-id="11b9d-131">Active Directory Domain Services Referenz</span><span class="sxs-lookup"><span data-stu-id="11b9d-131">Active Directory Domain Services Reference</span></span>](active-directory-domain-services-reference.md)
</dt> <dd>

<span data-ttu-id="11b9d-132">Active Directory Domain Services-Programmier Verweis.</span><span class="sxs-lookup"><span data-stu-id="11b9d-132">Active Directory Domain Services programming reference.</span></span>

</dd> </dl>

 

 
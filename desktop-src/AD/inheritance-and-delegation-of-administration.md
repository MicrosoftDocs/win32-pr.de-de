---
title: Vererbung und Delegierung der Verwaltung
description: Beschreibt AD DS Unterstützung der Vererbung von Berechtigungen in der Objektstruktur und auch der Objekt spezifischen Vererbung.
ms.assetid: db9cf8d9-6831-4456-b2a5-9f5b4f3e9100
ms.tgt_platform: multiple
keywords:
- Verwaltungs Vererbung und Delegierungs Active Directory
- Active Directory Active Directory, Vererbung von Berechtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d76db80497b54e71c806f3ccff9df549f9b2c1a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206262"
---
# <a name="inheritance-and-delegation-of-administration"></a><span data-ttu-id="fb87e-105">Vererbung und Delegierung der Verwaltung</span><span class="sxs-lookup"><span data-stu-id="fb87e-105">Inheritance and Delegation of Administration</span></span>

<span data-ttu-id="fb87e-106">Active Directory Domain Services unterstützt die Vererbung von Berechtigungen in der Objektstruktur, um die Ausführung von Verwaltungsaufgaben auf höheren Ebenen in der Struktur zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="fb87e-106">Active Directory Domain Services supports the inheritance of permissions down the object tree to allow administration tasks to be performed at higher levels in the tree.</span></span> <span data-ttu-id="fb87e-107">Dadurch können Administratoren vererbbare Berechtigungen für Objekte in der Nähe des Stamms einrichten, wie z. b. Domänen-und Organisationseinheiten, und diese Berechtigungen an verschiedene Objekte in der Struktur verteilen.</span><span class="sxs-lookup"><span data-stu-id="fb87e-107">This enables administrators to set up inheritable permissions on objects near the root, such as domain and organizational units, and have those permissions distributed to various objects in the tree.</span></span>

<span data-ttu-id="fb87e-108">Die Vererbung kann pro-ACE-Basis festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="fb87e-108">Inheritance can be set on a per-ACE basis.</span></span> <span data-ttu-id="fb87e-109">In der folgenden Tabelle sind die Flags aufgelistet, die in den **AceFlags** angegeben werden können, um die Vererbung des ACE zu steuern.</span><span class="sxs-lookup"><span data-stu-id="fb87e-109">The following table lists flags that can be specified in the **AceFlags** to control inheritance of the ACE.</span></span>



| <span data-ttu-id="fb87e-110">Flag</span><span class="sxs-lookup"><span data-stu-id="fb87e-110">Flag</span></span>                                                     | <span data-ttu-id="fb87e-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fb87e-111">Description</span></span>                                                                                                                                     |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb87e-112">**ADS- \_ aceflag \_ erben \_**</span><span class="sxs-lookup"><span data-stu-id="fb87e-112">**ADS\_ACEFLAG\_INHERIT\_ACE**</span></span><br/>                | <span data-ttu-id="fb87e-113">Bewirkt, dass der ACE in der Struktur geerbt wird.</span><span class="sxs-lookup"><span data-stu-id="fb87e-113">Causes the ACE to be inherited down in the tree.</span></span><br/>                                                                                     |
| <span data-ttu-id="fb87e-114">**ADS- \_ aceflag \_ No \_ propagieren- \_ \_ ACE**</span><span class="sxs-lookup"><span data-stu-id="fb87e-114">**ADS\_ACEFLAG\_NO\_PROPAGATE\_INHERIT\_ACE**</span></span><br/> | <span data-ttu-id="fb87e-115">Bewirkt, dass der ACE nur eine Ebene in der Struktur geerbt wird.</span><span class="sxs-lookup"><span data-stu-id="fb87e-115">Causes the ACE to be inherited down only one level in the tree.</span></span><br/>                                                                      |
| <span data-ttu-id="fb87e-116">**ADS- \_ aceflag \_ \_ nur von \_ ACE erben**</span><span class="sxs-lookup"><span data-stu-id="fb87e-116">**ADS\_ACEFLAG\_INHERIT\_ONLY\_ACE**</span></span><br/>          | <span data-ttu-id="fb87e-117">Bewirkt, dass der ACE für das Objekt ignoriert wird, für das es angegeben ist, nur geerbt werden und wirksam ist, wo es geerbt wurde.</span><span class="sxs-lookup"><span data-stu-id="fb87e-117">Causes the ACE to be ignored on the object it is specified on, only be inherited down, and be effective where it has been inherited.</span></span><br/> |



 

<span data-ttu-id="fb87e-118">Zusätzlich zum Festlegen der Vererbung unterstützt Active Directory Domain Services objektspezifische Vererbung.</span><span class="sxs-lookup"><span data-stu-id="fb87e-118">In addition to setting inheritance, Active Directory Domain Services supports object-specific inheritance.</span></span> <span data-ttu-id="fb87e-119">Dies ermöglicht es, dass vererbbare ACEs in der Struktur vererbt werden, aber nur für einen bestimmten Objekttyp wirksam werden.</span><span class="sxs-lookup"><span data-stu-id="fb87e-119">This allows the inheritable ACEs to be inherited down the tree, but be effective only on a specific type of object.</span></span> <span data-ttu-id="fb87e-120">Dies ist für die Delegierung der Verwaltung äußerst nützlich.</span><span class="sxs-lookup"><span data-stu-id="fb87e-120">This is extremely useful in delegating administration.</span></span> <span data-ttu-id="fb87e-121">Dies kann z. b. verwendet werden, um einen Objekt spezifischen vererbbaren ACE in einer Organisationseinheit festzulegen, der einer Gruppe die vollständige Kontrolle über alle Benutzer Objekte in der Organisationseinheit, aber nichts anderes ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="fb87e-121">For example, this can be used to set an object-specific inheritable ACE at an organizational unit that enables a group to have full control on all user objects in the organizational unit, but nothing else.</span></span> <span data-ttu-id="fb87e-122">Dadurch wird die Verwaltung der Benutzer in dieser Organisationseinheit an die Benutzer in dieser Gruppe delegiert.</span><span class="sxs-lookup"><span data-stu-id="fb87e-122">Thereby, the management of users in that organizational unit gets delegated to the users in that group.</span></span>

### <a name="delegating-service-administration-with-security-groups"></a><span data-ttu-id="fb87e-123">Delegieren der Dienst Verwaltung mit Sicherheitsgruppen</span><span class="sxs-lookup"><span data-stu-id="fb87e-123">Delegating Service Administration with Security Groups</span></span>

<span data-ttu-id="fb87e-124">Verwenden Sie Sicherheitsgruppen, um die Ihrem Anwendungsserver zugeordneten Administrator Rollen zu definieren und zu delegieren.</span><span class="sxs-lookup"><span data-stu-id="fb87e-124">Use Security groups to define and delegate administrative roles associated with your application server.</span></span> <span data-ttu-id="fb87e-125">Der Dienst kann z. b. einer Gruppe MyService-Administratoren zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="fb87e-125">For example, your service may be associated with a group MyService Administrators.</span></span> <span data-ttu-id="fb87e-126">Benutzer, die als MyService-Administratoren identifiziert werden, werden der Gruppe MyService-Administratoren hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="fb87e-126">Users who are identified as the MyService administrators will be added to MyService Administrators group.</span></span> <span data-ttu-id="fb87e-127">Das Setup Programm für MyService kann Zugriffs Steuerungs Listen für das Verzeichnis festlegen, damit MyService-Administratoren über ausreichende Berechtigungen zum Lesen/Schreiben von MyService-bezogenen Attributen oder zum Erstellen von MyService-spezifischen Objekten verfügen.</span><span class="sxs-lookup"><span data-stu-id="fb87e-127">The setup program for MyService can set ACLs on the directory to enable MyService Administrators sufficient permissions to read/write MyService-related attributes or create MyService-specific objects for example.</span></span>

### <a name="roles-in-security-groups-for-computers-running-your-service"></a><span data-ttu-id="fb87e-128">Rollen in Sicherheitsgruppen für Computer, auf denen der Dienst ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="fb87e-128">Roles in Security Groups for Computers Running Your Service</span></span>

<span data-ttu-id="fb87e-129">Verwenden Sie Sicherheitsgruppen, um die Gruppe von Computern zu definieren, denen der Zugriff auf die Objekte des Diensts im Verzeichnis gewährt wird.</span><span class="sxs-lookup"><span data-stu-id="fb87e-129">Use security groups to define the set of computers that are granted access to your service's objects in the directory.</span></span> <span data-ttu-id="fb87e-130">Der Dienst kann z. b. einer Gruppe MyService-Server zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="fb87e-130">For example, your service may be associated with a group MyService Servers.</span></span> <span data-ttu-id="fb87e-131">Alle Computer, auf denen der MyService-Server ausgeführt wird, werden der Gruppe "MyService Servers" hinzugefügt. dieser Gruppe kann dann Zugriff auf Teile des Verzeichnisses gewährt werden, in denen MyService-Serverdaten lesen/schreiben müssen.</span><span class="sxs-lookup"><span data-stu-id="fb87e-131">All computers running the MyService server are added to MyService Servers group and this group can then be given access to parts of the directory where MyService servers need to read/write data.</span></span> <span data-ttu-id="fb87e-132">Das Setup Programm für MyService kann Zugriffs Steuerungs Listen für das Verzeichnis festlegen, damit MyService-Server über ausreichende Berechtigungen zum Lesen/Schreiben von MyService-bezogenen Attributen oder zum Erstellen von MyService-spezifischen Objekten verfügen.</span><span class="sxs-lookup"><span data-stu-id="fb87e-132">The setup program for MyService can set ACLs on the directory to enable MyService Servers sufficient permissions to read/write MyService-related attributes or create MyService-specific objects for example.</span></span>

 

 






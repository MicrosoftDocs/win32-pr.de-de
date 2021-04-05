---
description: Access Control bezieht sich auf Sicherheitsfunktionen, die Steuern, wer auf Ressourcen im Betriebssystem zugreifen kann. Anwendungen greifen auf Zugriffs Steuerungsfunktionen zu, um festzulegen, wer auf bestimmte Ressourcen zugreifen oder den Zugriff auf von der Anwendung bereitgestellte Ressourcen steuern kann.
ms.assetid: d9ce4ec5-5c09-4b33-93a1-39638a925986
title: Access Control (Autorisierung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31c0198f0ce0de77750e0587d9b54c1e20cee756
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042138"
---
# <a name="access-control-authorization"></a><span data-ttu-id="4bf93-104">Access Control (Autorisierung)</span><span class="sxs-lookup"><span data-stu-id="4bf93-104">Access Control (Authorization)</span></span>

<span data-ttu-id="4bf93-105">Access Control bezieht sich auf Sicherheitsfunktionen, die Steuern, wer auf Ressourcen im Betriebssystem zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="4bf93-105">Access control refers to security features that control who can access resources in the operating system.</span></span> <span data-ttu-id="4bf93-106">Anwendungen greifen auf Zugriffs Steuerungsfunktionen zu, um festzulegen, wer auf bestimmte Ressourcen zugreifen oder den Zugriff auf von der Anwendung bereitgestellte Ressourcen steuern kann.</span><span class="sxs-lookup"><span data-stu-id="4bf93-106">Applications call access control functions to set who can access specific resources or control access to resources provided by the application.</span></span>

<span data-ttu-id="4bf93-107">In dieser Übersicht wird das Sicherheitsmodell zum Steuern des Zugriffs auf Windows-Objekte, z. b. Dateien, und zum Steuern des Zugriffs auf Verwaltungsfunktionen, wie das Festlegen der Systemzeit oder das Überwachen von Benutzeraktionen, beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4bf93-107">This overview describes the security model for controlling access to Windows objects, such as files, and for controlling access to administrative functions, such as setting the system time or auditing user actions.</span></span> <span data-ttu-id="4bf93-108">Das Thema [Access Control Modell](access-control-model.md) enthält eine allgemeine Beschreibung der Teile der Zugriffs Steuerung und deren Interaktion untereinander.</span><span class="sxs-lookup"><span data-stu-id="4bf93-108">The [Access Control Model](access-control-model.md) topic provides a high-level description of the parts of access control and how they interact with each other.</span></span>

<span data-ttu-id="4bf93-109">In den folgenden Themen wird die Zugriffs Steuerung beschrieben:</span><span class="sxs-lookup"><span data-stu-id="4bf93-109">The following topics describe access control:</span></span>

-   [<span data-ttu-id="4bf93-110">Sicherheit auf C2-Ebene</span><span class="sxs-lookup"><span data-stu-id="4bf93-110">C2-level Security</span></span>](c2-level-security.md)
-   [<span data-ttu-id="4bf93-111">Access Control Modell</span><span class="sxs-lookup"><span data-stu-id="4bf93-111">Access Control Model</span></span>](access-control-model.md)
-   [<span data-ttu-id="4bf93-112">Definitions Sprache für Sicherheits Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="4bf93-112">Security Descriptor Definition Language</span></span>](security-descriptor-definition-language.md)
-   [<span data-ttu-id="4bf93-113">Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="4bf93-113">Privileges</span></span>](privileges.md)
-   [<span data-ttu-id="4bf93-114">Generierung von Überwachungsdatensätzen</span><span class="sxs-lookup"><span data-stu-id="4bf93-114">Audit Generation</span></span>](audit-generation.md)
-   [<span data-ttu-id="4bf93-115">Sicherungs fähige Objekte</span><span class="sxs-lookup"><span data-stu-id="4bf93-115">Securable Objects</span></span>](securable-objects.md)
-   [<span data-ttu-id="4bf93-116">Access Control auf niedriger Ebene</span><span class="sxs-lookup"><span data-stu-id="4bf93-116">Low-level Access Control</span></span>](low-level-access-control.md)

<span data-ttu-id="4bf93-117">Im folgenden werden allgemeine Zugriffs Steuerungsaufgaben aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="4bf93-117">The following are common access control tasks:</span></span>

-   [<span data-ttu-id="4bf93-118">Steuern des Zugriffs auf ein Objekt durch DACLs</span><span class="sxs-lookup"><span data-stu-id="4bf93-118">How DACLs Control Access to an Object</span></span>](how-dacls-control-access-to-an-object.md)
-   [<span data-ttu-id="4bf93-119">Steuern der Erstellung von untergeordneten Objekten in C++</span><span class="sxs-lookup"><span data-stu-id="4bf93-119">Controlling Child Object Creation in C++</span></span>](controlling-child-object-creation-in-c--.md)
-   [<span data-ttu-id="4bf93-120">ACEs zum Steuern des Zugriffs auf die Eigenschaften eines Objekts</span><span class="sxs-lookup"><span data-stu-id="4bf93-120">ACEs to Control Access to an Object's Properties</span></span>](aces-to-control-access-to-an-object-s-properties.md)
-   [<span data-ttu-id="4bf93-121">Anfordern von Zugriffsrechten für ein Objekt</span><span class="sxs-lookup"><span data-stu-id="4bf93-121">Requesting Access Rights to an Object</span></span>](requesting-access-rights-to-an-object.md)

<span data-ttu-id="4bf93-122">In den folgenden Themen wird Beispielcode für Zugriffs Steuerungsaufgaben bereitgestellt:</span><span class="sxs-lookup"><span data-stu-id="4bf93-122">The following topics provide example code for access control tasks:</span></span>

-   [<span data-ttu-id="4bf93-123">Ändern der ACLs eines Objekts in C++</span><span class="sxs-lookup"><span data-stu-id="4bf93-123">Modifying the ACLs of an Object in C++</span></span>](modifying-the-acls-of-an-object-in-c--.md)
-   [<span data-ttu-id="4bf93-124">Erstellen einer Sicherheits Beschreibung für ein neues Objekt in C++</span><span class="sxs-lookup"><span data-stu-id="4bf93-124">Creating a Security Descriptor for a New Object in C++</span></span>](creating-a-security-descriptor-for-a-new-object-in-c--.md)
-   [<span data-ttu-id="4bf93-125">Steuern der Erstellung von untergeordneten Objekten in C++</span><span class="sxs-lookup"><span data-stu-id="4bf93-125">Controlling Child Object Creation in C++</span></span>](controlling-child-object-creation-in-c--.md)
-   [<span data-ttu-id="4bf93-126">Aktivieren und Deaktivieren von Berechtigungen in C++</span><span class="sxs-lookup"><span data-stu-id="4bf93-126">Enabling and Disabling Privileges in C++</span></span>](enabling-and-disabling-privileges-in-c--.md)
-   [<span data-ttu-id="4bf93-127">Suchen nach einer SID in einem Zugriffs Token in C++</span><span class="sxs-lookup"><span data-stu-id="4bf93-127">Searching for a SID in an Access Token in C++</span></span>](searching-for-a-sid-in-an-access-token-in-c--.md)
-   [<span data-ttu-id="4bf93-128">Suchen des Besitzers eines File-Objekts in C++</span><span class="sxs-lookup"><span data-stu-id="4bf93-128">Finding the Owner of a File Object in C++</span></span>](finding-the-owner-of-a-file-object-in-c--.md)
-   [<span data-ttu-id="4bf93-129">Übernehmen des Objekt Besitzes in C++</span><span class="sxs-lookup"><span data-stu-id="4bf93-129">Taking Object Ownership in C++</span></span>](taking-object-ownership-in-c--.md)
-   [<span data-ttu-id="4bf93-130">Erstellen einer DACL</span><span class="sxs-lookup"><span data-stu-id="4bf93-130">Creating a DACL</span></span>](/windows/desktop/SecBP/creating-a-dacl)

 

 

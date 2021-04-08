---
title: Steuern des Objekt Zugriffs in Active Directory Domain Services
description: Jedes Active Directory Directory-Dienst Objekt wird durch Windows 2000-Sicherheit geschützt.
ms.assetid: 0821069d-76bd-49cb-a617-8446d26e61d9
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services, Verwendung, Sicherheit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cac744ef63fa95c45d5af535f5155378d479fdb
ms.sourcegitcommit: 460af18ea55f4b12d47d5b8d4b883896e21adf00
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/04/2019
ms.locfileid: "104038408"
---
# <a name="controlling-object-access-in-active-directory-domain-services"></a><span data-ttu-id="cc9bc-104">Steuern des Objekt Zugriffs in Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="cc9bc-104">Controlling object access in Active Directory Domain Services</span></span>

<span data-ttu-id="cc9bc-105">Jedes Active Directory Directory-Dienst Objekt wird durch Windows 2000-Sicherheit geschützt.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-105">Each Active Directory directory service object is protected by Windows 2000 security.</span></span> <span data-ttu-id="cc9bc-106">Dieser Sicherheitsschutz steuert die Vorgänge, die von den einzelnen Sicherheits Prinzipalen im Verzeichnis durchgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-106">This security protection controls the operations that each security principal can perform in the directory.</span></span> <span data-ttu-id="cc9bc-107">In den folgenden Abschnitten wird beschrieben, wie eine Verzeichnis aktivierte Anwendung die Zugriffs Steuerungsfunktionen in Active Directory verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-107">The following sections describe how a directory-enabled application can use the access control features in Active Directory.</span></span>

-   [<span data-ttu-id="cc9bc-108">Funktionsweise von Access Control in Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="cc9bc-108">How Access Control Works in Active Directory Domain Services</span></span>](how-access-control-works-in-active-directory-domain-services.md)
-   [<span data-ttu-id="cc9bc-109">Wie sich die Zugriffs Steuerung auf Lesevorgänge, Schreibvorgänge, Objekt Erstellung und-Löschung auswirkt.</span><span class="sxs-lookup"><span data-stu-id="cc9bc-109">How access control affects read operations, write operation, object creation and deletion.</span></span>](how-security-affects-operations-in-active-directory-domain-services.md)
-   [<span data-ttu-id="cc9bc-110">Verwenden der IADs-und IDirectoryObject-Schnittstellen zum Arbeiten mit der Sicherheits Beschreibung eines Objekts</span><span class="sxs-lookup"><span data-stu-id="cc9bc-110">Using the IADs and IDirectoryObject interfaces to work with an object's security descriptor</span></span>](apis-for-working-with-security-descriptors.md)
-   [<span data-ttu-id="cc9bc-111">Ändern der Zugriffsberechtigungen für ein Objekt</span><span class="sxs-lookup"><span data-stu-id="cc9bc-111">Modifying the access permissions on an object</span></span>](setting-access-rights-on-an-object.md)
-   [<span data-ttu-id="cc9bc-112">Festlegen von Sicherheits Deskriptoren für neue Verzeichnisobjekte</span><span class="sxs-lookup"><span data-stu-id="cc9bc-112">How security descriptors are set on new directory objects</span></span>](how-security-descriptors-are-set-on-new-directory-objects.md)
-   [<span data-ttu-id="cc9bc-113">Erstellen einer Sicherheits Beschreibung für ein neues Verzeichnis Objekt</span><span class="sxs-lookup"><span data-stu-id="cc9bc-113">Creating a Security Descriptor for a New Directory Object</span></span>](creating-a-security-descriptor-for-a-new-directory-object.md)
-   [<span data-ttu-id="cc9bc-114">Verwenden der Vererbung von Zugriffsberechtigungen, um den administrativen Zugriff auf eine gesamte Unterstruktur des Verzeichnisses zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="cc9bc-114">Using inheritance of access permissions to enable administrative access to an entire subtree of the directory</span></span>](inheritance-and-delegation-of-administration.md)
-   [<span data-ttu-id="cc9bc-115">Erstellen, ändern und Lesen der Standard Sicherheits Beschreibung für eine Objektklasse</span><span class="sxs-lookup"><span data-stu-id="cc9bc-115">Creating, modifying, and reading the default security descriptor for an object class</span></span>](default-security-descriptor.md)
-   [<span data-ttu-id="cc9bc-116">Erstellen, festlegen und Überprüfen von Zugriffsrechten für Vorgänge, die über diejenigen hinausgehen, die von den vordefinierten rechten abgedeckt werden</span><span class="sxs-lookup"><span data-stu-id="cc9bc-116">Creating, setting, and checking control access rights for operations that go beyond those covered by the predefined rights</span></span>](control-access-rights.md)
-   [<span data-ttu-id="cc9bc-117">Verwenden von dsaddsidhistory</span><span class="sxs-lookup"><span data-stu-id="cc9bc-117">Using DsAddSidHistory</span></span>](using-dsaddsidhistory.md)
-   [<span data-ttu-id="cc9bc-118">Steuern der Objekt Sichtbarkeit</span><span class="sxs-lookup"><span data-stu-id="cc9bc-118">Controlling Object Visibility</span></span>](controlling-object-visibility.md)
-   [<span data-ttu-id="cc9bc-119">Null-DACLs und leere DACLs</span><span class="sxs-lookup"><span data-stu-id="cc9bc-119">Null DACLs and Empty DACLs</span></span>](null-dacls-and-empty-dacls.md)

 

 





---
description: WMI basiert auf standardmäßigen Windows-Sicherheits Deskriptoren zum Steuern und schützen des Zugriffs auf Sicherungs fähige Objekte wie WMI-Namespaces, Drucker, Dienste und DCOM-Anwendungen.
ms.assetid: 5893457d-3fc2-4d64-a6c2-0f410052ce52
ms.tgt_platform: multiple
title: Zugriff auf Sicherungs fähige WMI-Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad4ea78cd45d57856b0909283e7c2624fb26bd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217972"
---
# <a name="access-to-wmi-securable-objects"></a><span data-ttu-id="6873c-103">Zugriff auf Sicherungs fähige WMI-Objekte</span><span class="sxs-lookup"><span data-stu-id="6873c-103">Access to WMI Securable Objects</span></span>

<span data-ttu-id="6873c-104">WMI basiert auf standardmäßigen Windows- [*Sicherheits Deskriptoren*](/windows/desktop/SecGloss/s-gly) zum Steuern und schützen des Zugriffs auf Sicherungs fähige Objekte wie WMI-Namespaces, Drucker, Dienste und DCOM-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="6873c-104">WMI relies on standard Windows [*security descriptors*](/windows/desktop/SecGloss/s-gly) to control and protect access to securable objects like WMI namespaces, printers, services, and DCOM applications.</span></span> <span data-ttu-id="6873c-105">Weitere Informationen finden Sie unter [zugreifen auf WMI-Namespaces](access-to-wmi-namespaces.md).</span><span class="sxs-lookup"><span data-stu-id="6873c-105">For more information, see [Access to WMI Namespaces](access-to-wmi-namespaces.md).</span></span>

<span data-ttu-id="6873c-106">In diesem Abschnitt werden folgende Themen erörtert:</span><span class="sxs-lookup"><span data-stu-id="6873c-106">The following topics are discussed in this section:</span></span>

-   [<span data-ttu-id="6873c-107">Sicherheits Deskriptoren und SIDs</span><span class="sxs-lookup"><span data-stu-id="6873c-107">Security Descriptors and SIDs</span></span>](#security-descriptors-and-sids)
-   [<span data-ttu-id="6873c-108">Zugriffssteuerung</span><span class="sxs-lookup"><span data-stu-id="6873c-108">Access Control</span></span>](#access-control)
-   [<span data-ttu-id="6873c-109">Ändern der Zugriffssicherheit</span><span class="sxs-lookup"><span data-stu-id="6873c-109">Changing Access Security</span></span>](#changing-access-security)
-   [<span data-ttu-id="6873c-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6873c-110">Related topics</span></span>](#related-topics)

## <a name="security-descriptors-and-sids"></a><span data-ttu-id="6873c-111">Sicherheits Deskriptoren und SIDs</span><span class="sxs-lookup"><span data-stu-id="6873c-111">Security Descriptors and SIDs</span></span>

<span data-ttu-id="6873c-112">WMI behält die Zugriffssicherheit bei, indem das [*Zugriffs Token*](/windows/desktop/SecGloss/a-gly) des Benutzers, der versucht, auf ein Sicherungs fähiges Objekt zuzugreifen, mit der Sicherheits Beschreibung des Objekts verglichen wird.</span><span class="sxs-lookup"><span data-stu-id="6873c-112">WMI maintains access security by comparing the [*access token*](/windows/desktop/SecGloss/a-gly) of the user that attempts to access a securable object with the security descriptor of the object.</span></span>

<span data-ttu-id="6873c-113">Wenn ein Benutzer oder eine Gruppe auf einem System erstellt wird, erhält das Konto eine [*Sicherheits-ID (SID)*](/windows/desktop/SecGloss/s-gly) . die SID stellt sicher, dass ein Konto, das mit dem gleichen Namen wie ein zuvor gelöschtes Konto erstellt wurde, die vorherigen Sicherheitseinstellungen nicht erbt.</span><span class="sxs-lookup"><span data-stu-id="6873c-113">When a user or group is created on a system, the account is given a [*security identifier (SID)*](/windows/desktop/SecGloss/s-gly) The SID ensures that an account created with the same name as a previously deleted account does not inherit the previous security settings.</span></span> <span data-ttu-id="6873c-114">Ein Zugriffs Token wird erstellt, indem die SID, die Liste der Gruppen, denen der Benutzer angehört, und die Liste der aktivierten oder deaktivierten Berechtigungen kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="6873c-114">An access token is created by combining the SID, the list of groups of which the user is a member, and the list of enabled or disabled privileges.</span></span> <span data-ttu-id="6873c-115">Diese Token werden allen Prozessen und Threads zugewiesen, die sich im Besitz des Benutzers befinden.</span><span class="sxs-lookup"><span data-stu-id="6873c-115">These tokens are assigned to all processes and threads owned by the user.</span></span>

## <a name="access-control"></a><span data-ttu-id="6873c-116">Zugriffssteuerung</span><span class="sxs-lookup"><span data-stu-id="6873c-116">Access Control</span></span>

<span data-ttu-id="6873c-117">Wenn der Benutzer ein gesichertes Objekt verwenden möchte, wird das Zugriffs Token in der Sicherheits Beschreibung des-Objekts mit der freigegebenen [*Zugriffs Steuerungs Liste (DACL)*](/windows/desktop/SecGloss/d-gly) verglichen.</span><span class="sxs-lookup"><span data-stu-id="6873c-117">When the user wants to use a secured object, the access token is compared with the [*discretionary access control list (DACL)*](/windows/desktop/SecGloss/d-gly) in the security descriptor on the object.</span></span> <span data-ttu-id="6873c-118">Die DACL enthält Berechtigungen, die als [*Zugriffs Steuerungs Einträge (ACE)*](/windows/desktop/SecGloss/a-gly)bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="6873c-118">The DACL contains permissions called [*access control entries (ACE)*](/windows/desktop/SecGloss/a-gly).</span></span> <span data-ttu-id="6873c-119">[*System-Zugriffs Steuerungs Listen (SACL)*](/windows/desktop/SecGloss/s-gly) tun das gleiche wie DACLs, können jedoch Sicherheits Überwachungs Ereignisse generieren.</span><span class="sxs-lookup"><span data-stu-id="6873c-119">[*System access control lists (SACL)*](/windows/desktop/SecGloss/s-gly) do the same thing as DACLs, but can generate security audit events.</span></span> <span data-ttu-id="6873c-120">Ab Windows Vista kann WMI Überwachungs Einträge im Windows-Sicherheitsprotokoll erstellen.</span><span class="sxs-lookup"><span data-stu-id="6873c-120">Starting with Windows Vista, WMI can make auditing entries in the Windows Security Log.</span></span> <span data-ttu-id="6873c-121">Weitere Informationen zur Überwachung in WMI finden Sie unter [zugreifen auf WMI-Namespaces](access-to-wmi-namespaces.md).</span><span class="sxs-lookup"><span data-stu-id="6873c-121">For more information about auditing in WMI, see [Access to WMI Namespaces](access-to-wmi-namespaces.md).</span></span>

<span data-ttu-id="6873c-122">Die DACL und die SACL bestehen aus einer Liste von ACEs, die beschreiben, welche Benutzer über bestimmte Zugriffsrechte verfügen, einschließlich des Schreibvorgangs in das WMI-Repository, des Remote Zugriffs und der Ausführung sowie der Anmelde Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="6873c-122">Both the DACL and the SACL consist of a list of ACEs that describe which users have specific access rights, including writing to the WMI repository, remote access and execution, and logon permissions.</span></span> <span data-ttu-id="6873c-123">WMI speichert diese ACLs im WMI-Repository.</span><span class="sxs-lookup"><span data-stu-id="6873c-123">WMI stores these ACLs in the WMI repository.</span></span>

<span data-ttu-id="6873c-124">ACEs enthalten drei Typen von Zugriffsebenen oder GRANT/DENY-rechten: allow, Deny für DACL und System Audit (für SACLs).</span><span class="sxs-lookup"><span data-stu-id="6873c-124">ACEs hold three types of access levels or grant/deny rights: allow, deny for DACL, and system audit (for SACLs).</span></span> <span data-ttu-id="6873c-125">Deny ACEs vor zulassen von ACEs in der DACL oder SACL.</span><span class="sxs-lookup"><span data-stu-id="6873c-125">Deny ACEs precede allow ACEs in the DACL or SACL.</span></span> <span data-ttu-id="6873c-126">Wenn Sie die Benutzer Zugriffsrechte überprüfen, wird WMI in der Zugriffs Steuerungs Liste nacheinander ausgeführt, bis ein allow-ACE gefunden wird, der für das anfordernde Zugriffs Token gilt.</span><span class="sxs-lookup"><span data-stu-id="6873c-126">When checking the user access rights, WMI runs consecutively through the access control list until it finds an allow ACE that applies to the requesting access token.</span></span> <span data-ttu-id="6873c-127">Die verbleibenden ACEs werden nach diesem Punkt nicht geprüft.</span><span class="sxs-lookup"><span data-stu-id="6873c-127">The remaining ACEs are not checked after this point.</span></span> <span data-ttu-id="6873c-128">Wenn kein entsprechender Allow ACE gefunden wird, wird der Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="6873c-128">If no appropriate allow ACE is found, then access is denied.</span></span> <span data-ttu-id="6873c-129">Weitere Informationen finden Sie unter [Reihenfolge von ACEs in einer DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl) und [Erstellen einer DACL](/windows/desktop/SecBP/creating-a-dacl).</span><span class="sxs-lookup"><span data-stu-id="6873c-129">For more information, see [Order of ACEs in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl) and [Creating a DACL](/windows/desktop/SecBP/creating-a-dacl).</span></span>

## <a name="changing-access-security"></a><span data-ttu-id="6873c-130">Ändern der Zugriffssicherheit</span><span class="sxs-lookup"><span data-stu-id="6873c-130">Changing Access Security</span></span>

<span data-ttu-id="6873c-131">Mit den entsprechenden Berechtigungen können Sie die Sicherheit für ein Sicherungs fähiges Objekt mit einem Skript oder einer Anwendung ändern.</span><span class="sxs-lookup"><span data-stu-id="6873c-131">With appropriate permissions, you can change the security on a securable object with a script or application.</span></span> <span data-ttu-id="6873c-132">Sie können auch die Sicherheitseinstellungen für WMI-Namespaces mithilfe des [*WMI-Steuer*](gloss-w.md) Elements oder durch Hinzufügen einer SDDL-Zeichenfolge [(Security Descriptor Definition Language)](/windows/desktop/SecAuthZ/security-descriptor-definition-language) in der [*MOF*](gloss-m.md) -Datei (Managed Object Format) ändern, die Klassen für den Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="6873c-132">You can also change the security settings on WMI namespaces using the [*WMI Control*](gloss-w.md) or by adding a [Security Descriptor Definition Language (SDDL)](/windows/desktop/SecAuthZ/security-descriptor-definition-language) string in the [*Managed Object Format (MOF)*](gloss-m.md) file that defines classes for the namespace.</span></span> <span data-ttu-id="6873c-133">Weitere Informationen finden Sie unter [zugreifen auf WMI-Namespaces](access-to-wmi-namespaces.md), [Sichern von WMI-Namespaces](securing-wmi-namespaces.md)und [Ändern der Zugriffssicherheit für Sicherungs fähige Objekte](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="6873c-133">For more information, see [Access to WMI Namespaces](access-to-wmi-namespaces.md), [Securing WMI Namespaces](securing-wmi-namespaces.md), and [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6873c-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6873c-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6873c-135">WMI-sicherheitsdeskriptorobjekte</span><span class="sxs-lookup"><span data-stu-id="6873c-135">WMI Security Descriptor Objects</span></span>](wmi-security-descriptor-objects.md)
</dt> <dt>

[<span data-ttu-id="6873c-136">WMI-Sicherheits Konstanten</span><span class="sxs-lookup"><span data-stu-id="6873c-136">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="6873c-137">Benutzerkontensteuerung und WMI</span><span class="sxs-lookup"><span data-stu-id="6873c-137">User Account Control and WMI</span></span>](user-account-control-and-wmi.md)
</dt> <dt>

[<span data-ttu-id="6873c-138">WMI-sicherheitsdeskriptorobjekte</span><span class="sxs-lookup"><span data-stu-id="6873c-138">WMI Security Descriptor Objects</span></span>](wmi-security-descriptor-objects.md)
</dt> <dt>

[<span data-ttu-id="6873c-139">Zugriff auf WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="6873c-139">Access to WMI Namespaces</span></span>](access-to-wmi-namespaces.md)
</dt> </dl>

 

 

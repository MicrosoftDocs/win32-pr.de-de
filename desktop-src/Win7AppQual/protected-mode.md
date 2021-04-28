---
description: Geschützter Modus
ms.assetid: 88810916-A85E-4EC7-A6AE-1CA2A2205DBC
title: Geschützter Modus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc1b8b1e6931ed83ec59ccfe4c3c63d8e5b5eed
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116448"
---
# <a name="protected-mode"></a><span data-ttu-id="65151-103">Geschützter Modus</span><span class="sxs-lookup"><span data-stu-id="65151-103">Protected Mode</span></span>

<span data-ttu-id="65151-104">Die meisten Windows Internet Explorer 8-Sicherheitsfeatures sind in Internet Explorer 8 für windows XP mit dem Betriebssystem Service Pack 2 (SP2) und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="65151-104">Most Windows Internet Explorer 8 security features are available in Internet Explorer 8 for the Windows XP with Service Pack 2 (SP2) operating system and later versions.</span></span> <span data-ttu-id="65151-105">Der geschützte Modus ist nur für Windows Vista oder höhere Versionen verfügbar, da er auf den folgenden Sicherheitsfeatures basiert, die für Windows Vista neu sind:</span><span class="sxs-lookup"><span data-stu-id="65151-105">Protected Mode is available only for Windows Vista or later versions because it is based on the following security features that are new to Windows Vista:</span></span>

-   <span data-ttu-id="65151-106">[Die Benutzerkontensteuerung (User Account Control, UAC)](https://msdn.microsoft.com/library/aa511445.aspx) erleichtert die Ausführung ohne Administratorrechte.</span><span class="sxs-lookup"><span data-stu-id="65151-106">[User Account Control (UAC)](https://msdn.microsoft.com/library/aa511445.aspx) makes it easy to run without administrator privileges.</span></span> <span data-ttu-id="65151-107">Wenn Benutzer Programme mit eingeschränkten Benutzerberechtigungen ausführen, sind sie sicherer vor Angriffen als bei der Ausführung mit Administratorrechten.</span><span class="sxs-lookup"><span data-stu-id="65151-107">When users run programs with limited user privileges, they are safer from an attack than when they run with administrator privileges.</span></span> <span data-ttu-id="65151-108">Das Windows-Betriebssystem kann verhindern, dass bösartiger Code schädliche Aktionen ausführt.</span><span class="sxs-lookup"><span data-stu-id="65151-108">The Windows operating system can restrict the malicious code from carrying out damaging actions.</span></span>
-   <span data-ttu-id="65151-109">Ein Integritätsmechanismus schränkt den Schreibzugriff auf [sicherungsfähige Objekte](../secauthz/securable-objects.md) durch Prozesse mit niedrigerer Integrität ein, genauso wie die Mitgliedschaft in Benutzerkontengruppen die Rechte von Benutzern auf den Zugriff auf sensible Systemkomponenten einschränkt.</span><span class="sxs-lookup"><span data-stu-id="65151-109">An integrity mechanism restricts write access to [securable objects](../secauthz/securable-objects.md) by lower-integrity processes, in the same way that user account group membership restricts the rights of users to access sensitive system components.</span></span>
-   <span data-ttu-id="65151-110">[Benutzeroberfläche Privilege Isolation (UIPI)](/previous-versions/dotnet/articles/bb625963(v=msdn.10)) verhindert, dass Prozesse ausgewählte Fenstermeldungen und andere USER-APIs an Prozesse senden, die mit höherer Integrität ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="65151-110">[User Interface Privilege Isolation (UIPI)](/previous-versions/dotnet/articles/bb625963(v=msdn.10)) prevents processes from sending selected window messages and other USER APIs to processes that are running with higher integrity.</span></span>

<span data-ttu-id="65151-111">Die Sicherheitsinfrastruktur des Windows-Integritätsmechanismus ermöglicht es dem geschützten Modus, Windows Internet Explorer die Berechtigungen zur Verfügung zu stellen, die Benutzer zum Durchsuchen des Webs benötigen, während Benutzer Berechtigungen einbehalten, die Benutzer benötigen, um Programme unbeaufsichtigt zu installieren oder sensible Systemdaten zu ändern.</span><span class="sxs-lookup"><span data-stu-id="65151-111">The Windows Integrity Mechanism security infrastructure allows Protected Mode to provide Windows Internet Explorer with the privileges that users need to browse the web, while withholding privileges that users need to install programs silently or modify sensitive system data.</span></span>

<span data-ttu-id="65151-112">Benutzer können dieses Feature über ein Kontrollkästchen deaktivieren, und Administratoren können es mithilfe von Gruppenrichtlinie deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="65151-112">Users can disable this feature through a check box, and administrators can disable it by using Group Policy.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="65151-113">Sie sollten das Feature während der Problembehandlung nur als temporäres Measure deaktivieren, um das Verhalten der Anwendung zu vergleichen, wenn das Feature aktiviert ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="65151-113">You should disable the feature only as a temporary measure during troubleshooting to compare behavior of the application when the feature is enabled or not.</span></span> <span data-ttu-id="65151-114">Es wird empfohlen, dieses Feature dauerhaft zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="65151-114">We recommended that you keep this feature permanently enabled.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="65151-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="65151-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65151-116">Beheben von Kompatibilitätsproblemen in Webanwendungen mithilfe von Kompatibilitätsansicht</span><span class="sxs-lookup"><span data-stu-id="65151-116">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 

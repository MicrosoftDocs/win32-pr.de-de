---
description: .
ms.assetid: 88810916-A85E-4EC7-A6AE-1CA2A2205DBC
title: Geschützter Modus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ace82e27bbec3bb97a9ffbd3b64c9c6cee9e11e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865967"
---
# <a name="protected-mode"></a><span data-ttu-id="95238-103">Geschützter Modus</span><span class="sxs-lookup"><span data-stu-id="95238-103">Protected Mode</span></span>

<span data-ttu-id="95238-104">Die meisten Windows Internet Explorer 8-Sicherheitsfeatures sind in Internet Explorer 8 für das Betriebssystem Windows XP mit Service Pack 2 (SP2) und spätere Versionen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="95238-104">Most Windows Internet Explorer 8 security features are available in Internet Explorer 8 for the Windows XP with Service Pack 2 (SP2) operating system and later versions.</span></span> <span data-ttu-id="95238-105">Der geschützte Modus ist nur für Windows Vista oder spätere Versionen verfügbar, da er auf den folgenden Sicherheitsfeatures basiert, die für Windows Vista neu sind:</span><span class="sxs-lookup"><span data-stu-id="95238-105">Protected Mode is available only for Windows Vista or later versions because it is based on the following security features that are new to Windows Vista:</span></span>

-   <span data-ttu-id="95238-106">Die [Benutzerkontensteuerung (User Account Control, UAC)](https://msdn.microsoft.com/library/aa511445.aspx) erleichtert die Ausführung ohne Administratorrechte.</span><span class="sxs-lookup"><span data-stu-id="95238-106">[User Account Control (UAC)](https://msdn.microsoft.com/library/aa511445.aspx) makes it easy to run without administrator privileges.</span></span> <span data-ttu-id="95238-107">Wenn Benutzer Programme mit eingeschränkten Benutzerberechtigungen ausführen, sind Sie vor Angriffen sicherer, als wenn Sie mit Administratorrechten ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="95238-107">When users run programs with limited user privileges, they are safer from an attack than when they run with administrator privileges.</span></span> <span data-ttu-id="95238-108">Das Windows-Betriebssystem kann verhindern, dass böswillige Code schädliche Aktionen ausführt.</span><span class="sxs-lookup"><span data-stu-id="95238-108">The Windows operating system can restrict the malicious code from carrying out damaging actions.</span></span>
-   <span data-ttu-id="95238-109">Ein Integritäts Mechanismus schränkt den Schreibzugriff auf Sicherungs [fähige Objekte](../secauthz/securable-objects.md) durch Prozesse mit niedrigerer Integrität auf die gleiche Weise ein, wie die Benutzerkonten Gruppen-Mitgliedschaft die Rechte von Benutzern für den Zugriff auf sensible Systemkomponenten einschränkt.</span><span class="sxs-lookup"><span data-stu-id="95238-109">An integrity mechanism restricts write access to [securable objects](../secauthz/securable-objects.md) by lower-integrity processes, in the same way that user account group membership restricts the rights of users to access sensitive system components.</span></span>
-   <span data-ttu-id="95238-110">Die [Benutzeroberflächen-Berechtigungs Isolation (UIPI)](/previous-versions/dotnet/articles/bb625963(v=msdn.10)) verhindert, dass Prozesse ausgewählte Fenster Nachrichten und andere Benutzer-APIs an Prozesse senden, die mit höherer Integrität ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="95238-110">[User Interface Privilege Isolation (UIPI)](/previous-versions/dotnet/articles/bb625963(v=msdn.10)) prevents processes from sending selected window messages and other USER APIs to processes that are running with higher integrity.</span></span>

<span data-ttu-id="95238-111">Mit der Sicherheitsinfrastruktur des Windows-Integritäts Mechanismus kann der geschützte Modus Windows Internet Explorer die Berechtigungen bereitstellen, die Benutzer zum Durchsuchen des Internets benötigen, während gleichzeitig die Berechtigungen, die Benutzer zum unbeaufsichtigten Installieren von Programmen oder zum Ändern sensibler Systemdaten benötigen</span><span class="sxs-lookup"><span data-stu-id="95238-111">The Windows Integrity Mechanism security infrastructure allows Protected Mode to provide Windows Internet Explorer with the privileges that users need to browse the web, while withholding privileges that users need to install programs silently or modify sensitive system data.</span></span>

<span data-ttu-id="95238-112">Benutzer können diese Funktion mithilfe eines Kontrollkästchens deaktivieren, und Administratoren können Sie mithilfe von Gruppenrichtlinie deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="95238-112">Users can disable this feature through a check box, and administrators can disable it by using Group Policy.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="95238-113">Sie sollten die Funktion nur als temporäre Maßnahme bei der Problembehandlung deaktivieren, um das Verhalten der Anwendung zu vergleichen, wenn die Funktion aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="95238-113">You should disable the feature only as a temporary measure during troubleshooting to compare behavior of the application when the feature is enabled or not.</span></span> <span data-ttu-id="95238-114">Es wird empfohlen, diese Funktion dauerhaft zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="95238-114">We recommended that you keep this feature permanently enabled.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="95238-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="95238-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95238-116">Beheben von Kompatibilitätsproblemen in Webanwendungen mithilfe der Kompatibilitäts Ansicht</span><span class="sxs-lookup"><span data-stu-id="95238-116">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 

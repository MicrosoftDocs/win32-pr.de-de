---
description: Windows-Ressourcenschutz (WRP) verhindert, dass wichtige Systemdateien, Ordner und Registrierungsschlüssel ersetzt werden, die als Teil des Betriebssystems installiert werden.
ms.assetid: 39069f57-d9f6-4890-ba87-37175184d7a2
title: Informationen zu Windows-Ressourcenschutz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c102225a547c4e454c3fb67ac94f715cd3adf8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366131"
---
# <a name="about-windows-resource-protection"></a><span data-ttu-id="3b123-103">Informationen zu Windows-Ressourcenschutz</span><span class="sxs-lookup"><span data-stu-id="3b123-103">About Windows Resource Protection</span></span>

<span data-ttu-id="3b123-104">Windows-Ressourcenschutz (WRP) verhindert, dass wichtige Systemdateien, Ordner und Registrierungsschlüssel ersetzt werden, die als Teil des Betriebssystems installiert werden.</span><span class="sxs-lookup"><span data-stu-id="3b123-104">Windows Resource Protection (WRP) prevents the replacement of essential system files, folders, and registry keys that are installed as part of the operating system.</span></span> <span data-ttu-id="3b123-105">Es wurde ab Windows Server 2008 und Windows Vista verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3b123-105">It became available starting with Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="3b123-106">Die Berechtigung für den Vollzugriff zum Ändern von durch WRP geschützten Ressourcen ist auf Treuhänder beschränkt.</span><span class="sxs-lookup"><span data-stu-id="3b123-106">Permission for full access to modify WRP-protected resources is restricted to TrustedInstaller.</span></span> <span data-ttu-id="3b123-107">Durch WRP geschützte Ressourcen können nur mithilfe der [unterstützten Ressourcenaustausch Mechanismen](supported-file-replacement-mechanisms.md) mit dem Windows-Modul Installations Dienst geändert werden.</span><span class="sxs-lookup"><span data-stu-id="3b123-107">WRP-protected resources can only be changed using the [Supported Resource Replacement Mechanisms](supported-file-replacement-mechanisms.md) with the Windows Modules Installer service.</span></span> <span data-ttu-id="3b123-108">Der Schutz dieser Ressourcen verhindert Anwendungs-und Betriebssystem Fehler.</span><span class="sxs-lookup"><span data-stu-id="3b123-108">Protecting these resources prevents application and operating system failures.</span></span>

<span data-ttu-id="3b123-109">Anwendungen sollten nicht versuchen, durch WRP geschützte Ressourcen zu ändern, da diese von Windows und anderen Anwendungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3b123-109">Applications should not attempt to modify WRP-protected resources because these are used by Windows and other applications.</span></span> <span data-ttu-id="3b123-110">Wenn eine Anwendung versucht, eine durch WRP geschützte Ressource zu ändern, kann dies folgende Ergebnisse haben:</span><span class="sxs-lookup"><span data-stu-id="3b123-110">If an application attempts to modify a WRP-protected resource, it can have the following results.</span></span>

-   <span data-ttu-id="3b123-111">Anwendungsinstallations Programme, die versuchen, wichtige Windows-Dateien oder Registrierungsschlüssel zu ersetzen, zu ändern oder zu löschen, können die Anwendung möglicherweise nicht installieren und erhalten eine Fehlermeldung, dass der Zugriff auf die Ressource verweigert wurde.</span><span class="sxs-lookup"><span data-stu-id="3b123-111">Application installers that attempt to replace, modify, or delete critical Windows files or registry keys may fail to install the application and will receive an error message stating that access to the resource was denied.</span></span>
-   <span data-ttu-id="3b123-112">Anwendungen, die versuchen, Unterschlüssel hinzuzufügen oder zu entfernen oder die Werte geschützter Registrierungsschlüssel zu ändern, schlagen möglicherweise fehl, und es wird eine Fehlermeldung angezeigt, die besagt, dass der Zugriff auf die Ressource verweigert wurde.</span><span class="sxs-lookup"><span data-stu-id="3b123-112">Applications that attempt to add or remove sub-keys or change the values of protected registry keys may fail and will receive an error message stating that access to the resource was denied.</span></span>
-   <span data-ttu-id="3b123-113">Anwendungen, die auf das Schreiben von Informationen in geschützte Registrierungsschlüssel, Ordner oder Dateien angewiesen sind, können fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="3b123-113">Applications that rely on writing any information into protected registry keys, folders, or files may fail.</span></span>

<span data-ttu-id="3b123-114">WRP ist der neue Name für den Windows-Datei Schutz (WFP).</span><span class="sxs-lookup"><span data-stu-id="3b123-114">WRP is the new name for Windows File Protection (WFP).</span></span> <span data-ttu-id="3b123-115">WRP schützt Registrierungsschlüssel und Ordner sowie wichtige Systemdateien.</span><span class="sxs-lookup"><span data-stu-id="3b123-115">WRP protects registry keys and folders as well as essential system files.</span></span> <span data-ttu-id="3b123-116">WFP war in Microsoft Windows Server 2003 und Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3b123-116">WFP was available in Microsoft Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="3b123-117">WRP ersetzt WFP in Windows Server 2008 und Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3b123-117">WRP replaces WFP in Windows Server 2008 and Windows Vista.</span></span>

<span data-ttu-id="3b123-118">In den folgenden Themen wird WRP beschrieben:</span><span class="sxs-lookup"><span data-stu-id="3b123-118">The following topics describe WRP:</span></span>

-   [<span data-ttu-id="3b123-119">Liste geschützter Ressourcen</span><span class="sxs-lookup"><span data-stu-id="3b123-119">Protected Resource List</span></span>](protected-file-list.md)
-   [<span data-ttu-id="3b123-120">Erkennen von Ressourcenaustausch</span><span class="sxs-lookup"><span data-stu-id="3b123-120">Detecting Resource Replacement</span></span>](detecting-file-replacement.md)
-   [<span data-ttu-id="3b123-121">Unterstützte Mechanismen für die Ressourcen Ersetzung</span><span class="sxs-lookup"><span data-stu-id="3b123-121">Supported Resource Replacement Mechanisms</span></span>](supported-file-replacement-mechanisms.md)
-   [<span data-ttu-id="3b123-122">System File Checker</span><span class="sxs-lookup"><span data-stu-id="3b123-122">System File Checker</span></span>](system-file-checker.md)
-   [<span data-ttu-id="3b123-123">Überlegungen zur Remote Verwaltung</span><span class="sxs-lookup"><span data-stu-id="3b123-123">Remote Administration Considerations</span></span>](remote-administration-considerations.md)

 

 




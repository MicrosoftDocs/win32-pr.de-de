---
description: Die Ersetzung geschützter Ressourcen wird durch die folgenden Mechanismen unterstützt.
ms.assetid: a757e6cf-59df-4894-a0dc-40174b0aa147
title: Unterstützte Mechanismen für die Ressourcen Ersetzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2aaaa1d9cc8d24d8cd172be71ee40790bf8161a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368992"
---
# <a name="supported-resource-replacement-mechanisms"></a><span data-ttu-id="1e31c-103">Unterstützte Mechanismen für die Ressourcen Ersetzung</span><span class="sxs-lookup"><span data-stu-id="1e31c-103">Supported Resource Replacement Mechanisms</span></span>

<span data-ttu-id="1e31c-104">Die Ersetzung geschützter Ressourcen wird durch die folgenden Mechanismen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1e31c-104">Replacement of protected resources is supported through the following mechanisms.</span></span>

<span data-ttu-id="1e31c-105">Die Berechtigung für den vollständigen Zugriff zum Ändern von durch WRP geschützten Ressourcen unter Windows Vista und Windows Server 2008 ist auf die Treuhänder mit dem Windows modules Installer-Dienst beschränkt, indem die folgenden Mechanismen verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="1e31c-105">Permission for full access to modify WRP-protected resources on Windows Vista and Windows Server 2008 is restricted to TrustedInstaller with the Windows Modules Installer service using the following mechanisms:</span></span>

-   <span data-ttu-id="1e31c-106">Windows Service Packs, die von Treuhänder installiert werden.</span><span class="sxs-lookup"><span data-stu-id="1e31c-106">Windows Service Packs installed by TrustedInstaller.</span></span>
-   <span data-ttu-id="1e31c-107">Von Treuhänder installierte Hotfixes.</span><span class="sxs-lookup"><span data-stu-id="1e31c-107">Hotfixes installed by TrustedInstaller.</span></span>
-   <span data-ttu-id="1e31c-108">Betriebssystem Upgrades, die von Treuhänder installiert werden.</span><span class="sxs-lookup"><span data-stu-id="1e31c-108">Operating system upgrades installed by TrustedInstaller.</span></span>
-   <span data-ttu-id="1e31c-109">Windows Update von Treuhänder installiert.</span><span class="sxs-lookup"><span data-stu-id="1e31c-109">Windows Update installed by TrustedInstaller.</span></span>

<span data-ttu-id="1e31c-110">Anwendungen und Installationsprogramme, die versuchen, eine durch WRP geschützte Ressource durch andere Methoden als die angegebenen Methoden zu ersetzen, wird der Zugriff zum Ändern der Ressource und Generieren einer Fehlermeldung "Zugriff verweigert" verweigert.</span><span class="sxs-lookup"><span data-stu-id="1e31c-110">Applications and installers attempting to replace a WRP-protected resource by means other than these specified methods are denied access to change the resource and generate an access denied error message.</span></span>

<span data-ttu-id="1e31c-111">Für bekannte Installationsprogramme, die versuchen, durch WRP geschützte Ressourcen zu ersetzen, wird möglicherweise der Fehler "Zugriff verweigert" und die Fehlermeldung unterdrückt.</span><span class="sxs-lookup"><span data-stu-id="1e31c-111">For well-known installers attempting to replace WRP-protected resources, the access denied error and error message may be suppressed.</span></span> <span data-ttu-id="1e31c-112">In diesem Fall wird der Vorgang erfolgreich zurückgegeben, und die Fehlermeldung und die Fehlermeldung werden unterdrückt, aber auf die durch WRP geschützte Ressource werden keine Änderungen angewendet.</span><span class="sxs-lookup"><span data-stu-id="1e31c-112">In this case, the operation returns successfully, the error and error message are suppressed, but no changes are applied to the WRP-protected resource.</span></span> <span data-ttu-id="1e31c-113">Der Fehler wird möglicherweise nur für einen bekannten Installer unterdrückt, wenn alle der folgenden Kriterien erfüllt sind:</span><span class="sxs-lookup"><span data-stu-id="1e31c-113">The error may be suppressed for a well-known installer only when all of the following criteria are satisfied:</span></span>

-   <span data-ttu-id="1e31c-114">Dies ist eine Legacy Anwendung.</span><span class="sxs-lookup"><span data-stu-id="1e31c-114">This is a legacy application.</span></span> <span data-ttu-id="1e31c-115">Die Anwendung enthält kein Manifest mit einem requestedExecutionLevel, das die Anwendung identifiziert, die für Windows Vista oder Windows Server 2008 entworfen wurde.</span><span class="sxs-lookup"><span data-stu-id="1e31c-115">The application does not include a manifest with a requestedExecutionlevel that identifies the application as designed for Windows Vista or Windows Server 2008.</span></span>
-   <span data-ttu-id="1e31c-116">Der Fehler "Zugriff verweigert" wird nur durch den Versuch verursacht, eine durch WRP geschützte Ressource zu ändern.</span><span class="sxs-lookup"><span data-stu-id="1e31c-116">The access denied error is caused only by the attempt to modify a WRP-protected resource.</span></span>
-   <span data-ttu-id="1e31c-117">Ein Administrator installiert die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="1e31c-117">An Administrator is installing the application.</span></span>

<span data-ttu-id="1e31c-118">Weitere Informationen zum Verwenden der Windows Installer mit WRP finden Sie unter [Verwenden von Windows Installer und Windows-Ressourcenschutz](/windows/desktop/Msi/windows-resource-protection-on-windows-vista) im [Windows Installer](/windows/desktop/Msi/windows-installer-portal) SDK.</span><span class="sxs-lookup"><span data-stu-id="1e31c-118">For information about using the Windows Installer with WRP, see [Using Windows Installer and Windows Resource Protection](/windows/desktop/Msi/windows-resource-protection-on-windows-vista) in the [Windows Installer](/windows/desktop/Msi/windows-installer-portal) SDK.</span></span>

<span data-ttu-id="1e31c-119">**Windows Server 2003 und Windows XP:** Die Ersetzung von WFP-geschützten Systemdateien wird nur durch die folgenden Mechanismen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="1e31c-119">**Windows Server 2003 and Windows XP:** Replacement of WFP-protected system files is supported only through the following mechanisms:</span></span>

-   <span data-ttu-id="1e31c-120">Windows Service Pack-Installation mit Update.exe</span><span class="sxs-lookup"><span data-stu-id="1e31c-120">Windows Service Pack installation using Update.exe</span></span>
-   <span data-ttu-id="1e31c-121">Mit Hotfix.exe installierte Hotfixes</span><span class="sxs-lookup"><span data-stu-id="1e31c-121">Hotfixes installed using Hotfix.exe</span></span>
-   <span data-ttu-id="1e31c-122">Betriebssystem Upgrades mithilfe von Winnt32.exe</span><span class="sxs-lookup"><span data-stu-id="1e31c-122">Operating system upgrades using Winnt32.exe</span></span>
-   <span data-ttu-id="1e31c-123">Windows-Update</span><span class="sxs-lookup"><span data-stu-id="1e31c-123">Windows Update</span></span>

<span data-ttu-id="1e31c-124">Das Ersetzen geschützter Dateien durch andere Methoden als die angegebenen Methoden führt dazu, dass die ursprünglichen Dateien von WFP wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="1e31c-124">Replacing protected files by means other than these specified methods results in the original files being restored by WFP.</span></span>

 

 

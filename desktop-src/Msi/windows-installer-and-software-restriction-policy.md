---
description: Windows Installer ist in die Software Einschränkungs Richtlinie in Microsoft Windows XP integriert.
ms.assetid: b1e58336-8908-45ee-86f0-81b2314fa77a
title: Windows Installer-und Software Einschränkungs Richtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b080a1ed9a1396f4ac212e73d1fda6e2719bf40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363560"
---
# <a name="windows-installer-and-software-restriction-policy"></a><span data-ttu-id="c0a79-103">Windows Installer-und Software Einschränkungs Richtlinie</span><span class="sxs-lookup"><span data-stu-id="c0a79-103">Windows Installer and Software Restriction Policy</span></span>

<span data-ttu-id="c0a79-104">Windows Installer ist in die Software Einschränkungs Richtlinie in Microsoft Windows XP integriert.</span><span class="sxs-lookup"><span data-stu-id="c0a79-104">Windows Installer is integrated with Software Restriction Policy in Microsoft Windows XP.</span></span> <span data-ttu-id="c0a79-105">Die Software Einschränkungs Richtlinie kann über Gruppenrichtlinien konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="c0a79-105">Software Restriction Policy is configurable through group policy.</span></span> <span data-ttu-id="c0a79-106">Die Software Einschränkungs Richtlinie ermöglicht es Administratoren, Administratoren und nicht Administratoren das Ausführen von Dateien auf der Grundlage der Pfad-, URL-Zonen-, Hash-oder Herausgeber Kriterien einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="c0a79-106">Software Restriction Policy allows an administrator to restrict both administrators and nonadministrators from running files based upon the path, URL zone, hash, or publisher criteria.</span></span> <span data-ttu-id="c0a79-107">Die Richtlinie für Software Einschränkung hat zwei Ebenen: uneingeschränkt und unzulässig.</span><span class="sxs-lookup"><span data-stu-id="c0a79-107">Software Restriction Policy has two levels: unrestricted and disallowed.</span></span> <span data-ttu-id="c0a79-108">Mit der Windows Installer werden nur Pakete installiert, die auf uneingeschränkter Ebene ausgeführt werden dürfen.</span><span class="sxs-lookup"><span data-stu-id="c0a79-108">The Windows Installer only installs packages allowed to run at the unrestricted level.</span></span>

<span data-ttu-id="c0a79-109">Patches oder Transformationen müssen auch auf uneingeschränkter Ebene ausgeführt werden dürfen.</span><span class="sxs-lookup"><span data-stu-id="c0a79-109">Patches or transforms must also be allowed to run at the unrestricted level.</span></span> <span data-ttu-id="c0a79-110">Wenn ein Paket, ein Patch oder eine Transformation so konfiguriert ist, dass es auf einer anderen Ebene als uneingeschränkt ausgeführt wird, zeigt der Windows Installer eine Fehlermeldung an und protokolliert einen Eintrag im Anwendungs Ereignisprotokoll.</span><span class="sxs-lookup"><span data-stu-id="c0a79-110">If a package, patch, or transform is configured to run at a level different from unrestricted, the Windows Installer displays an error message and logs an entry in the application event log.</span></span> <span data-ttu-id="c0a79-111">Die Software Einschränkungs Richtlinie wird ausgewertet, wenn eine Anwendung zum ersten Mal installiert wird, wenn ein neuer Patch angewendet wird und wenn das Installationspaket erneut zwischengespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="c0a79-111">Software restriction policy is evaluated the first time an application is installed, when a new patch is applied, and when the installation package is re-cached.</span></span>

<span data-ttu-id="c0a79-112">Wenn ein Paket, ein Patch oder eine Transformation eingeschränkt ist, zeigt der Windows Installer eine Fehlermeldung an und schreibt einen Eintrag für die [Ereignisprotokollierung](event-logging.md) in das Anwendungs Ereignisprotokoll.</span><span class="sxs-lookup"><span data-stu-id="c0a79-112">If a package, patch, or transform is restricted, the Windows Installer displays an error message and writes an [Event Logging](event-logging.md) entry in the application event log.</span></span> <span data-ttu-id="c0a79-113">Die Software Einschränkungs Richtlinie wird ausgewertet, wenn eine Anwendung zum ersten Mal installiert wird, wenn ein neuer Patch angewendet wird und wenn das Installationspaket erneut zwischengespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="c0a79-113">Software restriction policy is evaluated the first time an application is installed, when a new patch is applied, and when the installation package is re-cached.</span></span>

<span data-ttu-id="c0a79-114">Weitere Informationen zu Software Einschränkungs Richtlinien finden Sie in der Produktdokumentation und [Durchsuchen der TechNet-Website](https://www.microsoft.com/technet/sitemap.mspx).</span><span class="sxs-lookup"><span data-stu-id="c0a79-114">For more information on software restriction policy, consult the product documentation and [search the TechNet Site](https://www.microsoft.com/technet/sitemap.mspx).</span></span>

 

 




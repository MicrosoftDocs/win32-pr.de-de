---
description: Parallele Assemblys werden mit den folgenden Typen von Manifest-und Konfigurationsdateien verwendet. Manifeste und Konfigurationen sind XML-Dateien.
ms.assetid: 8b969a8f-586c-4556-87be-92db6c61e8ce
title: Manifest-Dateireferenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ea9915ba8e5e0c43b7e9c96e62ea46c3f0061b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128820"
---
# <a name="manifest-files-reference"></a><span data-ttu-id="3614d-104">Manifest-Dateireferenz</span><span class="sxs-lookup"><span data-stu-id="3614d-104">Manifest Files Reference</span></span>

<span data-ttu-id="3614d-105">Parallele Assemblys werden mit den folgenden Typen von Manifest-und Konfigurationsdateien verwendet.</span><span class="sxs-lookup"><span data-stu-id="3614d-105">Side-by-side assemblies are used with the following types of manifest and configuration files.</span></span> <span data-ttu-id="3614d-106">Manifeste und Konfigurationen sind XML-Dateien.</span><span class="sxs-lookup"><span data-stu-id="3614d-106">Manifests and configurations are XML files.</span></span>



| <span data-ttu-id="3614d-107">Manifest</span><span class="sxs-lookup"><span data-stu-id="3614d-107">Manifest</span></span>                                                               | <span data-ttu-id="3614d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3614d-108">Description</span></span>                                                                                                                                                                                                   |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3614d-109">Assembly-Manifeste</span><span class="sxs-lookup"><span data-stu-id="3614d-109">Assembly manifests</span></span>](assembly-manifests.md)                           | <span data-ttu-id="3614d-110">Beschreibt die Namen, Versionen, Ressourcen und Assemblyabhängigkeiten von parallelen Assemblys.</span><span class="sxs-lookup"><span data-stu-id="3614d-110">Describes the names, versions, resources, and assembly dependencies of side-by-side assemblies.</span></span>                                                                                                               |
| [<span data-ttu-id="3614d-111">Anwendungs Manifeste</span><span class="sxs-lookup"><span data-stu-id="3614d-111">Application manifests</span></span>](application-manifests.md)                     | <span data-ttu-id="3614d-112">Beschreibt die Namen und Versionen von freigegebenen parallelen Assemblys, die von der Anwendung zur Laufzeit gebunden werden sollen und die auch Metadaten für private parallele Assemblys enthalten, die von der Anwendung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3614d-112">Describes the names and versions of shared side-by-side assemblies that the application should bind to at run time and may also contain metadata for private side-by-side assemblies used by the application.</span></span> |
| [<span data-ttu-id="3614d-113">Anwendungs Konfigurationsdateien</span><span class="sxs-lookup"><span data-stu-id="3614d-113">Application Configuration Files</span></span>](application-configuration-files.md) | <span data-ttu-id="3614d-114">Leitet die Assemblyversionen von Assemblyabhängigkeiten mithilfe einer [Konfiguration pro Anwendung](per-application-configuration.md)um.</span><span class="sxs-lookup"><span data-stu-id="3614d-114">Redirects the assembly versions of assembly dependencies using [per-application configuration](per-application-configuration.md).</span></span>                                                                            |
| [<span data-ttu-id="3614d-115">Verleger Konfigurationsdateien</span><span class="sxs-lookup"><span data-stu-id="3614d-115">Publisher Configuration Files</span></span>](publisher-configuration-files.md)     | <span data-ttu-id="3614d-116">Leitet die Assemblyversionen von Assemblyabhängigkeiten pro Assembly mithilfe einer [Herausgeber Konfiguration](publisher-configuration.md)um.</span><span class="sxs-lookup"><span data-stu-id="3614d-116">Redirects the assembly versions of assembly dependencies on a per-assembly basis using a [publisher configuration](publisher-configuration.md).</span></span>                                                              |



 

<span data-ttu-id="3614d-117">Eine Auflistung des Manifest-Datei Schemas finden Sie unter [Manifest-Datei Schema](manifest-file-schema.md).</span><span class="sxs-lookup"><span data-stu-id="3614d-117">For a listing of the manifest file schema, see [Manifest File Schema](manifest-file-schema.md).</span></span>

<span data-ttu-id="3614d-118">Eine Auflistung des Schemas der Anwendungs Konfigurationsdatei finden Sie unter [Schema der Anwendungs Konfigurationsdatei](application-configuration-file-schema.md).</span><span class="sxs-lookup"><span data-stu-id="3614d-118">For a listing of the application configuration file schema, see [Application Configuration File Schema](application-configuration-file-schema.md).</span></span>

<span data-ttu-id="3614d-119">Eine Auflistung des Schema der Verleger Konfigurationsdatei finden Sie unter [Schema der Verleger Konfigurationsdatei](publisher-configuration-file-schema.md).</span><span class="sxs-lookup"><span data-stu-id="3614d-119">For a listing of the publisher configuration file schema, see [Publisher Configuration File Schema](publisher-configuration-file-schema.md).</span></span>

<span data-ttu-id="3614d-120">Andere Technologien erweitern das von der Windows-Versionsverwaltung und Konfigurations Manifeste verwendete Format.</span><span class="sxs-lookup"><span data-stu-id="3614d-120">Other technologies extend the format used by Windows versioning and configuration manifests.</span></span> <span data-ttu-id="3614d-121">Entwickler sollten sich auf die Dokumentation beziehen, die sich speziell auf die Technologie bezieht, die für Informationen über das Manifest-Format verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3614d-121">Developers should refer to the documentation that is specific to the technology being used for information about the manifest format.</span></span> <span data-ttu-id="3614d-122">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="3614d-122">For example:</span></span>

-   [<span data-ttu-id="3614d-123">ClickOnce</span><span class="sxs-lookup"><span data-stu-id="3614d-123">ClickOnce</span></span>](/visualstudio/deployment/clickonce-reference?view=vs-2015)
-   [<span data-ttu-id="3614d-124">Übersicht: Common Language Runtime (CLR)</span><span class="sxs-lookup"><span data-stu-id="3614d-124">Common Language Runtime</span></span>](/dotnet/standard/clr)
-   <span data-ttu-id="3614d-125">[Benutzerkontensteuerung (User Account Control, UAC)](/previous-versions/bb756929(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="3614d-125">[User Account Control (UAC)](/previous-versions/bb756929(v=msdn.10))</span></span>

 

 

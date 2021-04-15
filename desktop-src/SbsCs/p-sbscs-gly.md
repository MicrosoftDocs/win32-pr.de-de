---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9BC3D6A3-D8F5-42C6-9A68-68F1741207D7
title: P (isolierte Anwendungen und parallele Assemblys)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c70c0775af4a6245e74de474413c3741625456
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393358"
---
# <a name="p-isolated-applications-and-side-by-side-assemblies"></a><span data-ttu-id="a3cff-103">P (isolierte Anwendungen und parallele Assemblys)</span><span class="sxs-lookup"><span data-stu-id="a3cff-103">P (Isolated Applications and Side-by-side Assemblies)</span></span>

<span data-ttu-id="a3cff-104">[a](a-sbscs-gly.md) B C [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O P Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z</span><span class="sxs-lookup"><span data-stu-id="a3cff-104">[A](a-sbscs-gly.md) B C [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O P Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="a3cff-105"><span id="_win32_per_application_configuration_gly"></span><span id="_WIN32_PER_APPLICATION_CONFIGURATION_GLY"></span>**Konfiguration pro Anwendung**</span><span class="sxs-lookup"><span data-stu-id="a3cff-105"><span id="_win32_per_application_configuration_gly"></span><span id="_WIN32_PER_APPLICATION_CONFIGURATION_GLY"></span>**per-application configuration**</span></span>
</dt> <dd>

<span data-ttu-id="a3cff-106">Konfiguration, die die globale Anwendungskonfiguration einer bestimmten Assembly überschreiben kann.</span><span class="sxs-lookup"><span data-stu-id="a3cff-106">Configuration that can override a specific assembly's global application configuration.</span></span> <span data-ttu-id="a3cff-107">Eine anwendungsspezifische Konfiguration wird durch eine Anwendungs konfigurationsmanifest-Datei angegeben, die im selben Ordner wie die ausführbare Datei installiert ist.</span><span class="sxs-lookup"><span data-stu-id="a3cff-107">A per-application configuration is specified by an application configuration manifest file installed in the same folder as the executable file.</span></span> <span data-ttu-id="a3cff-108">Die Manifest-Datei beschreibt die Version bzw. den Bereich der Versionen von parallelen Assemblys, die von der Anwendung verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a3cff-108">The manifest file describes the version, or range of versions, of side-by-side assemblies to be used by the application.</span></span> <span data-ttu-id="a3cff-109">Die Konfiguration pro Anwendung kann verwendet werden, wenn eine neue Version einer Assembly nicht mit einer Anwendung kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="a3cff-109">Per-application configuration might be used when a new version of an assembly is incompatible with an application.</span></span> <span data-ttu-id="a3cff-110">In diesem Fall kann die standardmäßige oder globale Konfiguration der Anwendung für eine bestimmte parallele Assembly überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="a3cff-110">In this case, the application's default or global configuration can be overridden for a specific side-by-side assembly.</span></span>

</dd> <dt>

<span data-ttu-id="a3cff-111"><span id="_win32_private_side_by_side_assembly_gly"></span><span id="_WIN32_PRIVATE_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**private parallele Assembly**</span><span class="sxs-lookup"><span data-stu-id="a3cff-111"><span id="_win32_private_side_by_side_assembly_gly"></span><span id="_WIN32_PRIVATE_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**private side-by-side assembly**</span></span>
</dt> <dd>

<span data-ttu-id="a3cff-112">Eine private parallele Assembly ist nur für eine bestimmte Anwendung sichtbar.</span><span class="sxs-lookup"><span data-stu-id="a3cff-112">A private side-by-side assembly is only visible to a specified application.</span></span> <span data-ttu-id="a3cff-113">Sie wird lokal in einer isolierten Anwendung installiert, und der Assemblycode wird für den Anwendungskontext privat.</span><span class="sxs-lookup"><span data-stu-id="a3cff-113">It is installed locally to an isolated application and the assembly's code becomes private to the application context.</span></span> <span data-ttu-id="a3cff-114">Die Abhängigkeiten einer privaten parallelen Assembly werden in der Anwendungs Manifest-Datei beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a3cff-114">The dependencies of a private side-by-side assembly are described in the application manifest file.</span></span> <span data-ttu-id="a3cff-115">Private parallele Assemblys können verwendet werden, um die negativen Auswirkungen der assemblyfreigabe (z. b. dll-Konflikte) auszugleichen und die Anwendungs Bereitstellung zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="a3cff-115">Private side-by-side assemblies can be used to offset the negative effects of assembly sharing, such as DLL conflicts, and to facilitate application deployment.</span></span>

</dd> <dt>

<span data-ttu-id="a3cff-116"><span id="_win32_public_key_token_gly"></span><span id="_WIN32_PUBLIC_KEY_TOKEN_GLY"></span>**öffentliches Schlüssel Token**</span><span class="sxs-lookup"><span data-stu-id="a3cff-116"><span id="_win32_public_key_token_gly"></span><span id="_WIN32_PUBLIC_KEY_TOKEN_GLY"></span>**public key token**</span></span>
</dt> <dd>

<span data-ttu-id="a3cff-117">Eine hexadezimale Zeichenfolge mit 16 Zeichen, die die letzten 8 Bytes des SHA-1-Hashs des öffentlichen Schlüssels darstellt, unter dem die Assembly signiert ist.</span><span class="sxs-lookup"><span data-stu-id="a3cff-117">A 16-character hexadecimal string that represents the last 8 bytes of the SHA-1 hash of the public key under which the assembly is signed.</span></span> <span data-ttu-id="a3cff-118">Der öffentliche Schlüssel, der zum Signieren des Katalogs verwendet wird, muss 2048 Bit oder größer sein.</span><span class="sxs-lookup"><span data-stu-id="a3cff-118">The public key used to sign the catalog must be 2048 bits or greater.</span></span> <span data-ttu-id="a3cff-119">Erforderlich für alle freigegebenen parallelen Assemblys.</span><span class="sxs-lookup"><span data-stu-id="a3cff-119">Required for all shared side-by-side assemblies.</span></span>

</dd> </dl>

 

 




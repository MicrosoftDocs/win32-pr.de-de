---
title: Funktionen zum Signieren von sicheren Start Features für Kernelmodustreiber
description: Funktionen zum Signieren von sicheren Start Features für Kernelmodustreiber
ms.assetid: 7FF64BA2-89E3-4E6F-B542-7BC7BF7F4FB2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a63a8b1fca1677aa125bac96dfec290dcd736b5
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "106342168"
---
# <a name="secure-boot-feature-signing-requirements-for-kernel-mode-drivers"></a><span data-ttu-id="3c2bd-103">Funktionen zum Signieren von sicheren Start Features für Kernelmodustreiber</span><span class="sxs-lookup"><span data-stu-id="3c2bd-103">Secure boot feature signing requirements for kernel-mode drivers</span></span>

## <a name="platforms"></a><span data-ttu-id="3c2bd-104">Plattformen</span><span class="sxs-lookup"><span data-stu-id="3c2bd-104">Platforms</span></span>

<span data-ttu-id="3c2bd-105">**Clients** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="3c2bd-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="3c2bd-106">**Server** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3c2bd-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="3c2bd-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3c2bd-107">Description</span></span>

<span data-ttu-id="3c2bd-108">In Windows 8 und Windows Server 2012, einschließlich WinPE, wurde der Kernel gesperrt, um zu verhindern, dass Schadsoftware, die von Start-oder Rootkits eingeführt wurde, die Sicherheitsanforderungen des Windows-Betriebssystems für signierte Treiber umgeht.</span><span class="sxs-lookup"><span data-stu-id="3c2bd-108">In Windows 8 and Windows Server 2012, including WinPE, the kernel has been locked down to prevent malware introduced by boot or root kits from circumventing Windows operating system security requirements for signed drivers.</span></span>

<span data-ttu-id="3c2bd-109">Diese Änderung wirkt sich auf alle Kernelmodustreiber für Geräte aus, die den sicheren Start von Unified Extensible Firmware Interface (UEFI) unterstützen. UEFI Secure Boot ist für die Windows 8-Zertifizierung für Client Computer und optional für-Server erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3c2bd-109">This change affects all kernel-mode drivers for devices that support unified extensible firmware interface (UEFI) Secure Boot; UEFI Secure Boot is required for Windows 8 certification for client machines, and optional for servers.</span></span> <span data-ttu-id="3c2bd-110">Er wirkt sich nicht auf Benutzermodus-Treiber aus.</span><span class="sxs-lookup"><span data-stu-id="3c2bd-110">It does not affect user-mode drivers.</span></span>

<span data-ttu-id="3c2bd-111">Die Standard Entwicklung für Kernelmodustreiber umfasst entweder die Verwendung des kernelmodusdebuggens oder die Start Konfigurationsdaten-Einstellung (BCD) <testsigning> .</span><span class="sxs-lookup"><span data-stu-id="3c2bd-111">Standard development for kernel-mode drivers involves either the use of kernel mode debugging or the boot configuration data (BCD) <testsigning> setting.</span></span> <span data-ttu-id="3c2bd-112">Beide werden deaktiviert, wenn der sichere Start aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3c2bd-112">Both of these are disabled when Secured Boot is on.</span></span>

## <a name="manifestation"></a><span data-ttu-id="3c2bd-113">Ausstrahlung</span><span class="sxs-lookup"><span data-stu-id="3c2bd-113">Manifestation</span></span>

<span data-ttu-id="3c2bd-114">Kernelmodustreiber können nicht ausgeführt werden, wenn Sie von einer vertrauenswürdigen Zertifizierungsstelle nicht ordnungsgemäß signiert wurden.</span><span class="sxs-lookup"><span data-stu-id="3c2bd-114">Kernel-mode drivers will not run if they are not properly signed by a trusted certification authority (CA).</span></span> <span data-ttu-id="3c2bd-115">Das Betriebssystem lässt nicht zu, dass nicht vertrauenswürdige Treiber ausgeführt werden, und Standardmechanismen wie Kernel Debugging und TESTSIGNING sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="3c2bd-115">The operating system will not allow untrusted drivers to run and standard mechanisms like kernel debugging and testsigning will not be permitted.</span></span>

## <a name="mitigation"></a><span data-ttu-id="3c2bd-116">Minderung</span><span class="sxs-lookup"><span data-stu-id="3c2bd-116">Mitigation</span></span>

<span data-ttu-id="3c2bd-117">Zum Testen von Treibern müssen Sie den sicheren Start im BIOS deaktivieren und die anderen Anforderungen an die Test Signierung erfüllen (siehe unten).</span><span class="sxs-lookup"><span data-stu-id="3c2bd-117">To test drivers, you must disable Secure Boot in BIOS as well as meet the other test-signing requirements (see below).</span></span>

<span data-ttu-id="3c2bd-118">Wenn Treiber häufiger verteilt werden, müssen Sie von einer vertrauenswürdigen Zertifizierungsstelle ordnungsgemäß signiert werden.</span><span class="sxs-lookup"><span data-stu-id="3c2bd-118">When distributing drivers more widely they must be properly signed by a trusted CA.</span></span>

## <a name="resources"></a><span data-ttu-id="3c2bd-119">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="3c2bd-119">Resources</span></span>

-   <span data-ttu-id="3c2bd-120">[Signatur Treiber](/previous-versions/windows/hardware/design/dn653563(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3c2bd-120">[Signing Drivers](/previous-versions/windows/hardware/design/dn653563(v=vs.85))</span></span>

 

 
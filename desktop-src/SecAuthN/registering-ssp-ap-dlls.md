---
description: Nachdem Sie ein Security Support Provider-/Authentifizierungspaket (Dynamic Link Library, SSP/AP-dll) mit einem oder mehreren benutzerdefinierten Sicherheitspaketen entwickelt haben, müssen Sie diese registrieren.
ms.assetid: db0d899e-dbd4-40d3-98d8-4d9668c01453
title: Registrieren von SSP/AP-DLLs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d279459b91633e0ef45e6e6d57b43489699a657
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756426"
---
# <a name="registering-sspap-dlls"></a><span data-ttu-id="e0d6b-103">Registrieren von SSP/AP-DLLs</span><span class="sxs-lookup"><span data-stu-id="e0d6b-103">Registering SSP/AP DLLs</span></span>

<span data-ttu-id="e0d6b-104">Nach der Entwicklung eines [*Security Support Provider*](../secgloss/s-gly.md) / -[*Authentifizierungs Pakets*](../secgloss/a-gly.md) Dynamic Link Library (SSP/AP dll), das ein oder mehrere benutzerdefinierte [*Sicherheitspakete*](../secgloss/s-gly.md)enthält, müssen Sie diese registrieren.</span><span class="sxs-lookup"><span data-stu-id="e0d6b-104">After developing a [*security support provider*](../secgloss/s-gly.md)/[*authentication package*](../secgloss/a-gly.md) dynamic-link library (SSP/AP DLL) containing one or more custom [*security packages*](../secgloss/s-gly.md), you must register it.</span></span> <span data-ttu-id="e0d6b-105">Fügen Sie zu diesem Zweck den Namen Ihrer benutzerdefinierten SSP/AP-dll den Daten des folgenden Registrierungs Werts hinzu:</span><span class="sxs-lookup"><span data-stu-id="e0d6b-105">To do so, add the name of your custom SSP/AP DLL to the data of the following registry value:</span></span>

<span data-ttu-id="e0d6b-106">**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **LSA** \\ **Security Packages**</span><span class="sxs-lookup"><span data-stu-id="e0d6b-106">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**Lsa**\\**Security Packages**</span></span>

<span data-ttu-id="e0d6b-107">Die Daten für diesen Registrierungs Wert sind eine Liste der Namen von SSP/AP-DLLs ohne die Erweiterung ". dll".</span><span class="sxs-lookup"><span data-stu-id="e0d6b-107">The data for this registry value is a list of the names of SSP/AP DLLs, without the ".dll" extension.</span></span> <span data-ttu-id="e0d6b-108">Der Datentyp für diese Liste ist **" \_ reg \_ MultiSZ** ", sodass \\ zwischen den einzelnen DLL-Namen in der Liste ein NULL-Zeichen ("0") vorhanden sein muss.</span><span class="sxs-lookup"><span data-stu-id="e0d6b-108">The data type for this list is **REG\_MULTI\_SZ** so there must be a null character ('\\0') between each DLL name in the list.</span></span>

<span data-ttu-id="e0d6b-109">SSP/AP-DLLs werden in der Regel im Verzeichnis "% SystemRoot%/System32" gespeichert.</span><span class="sxs-lookup"><span data-stu-id="e0d6b-109">Typically, SSP/AP DLLs are stored in the %systemroot%/system32 directory.</span></span> <span data-ttu-id="e0d6b-110">Wenn dies der Pfad zu Ihrer benutzerdefinierten SSP/AP-dll ist, schließen Sie den Pfad nicht als Teil des DLL-namens ein.</span><span class="sxs-lookup"><span data-stu-id="e0d6b-110">If this is the path to your custom SSP/AP DLL then do not include the path as part of the DLL name.</span></span> <span data-ttu-id="e0d6b-111">Wenn sich die dll jedoch in einem anderen Pfad befindet, schließen Sie den gesamten Pfad zur dll in den Namen ein.</span><span class="sxs-lookup"><span data-stu-id="e0d6b-111">If, however, the DLL is in a different path, include the complete path to the DLL in the name.</span></span>

<span data-ttu-id="e0d6b-112">Jedes Mal, wenn das System gestartet wird, lädt die LSA die SSP/AP-DLLs in diese Liste und führt die Initialisierungs Sequenz aus, die im [LSA-Modus Initialisierung](lsa-mode-initialization.md)beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="e0d6b-112">Each time the system starts, the LSA loads the SSP/AP DLLs in this list and performs the initialization sequence described in [LSA-Mode Initialization](lsa-mode-initialization.md).</span></span>

### <a name="registering-a-custom-security-package-as-the-default-tls-ssp"></a><span data-ttu-id="e0d6b-113">Registrieren eines benutzerdefinierten Sicherheitspakets als Standard-TLS-SSP</span><span class="sxs-lookup"><span data-stu-id="e0d6b-113">Registering a custom security package as the default TLS SSP</span></span>

<span data-ttu-id="e0d6b-114">Nachdem Sie eine benutzerdefinierte TLS-Security Support Provider entwickelt und wie oben beschrieben registriert haben, müssen Sie Sie auch als "Standard TLS-SSP" registrieren.</span><span class="sxs-lookup"><span data-stu-id="e0d6b-114">After developing a custom TLS security support provider and registering it as described above, you must also register it as the “default TLS SSP.”</span></span> <span data-ttu-id="e0d6b-115">Füllen Sie hierzu den Paketnamen Ihres benutzerdefinierten SSP mit den Daten des folgenden Registrierungs Werts:</span><span class="sxs-lookup"><span data-stu-id="e0d6b-115">To do so, populate the package name of your custom SSP to the data of the following registry value:</span></span>

<span data-ttu-id="e0d6b-116">**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **LSA** \\ **Standard TLS SSP**</span><span class="sxs-lookup"><span data-stu-id="e0d6b-116">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**Lsa**\\**Default TLS SSP**</span></span>

<span data-ttu-id="e0d6b-117">Die Daten für diesen Registrierungs Wert sind der Paketname von SSP, nicht der Name der dll.</span><span class="sxs-lookup"><span data-stu-id="e0d6b-117">The data for this registry value is the package name of SSP, not the dll name.</span></span> <span data-ttu-id="e0d6b-118">Der Datentyp hierfür ist **reg \_ SZ**.</span><span class="sxs-lookup"><span data-stu-id="e0d6b-118">The data type for this is **REG\_SZ**.</span></span>

<span data-ttu-id="e0d6b-119">Benutzermodusanwendungen, die "Standard-TLS-SSP" verwenden, verwenden den hier registrierten Standard.</span><span class="sxs-lookup"><span data-stu-id="e0d6b-119">User mode applications which use “default TLS SSP” will use the default registered here.</span></span> <span data-ttu-id="e0d6b-120">Kernelmodusanwendungen oder Benutzermodusanwendungen, die "Microsoft Unified Security Protocol Provider" oder andere spezifische TLS-SSP-Namen verwenden, sind von dieser Änderung nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="e0d6b-120">Kernel mode applications or user mode applications which use “Microsoft Unified Security Protocol Provider” or other specific TLS SSP names will not be impacted by this change.</span></span>

> [!Note]  
> <span data-ttu-id="e0d6b-121">Diese Registrierungsinformationen beziehen sich ausschließlich auf SSP/AP-dll.</span><span class="sxs-lookup"><span data-stu-id="e0d6b-121">This registry information pertains to SSP/AP DLL's only.</span></span> <span data-ttu-id="e0d6b-122">Weitere Informationen zum Registrieren von SSPs (Security Support Providers) finden Sie unter [schreiben und Installieren eines Sicherheits Unterstützungs Anbieters](writing-and-installing-a-security-support-provider.md).</span><span class="sxs-lookup"><span data-stu-id="e0d6b-122">For information about registering security support providers (SSPs), see [Writing and Installing a Security Support Provider](writing-and-installing-a-security-support-provider.md).</span></span> <span data-ttu-id="e0d6b-123">Informationen zu den Unterschieden zwischen SSP/AP und SSP-DLLs finden Sie unter [SSP/APS im Vergleich zu SSPs](ssp-aps-versus-ssps.md).</span><span class="sxs-lookup"><span data-stu-id="e0d6b-123">For information about the differences between SSP/AP and SSP DLLs, see [SSP/APs vs. SSPs](ssp-aps-versus-ssps.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e0d6b-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e0d6b-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0d6b-125">Einschränkungen bei der Registrierung und Installation eines Sicherheitspakets</span><span class="sxs-lookup"><span data-stu-id="e0d6b-125">Restrictions around Registering and Installing a Security Package</span></span>](restrictions-around-registering-and-installing-a-security-package.md)
</dt> </dl>

 

 

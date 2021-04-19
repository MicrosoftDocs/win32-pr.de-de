---
title: WFP-API
description: Die WFP-API (Windows Filtering Platform) ist in die folgenden Komponenten unterteilt.
ms.assetid: ff3f0d74-7e0b-4a3e-b66d-eaa61b89038a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4230c82105f85c36e6fb112508a7128758b2ad60
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2020
ms.locfileid: "106338700"
---
# <a name="wfp-api"></a><span data-ttu-id="a14b1-103">WFP-API</span><span class="sxs-lookup"><span data-stu-id="a14b1-103">WFP API</span></span>

<span data-ttu-id="a14b1-104">Die WFP-API (Windows Filtering Platform) ist in die folgenden Komponenten unterteilt.</span><span class="sxs-lookup"><span data-stu-id="a14b1-104">The Windows Filtering Platform (WFP) API is divided into the following components.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a14b1-105">Komponente</span><span class="sxs-lookup"><span data-stu-id="a14b1-105">Component</span></span></th>
<th><span data-ttu-id="a14b1-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a14b1-106">Description</span></span></th>
<th><span data-ttu-id="a14b1-107">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="a14b1-107">Header Files</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="a14b1-108"><a href="/windows-hardware/drivers/ddi/_netvista/">Callout-API</a> (f) $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="a14b1-108"><a href="/windows-hardware/drivers/ddi/_netvista/">Callout API</a> (FWPS)${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="a14b1-109"><a href="/windows-hardware/drivers/ddi/_netvista/">Datentypen</a> , die von Legenden verwendet werden. <strong>Hinweis</strong>  Diese Datentypen sind im Microsoft Windows Driver Development Kit (DDK) dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="a14b1-109"><a href="/windows-hardware/drivers/ddi/_netvista/">Data types</a> used by callouts.<strong>Note</strong>  These data types are documented in the Microsoft Windows Driver Development Kit (DDK).</span></span><br/></td>
<td><dl> <span data-ttu-id="a14b1-110">"f"</span><span class="sxs-lookup"><span data-stu-id="a14b1-110">fwpstypes.h</span></span><br />
<span data-ttu-id="a14b1-111">"f"</span><span class="sxs-lookup"><span data-stu-id="a14b1-111">fwpstypes.idl</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a14b1-112"><a href="/windows-hardware/drivers/ddi/_netvista/">Funktionen</a> und <a href="/windows-hardware/drivers/ddi/_netvista/">Enumerationstypen</a> , die zum Implementieren von Legenden verwendet werden. <strong>Hinweis</strong>  Diese Funktionen und Enumerationstypen sind im DDK dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="a14b1-112"><a href="/windows-hardware/drivers/ddi/_netvista/">Functions</a> and <a href="/windows-hardware/drivers/ddi/_netvista/">enumerated types</a> used to implement callouts.<strong>Note</strong>  These functions and enumerated types are documented in the DDK.</span></span><br/></td>
<td><dl> <span data-ttu-id="a14b1-113">"f"</span><span class="sxs-lookup"><span data-stu-id="a14b1-113">fwpsu.h</span></span><br />
<span data-ttu-id="a14b1-114">"f"</span><span class="sxs-lookup"><span data-stu-id="a14b1-114">fwpsk.h</span></span><br />
</dl></td>

</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="a14b1-115">IKE/AuthIP API (IKEEXT) $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="a14b1-115">IKE/AuthIP API (IKEEXT)${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="a14b1-116"><a href="fwp-enums.md">Enumerierte Typen</a> und <a href="fwp-structs.md">Strukturen</a> , die zum Verwalten von IKE-und AuthIP-Hauptmodusrichtlinien-und-Sicherheits Zuordnungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a14b1-116"><a href="fwp-enums.md">Enumerated types</a> and <a href="fwp-structs.md">structures</a> used for managing IKE and AuthIP main mode (MM) policy and security associations.</span></span></td>
<td><dl> <span data-ttu-id="a14b1-117">iketypes. h</span><span class="sxs-lookup"><span data-stu-id="a14b1-117">iketypes.h</span></span><br />
<span data-ttu-id="a14b1-118">iketypes. idl</span><span class="sxs-lookup"><span data-stu-id="a14b1-118">iketypes.idl</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a14b1-119"><a href="fwp-ike-functions.md">Funktionen</a> zum Verwalten von IKE-und AuthIP mm-Richtlinien und-Sicherheits Zuordnungen.</span><span class="sxs-lookup"><span data-stu-id="a14b1-119"><a href="fwp-ike-functions.md">Functions</a> used for managing IKE and AuthIP MM policy and security associations.</span></span></td>
<td><dl> <span data-ttu-id="a14b1-120">"f"</span><span class="sxs-lookup"><span data-stu-id="a14b1-120">fwpmu.h</span></span><br />
<span data-ttu-id="a14b1-121">"f"</span><span class="sxs-lookup"><span data-stu-id="a14b1-121">fwpmk.h</span></span><br />
</dl></td>

</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="a14b1-122">IPSec-API (IPSec) $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="a14b1-122">IPsec API (IPSEC)${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="a14b1-123"><a href="fwp-enums.md">Enumerierte Typen</a> und <a href="fwp-structs.md">Strukturen</a> zum Verwalten von IPSec-Richtlinien und Sicherheits Zuordnungen.</span><span class="sxs-lookup"><span data-stu-id="a14b1-123"><a href="fwp-enums.md">Enumerated types</a> and <a href="fwp-structs.md">structures</a> used for managing IPsec policies and security associations.</span></span></td>
<td><dl> <span data-ttu-id="a14b1-124">ipsectypes. h</span><span class="sxs-lookup"><span data-stu-id="a14b1-124">ipsectypes.h</span></span><br />
<span data-ttu-id="a14b1-125">ipsectypes. idl</span><span class="sxs-lookup"><span data-stu-id="a14b1-125">ipsectypes.idl</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a14b1-126"><a href="fwp-ipsec-functions.md">Funktionen</a> zum Verwalten von IPSec-Richtlinien und Sicherheits Zuordnungen.</span><span class="sxs-lookup"><span data-stu-id="a14b1-126"><a href="fwp-ipsec-functions.md">Functions</a> used for managing IPsec policies and security associations.</span></span></td>
<td><dl> <span data-ttu-id="a14b1-127">"f"</span><span class="sxs-lookup"><span data-stu-id="a14b1-127">fwpmu.h</span></span><br />
<span data-ttu-id="a14b1-128">"f"</span><span class="sxs-lookup"><span data-stu-id="a14b1-128">fwpmk.h</span></span><br />
</dl></td>

</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="a14b1-129">Verwaltungs-API (f) $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="a14b1-129">Management API (FWPM)${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="a14b1-130"><a href="fwp-enums.md">Enumerierte Typen</a> und <a href="fwp-structs.md">Strukturen</a> , die zum Verwalten der Filter-Engine verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a14b1-130"><a href="fwp-enums.md">Enumerated types</a> and <a href="fwp-structs.md">structures</a> used for managing the filter engine.</span></span></td>
<td><dl> <span data-ttu-id="a14b1-131">"f"-Typen</span><span class="sxs-lookup"><span data-stu-id="a14b1-131">fwpmtypes.h</span></span><br />
<span data-ttu-id="a14b1-132">"f"-Typen. idl</span><span class="sxs-lookup"><span data-stu-id="a14b1-132">fwpmtypes.idl</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a14b1-133"><a href="fwp-mgmt-functions.md">Funktionen</a> , die zum Verwalten der Filter-Engine verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a14b1-133"><a href="fwp-mgmt-functions.md">Functions</a> used for managing the filter engine.</span></span> <span data-ttu-id="a14b1-134">Diese Funktionen werden verwendet, um die folgenden Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="a14b1-134">These functions are used to perform the following tasks:</span></span><br/>
<ul>
<li><span data-ttu-id="a14b1-135">Festlegen und Abfragen von Filtern, Anbietern und Callouts.</span><span class="sxs-lookup"><span data-stu-id="a14b1-135">Set and query filters, providers, and callouts.</span></span></li>
<li><span data-ttu-id="a14b1-136">Rufen Sie IPSec-Statistiken ab.</span><span class="sxs-lookup"><span data-stu-id="a14b1-136">Retrieve IPsec statistics.</span></span></li>
<li><span data-ttu-id="a14b1-137">Konfigurieren Sie die Windows-Filter Plattform.</span><span class="sxs-lookup"><span data-stu-id="a14b1-137">Configure the Windows Filtering Platform.</span></span></li>
</ul></td>
<td><dl> <span data-ttu-id="a14b1-138">"f"</span><span class="sxs-lookup"><span data-stu-id="a14b1-138">fwpmu.h</span></span><br />
<span data-ttu-id="a14b1-139">"f"</span><span class="sxs-lookup"><span data-stu-id="a14b1-139">fwpmk.h</span></span><br />
</dl></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="a14b1-140">Freigegebene API (f)</span><span class="sxs-lookup"><span data-stu-id="a14b1-140">Shared API (FWP)</span></span></td>
<td><span data-ttu-id="a14b1-141">Grundlegende <a href="fwp-enums.md">enumerierte Typen</a> und <a href="fwp-structs.md">Strukturen</a> , die von der Windows-Filter Plattform gemeinsam genutzt werden</span><span class="sxs-lookup"><span data-stu-id="a14b1-141">Fundamental <a href="fwp-enums.md">enumerated types</a> and <a href="fwp-structs.md">structures</a> shared across the Windows Filtering Platform.</span></span></td>
<td><dl> <span data-ttu-id="a14b1-142">"f"</span><span class="sxs-lookup"><span data-stu-id="a14b1-142">fwptypes.h</span></span><br />
<span data-ttu-id="a14b1-143">"wptypes. idl"</span><span class="sxs-lookup"><span data-stu-id="a14b1-143">fwptypes.idl</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="a14b1-144">Datentyp Namen sind Großbuchstaben und Unterstriche.</span><span class="sxs-lookup"><span data-stu-id="a14b1-144">Data type names are all upper-case and underscore-delimited.</span></span> <span data-ttu-id="a14b1-145">Der Name beginnt immer mit einem Präfix, das seine Komponentengruppe identifiziert, z. b. [**fwpm \_ PROVIDER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider0).</span><span class="sxs-lookup"><span data-stu-id="a14b1-145">The name always begins with a prefix that identifies its component group, such as [**FWPM\_PROVIDER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider0).</span></span>

<span data-ttu-id="a14b1-146">Funktionsnamen sind gemischte Groß-und Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="a14b1-146">Function names are mixed-case and case-delimited.</span></span> <span data-ttu-id="a14b1-147">Der Name beginnt immer mit einem Präfix, das seine Komponentengruppe identifiziert, z. b. [**FwpmProviderContextAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextadd0).</span><span class="sxs-lookup"><span data-stu-id="a14b1-147">The name always begins with a prefix that identifies its component group, such as [**FwpmProviderContextAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextadd0).</span></span>

<span data-ttu-id="a14b1-148">Die meisten Daten-und Funktionsnamen enden mit einer Versionsnummer.</span><span class="sxs-lookup"><span data-stu-id="a14b1-148">Most data and function names end with a version number.</span></span> <span data-ttu-id="a14b1-149">In der Header Datei "fwpvi. h" werden Versions unabhängige Daten-und Funktionsnamen der Version zugeordnet, die für die Verwendung mit einem bestimmten Betriebssystem geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="a14b1-149">The fwpvi.h header file maps version-independent data and function names to the version that is appropriate for use with a given operating system.</span></span> <span data-ttu-id="a14b1-150">Weitere Informationen finden Sie unter [WFP-Version-Independent Namen und für bestimmte Versionen von Windows](wfp-version-independent-names-and-targeting-specific-versions-of-windows.md).</span><span class="sxs-lookup"><span data-stu-id="a14b1-150">For more information, see [WFP Version-Independent Names and Targeting Specific Versions of Windows](wfp-version-independent-names-and-targeting-specific-versions-of-windows.md).</span></span>

<span data-ttu-id="a14b1-151">Jede Komponente ist nicht eigenständig.</span><span class="sxs-lookup"><span data-stu-id="a14b1-151">Each component does not stand alone.</span></span> <span data-ttu-id="a14b1-152">Beispielsweise werden die IKE-Hauptmodus-Richtlinien (mm) in der IKEEXT-Komponente definiert, jedoch in einem Anbieter Kontext gespeichert und einem Filter zugeordnet, der beide in der fwpm-API-Komponente enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="a14b1-152">For example, IKE main mode (MM) policies are defined in the IKEEXT component, but are stored in a provider context and are associated with a filter both of which are found in the FWPM API component.</span></span>

## <a name="user-mode-and-kernel-mode-public-header-files"></a><span data-ttu-id="a14b1-153">User-Mode und Kernel-Mode öffentliche Header Dateien</span><span class="sxs-lookup"><span data-stu-id="a14b1-153">User-Mode and Kernel-Mode Public Header Files</span></span>

<span data-ttu-id="a14b1-154">Die meisten WFP-Funktionen können entweder über den Benutzermodus oder den Kernel Modus aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="a14b1-154">Most of the WFP functions can be called from either user mode or kernel mode.</span></span> <span data-ttu-id="a14b1-155">Allerdings geben benutzermodusfunktionen einen **DWORD** -Wert zurück, der einen Win32-Fehlercode darstellt, wohingegen Kernel Modus-Funktionen einen **NTSTATUS** -Wert zurückgeben, der einen NT-Statuscode darstellt.</span><span class="sxs-lookup"><span data-stu-id="a14b1-155">However, user-mode functions return a **DWORD** value that represents a Win32 error code, whereas kernel-mode functions return an **NTSTATUS** value that represents an NT status code.</span></span> <span data-ttu-id="a14b1-156">Folglich sind Funktionsnamen und Semantik zwischen dem Benutzermodus und dem Kernel Modus identisch, aber die Funktions Signaturen sind nicht.</span><span class="sxs-lookup"><span data-stu-id="a14b1-156">As a result, function names and semantics are identical between user mode and kernel mode, but function signatures are not.</span></span> <span data-ttu-id="a14b1-157">Hierfür sind separate Benutzermodus-und kernelmodusspezifische Header für die Funktionsprototypen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a14b1-157">This requires separate user-mode and kernel-mode specific headers for the function prototypes.</span></span> <span data-ttu-id="a14b1-158">Die Header Dateinamen im Benutzermodus enden mit "u", und der kernelmodusdateiname endet mit "k".</span><span class="sxs-lookup"><span data-stu-id="a14b1-158">User-mode header file names end in "u" and kernel-mode header file names end in "k".</span></span>

<span data-ttu-id="a14b1-159">In der folgenden Tabelle werden die Win32-Header Dateien aufgelistet, die die WFP-Funktionen definieren.</span><span class="sxs-lookup"><span data-stu-id="a14b1-159">The following table lists the Win32 header files that define the WFP functions.</span></span>

| <span data-ttu-id="a14b1-160">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="a14b1-160">Header Files</span></span> | <span data-ttu-id="a14b1-161">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a14b1-161">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a14b1-162">"f"</span><span class="sxs-lookup"><span data-stu-id="a14b1-162">fwpmk.h</span></span>      | <span data-ttu-id="a14b1-163">Kernel Modus-Funktionsprototypen für die Komponenten "swpm", "IPSec" und "IKEEXT".</span><span class="sxs-lookup"><span data-stu-id="a14b1-163">Kernel-mode function prototypes for FWPM, IPsec, and IKEEXT components.</span></span> <span data-ttu-id="a14b1-164">Nur im DDK verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a14b1-164">Available in the DDK only.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="a14b1-165">"f"</span><span class="sxs-lookup"><span data-stu-id="a14b1-165">fwpmu.h</span></span>      | <span data-ttu-id="a14b1-166">Im Benutzermodus-Funktionsprototypen für die Komponenten "swpm", "IPSec" und "IKEEXT".</span><span class="sxs-lookup"><span data-stu-id="a14b1-166">User-mode function prototypes for FWPM, IPsec, and IKEEXT components.</span></span> <span data-ttu-id="a14b1-167">Nur im Microsoft Windows Software Development Kit (SDK) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a14b1-167">Available in the Microsoft Windows Software Development Kit (SDK) only.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="a14b1-168">"f"</span><span class="sxs-lookup"><span data-stu-id="a14b1-168">fwpsk.h</span></span>      | <span data-ttu-id="a14b1-169">Kernel Modus-Funktionsprototypen und enumerierte Typen für die fwps-Komponente.</span><span class="sxs-lookup"><span data-stu-id="a14b1-169">Kernel-mode function prototypes and enumerated types for FWPS component.</span></span> <span data-ttu-id="a14b1-170">Nur im DDK verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a14b1-170">Available in the DDK only.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="a14b1-171">"f"</span><span class="sxs-lookup"><span data-stu-id="a14b1-171">fwpsu.h</span></span>      | <span data-ttu-id="a14b1-172">Funktionsprototypen im Benutzermodus und enumerierte Typen für die fwps-Komponente.</span><span class="sxs-lookup"><span data-stu-id="a14b1-172">User-mode function prototypes and enumerated types for FWPS component.</span></span> <span data-ttu-id="a14b1-173">Nur in der Windows SDK verfügbar. **Hinweis**  Die Enumerationstypen des Benutzermodus-fwps sind identisch mit den Enumerationstypen für den Kernel Modus-fwps.</span><span class="sxs-lookup"><span data-stu-id="a14b1-173">Available in the Windows SDK only.**Note**  The user-mode FWPS enumerated types are identical to the kernel-mode FWPS enumerated types.</span></span> <span data-ttu-id="a14b1-174">Diese Typen werden daher nur im DDK dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="a14b1-174">In consequence, these types are documented in the DDK only.</span></span><br/> <span data-ttu-id="a14b1-175">**Hinweis**  Die Prototypen von fwps-Funktionen im Benutzermodus sind identisch mit den Prototypen der fwps-Funktion im Kernelmodus, mit Ausnahme des Rückgabecodes.</span><span class="sxs-lookup"><span data-stu-id="a14b1-175">**Note**  The user-mode FWPS function prototypes are identical to the kernel-mode FWPS function prototypes with the exception of the return code.</span></span> <span data-ttu-id="a14b1-176">Fwps-Funktionen im Benutzermodus geben ein **DWORD** zurück, wohingegen fwps-Funktionen im Kernelmodus den **NTSTATUS** zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="a14b1-176">User-mode FWPS functions return a **DWORD**, whereas kernel-mode FWPS functions return an **NTSTATUS**.</span></span> <span data-ttu-id="a14b1-177">Folglich sind diese Funktionen nur im DDK dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="a14b1-177">In consequence, these functions are documented in the DDK only.</span></span><br/> |



 

<span data-ttu-id="a14b1-178">Alle benutzermodusfunktionen werden aus fwpuclnt.dll exportiert.</span><span class="sxs-lookup"><span data-stu-id="a14b1-178">All user-mode functions are exported from fwpuclnt.dll.</span></span> <span data-ttu-id="a14b1-179">Alle kernelmodusfunktionen werden aus fwpkclnt.sys exportiert.</span><span class="sxs-lookup"><span data-stu-id="a14b1-179">All kernel-mode functions are exported from fwpkclnt.sys.</span></span>

### <a name="management-fwpm-and-callout-fwps-data-types"></a><span data-ttu-id="a14b1-180">Datentypen für die Verwaltung ("f") und "Callout" ("f")</span><span class="sxs-lookup"><span data-stu-id="a14b1-180">Management (FWPM) and Callout (FWPS) Data Types</span></span>

<span data-ttu-id="a14b1-181">Die meisten Datentypen von Datentypen, die für Verwaltungsaufgaben verwendet werden, z. b. das Hinzufügen von Filtern oder Aufrufen einer Anwendung oder eines Treibers, verfügen über ein eigenes WPS-Pendant.</span><span class="sxs-lookup"><span data-stu-id="a14b1-181">Most FWPM data types, which are used for management tasks such as adding filters or callouts from an application or driver, have FWPS counterparts.</span></span> <span data-ttu-id="a14b1-182">Die fwps-Datentypen werden während der eigentlichen Filterung des Netzwerk Datenverkehrs im Kontext einer Legenden Routine für die Klassifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="a14b1-182">The FWPS data types are used during the actual filtering of network traffic, in the context of a callout routine for classification.</span></span>

<span data-ttu-id="a14b1-183">Zum Hinzufügen eines Filters zu einer bestimmten Filter-Engine-Ebene sollte der Programmierer z. b. einen fwpm-Typ verwenden, wie z `filter.layerKey = FWPM_LAYER_INBOUND_IPPACKET` . b.:.</span><span class="sxs-lookup"><span data-stu-id="a14b1-183">For example, in order to add a filter to a certain filtering engine layer, the programmer should use an FWPM type, like: `filter.layerKey = FWPM_LAYER_INBOUND_IPPACKET`.</span></span> <span data-ttu-id="a14b1-184">Um zu überprüfen, von welcher Ebene ein Aufruf aufgerufen wird, sollte der Programmierer den entsprechenden fwps-Typ verwenden: ` if (inFixedValues->layerId == FWPS_LAYER_INBOUND_IPPACKET)` .</span><span class="sxs-lookup"><span data-stu-id="a14b1-184">To check which layer a callout is being called from, the programmer should use the corresponding FWPS type: ` if (inFixedValues->layerId == FWPS_LAYER_INBOUND_IPPACKET)`.</span></span>

<span data-ttu-id="a14b1-185">Einige fwps-Gegenstücke zu fwpm-Datentypen erweitern die ursprünglichen fwpm-Datentypen.</span><span class="sxs-lookup"><span data-stu-id="a14b1-185">Some FWPS counterparts to FWPM data types are expanding the original FWPM data types.</span></span> <span data-ttu-id="a14b1-186">Um z. b. eine Filterbedingung auf vielen Filter-Engine-Ebenen hinzuzufügen, gibt der Programmierer `filterCondition.fieldKey = FWPM_CONDITION_IP_PROTOCOL` unabhängig von der Filter-Engine-Schicht an.</span><span class="sxs-lookup"><span data-stu-id="a14b1-186">For example, to add a filter condition at many filtering engine layers, the programmer specifies the `filterCondition.fieldKey = FWPM_CONDITION_IP_PROTOCOL` regardless of the filtering engine layer.</span></span> <span data-ttu-id="a14b1-187">Zum Ermitteln eines Filter Bedingungs Werts gibt der Programmierer einen ebenenspezifischen fwps-Typ an, z `inFixedValues->incomingValue[FWPS_FIELD_ALE_FLOW_ESTABLISHED_V4_IP_PROTOCOL]` . b.:.</span><span class="sxs-lookup"><span data-stu-id="a14b1-187">To find a filter condition value, the programmer specifies a layer specific FWPS type, like: `inFixedValues->incomingValue[FWPS_FIELD_ALE_FLOW_ESTABLISHED_V4_IP_PROTOCOL]`.</span></span>

<span data-ttu-id="a14b1-188">Die Datentypen für die Datentypen sind in der Regel kleiner als ihre Gegenstücke.</span><span class="sxs-lookup"><span data-stu-id="a14b1-188">The FWPS data types are generally smaller than their FWPM counterparts.</span></span> <span data-ttu-id="a14b1-189">Die Bezeichner der [**swpm-Filterungs Schicht**](management-filtering-layer-identifiers-.md) sind z. b. **GUID** s (16 Bytes), wohingegen die Bezeichner der [SWPS-filterebenenids](/windows-hardware/drivers/network/management-filtering-layer-identifiers) **UInt16** (16 Bit) sind.</span><span class="sxs-lookup"><span data-stu-id="a14b1-189">For example, the [**FWPM filtering layer identifiers**](management-filtering-layer-identifiers-.md) are **GUID** s (16-bytes) whereas the [FWPS filtering layer identifiers](/windows-hardware/drivers/network/management-filtering-layer-identifiers) are **UINT16** (16-bits).</span></span> <span data-ttu-id="a14b1-190">Die geringere Größe für die Datentypen von Datentypen verbessert die Systemleistung, da ganzzahlige Vergleiche **GUID** -Vergleiche für echt Zeit Datenverkehr überwiegen.</span><span class="sxs-lookup"><span data-stu-id="a14b1-190">The smaller size for FWPS data types improves system performance since integer comparisons outweigh **GUID** comparisons for real-time traffic.</span></span> <span data-ttu-id="a14b1-191">Außerdem wird der Kernel Speicher effizient verwendet, da die fwps-Typen alle im Kernel zum Verwalten der Filter verwendet werden, während die fwpm-Typen im Benutzermodus gespeichert werden, um die verschiedenen Ebenen zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="a14b1-191">Also, the kernel memory is used efficiently since the FWPS types are all used in the kernel for managing the filters, whereas the FWPM types are stored in user-mode to manage the different layers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a14b1-192">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a14b1-192">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a14b1-193">WFP-API-Objektmodell</span><span class="sxs-lookup"><span data-stu-id="a14b1-193">WFP API Object Model</span></span>](object-model.md)
</dt> <dt>

[<span data-ttu-id="a14b1-194">WFP-API-Objekt Verwaltung</span><span class="sxs-lookup"><span data-stu-id="a14b1-194">WFP API Object Management</span></span>](object-management.md)
</dt> </dl>


---
description: Details zur Änderung der Winsock-Katalog Änderung
ms.assetid: 4C86618D-4E79-486E-997F-9E2509FBF6B6
title: Details zur Änderung der Winsock-Katalog Änderung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6258ca87d5d1fba2de9364e5524110bb43c76513
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130404"
---
# <a name="winsock-catalog-change-tracing-details"></a><span data-ttu-id="56797-103">Details zur Änderung der Winsock-Katalog Änderung</span><span class="sxs-lookup"><span data-stu-id="56797-103">Winsock Catalog Change Tracing Details</span></span>

> [!Note]  
> <span data-ttu-id="56797-104">Mehrstufige Dienstanbieter sind veraltet.</span><span class="sxs-lookup"><span data-stu-id="56797-104">Layered Service Providers are deprecated.</span></span> <span data-ttu-id="56797-105">Ab Windows 8 und Windows Server 2012 verwenden Sie die [Windows-Filter Plattform](../fwp/windows-filtering-platform-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="56797-105">Starting with Windows 8 and Windows Server 2012, use [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md).</span></span>

 

<span data-ttu-id="56797-106">Die Änderungs Ereignis Ablauf Verfolgung von Winsock-Katalogen für Schicht-Dienstanbieter (LSPs) bezieht sich auf die LSP-Installation, LSP-Entfernung, LSP-Deaktivierung und Winsock-Katalog Zurücksetzungs Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="56797-106">Winsock Catalog Change event tracing for layered Service providers (LSPs) is related to LSP installation, LSP removal, LSP disable, and Winsock catalog reset operations.</span></span> <span data-ttu-id="56797-107">Alle der folgenden Ereignisse werden in den Channel *Microsoft-Windows-Winsock-WS2HELP/Operational* geschrieben, der sich von der anderen in Windows Vista und höher angemeldeten Winsock-Netzwerk Ereignis Ablauf Verfolgung unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="56797-107">All of the following events are written to the *Microsoft-Windows-Winsock-WS2HELP/Operational* channel which is different from the other Winsock network event tracing logged on Windows Vista and later.</span></span>

<span data-ttu-id="56797-108">Im folgenden werden die einzelnen Winsock-LSP-Ereignisse aufgeführt, die verfolgt werden können, und es wird beschrieben, welche Parameter und Informationen protokolliert werden.</span><span class="sxs-lookup"><span data-stu-id="56797-108">The following details each of the Winsock LSP events that can be traced and describes which parameters and information are logged.</span></span>

## <a name="lsp-install"></a><span data-ttu-id="56797-109">LSP-Installation</span><span class="sxs-lookup"><span data-stu-id="56797-109">LSP Install</span></span>

<span data-ttu-id="56797-110">Ereignis-ID = 1</span><span class="sxs-lookup"><span data-stu-id="56797-110">Event ID = 1</span></span>

<span data-ttu-id="56797-111">Ebene = 4 (Informationen)</span><span class="sxs-lookup"><span data-stu-id="56797-111">Level = 4 (Information)</span></span>

<span data-ttu-id="56797-112">Die folgenden Winsock-LSP-Ereignisse werden bei einem LSP-Installationsvorgang nachverfolgt:</span><span class="sxs-lookup"><span data-stu-id="56797-112">The following Winsock LSP events are traced for an LSP install operation:</span></span>

-   <span data-ttu-id="56797-113">Ein Protokolleintrag wird im Winsock-Katalog installiert.</span><span class="sxs-lookup"><span data-stu-id="56797-113">A protocol entry is installed into the Winsock catalog.</span></span>

<span data-ttu-id="56797-114">Die folgenden Parameter werden für ein LSP-Installations Ereignis protokolliert:</span><span class="sxs-lookup"><span data-stu-id="56797-114">The following parameters are logged for a LSP install event:</span></span>



| <span data-ttu-id="56797-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="56797-115">Parameter</span></span>                                                                                                | <span data-ttu-id="56797-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="56797-116">Description</span></span>                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56797-117"><span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>LSP-Name</span><span class="sxs-lookup"><span data-stu-id="56797-117"><span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>LSP Name</span></span><br/>     | <span data-ttu-id="56797-118">Der Name des LSP, der vom **szprotocol** -Member der [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur für den installierten LSP abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="56797-118">The name of the LSP as obtained from the **szProtocol** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being installed.</span></span><br/> |
| <span data-ttu-id="56797-119"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Sieren</span><span class="sxs-lookup"><span data-stu-id="56797-119"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalog</span></span><br/>         | <span data-ttu-id="56797-120">Der Winsock-Katalog (32-Bit oder 64-Bit), in dem der LSP installiert wird.</span><span class="sxs-lookup"><span data-stu-id="56797-120">The Winsock catalog (32-bit or 64-bit) where the LSP is being installed.</span></span> <span data-ttu-id="56797-121">Dies ist ein ganzzahliger Wert, der entweder 32 oder 64 ist.</span><span class="sxs-lookup"><span data-stu-id="56797-121">This is an integer value that is either 32 or 64.</span></span><br/>                                   |
| <span data-ttu-id="56797-122"><span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Ations</span><span class="sxs-lookup"><span data-stu-id="56797-122"><span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Installer</span></span><br/> | <span data-ttu-id="56797-123">Der Modul Dateiname der Anwendung, die die LSP-Installation aufruft.</span><span class="sxs-lookup"><span data-stu-id="56797-123">The module filename of the application making the LSP install call.</span></span><br/>                                                                                          |
| <span data-ttu-id="56797-124"><span id="GUID"></span><span id="guid"></span>GUID</span><span class="sxs-lookup"><span data-stu-id="56797-124"><span id="GUID"></span><span id="guid"></span>GUID</span></span><br/>                                            | <span data-ttu-id="56797-125">Der GUID-Wert des Winsock-Transport Anbieters, unter dem der LSP installiert wird.</span><span class="sxs-lookup"><span data-stu-id="56797-125">The GUID value of the Winsock transport provider that the LSP is being installed under.</span></span><br/>                                                                      |
| <span data-ttu-id="56797-126"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Kategorie</span><span class="sxs-lookup"><span data-stu-id="56797-126"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Category</span></span><br/>     | <span data-ttu-id="56797-127">Der **dwcatalogentryid** -Member der [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur für das zu installierende LSP.</span><span class="sxs-lookup"><span data-stu-id="56797-127">The **dwCatalogEntryId** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being installed.</span></span><br/>                                |



 

## <a name="lsp-uninstall"></a><span data-ttu-id="56797-128">LSP deinstallieren</span><span class="sxs-lookup"><span data-stu-id="56797-128">LSP Uninstall</span></span>

<span data-ttu-id="56797-129">Ereignis-ID = 2</span><span class="sxs-lookup"><span data-stu-id="56797-129">Event ID = 2</span></span>

<span data-ttu-id="56797-130">Ebene = 4 (Informationen)</span><span class="sxs-lookup"><span data-stu-id="56797-130">Level = 4 (Information)</span></span>

<span data-ttu-id="56797-131">Die folgenden Winsock-LSP-Ereignisse werden bei einem LSP-Deinstallations Vorgang nachverfolgt:</span><span class="sxs-lookup"><span data-stu-id="56797-131">The following Winsock LSP events are traced for an LSP uninstall operation:</span></span>

-   <span data-ttu-id="56797-132">Ein Protokolleintrag wird aus dem Winsock-Katalog entfernt.</span><span class="sxs-lookup"><span data-stu-id="56797-132">A protocol entry is removed from the Winsock catalog.</span></span>

<span data-ttu-id="56797-133">Die folgenden Parameter werden für ein LSP-Deinstallations Ereignis protokolliert:</span><span class="sxs-lookup"><span data-stu-id="56797-133">The following parameters are logged for a LSP uninstall event:</span></span>



| <span data-ttu-id="56797-134">Parameter</span><span class="sxs-lookup"><span data-stu-id="56797-134">Parameter</span></span>                                                                                                | <span data-ttu-id="56797-135">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="56797-135">Description</span></span>                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56797-136"><span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>LSP-Name</span><span class="sxs-lookup"><span data-stu-id="56797-136"><span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>LSP Name</span></span><br/>     | <span data-ttu-id="56797-137">Der Name des LSP, der vom **szprotocol** -Member der [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur für den zu entfernenden LSP abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="56797-137">The name of the LSP as obtained from the **szProtocol** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being removed.</span></span><br/> |
| <span data-ttu-id="56797-138"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Sieren</span><span class="sxs-lookup"><span data-stu-id="56797-138"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalog</span></span><br/>         | <span data-ttu-id="56797-139">Der Winsock-Katalog (32 Bit oder 64 Bit), in dem der LSP entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="56797-139">The Winsock catalog (32-bit or 64-bit) where the LSP is being removed.</span></span> <span data-ttu-id="56797-140">Dies ist ein ganzzahliger Wert, der entweder 32 oder 64 ist.</span><span class="sxs-lookup"><span data-stu-id="56797-140">This is an integer value that is either 32 or 64.</span></span><br/>                                   |
| <span data-ttu-id="56797-141"><span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Ations</span><span class="sxs-lookup"><span data-stu-id="56797-141"><span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Installer</span></span><br/> | <span data-ttu-id="56797-142">Der Modul Dateiname der Anwendung, die den LSP-Befehl zum Entfernen aufruft.</span><span class="sxs-lookup"><span data-stu-id="56797-142">The module filename of the application making the LSP remove call.</span></span><br/>                                                                                         |
| <span data-ttu-id="56797-143"><span id="GUID"></span><span id="guid"></span>GUID</span><span class="sxs-lookup"><span data-stu-id="56797-143"><span id="GUID"></span><span id="guid"></span>GUID</span></span><br/>                                            | <span data-ttu-id="56797-144">Der GUID-Wert des Winsock-Transport Anbieters, aus dem der LSP entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="56797-144">The GUID value of the Winsock transport provider that the LSP is removed from.</span></span><br/>                                                                             |
| <span data-ttu-id="56797-145"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Kategorie</span><span class="sxs-lookup"><span data-stu-id="56797-145"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Category</span></span><br/>     | <span data-ttu-id="56797-146">Der **dwcatalogentryid** -Member der [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur für den LSP, der entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="56797-146">The **dwCatalogEntryId** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being removed.</span></span><br/>                                |



 

## <a name="lsp-disable"></a><span data-ttu-id="56797-147">LSP deaktivieren</span><span class="sxs-lookup"><span data-stu-id="56797-147">LSP Disable</span></span>

<span data-ttu-id="56797-148">Ereignis-ID = 3</span><span class="sxs-lookup"><span data-stu-id="56797-148">Event ID = 3</span></span>

<span data-ttu-id="56797-149">Ebene = 4 (Informationen)</span><span class="sxs-lookup"><span data-stu-id="56797-149">Level = 4 (Information)</span></span>

<span data-ttu-id="56797-150">Die folgenden Winsock-LSP-Ereignisse werden für einen LSP-Deaktivierungs Vorgang nachverfolgt:</span><span class="sxs-lookup"><span data-stu-id="56797-150">The following Winsock LSP events are traced for an LSP disable operation:</span></span>

-   <span data-ttu-id="56797-151">Ein Protokolleintrag ist im Winsock-Katalog deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="56797-151">A protocol entry is disabled in the Winsock catalog.</span></span>

<span data-ttu-id="56797-152">Die folgenden Parameter werden für ein LSP-Deaktivierungs Ereignis protokolliert:</span><span class="sxs-lookup"><span data-stu-id="56797-152">The following parameters are logged for a LSP disable event:</span></span>



| <span data-ttu-id="56797-153">Parameter</span><span class="sxs-lookup"><span data-stu-id="56797-153">Parameter</span></span>                                                                                                | <span data-ttu-id="56797-154">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="56797-154">Description</span></span>                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56797-155"><span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>LSP-Name</span><span class="sxs-lookup"><span data-stu-id="56797-155"><span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>LSP Name</span></span><br/>     | <span data-ttu-id="56797-156">Der Name des LSP, der vom **szprotocol** -Member der [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur für das deaktivierte LSP abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="56797-156">The name of the LSP as obtained from the **szProtocol** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being disabled.</span></span><br/> |
| <span data-ttu-id="56797-157"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Sieren</span><span class="sxs-lookup"><span data-stu-id="56797-157"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalog</span></span><br/>         | <span data-ttu-id="56797-158">Der Winsock-Katalog (32 Bit oder 64 Bit), in dem der LSP deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="56797-158">The Winsock catalog (32-bit or 64-bit) where the LSP is being disabled.</span></span> <span data-ttu-id="56797-159">Dies ist ein ganzzahliger Wert, der entweder 32 oder 64 ist.</span><span class="sxs-lookup"><span data-stu-id="56797-159">This is an integer value that is either 32 or 64.</span></span><br/>                                   |
| <span data-ttu-id="56797-160"><span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Ations</span><span class="sxs-lookup"><span data-stu-id="56797-160"><span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Installer</span></span><br/> | <span data-ttu-id="56797-161">Der Modul Dateiname der Anwendung, die die LSP-Deaktivierung aufruft.</span><span class="sxs-lookup"><span data-stu-id="56797-161">The module filename of the application making the LSP disable call.</span></span><br/>                                                                                         |
| <span data-ttu-id="56797-162"><span id="GUID"></span><span id="guid"></span>GUID</span><span class="sxs-lookup"><span data-stu-id="56797-162"><span id="GUID"></span><span id="guid"></span>GUID</span></span><br/>                                            | <span data-ttu-id="56797-163">Der GUID-Wert des Winsock-Transport Anbieters, bei dem der LSP deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="56797-163">The GUID value of the Winsock transport provider where the LSP is being disabled.</span></span><br/>                                                                           |
| <span data-ttu-id="56797-164"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Kategorie</span><span class="sxs-lookup"><span data-stu-id="56797-164"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Category</span></span><br/>     | <span data-ttu-id="56797-165">Der **dwcatalogentryid** -Member der [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur für das deaktivierte LSP.</span><span class="sxs-lookup"><span data-stu-id="56797-165">The **dwCatalogEntryId** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being disabled.</span></span><br/>                                |



 

## <a name="winsock-catalog-reset"></a><span data-ttu-id="56797-166">Winsock-Katalog zurücksetzen</span><span class="sxs-lookup"><span data-stu-id="56797-166">Winsock Catalog Reset</span></span>

<span data-ttu-id="56797-167">Ereignis-ID = 4</span><span class="sxs-lookup"><span data-stu-id="56797-167">Event ID = 4</span></span>

<span data-ttu-id="56797-168">Ebene = 4 (Informationen)</span><span class="sxs-lookup"><span data-stu-id="56797-168">Level = 4 (Information)</span></span>

<span data-ttu-id="56797-169">Die folgenden Winsock-LSP-Ereignisse werden bei einem Winsock-Katalog Zurücksetzungs Vorgang nachverfolgt:</span><span class="sxs-lookup"><span data-stu-id="56797-169">The following Winsock LSP events are traced for a Winsock catalog reset operation:</span></span>

-   <span data-ttu-id="56797-170">Der Winsock-Katalog wird zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="56797-170">The Winsock catalog is reset.</span></span>

<span data-ttu-id="56797-171">Die folgenden Parameter werden für ein Winsock-Katalog Zurücksetzungs Ereignis protokolliert:</span><span class="sxs-lookup"><span data-stu-id="56797-171">The following parameters are logged for a Winsock catalog reset event:</span></span>



| <span data-ttu-id="56797-172">Parameter</span><span class="sxs-lookup"><span data-stu-id="56797-172">Parameter</span></span>                                                                                        | <span data-ttu-id="56797-173">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="56797-173">Description</span></span>                                                                                                              |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56797-174"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Sieren</span><span class="sxs-lookup"><span data-stu-id="56797-174"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalog</span></span><br/> | <span data-ttu-id="56797-175">Der Winsock-Katalog (32-Bit oder 64-Bit), der zurückgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="56797-175">The Winsock catalog (32-bit or 64-bit) that is being reset.</span></span> <span data-ttu-id="56797-176">Dies ist ein ganzzahliger Wert, der entweder 32 oder 64 ist.</span><span class="sxs-lookup"><span data-stu-id="56797-176">This is an integer value that is either 32 or 64.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="56797-177">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="56797-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56797-178">Kontrolle über die Winsock-Ablauf Verfolgung</span><span class="sxs-lookup"><span data-stu-id="56797-178">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="56797-179">Winsock-Ablauf Verfolgung</span><span class="sxs-lookup"><span data-stu-id="56797-179">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="56797-180">Winsock-Ablauf Verfolgungs Ebenen</span><span class="sxs-lookup"><span data-stu-id="56797-180">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> <dt>

[<span data-ttu-id="56797-181">Details der Winsock-Netzwerk Ereignis Ablauf Verfolgung</span><span class="sxs-lookup"><span data-stu-id="56797-181">Winsock Network Event Tracing Details</span></span>](winsock-tracing-event-details.md)
</dt> </dl>

 

 

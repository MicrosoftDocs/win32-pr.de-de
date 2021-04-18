---
description: Verwenden des Certified Output Protection-Protokolls (COPP)
ms.assetid: 23eebe93-416b-48c8-a05f-019e38b9a660
title: Verwenden des Certified Output Protection-Protokolls (COPP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76460e335985c2aab7f9047b55d2df05aace0269
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357879"
---
# <a name="using-certified-output-protection-protocol-copp"></a><span data-ttu-id="647ae-103">Verwenden des Certified Output Protection-Protokolls (COPP)</span><span class="sxs-lookup"><span data-stu-id="647ae-103">Using Certified Output Protection Protocol (COPP)</span></span>

<span data-ttu-id="647ae-104">Mit dem Certified Output Protection Protocol (COPP) kann eine Anwendung einen Videodaten Strom beim Durchlaufen vom Grafikadapter zum Anzeigegerät schützen.</span><span class="sxs-lookup"><span data-stu-id="647ae-104">Certified Output Protection Protocol (COPP) enables an application to protect a video stream as it travels from the graphics adapter to the display device.</span></span> <span data-ttu-id="647ae-105">Eine Anwendung kann COPP verwenden, um zu ermitteln, welche Art von physischem Connector mit dem Anzeigegerät verbunden ist und welche Arten von Ausgabe Schutz verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="647ae-105">An application can use COPP to discover what kind of physical connector is attached to the display device, and what types of output protection are available.</span></span> <span data-ttu-id="647ae-106">Schutzmechanismen umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="647ae-106">Protection mechanisms include the following:</span></span>

-   <span data-ttu-id="647ae-107">High-Bandwidth digitaler Content Protection (HDCP)</span><span class="sxs-lookup"><span data-stu-id="647ae-107">High-Bandwidth Digital Content Protection (HDCP)</span></span>
-   <span data-ttu-id="647ae-108">Copy Generation Management System – Analog (CGMS-A)</span><span class="sxs-lookup"><span data-stu-id="647ae-108">Copy Generation Management System — Analog (CGMS-A)</span></span>
-   <span data-ttu-id="647ae-109">Der Schutz von analogen Kopien (ACP)</span><span class="sxs-lookup"><span data-stu-id="647ae-109">Analog Copy Protection (ACP)</span></span>

<span data-ttu-id="647ae-110">Wenn der Grafikadapter einen dieser Mechanismen unterstützt, kann die Anwendung COPP zum Festlegen der Schutz Ebene verwenden.</span><span class="sxs-lookup"><span data-stu-id="647ae-110">If the graphics adapter supports one of these mechanisms, the application can use COPP to set the protection level.</span></span>

<span data-ttu-id="647ae-111">COPP definiert ein Protokoll, das verwendet wird, um einen sicheren Kommunikationskanal mit dem Grafiktreiber einzurichten.</span><span class="sxs-lookup"><span data-stu-id="647ae-111">COPP defines a protocol that is used to establish a secure communications channel with the graphics driver.</span></span> <span data-ttu-id="647ae-112">Er verwendet Message Authentication Codes (Macs), um die Integrität der von der Anwendung und dem Anzeigetreiber übergebenen COPP-Befehle zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="647ae-112">It uses Message Authentication Codes (MACs) to verify the integrity of the COPP commands that are passed between the application and the display driver.</span></span> <span data-ttu-id="647ae-113">Die Anwendung verwendet COPP durch Aufrufen von Methoden in der [**iamcertifiedoutputprotection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) -Schnittstelle des DirectShow-Video Mischungs-rendererfilters (VMR-7 oder VMR-9).</span><span class="sxs-lookup"><span data-stu-id="647ae-113">The application uses COPP by calling methods on the [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) interface of the DirectShow Video Mixing Renderer filter (VMR-7 or VMR-9).</span></span>

<span data-ttu-id="647ae-114">COPP definiert keine Informationen zu den Richtlinien für digitale Rechte, die möglicherweise für digitale Medieninhalte gelten.</span><span class="sxs-lookup"><span data-stu-id="647ae-114">COPP does not define anything about the digital rights policies that might apply to digital media content.</span></span> <span data-ttu-id="647ae-115">Außerdem implementiert COPP selbst keine Ausgabe Schutzsysteme.</span><span class="sxs-lookup"><span data-stu-id="647ae-115">Also, COPP itself does not implement any output protection systems.</span></span> <span data-ttu-id="647ae-116">Das COPP-Protokoll bietet lediglich eine Möglichkeit zum Festlegen und Abfragen von Schutz Ebenen auf dem Grafikadapter mithilfe der Schutzsysteme, die vom Adapter bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="647ae-116">The COPP protocol simply provides a way to set and query protection levels on the graphics adapter, using the protection systems provided by the adapter.</span></span>

<span data-ttu-id="647ae-117">In diesem Abschnitt wird davon ausgegangen, dass Sie mit den folgenden Technologien vertraut sind:</span><span class="sxs-lookup"><span data-stu-id="647ae-117">This section assumes that you are familiar with the following technologies:</span></span>

-   <span data-ttu-id="647ae-118">DirectShow</span><span class="sxs-lookup"><span data-stu-id="647ae-118">DirectShow</span></span>
-   <span data-ttu-id="647ae-119">SDK für Windows Media-Format</span><span class="sxs-lookup"><span data-stu-id="647ae-119">Windows Media Format SDK</span></span>
-   <span data-ttu-id="647ae-120">XML</span><span class="sxs-lookup"><span data-stu-id="647ae-120">XML</span></span>
-   <span data-ttu-id="647ae-121">Kryptografie mit öffentlichem Schlüssel und symmetrische Kryptografie</span><span class="sxs-lookup"><span data-stu-id="647ae-121">Public-key cryptography and symmetric cryptography</span></span>

<span data-ttu-id="647ae-122">Die Codebeispiele in diesem Abschnitt verwenden die CryptoAPI von Microsoft, um kryptografische Vorgänge auszuführen.</span><span class="sxs-lookup"><span data-stu-id="647ae-122">The code examples in this section use Microsoft's CryptoAPI to perform cryptographic operations.</span></span> <span data-ttu-id="647ae-123">Dieser Abschnitt enthält die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="647ae-123">This section contains the following topics:</span></span>

-   [<span data-ttu-id="647ae-124">Übersicht über COPP</span><span class="sxs-lookup"><span data-stu-id="647ae-124">Overview of COPP</span></span>](overview-of-copp.md)
-   [<span data-ttu-id="647ae-125">Abrufen der Zertifikat Kette des Treibers</span><span class="sxs-lookup"><span data-stu-id="647ae-125">Obtaining the Driver's Certificate Chain</span></span>](obtaining-the-drivers-certificate-chain.md)
-   [<span data-ttu-id="647ae-126">Überprüfen der Zertifikat Kette</span><span class="sxs-lookup"><span data-stu-id="647ae-126">Validating the Certificate Chain</span></span>](validating-the-certificate-chain.md)
-   [<span data-ttu-id="647ae-127">Zertifikat Sperr Listen</span><span class="sxs-lookup"><span data-stu-id="647ae-127">Certificate Revocation Lists</span></span>](certificate-revocation-lists.md)
-   [<span data-ttu-id="647ae-128">Importieren des öffentlichen Schlüssels des Treibers</span><span class="sxs-lookup"><span data-stu-id="647ae-128">Importing the Driver's Public Key</span></span>](importing-the-drivers-public-key.md)
-   [<span data-ttu-id="647ae-129">Initiieren einer COPP-Sitzung</span><span class="sxs-lookup"><span data-stu-id="647ae-129">Initiating a COPP Session</span></span>](initiating-a-copp-session.md)
-   [<span data-ttu-id="647ae-130">Senden von COPP-Status Anforderungen</span><span class="sxs-lookup"><span data-stu-id="647ae-130">Sending COPP Status Requests</span></span>](sending-copp-status-requests.md)
-   [<span data-ttu-id="647ae-131">Senden von COPP-Befehlen</span><span class="sxs-lookup"><span data-stu-id="647ae-131">Sending COPP Commands</span></span>](sending-copp-commands.md)
-   [<span data-ttu-id="647ae-132">Testen, ob ein Grafiktreiber COPP unterstützt</span><span class="sxs-lookup"><span data-stu-id="647ae-132">Testing Whether a Graphics Driver Supports COPP</span></span>](testing-whether-a-graphics-driver-supports-copp.md)
-   [<span data-ttu-id="647ae-133">COPP-Abfrage Verweis</span><span class="sxs-lookup"><span data-stu-id="647ae-133">COPP Query Reference</span></span>](copp-query-reference.md)
-   [<span data-ttu-id="647ae-134">COPP-Befehlsreferenz</span><span class="sxs-lookup"><span data-stu-id="647ae-134">COPP Command Reference</span></span>](copp-command-reference.md)

## <a name="related-topics"></a><span data-ttu-id="647ae-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="647ae-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="647ae-136">Verwenden des Video Mischungs Renderers</span><span class="sxs-lookup"><span data-stu-id="647ae-136">Using the Video Mixing Renderer</span></span>](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 




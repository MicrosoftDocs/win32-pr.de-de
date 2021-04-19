---
description: In diesem Abschnitt werden die Dokument Technologien beschrieben, die von Microsoft Windows unterstützt werden.
ms.assetid: 14ae2c97-8596-46db-a55c-ef706d2cd00b
title: XPS-Dokumente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa96324014d00a2a9fc106347fbeafe9842dedd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350131"
---
# <a name="xps-documents"></a><span data-ttu-id="2f3f9-103">XPS-Dokumente</span><span class="sxs-lookup"><span data-stu-id="2f3f9-103">XPS Documents</span></span>

<span data-ttu-id="2f3f9-104">In diesem Abschnitt werden die Dokument Technologien beschrieben, die von Microsoft Windows unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="2f3f9-104">This section describes the document technologies that are supported by Microsoft Windows.</span></span>

-   [<span data-ttu-id="2f3f9-105">Auswählen einer Dokument Technologie</span><span class="sxs-lookup"><span data-stu-id="2f3f9-105">Choosing a Document Technology</span></span>](#choosing-a-document-technology)
-   [<span data-ttu-id="2f3f9-106">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="2f3f9-106">In This Section</span></span>](#in-this-section)
-   [<span data-ttu-id="2f3f9-107">XPS-Dokument Tools</span><span class="sxs-lookup"><span data-stu-id="2f3f9-107">XPS Document Tools</span></span>](#xps-document-tools)
-   [<span data-ttu-id="2f3f9-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2f3f9-108">Related topics</span></span>](#related-topics)


## <a name="choosing-a-document-technology"></a><span data-ttu-id="2f3f9-109">Auswählen einer Dokument Technologie</span><span class="sxs-lookup"><span data-stu-id="2f3f9-109">Choosing a Document Technology</span></span>

<span data-ttu-id="2f3f9-110">Microsoft stellt verschiedene Dokument Technologien zur Unterstützung einer Vielzahl von Dokument Anwendungen bereit:</span><span class="sxs-lookup"><span data-stu-id="2f3f9-110">Microsoft provides several different document technologies to support a variety of document applications:</span></span>

-   <span data-ttu-id="2f3f9-111">**XPS und openxps**</span><span class="sxs-lookup"><span data-stu-id="2f3f9-111">**XPS and OpenXPS**</span></span>

    <span data-ttu-id="2f3f9-112">XPS und openxps werden in Windows 8 und höheren Versionen von Windows unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2f3f9-112">XPS and OpenXPS are supported in Windows 8 and later versions of Windows.</span></span> <span data-ttu-id="2f3f9-113">Sehen Sie sich das obige Diagramm an, um das richtige Verwendungs Szenario für XPS und openxps zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="2f3f9-113">See the preceding diagram to determine the correct usage scenario for XPS and OpenXPS.</span></span> <span data-ttu-id="2f3f9-114">Weitere Informationen zu diesen Dokument Technologien finden Sie unter [Open XML Paper Specification (openxps)](https://www.ecma-international.org/publications/standards/Ecma-388.htm).</span><span class="sxs-lookup"><span data-stu-id="2f3f9-114">For more information about these document technologies, see [Open XML Paper Specification (OpenXPS)](https://www.ecma-international.org/publications/standards/Ecma-388.htm).</span></span>

    <span data-ttu-id="2f3f9-115">Bei Verwendung von openxps mit Windows 8 und Windows Server 2012 wird die Unterstützung nur über die [XPS-Dokument-API](documents-xps.md) bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="2f3f9-115">In the case of using OpenXPS with Windows 8 and Windows Server 2012, support is only provided via the [XPS Document API](documents-xps.md)</span></span>

    <span data-ttu-id="2f3f9-116">Wenn Sie zwischen Microsoft XPS (msxps) und openxps konvertieren müssen, hat Microsoft ein Tool (XPSConverter.exe) bereitgestellt, das es Ihnen ermöglicht, msxps-formatierte Dokumente in das openxps-Format zu konvertieren und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="2f3f9-116">If you need to convert between Microsoft XPS (MSXPS) and OpenXPS, then Microsoft has provided a tool (XPSConverter.exe) that allows you to convert MSXPS-formatted documents to the OpenXPS format and vice versa.</span></span> <span data-ttu-id="2f3f9-117">Das Tool ist Teil des Windows Driver Kit (WDK).</span><span class="sxs-lookup"><span data-stu-id="2f3f9-117">The tool is part of the Windows Driver Kit (WDK).</span></span> <span data-ttu-id="2f3f9-118">Informationen zum Herunterladen des WDK finden Sie unter Vorgehens [Weise beim Herunterladen des WDK](/windows-hardware/drivers/download-the-wdk).</span><span class="sxs-lookup"><span data-stu-id="2f3f9-118">To download the WDK, see [How to get the WDK](/windows-hardware/drivers/download-the-wdk).</span></span>

    <span data-ttu-id="2f3f9-119">Weitere Informationen zu openxps und Windows 8 finden Sie [unter openxps-Unterstützung unter Windows](/windows-hardware/drivers/print/driver-support-for-openxps).</span><span class="sxs-lookup"><span data-stu-id="2f3f9-119">And for more information about OpenXPS and Windows 8, see [OpenXPS Support in Windows](/windows-hardware/drivers/print/driver-support-for-openxps).</span></span>

-   <span data-ttu-id="2f3f9-120">**XPS-Dokument-API**</span><span class="sxs-lookup"><span data-stu-id="2f3f9-120">**XPS Document API**</span></span>

    <span data-ttu-id="2f3f9-121">Die XPS-Dokument-API ist eine native Windows-API, die das XPS-OM unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2f3f9-121">The XPS Document API is a native Windows API that supports the XPS OM.</span></span> <span data-ttu-id="2f3f9-122">Die XPS-Dokument-API wurde in Windows 7 eingeführt und kann im benutzermodusprogramm und in XPSDrv-Druckertreibern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2f3f9-122">The XPS Document API was introduced in Windows 7 and can be used in user-mode programs and XPSDrv printer drivers.</span></span>

    <span data-ttu-id="2f3f9-123">Weitere Informationen finden Sie in der XPS-Dokument-API und in der [XPS Digital Signature-API](xps-digital-signatures.md).</span><span class="sxs-lookup"><span data-stu-id="2f3f9-123">For more information, see the XPS Document API, and [XPS Digital Signature API](xps-digital-signatures.md).</span></span>

    <span data-ttu-id="2f3f9-124">\*Die XPS-Dokument-API wird auch in Windows Vista mit Service Pack 2 (SP2) mit dem Platt Form Update für Windows Vista und Windows Server 2008 mit SP2 unterstützt. dabei wird das Platt Form Update für Windows Server 2008 verwendet.</span><span class="sxs-lookup"><span data-stu-id="2f3f9-124">\*The XPS Document API is also supported in Windows Vista with Service Pack 2 (SP2) with the Platform Update for Windows Vista and Windows Server 2008 with SP2 using the Platform Update for Windows Server 2008.</span></span> <span data-ttu-id="2f3f9-125">Weitere Informationen zum Platt Form Update für Windows Vista oder zum Platt Form Update für Windows Server 2008 finden Sie unter [Platt Form Update für Windows Vista](/windows/desktop/win7ip/platform-update-for-windows-vista-portal) .</span><span class="sxs-lookup"><span data-stu-id="2f3f9-125">For more information about the Platform Update for Windows Vista or the Platform Update for Windows Server 2008, see [Platform Update for Windows Vista](/windows/desktop/win7ip/platform-update-for-windows-vista-portal)</span></span>

-   <span data-ttu-id="2f3f9-126">**.NET Framework**</span><span class="sxs-lookup"><span data-stu-id="2f3f9-126">**.NET Framework**</span></span>

    <span data-ttu-id="2f3f9-127">.NET Framework bietet Unterstützung für XPS-Dokumente für Benutzermodus-Programme mit verwaltetem Code.</span><span class="sxs-lookup"><span data-stu-id="2f3f9-127">.NET Framework provides XPS document support to user-mode, managed-code programs.</span></span>

    <span data-ttu-id="2f3f9-128">.NET Framework 3,0 wird unter Windows XP mit Service Pack 2 (SP2) und höheren Versionen von Windows-Client Betriebssystemen und Windows Server 2003 mit Service Pack 2 (SP2) und höheren Versionen von Windows Server-Betriebssystemen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2f3f9-128">.NET Framework 3.0 is supported on Windows XP with Service Pack 2 (SP2) and later versions of Windows client operating systems, and on Windows Server 2003 with Service Pack 2 (SP2) and later versions of Windows server operating systems.</span></span>

    <span data-ttu-id="2f3f9-129">.NET Framework 3,5 wird unter Windows XP-Versionen von Windows-Client Betriebssystemen und Windows Server 2003 und höheren Versionen von Windows Server-Betriebssystemen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2f3f9-129">.NET Framework 3.5 is supported on Windows XP versions of Windows client operating systems, and on Windows Server 2003 and later versions of Windows server operating systems.</span></span>

    > [!Note]  
    > <span data-ttu-id="2f3f9-130">Wir empfehlen die Verwendung von .NET Framework nur zum Erstellen von XPS-Dokumenten in Client Anwendungen, nicht in Server Anwendungen, es sei denn, die Anwendung wird regelmäßig beendet, wie es bei einer Client Anwendung der Fall wäre.</span><span class="sxs-lookup"><span data-stu-id="2f3f9-130">We recommend the use of .NET Framework for creating XPS documents in client applications only, not in server applications unless the application exits periodically, as it would if it were a client application.</span></span>

     

    <span data-ttu-id="2f3f9-131">Weitere Informationen zur Unterstützung von Dokumenten in .NET Framework finden Sie unter [Windows Presentation Foundation Dokumente](/previous-versions/dotnet/netframework-3.0/ms749165(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2f3f9-131">For more information about document support in .NET Framework, see [Windows Presentation Foundation Documents](/previous-versions/dotnet/netframework-3.0/ms749165(v=vs.85)).</span></span>

> [!Note]  
> <span data-ttu-id="2f3f9-132">Verwenden Sie zum Arbeiten mit XPS-Dokumenten in einem Programm entweder die native XPS-Dokument-API oder die .NET Framework. die gleichzeitige Verwendung von beiden im gleichen Programm wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2f3f9-132">To work with XPS documents in a program, use either the native XPS Document API or the .NET Framework; simultaneous use of both in the same program is not supported.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="2f3f9-133">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="2f3f9-133">In This Section</span></span>

<span data-ttu-id="2f3f9-134">In diesem Abschnitt werden die nativen Windows-Dokument Technologien beschrieben, die von Microsoft Windows unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="2f3f9-134">This section describes the native Windows document technologies that are supported by Microsoft Windows.</span></span>



|                                                                    |                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2f3f9-135">XPS-Dokument-API</span><span class="sxs-lookup"><span data-stu-id="2f3f9-135">XPS Document API</span></span>](documents-xps.md)<br/>                   | <span data-ttu-id="2f3f9-136">Bietet ein vertrauenswürdiges Format für elektronisches Papier.</span><span class="sxs-lookup"><span data-stu-id="2f3f9-136">Provides a trustworthy format for electronic paper.</span></span><br/> <span data-ttu-id="2f3f9-137">Die in diesem Abschnitt beschriebene XPS-Dokument-API bietet Programmen und XPSDrv-Druckertreibern Zugriff auf den Inhalt und die Metadaten eines XPS-Dokuments.</span><span class="sxs-lookup"><span data-stu-id="2f3f9-137">The XPS Document API that is described in this section gives programs and XPSDrv print drivers access to the content and metadata of an XPS document.</span></span><br/> |
| [<span data-ttu-id="2f3f9-138">XPS-API für digitale Signaturen</span><span class="sxs-lookup"><span data-stu-id="2f3f9-138">XPS Digital Signature API</span></span>](xps-digital-signatures.md)<br/> | <span data-ttu-id="2f3f9-139">Ermöglicht das Signieren von Dokumenten, die Überprüfung der Identität des Signatur Gebers und die Angabe, ob sich ein XPS-Dokument seit der Signierung geändert hat.</span><span class="sxs-lookup"><span data-stu-id="2f3f9-139">Enables document signing, verification of the signer's identity, and indication of whether an XPS document has changed since it was signed.</span></span><br/>                                                                          |
| [<span data-ttu-id="2f3f9-140">Glossar für XPS-Dokumente</span><span class="sxs-lookup"><span data-stu-id="2f3f9-140">XPS Documents Glossary</span></span>](xpsapi-glossary.md)<br/>           | <span data-ttu-id="2f3f9-141">Definitionen der Begriffe, die von der [XPS-Dokument-API](documents-xps.md) und der [XPS Digital Signature-API](xps-digital-signatures.md)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2f3f9-141">Definitions of terms used by the [XPS Document API](documents-xps.md) and the [XPS Digital Signature API](xps-digital-signatures.md).</span></span><br/>                                                                              |



 

## <a name="xps-document-tools"></a><span data-ttu-id="2f3f9-142">XPS-Dokument Tools</span><span class="sxs-lookup"><span data-stu-id="2f3f9-142">XPS Document Tools</span></span>

<span data-ttu-id="2f3f9-143">Die folgenden Tools sind verfügbar, um Sie beim Testen und Beheben von Problemen mit XPS-Dokument Dateien zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="2f3f9-143">The following tools are available to assist you with testing and troubleshooting of XPS document files.</span></span>

-   <span data-ttu-id="2f3f9-144">[IsXPS](/previous-versions/aa348104(v=vs.110))</span><span class="sxs-lookup"><span data-stu-id="2f3f9-144">[IsXPS](/previous-versions/aa348104(v=vs.110))</span></span>

    <span data-ttu-id="2f3f9-145">Testet die Konformität einer Datei mit der XML Paper Specification (XPS) und der "Open Packaging Conventions (OPC)"-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="2f3f9-145">Tests a file's conformity to the XML Paper Specification (XPS) and the Open Packaging Conventions (OPC) Specification.</span></span>

-   [<span data-ttu-id="2f3f9-146">Xpsanalyzer</span><span class="sxs-lookup"><span data-stu-id="2f3f9-146">XpsAnalyzer</span></span>](/windows-hardware/drivers/devtest/xpsanalyzer)

    <span data-ttu-id="2f3f9-147">Ein Befehlszeilen Tool, mit dem XPS-Dokument Dateien auf Kompatibilität mit der XPS 1,0-Spezifikation analysiert werden.</span><span class="sxs-lookup"><span data-stu-id="2f3f9-147">A command-prompt tool that analyzes XPS document files for compatibility with the XPS 1.0 specification.</span></span>

-   <span data-ttu-id="2f3f9-148">[Ptkonformität](/previous-versions/dd327476(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="2f3f9-148">[PTConform](/previous-versions/dd327476(v=msdn.10))</span></span>

    <span data-ttu-id="2f3f9-149">Ein Tool zur Überprüfung der Gültigkeit von PrintTicket-und printdocuments-Dokumenten.</span><span class="sxs-lookup"><span data-stu-id="2f3f9-149">A tool that checks the validity of PrintTicket and PrintCapabilities documents.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2f3f9-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2f3f9-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f3f9-151">XPS-Druck-API</span><span class="sxs-lookup"><span data-stu-id="2f3f9-151">XPS Print API</span></span>](./printing-with-the-xpsprint-api.md)
</dt> <dt>

[<span data-ttu-id="2f3f9-152">Verpackung</span><span class="sxs-lookup"><span data-stu-id="2f3f9-152">Packaging</span></span>](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[<span data-ttu-id="2f3f9-153">Drucken</span><span class="sxs-lookup"><span data-stu-id="2f3f9-153">Printing</span></span>](./printdocs-printing.md)
</dt> <dt>
  
<span data-ttu-id="2f3f9-154">[Beispielprogramm drucken](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208))</span><span class="sxs-lookup"><span data-stu-id="2f3f9-154">[Print Sample Program](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208))</span></span>
</dt> </dl>

 


---
description: In diesem Abschnitt werden die Dokumenttechnologien beschrieben, die von Microsoft Windows unterstützt werden.
ms.assetid: 14ae2c97-8596-46db-a55c-ef706d2cd00b
title: XPS-Dokumente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 625c2f04a43db9433fe125b52a4bbc08e37fb4f4
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119985"
---
# <a name="xps-documents"></a><span data-ttu-id="63be8-103">XPS-Dokumente</span><span class="sxs-lookup"><span data-stu-id="63be8-103">XPS Documents</span></span>

<span data-ttu-id="63be8-104">In diesem Abschnitt werden die Dokumenttechnologien beschrieben, die von Microsoft Windows unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="63be8-104">This section describes the document technologies that are supported by Microsoft Windows.</span></span>

-   [<span data-ttu-id="63be8-105">Auswählen einer Dokumenttechnologie</span><span class="sxs-lookup"><span data-stu-id="63be8-105">Choosing a Document Technology</span></span>](#choosing-a-document-technology)
-   [<span data-ttu-id="63be8-106">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="63be8-106">In This Section</span></span>](#in-this-section)
-   [<span data-ttu-id="63be8-107">XPS-Dokumenttools</span><span class="sxs-lookup"><span data-stu-id="63be8-107">XPS Document Tools</span></span>](#xps-document-tools)
-   [<span data-ttu-id="63be8-108">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="63be8-108">Related topics</span></span>](#related-topics)


## <a name="choosing-a-document-technology"></a><span data-ttu-id="63be8-109">Auswählen einer Dokumenttechnologie</span><span class="sxs-lookup"><span data-stu-id="63be8-109">Choosing a Document Technology</span></span>

<span data-ttu-id="63be8-110">Microsoft stellt verschiedene Dokumenttechnologien zur Unterstützung einer Vielzahl von Dokumentanwendungen zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="63be8-110">Microsoft provides several different document technologies to support a variety of document applications:</span></span>

-   <span data-ttu-id="63be8-111">**XPS und OpenXPS**</span><span class="sxs-lookup"><span data-stu-id="63be8-111">**XPS and OpenXPS**</span></span>

    <span data-ttu-id="63be8-112">XPS und OpenXPS werden in Windows 8 und neueren Versionen von Windows unterstützt.</span><span class="sxs-lookup"><span data-stu-id="63be8-112">XPS and OpenXPS are supported in Windows 8 and later versions of Windows.</span></span> <span data-ttu-id="63be8-113">Im obigen Diagramm finden Sie informationen zum richtigen Verwendungsszenario für XPS und OpenXPS.</span><span class="sxs-lookup"><span data-stu-id="63be8-113">See the preceding diagram to determine the correct usage scenario for XPS and OpenXPS.</span></span> <span data-ttu-id="63be8-114">Weitere Informationen zu diesen Dokumenttechnologien finden Sie unter [Open XML Paper Specification (OpenXPS).](https://www.ecma-international.org/publications/standards/Ecma-388.htm)</span><span class="sxs-lookup"><span data-stu-id="63be8-114">For more information about these document technologies, see [Open XML Paper Specification (OpenXPS)](https://www.ecma-international.org/publications/standards/Ecma-388.htm).</span></span>

    <span data-ttu-id="63be8-115">Bei Verwendung von OpenXPS mit Windows 8 und Windows Server 2012 wird die Unterstützung nur über die [XPS-Dokument-API bereitgestellt.](documents-xps.md)</span><span class="sxs-lookup"><span data-stu-id="63be8-115">In the case of using OpenXPS with Windows 8 and Windows Server 2012, support is only provided via the [XPS Document API](documents-xps.md)</span></span>

    <span data-ttu-id="63be8-116">Wenn Sie zwischen Microsoft XPS (MSXPS) und OpenXPS konvertieren müssen, hat Microsoft ein Tool (XPSConverter.exe) bereitgestellt, mit dem Sie MSXPS-formatierte Dokumente in das OpenXPS-Format konvertieren können und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="63be8-116">If you need to convert between Microsoft XPS (MSXPS) and OpenXPS, then Microsoft has provided a tool (XPSConverter.exe) that allows you to convert MSXPS-formatted documents to the OpenXPS format and vice versa.</span></span> <span data-ttu-id="63be8-117">Das Tool ist Teil des Windows-Treiberkit (WDK).</span><span class="sxs-lookup"><span data-stu-id="63be8-117">The tool is part of the Windows Driver Kit (WDK).</span></span> <span data-ttu-id="63be8-118">Informationen zum Herunterladen des WDK finden Sie unter [How to get the WDK](/windows-hardware/drivers/download-the-wdk).</span><span class="sxs-lookup"><span data-stu-id="63be8-118">To download the WDK, see [How to get the WDK](/windows-hardware/drivers/download-the-wdk).</span></span>

    <span data-ttu-id="63be8-119">Weitere Informationen zu OpenXPS und Windows 8 finden Sie unter [OpenXPS-Unterstützung in Windows.](/windows-hardware/drivers/print/driver-support-for-openxps)</span><span class="sxs-lookup"><span data-stu-id="63be8-119">And for more information about OpenXPS and Windows 8, see [OpenXPS Support in Windows](/windows-hardware/drivers/print/driver-support-for-openxps).</span></span>

-   <span data-ttu-id="63be8-120">**XPS-Dokument-API**</span><span class="sxs-lookup"><span data-stu-id="63be8-120">**XPS Document API**</span></span>

    <span data-ttu-id="63be8-121">Die XPS-Dokument-API ist eine native Windows-API, die XPS OM unterstützt.</span><span class="sxs-lookup"><span data-stu-id="63be8-121">The XPS Document API is a native Windows API that supports the XPS OM.</span></span> <span data-ttu-id="63be8-122">Die XPS-Dokument-API wurde in Windows 7 eingeführt und kann in Benutzermodusprogrammen und XPSDrv-Druckertreibern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="63be8-122">The XPS Document API was introduced in Windows 7 and can be used in user-mode programs and XPSDrv printer drivers.</span></span>

    <span data-ttu-id="63be8-123">Weitere Informationen finden Sie unter XPS Document API (XPS-Dokument-API) und [XPS Digital Signature API (XPS Digital Signature-API).](xps-digital-signatures.md)</span><span class="sxs-lookup"><span data-stu-id="63be8-123">For more information, see the XPS Document API, and [XPS Digital Signature API](xps-digital-signatures.md).</span></span>

    <span data-ttu-id="63be8-124">\*Die XPS-Dokument-API wird auch in Windows Vista mit Service Pack 2 (SP2) mit dem Plattformupdate für Windows Vista und Windows Server 2008 mit SP2 unter Verwendung des Plattformupdates für Windows Server 2008 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="63be8-124">\*The XPS Document API is also supported in Windows Vista with Service Pack 2 (SP2) with the Platform Update for Windows Vista and Windows Server 2008 with SP2 using the Platform Update for Windows Server 2008.</span></span> <span data-ttu-id="63be8-125">Weitere Informationen zum Plattformupdate für Windows Vista oder zum Plattformupdate für Windows Server 2008 finden Sie unter [Plattformupdate für Windows Vista.](/windows/desktop/win7ip/platform-update-for-windows-vista-portal)</span><span class="sxs-lookup"><span data-stu-id="63be8-125">For more information about the Platform Update for Windows Vista or the Platform Update for Windows Server 2008, see [Platform Update for Windows Vista](/windows/desktop/win7ip/platform-update-for-windows-vista-portal)</span></span>

-   <span data-ttu-id="63be8-126">**.NET Framework**</span><span class="sxs-lookup"><span data-stu-id="63be8-126">**.NET Framework**</span></span>

    <span data-ttu-id="63be8-127">.NET Framework xps-Dokumentunterstützung für Programme mit verwaltetem Code im Benutzermodus.</span><span class="sxs-lookup"><span data-stu-id="63be8-127">.NET Framework provides XPS document support to user-mode, managed-code programs.</span></span>

    <span data-ttu-id="63be8-128">.NET Framework 3.0 wird unter Windows XP mit Service Pack 2 (SP2) und neueren Versionen von Windows-Clientbetriebssystemen und unter Windows Server 2003 mit Service Pack 2 (SP2) und neueren Versionen von Windows Server-Betriebssystemen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="63be8-128">.NET Framework 3.0 is supported on Windows XP with Service Pack 2 (SP2) and later versions of Windows client operating systems, and on Windows Server 2003 with Service Pack 2 (SP2) and later versions of Windows server operating systems.</span></span>

    <span data-ttu-id="63be8-129">.NET Framework 3.5 wird unter Windows XP-Versionen von Windows-Clientbetriebssystemen und unter Windows Server 2003 und höher von Windows Server-Betriebssystemen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="63be8-129">.NET Framework 3.5 is supported on Windows XP versions of Windows client operating systems, and on Windows Server 2003 and later versions of Windows server operating systems.</span></span>

    > [!Note]  
    > <span data-ttu-id="63be8-130">Wir empfehlen die Verwendung von .NET Framework zum Erstellen von XPS-Dokumenten nur in Clientanwendungen, nicht in Serveranwendungen, es sei denn, die Anwendung wird regelmäßig beendet, wie es bei einer Clientanwendung der Fall wäre.</span><span class="sxs-lookup"><span data-stu-id="63be8-130">We recommend the use of .NET Framework for creating XPS documents in client applications only, not in server applications unless the application exits periodically, as it would if it were a client application.</span></span>

     

    <span data-ttu-id="63be8-131">Weitere Informationen zur Dokumentunterstützung in .NET Framework finden Sie unter [Windows Presentation Foundation Documents](/previous-versions/dotnet/netframework-3.0/ms749165(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="63be8-131">For more information about document support in .NET Framework, see [Windows Presentation Foundation Documents](/previous-versions/dotnet/netframework-3.0/ms749165(v=vs.85)).</span></span>

> [!Note]  
> <span data-ttu-id="63be8-132">Um mit XPS-Dokumenten in einem Programm zu arbeiten, verwenden Sie entweder die native XPS-Dokument-API oder .NET Framework; die gleichzeitige Verwendung von beidem im gleichen Programm wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="63be8-132">To work with XPS documents in a program, use either the native XPS Document API or the .NET Framework; simultaneous use of both in the same program is not supported.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="63be8-133">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="63be8-133">In This Section</span></span>

<span data-ttu-id="63be8-134">In diesem Abschnitt werden die nativen Windows-Dokumenttechnologien beschrieben, die von Microsoft Windows unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="63be8-134">This section describes the native Windows document technologies that are supported by Microsoft Windows.</span></span>



| <span data-ttu-id="63be8-135">Dokumenttechnologie</span><span class="sxs-lookup"><span data-stu-id="63be8-135">Document technology</span></span>                                                                   | <span data-ttu-id="63be8-136">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="63be8-136">Description</span></span>                                                                                                                                                                                                                                |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="63be8-137">XPS-Dokument-API</span><span class="sxs-lookup"><span data-stu-id="63be8-137">XPS Document API</span></span>](documents-xps.md)<br/>                   | <span data-ttu-id="63be8-138">Stellt ein vertrauenswürdiges Format für elektronisches Papier zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="63be8-138">Provides a trustworthy format for electronic paper.</span></span><br/> <span data-ttu-id="63be8-139">Die in diesem Abschnitt beschriebene XPS-Dokument-API gewährt Programmen und XPSDrv-Druckertreibern Zugriff auf den Inhalt und die Metadaten eines XPS-Dokuments.</span><span class="sxs-lookup"><span data-stu-id="63be8-139">The XPS Document API that is described in this section gives programs and XPSDrv print drivers access to the content and metadata of an XPS document.</span></span><br/> |
| [<span data-ttu-id="63be8-140">XPS Digital Signature-API</span><span class="sxs-lookup"><span data-stu-id="63be8-140">XPS Digital Signature API</span></span>](xps-digital-signatures.md)<br/> | <span data-ttu-id="63be8-141">Ermöglicht das Signieren von Dokumenten, die Überprüfung der Identität des Signaturers und das Anzeigen, ob sich ein XPS-Dokument seit seiner Signierung geändert hat.</span><span class="sxs-lookup"><span data-stu-id="63be8-141">Enables document signing, verification of the signer's identity, and indication of whether an XPS document has changed since it was signed.</span></span><br/>                                                                          |
| [<span data-ttu-id="63be8-142">XPS-Dokumente – Glossar</span><span class="sxs-lookup"><span data-stu-id="63be8-142">XPS Documents Glossary</span></span>](xpsapi-glossary.md)<br/>           | <span data-ttu-id="63be8-143">Definitionen von Begriffen, die von der [XPS-Dokument-API](documents-xps.md) und der [XPS Digital Signature-API verwendet werden.](xps-digital-signatures.md)</span><span class="sxs-lookup"><span data-stu-id="63be8-143">Definitions of terms used by the [XPS Document API](documents-xps.md) and the [XPS Digital Signature API](xps-digital-signatures.md).</span></span><br/>                                                                              |



 

## <a name="xps-document-tools"></a><span data-ttu-id="63be8-144">XPS-Dokumenttools</span><span class="sxs-lookup"><span data-stu-id="63be8-144">XPS Document Tools</span></span>

<span data-ttu-id="63be8-145">Die folgenden Tools sind verfügbar, um Sie beim Testen und Beheben von Problemen mit XPS-Dokumentdateien zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="63be8-145">The following tools are available to assist you with testing and troubleshooting of XPS document files.</span></span>

-   <span data-ttu-id="63be8-146">[IsXPS](/previous-versions/aa348104(v=vs.110))</span><span class="sxs-lookup"><span data-stu-id="63be8-146">[IsXPS](/previous-versions/aa348104(v=vs.110))</span></span>

    <span data-ttu-id="63be8-147">Testet die Konformität einer Datei mit der XML Paper Specification (XPS) und der Open Packaging-Konventionen (OPC)-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="63be8-147">Tests a file's conformity to the XML Paper Specification (XPS) and the Open Packaging Conventions (OPC) Specification.</span></span>

-   [<span data-ttu-id="63be8-148">XpsAnalyzer</span><span class="sxs-lookup"><span data-stu-id="63be8-148">XpsAnalyzer</span></span>](/windows-hardware/drivers/devtest/xpsanalyzer)

    <span data-ttu-id="63be8-149">Ein Eingabeaufforderungstool, das XPS-Dokumentdateien auf Kompatibilität mit der XPS 1.0-Spezifikation analysiert.</span><span class="sxs-lookup"><span data-stu-id="63be8-149">A command-prompt tool that analyzes XPS document files for compatibility with the XPS 1.0 specification.</span></span>

-   <span data-ttu-id="63be8-150">[PTConform](/previous-versions/dd327476(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="63be8-150">[PTConform](/previous-versions/dd327476(v=msdn.10))</span></span>

    <span data-ttu-id="63be8-151">Ein Tool, das die Gültigkeit von PrintTicket- und PrintCapabilities-Dokumenten überprüft.</span><span class="sxs-lookup"><span data-stu-id="63be8-151">A tool that checks the validity of PrintTicket and PrintCapabilities documents.</span></span>

## <a name="related-topics"></a><span data-ttu-id="63be8-152">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="63be8-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63be8-153">XPS-Druck-API</span><span class="sxs-lookup"><span data-stu-id="63be8-153">XPS Print API</span></span>](./printing-with-the-xpsprint-api.md)
</dt> <dt>

[<span data-ttu-id="63be8-154">Verpackung</span><span class="sxs-lookup"><span data-stu-id="63be8-154">Packaging</span></span>](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[<span data-ttu-id="63be8-155">Drucken</span><span class="sxs-lookup"><span data-stu-id="63be8-155">Printing</span></span>](./printdocs-printing.md)
</dt> <dt>
  
<span data-ttu-id="63be8-156">[Beispielprogramm drucken](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208))</span><span class="sxs-lookup"><span data-stu-id="63be8-156">[Print Sample Program](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208))</span></span>
</dt> </dl>

 


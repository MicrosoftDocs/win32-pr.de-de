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
# <a name="xps-documents"></a>XPS-Dokumente

In diesem Abschnitt werden die Dokumenttechnologien beschrieben, die von Microsoft Windows unterstützt werden.

-   [Auswählen einer Dokumenttechnologie](#choosing-a-document-technology)
-   [In diesem Abschnitt](#in-this-section)
-   [XPS-Dokumenttools](#xps-document-tools)
-   [Verwandte Themen](#related-topics)


## <a name="choosing-a-document-technology"></a>Auswählen einer Dokumenttechnologie

Microsoft stellt verschiedene Dokumenttechnologien zur Unterstützung einer Vielzahl von Dokumentanwendungen zur Verfügung:

-   **XPS und OpenXPS**

    XPS und OpenXPS werden in Windows 8 und neueren Versionen von Windows unterstützt. Im obigen Diagramm finden Sie informationen zum richtigen Verwendungsszenario für XPS und OpenXPS. Weitere Informationen zu diesen Dokumenttechnologien finden Sie unter [Open XML Paper Specification (OpenXPS).](https://www.ecma-international.org/publications/standards/Ecma-388.htm)

    Bei Verwendung von OpenXPS mit Windows 8 und Windows Server 2012 wird die Unterstützung nur über die [XPS-Dokument-API bereitgestellt.](documents-xps.md)

    Wenn Sie zwischen Microsoft XPS (MSXPS) und OpenXPS konvertieren müssen, hat Microsoft ein Tool (XPSConverter.exe) bereitgestellt, mit dem Sie MSXPS-formatierte Dokumente in das OpenXPS-Format konvertieren können und umgekehrt. Das Tool ist Teil des Windows-Treiberkit (WDK). Informationen zum Herunterladen des WDK finden Sie unter [How to get the WDK](/windows-hardware/drivers/download-the-wdk).

    Weitere Informationen zu OpenXPS und Windows 8 finden Sie unter [OpenXPS-Unterstützung in Windows.](/windows-hardware/drivers/print/driver-support-for-openxps)

-   **XPS-Dokument-API**

    Die XPS-Dokument-API ist eine native Windows-API, die XPS OM unterstützt. Die XPS-Dokument-API wurde in Windows 7 eingeführt und kann in Benutzermodusprogrammen und XPSDrv-Druckertreibern verwendet werden.

    Weitere Informationen finden Sie unter XPS Document API (XPS-Dokument-API) und [XPS Digital Signature API (XPS Digital Signature-API).](xps-digital-signatures.md)

    \*Die XPS-Dokument-API wird auch in Windows Vista mit Service Pack 2 (SP2) mit dem Plattformupdate für Windows Vista und Windows Server 2008 mit SP2 unter Verwendung des Plattformupdates für Windows Server 2008 unterstützt. Weitere Informationen zum Plattformupdate für Windows Vista oder zum Plattformupdate für Windows Server 2008 finden Sie unter [Plattformupdate für Windows Vista.](/windows/desktop/win7ip/platform-update-for-windows-vista-portal)

-   **.NET Framework**

    .NET Framework xps-Dokumentunterstützung für Programme mit verwaltetem Code im Benutzermodus.

    .NET Framework 3.0 wird unter Windows XP mit Service Pack 2 (SP2) und neueren Versionen von Windows-Clientbetriebssystemen und unter Windows Server 2003 mit Service Pack 2 (SP2) und neueren Versionen von Windows Server-Betriebssystemen unterstützt.

    .NET Framework 3.5 wird unter Windows XP-Versionen von Windows-Clientbetriebssystemen und unter Windows Server 2003 und höher von Windows Server-Betriebssystemen unterstützt.

    > [!Note]  
    > Wir empfehlen die Verwendung von .NET Framework zum Erstellen von XPS-Dokumenten nur in Clientanwendungen, nicht in Serveranwendungen, es sei denn, die Anwendung wird regelmäßig beendet, wie es bei einer Clientanwendung der Fall wäre.

     

    Weitere Informationen zur Dokumentunterstützung in .NET Framework finden Sie unter [Windows Presentation Foundation Documents](/previous-versions/dotnet/netframework-3.0/ms749165(v=vs.85)).

> [!Note]  
> Um mit XPS-Dokumenten in einem Programm zu arbeiten, verwenden Sie entweder die native XPS-Dokument-API oder .NET Framework; die gleichzeitige Verwendung von beidem im gleichen Programm wird nicht unterstützt.

 

## <a name="in-this-section"></a>In diesem Abschnitt

In diesem Abschnitt werden die nativen Windows-Dokumenttechnologien beschrieben, die von Microsoft Windows unterstützt werden.



| Dokumenttechnologie                                                                   | Beschreibung                                                                                                                                                                                                                                |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [XPS-Dokument-API](documents-xps.md)<br/>                   | Stellt ein vertrauenswürdiges Format für elektronisches Papier zur Verfügung.<br/> Die in diesem Abschnitt beschriebene XPS-Dokument-API gewährt Programmen und XPSDrv-Druckertreibern Zugriff auf den Inhalt und die Metadaten eines XPS-Dokuments.<br/> |
| [XPS Digital Signature-API](xps-digital-signatures.md)<br/> | Ermöglicht das Signieren von Dokumenten, die Überprüfung der Identität des Signaturers und das Anzeigen, ob sich ein XPS-Dokument seit seiner Signierung geändert hat.<br/>                                                                          |
| [XPS-Dokumente – Glossar](xpsapi-glossary.md)<br/>           | Definitionen von Begriffen, die von der [XPS-Dokument-API](documents-xps.md) und der [XPS Digital Signature-API verwendet werden.](xps-digital-signatures.md)<br/>                                                                              |



 

## <a name="xps-document-tools"></a>XPS-Dokumenttools

Die folgenden Tools sind verfügbar, um Sie beim Testen und Beheben von Problemen mit XPS-Dokumentdateien zu unterstützen.

-   [IsXPS](/previous-versions/aa348104(v=vs.110))

    Testet die Konformität einer Datei mit der XML Paper Specification (XPS) und der Open Packaging-Konventionen (OPC)-Spezifikation.

-   [XpsAnalyzer](/windows-hardware/drivers/devtest/xpsanalyzer)

    Ein Eingabeaufforderungstool, das XPS-Dokumentdateien auf Kompatibilität mit der XPS 1.0-Spezifikation analysiert.

-   [PTConform](/previous-versions/dd327476(v=msdn.10))

    Ein Tool, das die Gültigkeit von PrintTicket- und PrintCapabilities-Dokumenten überprüft.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[XPS-Druck-API](./printing-with-the-xpsprint-api.md)
</dt> <dt>

[Verpackung](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[Drucken](./printdocs-printing.md)
</dt> <dt>
  
[Beispielprogramm drucken](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208))
</dt> </dl>

 


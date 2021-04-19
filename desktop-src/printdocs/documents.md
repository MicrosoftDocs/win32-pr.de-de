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
# <a name="xps-documents"></a>XPS-Dokumente

In diesem Abschnitt werden die Dokument Technologien beschrieben, die von Microsoft Windows unterstützt werden.

-   [Auswählen einer Dokument Technologie](#choosing-a-document-technology)
-   [In diesem Abschnitt](#in-this-section)
-   [XPS-Dokument Tools](#xps-document-tools)
-   [Zugehörige Themen](#related-topics)


## <a name="choosing-a-document-technology"></a>Auswählen einer Dokument Technologie

Microsoft stellt verschiedene Dokument Technologien zur Unterstützung einer Vielzahl von Dokument Anwendungen bereit:

-   **XPS und openxps**

    XPS und openxps werden in Windows 8 und höheren Versionen von Windows unterstützt. Sehen Sie sich das obige Diagramm an, um das richtige Verwendungs Szenario für XPS und openxps zu ermitteln. Weitere Informationen zu diesen Dokument Technologien finden Sie unter [Open XML Paper Specification (openxps)](https://www.ecma-international.org/publications/standards/Ecma-388.htm).

    Bei Verwendung von openxps mit Windows 8 und Windows Server 2012 wird die Unterstützung nur über die [XPS-Dokument-API](documents-xps.md) bereitgestellt.

    Wenn Sie zwischen Microsoft XPS (msxps) und openxps konvertieren müssen, hat Microsoft ein Tool (XPSConverter.exe) bereitgestellt, das es Ihnen ermöglicht, msxps-formatierte Dokumente in das openxps-Format zu konvertieren und umgekehrt. Das Tool ist Teil des Windows Driver Kit (WDK). Informationen zum Herunterladen des WDK finden Sie unter Vorgehens [Weise beim Herunterladen des WDK](/windows-hardware/drivers/download-the-wdk).

    Weitere Informationen zu openxps und Windows 8 finden Sie [unter openxps-Unterstützung unter Windows](/windows-hardware/drivers/print/driver-support-for-openxps).

-   **XPS-Dokument-API**

    Die XPS-Dokument-API ist eine native Windows-API, die das XPS-OM unterstützt. Die XPS-Dokument-API wurde in Windows 7 eingeführt und kann im benutzermodusprogramm und in XPSDrv-Druckertreibern verwendet werden.

    Weitere Informationen finden Sie in der XPS-Dokument-API und in der [XPS Digital Signature-API](xps-digital-signatures.md).

    \*Die XPS-Dokument-API wird auch in Windows Vista mit Service Pack 2 (SP2) mit dem Platt Form Update für Windows Vista und Windows Server 2008 mit SP2 unterstützt. dabei wird das Platt Form Update für Windows Server 2008 verwendet. Weitere Informationen zum Platt Form Update für Windows Vista oder zum Platt Form Update für Windows Server 2008 finden Sie unter [Platt Form Update für Windows Vista](/windows/desktop/win7ip/platform-update-for-windows-vista-portal) .

-   **.NET Framework**

    .NET Framework bietet Unterstützung für XPS-Dokumente für Benutzermodus-Programme mit verwaltetem Code.

    .NET Framework 3,0 wird unter Windows XP mit Service Pack 2 (SP2) und höheren Versionen von Windows-Client Betriebssystemen und Windows Server 2003 mit Service Pack 2 (SP2) und höheren Versionen von Windows Server-Betriebssystemen unterstützt.

    .NET Framework 3,5 wird unter Windows XP-Versionen von Windows-Client Betriebssystemen und Windows Server 2003 und höheren Versionen von Windows Server-Betriebssystemen unterstützt.

    > [!Note]  
    > Wir empfehlen die Verwendung von .NET Framework nur zum Erstellen von XPS-Dokumenten in Client Anwendungen, nicht in Server Anwendungen, es sei denn, die Anwendung wird regelmäßig beendet, wie es bei einer Client Anwendung der Fall wäre.

     

    Weitere Informationen zur Unterstützung von Dokumenten in .NET Framework finden Sie unter [Windows Presentation Foundation Dokumente](/previous-versions/dotnet/netframework-3.0/ms749165(v=vs.85)).

> [!Note]  
> Verwenden Sie zum Arbeiten mit XPS-Dokumenten in einem Programm entweder die native XPS-Dokument-API oder die .NET Framework. die gleichzeitige Verwendung von beiden im gleichen Programm wird nicht unterstützt.

 

## <a name="in-this-section"></a>In diesem Abschnitt

In diesem Abschnitt werden die nativen Windows-Dokument Technologien beschrieben, die von Microsoft Windows unterstützt werden.



|                                                                    |                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [XPS-Dokument-API](documents-xps.md)<br/>                   | Bietet ein vertrauenswürdiges Format für elektronisches Papier.<br/> Die in diesem Abschnitt beschriebene XPS-Dokument-API bietet Programmen und XPSDrv-Druckertreibern Zugriff auf den Inhalt und die Metadaten eines XPS-Dokuments.<br/> |
| [XPS-API für digitale Signaturen](xps-digital-signatures.md)<br/> | Ermöglicht das Signieren von Dokumenten, die Überprüfung der Identität des Signatur Gebers und die Angabe, ob sich ein XPS-Dokument seit der Signierung geändert hat.<br/>                                                                          |
| [Glossar für XPS-Dokumente](xpsapi-glossary.md)<br/>           | Definitionen der Begriffe, die von der [XPS-Dokument-API](documents-xps.md) und der [XPS Digital Signature-API](xps-digital-signatures.md)verwendet werden.<br/>                                                                              |



 

## <a name="xps-document-tools"></a>XPS-Dokument Tools

Die folgenden Tools sind verfügbar, um Sie beim Testen und Beheben von Problemen mit XPS-Dokument Dateien zu unterstützen.

-   [IsXPS](/previous-versions/aa348104(v=vs.110))

    Testet die Konformität einer Datei mit der XML Paper Specification (XPS) und der "Open Packaging Conventions (OPC)"-Spezifikation.

-   [Xpsanalyzer](/windows-hardware/drivers/devtest/xpsanalyzer)

    Ein Befehlszeilen Tool, mit dem XPS-Dokument Dateien auf Kompatibilität mit der XPS 1,0-Spezifikation analysiert werden.

-   [Ptkonformität](/previous-versions/dd327476(v=msdn.10))

    Ein Tool zur Überprüfung der Gültigkeit von PrintTicket-und printdocuments-Dokumenten.

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

 


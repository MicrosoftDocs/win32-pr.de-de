---
title: Informationen zum Plattformupdate für Windows Vista
description: Bietet eine Übersicht über das Plattformupdate für Windows Vista und das Plattformupdate für Windows Server 2008 und deren Features.
ms.assetid: ec5f03ae-9454-4964-943f-f97821984254
keywords:
- Plattformupdate für Windows Server 2008
- Plattformupdate für Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb9751331bf764ee486afe20a9dccd7f6b4691fee15e5000ccf8157561656409
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964569"
---
# <a name="about-platform-update-for-windows-vista"></a>Informationen zum Plattformupdate für Windows Vista

Das Plattformupdate für Windows Vista und das Plattformupdate für Windows Server 2008 sind Betriebssystemupdates von Endbenutzern, die die Verwendung ausgewählter Windows 7-Technologien in früheren Versionen des Windows-Betriebssystems unterstützen. Die Updates umfassen eine Reihe von Laufzeitbibliotheken, die es Anwendungsentwicklern ermöglichen, aktuelle Releases als Ziel zu verwenden: Windows 7 und Windows Server 2008 R2 sowie frühere Versionen, Windows Vista und Windows Server 2008.

## <a name="summary-of-supported-api-by-technology"></a>Zusammenfassung der unterstützten API nach Technologie

Jede Technologie, die vom Plattformupdate für Windows Vista und dem Plattformupdate für Windows Server 2008-Updates unterstützt wird, enthält eine Reihe von APIs, die in einer Anwendung verwendet werden können, die auf frühere Versionen von Windows.

Weitere Informationen zur Verwendung von APIs, die von den Updates in einer Anwendung unterstützt werden, die auf frühere Versionen von Windows zielt, finden Sie unter [Developing Application for Previous Versions of Windows](developing-applications-for-previous-versions-of-windows.md).

> [!Note]  
> Einige APIs, die einer Technologie zugeordnet sind, werden möglicherweise nicht unterstützt, und das Verhalten, die Leistung oder die Anforderungen für einige unterstützte APIs können in den verschiedenen Windows variieren. Um Details zur unterstützten API für eine bestimmte Technologie zu erhalten, klicken Sie auf den Link in einer der Zusammenfassungstabellen, um zum Abschnitt zu dieser Technologie zu wechseln.

 

### <a name="technologies-supported-with-platform-update-for-windows-vista"></a>Mit Plattformupdate für Windows Vista unterstützte Technologien

Um Details zur unterstützten API für eine bestimmte Technologie zu erhalten, klicken Sie auf den Link in einer der Zusammenfassungstabellen, um zum Abschnitt zu dieser Technologie zu wechseln.

Die Technologien, die für Windows Vista und Windows XP mit dem Plattformupdate für Windows Vista unterstützt werden, sind in der folgenden Tabelle aufgeführt.

| Technologie                                                                                    | Windows Vista | Windows XP |
|-----------------------------------------------------------------------------------------------|---------------|------------|
| [Windows Automation-API](#windows-automation-api)                                             | Ja           | Ja        |
| [Windows Grafik-, Bildverarbeitungs- und XPS-Bibliothek](#windows-graphics-imaging-and-xps-library)        | Ja           | Nein         |
| [Windows Menüband- und Animations-Manager-Bibliothek](#windows-ribbon-and-animation-manager-library) | Ja           | Nein         |
| [Windows Plattform für portable Geräte](#windows-portable-devices-platform)                       | Ja           | Nein         |



 

### <a name="technologies-supported-with-platform-update-for-windows-server-2008"></a>Unterstützte Technologien mit Plattformupdate für Windows Server 2008

Um Details zur unterstützten API für eine bestimmte Technologie zu erhalten, klicken Sie auf den Link in einer der Zusammenfassungstabellen, um zum Abschnitt zu dieser Technologie zu wechseln.

Die technologien, die für Windows Server 2008 und Windows Server 2003 mit dem Plattformupdate für Windows Server 2008 unterstützt werden, sind in der folgenden Tabelle aufgeführt.

| Technologie                                                                                    | WindowsServer 2008 | Windows Server 2003 |
|-----------------------------------------------------------------------------------------------|---------------------|---------------------|
| [Windows Automation-API](#windows-automation-api)                                             | Ja                 | Ja                 |
| [Windows Grafik-, Bildverarbeitungs- und XPS-Bibliothek](#windows-graphics-imaging-and-xps-library)        | Ja                 | Nein                  |
| [Windows Menüband- und Animations-Manager-Bibliothek](#windows-ribbon-and-animation-manager-library) | Ja                 | Nein                  |
| [Windows Plattform für portable Geräte](#windows-portable-devices-platform)                       | Nein                  | Nein                  |



 

## <a name="descriptions-of-supported-api-by-technology"></a>Beschreibungen der unterstützten API nach Technologie

Um Details zur unterstützten API für eine bestimmte Technologie zu erhalten, klicken Sie auf den Link in einer der Zusammenfassungstabellen, um zum Abschnitt zu dieser Technologie zu wechseln.

-   [Windows Automation-API](#windows-automation-api)
-   [Windows Grafik-, Bildverarbeitungs- und XPS-Bibliothek](#windows-graphics-imaging-and-xps-library)
-   [Windows Menüband- und Animations-Manager-Bibliothek](#windows-ribbon-and-animation-manager-library)
-   [Windows Plattform für portable Geräte](#windows-portable-devices-platform)

### <a name="windows-automation-api"></a>Windows Automation-API

Windows Automation API 3.0 ist eine Reihe von DLLs und API-Elementen, mit denen At-Produkte (Assistive Technology) einen besseren Computerzugriff für Personen bieten können, die physische oder kognitive Schwierigkeiten, Beeinträchtigungen oder Behinderungen haben. Darüber hinaus ist Windows Automation API 3.0 eine ideale Technologie für die Implementierung automatisierter Testtools, da anwendungen mithilfe der Automation-API 3.0 auf die Elemente der Benutzeroberfläche (UI) anderer Anwendungen zugreifen und diese bearbeiten können.

Microsoft Active Accessibility (MSAA) und Benutzeroberflächenautomatisierung sind ähnlich, da beide eine Möglichkeit zum Verfügbar machen und Sammeln von Informationen über Benutzeroberflächenelemente und Steuerelemente bieten, um die Barrierefreiheit der Benutzeroberfläche und die Automatisierung von Softwaretests zu unterstützen. Benutzeroberflächenautomatisierung ist eine Windows Implementierung der Benutzeroberflächenautomatisierung Spezifikation. Es handelt sich um eine neuere Technologie, die viele der Einschränkungen von MSAA behandelt.

Weitere Informationen über die Windows Automation-API 3.0 finden Sie unter [Windows Automation-API: Übersicht.](/windows/desktop/WinAuto/windows-automation-api-overview)

Das Plattformupdate für Windows Vista und das Plattformupdate für Windows Server 2008 unterstützen die folgenden Windows Automation-API 3.0:

-   [Microsoft Active Accessibility (MSAA)](#microsoft-active-accessibility-msaa)
-   [Benutzeroberflächenautomatisierung](#ui-automation)

### <a name="windows-editions-eligible-for-the-updates"></a>Windows Für die Updates geeignete Editionen

Das Plattformupdate für Windows Vista und das Plattformupdate für Windows Server 2008 ermöglichen die Unterstützung der Windows Automation-API 3.0 für die editionen von Windows, wie in der folgenden Tabelle gezeigt.



<table>
<thead>
<tr class="header">
<th>Windows-Version</th>
<th>Für das Update geeignete Editionen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows Vista</td>
<td><dl> Starter mit SP2 (x86)<br />
Home Basic mit SP2 (x86 und amd64)<br />
Home Premium mit SP2 (x86 und amd64)<br />
Business with SP2 (x86 and amd64) (Geschäft mit SP2 (x86 und amd64))<br />
Enterprise mit SP2 (x86 und amd64)<br />
Ultimate mit SP2 (x86 und amd64)<br />
</dl></td>
</tr>
<tr class="even">
<td>Windows XP</td>
<td><dl> Windows XP Home mit SP3 (x86)<br />
Windows XP Professional mit SP3 (x86)<br />
</dl></td>
</tr>
<tr class="odd">
<td>Windows Server 2008</td>
<td><dl> Windows Server 2008 mit SP2 (x86 und amd64)<br />
</dl></td>
</tr>
<tr class="even">
<td>Windows Server 2003</td>
<td><dl> Windows Server 2003 mit SP2 (x86 und amd64)<br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="microsoft-active-accessibility-msaa"></a>Microsoft Active Accessibility (MSAA)

Microsoft Active Accessibility (MSAA) ist eine Legacytechnologie, die erstmals mit Windows 95 eingeführt wurde. Es handelt sich um eine Reihe von APIs, die die Art und Weise verbessern, wie AT-Produkte (Assistive Technology) mit Anwendungen funktionieren, die auf Microsoft Windows. Die API stellt Programmierschnittstellen und Methoden zum Verfügbar machen von Informationen über Benutzeroberflächenelemente bereit.

Weitere Informationen zu Microsoft Active Accessibility finden Sie in der technischen [Übersicht.](/windows/desktop/WinAuto/technical-overview)

### <a name="supported-microsoft-active-accessibility-api-elements"></a>Unterstützte Microsoft Active Accessibility-API-Elemente

Alle APIs werden in früheren Versionen von Windows unterstützt, die für das Plattformupdate für Windows Vista oder das Plattformupdate für Windows Server 2008 geeignet sind.

### <a name="ui-automation"></a>Benutzeroberflächenautomatisierung

Benutzeroberflächenautomatisierung ist eine neuere Technologie, die die Benutzeroberflächenautomatisierung-Spezifikation implementiert und viele der Einschränkungen Microsoft Active Accessibility. Es handelt sich um eine Gruppe von APIs, die programmgesteuerten Zugriff auf die Benutzeroberflächenelemente von Anwendungen ermöglichen. Die bereitgestellte API unterstützt Hilfstechnologieprodukte und automatisierte Testtools dabei, auf die standardmäßigen und benutzerdefinierten Benutzeroberflächenelemente einer Anwendung zuzugreifen, sie zu identifizieren und zu bearbeiten.

Weitere Informationen zu Benutzeroberflächenautomatisierung finden Sie unter [Windows Automation-API: Benutzeroberflächenautomatisierung](../winauto/entry-uiauto-win32.md).

### <a name="supported-ui-automation-api-elements"></a>Unterstützte Benutzeroberflächenautomatisierung-API-Elemente

Alle APIs werden in früheren Versionen von Windows unterstützt, die für das Plattformupdate für Windows Vista oder das Plattformupdate für Windows Server 2008 geeignet sind.

### <a name="running-ui-automation-on-previous-windows-versions"></a>Ausführen Benutzeroberflächenautomatisierung unter vorherigen Windows Versionen

Aufgrund der Unterschiede in der Art und Weise, wie die allgemeinen Steuerelemente und die Windows-Standardsteuerelemente in verschiedenen Windows-Versionen implementiert werden, gibt es möglicherweise geringfügige Unterschiede in den Informationen, die die Benutzeroberflächenautomatisierung-Proxys für diese Steuerelemente von einer Version zur anderen abrufen.

### <a name="windows-graphics-imaging-and-xps-library"></a>Windows Grafik-, Bildverarbeitungs- und XPS-Bibliothek

Das Plattformupdate für Windows Vista unterstützt die folgenden Windows 7-APIs aus der Windows-, Bildverarbeitungs- und XPS-Bibliothek:

-   [Direct2D](#direct2d)
-   [Direct3D](#direct3d)
-   [DirectWrite](#directwrite)
-   [Verpackung](#packaging)
-   [Windows-Bilderstellungskomponente](#windows-imaging-component)
-   [XPS-Dokument](#xps-document)
-   [XPS Print](#xps-print)

### <a name="windows-editions-eligible-for-the-updates"></a>Windows Für updates berechtigte Editionen

Das Plattformupdate für Windows Vista und das Plattformupdate für Windows Server 2008 ermöglichen Windows Unterstützung für Grafiken, Bildverarbeitung und XPS-Bibliothek für die Editionen von Windows in der folgenden Tabelle.



<table>
<thead>
<tr class="header">
<th>Windows-Version</th>
<th>Editionen, die für Updates berechtigt sind</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows Vista</td>
<td><dl> Starter mit SP2 (x86)<br />
Home Basic mit SP2 (x86 und amd64)<br />
Home Premium mit SP2 (x86 und amd64)<br />
Business with SP2 (x86 and amd64) (Geschäft mit SP2 (x86 und amd64))<br />
Enterprise mit SP2 (x86 und amd64)<br />
Ultimate mit SP2 (x86 und amd64)<br />
</dl></td>
</tr>
<tr class="even">
<td>Windows Server 2008</td>
<td><dl> Windows Server 2008 mit SP2 (x86 und amd64)<br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="direct2d"></a>Direct2D

Die Direct2D-API ist eine neue hardwarebeschleunigte 2D-Grafik-API im unmittelbaren Modus, die leistungsstarkes und qualitativ hochwertiges Rendering für 2D-Geometrie, Bitmaps und Text bereitstellt. Die Direct2D-API ist für eine gute Zusammenarbeit mit vorhandenem Code konzipiert, der GDI, GDI+ oder Direct3D verwendet.

Weitere Informationen zu Direct2D finden Sie unter [Informationen zu Direct2D.](/windows/desktop/Direct2D/direct2d-overview)

### <a name="supported-direct2d-api-elements"></a>Unterstützte Direct2D-API-Elemente

Alle APIs werden in früheren Versionen von Windows unterstützt, die für das Plattformupdate für Windows Vista oder das Plattformupdate für Windows Server 2008 berechtigt sind.

### <a name="running-direct2d-on-previous-windows-versions"></a>Ausführen von Direct2D unter vorherigen Windows Versionen

Wenn der WDDM 1.1-Treiber auf Windows Vista fehlt, wird die Leistung der Direct2D/GDI-Interoperabilität beeinträchtigt.

### <a name="direct3d"></a>Direct3D

Das Plattformupdate für Windows Vista bietet BGRA-Oberflächenunterstützung für Direct3D10- und Direct3D10.1-Codepfade. Direct3D10Level9 ermöglicht direct3D10 die Arbeit mit Direct3D9-Hardware. Direct3D WARP10 ist ein performanter Softwarerasterizer für Direct3D10-Anwendungen. Direct3D11, die neueste Version von Direct3D, bietet neue Funktionen wie verbesserte Multithreadunterstützung, Mosaik, DirectCompute-Funktionalität und dynamische Shaderverknüpfung.

Wenn Sie Anwendungen erstellen, die Direct3D verwenden, ist das [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/aa937788.aspx) erforderlich.

Weitere Informationen zu Direct3D finden Sie unter [Direct3D](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/default.aspx) .

### <a name="supported-direct3d-api-elements"></a>Unterstützte Direct3D-API-Elemente

Alle APIs werden in früheren Versionen von Windows unterstützt, die für das Plattformupdate für Windows Vista oder das Plattformupdate für Windows Server 2008 berechtigt sind.

### <a name="directwrite"></a>DirectWrite

Die DirectWrite-API ist eine neue Text-API, die mehrere Funktionalitätsebenen bereitstellt, einschließlich Textlayout, Skriptverarbeitung, Glyphenrendering und Schriftartsystem. DirectWrite verwendet OpenType-Schriftarten und Das ClearType-Rendering im Unterpixel, um die Von Anwendungen bereitgestellte Textdarstellung zu verbessern. Textrendering wird bei Verwendung mit Direct2D hardwarebeschleunigend.

Weitere Informationen zu DirectWrite finden Sie unter [Einführung in DirectWrite](/windows/desktop/DirectWrite/introducing-directwrite).

### <a name="supported-directwrite-api-elements"></a>Unterstützte DirectWrite-API-Elemente

Alle APIs werden in früheren Versionen von Windows unterstützt, die für das Plattformupdate für Windows Vista oder das Plattformupdate für Windows Server 2008 berechtigt sind.

### <a name="running-directwrite-on-previous-windows-versions"></a>Ausführen von DirectWrite unter vorherigen Windows Versionen

Die folgenden Verhaltensprobleme können sich auf die Verwendung der DirectWrite-API in früheren Windows Versionen auswirken:

-   Skripts, die mit Windows 7 neu sind, werden in früheren Windows Versionen möglicherweise nicht vollständig ordnungsgemäß gerendert.
-   Gebietsschemas, die in früheren Windows Versionen nicht verfügbar waren, greifen auf das Standardverhalten zurück.
-   ClearType Tuner ist in früheren Windows Versionen nicht verfügbar.
-   Die GDI-Interoperabilität hat in einigen Szenarien in früheren Windows Versionen höhere Arbeitsspeicherkosten.

### <a name="packaging"></a>Verpackung

Das Plattformupdate für Windows Vista unterstützt eine begrenzte Teilmenge der Paketierungs-APIs, die zum Ausführen von Aufgaben mit der XPS-Dokument-API in nicht verwalteten Anwendungen erforderlich sind.

Weitere Informationen zu Paket-APIs finden Sie in der Übersicht über die [Paketierungs-API.](/previous-versions/windows/desktop/opc/packaging-api-overview)

### <a name="supported-packaging-api-elements"></a>Unterstützte Paketierungs-API-Elemente

Nur die folgenden Packaging-Schnittstellen werden unterstützt:

-   IOpcUri
-   IOpcPartUri
-   IOpcFactory (nur die folgenden Methoden werden unterstützt)
    -   CreatePackageRootUri
    -   CreatePartUri
    -   CreateStreamOnFile

Unterstützte Paketerstellungs-APIs können zum Erstellen von Datenströmen über Dateien sowie zum Erstellen und Interagieren mit paketbasierten URI verwendet werden.

### <a name="running-packaging-api-on-previous-windows-versions"></a>Ausführen der Paket-API in vorherigen Windows Versionen

Das Verhalten und die Leistung der unterstützten Packaging-Schnittstellen und -Methoden sind auf allen unterstützten Plattformen identisch.

Wenn eine Anwendung versucht, eine nicht unterstützte Packaging-Schnittstelle oder -Methode zu instanziieren oder aufzurufen, schlägt der Versuch fehl. Wenn der Aufruf an eine nicht unterstützte [**IOpcFactory-Methode**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcfactory) erfolgt, wird der E \_ NOTIMPL-Fehlercode zurückgegeben.

### <a name="windows-imaging-component"></a>Windows-Bilderstellungskomponente

Neue Features für die Windows Imaging Component (WIC) umfassen verbesserte Sicherheit, Unterstützung für hohe Farbe und bessere Metadateninteroperabilität. Darüber hinaus erweitert die Windows Imaging Component ihre Standards, indem sie Unterstützung für die progressive Bilddecodierung, erweiterte PNG-Features, GIF-Metadaten, HD-Fotoupdates und Metadaten bereitstellt, die APPn-Segmente umfassen.

Weitere Informationen zur Windows Imaging Component finden Sie in der [Übersicht über Windows Imaging Component](/windows/desktop/wic/-wic-about-windows-imaging-codec).

### <a name="supported-wic-api-elements"></a>Unterstützte WIC-API-Elemente

Alle APIs werden in früheren Versionen von Windows unterstützt, die für das Plattformupdate für Windows Vista oder das Plattformupdate für Windows Server 2008 berechtigt sind.

### <a name="xps-document"></a>XPS-Dokument

Die XPS-Dokument-APIs unterstützen das Erstellen, Ändern und Speichern von XPS-Dokumenten in nicht verwalteten Anwendungen.

Weitere Informationen zu XPS-Dokument-APIs finden Sie im [XPS-Dokumentprogrammierhandbuch.](/previous-versions//dd372978(v=vs.85))

### <a name="supported-xps-document-api-elements"></a>Unterstützte XPS-Dokument-API-Elemente

Nur die [XPS Digital Signatures-Schnittstellen](/previous-versions/windows/desktop/dd372947(v=vs.85)) werden in downleveln Betriebssystemversionen nicht unterstützt.

### <a name="xps-print"></a>XPS Print

Die XPS Print-APIs unterstützen das Drucken von XPS-Dokumenten aus Windows-basierten Anwendungen.

Weitere Informationen zu XPS-Druck-APIs finden Sie in der [XpsPrint-API.](/windows/desktop/printdocs/xpsprint-api)

### <a name="supported-xps-print-api-elements"></a>Unterstützte XPS-Druck-API-Elemente

Alle APIs werden in früheren Versionen von Windows unterstützt, die für das Plattformupdate für Windows Vista oder das Plattformupdate für Windows Server 2008 berechtigt sind.

### <a name="windows-ribbon-and-animation-manager-library"></a>Windows Menüband- und Animations-Manager-Bibliothek

Das Plattformupdate für Windows Vista unterstützt die folgenden Windows 7-APIs über das menüband- und Animationsbibliothek Windows:

-   [Windows Menübandframework](#windows-ribbon-and-animation-manager-library)
-   [Windows Animations-Manager](#windows-animation-manager)

### <a name="windows-editions-eligible-for-the-updates"></a>Windows Für updates berechtigte Editionen

Das Plattformupdate für Windows Vista und das Plattformupdate für Windows Server 2008 ermöglichen die Unterstützung Windows Menüband- und Animations-Manager-Bibliothek für die Editionen von Windows in der folgenden Tabelle.



<table>
<thead>
<tr class="header">
<th>Windows-Version</th>
<th>Editionen, die für Updates berechtigt sind</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows Vista</td>
<td><dl> Starter mit SP2 (x86)<br />
Home Basic mit SP2 (x86 und amd64)<br />
Home Premium mit SP2 (x86 und amd64)<br />
Business with SP2 (x86 and amd64) (Geschäft mit SP2 (x86 und amd64))<br />
Enterprise mit SP2 (x86 und amd64)<br />
Ultimate mit SP2 (x86 und amd64)<br />
</dl></td>
</tr>
<tr class="even">
<td>Windows Server 2008</td>
<td><dl> Windows Server 2008 mit SP2 (x86 und amd64)<br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="windows-ribbon-framework"></a>Windows Menübandframework

Das Windows-Menübandframework ist ein umfangreiches Befehlspräsentationssystem, das eine moderne Alternative zu den mehrschichtigen Menüs, Symbolleisten und Aufgabenbereichen herkömmlicher Windows bietet.

Das Framework ist eine Sammlung von Microsoft Win32-APIs, die eine Vielzahl neuer Benutzeroberflächenfunktionen für Windows-Entwickler bereitstellen und sowohl das Menüband als auch ein Kontextmenüsystem enthalten.

Weitere Informationen zum Menübandframework finden Sie unter [Introducing the Windows Ribbon Framework](../windowsribbon/windowsribbon-introduction.md).

### <a name="supported-ribbon-framework-api-elements"></a>Unterstützte Menübandframework-API-Elemente

Alle APIs werden in früheren Versionen von Windows unterstützt, die für das Plattformupdate für Windows Vista oder das Plattformupdate für Windows Server 2008 geeignet sind.

### <a name="windows-animation-manager"></a>Windows Animations-Manager

Der Windows Animation Manager (Windows Animation) ist eine programmgesteuerte Schnittstelle, die die Animation visueller Elemente von Windows unterstützt. Windows Animationen sollen die Entwicklung und Wartung von Animationssequenzen vereinfachen und Es Entwicklern ermöglichen, konsistente und intuitive Animationen zu implementieren. Windows Animationen können mit jeder Grafikplattform verwendet werden, einschließlich Direct2D, Direct3D oder GDI+.

Windows Animation ist eine Singlethread-COM-API, die alles bietet, was ein Entwickler zum Erstellen, Verwalten und Steuern der Benutzeroberflächenanimation benötigt.

Weitere Informationen zum Animations-Manager für Windows finden Sie unter Introducing Windows Animation ( Einführung [in Windows Animation).](/windows/desktop/UIAnimation/introducing-windows-animation-manager)

### <a name="supported-animation-manager-api-elements"></a>Unterstützte Animations-Manager-API-Elemente

Alle APIs werden in früheren Versionen von Windows unterstützt, die für das Plattformupdate für Windows Vista oder das Plattformupdate für Windows Server 2008 geeignet sind.

### <a name="windows-portable-devices-platform"></a>Windows Plattform für portable Geräte

Das Plattformupdate für Windows Vista unterstützt die Windows 7-Erweiterungen der Windows Portable Devices (WPD)-Plattform. Mit diesem Feature können Computer mit angeschlossenen Medien und Speichergeräten kommunizieren. WPD bietet eine flexible, stabile Möglichkeit für Computer, mit Digitalkameras, Musikplayern, Mobiltelefonen und vielen anderen Arten von verbundenen Geräten zu kommunizieren.

Weitere Informationen zu portablen Windows finden Sie unter Windows [Portable Devices](/windows-hardware/drivers/portable/) ( https://docs.microsoft.com/windows-hardware/drivers/portable/) .

### <a name="windows-editions-eligible-for-the-updates"></a>Windows Für die Updates geeignete Editionen

Das Plattformupdate für Windows Vista und das Plattformupdate für Windows Server 2008 ermöglichen die Unterstützung von Windows Portable Devices (WPD) für die editionen von Windows, wie in der folgenden Tabelle gezeigt.



<table>
<thead>
<tr class="header">
<th>Windows-Version</th>
<th>Für das Update geeignete Editionen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows Vista</td>
<td><dl> Starter mit SP2 (x86)<br />
Home Basic mit SP2 (x86 und amd64)<br />
Home Premium mit SP2 (x86 und amd64)<br />
Business with SP2 (x86 and amd64) (Geschäft mit SP2 (x86 und amd64))<br />
Enterprise mit SP2 (x86 und amd64)<br />
Ultimate mit SP2 (x86 und amd64)<br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="supported-wpd-api-elements"></a>Unterstützte WPD-API-Elemente

In der folgenden Tabelle sind die Features aufgeführt, die für Windows 7, Windows Vista und Windows Vista mit Plattformupdate für Windows Vista-Versionen des Windows-Betriebssystems unterstützt werden.

| WPD-Feature                    | Windows 7 | Windows Vista | Windows Vista mit Plattformupdate für Windows Vista |
|--------------------------------|-----------|---------------|------------------------------------------------------|
| MTP über USB                   | Ja       | Ja           | Ja                                                  |
| MTP über IP                    | Ja       | Ja           | Ja                                                  |
| MTP über Bluetooth             | Ja       | Nein            | Ja                                                  |
| WPD- und MTP-Gerätedienste    | Ja       | Nein            | Ja                                                  |
| WPD Automation                 | Ja       | Nein            | Nein                                                   |
| Multifunktion/Multitransport | Ja       | Nein            | Nein                                                   |
| Device Stage                   | Ja       | Nein            | Nein                                                   |
| Gerätesynchronisierungsplattform           | Ja       | Nein            | Nein                                                   |



 

Für Editionen von Windows 7 und Windows Vista, auf denen Microsoft Windows Media Player nicht standardmäßig installiert ist (die Editionen N und KN), müssen Sie das [Windows Media Format 11 SDK]( ../audio-and-video.md) ( installieren, um die WPD-Funktionalität zu https://msdn.microsoft.com/windows/bb190326.aspx) aktivieren. Weitere Informationen finden Sie im [artikel](https://support.microsoft.com/kb/953693) Knowledge Base ( ), der ursprünglich als Lösung für Windows Vista https://go.microsoft.com/fwlink/p/?linkid=158715) veröffentlicht wurde.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Plattformupdate für Windows Vista](platform-update-for-windows-vista-portal.md)
</dt> <dt>

**Übersichten**
</dt> <dt>

[Informationen zum Plattformupdate für Windows Vista](platform-update-for-windows-vista-overview.md)
</dt> <dt>

[Knowledge Base Artikel zum Plattformupdate für Windows Vista (KB-971644)](https://support.microsoft.com/kb/971644)
</dt> </dl>

 

 
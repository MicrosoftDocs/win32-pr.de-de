---
title: Informationen zum Platt Form Update für Windows Vista
description: Bietet eine Übersicht über das Platt Form Update für Windows Vista und das Platt Form Update für Windows Server 2008 und deren Features.
ms.assetid: ec5f03ae-9454-4964-943f-f97821984254
keywords:
- Platt Form Update für Windows Server 2008
- Platt Form Update für Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2bcd3e94f8784ce3d060a8e56c0b089a065d288
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "106364311"
---
# <a name="about-platform-update-for-windows-vista"></a>Informationen zum Platt Form Update für Windows Vista

Das Platt Form Update für Windows Vista und das Platt Form Update für Windows Server 2008 sind Betriebssystemupdates für Endbenutzer, die die Verwendung ausgewählter Windows 7-Technologien in früheren Versionen des Windows-Betriebssystems unterstützen. Die Updates umfassen eine Reihe von Laufzeitbibliotheken, die es Anwendungsentwicklern ermöglichen, die aktuellen Releases, Windows 7 und Windows Server 2008 R2 sowie frühere Versionen, Windows Vista und Windows Server 2008 als Ziel festzulegen.

## <a name="summary-of-supported-api-by-technology"></a>Zusammenfassung der unterstützten API nach Technologie

Jede Technologie, die vom Platt Form Update für Windows Vista und dem Platt Form Update für Windows Server 2008-Updates unterstützt wird, umfasst eine Reihe von APIs, die in einer Anwendung verwendet werden können, die auf eine frühere Version von Windows abzielt.

Weitere Informationen zur Verwendung von APIs, die von den Updates in einer Anwendung unterstützt werden, die auf frühere Versionen von Windows abzielt, finden Sie unter [entwickeln von Anwendungen für frühere Versionen von Windows](developing-applications-for-previous-versions-of-windows.md).

> [!Note]  
> Einige APIs, die einer Technologie zugeordnet sind, werden möglicherweise nicht unterstützt, und das Verhalten, die Leistung oder die Anforderungen für einige unterstützte APIs können in Windows-Versionen variieren. Ausführliche Informationen zur unterstützten API für eine bestimmte Technologie erhalten Sie, indem Sie auf den Link in einer der Zusammenfassungs Tabellen klicken, um zum Abschnitt über diese Technologie zu wechseln.

 

### <a name="technologies-supported-with-platform-update-for-windows-vista"></a>Mit dem Platt Form Update für Windows Vista unterstützte Technologien

Ausführliche Informationen zur unterstützten API für eine bestimmte Technologie erhalten Sie, indem Sie auf den Link in einer der Zusammenfassungs Tabellen klicken, um zum Abschnitt über diese Technologie zu wechseln.

In der folgenden Tabelle sind die Technologien aufgeführt, die für Windows Vista und Windows XP mit dem Platt Form Update für Windows Vista unterstützt werden.

| Technologie                                                                                    | Windows Vista | Windows XP |
|-----------------------------------------------------------------------------------------------|---------------|------------|
| [Windows Automation-API](#windows-automation-api)                                             | Ja           | Ja        |
| [Windows-Grafiken, Bildverarbeitung und XPS-Bibliothek](#windows-graphics-imaging-and-xps-library)        | Ja           | Nein         |
| [Windows-Multifunktionsleiste und Animation Manager-Bibliothek](#windows-ribbon-and-animation-manager-library) | Ja           | Nein         |
| [Plattform für tragbare Windows-Geräte](#windows-portable-devices-platform)                       | Ja           | Nein         |



 

### <a name="technologies-supported-with-platform-update-for-windows-server-2008"></a>Mit dem Platt Form Update für Windows Server 2008 unterstützte Technologien

Ausführliche Informationen zur unterstützten API für eine bestimmte Technologie erhalten Sie, indem Sie auf den Link in einer der Zusammenfassungs Tabellen klicken, um zum Abschnitt über diese Technologie zu wechseln.

Die Technologien, die für Windows Server 2008 und Windows Server 2003 mit dem Platt Form Update für Windows Server 2008 unterstützt werden, sind in der folgenden Tabelle aufgeführt.

| Technologie                                                                                    | WindowsServer 2008 | Windows Server 2003 |
|-----------------------------------------------------------------------------------------------|---------------------|---------------------|
| [Windows Automation-API](#windows-automation-api)                                             | Ja                 | Ja                 |
| [Windows-Grafiken, Bildverarbeitung und XPS-Bibliothek](#windows-graphics-imaging-and-xps-library)        | Ja                 | Nein                  |
| [Windows-Multifunktionsleiste und Animation Manager-Bibliothek](#windows-ribbon-and-animation-manager-library) | Ja                 | Nein                  |
| [Plattform für tragbare Windows-Geräte](#windows-portable-devices-platform)                       | Nein                  | Nein                  |



 

## <a name="descriptions-of-supported-api-by-technology"></a>Beschreibungen der unterstützten API nach Technologie

Ausführliche Informationen zur unterstützten API für eine bestimmte Technologie erhalten Sie, indem Sie auf den Link in einer der Zusammenfassungs Tabellen klicken, um zum Abschnitt über diese Technologie zu wechseln.

-   [Windows Automation-API](#windows-automation-api)
-   [Windows-Grafiken, Bildverarbeitung und XPS-Bibliothek](#windows-graphics-imaging-and-xps-library)
-   [Windows-Multifunktionsleiste und Animation Manager-Bibliothek](#windows-ribbon-and-animation-manager-library)
-   [Plattform für tragbare Windows-Geräte](#windows-portable-devices-platform)

### <a name="windows-automation-api"></a>Windows Automation-API

Windows Automation API 3,0 ist ein Satz von DLLs und API-Elementen, die Hilfstechnologieprodukte (at) ermöglichen, einen besseren Computer Zugriff für Einzelpersonen bereitzustellen, die physische oder kognitive Probleme, Beeinträchtigungen oder Behinderungen haben. Da Windows Automation API 3,0 außerdem Anwendungen den Zugriff auf und das Bearbeiten der Benutzeroberflächen Elemente anderer Anwendungen ermöglicht, ist es eine ideale Technologie zum Implementieren automatisierter TestTools.

Microsoft Active Accessibility (MSAA) und die Automatisierung der Benutzeroberfläche sind insofern ähnlich, als beide eine Möglichkeit zum verfügbar machen und Erfassen von Informationen zu Benutzeroberflächen Elementen und-Steuerelementen zur Unterstützung von Benutzeroberflächen-Barrierefreiheit und Softwaretest Automatisierung. Die Automatisierung der Benutzeroberfläche ist eine Windows-Implementierung der Benutzeroberflächenautomatisierungs-Spezifikation. Es handelt sich um eine neuere Technologie, die viele der Einschränkungen von MSAA behandelt.

Weitere Informationen zur Windows Automation-API 3,0 finden Sie unter [Windows Automation-API: Übersicht](/windows/desktop/WinAuto/windows-automation-api-overview).

Das Platt Form Update für Windows Vista und das Platt Form Update für Windows Server 2008 unterstützen die folgende Windows Automation-API 3,0:

-   [Microsoft Active Accessibility (MSAA)](#microsoft-active-accessibility-msaa)
-   [Benutzeroberflächenautomatisierung](#ui-automation)

### <a name="windows-editions-eligible-for-the-updates"></a>Für die Updates berechtigte Windows-Editionen

Das Platt Form Update für Windows Vista und das Platt Form Update für Windows Server 2008 ermöglichen die Unterstützung der Windows Automation-API 3,0 in den in der folgenden Tabelle aufgeführten Editionen von Windows.



<table>
<thead>
<tr class="header">
<th>Windows-Version</th>
<th>Für Update berechtigte Editionen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows Vista</td>
<td><dl> Starter mit SP2 (x86)<br />
Home Basic mit SP2 (x86 und amd64)<br />
Home Premium mit SP2 (x86 und amd64)<br />
Business mit SP2 (x86 und amd64)<br />
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
<td>Windows Server 2003</td>
<td><dl> Windows Server 2003 mit SP2 (x86 und amd64)<br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="microsoft-active-accessibility-msaa"></a>Microsoft Active Accessibility (MSAA)

Microsoft Active Accessibility (MSAA) ist eine ältere Technologie, die erstmals mit Windows 95 eingeführt wurde. Es handelt sich um einen Satz von APIs, die die Funktionsweise von Hilfstechnologieprodukten (at) mit Anwendungen unter Microsoft Windows verbessern. Die API stellt Programmierschnittstellen und Methoden zum verfügbar machen von Informationen über Benutzeroberflächen Elemente bereit.

Weitere Informationen zu Microsoft Active Accessibility finden Sie in der [technischen Übersicht](/windows/desktop/WinAuto/technical-overview).

### <a name="supported-microsoft-active-accessibility-api-elements"></a>Unterstützte Microsoft Active Accessibility-API-Elemente

Alle APIs werden in früheren Versionen von Windows unterstützt, die für das Platt Form Update für Windows Vista oder das Platt Form Update für Windows Server 2008 geeignet sind.

### <a name="ui-automation"></a>Benutzeroberflächenautomatisierung

Die Automatisierung der Benutzeroberfläche ist eine neuere Technologie, die die Benutzeroberflächenautomatisierungs-Spezifikation implementiert und viele der Einschränkungen von Microsoft Active Accessibility behandelt. Es handelt sich um einen Satz von APIs, die programmgesteuerten Zugriff auf die Benutzeroberflächen Elemente von Anwendungen bereitstellen. Die bereitgestellten API-Hilfe für Hilfstechnologieprodukte und automatisierte TestTools greifen auf die standardmäßigen und benutzerdefinierten Benutzeroberflächen Elemente einer Anwendung zu, identifizieren Sie und bearbeiten Sie.

Weitere Informationen zur Benutzeroberflächen Automatisierung finden Sie unter [Windows Automation-API: Automatisierung der Benutzeroberfläche](../winauto/entry-uiauto-win32.md).

### <a name="supported-ui-automation-api-elements"></a>Unterstützte UI Automation-API-Elemente

Alle APIs werden in früheren Versionen von Windows unterstützt, die für das Platt Form Update für Windows Vista oder das Platt Form Update für Windows Server 2008 geeignet sind.

### <a name="running-ui-automation-on-previous-windows-versions"></a>Ausführen von Benutzeroberflächen Automatisierung in früheren Windows-Versionen

Aufgrund der Unterschiede in der Implementierung der allgemeinen Steuerelemente und der Windows-Standard Steuerelemente auf verschiedenen Windows-Versionen kann es zu geringfügigen Unterschieden bei den Informationen kommen, die die Benutzeroberflächen-Automatisierungs Proxys für diese Steuerelemente von einer Version zum anderen abrufen.

### <a name="windows-graphics-imaging-and-xps-library"></a>Windows-Grafiken, Bildverarbeitung und XPS-Bibliothek

Das Platt Form Update für Windows Vista unterstützt die folgenden Windows 7-APIs aus der Windows-Grafik-,-Imaging-und XPS-Bibliothek:

-   [Direct2D](#direct2d)
-   [Direct3D](#direct3d)
-   [DirectWrite](#directwrite)
-   [Verpackung](#packaging)
-   [Windows-Bilderstellungskomponente](#windows-imaging-component)
-   [XPS-Dokument](#xps-document)
-   [XPS-Druck](#xps-print)

### <a name="windows-editions-eligible-for-the-updates"></a>Für die Updates berechtigte Windows-Editionen

Das Platt Form Update für Windows Vista und das Platt Form Update für Windows Server 2008 ermöglichen die Unterstützung von Windows-Grafiken,-Abbildern und XPS-Bibliotheken in den in der folgenden Tabelle aufgeführten Editionen von Windows.



<table>
<thead>
<tr class="header">
<th>Windows-Version</th>
<th>Für Update berechtigte Editionen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows Vista</td>
<td><dl> Starter mit SP2 (x86)<br />
Home Basic mit SP2 (x86 und amd64)<br />
Home Premium mit SP2 (x86 und amd64)<br />
Business mit SP2 (x86 und amd64)<br />
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

Bei der Direct2D-API handelt es sich um eine neue, Hardware beschleunigter 2D-Grafik-API, die leistungsstarke und qualitativ hochwertige Rendering für 2-d-Geometrie, Bitmaps und Text bereitstellt. Die Direct2D-API ist für die Zusammenarbeit mit vorhandenem Code konzipiert, der GDI, GDI+ oder Direct3D verwendet.

Weitere Informationen zu Direct2D finden Sie unter Informationen [zu Direct2D](/windows/desktop/Direct2D/direct2d-overview).

### <a name="supported-direct2d-api-elements"></a>Unterstützte Direct2D-API-Elemente

Alle APIs werden in früheren Versionen von Windows unterstützt, die für das Platt Form Update für Windows Vista oder das Platt Form Update für Windows Server 2008 geeignet sind.

### <a name="running-direct2d-on-previous-windows-versions"></a>Ausführen von Direct2D unter früheren Windows-Versionen

Wenn der WDDM 1,1-Treiber unter Windows Vista fehlt, verschlechtert sich die Leistung der Direct2D/GDI-Interoperabilität.

### <a name="direct3d"></a>Direct3D

Das Platt Form Update für Windows Vista bietet Unterstützung für die BGRA-Oberfläche für Direct3D10-und Direct3D 10.1-Code Pfade. Direct3D10Level9 ermöglicht Direct3D10-Funktionen, auf von Direct3D9-Hardware zu arbeiten. Direct3D WARP10 ist ein leistungsfähiger Software Raster für Direct3D10-Anwendungen. Direct3D11, die neueste Version von Direct3D, bietet neue Funktionen, wie z. b. verbesserte Multithreading Unterstützung, Mosaik Funktionen, DirectCompute-Funktionen und dynamische shaderverknüpfung.

Wenn Sie Anwendungen erstellen, die Direct3D verwenden, ist das [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/aa937788.aspx) erforderlich.

Weitere Informationen zu Direct3D finden Sie unter [Direct3D](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/default.aspx) .

### <a name="supported-direct3d-api-elements"></a>Unterstützte Direct3D-API-Elemente

Alle APIs werden in früheren Versionen von Windows unterstützt, die für das Platt Form Update für Windows Vista oder das Platt Form Update für Windows Server 2008 geeignet sind.

### <a name="directwrite"></a>DirectWrite

Die DirectWrite-API ist eine neue Text-API, die mehrere Funktionsebenen bereitstellt, einschließlich Text Layout, Skript Verarbeitung, Symbol Rendering und Schriftart System. DirectWrite verwendet OpenType-Schriftarten und das ClearType-unter Pixel, um die von den Anwendungen bereitgestellte Textdarstellung zu verbessern. Das Text Rendering wird bei Verwendung mit Direct2D Hardware beschleunigt.

Weitere Informationen zu DirectWrite finden Sie unter [Einführung in DirectWrite](/windows/desktop/DirectWrite/introducing-directwrite).

### <a name="supported-directwrite-api-elements"></a>Unterstützte DirectWrite-API-Elemente

Alle APIs werden in früheren Versionen von Windows unterstützt, die für das Platt Form Update für Windows Vista oder das Platt Form Update für Windows Server 2008 geeignet sind.

### <a name="running-directwrite-on-previous-windows-versions"></a>Ausführen von DirectWrite in früheren Windows-Versionen

Die folgenden Verhaltensprobleme können sich auf die Verwendung der DirectWrite-API in früheren Windows-Versionen auswirken:

-   Neue Windows 7-Skripts werden in früheren Windows-Versionen möglicherweise nicht vollständig ordnungsgemäß angezeigt.
-   Gebiets Schemas, die in früheren Windows-Versionen nicht verfügbar sind, fallen auf das Standardverhalten
-   Der ClearType-Tuner ist in früheren Windows-Versionen nicht verfügbar.
-   Die GDI-Interoperabilität hat in einigen Szenarien in früheren Windows-Versionen höhere Arbeitsspeicher Kosten.

### <a name="packaging"></a>Verpackung

Das Platt Form Update für Windows Vista unterstützt eine begrenzte Teilmenge der Paket-APIs, die zum Ausführen von Aufgaben mit der XPS-Dokument-API in nicht verwalteten Anwendungen benötigt werden.

Weitere Informationen zum Verpacken von APIs finden Sie in der [Übersicht](/previous-versions/windows/desktop/opc/packaging-api-overview)über die Paket-API.

### <a name="supported-packaging-api-elements"></a>Unterstützte Paket-API-Elemente

Es werden nur die folgenden Packungs Schnittstellen unterstützt:

-   Iopcurri
-   Iopcparamei
-   Iopcfactory (nur die folgenden Methoden werden unterstützt)
    -   "Kreatepackagerooturi"
    -   "Kreateparamei"
    -   "Kreatestreamonfile"

Unterstützte Paket-APIs können zum Erstellen von Streams über Dateien sowie zum Erstellen und interagieren mit einem Paket basierten URI verwendet werden.

### <a name="running-packaging-api-on-previous-windows-versions"></a>Ausführen der Paketierungs-API in früheren Windows-Versionen

Das Verhalten und die Leistung von unterstützten Packungs Schnittstellen und-Methoden sind auf allen unterstützten Plattformen identisch.

Wenn eine Anwendung versucht, eine nicht unterstützte Paketierungs Schnittstelle oder-Methode zu instanziieren oder aufzurufen, tritt ein Fehler auf. Wenn der-Vorgang an eine nicht unterstützte [**iopcfactory**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcfactory) -Methode erfolgt, wird der E \_ notimpl-Fehlercode zurückgegeben.

### <a name="windows-imaging-component"></a>Windows-Bilderstellungskomponente

Zu den neuen Features für die Windows Imaging Component (WIC) zählen erweiterte Sicherheit, Unterstützung für hohe Farben und eine bessere metadateninteroperabilität. Außerdem erweitert die Windows-Abbild Erstellungs Komponente die Einhaltung von Standards, indem Sie Unterstützung für progressives Decodieren von Bildern, erweiterte PNG-Features, GIF-Metadaten, HD-Foto Aktualisierungen und Metadaten bereitstellt, die sich auf APPN-Segmente

Weitere Informationen zur Windows-Abbild Erstellungs Komponente finden Sie unter Übersicht über die [Windows Imaging-Komponente](/windows/desktop/wic/-wic-about-windows-imaging-codec).

### <a name="supported-wic-api-elements"></a>Unterstützte WIC-API-Elemente

Alle APIs werden in früheren Versionen von Windows unterstützt, die für das Platt Form Update für Windows Vista oder das Platt Form Update für Windows Server 2008 geeignet sind.

### <a name="xps-document"></a>XPS-Dokument

Die XPS-Dokument-APIs unterstützen das Erstellen, ändern und Speichern von XPS-Dokumenten in nicht verwalteten Anwendungen.

Weitere Informationen zu XPS-Dokument-APIs finden Sie im [XPS-Dokument Programmier Handbuch.](/previous-versions//dd372978(v=vs.85))

### <a name="supported-xps-document-api-elements"></a>Unterstützte XPS-Dokument-API-Elemente

Nur die [XPS](/previous-versions/windows/desktop/dd372947(v=vs.85)) -Schnittstellen für digitale Signaturen werden in Betriebssystemversionen unterstützt.

### <a name="xps-print"></a>XPS-Druck

Die XPS-Druck-APIs unterstützen den Druck von XPS-Dokumenten aus Windows-basierten Anwendungen.

Weitere Informationen zu XPS-Druck-APIs finden Sie in der [XpsPrint-API](/windows/desktop/printdocs/xpsprint-api).

### <a name="supported-xps-print-api-elements"></a>Unterstützte XPS-druckenapi-Elemente

Alle APIs werden in früheren Versionen von Windows unterstützt, die für das Platt Form Update für Windows Vista oder das Platt Form Update für Windows Server 2008 geeignet sind.

### <a name="windows-ribbon-and-animation-manager-library"></a>Windows-Multifunktionsleiste und Animation Manager-Bibliothek

Das Platt Form Update für Windows Vista unterstützt die folgenden Windows 7-APIs aus dem Windows-Menüband und der Animations Bibliothek:

-   [Windows-Menü Band Framework](#windows-ribbon-and-animation-manager-library)
-   [Windows-Animations-Manager](#windows-animation-manager)

### <a name="windows-editions-eligible-for-the-updates"></a>Für die Updates berechtigte Windows-Editionen

Das Platt Form Update für Windows Vista und das Platt Form Update für Windows Server 2008 aktivieren die Unterstützung von Windows-Multifunktionsleisten-und Animations-Manager-Bibliotheken in den in der folgenden Tabelle aufgeführten Editionen von Windows.



<table>
<thead>
<tr class="header">
<th>Windows-Version</th>
<th>Für Update berechtigte Editionen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows Vista</td>
<td><dl> Starter mit SP2 (x86)<br />
Home Basic mit SP2 (x86 und amd64)<br />
Home Premium mit SP2 (x86 und amd64)<br />
Business mit SP2 (x86 und amd64)<br />
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



 

### <a name="windows-ribbon-framework"></a>Windows-Menü Band Framework

Das Windows-Menüband-Framework (Ribbon) ist ein umfassendes Befehls Präsentationssystem, das eine moderne Alternative zu den geschichteten Menüs, Symbolleisten und Aufgabenbereichen herkömmlicher Windows-Anwendungen bietet.

Das Framework ist eine Sammlung von Microsoft-Win32-APIs, die eine Reihe neuer Funktionen für die Benutzeroberfläche für Windows-Entwickler bereitstellen und sowohl das Menüband als auch ein Kontextmenü System umfasst.

Weitere Informationen zum Menüband-Framework finden Sie unter [Einführung in das Windows-Menü Band Framework](../windowsribbon/windowsribbon-introduction.md).

### <a name="supported-ribbon-framework-api-elements"></a>Unterstützte Menüband-Framework-API

Alle APIs werden in früheren Versionen von Windows unterstützt, die für das Platt Form Update für Windows Vista oder das Platt Form Update für Windows Server 2008 geeignet sind.

### <a name="windows-animation-manager"></a>Windows-Animations-Manager

Der Windows Animation Manager (Windows-Animation) ist eine programmgesteuerte Schnittstelle, die die Animation von visuellen Elementen von Windows-Anwendungen unterstützt. Die Windows-Animation dient zur Vereinfachung der Entwicklung und Wartung von Animationssequenzen und ermöglicht Entwicklern die Implementierung von Animationen, die konsistent und intuitiv sind. Windows-Animation kann mit jeder beliebigen Grafik Plattform verwendet werden, einschließlich Direct2D, Direct3D oder GDI+.

Windows-Animation ist eine Single Thread-com-API, die alles bereitstellt, was ein Entwickler zum Erstellen, verwalten und Steuern der Benutzeroberflächen Animation benötigt.

Weitere Informationen zum Windows Animation Manager finden Sie unter Einführung in die [Windows-Animation](/windows/desktop/UIAnimation/introducing-windows-animation-manager).

### <a name="supported-animation-manager-api-elements"></a>Unterstützte Animation Manager-API-Elemente

Alle APIs werden in früheren Versionen von Windows unterstützt, die für das Platt Form Update für Windows Vista oder das Platt Form Update für Windows Server 2008 geeignet sind.

### <a name="windows-portable-devices-platform"></a>Plattform für tragbare Windows-Geräte

Das Platt Form Update für Windows Vista unterstützt die Windows 7-Erweiterungen für die Windows Portable Devices (WPD)-Plattform. Diese Funktion ermöglicht Computern die Kommunikation mit angeschlossenen Medien und Speichergeräten. WPD bietet eine flexible und robuste Möglichkeit für Computer, mit digitalen Kameras, Musik Playern, Mobiltelefonen und vielen anderen Arten von verbundenen Geräten zu kommunizieren.

Weitere Informationen zu tragbaren Windows-Geräten finden Sie unter [Portable Windows-Geräte](/windows-hardware/drivers/portable/) ( https://docs.microsoft.com/windows-hardware/drivers/portable/) .

### <a name="windows-editions-eligible-for-the-updates"></a>Für die Updates berechtigte Windows-Editionen

Das Platt Form Update für Windows Vista und das Platt Form Update für Windows Server 2008 ermöglichen die Unterstützung von Windows Portable Devices (WPD) für die in der folgenden Tabelle aufgeführten Editionen von Windows.



<table>
<thead>
<tr class="header">
<th>Windows-Version</th>
<th>Für Update berechtigte Editionen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows Vista</td>
<td><dl> Starter mit SP2 (x86)<br />
Home Basic mit SP2 (x86 und amd64)<br />
Home Premium mit SP2 (x86 und amd64)<br />
Business mit SP2 (x86 und amd64)<br />
Enterprise mit SP2 (x86 und amd64)<br />
Ultimate mit SP2 (x86 und amd64)<br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="supported-wpd-api-elements"></a>Unterstützte WPD-API-Elemente

In der folgenden Tabelle sind die Funktionen aufgeführt, die für Windows 7, Windows Vista und Windows Vista mit Platt Form Update für Windows Vista-Versionen des Windows-Betriebssystems unterstützt werden.

| WPD-Funktion                    | Windows 7 | Windows Vista | Windows Vista mit Platt Form Update für Windows Vista |
|--------------------------------|-----------|---------------|------------------------------------------------------|
| MTP über USB                   | Ja       | Ja           | Ja                                                  |
| MTP über IP                    | Ja       | Ja           | Ja                                                  |
| MTP über Bluetooth             | Ja       | Nein            | Ja                                                  |
| WPD-und MTP-Geräte Dienste    | Ja       | Nein            | Ja                                                  |
| WPD-Automatisierung                 | Ja       | Nein            | Nein                                                   |
| Multifunction/Multi-Transport | Ja       | Nein            | Nein                                                   |
| Device Stage                   | Ja       | Nein            | Nein                                                   |
| Plattform für Geräte Synchronisierung           | Ja       | Nein            | Nein                                                   |



 

Bei Editionen von Windows 7 und Windows Vista, auf denen Microsoft Windows Media Player nicht standardmäßig installiert ist (die Editionen N und KN), müssen Sie das [Windows Media Format 11 SDK]( ../audio-and-video.md) installieren ( https://msdn.microsoft.com/windows/bb190326.aspx) um die WPD-Funktionalität zu aktivieren. Weitere Informationen finden Sie im [Knowledge Base-Artikel](https://support.microsoft.com/kb/953693) ( https://go.microsoft.com/fwlink/p/?linkid=158715) , der ursprünglich als Lösung für Windows Vista veröffentlicht wurde.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Platt Form Update für Windows Vista](platform-update-for-windows-vista-portal.md)
</dt> <dt>

**Übersichten**
</dt> <dt>

[Informationen zum Platt Form Update für Windows Vista](platform-update-for-windows-vista-overview.md)
</dt> <dt>

[Knowledge Base-Artikel zum Platt Form Update für Windows Vista (KB 971644)](https://support.microsoft.com/kb/971644)
</dt> </dl>

 

 
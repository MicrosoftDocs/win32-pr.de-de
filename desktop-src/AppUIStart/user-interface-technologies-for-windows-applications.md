---
title: Technologien für die Benutzeroberfläche
description: Dieses Thema enthält eine kurze Übersicht über die Microsoft-Technologien für die Entwicklung von Benutzeroberflächen für Windows-basierte Anwendungen.
ms.assetid: 5ecbaaf0-704e-4c27-b3ce-b5436e577d62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7d9343672d064cf073ea8018758b90083f440bd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103949030"
---
# <a name="user-interface-technologies"></a>Technologien für die Benutzeroberfläche

Dieses Thema enthält eine kurze Übersicht über die Microsoft-Technologien für die Entwicklung von Benutzeroberflächen für Windows-basierte Anwendungen. Sie enthält die Informationen, die erforderlich sind, um zu bestimmen, ob eine bestimmte Technologie verwendet werden soll, und gibt an, wo Sie weitere Informationen finden können.

In diesem Thema werden die folgenden Technologien beschrieben:

-   [Technologien für die Benutzeroberfläche für nicht verwaltete Anwendungen](#user-interface-technologies-for-unmanaged-applications)
    -   [Windows-Steuerelemente](#windows-controls)
    -   [Visuelle Stile](#visual-styles)
    -   [Windows-Menü Band Framework](#windows-ribbon-framework)
    -   [Windows-Animations-Manager](#windows-animation-manager)
    -   [Desktopfenster-Manager](#desktop-window-manager)
    -   [Windows Automation-API](#windows-automation-api)
    -   [Sprach-API](#speech-api)
    -   [API zur Vergrößerung](#magnification-api)
    -   [Ressourcen Compiler](#resource-compiler)
-   [Technologien für die Benutzeroberfläche für verwaltete Anwendungen](#user-interface-technologies-for-managed-applications)
    -   [Windows Forms](#windows-forms)
    -   [Windows Presentation Foundation](#windows-presentation-foundation)
    -   [Silverlight](#silverlight)
    -   [Expression Blend 3 +-Schrägung](/windows)
    -   [Benutzeroberflächen Automatisierung für verwaltete Anwendungen](#ui-automation-for-managed-applications)

## <a name="user-interface-technologies-for-unmanaged-applications"></a>Technologien für die Benutzeroberfläche für nicht verwaltete Anwendungen

In diesem Abschnitt werden die Microsoft-Technologien für die Entwicklung von Benutzeroberflächen für nicht verwaltete Windows-Anwendungen beschrieben. Diese Technologien sind für erfahrene C/C++-Entwickler gedacht, die mit WindowsAPI-Programmier Konzepten vertraut sind und das Microsoft Windows Software Development Kit (SDK) verwenden. Für einige Technologien gelten zusätzliche Voraussetzungen, wie z. b. Kenntnisse über Grafik Programmierungs Probleme oder Vertrautheit mit den Grundlagen der Component Object Model Programmierung (com).

### <a name="windows-controls"></a>Windows-Steuerelemente

Windows-Steuerelemente sind Benutzeroberflächen Elemente, die in Verbindung mit einem anderen Fenster (in der Regel ein Client Fenster oder Dialogfeld) verwendet werden, um dem Benutzer die Interaktion mit einer Anwendung zu ermöglichen. Viele Elemente, die die Benutzeroberfläche einer herkömmlichen Windows-basierten Anwendung bilden, sind Windows-Steuerelemente, einschließlich Elementen wie Menüs, Bild Lauf leisten, Schaltflächen, Listenfeldern, Struktur Ansichten usw.

Windows-Steuerelemente werden von allen Versionen von Windows unterstützt. Da sich die Laufzeitkomponenten, die die Steuerelemente unterstützen, jedoch im Laufe der Zeit weiterentwickelt haben, werden einige in höheren Versionen eingeführte Steuerelemente und Features in früheren Versionen nicht unterstützt. Anwendungen müssen die Versionen erkennen und nur die verfügbaren Features verwenden.

Sie sollten Windows-Steuerelemente verwenden, wenn Sie eine herkömmliche Benutzeroberfläche für eine nicht verwaltete, Windows-basierte Anwendung erstellen möchten, die auf einer Vielzahl von Windows-Versionen ausgeführt wird.

Weitere Informationen finden Sie unter [Windows](../controls/window-controls.md)-Steuerelemente.

### <a name="visual-styles"></a>Visuelle Stile

Visuelle Stile sind Spezifikationen für die Darstellung von-Steuerelementen. Beispielsweise kann ein visueller Stil die allgemeine Darstellung von Steuerelementen definieren und Softwareentwicklern ermöglichen, die visuelle Oberfläche dieser Steuerelemente so zu konfigurieren, dass Sie mit der Darstellung einer Anwendung koordiniert werden. Außerdem bieten visuelle Stile einen Mechanismus für alle Windows-basierten Anwendungen, um die Darstellung einer Anwendung zu standardisieren.

Visuelle Stile werden unter Windows XP und höher unterstützt und wirken sich nur auf die Darstellung der standardmäßigen Windows-Steuerelemente und der allgemeinen Microsoft Win32-Steuerelemente aus.

Sie sollten visuelle Stile verwenden, wenn Sie die Darstellung der standardmäßigen Windows-Steuerelemente und allgemeinen Steuerelemente so ändern müssen, dass Sie dem Aussehen der Benutzeroberfläche Ihrer Anwendung entsprechen.

Weitere Informationen finden Sie unter [visuelle Stile](../controls/themes-overview.md).

### <a name="windows-ribbon-framework"></a>Windows-Menü Band Framework

Das Windows-Menü Band Framework ist ein Funktions Reiches Befehls Präsentationssystem für Windows-basierte Anwendungen. Er besteht aus einer Multifunktionsleisten-Befehlsleiste, die die Hauptfunktionen einer Anwendung über eine Reihe von Registerkarten am oberen Rand eines Anwendungsfensters und ein Kontextmenü System verfügbar macht. Das Windows-Menü Band Framework wird von folgenden Windows-Versionen unterstützt:

-   Windows Vista mit Service Pack 2 (SP2) und Platt Form Update für Windows Vista
-   Windows 7 und höher
-   Windows Server 2008 R2
-   Windows Server 2008 mit Service Pack 2 (SP2) und Platt Form Update für Windows Server 2008

Sie sollten das Windows-Menü Band Framework verwenden, wenn Sie eine Befehls Benutzeroberfläche implementieren möchten, die eine Alternative zu den geschichteten Menüs, Symbolleisten und Aufgabenbereichen herkömmlicher Windows-Anwendungen darstellt.

Das Windows-Menüband-Framework ist für Entwickler gedacht, die mit der com-Programmierung vertraut sind.

Weitere Informationen finden Sie unter [Windows-Menü Band Framework](../windowsribbon/-uiplat-windowsribbon-entry.md).

### <a name="windows-animation-manager"></a>Windows-Animations-Manager

Der Windows-Animations-Manager unterstützt die Animation von UI-Elementen durch Bereitstellen einer leistungsstarken Animations-Engine und einer standardisierten programmgesteuerten Schnittstelle Die Plattform vereinfacht die Entwicklung und Wartung von UI-Animationssequenzen und ermöglicht Entwicklern die Implementierung von Konsistenz und intuitiver Benutzeroberflächen Animationen. Windows-Animation kann mit jeder beliebigen Grafik Plattform verwendet werden, einschließlich Direct2D, Microsoft Direct3D oder Windows GDI+.

Das Windows Animation Framework wird unter Windows Vista mit einem Platt Form Update für Windows VISTAWindows Vista mit SP2 und einem Platt Form Update für Windows Vista und Windows 7 und höher unterstützt.

Sie sollten Windows Animation Manager verwenden, wenn Sie der Benutzeroberfläche einer nicht verwalteten Windows-basierten Anwendung Animationssequenzen hinzufügen möchten.

Weitere Informationen finden Sie unter [Windows Animation Manager](../uianimation/-main-portal.md).

### <a name="desktop-window-manager"></a>Desktopfenster-Manager

Desktopfenster-Manager (DWM) ist eine Windows-Laufzeitkomponente, die die Desktop Komposition unterstützt, ein Feature, das in Windows Vista eingeführt wurde. Durch die Desktop Komposition ermöglicht DWM visuelle Effekte in der Benutzeroberfläche, z. b. Glasfenster Rahmen, 3D-Fenster Übergangs Animationen, Windows Flip-und Windows Flip3D-Unterstützung und Unterstützung für hohe Auflösung.

DWM macht eine API verfügbar, mit der viele der visuellen Effekte gesteuert werden, die mit der Desktop Komposition verknüpft sind. Eine Anwendung kann z. b. Miniaturansichten anzeigen, eine durchscheinend und verschwommene Auswirkung auf den Client Bereich von Fenstern der obersten Ebene anwenden, die Transparenz und die Übergangseffekte steuern, die in der nicht-Client-Windows-Region verwendet werden, usw.

DWM wird unter Windows Vista und Windows Server 2008 unterstützt.

Sie sollten DWM verwenden, wenn die Anwendung auf die visuellen Effekte der Desktop Komposition zugreifen und diese Steuern muss.

Weitere Informationen finden Sie unter [Desktopfenster-Manager](../dwm/dwm-overview.md).

### <a name="windows-automation-api"></a>Windows Automation-API

Mit der Windows-Automatisierungs-API können Entwickler Anwendungen erstellen, auf die für die größtmögliche Zielgruppe zugegriffen werden kann, einschließlich Personen mit Sehbehinderung, Hörbehinderungen oder Bewegungsbehinderungen. Die API stellt Informationen zu den Elementen bereit, die eine Anwendungs Benutzeroberfläche bilden. Hilfstechnologieanwendungen, wie z. b. Sprachausgabe, können die Benutzeroberfläche anhand der Informationen auf eine Weise darstellen, die von Menschen mit Behinderungen verwendet werden kann.

Die Windows Automation-API besteht aus zwei separaten API-Frameworks: Microsoft Active Accessibility und Microsoft UI Automation. Bei Microsoft Active Accessibility handelt es sich um eine Legacy-API, die in Windows 95 als Plattform-Add-in eingeführt wurde. Die Automatisierung der Benutzeroberfläche ist der Nachfolger von Microsoft Active Accessibility und eine Windows-Implementierung der Benutzeroberflächenautomatisierungs-Spezifikation.

Vollständige Unterstützung für Microsoft Active Accessibility ist in Windows XP und Windows Server 2003 integriert. Microsoft Active Accessibility wird auch unter Windows NT 4,0 mit Service Pack 6 (SP6) und höher und Windows 98 unterstützt. Die Automatisierung der Benutzeroberfläche wird unter den folgenden Betriebssystemen unterstützt: Windows XP, Windows Server 2003, Windows Server 2003 R2, Windows Vista, Windows 7, Windows Server 2008 und Windows Server 2008 R2.

Wenn Ihre Anwendung benutzerdefinierte Steuerelemente oder andere benutzerdefinierte Benutzeroberflächen Features enthält, sollten Sie die Windows Automation-API verwenden, um sicherzustellen, dass die benutzerdefinierten Steuerelemente und Features vollständig zugänglich sind Im Allgemeinen benötigen Entwickler ein mittleres Maß an Kenntnissen über COM-Objekte und-Schnittstellen, Unicode-und Windows-API-Programmierung.

Weitere Informationen finden Sie unter [Windows Automation-API](../winauto/windows-automation-api-portal.md).

### <a name="speech-api"></a>Sprach-API

Die Microsoft Speech API (SAPI) bietet eine allgemeine Schnittstelle zwischen einer Anwendung und Sprachmodulen. SAPI implementiert alle Low-Level-Details, die zum Steuern und Verwalten der Echt Zeit Vorgänge verschiedener Sprachmodule erforderlich sind.

Die beiden grundlegenden Arten von SAPI-Engines sind "TTS"-Systeme (Text-to-Speech) und Spracherkennung. TTS-Systeme synthetisieren Text Zeichenfolgen und-Dateien mithilfe synthetischer Stimmen in gesprochene Audiodaten. Sprach Erkennungs Tools konvertieren Menschen gesprochene Audiodaten in lesbare Text Zeichenfolgen und-Dateien.

Sie sollten SAPI verwenden, wenn Sie eine Benutzeroberfläche implementieren möchten, die es dem Benutzer ermöglicht, zusätzlich zu den Standardeingabe Geräten (z. b. Tastatur, Maus und Anzeige) mit Ihrer Anwendung zu interagieren.

Weitere Informationen finden Sie unter [Microsoft Speech API (SAPI) 5,4](/previous-versions/windows/desktop/ee125663(v=vs.85)).

### <a name="magnification-api"></a>API zur Vergrößerung

Mit der Vergrößerungs-API (MAPI) werden Teile des Bildschirms vergrößert und Farbeffekte und andere Transformationen angewendet. Diese API ist in erster Linie für Hilfstechnologieanwendungen gedacht, die Teile des Bildschirms vergrößern, damit Sie leichter zu erkennen sind.

MAPI wird unter Windows Vista, Windows 7, Windows Server 2008 und Windows Server 2008 R2 unterstützt. Es richtet sich an Entwickler, die mit den Konzepten der Grafik Programmierung vertraut sind.

Weitere Informationen finden Sie unter [Vergrößerungs-API](/previous-versions/windows/desktop/magapi/entry-magapi-sdk).

### <a name="resource-compiler"></a>Ressourcencompiler

Der Microsoft Windows-Ressourcen Compiler ist ein Anwendungs Entwicklungs Tool, das verwendet wird, um einer Windows-basierten Anwendung Benutzeroberflächen und andere Ressourcen hinzuzufügen. Eine Ressource ist eine nicht ausführbare Datei, die von einer Anwendung verwendet wird. Sie umfasst z. b. Dialogfelder, Menüs, Zeichen folgen, Cursor, Symbole, Bitmaps usw. Der Ressourcen Compiler ist in Microsoft Visual Studio und der Windows SDK enthalten.

Weitere Informationen finden Sie unter [Ressourcencompiler](../menurc/resource-compiler.md).

## <a name="user-interface-technologies-for-managed-applications"></a>Technologien für die Benutzeroberfläche für verwaltete Anwendungen

In diesem Abschnitt werden die Microsoft-Technologien für die Entwicklung von Benutzeroberflächen für verwaltete Windows-Anwendungen beschrieben, die im Kontext der .NET Framework ausgeführt werden. Weitere Informationen finden Sie unter [.net-Entwicklung](/previous-versions/ff361664(v=vs.100)).

### <a name="windows-forms"></a>Windows Forms

Windows Forms ist eine grafische Anwendungsprogrammierschnittstelle zum Erstellen von verwalteten Windows-Anwendungen, die auf dem .NET Framework basieren. In Windows Forms ist ein Formular eine visuelle Oberfläche, auf der Informationen für den Benutzer angezeigt werden und über die Sie Eingaben vom Benutzer erhalten.

Sie erstellen Windows Forms Anwendungen, indem Sie den Formularen Steuerelemente hinzufügen und Antworten auf Benutzeraktionen wie Mausklicks oder Tastatureingaben entwickeln. Ein Steuerelement ist ein diskretes Benutzeroberflächenelement, das Daten anzeigt oder Dateneingaben akzeptiert. Windows Forms enthält eine Vielzahl von Steuerelementen, die Sie Formularen hinzufügen können: Steuerelemente zur Anzeige von Textfeldern, Schaltflächen, Dropdownfeldern, Optionsfeldern und sogar Webseiten. Windows Forms unterstützt auch das Erstellen von benutzerdefinierten Steuerelementen.

Weitere Informationen finden Sie unter [Windows Forms](/previous-versions/dotnet/netframework-4.0/cc656767(v=vs.100)).

### <a name="windows-presentation-foundation"></a>Windows Presentation Foundation

Windows Presentation Foundation (WPF) ist der Nachfolger von [Windows Forms](/previous-versions/dotnet/netframework-4.0/cc656767(v=vs.100)). WPF ist ein Präsentationssystem zum entwickeln und Rendern von Benutzeroberflächen in Windows-basierten Client Anwendungen und im Browser gehosteten Anwendungen. Der Kern von WPF ist eine auflösungsunabhängige und vektorbasierte Rendering-Engine, die die Leistungsfähigkeit moderner Grafikhardware nutzt. Dieser Kern wird durch WPF um einen umfassenden Satz von Anwendungsentwicklungsfeatures erweitert, wozu Extensible Application Markup Language (XAML), Steuerelemente, Datenbindung, Layout, 2D- und 3D-Grafik, Animationen, Stile, Vorlagen, Dokumente, Medien, Text und Typographie zählen.

Da WPF in .NET Framework enthalten ist, können Sie Anwendungen erstellen, die andere Elemente der .NET Framework-Klassenbibliothek beinhalten. WPF wird unter Windows Vista, Windows 7, Windows Server 2008, Windows Server 2008 R2 unterstützt und ist auch für Windows XP mit Service Pack 2 (SP2) und Windows Server 2003 verfügbar.

Weitere Informationen finden Sie unter [Windows Presentation Foundation](/dotnet/framework/wpf/).

### <a name="silverlight"></a>Silverlight

Microsoft Silverlight ist eine leistungsstarke Entwicklungsplattform zum Erstellen von Rich-Media-Anwendungen und Geschäftsanwendungen für Web-, Desktop-und mobile Geräte.

Basierend auf dem .NET Framework funktioniert das kostenlose Silverlight-Plug-in auf mehreren Browsern, Geräten und Betriebssystemen, um neue Interaktivität im Web zu bieten. Dank umfangreicher Layout-und Formatierungsoptionen, leistungsstarken Kommunikationsprotokollen, robustem Datenzugriff und Unterstützung für Benutzerinteraktion und High-Definition-Medien können Sie mit Silverlight schnelle, reibungslose und visuell umfassende Kundenerfahrungen erzielen. Silverlight-Anwendungen können mit der Microsoft-Webplattform, Visual Studio und Expression Studio schnell entwickelt werden.

Weitere Informationen finden Sie unter [Microsoft Silverlight](/previous-versions/windows/silverlight/dotnet-windows-silverlight/cc838158(v=vs.95)).

### <a name="expression-blend-3--sketchflow"></a>Expression Blend 3 +-Schrägung

Expression Blend 3 + schrägungsflow ist ein visuelles Tool zum Entwerfen, Erstellen von Prototypen und Erstellen von ausgereiften Benutzeroberflächen für WPF-und Silverlight-Desktop-und-Webanwendungen. Sie erstellen eine Anwendung durch Zeichnen von Formen, Zeichnen von Steuerelementen wie Schaltflächen und Listenfeldern, sodass die Teile Ihrer Anwendung auf Mausklicks und andere Benutzereingaben reagieren, und formatieren alles, um Ihre eigenen zu sehen.

Weitere Informationen finden Sie unter [Prototypen mit "schrägungsflow](/previous-versions/visualstudio/design-tools/expression-studio-3/ee341458(v=expression.30))".

### <a name="ui-automation-for-managed-applications"></a>Benutzeroberflächen Automatisierung für verwaltete Anwendungen

Die Benutzeroberflächen Automatisierung ist ein Barrierefreiheits Framework für Windows, das auf allen Betriebssystemen verfügbar ist, die WPF unterstützen.

Die Benutzeroberflächen Automatisierung ermöglicht den programmgesteuerten Zugriff auf die meisten Elemente der Benutzeroberfläche auf dem Desktop, sodass Hilfstechnologieprodukte, z. b. Bildschirm Sprachausgaben, Informationen zur Benutzeroberfläche für Endbenutzer bereitstellen und die Benutzeroberfläche auf andere Weise als Standard Eingaben bearbeiten Die Benutzeroberflächen Automatisierung ermöglicht außerdem die Interaktion von automatisierten Test Skripts mit der Benutzeroberfläche.

Weitere Informationen finden Sie unter [Benutzeroberflächen Automatisierung für verwaltete Anwendungen](/dotnet/framework/ui-automation/).

 

 
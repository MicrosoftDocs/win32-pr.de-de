---
title: Benutzeroberfläche-Technologien
description: Dieses Thema enthält eine kurze Übersicht über die Microsoft-Technologien für die Entwicklung von UIs für Windows-basierte Anwendungen.
ms.assetid: 5ecbaaf0-704e-4c27-b3ce-b5436e577d62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a36bbf73d5b319e04ba2b02570c6fce4124a9ec6d54fcec201e77c4c9487dfa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702320"
---
# <a name="user-interface-technologies"></a>Benutzeroberfläche-Technologien

Dieses Thema enthält eine kurze Übersicht über die Microsoft-Technologien für die Entwicklung von UIs für Windows-basierte Anwendungen. Sie stellt die erforderlichen Informationen bereit, um zu bestimmen, ob eine bestimmte Technologie verwendet werden soll, und gibt an, wo Sie weitere Informationen dazu finden können.

In diesem Thema werden die folgenden Technologien beschrieben:

-   [Benutzeroberfläche-Technologien für nicht verwaltete Anwendungen](#user-interface-technologies-for-unmanaged-applications)
    -   [Windows Steuerelemente](#windows-controls)
    -   [Visuelle Stile](#visual-styles)
    -   [Windows Menübandframework](#windows-ribbon-framework)
    -   [Windows Animations-Manager](#windows-animation-manager)
    -   [Desktopfenster-Manager](#desktop-window-manager)
    -   [Windows Automation-API](#windows-automation-api)
    -   [Sprach-API](#speech-api)
    -   [API zur Vergrößerung](#magnification-api)
    -   [Ressourcencompiler](#resource-compiler)
-   [Benutzeroberfläche-Technologien für verwaltete Anwendungen](#user-interface-technologies-for-managed-applications)
    -   [Windows Forms](#windows-forms)
    -   [Windows Presentation Foundation](#windows-presentation-foundation)
    -   [Silverlight](#silverlight)
    -   [Ausdrucksmischung 3 + SketchFlow](/windows)
    -   [Benutzeroberflächenautomatisierung für verwaltete Anwendungen](#ui-automation-for-managed-applications)

## <a name="user-interface-technologies-for-unmanaged-applications"></a>Benutzeroberfläche-Technologien für nicht verwaltete Anwendungen

In diesem Abschnitt werden die Microsoft-Technologien zum Entwickeln von UIs für nicht verwaltete Windows Anwendungen beschrieben. Diese Technologien sind für erfahrene C/C++-Entwickler vorgesehen, die mit WindowsAPI-Programmierkonzepten vertraut sind und das Microsoft Windows Software Development Kit (SDK) verwenden. Einige Technologien verfügen über zusätzliche Voraussetzungen, z. B. Kenntnisse über Probleme bei der Grafikprogrammierung oder Vertrautheit mit den Grundlagen der com-Programmierung (Component Object Model).

### <a name="windows-controls"></a>Windows Steuerelemente

Windows-Steuerelemente sind Benutzeroberflächenelemente, die in Verbindung mit einem anderen Fenster (in der Regel ein Clientfenster oder Dialogfeld) verwendet werden, um dem Benutzer die Interaktion mit einer Anwendung zu ermöglichen. Viele der Elemente, aus denen die Benutzeroberfläche einer herkömmlichen Windows-basierten Anwendung besteht, sind Windows Steuerelemente, einschließlich Elementen wie Menüs, Bildlaufleisten, Schaltflächen, Listenfeldern, Strukturansichten usw.

Windows-Steuerelemente werden von allen Versionen von Windows unterstützt. Da sich jedoch die Laufzeitkomponenten, die die Steuerelemente unterstützen, im Laufe der Zeit weiterentwickelt haben, werden einige in späteren Versionen eingeführte Steuerelemente und Features in früheren Versionen nicht unterstützt. Anwendungen müssen die Versionen erkennen und nur die verfügbaren Features verwenden.

Sie sollten Windows-Steuerelemente verwenden, wenn Sie eine herkömmliche Benutzeroberfläche für eine nicht verwaltete Windows-basierte Anwendung erstellen möchten, die auf einer Vielzahl von Windows Versionen ausgeführt wird.

Weitere Informationen finden Sie unter [Windows Controls](../controls/window-controls.md).

### <a name="visual-styles"></a>Visuelle Stile

Visuelle Stile sind Spezifikationen für die Darstellung von Steuerelementen. Beispielsweise kann ein visueller Stil die allgemeine Darstellung von Steuerelementen definieren und Softwareentwicklern ermöglichen, die visuelle Benutzeroberfläche dieser Steuerelemente so zu konfigurieren, dass sie mit der Darstellung einer Anwendung koordiniert wird. Darüber hinaus bieten visuelle Stile einen Mechanismus für alle Windows-basierten Anwendungen, um die Darstellung einer Anwendung zu standardisieren.

Visuelle Stile werden auf Windows XP und höher unterstützt und wirken sich nur auf die Darstellung der standardmäßigen Windows-Steuerelemente und der allgemeinen Microsoft Win32-Steuerelemente aus.

Sie sollten visuelle Stile verwenden, wenn Sie die Darstellung der Standard-Windows-Steuerelemente und allgemeinen Steuerelemente so ändern müssen, dass sie dem Aussehen Ihrer Anwendungsoberfläche entsprechen.

Weitere Informationen finden Sie unter [Visuelle Stile.](../controls/themes-overview.md)

### <a name="windows-ribbon-framework"></a>Windows Menübandframework

Das Windows Menübandframework ist ein umfangreiches Befehlspräsentationssystem für Windows-basierte Anwendungen. Sie besteht aus einer Menübandbefehlsleiste, die die Hauptfunktionen einer Anwendung über eine Reihe von Registerkarten am oberen Rand eines Anwendungsfensters und ein Kontextmenüsystem verfügbar macht. Das Windows Menübandframework wird in den folgenden Windows Versionen unterstützt:

-   Windows Vista mit Service Pack 2 (SP2) und Plattformupdate für Windows Vista
-   Windows 7 und höher
-   Windows Server 2008 R2
-   Windows Server 2008 mit Service Pack 2 (SP2) und Plattformupdate für Windows Server 2008

Sie sollten Windows Menübandframework verwenden, wenn Sie eine Befehlsoberfläche implementieren möchten, die eine Alternative zu den mehrstufigen Menüs, Symbolleisten und Aufgabenbereichen herkömmlicher Windows Anwendungen ist.

Das Windows Menübandframework ist für Entwickler bestimmt, die mit COM-Programmierung vertraut sind.

Weitere Informationen finden Sie unter [Windows Menübandframework.](../windowsribbon/-uiplat-windowsribbon-entry.md)

### <a name="windows-animation-manager"></a>Windows Animations-Manager

Der Windows Animation Manager unterstützt die Animation von Benutzeroberflächenelementen, indem er eine leistungsstarke Animations-Engine und eine standardisierte programmgesteuerte Schnittstelle bereitstellt. Die Plattform vereinfacht die Entwicklung und Wartung von Benutzeroberflächenanimationssequenzen und ermöglicht Entwicklern die Implementierung konsistenter und intuitiver Benutzeroberflächenanimationen. Windows Animationen können mit jeder Grafikplattform verwendet werden, einschließlich Direct2D, Microsoft Direct3D oder Windows GDI+.

Das Windows Animationsframework wird unter Windows Vista mit Plattformupdate für Windows VistaWindows Vista mit SP2 und Plattformupdate für Windows Vista und Windows 7 und höher unterstützt.

Sie sollten Windows Animations-Manager verwenden, wenn Sie der Benutzeroberfläche einer nicht verwalteten Windows-basierten Anwendung Animationssequenzen hinzufügen möchten.

Weitere Informationen finden Sie unter [Windows Animation Manager.](../uianimation/-main-portal.md)

### <a name="desktop-window-manager"></a>Desktopfenster-Manager

Desktopfenster-Manager (DWM) ist eine Windows Laufzeitkomponente, die die Desktopkomposition unterstützt, ein in Windows Vista eingeführtes Feature. Durch die Desktopkomposition ermöglicht DWM visuelle Effekte auf der Benutzeroberfläche, z. B. Fensterrahmen, 3D-Fensterübergangsanimationen, Windows Flip und Windows Flip3D und Unterstützung für hohe Auflösung.

DWM macht eine API zum Steuern vieler visueller Effekte verfügbar, die der Desktopkomposition zugeordnet sind. Beispielsweise kann eine Anwendung Miniaturansichten anzeigen, einen durchscheinenden und unscharf wirkenden Effekt auf den Clientbereich von Fenstern der obersten Ebene anwenden, die Transparenz- und Übergangseffekte steuern, die im Nicht-Clientbereich von Fenstern verwendet werden usw.

DWM wird auf Windows Vista und Windows Server 2008 unterstützt.

Sie sollten DWM verwenden, wenn Ihre Anwendung auf die visuellen Effekte zugreifen und diese steuern muss, die der Desktopkomposition zugeordnet sind.

Weitere Informationen finden Sie unter [Desktopfenster-Manager](../dwm/dwm-overview.md).

### <a name="windows-automation-api"></a>Windows Automation-API

Die Windows Automation-API unterstützt Entwickler beim Erstellen von Anwendungen, die für eine möglichst breite Zielgruppe zugänglich sind, einschließlich Personen mit Seh-, Hör- oder Bewegungsbehinderungen. Die API stellt Informationen zu den Elementen zur Verfügung, aus denen sich eine Anwendungsbenutzeroberfläche zusammensetzen. Hilfstechnologieanwendungen wie Sprachausgaben können die Informationen verwenden, um die Benutzeroberfläche so darzustellen, dass sie von Menschen mit Behinderungen verwendet werden kann.

Die Windows Automation-API besteht aus zwei separaten API-Frameworks, Microsoft Active Accessibility und Microsoft Benutzeroberflächenautomatisierung. Microsoft Active Accessibility ist eine Legacy-API, die in Windows 95 als Plattform-Add-In eingeführt wurde. Benutzeroberflächenautomatisierung ist der Nachfolger von Microsoft Active Accessibility und eine Windows Implementierung der Benutzeroberflächenautomatisierung-Spezifikation.

Die vollständige Unterstützung für Microsoft Active Accessibility ist in Windows XP und Windows Server 2003 integriert. Microsoft Active Accessibility wird auch unter Windows NT 4.0 mit Service Pack 6 (SP6) und höher und Windows 98 unterstützt. Benutzeroberflächenautomatisierung wird unter den folgenden Betriebssystemen unterstützt: Windows XP, Windows Server 2003, Windows Server 2003 R2, Windows Vista, Windows 7, Windows Server 2008 und Windows Server 2008 R2.

Wenn Ihre Anwendung benutzerdefinierte Steuerelemente oder andere benutzerdefinierte Benutzeroberflächenfeatures enthält, sollten Sie die Windows Automation-API verwenden, um sicherzustellen, dass die benutzerdefinierten Steuerelemente und Features vollständig zugänglich sind. Im Allgemeinen benötigen Entwickler ein mittleres Maß an Kenntnissen über COM-Objekte und -Schnittstellen, Unicode- und Windows-API-Programmierung.

Weitere Informationen finden Sie unter [Windows Automation-API.](../winauto/windows-automation-api-portal.md)

### <a name="speech-api"></a>Sprach-API

Die Microsoft Speech API (SAPI) bietet eine high-level-Schnittstelle zwischen einer Anwendung und Sprach-Engines. SAPI implementiert alle Details auf niedriger Ebene, die zum Steuern und Verwalten der Echtzeitvorgänge verschiedener Sprach-Engines erforderlich sind.

Die beiden grundlegenden Typen von SAPI-Engines sind TTS-Systeme (Text-to-Speech) und Spracherkennungen. TTS-Systeme synthetisieren Textzeichenfolgen und -dateien mithilfe synthetischer Stimmen in gesprochenes Audio. Spracherkennungen konvertieren gesprochene Audioinhalte in lesbare Textzeichenfolgen und -dateien.

Sie sollten SAPI verwenden, wenn Sie eine Benutzeroberfläche implementieren möchten, die es dem Benutzer ermöglicht, mit Ihrer Anwendung über TTS und Spracherkennung zusätzlich zu den Standardeingabegeräten wie Tastatur, Maus und Anzeige zu interagieren.

Weitere Informationen finden Sie unter [Microsoft Speech API (SAPI) 5.4](/previous-versions/windows/desktop/ee125663(v=vs.85)).

### <a name="magnification-api"></a>API zur Vergrößerung

Die Vergrößerungs-API (MAPI) wird verwendet, um Teile des Bildschirms zu vergrößern und Farbeffekte und andere Transformationen anzuwenden. Diese API ist in erster Linie für Hilfstechnologieanwendungen vorgesehen, die Teile des Bildschirms vergrößern, um deren Anzeige zu erleichtern.

MAPI wird auf Windows Vista, Windows 7, Windows Server 2008 und Windows Server 2008 R2 unterstützt. Es richtet sich an Entwickler, die mit Grafikprogrammierungskonzepten vertraut sind.

Weitere Informationen finden Sie unter [Vergrößerungs-API.](/previous-versions/windows/desktop/magapi/entry-magapi-sdk)

### <a name="resource-compiler"></a>Ressourcencompiler

Der Microsoft Windows Resource Compiler ist ein Tool für die Anwendungsentwicklung, das verwendet wird, um einer Windows-basierten Anwendung Benutzeroberflächen und andere Ressourcen hinzuzufügen. Eine Ressource sind alle nicht ausführbaren Daten, die von einer Anwendung verwendet werden und z. B. Dialogfelder, Menüs, Zeichenfolgen, Cursor, Symbole, Bitmaps usw. enthalten. Der Ressourcencompiler ist in Microsoft Visual Studio und dem Windows SDK enthalten.

Weitere Informationen finden Sie unter [Ressourcencompiler](../menurc/resource-compiler.md).

## <a name="user-interface-technologies-for-managed-applications"></a>Benutzeroberfläche-Technologien für verwaltete Anwendungen

In diesem Abschnitt werden die Microsoft-Technologien zum Entwickeln von Beis für verwaltete Windows beschrieben, die im Kontext des .NET Framework. Weitere Informationen finden Sie unter [.NET-Entwicklung.](/previous-versions/ff361664(v=vs.100))

### <a name="windows-forms"></a>Windows Forms

Windows Forms ist eine grafische Anwendungsprogrammierschnittstelle zum Erstellen verwalteter Windows, die auf dem -.NET Framework. In Windows Formularen ist ein Formular eine visuelle Oberfläche, auf der Sie dem Benutzer Informationen anzeigen und über die Sie Eingaben vom Benutzer erhalten.

Sie erstellen Windows Forms-Anwendungen, indem Sie Steuerelementen zu Formularen hinzufügen und Antworten auf Benutzeraktionen wie Mausklicks oder Tastendruck entwickeln. Ein Steuerelement ist ein diskretes Benutzeroberflächenelement, das Daten anzeigt oder Dateneingaben akzeptiert. Windows Forms enthält eine Vielzahl von Steuerelementen, die Sie Formularen hinzufügen können: Steuerelemente zur Anzeige von Textfeldern, Schaltflächen, Dropdownfeldern, Optionsfeldern und sogar Webseiten. Windows Formulare unterstützen auch das Erstellen benutzerdefinierter Steuerelemente.

Weitere Informationen finden Sie unter [Windows Forms.](/previous-versions/dotnet/netframework-4.0/cc656767(v=vs.100))

### <a name="windows-presentation-foundation"></a>Windows Presentation Foundation

Windows Presentation Foundation (WPF) ist der Nachfolger von [Windows Forms.](/previous-versions/dotnet/netframework-4.0/cc656767(v=vs.100)) WPF ist ein Präsentationssystem zum Erstellen und Rendern von Benutzeroberflächen in Windows Clientanwendungen und im Browser gehosteten Anwendungen. Der Kern von WPF ist eine auflösungsunabhängige und vektorbasierte Rendering-Engine, die die Leistungsfähigkeit moderner Grafikhardware nutzt. Dieser Kern wird durch WPF um einen umfassenden Satz von Anwendungsentwicklungsfeatures erweitert, wozu Extensible Application Markup Language (XAML), Steuerelemente, Datenbindung, Layout, 2D- und 3D-Grafik, Animationen, Stile, Vorlagen, Dokumente, Medien, Text und Typographie zählen.

Da WPF in .NET Framework enthalten ist, können Sie Anwendungen erstellen, die andere Elemente der .NET Framework-Klassenbibliothek beinhalten. WPF wird unter Windows Vista, Windows 7, Windows Server 2008, Windows Server 2008 R2 und auch für Windows XP mit Service Pack 2 (SP2) und Windows Server 2003 unterstützt.

Weitere Informationen finden Sie unter [Windows Presentation Foundation](/dotnet/framework/wpf/).

### <a name="silverlight"></a>Silverlight

Microsoft Silverlight ist eine leistungsstarke Entwicklungsplattform zum Erstellen von Rich Media-Anwendungen und Geschäftsanwendungen für Web-, Desktop- und mobile Geräte.

Basierend auf der .NET Framework funktioniert das kostenlose Silverlight-Plug-In über mehrere Browser, Geräte und Betriebssysteme hinweg, um neue Interaktivität ins Web zu bringen. Mit umfangreichen Layout- und Formatierungsoptionen, leistungsstarken Kommunikationsprotokollen, stabilem Datenzugriff und Unterstützung für Benutzerinteraktion und High-Definition-Medien hilft Silverlight dabei, schnelle, reibungslose und visuell umfangreiche Kundenerfahrungen zu schaffen. Silverlight-Anwendungen können schnell mit dem Microsoft-Webplattform, Visual Studio und Expression Studio entwickelt werden.

Weitere Informationen finden Sie unter [Microsoft Silverlight](/previous-versions/windows/silverlight/dotnet-windows-silverlight/cc838158(v=vs.95)).

### <a name="expression-blend-3--sketchflow"></a>Ausdrucksblendung 3 + SketchFlow

Expression Blend 3 + SketchFlow ist ein visuelles Tool zum Entwerfen, Erstellen von Prototypen und Erstellen anspruchsvoller Benutzeroberflächen für WPF- und Silverlight-Desktop- und -Webanwendungen. Sie erstellen eine Anwendung, indem Sie Formen zeichnen, Steuerelemente wie Schaltflächen und Listenfelder zeichnen, die Teile Ihrer Anwendung auf Mausklicks und andere Benutzereingaben reagieren lassen und alles so formatieren, dass es eindeutig ihren eigenen ausschaut.

Weitere Informationen finden Sie unter [Prototyperstellung mit SketchFlow](/previous-versions/visualstudio/design-tools/expression-studio-3/ee341458(v=expression.30)).

### <a name="ui-automation-for-managed-applications"></a>Benutzeroberflächenautomatisierung für verwaltete Anwendungen

Benutzeroberflächenautomatisierung ist ein Barrierefreiheitsframework für Windows, das auf allen Betriebssystemen verfügbar ist, die WPF unterstützen.

Benutzeroberflächenautomatisierung bietet programmgesteuerten Zugriff auf die meisten Benutzeroberflächenelemente auf dem Desktop, sodass Hilfstechnologieprodukte wie Spracheingaben Endbenutzern Informationen über die Benutzeroberfläche bereitstellen und die Benutzeroberfläche mit anderen Als-Standardeingaben bearbeiten können. Benutzeroberflächenautomatisierung ermöglicht auch die Interaktion automatisierter Testskripts mit der Benutzeroberfläche.

Weitere Informationen finden Sie unter [Benutzeroberflächenautomatisierung für verwaltete Anwendungen.](/dotnet/framework/ui-automation/)

 

 
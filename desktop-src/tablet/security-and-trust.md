---
description: .NET Framework verfügt über ein Sicherheitsmodell, von dem Anwendungen je nach ihrem Ursprung verschieden behandelt werden.
ms.assetid: 37fa870a-6f38-44ae-943e-27697f6b9fba
title: Sicherheit und Vertrauensstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4e3039f8aa93c2ae563a918177462cd09a217af
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106361750"
---
# <a name="security-and-trust"></a>Sicherheit und Vertrauensstellung

.NET Framework verfügt über ein Sicherheitsmodell, von dem Anwendungen je nach ihrem Ursprung verschieden behandelt werden. Ausführbare Dateien und Assemblys aus dem Computer eines Benutzers werden im Allgemeinen mit voller Vertrauenswürdigkeit ausgeführt. dieselben ausführbaren Dateien und Assemblys, die über das Internet ausgeführt werden, werden im Allgemeinen mit teilweiser Vertrauenswürdigkeit Dadurch wird verhindert, dass bösartiger Code Informationen lesen oder ändern kann, auf die er keinen Zugriff haben sollte, wie z. b. lokale Dateien, Elemente in der Zwischenablage und andere Ressourcen. Wenn eine ausführbare Datei eine Assembly aufruft, die wiederum eine andere Assembly aufruft, die eine bestimmte Vertrauens Ebene erfordert, wird die niedrigste Vertrauens Ebene aller Komponenten in der Kette angewendet. Ein Administrator auf einem Computer kann jedoch bestimmte Berechtigungen festlegen, die die Standard Berechtigungen überschreiben.

Eine Übersicht über das Sicherheitsmodell ist in [sicheren, Light-Weight Client-Side](/archive/msdn-magazine/2002/january/dhtml-and-net-host-secure-lightweight-client-side-controls-in-microsoft-internet-explorer)-Steuerelementen angegeben, und Sie können in der Praxis Weitere Informationen zum Sicherheitsmodell in der [Code Zugriffssicherheit](/previous-versions/msp-n-p/ff648663(v=pandp.10))erhalten. Eine gute Übersicht über die Sicherheit von Bibliotheken (die besonders wichtig für [**UserControl**](/uwp/api/Windows.UI.Xaml.Controls.UserControl?view=winrt-19041) -Objekte auf einer Webseite ist) finden [Sie unter Verwenden von Bibliotheken aus teilweise vertrauenswürdigem Code](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconusinglibrariesfrompartiallytrustedcode.asp). weitere Sicherheitsinformationen zu verwalteten Steuerelementen finden Sie unter [Schreiben von sicheren verwalteten Steuerelementen](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconwritingsecuremanagedcontrols.asp%3fframe%3dtrue).

## <a name="permissions"></a>Berechtigungen

Die meisten verwalteten Objekte und Mitglieder der Tablet PC-Technologien-API haben zwei Anforderungen:

-   Die Ausführung ist immer erforderlich.
-   "FullTrust" ist erforderlich, wenn die " [vererancedemand](/previous-versions/windows/) "-Sicherheitsaktion stattfindet. Dies bedeutet, dass volle Vertrauenswürdigkeit erforderlich ist, wenn eine abgeleitete Klasse eine Klasse erbt oder eine Methode vom Tablet PC SDK überschreibt.

In der folgenden Tabelle werden die Klassen und Member aufgelistet, die zusätzliche Berechtigungen erfordern. Die Berechtigungen für eine bestimmte Klasse gelten auch für alle Member, die in dieser Tabelle nicht aufgeführt sind.



| Klasse oder Methode                                                                       | Berechtigungen                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CanPaste**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-canpaste)                                                  | [UIPermissionClipboard. AllClipboard](/dotnet/api/system.security.permissions.uipermissionclipboard?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                           |
| [**Ink. ClipboardCopy**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopy)                                    | [UIPermissionClipboard. OwnClipboard](/dotnet/api/system.security.permissions.uipermissionclipboard?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                           |
| [**Ink. ClipboardPaste**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardpaste)                                  | [UIPermissionClipboard. AllClipboard](/dotnet/api/system.security.permissions.uipermissionclipboard?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                           |
| [**InkCollector**](inkcollector-class.md)                                            | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                          |
| InkCollector (IntPtr)                                                                  | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) und [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/)<br/>         |
| InkCollector. handle                                                                   | [UIPermissionWindow. AllWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) und [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/) (siehe Hinweis unten)<br/> |
| InkEdit                                                                               | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                          |
| [InkOverlay](/previous-versions/ms552322(v=vs.100))                                   | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1)<br/>                                                                                                          |
| InkOverlay (IntPtr)                                                                    | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) und SecurityPermissionFlag. UnmanagedCode<br/>                                                                 |
| [InkOverlay. handle](/previous-versions/ms833109(v=msdn.10))                      | [UIPermissionWindow. AllWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1) und [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/) (siehe Hinweis unten)<br/> |
| [InkPicture](/previous-versions/aa514604(v=msdn.10))                                   | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1)<br/>                                                                                                          |
| ["Pendel Panel"](/previous-versions/aa514041(v=msdn.10))                             | Siehe Hinweis weiter unten.<br/>                                                                                                                                                                                     |
| [**Inkrenderer**](inkrenderer-class.md)                                              | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                          |
| [**Zeichnen**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-draw), [ **drawstroke**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-drawstroke)        | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) und [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/)<br/>         |
| Renderer. InkSpaceToPixel (IntPtr, Point), Renderer. InkSpaceToPixel (IntPtr, Point \[ \] )    | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) und [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/)<br/>         |
| Renderer. pixeluminkspace (IntPtr, Point), Renderer. pixeluminkspace (IntPtr, Point \[ \] )    | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) und [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/)<br/>         |
| [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))                                      | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1)<br/>                                                                                                          |
| DynamicRenderer (IntPtr)                                                               | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) und [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/)<br/>         |
| [**RealTimeStylus**](realtimestylus-class.md)                                        | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                          |
| RealTimeStylus (IntPtr), RealTimeStylus (IntPtr, Boolean), RealTimeStylus (IntPtr, Tablet) | [UIPermissionWindow. AllWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) und [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/)<br/>                  |



 

> [!Note]  
> Es ist in der Regel besser, ein Steuerelement anstelle eines Handles (IntPtr) für Konstruktoren zu verwenden, da Steuerelemente weniger Berechtigungen erfordern. Ebenso empfiehlt es sich, ein Grafik Objekt anstelle eines Handles für [Renderer. Draw](/previous-versions/ms828488(v=msdn.10)), [Renderer. InkSpaceToPixel](/previous-versions/ms828495(v=msdn.10)) und [Renderer. PixelToInkSpace](/previous-versions/ms828505(v=msdn.10))zu verwenden.

 

> [!Note]  
> Die Eigenschaften " [InkCollector. handle](/previous-versions/ms836504(v=msdn.10)) " und " [InkOverlay. handle](/previous-versions/ms833109(v=msdn.10)) " erfordern keine [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/) -Berechtigung, wenn das Handle für ein Windows Forms Steuerelement vorgesehen ist, dies aber für andere Fenster gilt.

 

> [!Note]  
> Für die Klasse " [](/previous-versions/ms571985(v=vs.100)) [pinputpanel](/previous-versions/aa514041(v=msdn.10)) " erfordern die folgenden Methoden und Eigenschaften " [SecurityPermissionFlag. AllFlags](/previous-versions/windows/): pinputpanel (IntPtr)", " [AttachedEditWindow](/previous-versions/ms582240(v=vs.100)) [](/previous-versions/ms567754(v=vs.100))", " [busy](/previous-versions/ms571975(v=vs.100))", " [commitpdinginput](/previous-versions/ms569650(v=vs.100))", " [CurrentPanel](/previous-versions/ms571976(v=vs.100))", " [defaultpanel](/previous-versions/ms571977(v=vs.100))", " [enabletsf](/previous-versions/ms569656(v=vs.100))", " [Facetten](/previous-versions/ms571978(v=vs.100))Tabelle [", "](/previous-versions/ms571983(v=vs.100)) [height](/previous-versions/ms571979(v=vs.100)) [", "](/previous-versions/ms571982(v=vs.100)) [HorizontalOffset](/previous-versions/ms571980(v=vs.100))", " [InputFailed](/previous-versions/ms567738(v=vs.100))" [](/previous-versions/ms571984(v=vs.100)), " [left](/previous-versions/ms571981(v=vs.100))", "Port Change [", "](/previous-versions/ms569667(v=vs.100)) [PanelChanged](/previous-versions/ms567741(v=vs.100)) [", "](/previous-versions/ms569778(v=vs.100)) [PanelMoving](/previous-versions/ms567748(v=vs.100))"

 

## <a name="other-considerations"></a>Weitere Überlegungen

Einige andere bekannte Sicherheitsüberlegungen sind:

-   Microsoft Internet Explorer 6 oder höher ist erforderlich, damit websteuer Elemente ordnungsgemäß funktionieren. Mit Internet Explorer 5,5 werden nur anfängliche verwaltete Steuerelemente geladen. zusätzliche Steuerelemente können zur Laufzeit nicht dynamisch geladen werden.
-   Wenn Sie Windows XP Service Pack 2 (SP2) und CLR 1.0 verwenden, müssen Sie für websteuer Elemente in Internet Explorer die Website als vertrauenswürdige Website hinzufügen, auch wenn Sie sich in der Intranetzone befinden. Wenn Sie dies tun, werden Sie jedoch nicht mehr in der Zone vertrauenswürdiger Sites ausgeführt, obwohl Sie in der Intranetzone ausgeführt werden. Dieses Problem ist mit CLR 1.1 behoben.

 

 
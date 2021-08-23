---
description: .NET Framework verfügt über ein Sicherheitsmodell, von dem Anwendungen je nach ihrem Ursprung verschieden behandelt werden.
ms.assetid: 37fa870a-6f38-44ae-943e-27697f6b9fba
title: Sicherheit und Vertrauensstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99806fa3256dfd08d8f4a14c70620c767331fb3cb95b83a7ecd6940b04c155cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708200"
---
# <a name="security-and-trust"></a>Sicherheit und Vertrauensstellung

.NET Framework verfügt über ein Sicherheitsmodell, von dem Anwendungen je nach ihrem Ursprung verschieden behandelt werden. Ausführbare Dateien und Assemblys, die vom Computer eines Benutzers stammen, werden in der Regel mit voller Vertrauenswürdigkeit ausgeführt. die gleichen ausführbaren Dateien und Assemblys, die über das Internet ausgeführt werden, werden in der Regel mit teilweiser Vertrauenswürdigkeit ausgeführt. Dadurch soll verhindert werden, dass schädlicher Code Informationen liest oder ändert, auf die er keinen Zugriff haben sollte, z. B. lokale Dateien, Elemente in der Zwischenablage und andere Ressourcen. Wenn eine ausführbare Datei eine Assembly aufruft, die wiederum eine andere Assembly aufruft, die eine bestimmte Vertrauensebene erfordert, wird die niedrigste Vertrauensebene aller Komponenten in der Kette angewendet. Ein Administrator auf einem Computer kann jedoch bestimmte Berechtigungen festlegen, die die Standardberechtigungen überschreiben.

Eine Übersicht über das Sicherheitsmodell finden Sie unter [Secure, Light-Weight Client-Side Controls](/archive/msdn-magazine/2002/january/dhtml-and-net-host-secure-lightweight-client-side-controls-in-microsoft-internet-explorer). Ausführlichere Informationen zum Sicherheitsmodell finden Sie unter [Codezugriffssicherheit in](/previous-versions/msp-n-p/ff648663(v=pandp.10))der Praxis. Eine gute Übersicht über die Sicherheit von Bibliotheken (die insbesondere für [**UserControl-Objekte**](/uwp/api/Windows.UI.Xaml.Controls.UserControl?view=winrt-19041) auf einer Webseite wichtig ist) finden Sie unter [Verwenden von Bibliotheken aus teilweise vertrauenswürdigen Code.](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconusinglibrariesfrompartiallytrustedcode.asp)Weitere Sicherheitsinformationen zu verwalteten Steuerelementen finden Sie unter Schreiben sicherer [verwalteter Steuerelemente.](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconwritingsecuremanagedcontrols.asp%3fframe%3dtrue)

## <a name="permissions"></a>Berechtigungen

Die meisten verwalteten Objekte und Member in der Api für Tablet PC-Technologien haben zwei Anforderungen:

-   Die Ausführung ist immer erforderlich.
-   FullTrust ist erforderlich, wenn die [Vererbungsdemand-Sicherheitsaktion](/previous-versions/windows/) durchgeführt wird. Dies bedeutet, dass volle Vertrauenswürdigkeit erforderlich ist, wenn eine abgeleitete Klasse eine Klasse erbt oder eine Methode vom Tablet PC SDK überschreibt.

In der folgenden Tabelle sind die Klassen und Member aufgeführt, die zusätzliche Berechtigungen erfordern. Die Berechtigungen für eine bestimmte Klasse gelten auch für alle Member, die in dieser Tabelle nicht aufgeführt sind.



| Klasse oder Methode                                                                       | Berechtigungen                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Canpaste**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-canpaste)                                                  | [UIPermissionClipboard.AllClipboard](/dotnet/api/system.security.permissions.uipermissionclipboard?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                           |
| [**Ink.ClipboardCopy**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopy)                                    | [UIPermissionClipboard.OwnClipboard](/dotnet/api/system.security.permissions.uipermissionclipboard?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                           |
| [**Ink.ClipboardPaste**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardpaste)                                  | [UIPermissionClipboard.AllClipboard](/dotnet/api/system.security.permissions.uipermissionclipboard?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                           |
| [**Inkcollector**](inkcollector-class.md)                                            | [UIPermissionWindow.SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                          |
| InkCollector(IntPtr)                                                                  | [UIPermissionWindow.SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) und [SecurityPermissionFlag.UnmanagedCode](/previous-versions/windows/)<br/>         |
| InkCollector.Handle                                                                   | [UIPermissionWindow.AllWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) und [SecurityPermissionFlag.UnmanagedCode](/previous-versions/windows/) (siehe Hinweis unten)<br/> |
| Inkedit                                                                               | [UIPermissionWindow.SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                          |
| [Inkoverlay](/previous-versions/ms552322(v=vs.100))                                   | [UIPermissionWindow.SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1)<br/>                                                                                                          |
| InkOverlay(IntPtr)                                                                    | [UIPermissionWindow.SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) und SecurityPermissionFlag.UnmanagedCode<br/>                                                                 |
| [InkOverlay.Handle](/previous-versions/ms833109(v=msdn.10))                      | [UIPermissionWindow.AllWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1) und [SecurityPermissionFlag.UnmanagedCode](/previous-versions/windows/) (siehe Hinweis unten)<br/> |
| [Inkpicture](/previous-versions/aa514604(v=msdn.10))                                   | [UIPermissionWindow.SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1)<br/>                                                                                                          |
| [Peninputpanel](/previous-versions/aa514041(v=msdn.10))                             | Siehe Hinweis weiter unten.<br/>                                                                                                                                                                                     |
| [**InkRenderer**](inkrenderer-class.md)                                              | [UIPermissionWindow.SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                          |
| [**Draw**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-draw), [ **DrawStroke**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-drawstroke)        | [UIPermissionWindow.SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) und [SecurityPermissionFlag.UnmanagedCode](/previous-versions/windows/)<br/>         |
| Renderer.InkSpaceToPixel(IntPtr,Point), Renderer.InkSpaceToPixel(IntPtr,Point \[ \] )    | [UIPermissionWindow.SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) und [SecurityPermissionFlag.UnmanagedCode](/previous-versions/windows/)<br/>         |
| Renderer.PixelToInkSpace(IntPtr,Point), Renderer.PixelToInkSpace(IntPtr,Point \[ \] )    | [UIPermissionWindow.SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) und [SecurityPermissionFlag.UnmanagedCode](/previous-versions/windows/)<br/>         |
| [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))                                      | [UIPermissionWindow.SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1)<br/>                                                                                                          |
| DynamicRenderer(IntPtr)                                                               | [UIPermissionWindow.SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) und [SecurityPermissionFlag.UnmanagedCode](/previous-versions/windows/)<br/>         |
| [**Realtimestylus**](realtimestylus-class.md)                                        | [UIPermissionWindow.SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                          |
| RealTimeStylus(IntPtr), RealTimeStylus(IntPtr,Boolean), RealTimeStylus(IntPtr,Tablet) | [UIPermissionWindow.AllWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) und [SecurityPermissionFlag.UnmanagedCode](/previous-versions/windows/)<br/>                  |



 

> [!Note]  
> Es ist im Allgemeinen vorzuziehen, ein Steuerelement anstelle eines Handles (IntPtr) für Konstruktoren zu verwenden, da Steuerelemente weniger Berechtigungen erfordern. Ebenso ist es besser, ein Graphics-Objekt anstelle eines Handles für [Renderer.Draw](/previous-versions/ms828488(v=msdn.10)), [Renderer.InkSpaceToPixel](/previous-versions/ms828495(v=msdn.10)) und [Renderer.PixelToInkSpace zu](/previous-versions/ms828505(v=msdn.10))verwenden.

 

> [!Note]  
> Die Eigenschaften [InkCollector.Handle](/previous-versions/ms836504(v=msdn.10)) und [InkOverlay.Handle](/previous-versions/ms833109(v=msdn.10)) erfordern keine [SecurityPermissionFlag.UnmanagedCode-Berechtigung,](/previous-versions/windows/) wenn das Handle für ein Windows Forms-Steuerelement, aber für andere Fenster vorgesehen ist.

 

> [!Note]  
> Für die [PenInputPanel-Klasse](/previous-versions/aa514041(v=msdn.10)) erfordern die folgenden Methoden und Eigenschaften [SecurityPermissionFlag.AllFlags:](/previous-versions/windows/)PenInputPanel(IntPtr), [AttachedEditWindow](/previous-versions/ms582240(v=vs.100)), [Busy](/previous-versions/ms571975(v=vs.100)), [CommitPendingInput](/previous-versions/ms569650(v=vs.100)), [CurrentPanel](/previous-versions/ms571976(v=vs.100)), [DefaultPanel](/previous-versions/ms571977(v=vs.100)), [EnableTsf](/previous-versions/ms569656(v=vs.100)), [Factoid](/previous-versions/ms571978(v=vs.100)), [Height](/previous-versions/ms571979(v=vs.100)), [HorizontalOffset](/previous-versions/ms571980(v=vs.100)), [InputFailed](/previous-versions/ms567738(v=vs.100)), [Left](/previous-versions/ms571981(v=vs.100)), [MoveTo](/previous-versions/ms569667(v=vs.100)), [PanelChanged](/previous-versions/ms567741(v=vs.100)), [PanelMoving](/previous-versions/ms567748(v=vs.100)), [Refresh](/previous-versions/ms569778(v=vs.100)), [Top](/previous-versions/ms571982(v=vs.100)), [VerticalOffset](/previous-versions/ms571983(v=vs.100)), [Visible](/previous-versions/ms571984(v=vs.100)), [VisibleChanged](/previous-versions/ms567754(v=vs.100))und [Width](/previous-versions/ms571985(v=vs.100)).

 

## <a name="other-considerations"></a>Weitere Überlegungen

Einige andere bekannte Sicherheitsüberlegungen sind:

-   Microsoft Internet Explorer 6 oder höher ist erforderlich, damit Websteuerelemente ordnungsgemäß funktionieren. Mit Internet Explorer 5.5 werden nur anfänglich verwaltete Steuerelemente geladen. Sie können zur Laufzeit keine zusätzlichen Steuerelemente dynamisch laden.
-   Wenn Sie Windows XP Service Pack 2 (SP2) und CLR1.0 verwenden, müssen Websteuerelemente in Internet Explorer die Website als vertrauenswürdige Website hinzufügen, auch wenn sie sich in der Intranetzone befinden. Wenn Sie dies tun, werden sie jedoch nicht mehr in der Zone "Vertrauenswürdige Website" ausgeführt, obwohl sie in der Intranetzone ausgeführt werden. Dieses Problem wurde mit CLR1.1 behoben.

 

 
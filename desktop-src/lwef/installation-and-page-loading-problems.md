---
title: Probleme beim Installieren und Laden von Seiten
description: Probleme beim Installieren und Laden von Seiten
ms.assetid: 1611c3f1-0411-4631-a64c-e7637fc7edd9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c9775e6a9afa957867d5279b9faaf506e32757f
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2020
ms.locfileid: "106339468"
---
# <a name="installation-and-page-loading-problems"></a>Probleme beim Installieren und Laden von Seiten

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

### <a name="when-i-attempt-to-install-microsoft-agent-on-microsoft-windows-nt-i-get-a-message-indicating-that-i-need-to-be-an-administrator"></a>Wenn ich versuche, den Microsoft-Agent unter Microsoft Windows NT zu installieren, erhalte ich eine Meldung, die besagt, dass ich Administrator sein muss.

Da der Microsoft-Agent beim Installieren von Dateien in das System Verzeichnis schreibt, müssen Sie über Administrator Berechtigungen (Nichtbenutzer) verfügen, um installiert werden zu können.

### <a name="when-i-attempt-to-install-microsoft-agent-i-get-one-of-the-following-errors-process-regsvr32-s-windowsmsagentagentctldll-error-while-creating-this-file-cannot-find-this-file-note-the-directory-location-cited-in-the-error-message-varies-depending-on-how-you-installed-windows-a-required-dll-msvcrtdll-was-not-found-error-creating-process-cwindowsmsagentagentsvrexe-regserver-reason-one-of-the-library-files-needed-to-run-this-application-cannot-be-found-note-the-directory-location-cited-in-the-error-message-varies-depending-on-how-you-installed-windows"></a>Wenn ich versuche, den Microsoft-Agent zu installieren, erhalte ich einen der folgenden Fehler: Process (regsvr32/s Windows \\ MSAgent \\AgentCtl.dll). Fehler beim Erstellen dieser Datei. Diese Datei wurde nicht gefunden. (Hinweis: der Verzeichnis Speicherort, der in der Fehlermeldung aufgeführt ist, hängt davon ab, wie Sie Windows installiert haben.) Eine erforderliche dll-MSVCRT.DLL wurde nicht gefunden. Fehler beim Erstellen des Prozesses <c: \\ Windows \\ MSAgent \\agentsvr.exe/RegServer>. Ursache: eine der Bibliotheksdateien, die zum Ausführen dieser Anwendung benötigt werden, wurde nicht gefunden. (Hinweis: der Verzeichnis Speicherort, der in der Fehlermeldung aufgeführt ist, hängt davon ab, wie Sie Windows installiert haben.)

Die Installation des Microsoft-Agents erfordert die ordnungsgemäße Installation von Regsvr32.exe, Msvcrt.dll (die Microsoft C-Lauf Zeit Bibliothek) und aktuelle OLE-DLLs. Weitere Informationen finden Sie unter DCOM Update: ( <https://docs.microsoft.com/openspecs/windows_protocols/ms-dcom/4a893f3d-bd29-48cd-9f43-d9777a4415b0> ). Die beste Möglichkeit, um sicherzustellen, dass alle richtigen Systemdateien vorhanden sind, ist die Installation von [Microsoft Internet Explorer 4,0](https://www.microsoft.com/ie/download) oder höher.

### <a name="when-i-attempt-to-load-a-page-scripted-for-microsoft-agent-i-get-a-scripting-error-vbscript-runtime-error-object-required"></a>Wenn ich versuche, eine Seite mit Skripts für den Microsoft-Agent zu laden, erhalte ich einen Skript Fehler: "VBScript-Laufzeitfehler, Objekt erforderlich".

Eine der folgenden Bedingungen kann dazu führen, dass die Meldung angezeigt wird:

-   Die Sicherheitsoptionen für Microsoft Internet Explorer müssen festgelegt werden, um ActiveX-Steuerelemente und Plug-ins zu aktivieren. Überprüfen Sie die Sicherheitsseite Ihres Browsers. Öffnen Sie in Microsoft Internet Explorer das Menü Ansicht, wählen Sie Optionen aus, klicken Sie auf die Registerkarte Sicherheit, und stellen Sie sicher, dass das Kontrollkästchen ActiveX-Steuerelemente aktivieren und Plug-Ins aktiviert ist.
-   Sie werden auf einem Dual-Boot-Windows 9X-oder Windows NT-System ausgeführt, und Sie haben den Microsoft-Agent auf einem Betriebssystem installiert, versuchen jedoch, vom anderen Betriebssystem auf die Seite zuzugreifen. Obwohl die Betriebssysteme Verzeichnisse und Dateien freigeben können, werden die vom Microsoft-Agent verwendeten Registrierungsinformationen nicht freigegeben. Daher müssen Sie den Microsoft-Agent auf dem Betriebssystem installieren, das Sie für den Zugriff auf Webseiten mit dem Zeichen verwenden.

### <a name="when-i-attempt-to-load-a-page-scripted-for-microsoft-agent-nothing-happens"></a>Wenn ich versuche, eine Seite mit skriskripten für den Microsoft-Agent zu laden, passiert nichts.

Dies kann vorkommen, wenn eine der folgenden Bedingungen zutrifft:

-   Überprüfen Sie die Sicherheitsoptionen Ihres Browsers. Der Browser muss festgelegt sein, um das Laden von ActiveX-Skripts und das Abspielen von ActiveX-Steuerelementen zu ermöglichen
-   Wenn Sie auf Seiten zugreifen, die mit dem Microsoft-Agent erstellt wurden, und Microsoft Internet Explorer verwenden, müssen Sie Version 3,02 oder höher verwenden (Laden Sie die neueste Version von Internet Explorer herunter [https://www.microsoft.com/windows/ie/](https://www.microsoft.com/windows/internet-explorer/default.aspx) <https://www.microsoft.com/windows/ie/> ). Öffnen Sie in Microsoft Internet Explorer das Menü Ansicht, wählen Sie Optionen aus, klicken Sie auf die Registerkarte Sicherheit, und aktivieren Sie alle aktiven Inhalts Kontrollkästchen.
-   Dieser Fehler kann auch von einem Java-Applet auf der Seite verursacht werden. Um den Microsoft-Agent auf derselben Seite wie ein Java-Applet auszuführen, benötigen Sie Version 2,0 des virtuellen Microsoft-Computers (VM). Weitere Informationen finden Sie in den [FAQ zu Programmierung und Skript](programming-scripting-faq.md)Erstellung.

### <a name="when-i-attempt-to-load-a-page-scripted-for-microsoft-agent-i-get-the-message-unable-to-initialize-microsoft-agent"></a>Wenn ich versuche, eine Seite für den Microsoft-Agent zu laden, erhalte ich die Meldung "der Microsoft-Agent kann nicht initialisiert werden."

Dies tritt normalerweise auf, wenn Sie nicht über den Microsoft-Agent oder ein anderes Steuerelement verfügen, das auf der Seite installiert ist, und Nein auswählen, wenn Sie aufgefordert werden, das Steuerelement Versuchen Sie, die Seite zu aktualisieren, obwohl die Seite möglicherweise nur funktioniert, wenn Sie alle erforderlichen Komponenten installieren.

### <a name="when-i-attempt-to-load-a-page-scripted-for-microsoft-agent-i-get-the-message-the-component-has-been-digitally-signed-by-its-publisher-but-the-signature-does-not-match-the-component-it-is-possible-that-this-component-has-been-damaged-or-tampered-with-do-you-want-to-continue"></a>Wenn ich versuche, eine Seite mit Skripterstellung für den Microsoft-Agent zu laden, erhalte ich die Meldung "die Komponente wurde vom Verleger Digital" signiert ", aber die Signatur stimmt nicht mit der Komponente. Es ist möglich, dass diese Komponente beschädigt oder manipuliert wurde? Möchten Sie den Vorgang fortsetzen?“

Dies wird möglicherweise angezeigt, wenn Sie versuchen, den Microsoft-Agent unter Microsoft Internet Explorer 3,02 zu installieren. Sie können entweder mit der Installation fortfahren oder Ihren Browser auf Internet Explorer 4,0 oder höher aktualisieren.

### <a name="when-i-attempt-to-load-a-page-scripted-for-microsoft-agent-using-netscape-navigator-or-other-internet-browsers-i-get-errors"></a>Wenn ich versuche, eine Seite mit dem Netscape Navigator (oder anderen Internet Browsern) für den Microsoft-Agent zu laden, erhalte ich Fehler.

Der Microsoft-Agent wird mit ActiveX-Schnittstellen implementiert. Sie können Sie nur mit einem Browser (z. b. Microsoft Internet Explorer) verwenden, der die Einbettung von ActiveX-Objekten über ein Skript auf einer Seite und nur auf Systemen unterstützt, auf denen Microsoft Windows 95, Windows 98 und Windows NT 4,0 (oder höher) ausgeführt wird. Wenn Sie Microsoft Internet Explorer () nicht verwenden [https://www.microsoft.com/windows/ie/](https://www.microsoft.com/windows/internet-explorer/default.aspx) , wenden Sie sich an Ihren Browserhersteller, um weitere Informationen zur ActiveX-Unterstützung zu erhalten.

 

 





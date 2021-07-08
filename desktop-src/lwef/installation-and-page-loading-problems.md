---
title: Installations- und Seitenladeprobleme
description: Installations- und Seitenladeprobleme
ms.assetid: 1611c3f1-0411-4631-a64c-e7637fc7edd9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3139a9224f88f49a31b1f71a981d1b49b3e42127
ms.sourcegitcommit: ecd0ba4732f5264aab9baa2839c11f7fea36318f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/07/2021
ms.locfileid: "113481945"
---
# <a name="installation-and-page-loading-problems"></a>Installations- und Seitenladeprobleme

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

### <a name="when-i-attempt-to-install-microsoft-agent-on-microsoft-windows-nt-i-get-a-message-indicating-that-i-need-to-be-an-administrator"></a>Wenn ich versuche, den Microsoft-Agent auf Microsoft Windows NT zu installieren, erhalte ich eine Meldung, die angibt, dass ich Administrator sein muss.

Da Der Microsoft-Agent bei der Installation Dateien in Ihr Systemverzeichnis schreibt, müssen Sie über Administratorrechte (nicht über Benutzerberechtigungen) für die Installation verfügen.

### <a name="when-i-attempt-to-install-microsoft-agent-i-get-one-of-the-following-errors-process-regsvr32-s-windowsmsagentagentctldll-error-while-creating-this-file-cannot-find-this-file-note-the-directory-location-cited-in-the-error-message-varies-depending-on-how-you-installed-windows-a-required-dll-msvcrtdll-was-not-found-error-creating-process-cwindowsmsagentagentsvrexe-regserver-reason-one-of-the-library-files-needed-to-run-this-application-cannot-be-found-note-the-directory-location-cited-in-the-error-message-varies-depending-on-how-you-installed-windows"></a>Wenn ich versuche, den Microsoft-Agent zu installieren, erhalte ich einen der folgenden Fehler: Process (Regsvr32 /s windows \\ msagent \\AgentCtl.dll). Fehler beim Erstellen dieser Datei. Diese Datei wurde nicht gefunden. (Hinweis: Der in der Fehlermeldung genannte Verzeichnisspeicherort variiert je nachdem, wie Sie Windows installiert haben.) Eine erforderliche DLL-MSVCRT.DLL wurde nicht gefunden. Fehler beim Erstellen des Prozesses <c: \\ windows \\ msagent \\agentsvr.exe /regserver>. Ursache: Eine der Bibliotheksdateien, die zum Ausführen dieser Anwendung erforderlich sind, wurde nicht gefunden. (Hinweis: Der in der Fehlermeldung genannte Verzeichnisspeicherort variiert je nachdem, wie Sie Windows installiert haben.)

Die Installation des Microsoft-Agents erfordert die ordnungsgemäße Installation von Regsvr32.exe, Msvcrt.dll (der Microsoft C-Laufzeitbibliothek) und aktuellen OLE-DLLs. Siehe DCOM-Update: ( <https://docs.microsoft.com/openspecs/windows_protocols/ms-dcom/4a893f3d-bd29-48cd-9f43-d9777a4415b0> ). Die beste Möglichkeit, sicherzustellen, dass alle richtigen Systemdateien vorhanden sind, ist die Installation [von Microsoft Internet Explorer 4.0](https://www.microsoft.com/ie/download) oder höher.

### <a name="when-i-attempt-to-load-a-page-scripted-for-microsoft-agent-i-get-a-scripting-error-vbscript-runtime-error-object-required"></a>Wenn ich versuche, eine Seite zu laden, für die ein Skript für den Microsoft-Agent erstellt wurde, erhalte ich einen Skriptfehler: "VBScript-Laufzeitfehler, Objekt erforderlich".

Eine der folgenden Bedingungen kann dazu führen, dass die Meldung angezeigt wird:

-   Ihre Sicherheitsoptionen für Microsoft Internet Explorer müssen festgelegt werden, um ActiveX Steuerelemente und Plug-Ins zu aktivieren. Überprüfen Sie die Sicherheitsseite Ihres Browsers. Öffnen Sie in Microsoft Internet Explorer das Menü Ansicht, wählen Sie Optionen aus, klicken Sie auf die Registerkarte "Sicherheit", und stellen Sie sicher, dass das Kontrollkästchen ActiveX Steuerelemente aktivieren und Plug-Ins aktiviert ist.
-   Sie werden auf einem Dual-Boot-Windows 9x- oder Windows NT-System ausgeführt, und Sie haben Den Microsoft-Agent auf einem Betriebssystem installiert, versuchen jedoch, über das andere Betriebssystem auf die Seite zuzugreifen. Obwohl die Betriebssysteme Verzeichnisse und Dateien gemeinsam nutzen können, werden die vom Microsoft-Agent verwendeten Registrierungsinformationen nicht freigegeben. Daher müssen Sie den Microsoft-Agent auf dem Betriebssystem installieren, das Sie für den Zugriff auf Webseiten verwenden, für die ein Skript mit dem Zeichen erstellt wurde.

### <a name="when-i-attempt-to-load-a-page-scripted-for-microsoft-agent-nothing-happens"></a>Wenn ich versuche, eine Seite zu laden, für die ein Skript für den Microsoft-Agent erstellt wurde, geschieht nichts.

Dies kann auftreten, wenn eine der folgenden Bedingungen vorliegt:

-   Überprüfen Sie die Sicherheitsoptionen Ihres Browsers. Ihr Browser muss so festgelegt werden, dass ActiveX Skripts geladen und ActiveX-Steuerelemente wiedergegeben werden können.
-   Wenn Sie mit dem Microsoft-Agent auf Seiten zugreifen und Microsoft Internet Explorer verwenden, benötigen Sie Version 3.02 oder höher (laden Sie die neueste Version von Internet Explorer unter [https://www.microsoft.com/windows/ie/](https://www.microsoft.com/windows/internet-explorer/default.aspx) <https://www.microsoft.com/windows/ie/> herunter). Öffnen Sie in Microsoft Internet Explorer das Menü Ansicht, wählen Sie Optionen aus, klicken Sie auf die Registerkarte "Sicherheit", und aktivieren Sie alle Kontrollkästchen Aktiver Inhalt.
-   Ein Java-Applet auf der Seite kann auch diesen Fehler verursachen. Zum Ausführen des Microsoft-Agents auf derselben Seite wie ein Java-Applet ist Version 2.0 des virtuellen Microsoft-Computers (VM) erforderlich. Weitere Informationen finden Sie in den häufig gestellten Fragen zur [Programmierung/Skripterstellung.](programming-scripting-faq.yml)

### <a name="when-i-attempt-to-load-a-page-scripted-for-microsoft-agent-i-get-the-message-unable-to-initialize-microsoft-agent"></a>Wenn ich versuche, eine Seite zu laden, für die ein Skript für den Microsoft-Agent erstellt wurde, erhalte ich die Meldung "Microsoft-Agent kann nicht initialisiert werden."

Dies tritt in der Regel auf, wenn Sie keinen Microsoft-Agent oder ein anderes Steuerelement installiert haben, das von der Seite verwendet wird, und Nein auswählen, wenn Sie aufgefordert werden, das Steuerelement zu installieren. Versuchen Sie, die Seite zu aktualisieren, obwohl die Seite möglicherweise nur funktioniert, wenn Sie alle benötigten Komponenten installieren.

### <a name="when-i-attempt-to-load-a-page-scripted-for-microsoft-agent-i-get-the-message-the-component-has-been-digitally-signed-by-its-publisher-but-the-signature-does-not-match-the-component-it-is-possible-that-this-component-has-been-damaged-or-tampered-with-do-you-want-to-continue"></a>Wenn ich versuche, eine Seite zu laden, für die ein Skript für den Microsoft-Agent erstellt wurde, erhalte ich die Meldung "Die Komponente wurde vom Herausgeber digital "signiert", aber die Signatur stimmt nicht mit der Komponente überein. Ist es möglich, dass diese Komponente beschädigt oder manipuliert wurde? Möchten Sie den Vorgang fortsetzen?“

Dies kann angezeigt werden, wenn Sie versuchen, den Microsoft-Agent auf Microsoft Internet Explorer 3.02 zu installieren. Sie können entweder mit der Installation fortfahren oder Ihren Browser auf Internet Explorer 4.0 oder höher aktualisieren.

### <a name="when-i-attempt-to-load-a-page-scripted-for-microsoft-agent-using-netscape-navigator-or-other-internet-browsers-i-get-errors"></a>Wenn ich versuche, eine Seite zu laden, für die ein Skript für den Microsoft-Agent mit Netscape Navigator (oder anderen Internetbrowsern) erstellt wurde, erhalte ich Fehler.

Der Microsoft-Agent wird mithilfe ActiveX Schnittstellen implementiert. Sie können es nur mit einem Browser (z. B. Microsoft Internet Explorer) verwenden, der das Einbetten ActiveX Objekte über Skripts auf einer Seite und nur auf Systemen unterstützt, auf denen Microsoft Windows 95, Windows 98 und Windows NT 4.0 (oder höher) ausgeführt wird. Wenn Sie Microsoft Internet Explorer ( ) nicht verwenden, wenden Sie [https://www.microsoft.com/windows/ie/](https://www.microsoft.com/windows/internet-explorer/default.aspx) sich an Ihren Browseranbieter, um weitere Informationen zum Support ActiveX zu erhalten.

 

 





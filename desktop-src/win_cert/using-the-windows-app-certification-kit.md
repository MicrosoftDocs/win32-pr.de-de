---
title: Verwenden des Zertifizierungskits für Windows-Apps
description: Um ihrer Desktop-App die beste Chance zu geben, eine Zertifizierung zu erhalten, überprüfen und testen Sie Sie auf Ihrem Computer, bevor Sie Sie zur Zertifizierung einreichen und im Windows Store auflisten.
ms.assetid: 8B460B84-0997-4987-9B66-90F9C6D88D83
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 89b3c6e4de3286dd6418c4c8e186bcadaddf00b7
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "104391130"
---
# <a name="using-the-windows-app-certification-kit"></a>Verwenden des Zertifizierungskits für Windows-Apps

Um ihrer Desktop-App die beste Chance zu geben, eine Zertifizierung zu erhalten, überprüfen und testen Sie Sie auf Ihrem Computer, bevor Sie Sie zur Zertifizierung einreichen und im Windows Store auflisten. Zum Zertifizieren der APP müssen Sie das [zertifizierungskit für Windows-apps](/previous-versions//mt637081(v=vs.85))installieren und ausführen. Ausführliche Informationen zu bestimmten Tests im Kit finden Sie unter [Tests des Zertifizierungs Kits für Windows-apps](windows-app-certification-kit-tests.md).

Einen Überblick über den Zertifizierungsprozess und die Verwendung dieses Tools finden [Sie unter zertifizieren ihrer Desktop-App](windows-certification-portal.md).

Die aktuelle Version von Windows ACK ist in 14 Sprachen verfügbar (Tschechisch, Englisch, Französisch, Deutsch, Italienisch, Japanisch, Koreanisch, Polnisch, Portugiesisch (Brasilien), Russisch, Chinesisch (vereinfacht), Spanisch, Chinesisch (traditionell), Spanisch, Chinesisch (traditionell) und Türkisch).

## <a name="prerequisites"></a>Voraussetzungen

Vor der Installation von Windows ACK muss das Betriebssystem installiert und ausgeführt werden.

1. Installieren Sie das Betriebssystem, für das Sie apps entwickeln, und führen Sie es aus.

-   Wenn Sie Apps für Windows 7 entwickeln, können Sie Windows 7, Windows 8 oder Windows 8.1 installieren und ausführen.
-   Wenn Sie eine Windows 8-Desktop-App oder Windows 8-Desktop Geräte-App entwickeln, können Sie Windows 8 oder Windows 8.1 installieren und ausführen.
-   Wenn Sie eine Windows 8.1 Desktop-App oder Windows 8-Desktop Geräte-App entwickeln, installieren Sie Windows 8.1.

2. Installieren Sie das [Windows-zertifizierungskit für apps 3,3](/previous-versions//mt637081(v=vs.85)), das im Windows Software Development Kit (SDK) für Windows 8.1 enthalten ist.

**Hinweis:** Wenn Sie das zertifizierungskit für Windows-apps 3,3 oder höher auf Ihrem PC installieren, ersetzen Sie alle zuvor installierten Kit-Versionen.

## <a name="instructions-to-run-windows-app-certification-kit-33"></a>Anweisungen zum Ausführen des Windows App Certification Kit 3,3

**Validieren ihrer Desktop-App mithilfe des Windows-zertifizierungskit für apps 3,3 interaktiv**

1.  Suchen Sie im Startmenü nach Windows App CERT Kit.
2.  Klicken Sie im zertifizierungskit für Windows-apps auf die Test Validierungs Kategorie, die Sie ausführen möchten. Wenn Sie eine Desktop-App validieren, klicken Sie auf **Desktop-App** überprüfen.
3.  Navigieren Sie im nächsten Bildschirm zu der Setup Datei der Desktop-App, die Sie überprüfen möchten.
    -   **Hinweis:** Mithilfe der [Befehlszeilen Schritte](#commandlinesteps) können Sie ggf. Optionen oder einen Installations Schalter einschließen.
4.  Geben Sie den App-nutzentyp an, und klicken Sie dann auf **weiter**. Das Windows-zertifizierungskit für apps startet die Installation der Desktop-App mithilfe der Setup Dateien, damit die Installation überprüft werden kann.
5.  Wenn Sie aufgefordert werden, das System neu zu starten, um das Setup abzuschließen, klicken Sie auf **Nein**. Wenn Ihre APP mehrere Komponenten oder externe Abhängigkeiten installieren muss, wählen Sie den Namen für Ihre APP sorgfältig aus. Der Name, den Sie hier auswählen, ist der Name, den Ihre APP erhält, wenn Sie im Windows Store aufgeführt wird. Wenn die Überprüfung beendet ist, speichern Sie den Bericht mit dem Namen, den Sie in Schritt 6 für Ihre APP erhalten haben. Das Windows-zertifizierungskit für Apps erstellt eine XML-Berichtsdatei und speichert Sie.
6.  Navigieren Sie zu dem Ordner, in dem Sie den Bericht gespeichert haben, und öffnen Sie ihn, um die Testergebnisse anzuzeigen. Wenn der Test fehlgeschlagen ist und Sie für einen Verzicht berechtigt sind, werden die Informationen, die Sie übermitteln müssen, hier aufgeführt. Sie müssen eine ausführliche Beschreibung für jede mögliche Anforderung zur Aufhebung der Anforderung einreichen.

**Überprüfen Ihrer Windows-Desktop-App mithilfe des Windows-zertifizierungsk3,3 IT für apps über die Befehlszeile**

1.  Navigieren Sie zu dem Ordner, in dem Sie den Bericht gespeichert haben, und öffnen Sie ihn, um die Testergebnisse anzuzeigen. Fehlgeschlagene Tests mit einer möglichen Anforderung zum Anfordern von Anforderungen sind hier aufgeführt. Sie müssen eine ausführliche Beschreibung für jede mögliche Anforderung zur Aufhebung der Anforderung einreichen.
2.  Geben Sie in dem Ordner mit dem zertifizierungskit für Windows-Apps die folgenden Befehle in dieser Reihenfolge ein:

    -   <span id="commandLineSteps"></span><span id="commandlinesteps"></span><span id="COMMANDLINESTEPS"></span>`appcert.exe reset`
    -   `appcert test -apptype desktop -setuppath d:\cdrom\setup.exe  -appusage peruser -reportoutputpath [report file name]`

    dabei `[report file name]` gilt: der voll qualifizierte Dateiname der XML-Datei, die das Kit erstellt, um den Testbericht zu enthalten.

3.  Nachdem der Test abgeschlossen ist, öffnen Sie die Berichtsdatei namens \[ Name der Berichtsdatei, und zeigen Sie \] die Testergebnisse an.

    **Hinweis:** Weitere Informationen zur Befehlszeile des zertifizierungskit für Windows-apps erhalten Sie, wenn Sie den Befehl appcert.exe/?

    Das zertifizierungskit für Windows-apps muss im Kontext einer aktiven Benutzersitzung ausgeführt werden, aber es ist nicht möglich, apps in einer nicht interaktiven Sitzung zu starten. Die Art und Weise, wie das Kit Token zum Ausführen von Tests mit oder ohne Administratorrechte verarbeitet, hängt ebenfalls von diesem Benutzer Sitzungs Kontext ab. Das Kit kann von einem Dienst ausgeführt werden, der Dienst muss jedoch in der Lage sein, den Kit-Prozess in einer aktiven Benutzersitzung zu erzeugen.

**Verwenden des Zertifizierungs Kits für Windows-Apps zum Überprüfen Ihrer Windows 7-apps**

-   Das Windows-zertifizierungskit für apps hat das Windows Software Logo Kit ersetzt. Wenn Sie das Windows 7-Logo für Ihre APP verwenden möchten, verwenden Sie das zertifizierungskit für Windows-Apps für die Validierungstests und den Bericht. Das Kit kann erkennen, auf welchem Betriebssystem es ausgeführt wird und automatisch für Windows 7-apps gestartet wird. Führen Sie den gleichen Prozess zum Überprüfen von Windows 7-Apps aus.

**Einreichen zur Zertifizierung**

-   Nachdem Ihre APP überprüft wurde, können Sie Sie [über den Übermittlungs Prozess des Portals](https://www.microsoft.com/?ref=go)zur Zertifizierung einreichen.

## <a name="reference-documents"></a>Referenzdokumente

-   [Zertifizierungsanforderungen für Windows-Desktop-Apps](/windows/desktop/win_cert/certification-requirements-for-windows-desktop-apps)
-   [Whitepaper zur APP-Zertifizierung](https://www.microsoft.com/download/details.aspx?id=27414)
-   [Windows Store-Onboarding für Desktop-Apps](/previous-versions//dn322034(v=vs.85))
-   [Zertifizierungsanforderungen für die Windows 7-Desktop-App](https://techcommunity.microsoft.com/t5/windows-hardware-certification/bg-p/WindowsHardwareCertification)

## <a name="windows-app-certification-kit-tests"></a>Tests im Zertifizierungskit für Windows-Apps

Wir haben das Kit geändert, damit die [Windows-ACK-Tests](windows-app-certification-kit-tests.md) einfacher zu verwenden sind. Das Kit hat jetzt Folgendes:

-   Eine neue vereinfachte Benutzeroberfläche
-   Verbesserter Multi-User-Test, der nicht mehr erfordert, dass Sie ein zweites Benutzerkonto einrichten.

 

 
---
title: Verwenden des Zertifizierungskits für Windows-Apps
description: Damit Ihre Desktop-App die beste Chance hat, zertifiziert zu werden, überprüfen und testen Sie sie auf Ihrem Computer, bevor Sie sie zur Zertifizierung und Auflistung im Windows Store übermitteln.
ms.assetid: 8B460B84-0997-4987-9B66-90F9C6D88D83
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8692e87f8bd152b730129c0d8684bc7ec2ca91964ecd6c25e98eb3db3e0fce44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118708748"
---
# <a name="using-the-windows-app-certification-kit"></a>Verwenden des Zertifizierungskits für Windows-Apps

Damit Ihre Desktop-App die beste Chance hat, zertifiziert zu werden, überprüfen und testen Sie sie auf Ihrem Computer, bevor Sie sie zur Zertifizierung und Auflistung im Windows Store übermitteln. Um Ihre App zu zertifizieren, müssen Sie das [Windows App Certification Kit](/previous-versions//mt637081(v=vs.85))installieren und ausführen. Ausführliche Informationen zu bestimmten Tests im Kit finden Sie unter Windows Tests des [App Certification Kit.](windows-app-certification-kit-tests.md)

Einen überblick über den Zertifizierungsprozess und die Verwendung dieses Tools finden Sie unter [Zertifizieren Ihrer Desktop-App.](windows-certification-portal.md)

Das aktuelle Release von Windows ACK ist in 14 Sprachen verfügbar (Tschechisch, Englisch, Französisch, Deutsch, Italienisch, Japanisch, Koreanisch, Polnisch, Portugiesisch (Brasilien), Russisch, Vereinfachtes Chinesisch, Spanisch, Traditionelles Chinesisch und Türkisch.

## <a name="prerequisites"></a>Voraussetzungen

Bevor Sie die Windows ACK installieren, müssen Sie das Betriebssystem installieren und ausführen.

1. Installieren Sie das Betriebssystem, für das Sie Apps entwickeln, und führen Sie es aus.

-   Wenn Sie Apps für Windows 7 entwickeln, können Sie Windows 7, Windows 8 oder Windows 8.1 installieren und ausführen.
-   Wenn Sie eine Windows 8 Desktop-App oder Windows 8 Desktopgeräte-App entwickeln, können Sie Windows 8 oder Windows 8.1 installieren und ausführen.
-   Wenn Sie eine Windows 8.1 Desktop-App oder Windows 8 Desktopgeräte-App entwickeln, installieren Sie Windows 8.1.

2. Installieren Sie das [Windows App Certification Kit 3.3,](/previous-versions//mt637081(v=vs.85))das im Windows Software Development Kit (SDK) für Windows 8.1 enthalten ist.

**Hinweis:** Wenn Sie Windows App Certification Kit 3.3 oder höher auf Ihrem PC installieren, ersetzen Sie jede zuvor installierte Version des Kits.

## <a name="instructions-to-run-windows-app-certification-kit-33"></a>Anweisungen zum Ausführen Windows App Certification Kit 3.3

**Überprüfen Ihrer Desktop-App mit dem Windows App Certification Kit 3.3 interaktiv**

1.  Suchen Sie im Startmenü nach Windows App Cert Kit.
2.  Klicken Sie im Windows App Certification Kit auf die Testvalidierungskategorie, die Sie ausführen möchten. Wenn Sie eine Desktop-App überprüfen, wählen Sie **Desktop-App überprüfen** aus.
3.  Navigieren Sie auf dem nächsten Bildschirm zur Setupdatei der Desktop-App, die Sie überprüfen möchten.
    -   **Hinweis:** Sie können die [Befehlszeilenschritte](#commandlinesteps) verwenden, um bei Bedarf Optionen oder einen Installationsschalter einzufügen.
4.  Geben Sie den App-Nutzungstyp an, und klicken Sie dann auf **Weiter.** Das Windows App Certification Kit beginnt mit der Installation der Desktop-App mithilfe der Setupdateien, damit die Installation überprüft werden kann.
5.  Wenn Sie aufgefordert werden, das System neu zu starten, um das Setup abzuschließen, wählen Sie **Nein** aus. Wenn Ihre App mehrere Komponenten oder externe Abhängigkeiten installieren muss, wählen Sie den Namen für Ihre App sorgfältig aus. Der name, den Sie hier auswählen, ist der Name, den Ihre App erhält, wenn sie im Windows Store aufgeführt wird. Speichern Sie nach Abschluss der Überprüfung den Bericht mit dem Namen, den Sie Ihrer App in Schritt 6 gegeben haben. Das Windows App Certification Kit erstellt eine XML-Berichtsdatei und speichert sie.
6.  Navigieren Sie zu dem Ordner, in dem Sie den Bericht gespeichert haben, und öffnen Sie ihn, um die Ergebnisse des Tests anzuzeigen. Wenn ihr Test nicht erfolgreich war und Sie zu einem Widerruf berechtigt sind, werden die Informationen, die Sie übermitteln müssen, hier aufgeführt. Sie müssen eine ausführliche Beschreibung für jede mögliche Aufhebungsanforderung übermitteln.

**Überprüfen Ihrer Windows Desktop-App mithilfe des Windows App Certification Kit 3.3 über eine Befehlszeile**

1.  Navigieren Sie zu dem Ordner, in dem Sie den Bericht gespeichert haben, und öffnen Sie ihn, um die Ergebnisse des Tests anzuzeigen. Fehlgeschlagene Tests mit einer möglichen Aufhebungsanforderung sind hier aufgeführt. Sie müssen eine ausführliche Beschreibung für jede mögliche Aufhebungsanforderung übermitteln.
2.  Geben Sie in dem Ordner, der das Windows App Certification Kit enthält, die folgenden Befehle in dieser Reihenfolge ein:

    -   <span id="commandLineSteps"></span><span id="commandlinesteps"></span><span id="COMMANDLINESTEPS"></span>`appcert.exe reset`
    -   `appcert test -apptype desktop -setuppath d:\cdrom\setup.exe  -appusage peruser -reportoutputpath [report file name]`

    where: `[report file name]` ist der vollqualifizierte Dateiname der XML-Datei, die das Kit erstellt, um den Testbericht zu enthalten.

3.  Öffnen Sie nach Abschluss des Tests die Berichtsdatei namens Name der \[ Berichtsdatei, \] und zeigen Sie die Testergebnisse an.

    **Hinweis:** Geben Sie den Befehl appcert.exe /? ein, um weitere Informationen zur Windows App Certification Kit-Befehlszeile zu erhalten.

    Das Windows App Certification Kit muss im Kontext einer aktiven Benutzersitzung ausgeführt werden, Aber Sie können Apps nicht in einer nicht interaktiven Sitzung starten. Die Art und Weise, wie das Kit Token zum Ausführen von Tests mit oder ohne Administratorrechte behandelt, hängt auch von diesem Benutzersitzungskontext ab. Das Kit kann von einem Dienst ausgeführt werden, aber der Dienst muss in der Lage sein, den Kit-Prozess in einer aktiven Benutzersitzung zu starten.

**Verwenden des Windows App Certification Kit zum Überprüfen Ihrer Windows 7-Apps**

-   Das Windows App Certification Kit ersetzt das Windows Software Logo Kit. Wenn Sie das Windows 7-Logo für Ihre App verwenden möchten, verwenden Sie das Windows App Certification Kit für Ihre Validierungstests und Berichte. Das Kit kann erkennen, unter welchem Betriebssystem es ausgeführt wird, und wird automatisch für Windows 7 Apps gestartet. Führen Sie den gleichen Prozess zum Überprüfen von Windows 7 Apps aus.

**Einreichen zur Zertifizierung**

-   Nachdem Ihre App überprüft wurde, können Sie sie [über den Portalübermittlungsprozess](https://www.microsoft.com/?ref=go)zur Zertifizierung übermitteln.

## <a name="reference-documents"></a>Referenzdokumente

-   [Zertifizierungsanforderungen für Windows Desktop-Apps](/windows/desktop/win_cert/certification-requirements-for-windows-desktop-apps)
-   [Whitepaper zur App-Zertifizierung](https://www.microsoft.com/download/details.aspx?id=27414)
-   [Windows Store Onboarding für Desktop-Apps](/previous-versions//dn322034(v=vs.85))
-   [zertifizierungsanforderungen für Windows 7 Desktop-Apps](https://techcommunity.microsoft.com/t5/windows-hardware-certification/bg-p/WindowsHardwareCertification)

## <a name="windows-app-certification-kit-tests"></a>Tests im Zertifizierungskit für Windows-Apps

Wir haben das Kit geändert, um die Verwendung der [Windows ACK-Tests](windows-app-certification-kit-tests.md) zu vereinfachen. Das Kit verfügt jetzt über Folgendes:

-   Eine neue vereinfachte Benutzeroberfläche
-   Verbesserter Mehrbenutzertest, der nicht mehr erfordert, dass Sie ein zweites Benutzerkonto einrichten

 

 
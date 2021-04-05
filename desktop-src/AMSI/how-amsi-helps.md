---
title: Wie AMSI Ihnen hilft, gegen Schadsoftware zu schützen
description: Als Anwendungsentwickler können Sie aktiv an der Abwehr von Schadsoftware teilnehmen. Insbesondere können Sie Ihre Kunden vor dynamischer Skript basierter Schadsoftware und vor nicht herkömmlichen Wege von Cyberangriffen schützen.
ms.topic: article
ms.date: 02/27/2019
ms.openlocfilehash: 0d6aee30034312073123f5ab14b1924fd01e6eac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708148"
---
# <a name="how-the-antimalware-scan-interface-amsi-helps-you-defend-against-malware"></a>Wie die Antimalware-Scan Schnittstelle (AMSI) Sie bei der Verteidigung gegen Schadsoftware unterstützt

Eine Einführung in die Windows Antimalware Scan Interface (AMSI) finden Sie unter [Antimalware Scan Interface (AMSI)](antimalware-scan-interface-portal.md).

Als Anwendungsentwickler können Sie aktiv an der Abwehr von Schadsoftware teilnehmen. Insbesondere können Sie Ihre Kunden vor dynamischer Skript basierter Schadsoftware und vor nicht herkömmlichen Wege von Cyberangriffen schützen.

Angenommen, die Anwendung ist skriptfähig: Sie akzeptiert ein beliebiges Skript und führt Sie über eine Skript-Engine aus. Wenn ein Skript für die Bereitstellung an die Skript-Engine bereit ist, kann die Anwendung die Windows AMSI-APIs aufzurufen, um eine Überprüfung des Inhalts anzufordern. Auf diese Weise können Sie sicher ermitteln, ob das Skript bösartig ist, bevor Sie es ausführen.

Dies gilt auch, wenn das Skript zur Laufzeit generiert wurde. Skript (bösartig oder anderweitig), kann mehrere Durchgänge von "de-obfuscess" durchlaufen. Letztendlich müssen Sie die Skript-Engine jedoch mit reinem, nicht verarbeittem Code bereitstellen. Und das ist der Punkt, an dem Sie die AMSI-APIs aufrufen.

Hier sehen Sie eine Abbildung der AMSI-Architektur, bei der Ihre eigene Anwendung durch eines der Felder "andere Anwendung" dargestellt wird.

![die AMSI-Architektur](images/AMSI7Archi.jpg)

Die Windows AMSI-Schnittstelle ist geöffnet. Dies bedeutet, dass jede Anwendung Sie anrufen kann. und alle registrierten antischadsoftwaremodule können die an Sie gesendeten Inhalte verarbeiten.

Wir dürfen die Diskussion nicht auf die Skript-Engines beschränken. Möglicherweise handelt es sich bei Ihrer Anwendung um eine Kommunikations-APP, die sofort Nachrichten auf Viren scannt, bevor Sie Sie Ihren Kunden anzeigt. Oder vielleicht ist Ihre Software ein Spiel, das Plug-ins vor der Installation überprüft. Es gibt zahlreiche Möglichkeiten und Szenarios für die Verwendung von AMSI.

## <a name="amsi-in-action"></a>AMSI in Aktion

Werfen wir einen Blick auf AMSI in Action. In diesem Beispiel ist Windows Defender die Anwendung, die AMSI-APIs aufruft. Sie können jedoch dieselben APIs in ihrer eigenen Anwendung abrufen.

Im folgenden finden Sie ein Beispiel für ein Skript, das die XOR-Encoding-Technik verwendet, um die Absicht auszublenden (ob diese Absicht harmlos ist oder nicht). Diese Abbildung zeigt, dass das Skript aus dem Internet heruntergeladen wurde.

![in Base64 codiertes Beispielskript](images/AMSI8.png)

Um die Dinge interessanter zu machen, können wir dieses Skript manuell in der Befehlszeile eingeben, damit keine Datei vorhanden ist, die überwacht werden kann. Dies spiegelt den sogenannten "filless Threat" wider. Es ist nicht so einfach wie das Scannen von Dateien auf dem Datenträger. Die Bedrohung könnte eine Hintertür sein, die sich nur im Arbeitsspeicher eines Computers befindet.

Im folgenden sehen Sie das Ergebnis der Ausführung des Skripts in Windows PowerShell. Sie werden feststellen, dass Windows Defender das AMSI-Testbeispiel in diesem komplizierten Szenario erkennen kann, indem Sie lediglich die standardmäßige AMSI-Testbeispiel Signatur verwenden.

![Erkennen des AMSI-Test Beispiels durch Windows Defender](images/AMSI9proper.png)

## <a name="amsi-integration-with-javascriptvba"></a>AMSI-Integration in JavaScript/VBA

Der dargestellte Workflow unten beschreibt den End-to-End-Ablauf eines anderen Beispiels, in dem wir die Integration von AMSI in die Makro Ausführung innerhalb Microsoft Office veranschaulichen.

![AMSI-Integration in JavaScript/VBA](images/integ-js-vba.png)

- Der Benutzer erhält ein Dokument mit einem (bösartigen) Makro, das statische Antivirussoftware-Scans durch die Verwendung von Techniken wie Verschleierung, Kenn Wort geschützter Dateien oder anderen eingibt.
- Der Benutzer öffnet dann das Dokument mit dem (bösartigen) Makro. Wenn das Dokument in der geschützten Ansicht geöffnet wird, klickt der Benutzer auf **Bearbeitung aktivieren** , um die geschützte Ansicht zu beenden.
- Der Benutzer klickt auf **Makros aktivieren** , um das Ausführen von Makros zuzulassen.
- Beim Ausführen des Makros verwendet die VBA-Laufzeit einen Zirkel Puffer, um \[ 1 \] Daten und Parameter zu protokollieren, die sich auf Aufrufe von Win32-, com-und VBA-APIs beziehen.
- Wenn bestimmte Win32-oder COM-APIs, die als ein hohes Risiko angesehen werden (auch als *Trigger* bezeichnet) \[ \] , beobachtet werden, wird die Makro Ausführung angehalten, und der Inhalt des Zirkel Puffers wird an AMSI übermittelt.
- Der registrierte AMSI Anti-Malware-Dienstanbieter antwortet mit einem Urteil, um anzugeben, ob das Makro Verhalten bösartig ist.
- Wenn das Verhalten nicht bösartig ist, wird die Makro Ausführung fortgesetzt.
- Andernfalls schließt Microsoft Office die Sitzung in Reaktion auf die Warnung \[ 3 \] , und die AV kann die Datei unter Quarantäne stellen, wenn das Verhalten bösartig ist.

## <a name="what-does-this-mean-for-you"></a>Was bedeutet dies für Sie?

Für Windows-Benutzer werden Schadsoftware, die obfuskations-und ausweibungs Techniken auf den integrierten Skripting-Hosts von Windows 10 verwendet, automatisch auf eine viel tiefere Ebene als je zuvor überprüft, was zusätzliche Schutzstufen bietet.

Für Sie als Anwendungsentwickler sollten Sie in Erwägung gezogen haben, dass Ihre Anwendung die Windows AMSI-Schnittstelle aufruft, wenn Sie von der zusätzlichen Überprüfung und Analyse von potenziell schädlichem Inhalt profitieren möchten (und ihre Kunden mit schützen).

Als Antivirussoftware-Anbieter können Sie die Unterstützung für die AMSI-Schnittstelle implementieren. Wenn Sie dies tun, bietet die Engine viel tieferen Einblick in die Daten, die Anwendungen (einschließlich integrierter Skript Erstellungs Hosts von Windows 10) potenziell bösartig sind.

## <a name="more-background-info-about-fileless-threats"></a>Weitere Hintergrundinformationen zu filterlosen Bedrohungen

Sie sind möglicherweise neugierig auf Weitere Hintergrundinformationen zu den Arten von Filtern, die von Windows AMSI entwickelt wurden, um Sie Gegenmaßnahmen zu unterstützen. In diesem Abschnitt sehen wir uns das herkömmliche Cat-and-Mouse-Spiel an, das sich im Malware Ökosystem abspielt.

Wir verwenden PowerShell als Beispiel. Sie können jedoch dieselben Techniken und Prozesse nutzen, die wir mit jeder dynamischen Sprache &mdash; VBScript, Perl, Python, Ruby und mehr veranschaulichen.

Im folgenden finden Sie ein Beispiel für ein schädliches PowerShell-Skript.

![Beispiel eines bösartigen PowerShell-Skripts](images/AMSI1.png)

Obwohl mit diesem Skript lediglich eine Meldung auf den Bildschirm geschrieben wird, ist Schadsoftware in der Regel eher fehlerfrei. Sie können jedoch problemlos eine Signatur schreiben, um diese zu erkennen. Die Signatur könnte z. b. nach der Zeichenfolge "Write-Host" pwnd! "" suchen. in jeder Datei, die der Benutzer öffnet. Großartig: Wir haben unsere erste Schadsoftware erkannt!

Nachdem die erste Signatur erkannt wurde, reagieren die Autoren von Schadsoftware. Sie reagieren, indem Sie dynamische Skripts wie in diesem Beispiel erstellen.

![ein Beispiel für ein dynamisches Skript](images/AMSI2.png)

In diesem Szenario erstellen Autoren von Schadsoftware eine Zeichenfolge, die das auszuführen PowerShell-Skript darstellt. Sie verwenden jedoch eine einfache Verkettung von Zeichen folgen, um die frühere Signatur zu unterbrechen. Wenn Sie jemals die Quelle einer AD-geladenen Webseite anzeigen, sehen Sie viele Instanzen dieser Technik, die verwendet werden, um AD-blockierende Software zu vermeiden.

Schließlich übergibt der Autor der Malware diese verketteten Zeichenfolge an den `Invoke-Expression` &mdash; PowerShell-Cmdlet-Mechanismus, um Skripts auszuwerten, die zur Laufzeit erstellt oder erstellt werden.

Als Reaktion auf die Antischadsoftware beginnt eine einfache sprach Emulation. Wenn z. b. zwei Zeichen folgen verkettet werden, emulieren wir die Verkettung dieser beiden Zeichen folgen und führen dann unsere Signaturen für das Ergebnis aus. Leider ist dies ein ziemlich zerbrechlicher Ansatz, da Sprachen in der Regel über viele Möglichkeiten zum darstellen und Verketten von Zeichen folgen verfügen.

Nach dem abgefangen durch diese Signatur werden schadsoftwareautoren z. b. zu etwas komplizierteren, &mdash; z. b. zum Codieren von Skript Inhalten in Base64, wie im folgenden Beispiel gezeigt.

![Beispiel für Skript Inhalt in Base64](images/AMSI3.png)

Die meisten antischadsoftwaremodule implementieren auch die Base64-Decodierung, damit Sie ressourcenintensiv sind. Da wir außerdem eine Base64-Decodierung der Emulation implementieren, sind wir für einen Zeitraum im voraus.

In der Antwort werden schadsoftwareautoren in algorithmische Verschleierung verschoben, &mdash; z. b. ein einfacher XOR-Codierungs Mechanismus in den Skripts, die Sie ausführen.

![Beispiel eines algorithmischen Verschleierung-Skripts](images/AMSI4.png)

An diesem Punkt liegt es in der Regel daran, dass Antivirenmodule emuliert oder erkannt werden, sodass wir nicht unbedingt erkennen, was dieses Skript macht. Wir können jedoch mit dem Schreiben von Signaturen für die obfuskations-und Codierungsverfahren beginnen. Tatsächlich handelt es sich dabei um die meisten Signaturen für skriptbasierte Schadsoftware.

Aber was ist, wenn der Obfuscator so trivial ist, dass er viele gut verhaltene Skripts sieht? Eine Signatur dafür würde eine akzeptable Anzahl falsch positiver Ergebnisse generieren. Im folgenden finden Sie ein Beispiel für ein *Stager* -Skript, das zu harmlos ist, um selbst zu erkennen.

![ein Beispiel für ein Stager-Skript, das zu unschädlich ist, um eigenständig zu erkennen](images/AMSI5.png)

In diesem Beispiel wird eine Webseite heruntergeladen und ein Teil des Inhalts aufgerufen. Dies ist die Entsprechung in Visual Basic Skripts.

![die Entsprechung in Visual Basic Skript](images/AMSI6.png)

In beiden Beispielen wird durch das Antivirenmodul überprüft, ob Dateien vom Benutzer geöffnet werden. Wenn der schädliche Inhalt nur im Arbeitsspeicher vorhanden ist, kann der Angriff potenziell nicht erkannt werden.

In diesem Abschnitt wurden die Einschränkungen der Erkennung mithilfe herkömmlicher Signaturen aufgezeigt. Obwohl ein bösartiges Skript mehrere Durchgänge von "de-obfuscting" durchlaufen kann, muss es letztendlich die Skript-Engine mit reinem, nicht übergreifendem Code bereitstellen. Und zu diesem Zeitpunkt, &mdash; wie wir im ersten Abschnitt oberhalb der &mdash; von Windows 10 integrierten Skript Hosts beschrieben werden, werden die AMSI-APIs aufgerufen, um eine Überprüfung dieses ungeschützten Inhalts anzufordern. Und Ihre Anwendung kann dasselbe tun.

## <a name="related-resources"></a>Zugehörige Ressourcen

* [Filterlose Bedrohungen](/windows/security/threat-protection/intelligence/fileless-threats)
* [Office VBA + AMSI: der Schleier wird bei bösartigen Makros getrennt](https://cloudblogs.microsoft.com/microsoftsecure/2018/09/12/office-vba-amsi-parting-the-veil-on-malicious-macros/)
* [Nicht sichtbar, aber nicht unsichtbar: Bekämpfung von nicht sichtbaren Schadsoftware mit Verhaltens Überwachung, AMSI und Next-Gen-AV](https://cloudblogs.microsoft.com/microsoftsecure/2018/09/27/out-of-sight-but-not-invisible-defeating-fileless-malware-with-behavior-monitoring-amsi-and-next-gen-av/)

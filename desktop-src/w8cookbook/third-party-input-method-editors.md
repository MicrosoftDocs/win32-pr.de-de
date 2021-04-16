---
title: Eingabemethoden-Editoren von Drittanbietern
description: Eingabemethoden-Editoren von Drittanbietern
ms.assetid: 7FFD7210-2335-4499-A36A-ACFAECEB01F9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cca9768de96b9dcdeac7f4b0da210f7aa788801b
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "104563954"
---
# <a name="third-party-input-method-editors"></a>Eingabemethoden-Editoren von Drittanbietern

## <a name="platforms"></a>Plattformen

**Clients** -Windows 8  
**Server** -Windows Server 2012  


## <a name="description"></a>BESCHREIBUNG

Eingabemethoden-Editoren (Input Method Editors, IMEs) sind Softwarekomponenten, die es Benutzern ermöglichen, Text in einer Sprache einzugeben, die mehr Zeichen enthält, als auf einer Tastatur dargestellt werden können. (Dies ist häufig, aber nicht auf ostasiatische Sprachen beschränkt.) Anstatt jedes einzelne Zeichen, das in einem einzelnen Schlüssel angezeigt wird, geben Benutzer Tastenkombinationen ein, die dann vom IME interpretiert werden. Der IME generiert das Zeichen, das mit dem Satz von Tastenkombinationen übereinstimmt, und zeigt dem Benutzer mitunter eine Liste möglicher Zeichen an, die ausgewählt werden können, und fügt das Zeichen anschließend in das Bearbeitungs Steuerelement der APP des Benutzers ein.

In der Vergangenheit ermöglichte Windows das Ausführen von Drittanbieter-IMEs im Windows-System, und diese Funktion wird für Windows 8 fortgesetzt. Benutzer können ein Drittanbieter-IME installieren und verwenden. Außerdem Härten wir das System und die Prozesse, um böswillige IMEs zu verhindern, die Sicherheit zu verbessern und die Benutzer Leistung zu verbessern.

In Windows 8 finden Sie Folgendes:

-   IME-Unterstützung von Drittanbietern für Hardware Tastatur und Fingereingabe Tastatur
-   Drittanbieter von IME-Anbietern müssen die Microsoft-Richtlinien befolgen, um Ihre IMEs für Windows 8 zu entwickeln.
-   Drittanbieter-IMEs müssen digital signiert sein.
-   Die IMEs von Drittanbietern muss mit dem Text Services Framework (TSF) kompatibel sein, und die richtigen IME-Flags müssen so festgelegt werden, dass Sie in Windows 8 richtig ausgeführt werden
-   Ältere Drittanbieter-IMEs können in Desktop-Apps ausgeführt werden, werden jedoch in Windows Store-Apps blockiert.
-   Drittanbieter-IMEs können das von Windows bereitgestellte Touchscreen-Tastaturlayout verwenden, um den IME zu verknüpfen, sodass Benutzer ihren IME mit Fingereingabe Tastatur verwenden können. Bestimmte Funktionen von in-Box-IMEs für Berührungs Tastaturen stehen jedoch nicht für Drittanbieter-IMEs zur Verfügung.
-   Windows Defender entfernt böswillige IMEs aus dem Windows-System.

## <a name="manifestation"></a>Ausstrahlung

**Änderungen an der Eingabe Sprache und der Eingabemethode wechseln**

Anstatt alle IME-Modussymbole zusammen mit dem IME-Branding-Symbol anzuzeigen, wird nur ein IME-Modus-Symbol zusammen mit dem IME-Branding-Symbol angezeigt. Die beiden folgenden Abbildungen zeigen das Windows 8-eingabeflyout und das IME-Flyout mit japanischer IME als aktuelle Eingabemethode. Wenn Sie auf das IME-Branding-Symbol klicken, können Sie die Eingabemethoden wechseln.

![Eingabemethoden wechseln](images/inputindicator2.png)

Wenn Sie auf das Symbol für den IME-Modus klicken, können Sie zu einem anderen IME-Modus wechseln.

![Switch-IME-Modi](images/inputindicator1.png)

Wenn ein IME von der sprach Leiste abhängig ist, um seine Mode-Symbole in Windows 7 anzuzeigen, muss der IME geändert werden, um das Brandingsymbol und das Symbol Modus im Eingabe Indikator in Windows 8 anzuzeigen.

> [!Note]  
> Hinweis: die Details zur Anzeige des Branding-Symbols und-Modus-Symbols im Systray auf der Desktop-Taskleiste werden in den Windows 8 IME-Richtlinien dokumentiert und öffentlich veröffentlicht.

 

**Neue Windows-Umgebung**

Die Umgebung in Windows 8 ändert das Querformat für IMEs. Die Konzepte von Windows Store-Apps, lokalen Kontext-App-Containern und API-Einschränkungen für IMEs waren in Windows 7 nicht vorhanden. Einige vorhandene Windows 7-IMEs reagieren nicht mehr, wenn Sie in einer Windows Store-App ausgeführt werden, sodass ältere IMEs nicht in Windows Store-Apps ausgeführt werden dürfen. Stellen Sie außerdem sicher, dass neue Versionen von IMEs überprüft werden, um sicherzustellen, dass Sie mit der neuen Benutzeroberflächen Umgebung kompatibel sind, bevor Sie in Windows Store-Apps ausgeführt werden.

## <a name="mitigation"></a>Minderung

Sie können einen Desktop kompatiblen IME auf dem System verwenden. Dies ist möglicherweise die beste Option, wenn Sie hauptsächlich Desktop-Apps verwenden und Sie weiterhin eine bevorzugte Legacy-IME für die Eingabe verwenden möchten. Es wird empfohlen, dass Sie eine Windows 8-IME verwenden und keine älteren/nicht zertifizierten IMEs verwenden. Benachrichtigungen werden sowohl von der CPL der Sprache als auch vom Eingabe Schalter bereitgestellt, um Sie vor den Auswirkungen der Verwendung eines Desktop kompatiblen IME zu warnen.

Wenn ein Desktop kompatibler IME nicht in Ihrem System funktioniert, wird eines der folgenden Verhaltensweisen angezeigt:

-   Die Benutzeroberfläche der Sprache cpl bezeichnet Desktop kompatible IMEs und zeigt eine Meldung an, dass nicht kompatible IMEs nur in Desktop-apps funktionieren.
-   Das eingabeflyout blendet Desktop kompatible IMEs aus, wenn sich der Benutzer in Windows Store-Apps befindet. Dies gibt an, dass der IME in dieser APP nicht funktioniert. (Auf dem Desktop sind Desktop kompatible IMEs nicht ausgegraut). Wenn Sie mit einem nicht kompatiblen IME zu Windows Store-Apps wechseln und erkennen, dass IME deaktiviert ist, verwenden Sie den Eingabe Indikator, um zu einem IME zu wechseln, der mit Windows Store-Apps kompatibel ist.

Legacy-oder Desktop kompatible IMEs sind auf folgende Bedingungen beschränkt:

-   Aktualisieren von Windows 7 auf Windows 8 mit Drittanbieter-IMEs auf dem System
-   Der Anbieter hat eine Version, die mit Windows 8 kompatibel ist, nicht freigegeben, und der Benutzer versucht, eine vorhandene Windows 7-Version in der Zwischenzeit zu verwenden.

## <a name="solution"></a>Lösung

**Allgemein**

Verwenden Sie die vorhandene TSF-Infrastruktur (Text Services Framework), um Ihre IME-Logik und die allgemeinen Steuerelemente der Windows Store-App für Ihre Benutzeroberflächen zu implementieren. Erstellen Sie eigene Fenster zum Hosten Ihrer Benutzeroberfläche.

Neue Such-APIs werden hinzugefügt, um die Such Vorhersage zu verbessern und eine saubere Such Oberfläche in der Benutzeroberfläche bereitzustellen.

APIs werden auch hinzugefügt, um Drittanbieter-IMEs zu benachrichtigen, wenn eine Fingereingabe Tastatur aufgerufen wird, um die Benutzeroberfläche vor der über tastentastatur zu schützen. Ein Standardmäßiges klassisches Touchscreen-Tastaturlayout wird für Drittanbieter-IMEs automatisch geladen. Es sind keine weiteren Schritte erforderlich, um mit diesem klassischen Fingereingabe-Tastaturlayout zu integrieren. Drittanbieter-IMEs können jedoch ein alternatives Fingerabdruck Layout anfordern.

Machen Sie sich mit den Windows 8 IME-Richtlinien vertraut, damit Sie wichtige Windows Store-App-Benutzeroberflächen-Prinzipien in Ihrem IME herauf Stufen können. Bei den Richtlinien, die den Richtlinien entsprechen, muss ein Flag festgelegt werden, um anzugeben, dass der IME mit dem Microsoft-Entwurf kompatibel ist. Windows 8 blockiert, dass alle Desktop kompatiblen IMEs in Windows Store-Apps ausgeführt werden.

Digitale Signierung, zusätzlich zur Sperrung durch Windows Defender, verhindert, dass böswillige IMEs auf dem Windows 8-System installiert werden. Bei der Identitätsüberprüfung wird die dll-dll eines Drittanbieters digital signiert. Nur IMEs, die über diese digitale Signatur verfügen, können auf dem System installiert werden, ohne dass dem Benutzer eine kritische Warnmeldung angezeigt wird. Benutzer können böswillige IMEs melden. Nachdem eine IME als bösartig festgelegt wurde, wird Sie von Windows Defender aus dem Windows-System entfernt.

**Textdienstframework**

Der IME muss TSF-fähig sein, damit er in Windows 8 ausgeführt werden kann. Windows 8 blockiert das Ausführen von nicht TSF-fähigen IMEs in Windows Store-Apps. Wenn eine APP gestartet wird, lädt TSF die IME. dll für den IME, den der Benutzer im App-Prozess ausgewählt hat.

> [!Note]  
> Um separate Funktionen oder Benutzeroberflächen zwischen Windows Store-Apps und Desktop-Apps bereitzustellen, kann die von TSF geladene DLL überprüfen, in welche Art von APP Sie geladen wird. Der IME Ruft die [itfthreadmgrex:: getactiveflags](/windows/win32/api/msctf/nf-msctf-itfthreadmgrex-getactiveflags) -Methode auf und überprüft das tf \_ TMF \_ immersivemode-Flag und kann je nach Ergebnis eine andere APP-Logik auslöst.

 

Wenn eine IME in eine Windows Store-App geladen wird, unterliegt Sie denselben App-Container Einschränkungen wie die APP selbst. Durch dieses Verhalten wird sichergestellt, dass die IMEs nicht in der Lage ist, Sicherheits Verträge für Windows Store-Apps zu verletzen, obwohl Sie Zugriff auf das Desktop-SDK haben (da Sie nicht vom Windows Store verteilt oder zertifiziert werden). Einige Funktionen, die zurzeit durchgeführt werden, sind in einem App-Container betroffen. Zu diesen Funktionen gehören:

-   Wörterbuchdateien
-   Internet Aktualisierung
-   Schulungs-Learning
-   Freigeben von Informationen zwischen Prozessen

Weitere Informationen finden Sie in den Richtlinien zu Windows 8 IME.

Ältere IMEs können nicht in Windows Store-Apps verwendet werden, um das Potenzial von Benutzeroberflächen zu vermeiden, einschließlich Systemunterbrechungen. Mit den Windows Store-Apps kompatible IMEs müssen sich selbst deklarieren, indem Sie ein Flag festlegen, das diese Kompatibilität angibt. Dieses Flag wird von TSF in der TF- \_ inputprocessorprofile-Struktur bereitgestellt. Details zur Verwendung dieses Flags zum Deklarieren eines Drittanbieter-IME als Windows Store-APP-kompatibel werden dokumentiert und öffentlich in den Windows 8 IME-Richtlinien veröffentlicht.

Mit Windows Store-Apps kompatible IMEs dürfen in Desktop-Apps oder Windows Store-Apps ausgeführt werden. Nicht kompatible IMEs können nur in Desktop Prozessen ausgeführt werden.

**User interface (Benutzeroberfläche)**

Obwohl Drittanbieter-IMEs Zugriff auf Desktop windowingapis haben, müssen Sie dieselben Fenster-API-Einschränkungen wie die APP einhalten, in der Sie ausgeführt werden. So kann z. b. ein IME nicht über eine Windows Store-App hinaus gezeichnet werden, während diese in einer Desktop-App aktiv ist. API-Einschränkungen werden zur Vermeidung dieser Szenarien eingesetzt:

-   Desktop-Apps, die sich auf Windows Store-Apps konzentrieren
-   Erstellen von Desktop-Apps in der Windows Store-App
-   Desktop-Apps, die Windows Store-Apps beeinträchtigen

**Unterstützung der Bildschirmtastatur**

Obwohl die Unterstützung der Fingereingabe Tastatur (TKB) für IME-Drittanbieter weiterhin verfügbar ist, ist in Windows 8 keine vollständig anpassbare und integrierte Berührungs Tastatur verfügbar. Allerdings können die IMEs von Drittanbietern dem Tastaturlayout zugeordnet werden, das für die Berührungs Optimierung optimiert ist. Der Windows Soft Input Panel (SIP) stellt standardmäßig ein klassisches Tastaturlayout für Drittanbieter-IMEs bereit. Da die klassische Tastatur wichtige Ereignisse generiert, die der Hardware Tastatur ähneln, gibt es zurzeit keine besondere Implementierungs Anforderung für Drittanbieter-IMEs, mit einer Touchscreen-Tastatur zu arbeiten. Bei der Eingabe Behandlung für Hardwareschlüssel Ereignisse werden auch Schlüsselereignisse von klassischen Berührungs Layouts behandelt.

> [!Note]  
> Hinweis: IMEs müssen möglicherweise mit der Verarbeitung von Unicode-Eingabe Ereignissen beginnen, wenn die Unterstützung von TKB erweitert wird, um auch optimierte Tastaturlayouts einzuschließen.

 

Ein Drittanbieter-IME kann auswählen, ob das optimierte Tastaturlayout für den IME verwendet werden soll. Weitere Informationen finden Sie in der IME-Richtlinie von Drittanbietern.

Stellen Sie sicher, dass die Benutzeroberfläche Ihres Kandidaten Bereichs (und andere Elemente der Benutzeroberfläche) nicht unterhalb der Fingereingabe Tastatur gezeichnet werden. In den meisten Fällen sollte die APP die Größe des Fensters ändern, um die Touchscreen-Tastatur zu berücksichtigen. Wenn eine APP dies jedoch nicht durchführt, können Sie weiterhin die inputpaneframework-API verwenden, um die Position der Touchscreen-Tastatur zu erlernen. Drittanbieter-IDs können diese API verwenden, um den von der touchtastatur genutzten Bildschirmbereich vor dem Zeichnen von Kandidaten (oder anderen) UIs zu erhalten und die Benutzeroberfläche erneut zu übertragen, um das Zeichnen unterhalb der touchtastatur zu vermeiden.

**Suchen**

In Windows 8 können Windows Store-Apps Ihren Benutzern problemlos Suchfunktionen bereitstellen, indem Sie den [Such Vertrag](/previous-versions/windows/apps/hh464906(v=win.10)) implementieren und in den Suchbereich integrieren. Der Suchbereich ist ein zentraler Ort, an dem Benutzer Suchvorgänge für alle Ihre apps durchführen können. Windows unterstützt apps, die den Suchbereich verwenden, Ihre Benutzer, wo Sie so schnell wie möglich sind. Insbesondere für IME-Benutzer bietet Sie eine einzigartige Suchfunktion, mit der kompatible IMEs in Windows 8 integriert werden kann, um eine höhere Effizienz und Benutzerfreundlichkeit zu erzielen.

Ein IME ist mit der integrierten Suchfunktion kompatibel, wenn diese folgende Kriterien erfüllt:

-   Ist kompatibel mit der Windows Store-App-Umgebung
-   Implementiert APIs im TFS-uiless-Modus
-   Implementiert APIs für die Integration von TFS-Suche:
-   -   ITF searchcandidateprovider
    -   ITF searchhardwarekeyboardverhaltensweisen

Wenn Sie im Suchbereich aktiviert ist, wird der kompatible IME im uiless-Modus abgelegt und kann die Benutzeroberfläche nicht anzeigen. Stattdessen werden Konvertierungs Kandidaten an Windows gesendet, die dann im Inline Kandidatenlisten-Steuerelement angezeigt werden.

Der IME sendet auch Windows-Kandidaten, die zum Ausführen der aktuellen Suche verwendet werden sollen – diese Kandidaten können mit den Konvertierungs Kandidaten übereinstimmen oder auf die Suche zugeschnitten werden. Gute Such Kandidaten erfüllen folgende Kriterien:

-   Keine Präfix Überlappung
-   Kein Vorhersage Kandidat (nur Abschluss)

IMEs, die die Kriterien nicht erfüllen und nicht mit Search kompatibel sind, werden auf die gleiche Weise wie in anderen Windows Store-App-Steuerelementen angezeigt und können die Benutzeroberflächen Integration und Such Kandidaten nicht nutzen. (Apps empfangen nur Abfragen, nachdem der Benutzer das Verfassen der Erstellung abgeschlossen hat.)

Wenn eine APP, die den Such Vertrag unterstützt, eine Abfrage empfängt, enthält das Abfrage Ereignis ein "querytextalternatives"-Array mit allen bekannten Alternativen, das von der relevantesten (wahrscheinlichsten) bis zum am wenigsten relevanten (unwahrscheinlich) ist. Wenn Alternativen bereitgestellt werden, sollte die APP jede Alternative als Abfrage behandeln und alle Ergebnisse zurückgeben, die mit einer der alternativen übereinstimmen (als ob der Benutzer mehrere Abfragen gleichzeitig ausgegeben hätte) und im Grunde eine "oder"-Abfrage an den Dienst ausgeben, der die Ergebnisse liefert. Um die Leistung zu verbessern, schränken apps häufig die Übereinstimmungen mit den 10 relevantesten Alternativen ein.

**Digitale IME-Signatur**

Alle Drittanbieter-IMEs müssen digital signiert werden, damit Sie als IME auf dem Windows 8-System installiert werden können. Mithilfe von SmartScreen können Benutzer eine Warnmeldung anzeigen, wenn Sie eine nicht signierte IME aus dem Web herunterladen. So rufen Sie ein Zertifikat ab und Signieren Ihre Dateien:

-   **Verwenden einer Authenticode-Signatur zum digitalen Signieren von Programmen**
    -   Abrufen eines gültigen Authenticode-Code Signatur Zertifikats von einer der vielen Zertifizierungsstellen, die von Windows unterstützt werden
    -   Verwenden von Entwicklungs Tools (z. b. [signtool.exe](../seccrypto/signtool.md)) zum Signieren der apps vor der Verteilung
    -   Weitere Informationen und eine Schritt-für-Schritt-Beschreibung des Code Signatur Prozesses finden Sie im Blogeintrag alles, was [Sie über die Authenticode-Code Signatur wissen müssen](/archive/blogs/ieinternals/everything-you-need-to-know-about-authenticode-code-signing) .
-   **Sicherstellen, dass Downloads nicht als Malware erkannt werden**
    -   Heruntergeladene Programme, die als Malware erkannt und bestätigt werden, wirken sich sowohl auf den Download als auch auf den Ruf des digitalen Zertifikats aus, das zum Signieren der Datei verwendet wird
-   **Für Windows-Zertifizierung anwenden**
    -   Besuchen Sie die Windows-App-Zertifizierungs Seite auf MSDN

Weitere Informationen finden Sie in den folgenden Artikeln zu digitalen Signaturen und Code Signatur:

-   [Übersicht über Authenticode](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537359(v=vs.85))
-   [Sicherstellen der Integrität und Authentizität](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))
-   [Bewährte Methoden für die Code Signatur](/previous-versions/windows/hardware/design/dn653556(v=vs.85))
-   [Was sind digitale Zertifikate?](/previous-versions/office/developer/office2000/aa190113(v=office.10))

Wenn ein IME **nicht signiert ist** , empfängt der Benutzer diese Warnmeldung, wenn er versucht, den IME herunterzuladen:

![die Meldung "IME ist nicht signiert"](images/downloadwarning02-fhu-ivu.png)

Wenn ein IME signiert ist, wird den Benutzern stattdessen diese Meldung angezeigt:

![IME-signierte Nachricht](images/downloadwarning01-fhu-vcu.png)

Basierend auf diesen Benachrichtigungen können Benutzer auswählen, ob die Datei gelöscht oder die Warnung ignoriert und das heruntergeladene Programm ausgeführt werden soll.

**IME-Sperrung**

Solche, die böswillige oder nicht den Windows 8-IME-Richtlinien folgen, können mithilfe von Windows Defender aus dem System entfernt werden. Weitere Informationen über böswillige IMEs finden Sie im Artikel zu [Drittanbieter-IMEs in Windows 8](/previous-versions/windows/apps/hh967426(v=win.10)).

## <a name="resources"></a>Ressourcen

-   [Itfthreadmgrex:: Get Active Flags-Methode](/windows/win32/api/msctf/nf-msctf-itfthreadmgrex-getactiveflags)
-   [SignTool](../seccrypto/signtool.md)
-   [Alles, was Sie über die Authenticode-Code Signatur wissen müssen](https://blogs.msdn.com/b/ieinternals/archive/2011/03/22/authenticode-code-signing-for-developers-for-file-downloads-building-smartscreen-application-reputation.aspx)
-   [Windows-App-Verträge und-Erweiterungen](/previous-versions/windows/apps/hh464906(v=win.10))
-   [Zertifizierungsanforderungen für Windows 8-Desktop-Apps](../win_cert/certification-requirements-for-windows-desktop-apps.md)
-   [Zertifizierungsanforderungen für Windows-apps](https://msdn.microsoft.com/library/windows/apps/51A7C609-94AB-49ab-B8E0-F26FF776DDB4.aspx)
-   [Verwenden des Zertifizierungskits für Windows-Apps](../win_cert/using-the-windows-app-certification-kit.md)
-   [Übersicht über Authenticode](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537359(v=vs.85))
-   [Sicherstellen der Integrität und Authentizität](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)#Ensuring_Integrity_a)
-   [Bewährte Methoden für die Code Signatur](/previous-versions/windows/hardware/design/dn653556(v=vs.85))
-   [Was sind digitale Zertifikate?](/previous-versions/office/developer/office2000/aa190113(v=office.10))

 

 
---
title: Gruppenrichtlinien
description: Background Intelligent Transfer Service (Bits) verwendet die folgenden Gruppenrichtlinien, um Bits-Übertragungen und-Einstellungen zu konfigurieren. Weitere Informationen darüber, welche Version von Bits von unterschiedlichen Versionen von Windows verwendet wird, finden Sie im Thema Neuerungen.
ms.assetid: 32c7e2b1-bac2-4708-a30c-f6b2a816c1a4
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: f3ff0070c489759055bdaae1d2e68d8718a7bae5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206307"
---
# <a name="group-policies"></a>Gruppenrichtlinien

> [!NOTE]
> Ausführliche Informationen zur Verwendung der Verwaltung mobiler Geräte (Mobile Device Management, MDM) zum Festlegen von Richtlinien für Background Intelligent Transfer Service (Bits) finden Sie unter [Policy CSP](/windows/client-management/mdm/policy-configuration-service-provider).

Background Intelligent Transfer Service (Bits) verwendet die folgenden Gruppenrichtlinien, um Bits-Übertragungen und-Einstellungen zu konfigurieren. Weitere Informationen darüber, welche Version von Bits von unterschiedlichen Versionen von Windows verwendet wird, finden Sie im Thema [Neuerungen](what-s-new.md) .

> [!NOTE]  
> Wenn der Richtlinien Wert nicht festgelegt ist, verwendet Bits den Standardrichtlinien Wert.

**So aktivieren Sie eine Bits-Richtlinie**

1.  Öffnen Sie Gruppenrichtlinie, indem Sie **gpeer dit. msc/gpcomputer: "***Computername***"** im Fenster " **Ausführen** " oder an der Eingabeaufforderung in einem cmd-Fenster eingeben.
2.  Bits-Richtlinien befinden sich unter **Computer Konfiguration**, **Administrative Vorlagen**, **Netzwerk** **Background Intelligent Transfer Service**.
3.  Klicken Sie mit der rechten Maustaste auf die Richtlinie und wählen Sie **Bearbeiten**
4.  Befolgen Sie die Anweisungen zum Aktivieren und Festlegen der Richtlinie.

Die Gruppenrichtlinien für Bits befinden sich in der Registrierung unter **HKEY \_ local \_ Machine** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **Bits**. Beachten Sie, dass nur die konfigurierten Richtlinien in der Registrierung aufgeführt sind.

|Richtlinie|BESCHREIBUNG|
|-|-|
|JobInactivityTimeout<br/>Bits 1,0|Standardmäßig verwaltet Bits Informationen zu einem Auftrag für 90 Tage. Wenn für diesen Zeitraum keine Aktivität für den Auftrag vorhanden ist, bricht Bits den Auftrag ab. Der Übertragungs Fortschritt oder die Eigenschafts Änderungen haben den Timer zurückgesetzt.<br/> Sie müssen diese Richtlinie möglicherweise anpassen, wenn sich der Benutzer über einen längeren Zeitraum nicht anmelden oder eine Netzwerkverbindung nicht aufrecht erhält.|
|MaxInternetBandwidth<br/>BITS 2,0|Schränkt die Netzwerkbandbreite ein, die Bits für Hintergrund Übertragungen verwendet (diese Richtlinie wirkt sich nicht auf Vordergrund Übertragungen aus).<br/>Geben Sie eine Beschränkung an, die während eines bestimmten Zeitintervalls verwendet werden soll, sowie eine Beschränkung für die Verwendung zu allen anderen Zeiten. Beschränken Sie z. b. die Verwendung der Netzwerkbandbreite auf 10 KBit pro Sekunde (Kbit/s) von 8:00 Uhr. bis 5:00 Uhr und die gesamte verfügbare Bandbreite für den Rest der Zeit verwenden.<br/>**Hinweis**: das Ändern der Systemuhr wirkt sich nicht auf das Zeitintervall für die Bandbreitenbeschränkung aus. Beispiel: Wenn die aktuelle Uhrzeit 2:00 Uhr ist. das Intervall für die Bandbreitenbeschränkung beginnt um 3:00 Uhr, und die Systemuhr wird eine Stunde vorwärts verschoben, bedeutet jedoch nicht, dass Bits die Bandbreitenbeschränkung eine Stunde früh erzwingen wird, wenn die Bandbreitenbeschränkung immer noch in einer Stunde stattfindet. Um die Änderung der Systemuhr in Bits widerzuspiegeln, müssen Sie den Computer oder den Bits-Dienst neu starten.<br/>Geben Sie den Grenzwert in Kbit pro Sekunde an. Basieren Sie auf der Größe der Netzwerkverbindung, nicht auf der Netzwerkschnittstellenkarte (NIC) des Computers. Bits verwendet ungefähr zwei Kbit, wenn Sie einen Wert angeben, der kleiner als zwei Kbit ist. Um zu verhindern, dass BITS-Übertragungen durchgesetzt werden, geben Sie ein Limit von 0 Wenn Sie einen Grenzwert von NULL angeben, werden alle Hintergrund Aufträge von Bits in einen vorübergehenden Fehlerzustand versetzt. (Der Fehlercode wird auf BG_E_BLOCKED_BY_POLICY festgelegt.) Bits versetzt die Aufträge nach Ablauf des Zeitintervalls in den Warteschlangen Zustand.<br/> Wenn Sie diese Richtlinie deaktivieren oder nicht konfigurieren, verwendet Bits die gesamte verfügbare nicht verwendete Bandbreite.<br/> Normalerweise verwenden Sie diese Richtlinie, um zu verhindern, dass BITS-Übertragungen für die Netzwerkbandbreite konkurrieren, wenn der Client über einen schnellen Netzwerkadapter verfügt (10 Mbit/s), aber über eine langsame Verbindung (56 Kbit/s) mit dem Netzwerk<br/> Informationen zur Verwendung der Netzwerkbandbreite durch Bits finden Sie unter [Netzwerkbandbreite](network-bandwidth.md).|
|Maxdownloadtime<br/>Bits 3,0|Bestimmt die Zeitdauer, die Bits zum aktiven übertragen der Dateien im Auftrag aufwenden kann. Der Standardwert ist 90 Tage.<br/> Um diese Richtlinie für einen bestimmten Auftrag zu überschreiben, müssen Sie die [**IBackgroundCopyJob4:: setmaximumdownloadtime**](/windows/desktop/api/bits3_0/nf-bits3_0-ibackgroundcopyjob4-setmaximumdownloadtime) -Methode aufrufen.|
|"Maxjobspermachine"<br/>Bits 3,0|Schränkt die Anzahl der Aufträge ein, die Benutzer auf dem Computer erstellen können. Der Standardwert ist 300 Aufträge. Diese Richtlinie gilt nicht für Benutzer mit Administratorrechten oder Dienst Konten.|
|"Maxjobsperuser"<br/>Bits 3,0|Schränkt die Anzahl der Aufträge ein, die ein Benutzer auf dem Computer erstellen kann. Der Standardwert ist 60 Aufträge pro Benutzer. Diese Richtlinie gilt nicht für Benutzer mit Administratorrechten oder Dienst Konten.|
|"Maxfilesperjob"<br/>Bits 3,0|Schränkt die Anzahl der Dateien ein, die ein Benutzer einem Auftrag hinzufügen kann. Der Standardwert ist 200 Dateien pro Auftrag. Diese Richtlinie gilt nicht für Benutzer mit Administratorrechten oder Dienst Konten.|
|"Maxrangesperfile"<br/>Bits 3,0|Schränkt die Anzahl der Bereiche ein, die ein Benutzer für eine Datei angeben kann. Der Standardwert ist 500 Bereiche. Diese Richtlinie gilt nicht für Benutzer mit Administratorrechten oder Dienst Konten.|

Bits verwendet die folgenden Gruppenrichtlinien, um zu aktivieren und zu konfigurieren, wie Bits mit BranchCache interagiert.

|Richtlinie|BESCHREIBUNG|
|-|-|
|Disablebranchcache<br/>Bits 4,0|Standardmäßig ist die Windows BranchCache-Funktion aktiviert. Legen Sie diese Richtlinie fest, um zu verhindern, dass BITS-Clients Inhalte mit Windows BranchCache übertragen.<br/>**Hinweis**: Diese Einstellung wirkt sich nicht auf die Verwendung von Windows BranchCache durch andere Anwendungen als Bits aus. Diese Richtlinie gilt nicht für BITS-Übertragungen über SMB (Server Message Block). Diese Einstellung hat keine Auswirkung, wenn die Verwaltungs Einstellungen des Computers für den Windows-BranchCache die Verwendung vollständig deaktivieren.|

Bits verwendet die folgenden Gruppenrichtlinien, um die Bandbreitendrosselung zu konfigurieren.

|Richtlinie|BESCHREIBUNG|
|-|-|
|Enablemaintenancelimits<br/>Bits 4,0|Begrenzt die Netzwerkbandbreite, die Bits für Hintergrund Übertragungen verwendet, während der Wartungs Tage und-Stunden. Mit Wartungsplänen wird die für Hintergrund Übertragungen verwendete Netzwerkbandbreite weiter eingeschränkt.<br/> Geben Sie eine Beschränkung an, die für Hintergrund Aufträge während eines Wartungs Zeitplans verwendet werden soll. Wenn Aufträge mit normaler Priorität z. b. derzeit auf einen Arbeitszeitplan auf 256 KBit/s beschränkt sind, können Sie die Netzwerkbandbreite normaler Prioritäts Aufträge auf 0 Kbit/s von 8:00 Uhr beschränken. auf 10:00 Uhr geändert. nach einem Wartungs Zeitplan.<br/>**Hinweis**: die Bandbreiten Limits, die für den Wartungs Zeitraum festgelegt sind, ersetzen alle Limits, die für die Arbeit und andere Zeitpläne definiert sind.|
|Enablebandwidthlimits<br/>Bits 4,0|Begrenzt die Netzwerkbandbreite, die Bits für Hintergrund Übertragungen während der Arbeit und arbeitsfreie Tage und Stunden verwendet. Der Arbeitszeitplan wird mit einem wöchentlichen Kalender definiert, der aus Wochentagen und Tagesstunden besteht. Alle Stunden und Tage, die nicht in einem Arbeitszeitplan definiert sind, gelten als nicht-Arbeitsstunden.<br/> Geben Sie eine Beschränkung an, die für Hintergrund Aufträge während eines Arbeitszeitplans verwendet werden soll. Beispielsweise können Sie die Netzwerkbandbreite von Aufträgen mit niedriger Priorität von 8:00 Uhr auf 128 Kbit/s begrenzen. bis 5:00 Uhr an Montag bis Freitag, und legen Sie dann das Limit für arbeitsfreie Stunden auf 512 Kbit/s fest.|


## <a name="related-topics"></a>Zugehörige Themen
* [Policy CSP](/windows/client-management/mdm/policy-configuration-service-provider)

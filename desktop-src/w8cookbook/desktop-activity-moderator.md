---
title: Desktopaktivitätenmoderator
description: Desktopaktivitätenmoderator
ms.assetid: F1C54DB0-0AFC-4A1B-9697-6CEB519C2663
keywords:
- Akku Lebensdauer
- verbundener Standby
- ten
- Drosselung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b8bb3d7925633d3feca8bb6ed5af191670af681
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "103730720"
---
# <a name="desktop-activity-moderator"></a>Desktopaktivitätenmoderator

## <a name="platform"></a>Plattform

**Clients** – Windows 8 


> [!Note]  
> Der Damm ist nur auf Windows 8-Client Computern vorhanden, die Connected Standby unterstützen. Der Damm ist auf Server-SKUs nicht vorhanden.

 

  

> [!Note]  
> Windows Store-Apps, die für Windows 8 erstellt wurden, werden vom-Staudamm nicht beeinträchtigt.

 

  
</dl>

## <a name="description"></a>BESCHREIBUNG

Unsere Kunden wechseln zu leichteren, kleineren und mobilen Plattformen, um Ihre computinganforderungen zu erfüllen. Im Rahmen der Umstellung auf mobile Geräte haben sich Benutzer zunehmend Sorgen um die Akku Lebensdauer Ihrer Geräte. Der Desktop Activity Moderator (Dam) ist eines von mehreren neuen Features in Windows 8, das entwickelt wurde, um eine konsistente, lange Akku Lebensdauer für Geräte sicherzustellen, die Connected Standby unterstützen.

Der verbundene Standbymodus tritt auf, wenn das Gerät eingeschaltet ist, der Bildschirm jedoch ausgeschaltet ist. In diesem Energiezustand ist das System technisch immer "on" (zur Unterstützung wichtiger Szenarien wie e-Mail, VoIP, Social Networking und Instant Messaging mit Windows Store-Apps). Dies entspricht dem Zustand, in dem sich ein Smartphone befindet, wenn der Benutzer den Netzschalter drückt.

Daher muss Software (einschließlich apps und Betriebssystem Software) während des verbundenen Standbymodus gut funktionieren. Der Damm wurde erstellt, um die Ausführung der Desktop-App auf eine Weise zu unterdrücken, die dem Ruhezustand (S3 auf ACPI-Geräten) ähnelt. Dies geschieht durch Anhalten oder Einschränken von Desktop Softwareprozessen auf dem gesamten System nach einem verbundenen Standby-Eintrag. Dadurch können Systeme, die verbundenen Standby unterstützen, eine minimierte Ressourcennutzung und eine lange, konsistente Akku Lebensdauer bereitzustellen und gleichzeitig den Windows Store-Apps die Bereitstellung der verbundenen Umgebungen ermöglichen

## <a name="details"></a>Details

Der Damm ist ein Kernelmodustreiber, der beim Systemstart geladen und initialisiert wird, wenn das System den verbundenen Standbymodus unterstützt. (Dies wird durch Auswerten von bestimmt, ob das Feld "AOAC" im System \_ \_Die von callntpowerinformation zurückgegebene Energie Funktionsstruktur ist auf true festgelegt.)

Wenn der Damm aktiviert ist und Ihr Desktop Prozess erstellt wird, fügt der Damm Ihren Prozess den vom System verwalteten Auftrags Objekten hinzu:

-   Wenn der Prozess in Sitzung 0 erstellt wurde, wird der Prozess einem Auftrags Objekt hinzugefügt, das der **Drosselung** unterliegt.
-   Wenn der Prozess in einer interaktiven Sitzung (Sitzung 1 oder höher) erstellt wurde, wird der Prozess einem Auftrags Objekt hinzugefügt, das der unter **Brechung** unterliegt.

> [!Note]  
> Für Windows 8 können Auftrags Objekte eingebettet werden. Dies bedeutet, dass die Nutzung von Auftrags Objekten durch den Staudamm nicht die vorhandene Verwendung von Auftrags Objekten einer APP beeinträchtigt.

 

Wenn der Bildschirm eingeschaltet ist, wird der Damm entzigiert und wirkt sich nicht auf Prozesse im System aus. Wenn sich das System im Standbymodus befindet, kann der Damm abhängig von der Aktivität im System Prozesse Drosseln oder aussetzen.

-   Bei Prozessen, die angehalten werden, werden alle Threads angehalten (unter Umständen nicht ausgeführt); der APP-Zustand (Prozess Speicher) wird beibehalten.
-   Prozesse, die dem Drosselungs Zeitraum zwischen angehalten und nicht angehalten (eine große Mehrheit der Zeit wird im angehaltenen Zustand aufgewendet)
    -   Beachten Sie, dass Windows möglicherweise auch erkennt, dass wichtige Aktivitäten auftreten, und die Einschränkung gedrosselt Dienste für längere Zeiträume während dieser Aktivität aufheben können.
    -   Beachten Sie außerdem, dass während des verbundenen Standbymodus Sensoren und Netzwerke möglicherweise nicht verfügbar sind. Daher sollten gedrosselte Prozesse so entworfen werden, dass Sie gegenüber schlechten Netzwerkbedingungen stabil sind (für die meisten Prozesse ist dies keine Änderung erforderlich).

Wenn die Unterbrechung der Unterbrechung aktiviert oder aufgehoben wird, löst die-Sperre die Übermittlung einer WM- \_ powerbroadcast-Nachricht an die Prozesse aus, die der Unterbrechung unterliegen, die für die Nachrichtenübermittlung (über API-Aufrufe oder Kompatibilitäts-Shim, weiter unten beschrieben) Nach einer Verzögerung von wenigen Sekunden hält der Staudamm den Prozess an.

Es gibt keine Benachrichtigungen, wenn die Drosselung von Dämmen aktiviert oder aufgehoben wird. Prozesse sollten nicht geändert werden. Prozesse funktionieren weiterhin, auch wenn Sie langsamer ausfallen.

## <a name="manifestation"></a>Ausstrahlung

Prozesse werden während des verbundenen Standbystatus häufig angehalten oder gedrosselt. Bei der Mehrzahl der angehaltenen apps sollte dies einem S3-/Fortsetzungs-oder S4-Ruhezustand/fortsetzen-Übergang sehr ähnlich sein. Zu den Manifestationen zählen u. a. Inkonsistenzen in der Betriebszeit/Laufzeit und die Zeit der Wall-Uhr, Inkonsistenzen im Zeit Geber Verhalten oder drastische Änderungen des Betriebssystem Zustands vor und nach dem aussetzen.

Unterbrechung und Drosselung werden als Einheit durchgeführt (alle untergeordneten Prozesse werden in Unison angehalten und nicht angehalten, und alle Prozesse, die gedrosselt werden können, werden gedrosselt, und die Drosselung erfolgt in Unison). Daher stellt die Kommunikation zwischen zwei angehaltenen Prozessen oder zwei gedrosselte Prozesse kein Problem dar.

Software, die auf Prozess übergreifender Kommunikation basiert, muss möglicherweise besondere Aspekte berücksichtigen:

-   **Kommunikation zwischen Prozessen in Sitzung 0 (gedrosselt) und Sitzung 1 + (** angehalten) – Beispiele sind Info leisten Symbole oder UI-Komponenten, die den aktuellen Dienststatus darstellen.
-   **Kommunikation zwischen Komponenten im Benutzermodus (Sitzung 0 oder 1) und Treibern (die weder eingeschränkt noch** angehalten wurden) – Beispiele hierfür sind Dienste, die im Auftrag eines Treibers funktionieren.

Wenn die prozessübergreifende Kommunikation in diesen Fällen nicht ordnungsgemäß behandelt wird, können apps nicht reagiert oder nicht reagieren (obwohl der Benutzer diese Auswirkung möglicherweise nicht direkt sieht, da der Bildschirm im verbundenen Standbymodus deaktiviert wird). In den meisten Fällen sollten Dienste und Treiber jedoch bereits so entwickelt werden, dass Sie für prozessübergreifende Kommunikationsprobleme robust sind.

Anbieter, die Software für das Internet erstellen oder davon abhängig sind, sollten berücksichtigen, wie sich die Prozessunterbrechung auf Verbindungs Lebensdauern und Handshakes auswirkt. Da die Netzwerk Konnektivität im verbundenen Standbymodus möglicherweise nicht verfügbar ist, sollten Entwickler der in Sitzung 0 erstellten Prozesse vor allem erkennen, wie sich die zeitweiligen Netzwerkverbindungen auf den Prozess auswirken.

## <a name="solution"></a>Lösung

Windows Store-Apps werden vom-Staudamm nicht beeinträchtigt. Wenn Ihre Desktop-app durch den Staudamm beeinträchtigt wird, können Sie Benachrichtigungen anfordern, bevor die Unterbrechung erfolgt (z. b. zum Speichern des Zustands oder zum Schließen von Netzwerkverbindungen), indem Sie eine der folgenden Methoden verwenden:

-   Wenn Ihre APP über ein Fenster (HWND) verfügt und Sie diese Benachrichtigungen über die Fenster Prozedur verarbeiten möchten, können Sie [registersuspendresumenotifizum](/windows/win32/api/winuser/nf-winuser-registersuspendresumenotification) registrieren für diese Nachrichten (oder [unregistersuspendresumenotifito](/windows/win32/api/winuser/nf-winuser-unregistersuspendresumenotification) Unregister) aufrufen. Sie können \_ \_ \_ das Handle für den Geräte Benachrichtigungsfenster im flags-Parameter verwenden und das HWND des Fensters in als Empfänger Parameter übergeben. Die empfangene Nachricht ist die WM- \_ powerbroadcast-Nachricht.
-   Wenn Ihre APP kein Fenster (HWND) hat oder Sie einen direkten Rückruf wünschen, rufen Sie [powerregistersuspendresumenotifiauf](/windows/win32/api/powerbase/nf-powerbase-powerregistersuspendresumenotification) , um sich für diese Nachrichten zu registrieren (oder [powerunregistersuspendresumenotifito](/windows/win32/api/powerbase/nf-powerbase-powerunregistersuspendresumenotification) Unregister). Sie müssen \_ \_ den Rückruf für die Geräte Benachrichtigung im flags-Parameter verwenden und einen Wert vom Typ "pdevice \_ Notify \_ subscribe Parameters" \_ im Parameter "Recipient" übergeben.
-   Wenn Ihre APP nicht neu kompiliert werden kann, können Sie diese WM- \_ powerbroadcast-Nachrichten über das [AppCompat-Toolkit](../win7appqual/application-compatibility-toolkit--act-.md) (mit dem promotedam-Shim) empfangen.

Die Suspend-Nachricht lautet WM \_ powerbroadcast mit wParam = PBT \_ apmsuspend. diese Nachricht wird gleichzeitig an alle in den System Vorgängen abgewicknten Prozesse übertragen. Ihre APP muss schnell und effizient auf dem anhaltepfad arbeiten. Das Timeout nach der Übertragungs Benachrichtigung erfolgt global, nicht pro Prozess, sodass der Prozess möglicherweise für Systemressourcen in Konflikt steht, wenn die in diesem Pfad erforderliche Arbeit sehr umfangreich ist.

Die Fortsetzung der Nachricht lautet WM \_ powerbroadcast mit wParam = PBT \_ apmresume. diese Nachricht wird nach einer Wiederaufnahme gleichzeitig an alle abgewicknten Prozesse übertragen. Die relative Zeit der Übermittlung an das System beenden aus dem verbundenen Standbymodus ist nicht garantiert.

Bei Kamera bezogenen Anwendungen müssen Anwendungen während der Unterbrechungs Benachrichtigung alle Verweise auf die Kamera freigeben (alle Aufzeichnungs Pipeline Objekte müssen heruntergefahren und verworfen werden).  Um einen möglichen Akku Ausgleich zu vermeiden, schließt der Windows-Kamera-Frame Server von Windows 10 RS3 + Systems alle Erfassungs Sitzungen, wenn die Anwendung die Unterbrechungs Benachrichtigung nicht ordnungsgemäß verarbeitet.  Dies hat den Nebeneffekt, dass sich die Aufzeichnungs Pipeline der Anwendung nicht mehr in einem funktionierenden Zustand befindet, wenn das System in den Standbymodus oder den S3/S4-Status versetzt wird.

## <a name="tests"></a>Tests

Testen Sie Ihre Software über verbundene Standby-Übergänge.

## <a name="resources"></a>Ressourcen

-   [Lösungen für die mobile Akku Lebensdauer für Windows 7](/previous-versions/windows/hardware/design/dn641606(v=vs.85))
-   [System \_ Energie \_ Funktionen](/windows/win32/api/winnt/ns-winnt-system_power_capabilities)
-   [Callntpowerinformation-Funktion](/windows/win32/api/powerbase/nf-powerbase-callntpowerinformation)
-   [Auftrags Objekte](../procthread/job-objects.md)
-   [Registersuspendresumenotifizierung](/windows/win32/api/winuser/nf-winuser-registersuspendresumenotification)
-   [Unregistersuspendresumenotifi](/windows/win32/api/winuser/nf-winuser-unregistersuspendresumenotification)
-   [Powerregistersuspendresumenotifi](/windows/win32/api/powerbase/nf-powerbase-powerregistersuspendresumenotification)
-   [Powerunregistersuspendresumenotifi](/windows/win32/api/powerbase/nf-powerbase-powerunregistersuspendresumenotification)
-   [AppCompat-Toolkit](../win7appqual/application-compatibility-toolkit--act-.md)

 

 
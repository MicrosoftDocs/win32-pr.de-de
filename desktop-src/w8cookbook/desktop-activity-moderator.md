---
title: Desktopaktivitätenmoderator
description: Desktopaktivitätenmoderator
ms.assetid: F1C54DB0-0AFC-4A1B-9697-6CEB519C2663
keywords:
- Akkulebensdauer
- Verbundener Standbymodus
- Aussetzung
- Drosselung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b465bbb377a06fdad50d04d5fcf788cb2e687fdf5db852125e4143fd971773d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815420"
---
# <a name="desktop-activity-moderator"></a>Desktopaktivitätenmoderator

## <a name="platform"></a>Plattform

**Clients** – Windows 8 


> [!Note]  
> Das STANDBY ist nur auf Windows 8 Clientcomputern vorhanden, die den verbundenen Standbymodus unterstützen. DIE NOTE ist auf Server-SKUs nicht vorhanden.

 

  

> [!Note]  
> Windows Store Apps, die für Windows 8 erstellt wurden, sind nicht von DER -Sperre betroffen.

 

  
</dl>

## <a name="description"></a>Beschreibung

Unsere Kunden entwickeln sich auf einfachere, kleinere und mobilere Plattformen um, um ihre Computinganforderungen zu erfüllen. Im Rahmen der Umstellung auf mobile Geräte haben sich Benutzer zunehmend Gedanken über die Akkulaufzeit ihrer Geräte machen. Desktop Activity Moderator (CSV) ist eines von mehreren neuen Features in Windows 8, die eine konsistente, lange Akkulebensdauer für Geräte gewährleisten, die den verbundenen Standbymodus unterstützen.

Der verbundene Standbymodus tritt auf, wenn das Gerät eingeschaltet ist, der Bildschirm jedoch ausgeschaltet ist. In diesem Energiezustand ist das System technisch immer "eingeschaltet" (um wichtige Szenarien wie E-Mail, VoIP, soziale Netzwerke und Instant Messaging mit Windows Store-Apps zu unterstützen). Dies entspricht dem Zustand, in dem sich ein Smartphone befindet, wenn der Benutzer auf den Netzschalter drückt.

Daher muss sich Software (einschließlich Apps und Betriebssystemsoftware) während des verbundenen Standbymodus gut verhalten. Die EDITIONS-App wurde erstellt, um die Ausführung von Desktop-Apps auf ähnliche Weise zu unterdrücken wie den Standbyzustand (S3 auf ACPI-Geräten). Dies geschieht durch Anhalten oder Drosseln von Desktopsoftwareprozessen im gesamten System nach dem verbundenen Standbyeintrag. Auf diese Weise können Systeme, die den verbundenen Standbymodus unterstützen, eine minimierte Ressourcennutzung und eine lange, konsistente Akkulaufzeit bereitstellen und gleichzeitig Windows Store Apps ermöglichen, die von ihnen zugesicherten verbundenen Funktionen bereitzustellen.

## <a name="details"></a>Details

DER STANDBY ist ein Kernelmodustreiber, der beim Systemstart geladen und initialisiert wird, wenn das System den verbundenen Standbymodus unterstützt. (Dies wird bestimmt, indem ausgewertet wird, ob das AOAC-Feld im SYSTEM \_ Die \_ von CallNtPowerInformation zurückgegebene POWER CAPABILITIES-Struktur ist auf TRUE festgelegt.

Wenn das EDITIONS-Objekt aktiviert ist und Ihr Desktopprozess erstellt wird, fügt DER PROZESS den vom System verwalteten Auftragsobjekten hinzu:

-   Wenn der Prozess in Sitzung 0 erstellt wurde, fügt DER PROZESS einem Auftragsobjekt hinzu, das einer **Drosselung** unterliegt.
-   Wenn der Prozess in einer interaktiven Sitzung (Sitzung 1 oder höher) erstellt wurde, fügt DER PROZESS einem Auftragsobjekt hinzu, das **unterbrochen werden** muss.

> [!Note]  
> Für Windows 8 können Auftragsobjekte geschachtelt werden. Dies bedeutet, dass die Verwendung von Auftragsobjekten durch die VERWENDUNG von AUFTRAGSOBJEKTEN durch die VERWENDUNG von Auftragsobjekten durch eine App nicht beeinträchtigt wird.

 

Wenn der Bildschirm eingeschaltet ist, wird der SCREEN ausgesperrt und wirkt sich nicht auf Prozesse auf dem System aus. Wenn sich das System im verbundenen Standbymodus befindet, kann DIEs abhängig von der Aktivität des Systems dazu führen, dass DIE PROZESSE gedrosselt oder angehalten werden.

-   Bei Prozessen, die angehalten werden, sind alle Threads angehalten (unter keinen Umständen zulässig). App-Status (Prozessspeicher) wird beibehalten
-   Prozesse, die einem Drosselungszyklus zwischen angehalten und nicht verwendet unterliegen (ein großteil der Zeit wird im Angehalten-Zustand aufgewendet).
    -   Beachten Sie, dass Windows möglicherweise auch erkennen, dass kritische Aktivitäten ausgeführt werden und gedrosselte Dienste während dieser Aktivität für längere Zeit nicht verwendet werden.
    -   Beachten Sie außerdem, dass Sensoren und Netzwerke im verbundenen Standbymodus möglicherweise nicht verfügbar sind, sodass gedrosselte Prozesse so entworfen werden sollten, dass sie gegen schlechte Netzwerkbedingungen resilient sind (für die meisten Prozesse erfordert dies keine Änderung).

Wenn die SUSPEND-Unterbrechung aktiviert oder aufgehoben wird, löst DER DURCH die Übermittlung einer WM POWERBROADCAST-Nachricht an die Prozesse aus, für die eine Unterbrechung erforderlich ist, die sich für \_ die Nachrichtenübermittlung entschieden haben (per API-Aufruf oder Kompatibilitätss shim, wie weiter unten beschrieben). Nach einigen Sekunden Verzögerung wird der Prozess von SUSPEND angehalten.

Es gibt keine Benachrichtigungen, wenn die EINSCHRÄNKUNGsdrosselung aktiv ist oder nicht mehr verwendet wird. Prozesse sollten nicht geändert werden müssen. -Prozesse funktionieren weiterhin, wenn auch mit einer langsameren Rate.

## <a name="manifestation"></a>Manifestation

Prozesse werden während des verbundenen Standbyzustands häufig angehalten oder gedrosselt. Für die meisten angehaltenen Apps sollte dies sehr ähnlich wie ein Übergang vom 3. Anhalten/Fortsetzen oder S4-Ruhezustand/Wiederaufnahme sein. Zu den Schwankungen zählen u. a. Inkonsistenzen in Betriebszeit/Laufzeit im Vergleich zur Uhr, Inkonsistenzen im Timerverhalten oder drastische Änderungen des Betriebssystemzustands vor und nach Abschluss des Anhaltens.

Das Anhalten und Drosseln erfolgt als Einheit (alle suspendierbaren Prozesse werden angehalten und nicht zusammengehörig verwendet, und alle Prozesse, die gedrosselt werden können, werden gedrosselt und nicht zusammengedrosselt), sodass die Kommunikation zwischen zwei angehaltenen Prozessen oder zwei gedrosselten Prozessen kein Problem darstellt.

Software, die auf prozessübergreifender Kommunikation basiert, muss möglicherweise besonders berücksichtigt werden:

-   **Kommunikation zwischen Prozessen in Sitzung 0 (gedrosselt) und Sitzung 1+ (angehalten):** Beispiele hierfür sind Taskleistensymbole oder Benutzeroberflächenkomponenten, die den aktuellen Dienstzustand darstellen.
-   **Kommunikation zwischen Komponenten im Benutzermodus (Sitzung 0 oder 1) und Treibern (die weder gedrosselt noch angehalten sind)** – Beispiele hierfür sind Dienste, die im Auftrag eines Treibers funktionieren.

Wenn die prozessübergreifende Kommunikation in diesen Fällen nicht ordnungsgemäß verarbeitet wird, können Apps hängen bleiben oder nicht reagieren (obwohl der Benutzer diese Auswirkung möglicherweise nicht direkt erkennt, da der Bildschirm im verbundenen Standbymodus ausgeschaltet ist). In den meisten Fällen sollten Dienste und Treiber jedoch bereits entwickelt werden, um robust gegen prozessübergreifende Kommunikationsprobleme zu sein.

Anbieter, die Software für das Web erstellen oder davon abhängig sind, sollten berücksichtigen, wie sich das Anhalten des Prozesses auf die Lebensdauer von Verbindungen und Handshakes auswirkt. Darüber hinaus sollten Entwickler von Prozessen, die in Sitzung 0 erstellt wurden, besonders wissen, wie sich zeitweilige Netzwerkverbindungen auf den Prozess auswirken, da die Netzwerkkonnektivität im Modus "Verbundener Standbymodus" möglicherweise nicht verfügbar ist.

## <a name="solution"></a>Lösung

Windows Store Apps sind nicht von DER ENTE betroffen. Wenn Ihre Desktop-App von DER ENERGIESPARE betroffen ist, können Sie mit einer der folgenden Methoden Benachrichtigungen anfordern, bevor die Unterbrechung ausgeführt wird (z. B. um den Zustand zu speichern oder Netzwerkverbindungen zu schließen):

-   Wenn Ihre App über ein Fenster (HWND) verfügt und Sie diese Benachrichtigungen über Ihre Fensterprozedur behandeln möchten, rufen Sie [RegisterSuspendResumeNotification](/windows/win32/api/winuser/nf-winuser-registersuspendresumenotification) auf, um sich für diese Nachrichten zu registrieren (oder [UnregisterSuspendResumeNotification,](/windows/win32/api/winuser/nf-winuser-unregistersuspendresumenotification) um die Registrierung zu aufheben). Sie können DEVICE NOTIFY WINDOW HANDLE im Flags-Parameter verwenden und den \_ \_ \_ HWND Ihres Fensters als Recipient-Parameter übergeben. Die empfangene Nachricht ist die WM \_ POWERBROADCAST-Nachricht.
-   Wenn Ihre App kein Fenster (HWND) hat oder Sie einen direkten Rückruf wünschen, rufen Sie [PowerRegisterSuspendResumeNotification](/windows/win32/api/powerbase/nf-powerbase-powerregistersuspendresumenotification) auf, um sich für diese Nachrichten zu registrieren (oder [PowerUnregisterSuspendResumeNotification,](/windows/win32/api/powerbase/nf-powerbase-powerunregistersuspendresumenotification) um die Registrierung zu aufheben). Sie müssen DEVICE \_ NOTIFY \_ CALLBACK im Flags-Parameter verwenden und einen Wert vom Typ PDEVICE \_ NOTIFY SUBSCRIBE PARAMETERS im \_ \_ Recipient-Parameter übergeben.
-   Wenn Ihre App nicht neu kompiliert werden kann, können Sie diese \_ WM-POWERBROADCAST-Nachrichten über das [AppCompat-Toolkit](../win7appqual/application-compatibility-toolkit--act-.md) (mithilfe des PromoteVAS-Shims) empfangen.

Die Meldung zum Anhalten ist WM \_ POWERBROADCAST mit wParam=PBT \_ APMSUSPEND. Diese Nachricht wird gleichzeitig an alle prozesse im System übertragen. Ihre App muss alle Aufgaben auf dem Unterbrechungspfad schnell und effizient ausführen. Das Timeout nach der Broadcastbenachrichtigung ist global und nicht pro Prozess, sodass Ihr Prozess möglicherweise um Systemressourcen in Abkämmung steht, wenn die in diesem Pfad erforderliche Arbeit umfangreich ist.

Die Fortsetzungsnachricht ist WM \_ POWERBROADCAST mit wParam=PBT \_ APMRESUME. Diese Nachricht wird nach einem Fortsetzen gleichzeitig an alle angemeldeten Prozesse übertragen. Die relative Zeit der Übermittlung an das System aus dem verbundenen Standbymodus ist nicht garantiert.

Bei kamerabezogenen Anwendungen müssen Anwendungen beim Übergang des Energiezustands während der Unterbrechungsbenachrichtigung alle Verweise auf die Kamera freigeben (alle Aufzeichnungspipelineobjekte müssen heruntergefahren und verworfen werden).  Um einen möglichen Akkuladezustand zu vermeiden, schließt Windows-Kamera Frame Server-Dienst auf Windows 10 RS3+-Systemen alle Erfassungssitzungen, wenn die Anwendung die Unterbrechungsbenachrichtigung nicht ordnungsgemäß verarbeitet.  Dies hat den Nebeneffekt, dass die Erfassungspipeline der Anwendung nicht mehr funktionsfähig ist, wenn das System aus dem Standby- oder S3/S4-Zustand ausfällt.

## <a name="tests"></a>Tests

Testen Sie Ihre Software über verbundene Standbyübergänge hinweg.

## <a name="resources"></a>Ressourcen

-   [Mobile Battery Life-Lösungen für Windows 7](/previous-versions/windows/hardware/design/dn641606(v=vs.85))
-   [\_ \_ SYSTEMLEISTUNGSFUNKTIONEN](/windows/win32/api/winnt/ns-winnt-system_power_capabilities)
-   [CallNtPowerInformation-Funktion](/windows/win32/api/powerbase/nf-powerbase-callntpowerinformation)
-   [Auftragsobjekte](../procthread/job-objects.md)
-   [RegisterSuspendResumeNotification](/windows/win32/api/winuser/nf-winuser-registersuspendresumenotification)
-   [UnregisterSuspendResumeNotification](/windows/win32/api/winuser/nf-winuser-unregistersuspendresumenotification)
-   [PowerRegisterSuspendResumeNotification](/windows/win32/api/powerbase/nf-powerbase-powerregistersuspendresumenotification)
-   [PowerUnregisterSuspendResumeNotification](/windows/win32/api/powerbase/nf-powerbase-powerunregistersuspendresumenotification)
-   [AppCompat-Toolkit](../win7appqual/application-compatibility-toolkit--act-.md)

 

 
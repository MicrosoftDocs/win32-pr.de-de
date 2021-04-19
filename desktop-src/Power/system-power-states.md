---
description: Für den Benutzer scheint das System entweder ein-oder ausgeschaltet zu sein.
ms.assetid: 3d897a88-125e-457f-9ea7-ac2056b0767a
title: System Energiestatus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f18cf6323ae852a871869066a2e9baa2860e6978
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349214"
---
# <a name="system-power-states"></a>System Energiestatus

Für den Benutzer scheint das System entweder ein-oder ausgeschaltet zu sein. Es sind keine weiteren erkennbaren Zustände vorhanden. Das System unterstützt jedoch mehrere Energiezustände, die den in der Advanced Configuration and Power Interface (ACPI)-Spezifikation definierten Energiezuständen entsprechen. Es gibt auch Variationen dieser Zustände, z. b. hybride Standbymodus und schneller Start. In diesem Thema werden diese Zustände vorgestellt, und es wird beschrieben, wie Sie miteinander in Beziehung stehen.

> [!NOTE]
> Systemintegratoren und Entwickler, die Treiber oder Anwendungen mit einem Systemdienst erstellen, sollten besonders vorsichtig auf Probleme mit der Treiber Qualität, z. b. Speicher Verluste, achten. Obwohl die Treiber Qualität immer wichtig war, kann die Betriebszeit zwischen Kernel Neustarts erheblich länger sein als in früheren Versionen des Betriebssystems, da bei vom Benutzer initiierten Ruhe-und Herunterfahr Vorgängen der Kernel, die Treiber und die Dienste beibehalten und wieder hergestellt und nicht neu gestartet werden.

 

In der folgenden Tabelle sind die ACPI-Strom Zustände vom höchsten bis zum niedrigsten Stromverbrauch aufgelistet.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Betriebszustand</th>
<th>ACPI-Status</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>In Bearbeitung<br/></td>
<td>S0<br/></td>
<td>Das System ist vollständig verwendbar. Hardware Komponenten, die nicht verwendet werden, können Energie sparen, indem Sie einen niedrigeren Energiezustand eingeben.<br/></td>
</tr>
<tr class="even">
<td>Standby<br/> (Moderner Standby-Modus)<br/></td>
<td>S0 im Leerlauf<br/></td>
<td>Einige SOC-Systeme unterstützen einen Energiesparmodus, der als <a href="/windows-hardware/design/device-experiences/modern-standby">moderner Standby</a>bezeichnet wird. In diesem Zustand kann das System sehr schnell von einem Energiespar Status in den Status "Hochenergie" wechseln, um schnell auf Hardware-und Netzwerkereignisse reagieren zu können. Systeme, die modern Standby unterstützen, verwenden nicht S1-S3.<br/></td>
</tr>
<tr class="odd">
<td>Standby<br/></td>
<td>S1<br/> S2<br/> S3<br/></td>
<td>Das System ist anscheinend deaktiviert. In diesen Zuständen verbrauchte Stromversorgung (S1-S3) ist kleiner als S0 und mehr als S4; S3 beansprucht weniger Energie als S2, und S2 beansprucht weniger Energie als S1. Systeme unterstützen in der Regel einen dieser drei Zustände, nicht alle drei.<br/> In diesen Zuständen (S1-S3) wird flüchtiger Arbeitsspeicher aktualisiert, um den Systemstatus zu erhalten. Einige Komponenten bleiben eingeschaltet, sodass der Computer aus der Eingabe von der Tastatur, dem LAN oder einem USB-Gerät aktiviert werden kann.<br/> Der <em>hybride</em>Standbymodus, der auf Desktops verwendet wird, ist der Ort, an dem ein System eine Ruhe Zustands Datei mit S1 S3 verwendet. Die Ruhe Zustands Datei speichert den Systemstatus für den Fall, dass das System im Standbymodus Energie verliert.<br/>
<blockquote>
[!Note]<br />
SOC-Systeme, die den modernen Standby unterstützen (der Energiesparmodus im Leerlauf), verwenden nicht S1-S3.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td>Ruhezustand<br/></td>
<td>S4<br/></td>
<td>Das System ist anscheinend deaktiviert. Der Stromverbrauch wird auf die niedrigste Ebene reduziert. Das System speichert den Inhalt des flüchtigen Speichers in einer Ruhe Zustands Datei, um den Systemstatus zu erhalten. Einige Komponenten bleiben eingeschaltet, sodass der Computer aus der Eingabe von der Tastatur, dem LAN oder einem USB-Gerät aktiviert werden kann. Der Arbeitskontext kann wieder hergestellt werden, wenn er auf nicht flüchtigen Medien gespeichert ist. <br/> Der <em>schnelle Start</em> ist der Ort, an dem der Benutzer abgemeldet wird, bevor die Ruhe Zustands Datei erstellt wird. Dies ermöglicht eine kleinere Ruhe Zustands Datei und eignet sich besser für Systeme mit weniger Speicherfunktionen.<br/></td>
</tr>
<tr class="odd">
<td>Soft ausschalten<br/></td>
<td>S5<br/></td>
<td>Das System ist anscheinend deaktiviert. Dieser Status besteht aus einem vollständigen Herunterfahren und einem Start Zyklus.<br/></td>
</tr>
<tr class="even">
<td>Mechanisch ausgeschaltet<br/></td>
<td>G3<br/></td>
<td>Das System ist vollständig ausgeschaltet und beansprucht keine Stromversorgung. Das System wird erst nach einem vollständigen Neustart wieder in den Arbeitszustand zurückversetzt.<br/></td>
</tr>
</tbody>
</table>



 

Die [**System \_ Energie \_ Zustands**](/windows/desktop/api/WinNT/ne-winnt-system_power_state) -Enumeration definiert Werte, die zum Angeben von System Energiezuständen verwendet werden.

## <a name="working-state-s0"></a>Arbeitszustand (S0)

Während des Arbeits Zustands ist das System aktiv und wird ausgeführt. In einfachen Worten ist das Gerät "on". Unabhängig davon, ob der Bildschirm ein-oder ausgeschaltet ist, befindet sich das Gerät in einem vollständigen Betriebsstatus. Um Energie zu sparen, insbesondere auf Geräten mit Akku Betrieb, empfehlen wir dringend, Hardwarekomponenten herunter zu schalten, wenn Sie nicht verwendet werden.

> [!IMPORTANT]
> Schalten Sie Hardwarekomponenten immer dann ein, wenn Sie nicht verwendet werden, unabhängig vom Zustand. Der niedrige Stromverbrauch ist ein wichtiger Aspekt für Consumer mobiler Geräte.

 

## <a name="sleep-state-modern-standby"></a>Ruhezustand (moderner Standby-Modus)

Im Modus "S0 Low-Power Idle" des Arbeits Zustands, auch als [moderner Standby](/windows-hardware/design/device-experiences/modern-standby)bezeichnet, bleibt das System teilweise funktionsfähig. Während des modernen Standbymodus kann das System immer auf dem neuesten Stand bleiben, wenn ein geeignetes Netzwerk verfügbar ist, und auch aktivieren, wenn Echt Zeit Maßnahmen erforderlich sind, wie z. b. die Wartung des Betriebssystems. Moderner Standby wird deutlich schneller als S1-S3 aktiviert. Weitere Informationen finden Sie unter [modern Standby](/windows-hardware/design/device-experiences/modern-standby).

> [!Note]  
> Der moderne Standby-Modus ist nur auf einigen SOC-Systemen verfügbar. Wenn es unterstützt wird, wird S1-S3 vom System nicht unterstützt.

 

## <a name="sleep-state-s1-s3"></a>Ruhezustand (S1-S3)

Das System wechselt basierend auf einer Reihe von Kriterien in den Standbymodus, einschließlich Benutzer-oder Anwendungs Aktivitäten und Einstellungen, die der Benutzer auf der **Power &** -standbyseite der App " **Einstellungen** " festlegt. Standardmäßig verwendet das System den niedrigsten Energiesparmodus, der von allen aktivierten Aktivierungs Geräten unterstützt wird. Weitere Informationen darüber, wie das System festlegt, wann in den Standbymodus gewechselt wird, finden Sie unter System Standby- [Kriterien](system-sleep-criteria.md)

Bevor das System in den Standbymodus wechselt, bestimmt es den entsprechenden Ruhezustand, benachrichtigt Anwendungen und Treiber über den ausstehenden Übergang und wechselt dann in den Ruhezustand. Im Fall eines kritischen Übergangs, z. b. wenn der Schwellenwert für die kritische Akkukapazität erreicht wird, werden Anwendungen und Treiber vom System nicht benachrichtigt. Anwendungen müssen darauf vorbereitet werden, und die entsprechende Aktion wird ausgeführt, wenn das System in den Arbeitszustand zurückkehrt.

In diesen Zuständen (S1-S3) wird flüchtiger Arbeitsspeicher aktualisiert, um den Systemstatus zu erhalten. Einige Komponenten bleiben eingeschaltet, sodass der Computer aus der Eingabe von der Tastatur, dem LAN oder einem USB-Gerät aktiviert werden kann.

Das System wird auch als Reaktion auf eine Benutzeraktivität oder ein Reaktivierungs Ereignis, das von einer Anwendung definiert ist, im Standbymodus aktiviert. Weitere Informationen finden Sie unter [System Aktivierungs Ereignisse](system-wake-up-events.md). Die Zeitspanne, die das System für die Aktivierung benötigt, hängt von dem Ruhezustand ab, von dem aus die Aktivierung erfolgt. Das System nimmt aufgrund der zusätzlichen Arbeit, die die Hardware möglicherweise erledigen muss, mehr Zeit in Anspruch (S3) als in einem Zustand mit niedrigerer Leistung (S1), da die Hardware möglicherweise nicht mehr benötigt wird (stabilisieren der Netzteil, Neuinitialisierung des Prozessors usw.).

> [!Caution]  
> Beim Aufrufen von [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate)sollten Sie den Wert " **es \_ awaymode \_ Required** " nur verwenden, wenn dies für Medienanwendungen absolut notwendig ist, die das System benötigen, um Hintergrundaufgaben auszuführen, z. b. das Aufzeichnen von Fernsehinhalten oder das Streaming von Medien auf anderen Geräten, während das System scheinbar im Ruhezustand ist Anwendungen, für die keine kritische Hintergrundverarbeitung erforderlich ist oder die auf tragbaren Computern ausgeführt werden, sollten den Modus "Weg" nicht aktivieren, da dadurch die Stromversorgung des Systems durch Eingabe von "true" verhindert wird.

 

### <a name="hybrid-sleep-s1-s3--hibernation-file"></a>Hybrider Standbymodus (S1-S3 und Ruhe Zustands Datei)

Der *hybride* Standbymodus ist ein spezieller Zustand, bei dem es sich um eine Kombination aus Standby-und Ruhe Zustands Zuständen handelt, wenn ein System eine Ruhe Zustands Datei mit S1-S3 verwendet. Es ist nur auf einigen Systemen verfügbar. Wenn diese Option aktiviert ist, schreibt das System eine Ruhe Zustands Datei, wechselt jedoch in einen Hochenergie Spar Modus. Wenn die Stromversorgung unterbrochen wird, während das System ausfällt, wird das System aus dem Ruhezustand aktiviert, was länger dauert, aber den Systemzustand des Benutzers wiederherstellt.

## <a name="hibernate-state-s4"></a>Ruhezustand (S4)

Windows verwendet den Ruhezustand, um eine schnelle Start Funktion bereitzustellen. Wenn Sie verfügbar ist, wird Sie auch auf mobilen Geräten verwendet, um die verwendbare Akku Lebensdauer eines Systems zu erweitern, indem ein Mechanismus zum Speichern des gesamten Benutzer Zustands vor dem Herunterfahren des Systems bereitgestellt wird. Bei einem Ruhezustand wird der gesamte Inhalt des Arbeitsspeichers in eine Datei auf dem primären Systemlaufwerk (der Ruhe Zustands *Datei*) geschrieben. Dadurch wird der Status des Betriebssystems, der Anwendungen und der Geräte beibehalten. Wenn der kombinierte Speicherbedarf den gesamten physischen Arbeitsspeicher beansprucht, muss die Ruhe Zustands Datei groß genug sein, um sicherzustellen, dass genügend Speicherplatz vorhanden ist, um den gesamten Inhalt des physischen Speichers zu speichern. Da Daten in einen nicht flüchtigen Speicher geschrieben werden, benötigt DRAM keine selbst Aktualisierung und kann ausgeschaltet werden. Dies bedeutet, dass der Energieverbrauch des Ruhe Zustands sehr gering ist, fast identisch mit dem Ausschalten.

Während eines vollständigen herunter Fahrens und Starts (S5) wird die gesamte Benutzersitzung beim nächsten Start abgebrochen und neu gestartet. Im Gegensatz dazu wird die Benutzersitzung während eines Ruhe Zustands (S4) geschlossen, und der Benutzer Zustand wird gespeichert.

### <a name="fast-startup-reduced-hibernation-file"></a>Schneller Start (reduzierte Ruhe Zustands Datei)

Beim *schnellen Start* handelt es sich um eine Art von Herunterfahren, bei der eine Ruhe Zustands Datei zum Beschleunigen des nachfolgenden Starts verwendet wird. Während dieser Art des herunter Fahrens wird der Benutzer vor der Erstellung der Ruhe Zustands Datei abgemeldet. Der schnelle Start ermöglicht eine kleinere Ruhe Zustands Datei und eignet sich besser für Systeme mit weniger Speicherfunktionen. Weitere Informationen finden Sie unter Ruhe Zustands [Dateitypen](#hibernation-file-types).

Wenn Sie den schnellen Start verwenden, wird dem Benutzer das System so angezeigt, als ob das vollständige Herunterfahren (S5) erfolgt ist, obwohl das System tatsächlich S4 durchlaufen hat. Dazu gehört auch die Reaktion des Systems auf Geräte Aktivierungs Alarme.

Beim schnellen Start werden Benutzersitzungen protokolliert, aber der Inhalt des Kernels (Sitzung 0) wird auf die Festplatte geschrieben. Dies ermöglicht einen schnelleren Start.

Um Programm gesteuert ein schnelles Herunterfahren im Startmenü zu initiieren, müssen Sie die Funktion [**InitiateShutdown**](/windows/desktop/api/winreg/nf-winreg-initiateshutdowna) mit dem **\_ Hybrid** -Flag Herunterfahren oder der [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) -Funktion mit dem EWX-Flag für **\_ Hybrid \_ Shutdown** Herunterfahren abrufen.

> [!Note]  
> Ab Windows 8 ist der schnelle Start der Standard Übergang, wenn ein System heruntergefahren wird. Ein vollständiges Herunterfahren (S5) erfolgt, wenn ein Systemneustart angefordert wird (oder eine Anwendung eine Shutdown-API aufruft).

 

### <a name="entering-hibernation"></a>Wechsel in den Ruhezustand

Wenn eine Ruhe Zustands Anforderung erfolgt, treten die folgenden Schritte auf, wenn das System in den Ruhezustand wechselt:

1.  Apps und Dienste werden benachrichtigt
2.  Treiber werden benachrichtigt
3.  Benutzer-und Systemstatus werden in einem komprimierten Format auf dem Datenträger gespeichert.
4.  Die Firmware wird benachrichtigt.

> [!Note]  
> Ab Windows 8 werden alle Kerne im System verwendet, um die Daten im Arbeitsspeicher zu komprimieren und auf den Datenträger zu schreiben.

 

Um einen Ruhe Zustands Wechsel Programm gesteuert zu initiieren, müssen Sie die Funktion [**SetSuspendState**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) aufrufen.

### <a name="resuming-from-hibernation"></a>Fortsetzen aus dem Ruhezustand

Wenn ein System aus dem Ruhezustand wieder aufgenommen wird.

Wenn ein System eingeschaltet ist, treten die folgenden Schritte auf, wenn das System aus dem Ruhezustand wieder aufgenommen wird.

1.  System Beitrag
2.  Der System Arbeitsspeicher wird dekomprimiert und aus der Ruhe Zustands Datei wieder hergestellt.
3.  Geräte Initialisierung
4.  Treiber werden in dem Zustand wieder hergestellt, in dem Sie vor dem Ruhezustand waren.
5.  Dienste werden in dem Zustand wieder hergestellt, in dem Sie vor dem Ruhezustand waren.
6.  System wird für die Anmeldung verfügbar.

Eine Wiederaufnahme aus dem Ruhezustand beginnt mit einem System Beitrag, der mit dem Herunterfahren von S5 vergleichbar ist. Der Betriebssystem-Start-Manager bestimmt, dass eine Fortsetzung aus dem Ruhezustand erforderlich ist, indem eine gültige Ruhe Zustands Datei erkannt wird. Anschließend wird das System angewiesen, den Vorgang fortzusetzen und den Inhalt des Arbeitsspeichers und aller Architektur Register wiederherzustellen. Im Fall einer Fortsetzung aus dem Ruhezustand wird der Inhalt des System Arbeitsspeichers vom Datenträger eingelesen, entpackt und wieder hergestellt, wobei das System in den Zustand versetzt wird, in dem es sich in dem Ruhezustand befand. Nachdem der Arbeitsspeicher wieder hergestellt wurde, werden die Geräte neu gestartet, der Computer wechselt in den Zustand "wird ausgeführt", der für die Anmeldung bereit ist.

> [!Note]  
> Während einer Wiederaufnahme aus dem Ruhezustand werden Treiber und Dienste benachrichtigt, aber nicht neu gestartet. Sie werden nur in dem Zustand wieder hergestellt, in dem Sie vor dem Ruhezustand waren.

 

### <a name="hibernation-file-types"></a>Ruhe Zustands Dateitypen

Ruhe Zustands Dateien werden für den hybriden Standbymodus, den schnellen Start und den Standard-Ruhezustand (weiter oben beschrieben) verwendet. Es gibt zwei Typen, die sich nach Größe unterscheiden, eine vollständige und reduzierte Größe der Ruhe Zustands Datei. Nur beim schnellen Start kann eine reduzierte Ruhe Zustands Datei verwendet werden.



| Ruhe Zustands Dateityp | Standardgröße           | Unterstützt...                           |
|-----------------------|------------------------|---------------------------------------|
| Vollständig                  | 40% des physischen Speichers | Ruhezustand, hybride Standbymodus, schneller Start |
| Gerten               | 20% des physischen Arbeitsspeichers | schneller Start                          |



 

Um den Typ der verwendeten Ruhe Zustands Datei zu überprüfen oder zu ändern, führen Sie das **powercfg.exe** -Hilfsprogramm aus. In den folgenden Beispielen wird veranschaulicht, wie. Wenn Sie hierzu weitere Informationen benötigen, führen Sie `powercfg /? hibernate` aus.



|                                                                         |                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beispiel                                                                 | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                        |
| `powercfg /a`<br/>                                                | **Überprüfen Sie den Dateityp des Ruhe Zustands.** Wenn eine vollständige Ruhe Zustands Datei verwendet wird, ist der Status "Ruhezustand" eine verfügbare Option. Wenn eine reduzierte Ruhe Zustands Datei verwendet wird, werden die Ergebnisse als Ruhezustand nicht unterstützt. Wenn das System nicht über eine Ruhe Zustands Datei verfügt, werden die Ergebnisse als "Ruhezustand" nicht aktiviert.<br/> |
| `powercfg /h /type full`<br/>                                     | **Ändern Sie den Dateityp für den Ruhezustand in vollständig.** Dies wird nicht für Systeme mit weniger als 32 GB Speicher empfohlen.<br/>                                                                                                                                                                                                                        |
| `powercfg /h /type reduced`<br/>                                  | **Ändern Sie den Dateityp für den Ruhezustand in reduziert.** Wenn der Befehl "der Parameter ist falsch" zurückgibt, sehen Sie sich das folgende Beispiel an.<br/>                                                                                                                                                                                                        |
| `powercfg /h /size 0`<br/> `powercfg /h /type reduced`<br/> | **Ändern Sie den Dateityp für den Ruhezustand in "reduziert"** Wenn die Ruhe Zustands Datei auf eine benutzerdefinierte Größe größer als 40% festgelegt ist, müssen Sie zuerst die Größe der Datei auf NULL festlegen. Wiederholen Sie dann die reduzierte Konfiguration.<br/>                                                                                                                       |



 

## <a name="soft-off-state-s5"></a>Soft-Off-Zustand (S5)

Der weiche Zustand ist, wenn das System ohne eine Ruhe Zustands Datei vollständig heruntergefahren wird. Soft off wird auch als "vollständiges Herunterfahren" bezeichnet. Während eines vollständigen herunter Fahrens und Starts wird die gesamte Benutzersitzung beim nächsten Start abgebrochen und neu gestartet. Folglich dauert ein Start/Start mit diesem Zustand erheblich länger als S1-S4. Ein vollständiges Herunterfahren (S5) erfolgt, wenn ein Systemneustart angefordert wird (oder eine Anwendung eine Shutdown-API aufruft).

## <a name="mechanical-off-state-g3"></a>Zustand "mechanisch ausgeschaltet" (G3)

In diesem Zustand ist das System vollständig ausgeschaltet und beansprucht keine Stromversorgung. Das System wird erst nach einem vollständigen Neustart wieder in den Arbeitszustand zurückversetzt.

## <a name="wake-on-lan-behavior"></a>Wake-on-LAN-Verhalten

Die Funktion Wake-on-LAN (WOL) aktiviert den Computer in einem niedrigen Energiezustand, wenn ein Netzwerkadapter ein WOL-Ereignis erkennt (in der Regel ein speziell konstruiertes Ethernet-Paket).

WOL wird aus dem Standbymodus (S3) oder Ruhezustand (S4) unterstützt. Dies wird nicht unterstützt, wenn der schnelle Start oder das weiche Herunterfahren (S5) beendet wird. NICs sind in diesen Zuständen nicht für die Aktivierung aktiviert, da die Benutzer nicht erwarten, dass Ihre Systeme selbst aktiviert werden.

> [!Note]  
> WOL wird von Soft Off (S5) nicht offiziell unterstützt. Allerdings unterstützt das BIOS auf einigen Systemen möglicherweise die Aufrüsten von NICs für Wake-on, auch wenn Windows nicht an dem Prozess beteiligt ist.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Energie Verwaltung](about-power-management.md)
</dt> </dl>

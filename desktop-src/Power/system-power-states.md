---
description: Für den Benutzer scheint das System entweder ein- oder ausgeschaltet zu sein.
ms.assetid: 3d897a88-125e-457f-9ea7-ac2056b0767a
title: Systemleistungszustände
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eb93931326b67c7469b6a8ae256892e2dd77d4b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469907"
---
# <a name="system-power-states"></a>Systemleistungszustände

Für den Benutzer scheint das System entweder ein- oder ausgeschaltet zu sein. Es gibt keine anderen erkennbaren Zustände. Das System unterstützt jedoch mehrere Energiezustände, die den in der Advanced Configuration and Power Interface (ACPI)-Spezifikation definierten Energiezuständen entsprechen. Es gibt auch Variationen dieser Zustände, z. B. hybrider Standbymodus und schneller Start. In diesem Thema werden diese Zustände vorgestellt, und es wird beschrieben, wie sie miteinander in Beziehung stehen.

> [!NOTE]
> Systemintegratoren und Entwickler, die Treiber oder Anwendungen mit einem Systemdienst erstellen, sollten bei Problemen mit der Treiberqualität, z. B. Speicherverlusten, besonders vorsichtig sein. Die Treiberqualität war zwar schon immer wichtig, aber die Betriebszeit zwischen Kernelneustarts kann erheblich länger sein als bei früheren Versionen des Betriebssystems, da beim vom Benutzer initiierten Standbymodus und Herunterfahren der Kernel, die Treiber und die Dienste beibehalten und wiederhergestellt und nicht neu gestartet werden.

 

In der folgenden Tabelle sind die ACPI-Energiezustände vom höchsten bis zum niedrigsten Energieverbrauch aufgeführt.




| Betriebszustand | ACPI-Status | BESCHREIBUNG | 
|-------------|------------|-------------|
| In Bearbeitung<br /> | S0<br /> | Das System kann vollständig verwendet werden. Hardwarekomponenten, die nicht verwendet werden, können energiesparend sein, indem sie in einen niedrigeren Energiezustand gelangen.<br /> | 
| Standby<br /> (Moderner Standbymodus)<br /> | S0 mit geringer Energie im Leerlauf<br /> | Einige SoC-Systeme unterstützen einen Energiesparzustand im Leerlauf, der als <a href="/windows-hardware/design/device-experiences/modern-standby">Moderner Standbymodus</a>bezeichnet wird. In diesem Zustand kann das System sehr schnell von einem Zustand mit geringer Leistung in einen Zustand mit hoher Leistung wechseln, sodass es schnell auf Hardware- und Netzwerkereignisse reagieren kann. Systeme, die modernen Standbymodus unterstützen, verwenden nicht S1-S3.<br /> | 
| Standby<br /> | S1<br /> S2<br /> S3<br /> | Das System scheint deaktiviert zu sein. Der in diesen Zuständen verbrauchte Strom (S1-S3) ist kleiner als S0 und größer als S4. S3 verbraucht weniger Strom als S2, und S2 verbraucht weniger Strom als S1. Systeme unterstützen in der Regel einen dieser drei Zustände, nicht alle drei.<br /> In diesen Zuständen (S1-S3) wird flüchtiger Speicher aktualisiert, um den Systemstatus aufrechtzuerhalten. Einige Komponenten bleiben eingeschaltet, sodass der Computer von der Tastatur, dem LAN oder einem USB-Gerät aus reaktivieren kann.<br /><em>Hybrider Standbymodus,</em>der auf Desktops verwendet wird, ist der Ort, an dem ein System eine Ruhezustandsdatei mit S1-S3 verwendet. In der Ruhezustandsdatei wird der Systemzustand gespeichert, falls das System im Energiesparmodus aus dem Energiesparmodus ausschaltet.<br /><blockquote>[!Note]<br />SoC-Systeme, die modernen Standbymodus unterstützen (leerer Energiesparzustand), verwenden nicht S1-S3.</blockquote><br /><br /> | 
| Ruhezustand<br /> | S4<br /> | Das System scheint deaktiviert zu sein. Der Stromverbrauch wird auf die niedrigste Ebene reduziert. Das System speichert den Inhalt des flüchtigen Speichers in einer Ruhezustandsdatei, um den Systemstatus beizubehalten. Einige Komponenten bleiben eingeschaltet, sodass der Computer von der Tastatur, dem LAN oder einem USB-Gerät aus reaktivieren kann. Der Arbeitskontext kann wiederhergestellt werden, wenn er auf nicht flüchtigen Medien gespeichert ist. <br /><em>Beim schnellen Start</em> wird der Benutzer abgemeldet, bevor die Ruhezustandsdatei erstellt wird. Dies ermöglicht eine kleinere Ruhezustandsdatei, die besser für Systeme mit weniger Speicherfunktionen geeignet ist.<br /> | 
| Soft Off<br /> | S5<br /> | Das System scheint deaktiviert zu sein. Dieser Zustand besteht aus einem vollständigen Herunterfahren und einem Startzyklus.<br /> | 
| Separator Off<br /> | G3<br /> | Das System ist vollständig ausgeschaltet und verbraucht keinen Strom. Das System kehrt erst nach einem vollständigen Neustart in den Arbeitszustand zurück.<br /> | 




 

Die [**SYSTEM \_ POWER \_ STATE-Enumeration**](/windows/desktop/api/WinNT/ne-winnt-system_power_state) definiert Werte, die zum Angeben von Systemleistungszuständen verwendet werden.

## <a name="working-state-s0"></a>Arbeitszustand (S0)

Während des Arbeitszustands ist das System aktiv und wird ausgeführt. Einfach ausgedrückt: Das Gerät ist "on". Unabhängig davon, ob der Bildschirm ein- oder ausgeschaltet ist, befindet sich das Gerät in einem vollständig ausgeführten Zustand. Um Energie zu sparen, insbesondere bei akkugestützten Geräten, wird dringend empfohlen, Hardwarekomponenten auszuschalten, wenn sie nicht verwendet werden.

> [!IMPORTANT]
> Schalten Sie Hardwarekomponenten herunter, wenn sie nicht verwendet werden – unabhängig vom Zustand. Ein niedriger Energieverbrauch ist ein wichtiger Aspekt für Verbraucher mobiler Geräte.

 

## <a name="sleep-state-modern-standby"></a>Standbyzustand (moderner Standbymodus)

Im Energiesparmodus S0 des Betriebszustands, der auch als [moderner Standbymodus](/windows-hardware/design/device-experiences/modern-standby)bezeichnet wird, wird das System teilweise ausgeführt. Während des modernen Standbymodus kann das System immer auf dem neuesten Stand bleiben, wenn ein geeignetes Netzwerk verfügbar ist, und auch aktiviert werden, wenn Echtzeitaktionen erforderlich sind, wie z. B. die Wartung des Betriebssystems. Moderner Standbymodus wird deutlich schneller aktiviert als S1-S3. Weitere Informationen finden Sie unter [Modern Standby](/windows-hardware/design/device-experiences/modern-standby).

> [!Note]  
> Moderner Standbymodus ist nur auf einigen SoC-Systemen verfügbar. Wenn dies unterstützt wird, unterstützt das System S1-S3 nicht.

 

## <a name="sleep-state-s1-s3"></a>Standbyzustand (S1-S3)

Das System wechselt basierend auf einer Reihe von Kriterien in den Standbymodus, einschließlich Benutzer- oder Anwendungsaktivitäten und Einstellungen, die der Benutzer auf der Power **& Standbyseite** der **Einstellungen-App** festlegt. Standardmäßig verwendet das System den niedrigsten Standbyzustand, der von allen aktivierten Aktivierungsgeräten unterstützt wird. Weitere Informationen dazu, wie das System bestimmt, wann in den Standbymodus einzusteigen ist, finden Sie unter [System Standby Criteria](system-sleep-criteria.md).

Bevor das System in den Standbymodus wechselt, bestimmt es den geeigneten Standbyzustand, benachrichtigt Anwendungen und Treiber über den ausstehenden Übergang und übergibt dann das System in den Standbyzustand. Im Fall eines kritischen Übergangs, z. B. wenn der kritische Akkuschwellenwert erreicht wird, benachrichtigt das System Anwendungen und Treiber nicht. Anwendungen müssen darauf vorbereitet sein und die entsprechende Aktion ergreifen, wenn das System in den Arbeitszustand zurückkehrt.

In diesen Zuständen (S1-S3) wird flüchtiger Speicher aktualisiert, um den Systemstatus aufrechtzuerhalten. Einige Komponenten bleiben eingeschaltet, sodass der Computer von der Tastatur, dem LAN oder einem USB-Gerät aus reaktivieren kann.

Das System wird auch als Reaktion auf Benutzeraktivitäten oder ein von einer Anwendung definiertes Aktivierungsereignis aus dem Standbymodus aktiviert. Weitere Informationen finden Sie unter [Systemreaktivierungsereignisse.](system-wake-up-events.md) Wie lange die Aktivierung des Systems dauert, hängt vom Standbyzustand ab, aus dem es weckt. Das System benötigt mehr Zeit für das Reaktivieren von einem niedrigeren Zustand (S3) als von einem höheren Zustand (S1) aufgrund der zusätzlichen Arbeit, die die Hardware möglicherweise erledigen muss (Stabilisierung der Stromversorgung, erneute Initialisierung des Prozessors usw.).

> [!Caution]  
> Beim Aufrufen von [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate)sollte der **WERT ES \_ AWAYMODE \_ REQUIRED** nur dann verwendet werden, wenn dies von Medienanwendungen unbedingt erforderlich ist, die das System zum Ausführen von Hintergrundaufgaben wie der Aufzeichnung von Fernsehinhalten oder dem Streaming von Medien auf anderen Geräten im Ruhezustand auffordern. Anwendungen, die keine kritische Hintergrundverarbeitung erfordern oder auf portablen Computern ausgeführt werden, sollten den Auslagerungsmodus nicht aktivieren, da sie verhindern, dass das System Energie spart, indem es in den echten Standbymodus wechselt.

 

### <a name="hybrid-sleep-s1-s3--hibernation-file"></a>Hybrider Standbymodus (S1-S3 + Ruhezustandsdatei)

*Hybrider Standbymodus* ist ein spezieller Zustand, der eine Kombination aus dem Ruhezustand und dem Ruhezustand ist, wenn ein System eine Ruhezustandsdatei mit S1-S3 verwendet. Sie ist nur auf einigen Systemen verfügbar. Wenn diese Option aktiviert ist, schreibt das System eine Ruhezustandsdatei, wechselt aber in einen energiesparstärkeren Zustand. Wenn die Stromversorgung verloren geht, während sich das System im Ruhezustand befindet, wird das System aus dem Ruhezustand reaktiviert, was länger dauert, aber den Systemstatus des Benutzers wiederherstellt.

## <a name="hibernate-state-s4"></a>Ruhezustand (S4)

Windows verwendet den Ruhezustand, um ein schnelles Starterlebnis zu ermöglichen. Wenn verfügbar, wird es auch auf mobilen Geräten verwendet, um die nutzbare Akkulaufzeit eines Systems zu verlängern, indem ein Mechanismus zum Speichern des gesamten Benutzerzustands vor dem Herunterfahren des Systems bereitgestellt wird. Bei einem Ruhezustandsübergang wird der gesamte Inhalt des Arbeitsspeichers in eine Datei auf dem primären Systemlaufwerk, der *Ruhezustandsdatei,* geschrieben. Dadurch wird der Zustand des Betriebssystems, der Anwendungen und der Geräte beibehalten. Wenn der kombinierte Speicherbedarf den gesamten physischen Speicher belegt, muss die Ruhezustandsdatei groß genug sein, um sicherzustellen, dass Speicherplatz vorhanden ist, um den gesamten Inhalt des physischen Speichers zu speichern. Da Daten in einen nicht flüchtigen Speicher geschrieben werden, muss DRAM keine Selbstaktualisierung beibehalten und kann ausgeschaltet werden. Dies bedeutet, dass der Energieverbrauch des Ruhezustands sehr gering ist, fast identisch mit dem Ausschalten.

Während des vollständigen Herunterfahrens und Startens (S5) wird die gesamte Benutzersitzung heruntergefahren und beim nächsten Start neu gestartet. Im Gegensatz dazu wird während eines Ruhezustands (S4) die Benutzersitzung geschlossen und der Benutzerzustand gespeichert.

### <a name="fast-startup-reduced-hibernation-file"></a>Schneller Start (reduzierte Ruhezustandsdatei)

*Der schnelle Start* ist eine Art des Herunterfahrens, die eine Ruhezustandsdatei verwendet, um den nachfolgenden Start zu beschleunigen. Während dieses Herunterfahrens wird der Benutzer abgemeldet, bevor die Ruhezustandsdatei erstellt wird. Der schnelle Start ermöglicht eine kleinere Ruhezustandsdatei, die besser für Systeme mit weniger Speicherfunktionen geeignet ist. Weitere Informationen finden Sie unter [Ruhezustandsdateitypen.](#hibernation-file-types)

Bei Verwendung des schnellen Starts sieht das System für den Benutzer so aus, als ob ein vollständiges Herunterfahren (S5) erfolgt wäre, obwohl das System tatsächlich S4 durchgegangen ist. Dies schließt ein, wie das System auf Geräteaktivierungsalarm reagiert.

Beim schnellen Start werden Benutzersitzungen abgemeldet, aber der Inhalt des Kernels (Sitzung 0) wird auf die Festplatte geschrieben. Dies ermöglicht einen schnelleren Start.

Um programmgesteuert ein schnelles Herunterfahren im Startstil zu initiieren, rufen Sie die [**InitiateShutdown-Funktion**](/windows/desktop/api/winreg/nf-winreg-initiateshutdowna) mit dem **SHUTDOWN \_ HYBRID-Flag** oder die [**ExitWindowsEx-Funktion**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) mit dem **EWX \_ HYBRID \_ SHUTDOWN-Flag** auf.

> [!Note]  
> Ab Windows 8 ist der schnelle Start der Standardübergang, wenn ein Herunterfahren des Systems angefordert wird. Ein vollständiges Herunterfahren (S5) tritt auf, wenn ein Systemneustart angefordert wird (oder eine Anwendung eine Herunterfahren-API aufruft).

 

### <a name="entering-hibernation"></a>Eintritt in den Ruhezustand

Wenn eine Ruhezustandsanforderung erfolgt, erfolgen die folgenden Schritte, wenn das System in den Ruhezustand eintritt:

1.  Apps und Dienste werden benachrichtigt.
2.  Treiber werden benachrichtigt
3.  Der Benutzer- und Systemstatus wird in einem komprimierten Format auf dem Datenträger gespeichert.
4.  Firmware wird benachrichtigt

> [!Note]  
> Ab Windows 8 werden alle Kerne im System verwendet, um die Daten im Arbeitsspeicher zu komprimieren und auf den Datenträger zu schreiben.

 

Um programmgesteuert einen Ruhezustandsübergang zu initiieren, rufen Sie die [**SetSuspendState-Funktion**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) auf.

### <a name="resuming-from-hibernation"></a>Fortsetzen aus dem Ruhezustand

Wenn ein System aus dem Ruhezustand fortgesetzt wird.

Wenn ein System eingeschaltet wird, erfolgen die folgenden Schritte, wenn das System aus dem Ruhezustand fortgesetzt wird.

1.  System-POST
2.  Der Systemspeicher wird dekomprimiert und aus der Ruhezustandsdatei wiederhergestellt.
3.  Gerätein initialisierung
4.  Treiber werden in dem Zustand wiederhergestellt, in dem sie sich vor dem Ruhezustand befinden.
5.  Dienste werden in dem Zustand wiederhergestellt, in dem sie sich vor dem Ruhezustand befinden.
6.  Das System wird für die Anmeldung verfügbar.

Ein Fortsetzen aus dem Ruhezustand beginnt mit einem Post-System, das einem Herunterfahren von S5 ähnelt. Der Start-Manager des Betriebssystems stellt fest, dass eine Fortsetzung des Ruhezustands erforderlich ist, indem eine gültige Ruhezustandsdatei erkannt wird. Anschließend wird das System zum Fortsetzen des Systems und zum Wiederherstellen des Inhalts des Arbeitsspeichers und aller Architekturregister angedrungen. Im Fall einer Wiederaufnahme aus dem Ruhezustand wird der Inhalt des Systemspeichers vom Datenträger eingelesen, dekomprimiert und wiederhergestellt, und das System wird in den zustandsbewegten Zustand des Systems zurückgelesen, als der Ruhezustand auftrat. Nach der Wiederherstellung des Arbeitsspeichers werden die Geräte neu gestartet, und der Computer wird wieder ausgeführt und kann sich anmelden.

> [!Note]  
> Während einer Wiederaufnahme des Ruhezustands werden Treiber und Dienste benachrichtigt, aber nicht neu gestartet. Sie werden nur in dem Zustand wiederhergestellt, in dem sie sich vor dem Ruhezustand befinden.

 

### <a name="hibernation-file-types"></a>Ruhezustandsdateitypen

Ruhezustandsdateien werden für hybriden Ruhezustand, schnellen Start und Standard-Ruhezustand (oben beschrieben) verwendet. Es gibt zwei Typen, die sich nach Größe unterscheiden: eine vollständige und eine reduzierte Ruhezustandsdatei. Nur beim schnellen Start kann eine reduzierte Ruhezustandsdatei verwendet werden.



| Ruhezustandsdateityp | Standardgröße           | Unterstützt...                           |
|-----------------------|------------------------|---------------------------------------|
| Vollständig                  | 40 % des physischen Speichers | Ruhezustand, Hybridmodus, schneller Start |
| Reduziert               | 20 % des physischen Speichers | Schneller Start                          |



 

Um den Typ der verwendeten Ruhezustandsdatei zu überprüfen oder zu ändern, führen Sie das **hilfsprogrammpowercfg.exe** aus. In den folgenden Beispielen wird dies veranschaulicht. Wenn Sie hierzu weitere Informationen benötigen, führen Sie `powercfg /? hibernate` aus.



| Beispiel                                                                        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `powercfg /a`<br/>                                                | **Überprüfen Sie den Dateityp für den Ruhezustand.** Wenn eine vollständige Ruhezustandsdatei verwendet wird, ist der Ergebniszustand, dass der Ruhezustand eine verfügbare Option ist. Wenn eine reduzierte Ruhezustandsdatei verwendet wird, wird in den Ergebnissen der Ruhezustand nicht unterstützt. Wenn das System über keine Ruhezustandsdatei verfügt, wird in den Ergebnissen angezeigt, dass der Ruhezustand nicht aktiviert wurde.<br/> |
| `powercfg /h /type full`<br/>                                     | **Ändern Sie den Dateityp für den Ruhezustand in Vollständig.** Dies wird auf Systemen mit weniger als 32 GB Speicher nicht empfohlen.<br/>                                                                                                                                                                                                                        |
| `powercfg /h /type reduced`<br/>                                  | **Ändern Sie den Dateityp für den Ruhezustand in Reduziert.** Wenn der Befehl "der Parameter ist falsch" zurückgibt, sehen Sie sich das folgende Beispiel an.<br/>                                                                                                                                                                                                        |
| `powercfg /h /size 0`<br/> `powercfg /h /type reduced`<br/> | **Versuchen Sie erneut, den Dateityp für den Ruhezustand in reduziert zu ändern.** Wenn die Ruhezustandsdatei auf eine benutzerdefinierte Größe größer als 40 % festgelegt ist, müssen Sie zuerst die Größe der Datei auf 0 (null) festlegen. Wiederholen Sie dann die reduzierte Konfiguration.<br/>                                                                                                                       |



 

## <a name="soft-off-state-s5"></a>Soft Off-Zustand (S5)

Der Soft off-Zustand ist , wenn das System ohne Eine Ruhezustandsdatei vollständig heruntergefahren wird. Soft off wird auch als "vollständiges Herunterfahren" bezeichnet. Während des vollständigen Herunterfahrens und Startens wird die gesamte Benutzersitzung beim nächsten Start heruntergefahren und neu gestartet. Folglich dauert ein Start/Start aus diesem Zustand erheblich länger als S1-S4. Ein vollständiges Herunterfahren (S5) tritt auf, wenn ein Systemneustart angefordert wird (oder eine Anwendung eine Herunterfahren-API aufruft).

## <a name="mechanical-off-state-g3"></a>Ausschaltzustand (G3)

In diesem Zustand ist das System vollständig ausgeschaltet und verbraucht keine Stromversorgung. Das System kehrt erst nach einem vollständigen Neustart in den Betriebszustand zurück.

## <a name="wake-on-lan-behavior"></a>Wake-On-LAN-Verhalten

Das Wake-On-LAN-Feature (WAKE) reaktiviert den Computer aus einem niedrigen Energiezustand, wenn ein Netzwerkadapter ein WAKE-Ereignis erkennt (in der Regel ein speziell konstruiertes Ethernet-Paket).

NAT wird vom Ruhezustand (S3) oder Ruhezustand (S4) unterstützt. Dies wird beim schnellen Start oder beim Herunterfahren (S5) nicht unterstützt. NiCs sind in diesen Zuzuständen nicht aktivierungserweckt, da Benutzer nicht erwarten, dass ihre Systeme selbst reaktivieren.

> [!Note]  
> OFF (Soft Off, S5) wird offiziell nicht unterstützt. Allerdings unterstützt das BIOS auf einigen Systemen möglicherweise das Arming von NICs für die Aktivierung, auch wenn Windows nicht am Prozess beteiligt ist.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Energieverwaltung](about-power-management.md)
</dt> </dl>

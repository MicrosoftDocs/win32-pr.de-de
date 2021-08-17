---
title: Plug-In-Architektur
description: Biometrische Einheiten machen die Funktionen eines Geräts für das Framework über eine Standardschnittstelle verfügbar, die aus Sensor-, Engine- und Speicheradaptern besteht.
ms.assetid: d2835413-70a3-45fa-93e2-3fe78097554f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33a82f85387698f7fb80c65525004ac541a1108635ca3d929adda7b0cbb932cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119411064"
---
# <a name="plug-in-architecture"></a>Plug-In-Architektur

Biometrische Geräte werden in einer Vielzahl von Typen und Konfigurationen hergestellt. Das Windows Biometric Framework bietet eine erweiterbare Architektur, mit der Entwickler von Drittanbietern benutzerdefinierte Plug-In-Komponenten erstellen können. Die primäre Komponente ist ein Softwareobjekt, das als biometrische Einheit bezeichnet wird. Biometrische Einheiten machen die Funktionen eines Geräts für das Framework über eine Standardschnittstelle verfügbar, die aus Sensor-, Engine- und Speicheradaptern besteht. Biometrische Einheiten und die zugehörigen Komponenten werden in den folgenden Themen erläutert.

## <a name="biometric-unit"></a>Biometrische Einheit

Die zentrale Komponente der Plug-In-Architektur für Windows Biometric Framework ist die biometrische Einheit, ein Softwareobjekt, das die Funktionen eines biometrischen Geräts über eine Standardschnittstelle für das Framework verfügbar macht.

Jeder biometrischen Einheit ist ein einzelner physischer Sensor zugeordnet. Der Sensor erfasst biometrische Daten und kann je nach Hardwarefunktionen auch andere biometrische Vorgänge wie Vorlagenabgleich und -speicherung durchführen. Sensoren, die das Onboarding von Abgleich oder Speicher nicht unterstützen, benötigen zusätzliche Softwaremodule, um diese Funktionen auszuführen. Weitere Informationen finden Sie unter [Adapter.](/previous-versions//dd401508(v=vs.85))

Die folgende Abbildung zeigt, wie Daten durch eine biometrische Einheit fließen. Im Wesentlichen bildet der Datenfluss einen Typ von Pipeline. Die erste Eingabe für die Pipeline ist ein biometrisches Beispiel, das von einem physischen Sensor erfasst wird. Die Engine versucht, das Beispiel mit Vorlagen abzugleichen, die bereits im Vorlagenspeicher vorhanden sind, oder, wenn keine Übereinstimmung gefunden wird, erstellt eine neue Vorlage aus wiederholten physischen Stichproben und speichert die Vorlage im Speicher.

![Daten, die durch eine biometrische Einheit fließen](images/biometricunit-dataflow.png)

## <a name="biometric-unit-life-cycle"></a>Lebenszyklus biometrischer Einheiten

### <a name="creation"></a>Erstellung

When the Windows Biometric Service starts or when it receives a hardware notification from the Plug and Play manager, it scans for any hardware that supports the well-known interface GUID\_DEVINTERFACE\_BIOMETRIC\_READER (E2B5183A-99EA-4cc3-AD6B-80CA8D715B80). Für jedes ermittelte biometrische Gerät gilt Folgendes:

-   Öffnet ein Handle für das Gerät.
-   Fragt die Gerätefunktionen mithilfe einer Windows Steuerungsschnittstelle des biometrischen Treibers ab.
-   Öffnet den Geräteregistrierungsschlüssel und versucht, Informationen zu zugeordneten Adapter-Plug-Ins zu finden.
-   Öffnet die Windows Biometrischer Dienstregistrierungsschlüssel und sucht nach Informationen zu allen globalen Plug-Ins, die die gerätespezifischen Werte aus dem vorherigen Schritt überschreiben sollten.
-   Erstellt eine biometrische Einheit zur Darstellung des Geräts und übergibt die Einheit an einen biometrischen Dienstanbieter.

### <a name="configuration"></a>Konfiguration

Nachdem ein biometrischer Dienstanbieter (BSP) eine biometrische Einheit akzeptiert hat, konfiguriert er die Einheit und weist sie einem Sensorpool zu. Weitere Informationen finden Sie unter [Sensorpools.](sensor-pools.md) Die Einheit wird konfiguriert, indem die entsprechenden Adapter geladen, eine Verbindung mit einem Vorlagenspeicher hergestellt und möglicherweise der Betriebsmodus geändert wird. Eine biometrische Einheit kann für den Betrieb in einem von zwei Modi konfiguriert werden:

-   Im Basismodus fungiert die Einheit als einfaches Erfassungsgerät. Es verwendet keine integrierte Verarbeitung oder keinen Speicher, sondern benötigt ausschließlich Softwareadapter für zusätzliche Unterstützung. Es sollte in der Lage sein, Stichproben in einem Standardformat zu generieren. Fingerabdruckleser sollten beispielsweise Stichproben generieren, die ANSI INCITS 381-2004 entsprechen. Der Grundmodus dient der Unterstützung der Interoperabilität zwischen Komponenten verschiedener Anbieter.
-   Im erweiterten Modus verwendet die biometrische Einheit integrierte Verarbeitungs- und Speicherfunktionen. Sie muss die Standardschnittstellen verfügbar machen, kann jedoch Stichproben in jedem gewünschten Format generieren und verarbeiten.

Wenn eine biometrische Einheit von einem Sensorpool in einen anderen verschoben wird, werden die Adapter entladen und für den neuen Sensorpool neu konfiguriert. Die Identität der biometrischen Einheit bleibt konstant. nur die Hardwarekonfiguration und Adapter-Plug-Ins ändern sich.

### <a name="shut-down"></a>Herunterfahren

Wenn der Windows Biometric Service heruntergefahren wird oder der Plug & Play-Manager ihn benachrichtigt, dass eine Einheit entfernt wurde, löscht der Dienst alle biometrischen Einheiten.

## <a name="adapters"></a>Adapter

Plug-In-Softwarekomponenten, die als Adapter bezeichnet werden, verbinden eine biometrische Einheit mit der zugrunde liegenden Hardware und stellen alle Funktionen bereit, die auf der Sensorhardware möglicherweise fehlen. Es gibt drei Arten von Adaptern, die Sie erstellen können:

-   Ein Sensoradapter umschließt ein biometrisches Gerät und bietet eine Standardschnittstelle zum Konfigurieren des Sensors, Erfassen von Stichproben und Steuern des Flusses biometrischer Daten an die Verarbeitungs-Engine.
-   Ein Engine-Adapter generiert biometrische Vorlagen aus erfassten Beispielen, gleicht Stichproben mit vorhandenen Vorlagen ab und indiziert Vorlagen.
-   Ein Speicheradapter verwaltet Vorlagendatenbanken.

Adapter können zur Laufzeit geladen und entladen werden. Dadurch kann der Windows Biometric Service eine biometrische Einheit dynamisch neu konfigurieren, indem er eine Verbindung mit einer anderen Gruppe von Adaptern herstellt.

Schließlich machen alle Sensor-, Engine- und Speicheradapterschnittstellen zwei Methoden verfügbar: **ControlUnit** und **ControlUnitPrivileged,** mit denen Clientanwendungen auf vom Anbieter definierte benutzerdefinierte Adapterfunktionen zugreifen können. Dadurch kann der Anbieter einen nahezu unbegrenzten Satz von Steuerungsvorgängen für ein Gerät definieren. Darüber hinaus kann ein Anbieter durch Auswahl der zu implementierenden Funktion einige Steuerungsvorgänge für nicht privilegierte Benutzer verfügbar machen und gleichzeitig andere Vorgänge auf privilegierte Benutzer beschränken.

Weitere Informationen zum Erstellen von Adaptern finden Sie unter [Erstellen von Adapter-Plug-Ins.](creating-adapter-plug-ins.md)

## <a name="adapter-performance-requirements"></a>Adapterleistungsanforderungen

Da das Ziel insgesamt eine schnelle Reaktion ist, wird die Leistung eines Adapters nicht in Bezug auf die Zeitlimits für bestimmte Routinen angegeben. Stattdessen wird die Leistung als Satz von Anforderungen für die allgemeine Benutzererfahrung angegeben.

Es gibt zwei Anforderungen:

-   Jede Interaktion zwischen dem Benutzer und dem Betriebssystem, die biometrische Daten umfasst, muss innerhalb von zwei Sekunden abgeschlossen sein. Dieses Intervall misst die Start-zu-Finish-Zeit, die der Benutzer von dem Zeitpunkt, zu dem er den Sensor berührt oder wischt, bis zu dem Zeitpunkt, zu dem etwas sichtbares auf dem Gerätebildschirm geschieht, wahrnimmt. (Beispielsweise darf es während der Entsperrung nicht mehr als zwei Sekunden zwischen dem Benutzer, der den Fingerabdrucksensor berührt oder wischt, und dem Sperrbildschirm, der die Identität des Benutzers bestätigt, kommen.)
-   Für die anfängliche Darstellung von Anmeldeinformationskacheln auf dem Anmelde- oder Sperrbildschirm lassen wir etwas mehr Zeit (drei Sekunden, Maximum) zu, aber wir bevorzugen immer noch früher als später. Insbesondere muss die Biokachel innerhalb von drei Sekunden nach der Darstellung des Sperr- oder Anmeldebereichs auf dem Bildschirm angezeigt werden.

Diese Zahlen sind nicht willkürlich. Zahlreiche Studien haben gezeigt, dass Menschliche tendenziell alles erleben, was innerhalb eines Zwei-Sekunden-Intervalls als Teil des "jetzt"-Moments geschieht. Wenn Ereignis A und Ereignis B innerhalb von zwei Sekunden voneinander auftreten, werden diese Ereignisse als gleichzeitig wahrgenommen. Wenn die Ereignisse mehr als drei Sekunden voneinander getrennt sind, denken Die Menschen, dass es eine Verzögerung gibt– sie glauben, dass etwas zu lange dauert. Dies ist also ein Problem hartverkabelter Menschlicher.

 

 
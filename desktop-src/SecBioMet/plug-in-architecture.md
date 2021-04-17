---
title: Plug-in-Architektur
description: Biometrische Einheiten machen die Funktionen eines Geräts für das Framework über eine Standardschnittstelle verfügbar, die aus Sensor-, Engine-und Speicher Adaptern besteht.
ms.assetid: d2835413-70a3-45fa-93e2-3fe78097554f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52e43af9c0ea5a8db57cc0e0970b5625b1ba118f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473709"
---
# <a name="plug-in-architecture"></a>Plug-in-Architektur

Biometrische Geräte werden in einer Vielzahl von Typen und Konfigurationen gefertigt. Die Windows-Biometrieframework adressiert diese Vielfalt durch Bereitstellung einer erweiterbaren Architektur, mit der Entwickler von Drittanbietern benutzerdefinierte Plug-in-Komponenten erstellen können. Die primäre Komponente ist ein Software Objekt, das als biometrische Einheit bezeichnet wird. Biometrische Einheiten machen die Funktionen eines Geräts für das Framework über eine Standardschnittstelle verfügbar, die aus Sensor-, Engine-und Speicher Adaptern besteht. In den folgenden Themen werden biometrische Einheiten und deren Komponenten erläutert.

## <a name="biometric-unit"></a>Biometrische Einheit

Die zentrale Komponente der Windows-Biometrieframework-Plug-in-Architektur ist die biometrische Einheit, ein Software Objekt, das die Funktionen eines biometrischen Geräts über eine Standardschnittstelle für das Framework verfügbar macht.

Jeder biometrischen Einheit ist ein einzelner physischer Sensor zugeordnet. Der Sensor erfasst biometrische Daten und kann abhängig von den Hardwarefunktionen auch andere biometrische Vorgänge ausführen, wie z. b. die Vorlagen Übereinstimmung und den Speicher. Sensoren, die das Integrieren von Abgleich oder Speicher nicht unterstützen, erfordern zusätzliche Softwaremodule, um diese Funktionen auszuführen. Weitere Informationen finden Sie unter [Adapter](/previous-versions//dd401508(v=vs.85)).

In der folgenden Abbildung wird gezeigt, wie Daten durch eine biometrische Einheit fließen. Im Wesentlichen bildet der Datenfluss einen Typ von Pipeline. Die erste Eingabe für die Pipeline ist ein biometrisches Beispiel, das von einem physischen Sensor aufgezeichnet wird. Die Engine versucht, das Beispiel mit Vorlagen abzugleichen, die bereits im Vorlagen Speicher vorhanden sind, oder erstellt eine neue Vorlage aus wiederholten physischen Beispielen, wenn keine Entsprechung gefunden wird, und speichert die Vorlage im Speicher.

![Daten, die durch eine biometrische Einheit fließen](images/biometricunit-dataflow.png)

## <a name="biometric-unit-life-cycle"></a>Lebenszyklus der biometrischen Einheit

### <a name="creation"></a>Erstellung

Wenn der Windows-biometrische Dienst startet oder eine Hardware Benachrichtigung vom Plug & Play-Manager empfängt, sucht er nach Hardware, die den bekannten Schnittstellen-GUID \_ devinterface- \_ \_ biometrilereader (E2B5183A-99EA-4cc3-AD6B-80CA8D715B80) unterstützt. Wählen Sie für jedes biometrische Gerät Folgendes aus:

-   Öffnet ein Handle für das Gerät.
-   Fragt die Gerätefunktionen mithilfe einer Windows-Biometrie-treibersteuerungschnittstelle ab.
-   Öffnet den Geräte Registrierungsschlüssel und versucht, Informationen zu zugeordneten Adapter-Plug-ins zu suchen.
-   Öffnet den Windows-biometrischen Dienst Registrierungsschlüssel und sucht nach Informationen zu beliebigen globalen Plug-ins, die die gerätespezifischen Werte überschreiben sollen, die im vorherigen Schritt gefunden wurden.
-   Erstellt eine biometrische Einheit zur Darstellung des Geräts und übergibt die Einheit an einen biometrischen Dienstanbieter.

### <a name="configuration"></a>Konfiguration

Nachdem ein biometrischer Dienstanbieter (Service Provider, BSP) eine biometrische Einheit akzeptiert hat, wird die Einheit konfiguriert und einem Sensor Pool zugewiesen. Weitere Informationen finden Sie unter [Sensor Pools](sensor-pools.md). Die Einheit wird konfiguriert, indem die entsprechenden Adapter geladen werden, eine Verbindung mit einem Vorlagen Speicher hergestellt und möglicherweise der Betriebsmodus geändert wird. Eine biometrische Einheit kann für den Betrieb in einem von zwei Modi konfiguriert werden:

-   Im Modus "Basic" fungiert die Einheit als einfaches Erfassungsgerät. Sie verwendet nicht die Verarbeitung oder Speicherung von Netz Geräten, sondern basiert ausschließlich auf Software Adaptern für zusätzliche Unterstützung. Er sollte in der Lage sein, Beispiele in einem Standardformat zu generieren. Fingerabdruckleser sollten z. b. Beispiele generieren, die ANSI-incipten 381-2004 entsprechen. Der grundlegende Modus besteht darin, die Interoperabilität zwischen Komponenten verschiedener Anbieter zu unterstützen.
-   Im erweiterten Modus verwendet die biometrische Einheit das Integrieren von Verarbeitungs-und Speicherfunktionen. Es muss die Standardschnittstellen verfügbar machen, kann jedoch Beispiele in jedem beliebigen Format generieren und verarbeiten.

Wenn eine biometrische Einheit von einem Sensor Pool in einen anderen verschoben wird, werden die zugehörigen Adapter entladen und für den neuen Sensor Pool neu konfiguriert. Die Identität der biometrischen Einheit bleibt konstant. nur die Hardwarekonfiguration und Adapter-Plug-ins werden geändert.

### <a name="shut-down"></a>Herunterfahren

Wenn der Windows-biometrische Dienst heruntergefahren wird oder der Plug & Play-Manager ihn darüber benachrichtigt, dass eine Einheit entfernt wurde, löscht der Dienst alle biometrischen Einheiten.

## <a name="adapters"></a>Adapter

Die Plug-in-Softwarekomponenten, die als Adapter bezeichnet werden, verbinden eine biometrische Einheit mit der zugrunde liegenden Hardware und stellen alle Funktionen bereit, die möglicherweise in der Sensor Hardware fehlen. Es gibt drei Arten von Adaptern, die Sie erstellen können:

-   Ein Sensor Adapter dient als Wrapper für ein biometrisches Gerät und stellt eine Standardschnittstelle zum Konfigurieren des Sensors, zum Erfassen von Beispielen und zum Steuern des Flusses biometrischer Daten an die Verarbeitungs-Engine bereit.
-   Ein Engine-Adapter generiert biometrische Vorlagen aus aufgezeichneten Beispielen, entspricht Beispielen für vorhandene Vorlagen und Index Vorlagen.
-   Ein Speicher Adapter verwaltet Vorlagen Datenbanken.

Adapter können zur Laufzeit geladen und entladen werden. Dadurch kann der biometrische Windows-Dienst eine biometrische Einheit dynamisch neu konfigurieren, indem Sie Sie mit einer anderen Gruppe von Adaptern verbindet.

Schließlich stellen alle Sensor-, Engine-und Speicher Adapter Schnittstellen zwei Methoden ( **Controlunit** und **controlunitprivilegierte**) zur Verfügung, mit denen Client Anwendungen auf vom Hersteller definierte benutzerdefinierte Adapter Funktionen zugreifen können. Dies ermöglicht es dem Hersteller, einen fast unbegrenzten Satz von Steuerungs Vorgängen für ein Gerät zu definieren. Durch die Auswahl der zu implementierenden Funktion kann ein Hersteller außerdem festlegen, dass einige Steuerungs Vorgänge für nicht privilegierte Benutzer verfügbar gemacht werden, während andere Vorgänge auf privilegierte Benutzer beschränkt werden.

Weitere Informationen zum Erstellen von Adaptern finden Sie unter [Erstellen von Adapter-Plug-ins](creating-adapter-plug-ins.md).

## <a name="adapter-performance-requirements"></a>Leistungsanforderungen für Adapter

Da das Ziel eine schnelle Antwort insgesamt ist, wird die Leistung eines Adapters nicht in Bezug auf Zeitlimits für bestimmte Routinen angegeben. Stattdessen wird die Leistung als eine Reihe von Anforderungen für die gesamte Benutzer Leistung angegeben.

Es gibt zwei Anforderungen:

-   Jede Interaktion zwischen dem Benutzer und dem Betriebssystem, das Biometrie erfordert, muss innerhalb von zwei Sekunden ausgeführt werden. In diesem Intervall wird die Start-bis-Ende-Zeit gemessen, die der Benutzer von dem Zeitpunkt, an dem er sich befindet, bis zu dem Zeitpunkt, an dem Sie sichtbar sind, auf dem Geräte Bildschirm abfängt. (Z. b. während des entsperrungs Zeitfensters dürfen nicht mehr als eine Verzögerung von zwei Sekunden zwischen dem Benutzer und dem Sperrbildschirm, der die Identität des Benutzers bestätigt, liegen.)
-   Für die anfängliche Darstellung von Kacheln für Anmelde Informationen auf dem Anmelde-oder Sperrbildschirm ist ein wenig Zeit (drei Sekunden, maximal) zulässig, aber wir bevorzugen immer noch früher als später. Insbesondere muss die Kachel "Bio" auf dem Bildschirm innerhalb von drei Sekunden nach der Darstellung des Sperr-oder Anmelde Panels sichtbar sein.

Diese Zahlen sind nicht willkürlich. Viele Studien haben ergeben, dass Menschen in der Regel innerhalb eines Zeitraums von zwei Sekunden alle Vorgänge erleben, die im Rahmen des "jetzt"-Zeitintervalls auftreten. Wenn Ereignis A und Ereignis B innerhalb von zwei Sekunden zueinander auftreten, werden diese Ereignisse als gleichzeitig betrachtet. Wenn die Ereignisse durch mehr als ungefähr drei Sekunden voneinander getrennt sind, denken Sie daran, dass es eine Verzögerung gibt – das heißt, dass es zu lange dauert. Das ist also ein Problem der hart verdrahteten Menschen Psychologie.

 

 
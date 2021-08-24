---
description: Teilnahme von Hardwaregeräten am Filter Graph
ms.assetid: 27e1c097-9bb4-4f9c-b9f9-0d4225c0d290
title: Teilnahme von Hardwaregeräten am Filter Graph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b3b2940b6c434459d1213dd0f4265f4d9250e548ede7f2509f7f68c27166861
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119389160"
---
# <a name="how-hardware-devices-participate-in-the-filter-graph"></a>Teilnahme von Hardwaregeräten am Filter Graph

In diesem Artikel wird beschrieben, wie DirectShow mit Audio- und Videohardware interagiert.

**Wrapperfilter**

Alle DirectShow-Filter sind Softwarekomponenten im Benutzermodus. Damit ein Hardwaregerät im Kernelmodus, z. B. eine Videoaufnahmekarte, einem DirectShow-Filterdiagramm beitreten kann, muss das Gerät als Benutzermodusfilter dargestellt werden. Diese Funktion wird von spezialisierten Wrapperfiltern ausgeführt, die mit DirectShow bereitgestellt werden. Zu diesen Filtern gehören der [Audio capture-Filter,](audio-capture.md) der [VFW](vfw-capture-filter.md) Capture-Filter, der [TV-Tuner-Filter,](tv-tuner-filter.md) der [TV](tv-audio-filter.md) Audio-Filter und der Analog Video [Crossbar-Filter.](analog-video-crossbar-filter.md) DirectShow bietet auch einen Filter mit dem Namen KsProxy, der jede Art von WDM-Streaminggerät (Windows Driver Model) darstellen kann. Hardwarehersteller können KsProxy erweitern, um benutzerdefinierte Funktionen zu unterstützen, indem sie ein *Ksproxy-Plug-In* bereitstellen, bei dem es sich um ein von KsProxy aggregiertes COM-Objekt handelt.

Die Wrapperfilter machen COM-Schnittstellen verfügbar, die die Funktionen des Geräts darstellen. Die Anwendung verwendet diese Schnittstellen, um Informationen an und aus dem Filter zu übergeben. Der Filter übersetzt die COM-Methodenaufrufe in Gerätetreiberaufrufe, übergibt diese Informationen im Kernelmodus an den Treiber und übersetzt das Ergebnis dann wieder an die Anwendung. Die Filter TV Tuner, TV Audio, Analog Video Crossbar und KsProxy unterstützen benutzerdefinierte Treibereigenschaften über die [**IKsPropertySet-Schnittstelle.**](ikspropertyset.md) Der VFW-Erfassungsfilter und der Audioaufnahmefilter sind auf diese Weise nicht erweiterbar.

Für Anwendungsentwickler ermöglichen Wrapperfilter es der Anwendung, Geräte genauso zu steuern, wie sie jeden anderen DirectShow-Filter steuern. Es ist keine spezielle Programmierung erforderlich. Die Details der Kommunikation mit dem Kernelmodusgerät sind im Filter gekapselt.

**Video für Windows Geräte**

Der VFW-Erfassungsfilter unterstützt frühere Video for Windows(VfW)-Erfassungskarten. Wenn eine VfW-Karte auf dem Zielsystem vorhanden ist, kann sie mithilfe des [DirectShow-Systemgeräte-Enumerators](system-device-enumerator.md)gefunden und dem Filterdiagramm hinzugefügt werden. Weitere Informationen finden Sie unter [Aufzählen von Geräten und Filtern.](enumerating-devices-and-filters.md)

**Audioaufnahme und Mischen von Geräten (Soundkarten)**

Neuere Soundkarten verfügen über Eingabebuchsen für Mikrofone und andere Gerätetypen. In der Regel verfügen diese Karten auch über On-Board-Mischungsfunktionen zum Steuern der Lautstärke, des Trebles und des Tafelns der einzelnen Eingaben. In DirectShow werden die Eingaben und der Mixer der Soundkarte vom Audioaufnahmefilter umschlossen. Jede Soundkarte kann mit dem Systemgeräte-Enumerator gefunden werden. Um die Soundkarten in Ihrem System anzeigen zu können, führen Sie GraphEdit aus, und wählen Sie aus der Kategorie Audioaufnahmequellen aus. Jeder Filter in dieser Kategorie ist eine separate Instanz des Audioaufnahmefilters. (Siehe [Verwenden von GraphEdit](using-graphedit.md).)

**WDM-Streaminggeräte**

Neuere Hardwaredecoder und Erfassungskarten entsprechen der WDM-Spezifikation (Windows Driver Model). Diese Geräte verfügen über eine höhere Funktionalität als VfW-Geräte. WDM-Videoaufnahmekarten können Features unterstützen, die unter VfW nicht verfügbar sind, einschließlich der Enumeration von Erfassungsformaten, der programmgesteuerten Steuerung von Videoparametern wie Farbton und Helligkeit, programmgesteuerter Eingabeauswahl und TV-Tuner-Unterstützung.

Zur Unterstützung von WDM-Streaminggeräten stellt DirectShow den KsProxy-Filter (ksproxy.ax. KsProxy wurde als "Filter für Stichstiche" bezeichnet, da so viele verschiedene Dinge durchgeführt werden. Die Anzahl der Stecknadeln im Filter und die Anzahl der vom Filter verfügbar gemachten COM-Schnittstellen hängen von den Funktionen des zugrunde liegenden Treibers ab. KsProxy wird nicht im Filterdiagramm unter dem Namen "KsProxy" angezeigt. Es wird immer der Angezeigte Name des Geräts verwendet, der in der Registrierung zu finden ist. Um die WDM-Geräte auf Ihrem System anzeigen zu können, führen Sie GraphEdit aus, und wählen Sie aus den WDM-Streamingkategorien aus. Auch wenn Sie nur über eine WDM-Karte auf Ihrem System verfügen, kann diese Karte mehr als ein Gerät enthalten. Jedes Gerät wird als separater Filter dargestellt, und jeder dieser Filter ist tatsächlich KsProxy.

Eine Anwendung verwendet den Systemgeräte-Enumerator, um WDM-Gerätemoniker auf dem System zu suchen. KsProxy wird instanziiert, indem **BindToObject für den** Moniker aufruft. Da KsProxy alle Arten von WDM-Geräten darstellen kann, muss der Treiber abfragen, um zu bestimmen, welche Eigenschaftensätze der Treiber unterstützt. Eigenschaftssätze sind Sammlungen von Datenstrukturen, die von WDM-Treibern und auch von einigen Benutzermodusfiltern verwendet werden, z. B. MPEG-2-Softwaredecoder. KsProxy konfiguriert sich selbst, um die COM-Schnittstellen verfügbar zu machen, die diesen Eigenschaftensätzen entsprechen. KsProxy übersetzt die COM-Methodenaufrufe in Eigenschaftensätze und sendet diese an den Treiber. Hardwarehersteller können KsProxy erweitern, indem sie Plug-Ins zur Verfügung stellen. Dabei handelt es sich um anbieterspezifische Schnittstellen, die die speziellen Funktionen eines Geräts verfügbar machen. Alle diese Details werden in der Anwendung ausgeblendet. Die Anwendung steuert das Gerät mit KsProxy auf die gleiche Weise wie jeder andere DirectShow-Filter.

**Kernelstreaming**

WDM-Geräte unterstützen Kernelstreaming, bei dem Daten vollständig im Kernelmodus gestreamt werden, ohne jemals in den Benutzermodus zu wechseln. Das Wechseln zwischen Kernelmodus und Benutzermodus ist rechenintensiv. Kernelstreaming ermöglicht hohe Bitraten, ohne die Host-CPU zulasten zu machen. WDM-basierte Filter können Kernelstreaming verwenden, um Multimediadaten direkt von einem Hardwaregerät an ein anderes zu übergeben, entweder auf derselben Karte oder auf einer anderen Karte, ohne die Daten in den Hauptspeicher des Systems zu kopieren.

Aus Sicht einer Anwendung sieht es so aus, als würden die Daten von einem Benutzermodusfilter zum nächsten wechseln. In Wirklichkeit werden die Daten möglicherweise nie in den Benutzermodus übertragen, sondern stattdessen direkt von einem Gerät im Kernelmodus auf ein anderes gestreamt, bis sie auf der Grafikkarte gerendert werden. Einige Szenarien, z. B. die Erfassung in einer Datei, erfordern, dass die Daten zu einem bestimmten Zeitpunkt vom Kernelmodus in den Benutzermodus übergeben werden. Dieser Schalter erfordert jedoch nicht unbedingt, dass die Daten an einen neuen Speicherort im Arbeitsspeicher kopiert werden.

Anwendungsentwickler müssen sich in der Regel nicht um die Details des Kernelstreamings sorgen, mit Ausnahme von Hintergrundinformationen. Ausführlichere Informationen zu WDM, Kernelstreaming, KsProxy und verwandten Themen finden Sie im Microsoft DDK.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Die Filter-Graph und ihre Komponenten](the-filter-graph-and-its-components.md)
</dt> </dl>

 

 




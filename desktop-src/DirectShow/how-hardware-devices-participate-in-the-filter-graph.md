---
description: Einbeziehung von Hardware Geräten in das Filter Diagramm
ms.assetid: 27e1c097-9bb4-4f9c-b9f9-0d4225c0d290
title: Einbeziehung von Hardware Geräten in das Filter Diagramm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68794bbc046e633e9a435b2628a20b8ea8aab174
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480739"
---
# <a name="how-hardware-devices-participate-in-the-filter-graph"></a>Einbeziehung von Hardware Geräten in das Filter Diagramm

In diesem Artikel wird beschrieben, wie DirectShow mit Audio-und Video Hardware interagiert.

**Wrapper Filter**

Alle DirectShow-Filter sind benutzermodussoftwarekomponenten. Damit ein Hardware Gerät im Kernelmodus, z. b. eine Video Erfassungs Karte, einem DirectShow-Filter Diagramm beitreten kann, muss das Gerät als Filter im Benutzermodus dargestellt werden. Diese Funktion wird von spezialisierten "Wrapper"-Filtern ausgeführt, die mit DirectShow bereitgestellt werden. Zu diesen Filtern gehören der [audioerfassungs](audio-capture.md) Filter, der [VFW-Erfassungs](vfw-capture-filter.md) Filter, der [TV](tv-tuner-filter.md) -gatewayfilter, der [TV-Audiofilter](tv-audio-filter.md) und der [analoge Video Crossbar](analog-video-crossbar-filter.md) -Filter. DirectShow bietet auch einen Filter mit dem Namen "ksproxy", der alle Arten von Windows-Treibermodell (WDM)-Streaminggeräten darstellen kann. Hardware Anbieter können ksproxy erweitern, um benutzerdefinierte Funktionen zu unterstützen, indem Sie ein *ksproxy-Plug-in* bereitstellen, bei dem es sich um ein COM-Objekt handelt, das von ksproxy

Die Wrapper Filter machen com-Schnittstellen verfügbar, die die Funktionen des Geräts darstellen. Diese Schnittstellen werden von der Anwendung verwendet, um Informationen an den und aus dem Filter zu übergeben. Der Filter übersetzt die com-Methodenaufrufe in Gerätetreiber Aufrufe, übergibt diese Informationen an den Treiber im Kernel Modus und übersetzt das Ergebnis dann wieder in die Anwendung. Die Filter "TV-Tuner", "TV-Audiodatei", "analoge Video Crossbar" und "ksproxy" unterstützen benutzerdefinierte Treiber Eigenschaften über die " [**iksproperty**](ikspropertyset.md) Der Vfw-Erfassungs Filter und der audioerfassungs Filter sind auf diese Weise nicht erweiterbar.

Für Anwendungsentwickler ermöglichen Wrapper Filter der Anwendung die Steuerung von Geräten, ebenso wie alle anderen DirectShow-Filter. Es ist keine spezielle Programmierung erforderlich. die Details der Kommunikation mit dem kernelmodusgerät werden innerhalb des Filters gekapselt.

**Video für Windows-Geräte**

Der Vfw-Erfassungs Filter unterstützt frühere Video für Windows-Erfassungs Karten (Vfw). Wenn eine VFW-Karte auf dem Zielsystem vorhanden ist, kann diese ermittelt und mithilfe des DirectShow- [Systemgeräte Enumerators](system-device-enumerator.md)dem Filter Diagramm hinzugefügt werden. Weitere Informationen finden Sie unter Auflisten von [Geräten und Filtern](enumerating-devices-and-filters.md).

**Audioerfassung und-Vermischung von Geräten (Sound Karten)**

Neuere Soundkarten enthalten Eingabedaten für das Mikrofon und andere Arten von Geräten. In der Regel verfügen diese Karten auch über eine webbasierte Mischung, um das Volume, den Treble und den Bass der einzelnen Eingaben zu steuern. In DirectShow werden Eingaben und Mixer der Audiokarte durch den audioerfassungs Filter umschließt. Jede Soundkarte kann mit dem Enumerator "System Geräte" ermittelt werden. Zum Anzeigen der Soundkarten in Ihrem System führen Sie GraphEdit aus, und wählen Sie aus der Kategorie audioerfassungs Quellen aus. Jeder Filter in dieser Kategorie ist eine separate Instanz des audioerfassungs Filters. (Siehe [Verwenden von GraphEdit](using-graphedit.md).)

**WDM-Streaminggeräte**

Neuere Hardware-Decoder und Erfassungs Karten entsprechen der Windows-Treibermodell (WDM)-Spezifikation. Diese Geräte verfügen über eine höhere Funktionalität als VFW-Geräte. WDM-Video Erfassungs Karten können Funktionen unterstützen, die unter VFW nicht verfügbar sind, einschließlich der Enumeration von Aufzeichnungs Formaten, der programmgesteuerten Steuerung von Video Parametern wie Hue und Helligkeit, programmgesteuerte Eingabeauswahl und TV-tunerunterstützung.

Zur Unterstützung von WDM-Streaminggeräten stellt DirectShow den ksproxy-Filter (ksproxy.ax) bereit. Ksproxy wurde als "Swiss Army Knife Filter" bezeichnet, da es so viele verschiedene Dinge tut. Die Anzahl der Pins im Filter und die Anzahl der vom Filter verfügbar gemachten com-Schnittstellen hängen von den Funktionen des zugrunde liegenden Treibers ab. Ksproxy wird im Filter Diagramm unter dem Namen "ksproxy" nicht angezeigt. Es wird immer der Anzeige Name des Geräts angezeigt, das in der Registrierung enthalten ist. Um die WDM-Geräte auf Ihrem System anzuzeigen, führen Sie GraphEdit aus, und wählen Sie aus den WDM-streamingkategorien aus. Auch wenn Sie nur eine WDM-Karte auf Ihrem System haben, kann diese Karte mehr als ein Gerät enthalten. Jedes Gerät wird als separater Filter dargestellt, und jeder dieser Filter ist tatsächlich ksproxy.

Eine Anwendung verwendet den Enumerator "System Geräte", um WDM-gerätermoniker auf dem System zu suchen. Ksproxy wird durch Aufrufen von **BindToObject** für den Moniker instanziiert. Da ksproxy alle Arten von WDM-Geräten darstellen kann, muss der Treiber abgefragt werden, um zu bestimmen, welche Eigenschaften vom Treiber unterstützt werden. Eigenschaften Sätze sind Auflistungen von Datenstrukturen, die von WDM-Treibern verwendet werden, sowie von einigen benutzermodusfiltern wie MPEG-2-Software Decodern. Ksproxy konfiguriert sich selbst so, dass die COM-Schnittstellen verfügbar gemacht werden, die diesen Eigenschaften Sätzen entsprechen. Ksproxy übersetzt die com-Methodenaufrufe in Eigenschaften Sätze und sendet diese an den Treiber. Hardware Anbieter können ksproxy durch Bereitstellen von Plug-Ins erweitern, bei denen es sich um anbieterspezifische Schnittstellen handelt, die die speziellen Funktionen eines Geräts verfügbar machen. Alle diese Details werden in der Anwendung ausgeblendet. Die Anwendung steuert das Gerät mithilfe von ksproxy auf dieselbe Weise wie jeder andere DirectShow-Filter.

**Kernel Streaming**

WDM-Geräte unterstützen Kernel Streaming, bei dem Daten vollständig im Kernel Modus gestreamt werden, ohne jemals in den Benutzermodus zu wechseln. Der Wechsel zwischen Kernel Modus und Benutzermodus ist Rechen intensiv. Das Kernel Streaming ermöglicht hohe Bitraten, ohne die Host-CPU zu belasten. WDM-basierte Filter können Kernel Streaming verwenden, um Multimedia-Daten direkt von einem Hardware Gerät an ein anderes zu übergeben, entweder auf derselben Karte oder auf einer anderen Karte, ohne dass die Daten in den Hauptspeicher des Systems kopiert werden.

Aus Sicht der Anwendung wird Sie so angezeigt, als ob die Daten von einem benutzermodusfilter zum nächsten verschoben werden. In der Praxis werden die Daten möglicherweise nie an den Benutzermodus übergeben. Sie werden stattdessen möglicherweise direkt von einem kernelmodusgerät zu einem anderen gestreamt, bis es auf der Grafikkarte gerendert wird. In einigen Szenarien, z. b. bei der Erfassung in einer Datei, ist es erforderlich, dass die Daten zu einem bestimmten Zeitpunkt vom Kernel Modus in den Benutzermodus übergehen Dieser Schalter erfordert jedoch nicht notwendigerweise, dass die Daten an einen neuen Speicherort im Arbeitsspeicher kopiert werden.

Anwendungsentwickler müssen sich im Allgemeinen nicht mit den Details des Kernel Streamings befassen, außer als Hintergrundinformationen. Ausführlichere Informationen zu WDM, Kernel Streaming, ksproxy und verwandten Themen finden Sie im Microsoft-DDK.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Das Filter Diagramm und dessen Komponenten](the-filter-graph-and-its-components.md)
</dt> </dl>

 

 




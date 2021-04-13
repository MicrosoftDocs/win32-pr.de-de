---
description: Netzwerk Quell Features
ms.assetid: a4e20ecb-c145-4823-ae59-f6fc88593d86
title: Netzwerk Quell Features
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e937a97cf743740d9cebf84ad477c52cdee5083
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104559421"
---
# <a name="network-source-features"></a>Netzwerk Quell Features

Die Netzwerkquelle stellt die Basis Implementierung für das Streaming von Mediendateien bereit und [**macht die imfmediasource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) -Schnittstelle verfügbar. Die spezifische Implementierung der Netzwerkquelle hängt von dem Protokoll ab, das zum Öffnen der Quelle verwendet wird, z. b. RTSP oder http. Die Protokoll spezifischen Netzwerk Quellen erweitern die grundlegende Netzwerkfunktionalität. Informationen zu den unterstützten Schemas und Protokollen finden Sie [unter Unterstützte Protokolle](supported-protocols.md).

Die Netzwerkquelle:

-   Implementiert Funktionen wie Caching, Proxy Erkennung und automatische Verbindungs Wiederherstellung.
-   Konvertiert Protokoll unabhängige Aufrufe vom quellresolver in Protokoll spezifische Aufrufe.
-   Interagiert mit der Socketschicht und dem Betriebssystem. Analysiert die SDP-Beschreibung und verwendet Sie als Konfigurationsdaten und liest Streamdaten aus der zugrunde liegenden Socketschicht. Beim Empfang ist die Netzwerkquelle für die Neuanordnung und das Anfordern von erneuten Übertragungen von Paketen verantwortlich.

## <a name="network-source-creation"></a>Netzwerk Quellen Erstellung

Das Erstellen einer Medienquelle für eine Quelle aus dem Netzwerk unterscheidet sich nicht von einer Medienquelle für eine lokale Datei. Die Anwendung übergibt die URL für die Quelle an [quellresolver](source-resolver.md) -Methoden, z. b. [**imfsourceresolver:: forateobjectfromurl**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) oder [**imfsourceresolver:: beginkreateobjectfromurl**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) und gibt das Flag für die MF- \_ Auflösung \_ MediaSource an. Weitere Informationen zur Verwendung dieses Flags finden Sie unter [using the Source Resolver](using-the-source-resolver.md).

Abhängig von dem von der Anwendung bereitgestellten Schema lädt der quellresolver das entsprechende Schema Handler-Objekt, das die [**IMF Schema Handler**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler) -Schnittstelle verfügbar macht. Die Anwendung kann den Schema Handler auch direkt verwenden, um die Netzwerkquelle durch Aufrufen von [**imfschemehandler:: begincreateobject**](/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-begincreateobject)zu erstellen.

Weitere Informationen finden Sie unter [Schema Handler und Byte-Stream Handler](scheme-handlers-and-byte-stream-handlers.md).

Media Foundation unterstützt keine Byte Datenströme für Netzwerk Quellen. Das Byte-Datenstrom Objekt wird nur im heruntergeladenen Inhalts Szenario unterstützt. Alle Daten werden so schnell wie möglich übertragen, sodass Sie als Datei auf dem lokalen Computer gespeichert werden können. Webserver stellen heruntergeladene Daten bereit. Nachdem der Download begonnen hat, erfolgt keine Kommunikation zwischen dem Client und dem Server. In diesem Fall wird das HTTP-Download Protokoll verwendet.

Wenn die Anwendung den Quell Konflikt Löser anfordert, ein bytestreamobjekt für die Schemas "http:", "MMS:" oder "RTSP:" zu erstellen, schlägt der-Vorgang mit dem Fehler "MF \_ E \_ nicht unterstützter Schema" fehl \_ .

> [!Note]  
> In Windows 7 unterstützt die Netzwerkquelle Windows Media Station-Dateien (. NSC). Diese Dateien werden beim Multicast Streaming von Medieninhalten über ein Netzwerk verwendet. Zum Erstellen der Netzwerkquelle für eine angegebene. NSC-Datei: die Anwendung muss den quellresolver verwenden.

 

Wenn die Anwendung den Schema Handler verwendet, ignoriert der asynchrone-Befehl den *dwFlags* -Parameter und gibt bei Abschluss einen Zeiger auf die Netzwerkquelle zurück.

Die folgende Abbildung zeigt den Datenfluss für das Medien Streaming mithilfe der Netzwerkquelle.

![Flussdiagramm, das Pfade von der Anwendung zum Streamingserver anzeigt, mit einer Schleife zwischen Netzwerkquelle und Medien Sitzung](images/3f9186ea-53ed-4a31-a097-92f39fa08624.gif)

## <a name="network-source-configuration"></a>Netzwerk Quell Konfiguration

In diesem Thema werden die von der Netzwerkquelle unterstützten Funktionen und die zugehörigen Konfigurationsoptionen beschrieben. Eine Anwendung kann die Netzwerkquelle konfigurieren, wenn das Netzwerk Quell Objekt erstellt wird. Diese Optionen werden in einem **IPropertyStore** -Objekt gespeichert, das von der Anwendung an den *prequicparameter* der Quell Konflikt Löser-Methoden oder [**imvschemehandler:: beginkreateobject**](/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-begincreateobject)übergeben werden muss.

### <a name="auto-reconnect"></a>Automatisch wiederherstellen der Verbindung

Die Funktion zum automatischen erneuten Verbinden der Netzwerkquelle ermöglicht es einem Client, automatisch erneut eine Verbindung mit dem Medienserver herzustellen, wenn die TCP-Verbindung mit dem Server fehlschlägt oder wenn der Client Pakete nicht empfangen kann. Wenn die Verbindung nicht hergestellt werden kann, versucht die Netzwerkquelle, mithilfe derselben Konfiguration, die in der vorherigen Verbindung verwendet wurde, erneut eine Verbindung mit dem Medienserver herzustellen. Der Vorgang zur erneuten Verbindung ist asynchron. Die Netzwerkquelle löst das [mereconnectstart](mereconnectstart.md) -Ereignis aus, wenn die Verbindung wieder hergestellt wird, und das [mereconnectend](mereconnectend.md) -Ereignis, wenn die erneute Verbindung erfolgreich ist oder fehlschlägt.

Wenn die Anzahl der Versuche zum erneuten verbinden den maximalen Wert überschreitet, der durch die [**\_ autoreconnectlimit-Eigenschaft von mnenetsource**](mfnetsource-autoreconnectlimit-property.md) festgelegt wird, wird der Vorgang zum erneuten Verbinden abgebrochen. Die Anzahl der Versuche zum erneuten Herstellen der Verbindung wird in der " [**MF NetSource"-Eigenschaft " \_ autoreconnectprogress**](mfnetsource-autoreconnectprogress-property.md) " gespeichert.

Die automatische Wiederherstellung der Verbindung ermöglicht die reibungslose Wiedergabe von Medieninhalten, auch wenn die TCP-Verbindung mit dem Medienserver ausfällt. Für eine reibungslose Wiedergabe muss der Client über ausreichend Daten (mindestens 1 bis 2 Minuten) im Cache verfügen, um die Wiedergabe bis zur erneuten Verbindungs Herstellung fortzusetzen. Die maximale Datenmenge, die von der Netzwerkquelle puffert werden kann, kann in der Eigenschaft " [**\_ maxbuffertimems" von MF-Quelle**](mfnetsource-maxbuffertimems-property.md) festgelegt werden.

### <a name="fast-streaming"></a>Schnelles Streaming

Der Netzwerk Quell Client fordert den Server auf, Daten am Anfang des Inhalts schneller zu streamen, als durch die Bitrate des Inhalts angegeben. Wenn der *schnelle Start* auf dem Server aktiviert ist, sendet der Server einen beschleunigten Bitrate-Datenstrom, sodass der Client eine ausreichende Datenmenge schneller als in Echtzeit Puffern kann. Dadurch wird die Benutzer Leistung verbessert, indem anfängliche Puffer Verzögerungen minimiert werden. Dies kann durch verschiedene Faktoren verursacht werden, wie z. b. eine geringe Geschwindigkeit des Client Computers oder des Netzwerks und die verfügbare Bandbreite.

Legen Sie die [**mfnetsource \_ acceleratedstreamingduration**](mfnetsource-acceleratedstreamingduration-property.md) -Eigenschaft fest, um die Menge der schnellen Streamingdaten anzugeben, die vom Client angefordert werden können. Wenn die Netzwerkquelle UDP als Transportprotokoll verwendet, geben Sie die maximale Menge an schnellen Streamingdaten an, indem Sie stattdessen die Eigenschaft " [**MF NetSource \_ maxudpacceleratedstreamingduration**](mfnetsource-maxudpacceleratedstreamingduration-property.md) " festlegen.

Schnelles Streaming auf dem Client ist auch über die Funktion " *schnelles Zwischenspeichern* " möglich – das Streaming von bedarfsgesteuerten Inhalten schneller als in Echtzeit und das Zwischenspeichern von Daten im lokalen Cache des Clients. Um diese Art von schnellem Streaming verwenden zu können, muss der schnelle Cache in der Netzwerkquelle aktiviert werden, und der Server muss ihn unterstützen. Wenn der Client Inhalt vom Server anfordert, prüft die Netzwerkquelle zunächst, ob der Inhalt bereits im Cache des Clients vorhanden ist. Wenn sich der Inhalt im lokalen Cache des Clients befindet und nicht abgelaufen ist, wird er gerendert. Wenn sich der Inhalt nicht im lokalen Cache befindet oder bereits abgelaufen ist, wird der Inhalt gestreamt und zwischengespeichert, und die Netzwerkquelle gibt ihn aus dem lokalen Cache wieder. In nachfolgenden Anforderungen werden für Wiedergabelisten nur fehlende Einträge zwischengespeichert und dann wiedergegeben. Wenn sich ein Wiedergabelisten Eintrag bereits im lokalen Cache des Clients befindet, wird er von dort wiedergegeben und nicht erneut zwischengespeichert.

Standardmäßig ist der schnelle Cache auf dem Netzwerk Quell Client aktiviert. Die folgenden Faktoren bestimmen jedoch auch, ob die Funktion verwendet wird:

-   Auf dem Client muss eine zusätzliche Bandbreite verfügbar sein, um den Inhalt schneller herunterladen und Zwischenspeichern zu können als die normale Geschwindigkeit.
-   Auf dem Client muss genügend Speicherplatz vorhanden sein. Wenn der Client nach dem Zwischenspeichern der angeforderten on-Demand-Inhalte über weniger als 100 MB freien Speicherplatz verfügt, wird er nicht zwischengespeichert, sondern gleichzeitig gestreamt und gerendert.

Die Funktion "schnelles Cache" wird durch die Eigenschaft " [**\_ cacheaktivierte MF-Quelle**](mfnetsource-cacheenabled-property.md) " gesteuert.

### <a name="buffer-management"></a>Pufferverwaltung

Die Netzwerkquelle stellt eine effiziente Puffer Verwaltung bereit, die den Puffer Status auf dem Client überwacht. Standardmäßig werden bei der Netzwerkquelle 5 Sekunden Daten beim Start Puffer angezeigt. Sie können diesen Wert konfigurieren, indem Sie die Eigenschaft " [**MF NetSource \_ BufferingTime**](mfnetsource-bufferingtime-property.md) " festlegen. Basierend auf diesem Eigenschafts Wert berechnet die Netzwerkquelle die Puffergröße, die ausreichend ist, um eine reibungslose und ununterbrochene Wiedergabe der Medieninhalte sicherzustellen. Wenn diese Eigenschaft auf 0 festgelegt ist, wird die Puffer Verwaltung deaktiviert. Wenn die Menge an Inhalt im Puffer gering ist, beginnt die Netzwerkquelle mit der Pufferung und löst das [mebufferingstarted](mebufferingstarted.md) -Ereignis aus, um anzugeben, dass die Pufferung begonnen hat. Beim Empfang dieses Ereignisses beendet die Pipeline das Rendering. Wenn die Pufferung fertiggestellt ist, löst die Netzwerkquelle das [mebufferingbeendete](mebufferingstopped.md) -Ereignis aus, und der Client kann das Rendering erneut starten.

Der Client beginnt mit dem Rendern des Inhalts, nachdem er die Menge der Daten gesammelt hat, die durch die Puffergröße des ersten Beispiels angegeben wird. Wenn dieser Wert niedriger als die berechnete Puffergröße ist, wird die Wiedergabe sofort gestartet. Dieses Verhalten ähnelt dem schnellen Start Feature.

Die [**\_ maxbuffertimems-Eigenschaft von MF NetSource**](mfnetsource-maxbuffertimems-property.md) speichert die maximale Datenmenge, die gepuffert werden kann.

### <a name="bandwidth-selection"></a>Bandbreiten Auswahl

Wenn ein Client eine Verbindung mit dem Medienserver herstellt, führt die Netzwerkquelle im Rahmen der Verbindungs Einrichtung eine *statische Paket paar* Messung aus, um die anfängliche Verknüpfungs Bandbreite zwischen Client und Server einzuschätzen. Basierend auf dem Ergebnis dieser Messung können vom Client Audio-und Videostreams ausgewählt werden, die innerhalb der geschätzten Bandbreite liegen. Dadurch wird die reibungslose Wiedergabe der Streamingmedieninhalte sichergestellt.

Während der Schnellstart Phase wird die *dynamische Paket paar* Messung durchgeführt. Bei diesem Vorgang empfängt der Client große Datenmengen, bei denen es sich um mehrere Pakete oder Stichproben handeln kann.

Das Ergebnis der dynamischen Paket paar Messung ist präziser als die von der statischen Paket paar Messung zurückgegebene Schätzung der Link Bandbreite, da der statische Paket paar Prozess ein einzelnes Paket mit fester Größe sendet, das möglicherweise keine exakten Ergebnisse für Netzwerke mit hoher Bandbreite liefert.

Die Anwendung kann die geschätzte Bandbreite mithilfe der Eigenschaft " [**MF NetSource \_ ppbandwidth**](mfnetsource-ppbandwidth-property.md) " erhalten.

Netzwerkbedingungen können sich dynamisch ändern, was zu einem Fehler bei der Wiedergabe der Netzwerkquelle führt. Die Netzwerkquelle kann die anfängliche Datenstrom Auswahl des Clients basierend auf der Empfangs Rate und dem Puffer Status ändern. Beispielsweise kann der Client während der Überlastung des Netzwerks zu einer niedrigeren Bitrate wechseln und zurück zu einer höheren Bitrate wechseln, wenn sich der Netzwerk Datenverkehr verbessert hat und der Client eine ausreichende Menge an gepuffertem Inhalt angesammelt hat.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Netzwerk in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




---
description: Media Foundation Attribute für ASF-Header Objekte
ms.assetid: 82d2bdeb-4ccf-4713-980e-59bddc7d9b6a
title: Media Foundation Attribute für ASF-Header Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4db74ccb03536c7766dd7e1564119edbd41d5dbe
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351599"
---
# <a name="media-foundation-attributes-for-asf-header-objects"></a>Media Foundation Attribute für ASF-Header Objekte

Das ASF-Header Objekt der obersten Ebene für eine Datei enthält mehrere ASF-unter Header Objekte. Das ContentInfo-Objekt speichert Informationen aus allen diesen Header Objekten und macht bestimmte Werte für eine Anwendung über Attribute verfügbar.

## <a name="file-properties-object"></a>Dateieigenschaften Objekt

Dieses Header Objekt ist in allen ASF-Dateien vorhanden. Diese Felder beschreiben die Attribute auf Dateiebene der gesamten Präsentation. In der folgenden Tabelle werden die Felder im Dateieigenschaften Objekt und die entsprechenden Präsentations deskriptorattribute aufgelistet.



| Objektfeld "Dateieigenschaften" | Präsentations deskriptorattribut                                                                            | BESCHREIBUNG                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| Datei-ID                      | [**Datei-ID für MF \_ PD \_ ASF \_ File Properties \_ \_**](mf-pd-asf-fileproperties-file-id-attribute.md)                  | Eindeutiger Bezeichner für diese Datei.                                                               |
| Dateigröße                    | [**gesamte MF- \_ PD- \_ \_ Datei \_ Größe**](mf-pd-total-file-size-attribute.md)                                         | Größe der Datei in Bytes.                                                                    |
| Erstellungsdatum                | [**Zeitpunkt der Erstellung der MF \_ PD- \_ \_ Dateieigenschaften \_ \_**](mf-pd-asf-fileproperties-creation-time-attribute.md)      | Das Datum und die Uhrzeit der Dateierstellung.                                                               |
| Anzahl von Datenpaketen           | [**MF-,-Paket- \_ \_ \_ Dateieigenschaften \_ Pakete**](mf-pd-asf-fileproperties-packets-attribute.md)                   | Anzahl von Datenpaketen im ASF-Datenobjekt.                                                 |
| Wiedergabedauer                | [**\_Dauer der \_ \_ \_ Wiedergabe \_ Dauer von MF PD ASF File Properties**](mf-pd-asf-fileproperties-play-duration-attribute.md)      | Benötigte Zeit für die Wiedergabe der Datei in 100-Nanosecond-Einheiten. Dieser Wert enthält die Vorabversion. |
| Sende Dauer                | [**\_Dauer der \_ \_ \_ Sende \_ Dauer von MF PD ASF File Properties**](mf-pd-asf-fileproperties-send-duration-attribute.md)      | Benötigte Zeit zum Senden der Datei in 100-Nanosecond-Einheiten.                                       |
| Ein Vorlauf ausgeführt                      | [**MF \_ PD \_ ASF \_ FileProperties- \_ Vorabversion**](mf-pd-asf-fileproperties-preroll-attribute.md)                   | Zeitspanne, die zum Puffern von Daten vor der Wiedergabe der Datei in 100-Nanosecond-Einheiten zu puffern ist.            |
| Flags                        | [**MF-und MF- \_ \_ dateproperties- \_ \_ Flags**](mf-pd-asf-fileproperties-flags-attribute.md)                       | Flags, die angeben, ob die Datei übertragen oder durchsuchbar ist.                                    |
| Minimale Datenpaket Größe     | [**MF \_ PD \_ ASF \_ File Properties \_ Min. \_ Paket \_ Größe**](mf-pd-asf-fileproperties-min-packet-size-attribute.md) | Minimale Größe der Datenpakete in der Datei (in Bytes).                                        |
| Maximale Datenpaket Größe     | [**\_maximal zulässige \_ \_ \_ \_ Paket \_ Größe für MF PD ASF File Properties**](mf-pd-asf-fileproperties-max-packet-size-attribute.md) | Maximale Größe der Datenpakete in der Datei (in Bytes).                                        |
| Maximale Bitrate              | [**MF \_ PD \_ ASF \_ File Properties \_ Max. \_ Bitrate**](mf-pd-asf-fileproperties-max-bitrate-attribute.md)          | Maximale sofortige Bitrate in Bits pro Sekunde.                                            |



 

## <a name="stream-properties-object"></a>Stream Properties-Objekt

Dieses Header Objekt beschreibt die Eigenschaften der Datenströme in der ASF-Datei. In Media Foundation wird dies durch das Profil Objekt und das Datenstrom-Konfigurationsobjekt verwaltet. Weitere Informationen finden Sie unter [Erstellen und Konfigurieren von ASF-Streams](creating-and-configuring-asf-streams.md).

## <a name="codec-list-object"></a>Codec-Listen Objekt

Wenn dieses Header Objekt vorhanden ist, stellt das [**MF \_ PD \_ ASF \_ codeclist**](mf-pd-asf-codeclist-attribute.md) -Attribut eine Liste von Codecs bereit, die verwendet wurden, um die Datenströme innerhalb der ASF-Datei zu codieren. Jeder Stream sollte seine Codec-Informationen in diesem-Objekt enthalten.

## <a name="script-command-object"></a>Skript Befehls Objekt

Wenn dieses Header Objekt vorhanden ist, gibt es eine Liste der Skript Befehle an, die in der ASF-Datei unterstützt werden. Ein Skript Befehl besteht aus einem Befehlstyp, einem Befehlsnamen und einer Präsentationszeit. Der Befehlstyp und der Befehls Name sind Zeichen folgen mit breit Zeichen. Diese Befehle können verwendet werden, um den Client zu benachrichtigen, eine Aktion zu einem bestimmten Zeitpunkt in der Präsentation auszuführen. Beispielsweise kann eine Anwendung den Befehlstyp "Dateiname" verwenden, um eine fortlaufende Sequenz von ASF-Dateien wiederzugeben.

Um die Liste der Skript Befehle zu erhalten, erhalten Sie das MF-Attribut "- [**\_ ASF- \_ \_ Skript**](mf-pd-asf-script-attribute.md) " aus dem Präsentations Deskriptor. Eine Anwendung sollte vor dem Starten der Wiedergabe alle Skript Befehle abrufen.

## <a name="marker-object"></a>Markerobjekt

Ein Marker ist ein Lesezeichen innerhalb einer ASF-Datei. Eine Anwendung kann Marker verwenden, um verschiedene Punkte innerhalb des Inhalts zu suchen. Jeder Marker besteht aus einem Markernamen, der zugeordneten Präsentationszeit und dem Offset vom Anfang der Datei. Das [**MF PD-Attribut " \_ \_ ASF \_ Marker**](mf-pd-asf-marker-attribute.md) " stellt eine Liste von Markern bereit, die für die Datei verfügbar sind.

## <a name="stream-bitrate-properties-object"></a>Eigenschaften Objekt der Stream-Bitrate

Dieser Header speichert die durchschnittliche Bitrate der einzelnen Datenströme, die in der ASF-Datei vorhanden sind. Dieser Wert wird auf dem Datenstrom Deskriptor für den Stream im [**MF SD-Attribut \_ \_ \_ streambitraten \_ Bitrate**](mf-sd-asf-streambitrates-bitrate-attribute.md) gespeichert.

## <a name="content-encryption-object"></a>Inhalts Verschlüsselungs Objekt

Dieses Header Objekt ist vorhanden, wenn der Inhaltsanbieter den Inhalt mithilfe von Microsoft Digital Rights Management geschützt hat. In der folgenden Tabelle sind die Felder im Inhalts Verschlüsselungs Objekt und die entsprechenden Präsentations deskriptorattribute aufgeführt:



| Inhalts Verschlüsselungs Objekt-Feld | Präsentations deskriptorattribut                                                                         | BESCHREIBUNG                                                                                        |
|---------------------------------|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| Geheime Daten                     | [**Daten für die MF \_ PD- \_ ASF- \_ Inhalts Verschlüsselung \_ \_**](mf-pd-asf-contentencryption-secret-data-attribute.md) | Ein Bytearray, das geheime Daten enthält.                                                                 |
| Schutztyp                 | [**MF \_ PD \_ ASF \_ contentencryption- \_ Typ**](mf-pd-asf-contentencryption-type-attribute.md)                | NULL-terminierte Zeichenfolge mit dem Wert "DRM".                                                       |
| Schlüssel-ID                          | [**\_Benutzer- \_ ID-Schlüssel-ID für MF PD ASF \_ \_**](mf-pd-asf-contentencryption-keyid-attribute.md)              | Eine auf NULL endenden Zeichenfolge, die den Schlüssel Bezeichner beschreibt.                                          |
| Lizenz-URL                     | [**Lizenz-URL für MF \_ PD \_ ASF \_ contentencryption \_ \_**](mf-pd-asf-contentencryption-license-url-attribute.md) | Eine auf NULL endende Zeichenfolge, die die URL enthält, von der die Lizenz zur Verwendung des Inhalts abgerufen wird. |



 

## <a name="extended-content-encryption-object"></a>Verschlüsselungs Objekt für erweiterte Inhalte

Dieses Header Objekt ist vorhanden, wenn der Inhalt vom Inhaltsanbieter mithilfe des Windows Media Rights Manager 7 SDK geschützt wurde. Das Paket für die MF-Version [**\_ \_ ASF \_ contentencryption \_ License \_ URL**](mf-pd-asf-contentencryption-license-url-attribute.md) stellt ein Bytearray bereit, das dem Datenfeld des Header Objekts entspricht. Dieses Feld ist erforderlich, um den Inhalt zu verwenden.

## <a name="extended-stream-properties-object"></a>Eigenschaften Objekt für erweiterte Streams

Dieser Header ist Teil des Header Erweiterungs Objekts. Das Eigenschaften Objekt für erweiterte Streams stellt Eigenschaften des Datenstroms bereit, die nicht im Stream Properties-Objekt definiert sind. Diese Eigenschaften werden hauptsächlich verwendet, um die "Leaky Bucket"-Parameter zu bestimmen, die vom Decoder verwendet werden. Diese Eigenschaften werden auch vom Encoder verwendet, wenn Daten komprimiert werden. Dies wird durch das Profil Objekt und das Datenstrom-Konfigurationsobjekt verwaltet. Weitere Informationen finden Sie unter [Erstellen und Konfigurieren von ASF-Streams](creating-and-configuring-asf-streams.md).

In der folgenden Tabelle werden die Eigenschaften Felder für erweiterte Stream-Eigenschaften und die entsprechenden streamdeskriptorattribute aufgelistet.



| Feld "erweiterte Datenstrom Eigenschaften" | Streamdeskriptorattribut                                                                                | BESCHREIBUNG                                                                                                              |
|----------------------------------|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Daten Bitrate                     | [**MF SD-Datei (in Bytes) \_ \_ \_ \_ \_ \_**](mf-sd-asf-extstrmprop-avg-data-bitrate-attribute.md)   | Durchschnittliche Datenrate in Bits pro Sekunde.                                                                                   |
| Puffergröße                      | [**MF \_ SD \_ ASF \_ extstraumprop \_ AVG \_ bufferSize**](mf-sd-asf-extstrmprop-avg-buffersize-attribute.md)        | Die Größe des Bucket-Bucket. Der Wert ist die Anzahl der Millisekunden, die Daten in den Puffer mit der durchschnittlichen Datenrate einfügen können.      |
| Alternative Daten Bitrate           | [**MF \_ SD \_ , \_ \_ maximal zulässige \_ Daten \_ Bitrate**](mf-sd-asf-extstrmprop-max-data-bitrate-attribute.md)   | Spitzen Datenrate in Stichen pro Sekunde. Die Spitzen Datenrate wird für Streams mit einer Variablen Bitrate verwendet.                    |
| Alternative Puffergröße            | [**MF \_ SD. \_ ASF \_ extstraumprop \_ Max \_ bufferSize**](mf-sd-asf-extstrmprop-max-buffersize-attribute.md)        | Maximale Größe des unzulässigen Bucket. Der Wert ist die Anzahl der Millisekunden, die Daten in den Puffer mit der Spitzen Datenrate einfügen können. |
| Stream-Sprach-ID               | [**MF \_ SD \_ - \_ Datei-ID der extstrinmprop- \_ Sprache \_ ID \_ Index**](mf-sd-asf-extstrmprop-language-id-index-attribute.md) | Die Sprache, die der Stream verwendet, als Index in der Liste der Sprachen im sprach Listen Objekt angegeben.         |



 

## <a name="language-list-object"></a>Sprach Listen Objekt

Dieses Header Objekt ist Teil des Header Erweiterungs Objekts. Falls vorhanden, bietet das MF PD-Attribut " [**\_ \_ ASF \_ langlist**](mf-pd-asf-langlist-attribute.md) " eine Liste von sprach bezeichatoren, die in der Datei unterstützt werden. Die Bezeichner sind mit RFC 1766 für die Angabe von Sprachen kompatibel.

## <a name="mutual-exclusion-object"></a>Gegenseitiges Ausschluss Objekt

Dieser Header gibt Gruppen von Streams und deren Eigenschaften an, von denen jeweils nur eine zugestellt wird. Weitere Informationen finden Sie unter [Verwenden des gegenseitigen Ausschlusses für ASF-Streams](using-mutual-exclusion-for-asf-streams.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASF-ContentInfo-Objekt](asf-contentinfo-object.md)
</dt> <dt>

[ASF-Header Objekt](asf-file-structure.md)
</dt> <dt>

[Unterstützung von ASF in Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 




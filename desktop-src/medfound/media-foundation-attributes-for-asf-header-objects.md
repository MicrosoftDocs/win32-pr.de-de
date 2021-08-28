---
description: Media Foundation Attribute für ASF-Headerobjekte
ms.assetid: 82d2bdeb-4ccf-4713-980e-59bddc7d9b6a
title: Media Foundation Attribute für ASF-Headerobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 426f0125373000c370f848239717b00aa2615fc16faa84270236704e124cb3bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061180"
---
# <a name="media-foundation-attributes-for-asf-header-objects"></a>Media Foundation Attribute für ASF-Headerobjekte

Das ASF-Headerobjekt der obersten Ebene für eine Datei enthält mehrere ASF-Unterheaderobjekte. Das ContentInfo-Objekt speichert Informationen aus allen diesen Headerobjekten und macht bestimmte Werte über Attribute für eine Anwendung verfügbar.

## <a name="file-properties-object"></a>Dateieigenschaftenobjekt

Dieses Headerobjekt ist in allen ASF-Dateien vorhanden. Diese Felder beschreiben die Attribute auf Dateiebene der gesamten Präsentation. In der folgenden Tabelle sind die Felder im Dateieigenschaftenobjekt und die entsprechenden Präsentationsdeskriptorattribute aufgeführt.



| Feld "File Properties Object" (Dateieigenschaftenobjekt) | Präsentationsdeskriptorattribut                                                                            | BESCHREIBUNG                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| Datei-ID                      | [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ FILE \_ ID**](mf-pd-asf-fileproperties-file-id-attribute.md)                  | Eindeutiger Bezeichner für diese Datei.                                                               |
| Dateigröße                    | [**MF \_ PD \_ \_ \_ GESAMTDATEIGRÖßE**](mf-pd-total-file-size-attribute.md)                                         | Größe der Datei in Bytes.                                                                    |
| Erstellungsdatum                | [**ERSTELLUNGSZEIT DER MF \_ \_ PD-ASF-DATEIEIGENSCHAFTEN \_ \_ \_**](mf-pd-asf-fileproperties-creation-time-attribute.md)      | Das Datum und die Uhrzeit der Dateierstellung.                                                               |
| Anzahl der Datenpakete           | [**MF \_ \_ PD-ASF-DATEIEIGENSCHAFTENPAKETE \_ \_**](mf-pd-asf-fileproperties-packets-attribute.md)                   | Anzahl der Datenpakete im ASF-Datenobjekt.                                                 |
| Wiedergabedauer                | [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ PLAY \_ DURATION**](mf-pd-asf-fileproperties-play-duration-attribute.md)      | Erforderliche Zeit für die Wiedergabe der Datei in Einheiten von 100 Nanosekunden. Dieser Wert enthält die Vorabrollzeit. |
| Sendedauer                | [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ SEND \_ DURATION**](mf-pd-asf-fileproperties-send-duration-attribute.md)      | Erforderliche Zeit zum Senden der Datei in Einheiten von 100 Nanosekunden.                                       |
| Vorabrolling                      | [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ PREROLL**](mf-pd-asf-fileproperties-preroll-attribute.md)                   | Zeitdauer zum Puffern von Daten vor der Wiedergabe der Datei in Einheiten von 100 Nanosekunden.            |
| Flags                        | [**MF \_ \_ PD-ASF-DATEIEIGENSCHAFTENFLAGS \_ \_**](mf-pd-asf-fileproperties-flags-attribute.md)                       | Flags, die angeben, ob die Datei übertragen oder durchsetzbar ist.                                    |
| Minimale Datenpaketgröße     | [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ MIN \_ PACKET \_ SIZE**](mf-pd-asf-fileproperties-min-packet-size-attribute.md) | Mindestgröße der Datenpakete in der Datei in Bytes.                                        |
| Maximale Datenpaketgröße     | [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ MAX \_ PACKET \_ SIZE**](mf-pd-asf-fileproperties-max-packet-size-attribute.md) | Maximale Größe der Datenpakete in der Datei in Bytes.                                        |
| Maximale Bitrate              | [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ MAX \_ BITRATE**](mf-pd-asf-fileproperties-max-bitrate-attribute.md)          | Maximale sofortige Bitrate in Bits pro Sekunde.                                            |



 

## <a name="stream-properties-object"></a>Stream Properties-Objekt

Dieses Headerobjekt beschreibt die Eigenschaften der Streams in der ASF-Datei. In Media Foundation wird dies vom Profilobjekt und dem Streamkonfigurationsobjekt verwaltet. Weitere Informationen finden Sie unter [Creating and Configuring ASF Streams](creating-and-configuring-asf-streams.md).

## <a name="codec-list-object"></a>Codec-Listenobjekt

Wenn dieses Headerobjekt vorhanden ist, stellt das [**MF \_ PD \_ ASF \_ CODECLIST-Attribut**](mf-pd-asf-codeclist-attribute.md) eine Liste von Codecs zur Auswahl, die zum Codieren der Streams in der ASF-Datei verwendet wurden. Jeder Stream sollte über seine Codecinformationen in diesem Objekt verfügen.

## <a name="script-command-object"></a>Skriptbefehlsobjekt

Wenn dieses Headerobjekt vorhanden ist, gibt es eine Liste von Skriptbefehlen an, die in der ASF-Datei unterstützt werden. Ein Skriptbefehl besteht aus einem Befehlstyp, einem Befehlsnamen und einer Präsentationszeit. Der Befehlstyp und der Befehlsname sind Breitzeichenzeichenfolgen. Diese Befehle können verwendet werden, um den Client zu benachrichtigen, eine Aktion an einem bestimmten Punkt in der Präsentation auszuführen. Beispielsweise kann eine Anwendung den Befehlstyp "FILENAME" verwenden, um eine fortlaufende Sequenz von ASF-Dateien wiederderherzustellen.

Um die Liste der Skriptbefehle zu erhalten, erhalten Sie das [**MF \_ PD \_ ASF \_ SCRIPT-Attribut**](mf-pd-asf-script-attribute.md) aus dem Präsentationsdeskriptor. Eine Anwendung sollte alle Skriptbefehle abrufen, bevor die Wiedergabe gestartet wird.

## <a name="marker-object"></a>Markerobjekt

Ein Marker ist ein Lesezeichen innerhalb einer ASF-Datei. Eine Anwendung kann Marker verwenden, um nach verschiedenen Punkten innerhalb des Inhalts zu suchen. Jeder Marker besteht aus einem Markernamen, der zugeordneten Präsentationszeit und dem Offset vom Anfang der Datei. Das [**MF \_ PD \_ ASF \_ MARKER-Attribut**](mf-pd-asf-marker-attribute.md) stellt eine Liste von Markern bereit, die für die Datei verfügbar sind.

## <a name="stream-bitrate-properties-object"></a>Eigenschaftenobjekt für Streambitrate

Dieser Header speichert die durchschnittliche Bitrate jedes Streams, der in der ASF-Datei vorhanden ist. Dieser Wert wird im Streamdeskriptor für den Stream im [**MF \_ SD \_ ASF \_ STREAMBITRATES \_ BITRATE-Attribut**](mf-sd-asf-streambitrates-bitrate-attribute.md) gespeichert.

## <a name="content-encryption-object"></a>Content Encryption-Objekt

Dieses Headerobjekt ist vorhanden, wenn der Inhaltsanbieter den Inhalt mithilfe von Microsoft Digital Rights Management. In der folgenden Tabelle sind die Felder im Content Encryption-Objekt und die entsprechenden Darstellungsdeskriptorattribute aufgeführt:



| Content Encryption Object-Feld | Präsentationsdeskriptorattribut                                                                         | BESCHREIBUNG                                                                                        |
|---------------------------------|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| Geheimnisdaten                     | [**MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ SECRET \_ DATA**](mf-pd-asf-contentencryption-secret-data-attribute.md) | Bytearray mit Geheimnisdaten.                                                                 |
| Schutztyp                 | [**MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ TYPE**](mf-pd-asf-contentencryption-type-attribute.md)                | Auf NULL beendete Zeichenfolge mit dem Wert "DRM".                                                       |
| Schlüssel-ID                          | [**MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ KEYID**](mf-pd-asf-contentencryption-keyid-attribute.md)              | Mit NULL beendete Zeichenfolge, die den Schlüsselbezeichner beschreibt.                                          |
| Lizenz-URL                     | [**MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ LICENSE \_ URL**](mf-pd-asf-contentencryption-license-url-attribute.md) | Auf NULL beendete Zeichenfolge, die die URL enthält, von der die Lizenz zum Verwenden des Inhalts erworben werden soll. |



 

## <a name="extended-content-encryption-object"></a>Erweitertes Inhaltsverschlüsselungsobjekt

Dieses Headerobjekt ist vorhanden, wenn der Inhaltsanbieter den Inhalt mithilfe des Windows Media Rights Manager 7 SDK geschützt hat. Das [**MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ LICENSE \_ URL-Attribut**](mf-pd-asf-contentencryption-license-url-attribute.md) stellt ein Bytearray zur Auswahl, das dem Feld Data des Headerobjekts entspricht. Dieses Feld ist erforderlich, um den Inhalt zu verwenden.

## <a name="extended-stream-properties-object"></a>Erweitertes Streameigenschaftenobjekt

Dieser Header ist Teil des Headererweiterungsobjekts. Das Objekt mit erweiterten Streameigenschaften stellt Eigenschaften des Streams zur, die nicht im Stream properties-Objekt definiert sind. Diese Eigenschaften werden hauptsächlich verwendet, um die "leaky bucket"-Parameter zu bestimmen, die vom Decoder verwendet werden. Diese Eigenschaften werden auch vom Encoder beim Komprimieren von Daten verwendet. Dies wird vom Profilobjekt und dem Streamkonfigurationsobjekt verwaltet. Weitere Informationen finden Sie unter [Creating and Configuring ASF Streams](creating-and-configuring-asf-streams.md).

In der folgenden Tabelle sind die Felder extended Stream Properties Object und die entsprechenden Streamdeskriptorattribute aufgeführt.



| Feld "Erweiterte Streameigenschaften" | Streamdeskriptorattribut                                                                                | BESCHREIBUNG                                                                                                              |
|----------------------------------|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Datenbitrate                     | [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ AVG \_ DATA \_ BITRATE**](mf-sd-asf-extstrmprop-avg-data-bitrate-attribute.md)   | Durchschnittliche Datenrate in Bits pro Sekunde.                                                                                   |
| Puffergröße                      | [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ AVG \_ BUFFERSIZE**](mf-sd-asf-extstrmprop-avg-buffersize-attribute.md)        | Undichte Bucketgröße. Der Wert ist die Anzahl von Millisekunden an Daten, die mit der durchschnittlichen Datenrate in den Puffer passen können.      |
| Alternative Datenbitrate           | [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ MAX \_ DATA \_ BITRATE**](mf-sd-asf-extstrmprop-max-data-bitrate-attribute.md)   | Spitzendatenrate in Bits pro Sekunde. Die Spitzendatenrate wird für Datenströme mit variabler Bitrate verwendet.                    |
| Alternative Puffergröße            | [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ MAX \_ BUFFERSIZE**](mf-sd-asf-extstrmprop-max-buffersize-attribute.md)        | Maximale Bucketgröße für Lecks. Der Wert ist die Anzahl von Millisekunden von Daten, die bei der Spitzendatenrate in den Puffer passen können. |
| Streamsprach-ID               | [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ LANGUAGE \_ ID \_ INDEX**](mf-sd-asf-extstrmprop-language-id-index-attribute.md) | Die Sprache, die der Stream verwendet, angegeben als Index in der Liste der Sprachen im Sprachlistenobjekt.         |



 

## <a name="language-list-object"></a>Sprachlistenobjekt

Dieses Headerobjekt ist Teil des Headererweiterungsobjekts. Falls vorhanden, stellt das [**MF \_ PD \_ ASF \_ LANGLIST-Attribut**](mf-pd-asf-langlist-attribute.md) eine Liste von Sprachbezeichnern bereit, die in der Datei unterstützt werden. Die Bezeichner sind mit RFC 1766 zum Angeben von Sprachen kompatibel.

## <a name="mutual-exclusion-object"></a>Objekt für gegenseitigen Ausschluss

Dieser Header gibt Gruppen von Streams und deren Eigenschaften an, von denen jeweils nur eine übermittelt wird. Weitere Informationen finden Sie unter [Using Mutual Exclusion for ASF Streams](using-mutual-exclusion-for-asf-streams.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASF ContentInfo-Objekt](asf-contentinfo-object.md)
</dt> <dt>

[ASF-Headerobjekt](asf-file-structure.md)
</dt> <dt>

[ASF-Unterstützung in Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 




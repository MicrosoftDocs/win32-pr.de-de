---
description: Media Foundation stellt die ASF-Medienquelle bereit, mit der eine Anwendung eine ASF-Datei in der Pipeline Ebene der Architektur darstellen kann.
ms.assetid: a2d2b382-d666-4a37-a6a9-0b839fbfbec3
title: ASF-Medienquelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75dc682d48339ce4ff707e7859a6962b9f5cfd92
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106364295"
---
# <a name="asf-media-source"></a>ASF-Medienquelle

Media Foundation stellt die ASF-Medienquelle bereit, mit der eine Anwendung eine ASF-Datei in der Pipeline Ebene der Architektur darstellen kann.

Um eine ASF-Datei wiederzugeben, kann eine Anwendung die ASF-Medienquelle verwenden, um Daten in eine Wiedergabe Pipeline zu übertragen. In einem Codierungs Szenario kann die Anwendung die ASF-Medienquelle als Quelle verwenden, um Sie in ein anderes Format zu konvertieren oder eine Datei mit höherem Bitrate in eine niedrigere Bitrate-Datei zu konvertieren, ohne die Formate zu ändern. Die ASF-Medienquelle muss in der Pipeline Schicht verwendet werden, d. h., eine Anwendung muss die Medien Sitzung verwenden, um den Vorgang zu steuern. Diese Zugriffsebene ermöglicht es den Anwendungen, Ereignisse zu erhalten, während die Medien Sitzung ausgeführt wird. Um auf den ASF-Inhalt Zugriff auf niedrigerer Ebene zu erhalten, muss eine Anwendung die Wrapper Komponenten der wmcontainer-Ebene verwenden.

Die ASF-Medienquelle implementiert die [**imfmediasource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) -Schnittstelle, bei der es sich um die generische Schnittstelle für Medienquellen in Media Foundation handelt. Wie jede andere Medienquelle bietet die ASF-Medienquelle einen Präsentations Deskriptor, der hauptsächlich das ASF-Header Objekt beschreibt. Außerdem bietet die ASF-Medienquelle streamdeskriptoren, die jeden Stream in den Medieninhalten darstellen. Weitere Informationen finden Sie unter [Struktur der ASF-Datei](asf-file-structure.md).

-   [Erstellen der ASF-Medienquelle](#creating-the-asf-media-source)
-   [Konfigurationseinstellungen für die ASF-Medienquelle](#configuration-settings-for-the-asf-media-source)
-   [Objektmodell der ASF-Medienquelle](#asf-media-source-object-model)
-   [ASF-Medienquellen Dienste](#asf-media-source-services)
    -   [Zeit Code Übersetzung](#timecode-translation)
-   [Zugehörige Themen](#related-topics)

## <a name="creating-the-asf-media-source"></a>Erstellen der ASF-Medienquelle

Zum Erstellen der ASF-Medienquelle muss die Anwendung den [quellresolver](source-resolver.md)verwenden. Zum Erstellen der ASF-Medienquelle muss die Anwendung die Quelle bereitstellen, für die der quellresolver die ASF-Medienquelle erstellt. Die Quell Informationen müssen bereitgestellt werden, indem entweder die URL der Quelldatei oder der Bytestream angegeben wird, der die Medien enthält. Wenn die Anwendung die Erstellung der ASF-Medienquelle durch Angabe der URL auswählt, muss Sie entweder [**imfsourceresolver:: anateobjectfromurl**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) für den synchronen Vorgang oder **imfsourceresolver:: begin... Endkreateobjectfromurl** für asynchronen Vorgang. Der Vorgang zum Erstellen der Medienquelle aus einem Bytestream ist ähnlich. Die Anwendung muss entweder [**imfsourceresolver:: forateobjectfrobare testream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream) für den synchronen Vorgang oder **imfsourceresolver:: begin... Endkreateobjectfromb** -Datenstrom für asynchronen Vorgang. Diese Aufrufe müssen die MF \_ Resolution \_ MediaSource im *dwFlags* -Parameter angeben. Weitere Informationen zur Verwendung dieses Flags finden Sie unter Using the Source Resolver.

Wenn die Anwendung eine URL angibt, kann die URL-Zeichenfolge für eine lokale Datei den Pfad der Mediendatei enthalten oder das Schema "file:" als Präfix aufweisen. Die Dateinamenerweiterung muss ". ASF", ". WM", "L". wma "oder". wmv "lauten. Bei einer ASF-Datei im Netzwerk erstellt der quellresolver die [Netzwerkquelle](network-source-features.md), in der die ASF-Medienquelle verwendet wird.

Während der Objekt Erstellung sucht der quellresolver die Liste der Schema Handler und der Byte Datenstrom Handler in der Systemregistrierung und lädt den nächstgelegenen übereinstimmenden Handler, der den Medieninhalt analysieren kann, und auch das Medienquellen Objekt unterhalb von. Unabhängig von der Methode, die zum Erstellen der Medienquelle (URL und Bytestream) verwendet wird, erstellt der quellresolver einen Bytestream und liest den Inhalt des Quell Mediums in den Bytestream. Weitere Informationen finden Sie unter [Schema Handler und Byte-Stream Handler](scheme-handlers-and-byte-stream-handlers.md).

Ein Codebeispiel zum Erstellen einer Medienquelle finden [Sie unter Using the Source Resolver](using-the-source-resolver.md).

## <a name="configuration-settings-for-the-asf-media-source"></a>Konfigurationseinstellungen für die ASF-Medienquelle

Der quellresolver fragt die Funktionen des zugrunde liegenden Bytestreams ab und bestimmt, welche Vorgänge für die neu erstellte Medienquelle zulässig sind. Eine dieser Funktionen ist das suchen. Wenn ein Suchvorgang zulässig ist, kann die Anwendung den Suchmodus angeben, den die Medienquelle beim Suchen eines bestimmten Punkts in der Präsentation verwendet.

Eine Anwendung kann während der Objekt Erstellung den Suchmodus festlegen, der von der Medienquelle verwendet werden soll. Nachdem die ASF-Medienquelle mit dem angegebenen Suchmodus erstellt wurde, kann Sie in der Medienquelle nicht geändert oder während einer Präsentation dynamisch geändert werden. Sucheinstellungen werden als Eigenschaften im Anwendungs Aufrufe der relevanten quellresolver-Methoden angegeben, die zum Erstellen der Medienquelle verwendet werden. Diese Eigenschaften werden in einem Eigenschaften Speicher festgelegt und an den *pproperties* -Parameter übergeben. Wenn diese Eigenschaften nicht übermittelt werden, funktioniert die Medienquelle mit den Standardeinstellungen. Weitere Informationen zum Festlegen dieser Eigenschaften finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).

Wenn die Suche zulässig ist, unterstützt die ASF-Medienquelle die folgenden Suchmodi:

-   Exakte Suche: in diesem Modus basiert die ASF-Medienquelle auf dem Objekt "ASF Index" der ASF-Datei. Wenn die Datei nicht über das Index Objekt verfügt, wird die exakte Suche deaktiviert, und je nach den von der Anwendung angegebenen Eigenschaften, die für die Medienquelle festgelegt werden, wird einer der anderen Modi verwendet.
-   Ungefähre Suche: Dieser Modus wird von der Anwendung angefordert, indem [**mfpkey \_ asfmediasource \_ approxseek**](mfpkey-asfmediasource-approxseek-property.md) im Eigenschaften Speicher an die entsprechenden quellresolver-Methoden übergeben wird. Das ungefähre suchen wird jedoch nur verwendet, wenn der Bytestream keine zeitbasierte Suche unterstützt. In diesem Modus wird von der Medienquelle eine Startzeit festgelegt, die relativ näher an der Suchzeit liegt. Wenn die ASF-Datei ein ASF-Index Objekt enthält, wird Sie zur Berechnung der Startzeit verwendet. Das ungefähre suchen ist weniger genau, aber schneller als die genaue Suche, da die Zeit, die zum Rendering des ersten Beispiels zur vordefinierten Startzeit benötigt wird, schneller ist.
-   Iteratives suchen: zum Festlegen dieses Modus muss die Anwendung die Eigenschaft " [mfpkey \_ asfmediasource \_ iterativeseekifnoindex](mfpkey-asfmediasource-iterativeseekifnoindex.md) " festlegen. Iteratives suchen ist ein Algorithmus, mit dem eine Position in einer ASF-Datei gefunden wird, die kein ASF-Index Objekt enthält. In diesem Modus bestimmt die Medienquelle eine grobe Schätzung des suchpunkts durchlesen des Byte Datenstrom Offsets. Es verwendet eine Reihe von Näherungen, die auf der durchschnittlichen Bitrate basieren, um die Ziel Suchzeit progressiv näher zu bringen. (Der Algorithmus ähnelt einer binären Suche.) Das iterative suchen kann länger dauern als die Suche mithilfe des Index Objekts, sodass es standardmäßig deaktiviert ist. Wenn Sie diese Eigenschaft festlegen, verwenden Sie die folgenden Eigenschaften, um die Suchparameter festzulegen: [mfpkey \_ asfmediasource \_ iterativeseek \_ Max \_ count](mfpkey-asfmediasource-iterativeseek-max-count.md)[mfpkey \_ asfmediasource \_ iterativeseek \_ Tolerance \_ in \_ millisecond](mfpkey-asfmediasource-iterativeseek-tolerance-in-millisecond.md). Diese Eigenschaften legen die maximale Anzahl von Iterationen bzw. die Toleranz fest. Der Algorithmus wird angehalten, wenn die maximale Anzahl von Iterationen erreicht wird, oder wenn ein Paket gefunden wird, dessen Entfernung von der Suchzeit innerhalb der angegebenen Toleranz liegt.

Kurz gesagt, hat die Anwendung die Möglichkeit, eine ungefähre oder iterative Suche auszuwählen, wenn die ASF-Datei kein ASF-Index Objekt enthält.

## <a name="asf-media-source-object-model"></a>Objektmodell der ASF-Medienquelle

Die ASF-Medienquelle implementiert die [**imfmediasource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) -Schnittstelle und macht die folgenden Schnittstellen verfügbar. Eine Anwendung kann einen Verweis auf diese Schnittstellen abrufen, indem Sie **imfmediasource:: QueryInterface** in der ASF-Medienquelle aufruft.



| Schnittstelle                                                | BESCHREIBUNG                                                                                                                                        |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Imfmediasource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                 | Für alle Medienquellen erforderlich.                                                                                                                    |
| [**IMF Media Event Generator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) | Für alle Medienquellen erforderlich. Ermöglicht es Anwendungen, Ereignisse aus der Medienquelle über die Medien Sitzung zu erhalten.                                 |
| [**IMF-Dienst**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                   | Fragt die Medienquelle für die angegebene Dienst Schnittstelle ab.                                                                                      |
| [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)               | Legt Eigenschaften für die Medienquelle fest und ruft diese ab. Jede Eigenschaft enthält einen beschreibenden Namen und einen Wert.                                               |
| [**IMF-Metadaten**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata)                       | Beschreibt die Metadaten für die ASF-Datei.                                                                                                           |
| [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider)       | Ruft eine Auflistung von Metadaten entweder für eine gesamte Präsentation oder für einen Datenstrom in der Präsentation ab.                                      |
| [**Imfratesupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)                 | Fragt den Bereich der unterstützten Wiedergabe Raten ab, einschließlich der umgekehrten Wiedergabe.                                                                |
| [**Imfratecontrol**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)                 | Ruft die Wiedergabe Rate ab oder legt Sie fest.                                                                                                                    |
| [**Imbtreudinput**](/windows/desktop/api/mfidl/nn-mfidl-imftrustedinput)               | Ruft die ITA für jeden der in der Quelle enthaltenen ASF-Streams ab.                                                                                  |
| [**Imfpmpclient**](/windows/desktop/api/mfidl/nn-mfidl-imfpmpclient)                     | Ermöglicht es einer Medienquelle, einen Zeiger auf die [**imfpmphost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) -Schnittstelle zu erhalten, die zum Erstellen von Objekten im PMP-Prozess verwendet wird. |
| [**IMF timecodetranslation**](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate)     | Konvertiert zwischen den Zeit Codes von Motion Picture und TV Engineers (SMPTE) und 100-Nanosecond-Zeiteinheiten.                              |



 

## <a name="asf-media-source-services"></a>ASF-Medienquellen Dienste

Die ASF-Medienquelle bietet verschiedene Dienste, die für die ASF-Datei vorgesehen sind. Um einen Zeiger auf einen bestimmten Dienst zu erhalten, muss die Anwendung einen der folgenden Dienst Bezeichner im [**mfgetservice**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice)-Befehl verwenden. Weitere Informationen finden Sie unter [Dienst Schnittstellen](service-interfaces.md).



| Dienst Bezeichner               | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MF- \_ Raten \_ Steuerungs \_ Dienst       | Mithilfe dieses Bezeichners kann eine Anwendung einen Zeiger auf die Schnittstellen [**imfratesupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) oder [**imfratecontrol**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) erhalten. Wenn Sie das von der Medienquelle implementierte Raten Unterstützungs Objekt verwenden, kann die Anwendung überprüfen, ob eine bestimmte Rate von der zugrunde liegenden ASF-Mediendatei unterstützt wird. Außerdem erhält Sie die schnellste und langsamste Rate. Mithilfe des Raten Steuerungs Objekts kann die Anwendung die Wiedergabe Rate erhalten und festlegen. Wenn die Anwendung eine bestimmte Rate für die Wiedergabe angibt, prüft die ASF-Medienquelle zunächst, ob die angeforderte Rate innerhalb der Datenübertragungsrate liegt (festgelegt durch "fasted" und "langsamste Raten"), und legt dann die Rate fest. Dies prüft nicht, ob Variablen Bedingungen vorhanden sind, da die Bitrate abhängig von der Netzwerkbandbreite jederzeit geändert werden kann. Weitere Informationen finden Sie unter [Raten Kontrolle](rate-control.md). |
| MF \_ - \_ Metadatenanbieter- \_ Dienst  | Mithilfe dieses Bezeichners kann die Anwendung einen Zeiger auf die [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) -Schnittstelle der ASF-Medienquelle erhalten. Diese Schnittstelle bietet Zugriff auf Informationen über die ASF-Datei, insbesondere die ASF-Header Objekte und die Streams, die im Medieninhalt enthalten sind. Header Informationen werden über Präsentations deskriptorattribute und streaminformationen über streamdeskriptorattribute bereitgestellt. Weitere Informationen zu diesen Attributen finden Sie unter [Media Foundation Attribute für ASF-Header Objekte](media-foundation-attributes-for-asf-header-objects.md). Zusätzlich zu den Informationen, die über Attribute verfügbar gemacht werden, gibt es auch beschreibende Metadaten, die als Eigenschaften festgelegt werden.                                                                                                 |
| MF- \_ Eigenschaften \_ Handler- \_ Dienst   | Mithilfe dieses Bezeichners kann die Anwendung einen Zeiger auf die [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Schnittstelle der ASF-Medienquelle erhalten. Der Eigenschaften Speicher enthält alle Metadaten, die mit der ASF-Datei verknüpft sind. Dieser Bezeichner ist neu in Windows 7 und ersetzt den MF- \_ \_ Metadatenanbieter- \_ Dienst zum erhalten von Metadateneigenschaften.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| MF-Quell \_ Statistik \_ Dienst | Weitere Informationen finden Sie unter Abrufen von Netzwerk Statistiken in der [Client Protokollierung](client-logging.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| MF- \_ Zeit Code \_ Dienst            | Mithilfe dieses Bezeichners kann die Anwendung einen Zeiger auf die [**imftimecodetranslation**](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate) -Schnittstelle der Medienquelle erhalten. Diese Implementierung kann verwendet werden, um Zeit Code Übersetzungen, wie z. b. das Umrechnen von SMPTE-Zeit Code in 100-Nano-Einheiten und zurück.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

### <a name="timecode-translation"></a>Zeit Code Übersetzung

Die ASF-Medienquelle bietet einen Zeit Code Übersetzungsdienst, mit dem Ihre Anwendung SMPTE-Zeit Code in die nächste Präsentationszeit (in 100-Nanosecond-Einheit) konvertieren kann. Umgekehrt kann die Anwendung auch den Zeit Code für eine angeforderte Präsentationszeit erhalten. Der Dienst ist über die [**IMF timecodetranslation**](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate) -Schnittstelle verfügbar, die von der ASF-Medienquelle implementiert wird. Die Methodenaufrufe für diesen Schnittstellen Zeiger sind asynchron, der aus dem Haupt Anwendungs Thread ausgeführt werden kann, ohne dass die Benutzeroberfläche der Anwendung blockiert wird.

In den folgenden Schritten wird das Verfahren für Zeit Code Übersetzung zusammengefasst:

1.  Abrufen eines Zeigers auf die [**imftimecodetranslation**](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate) -Schnittstelle der ASF-Medienquelle durch Aufrufen von " [**mfgetservice**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) " und angeben des Konfigurations-ID- **\_ \_ Dienst** Bezeichners.
2.  Aufrufen von [**imftimecodetranslation:: beginconverttimecodetohns**](/windows/desktop/api/mfidl/nf-mfidl-imftimecodetranslate-beginconverttimecodetohns) oder [**imftimecodetranslation:: beginconverthnstotimecode**](/windows/desktop/api/mfidl/nf-mfidl-imftimecodetranslate-beginconverthnstotimecode) und angeben der Zeit, die übersetzt werden soll. Für **beginconverttimecodeumhns** muss der Zeit Code als [**PROPVARIANT**](/windows/win32/api/propidl/ns-propidl-propvariant) -Variable mit dem **VT \_ I8** -Datentyp angegeben werden. Die **beginconverthnstotimecode** -Methode erfordert die Zeit in 100-Nanosecond-Einheiten als [**MF-Zeittyp**](mftime.md) .
3.  Schließen Sie den asynchronen Vorgang ab, indem Sie [**imftimecodetranslation:: endconverttimecodetohns**](/windows/desktop/api/mfidl/nf-mfidl-imftimecodetranslate-endconverttimecodetohns) oder **imftimecodetranslation:: endconverttimecodetohns** entsprechend aufrufen.

Während der Erstellung der Medienquelle erstellt der quellresolver einen Bytestream für die Datei, aus der die Medienquelle den ASF-Inhalt liest. Damit die Zeit Konvertierungen erfolgreich ausgeführt werden können, muss der Bytestream, der der ASF-Datei zugeordnet ist, Suchfunktionen aufweisen. Andernfalls ruft die Anwendung den Fehler "MF \_ E \_ Bytestream \_ nicht \_ durchsuchbar"  ab. Eine weitere Anforderung für Zeit Konvertierungen besteht darin, dass die von der ASF-Medienquelle dargestellte ASF-Datei über ASF-Index Objekte verfügen muss. Die Präsentations Zeiten und die Zeit Codes werden aus den ASF-Index Objekten extrahiert, die alle Indizes und die entsprechenden Such Punkte für die ASF-Datei verwalten. Für die Zeit-zu-Zeit-Code Übersetzung in der Präsentation muss die ASF-Datei ein einfaches Index Objekt enthalten. für die Zeit Code-zu-Präsentation-Zeit Übersetzung muss die ASF-Datei über ein Index Objekt verfügen. Die Konvertierungs Vorgänge basieren auf dem zugrunde liegenden *Indexer* (wmcontainer-Komponente) zum Analysieren und Lesen des Index Objekts, das der ASF-Datei zugeordnet ist. Wenn die Datei kein Index Objekt enthält, empfängt die Anwendung asynchron den Fehlercode für die MF- \_ E \_ ohne \_ Index.

Um die von der Anwendung angeforderte Zeit zu übersetzen, listet die Medienquelle die Streams in der Datei auf und findet den Stream, der das entsprechende ASF-Index-Objekt enthält. Wenn ein solcher Stream gefunden wird, analysiert die Medienquelle, dass die ASF-Pakete des Streams analysiert werden, bis der richtige Zeit Code erreicht wird. Nachdem Sie das richtige Beispiel gefunden hat, wird die entsprechende Präsentationszeit oder der Zeit Code aus dem Beispiel abgerufen und an den Aufrufer zurückgegeben.

### <a name="script-command-support"></a>Skript Befehls Unterstützung

Wenn Sie eine ASF-Topologie erstellen, die einen Skript Datenstrom enthält, wird der Topologie ein Skript-Stream-Knoten hinzugefügt. Dieser Knoten sendet IMF Samples zum richtigen Zeitpunkt. Das imfsample, das vom Skript Quellknoten bereitgestellt wird, speichert die Daten in imfmediabuffer, das mit dem Beispiel verknüpft ist. Sie können CopyTo Buffer für das Beispiel zum Abrufen eines imfmediabuffer und zum anschließenden Abrufen der Sperre für den Puffer abrufen, um die Daten abzurufen. 

Die Skript Datenstrom-Nutzlasten werden als Typzeichenfolge in den Puffer gepackt, gefolgt von NULL, gefolgt von der Befehls Zeichenfolge, gefolgt von NULL. Zeichen folgen sind im ASF-Format Unicode.

Eine Nutzlast könnte z. b. wie folgt aussehen (wobei \ 0 ein NULL-Zeichen angibt):

*Url\0http://contoso.com\0*

*Text\0this is a caption\0*



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Komponenten der Pipeline Schicht-ASF](pipeline-layer-asf-components.md)
</dt> <dt>

[Unterstützung von ASF in Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 

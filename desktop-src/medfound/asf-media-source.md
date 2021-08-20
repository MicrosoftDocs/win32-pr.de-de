---
description: Media Foundation stellt die ASF-Medienquelle bereit, mit der eine Anwendung eine ASF-Datei auf der Pipelineebene der Architektur darstellen kann.
ms.assetid: a2d2b382-d666-4a37-a6a9-0b839fbfbec3
title: ASF-Medienquelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b3222f32649aa5cb3f4d1d4688a9f7fb7402167e7831377fd8b04d6c879e23b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117881151"
---
# <a name="asf-media-source"></a>ASF-Medienquelle

Media Foundation stellt die ASF-Medienquelle bereit, mit der eine Anwendung eine ASF-Datei auf der Pipelineebene der Architektur darstellen kann.

Um eine ASF-Datei wiederzugeben, kann eine Anwendung die ASF-Medienquelle verwenden, um Daten in eine Wiedergabepipeline zu feeden. In einem Codierungsszenario kann die Anwendung die ASF-Medienquelle als Quelle verwenden, um in ein anderes Format zu konvertieren oder eine Datei mit höherer Bitrate in eine Datei mit niedrigerer Bitrate zu konvertieren, ohne die Formate zu ändern. Die ASF-Medienquelle muss in der Pipelineebene verwendet werden, d. h., eine Anwendung muss die Mediensitzung verwenden, um den Vorgang zu steuern. Diese Zugriffsebene ermöglicht es den Anwendungen, Ereignisse abzurufen, während die Mediensitzung ausgeführt wird. Um zugriff auf den ASF-Inhalt auf niedrigerer Ebene zu erhalten, muss eine Anwendung die WMContainer Layer ASF-Komponenten verwenden.

Die ASF-Medienquelle implementiert die [**INTERFACESMediaSource-Schnittstelle,**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) die die generische Schnittstelle für Medienquellen in Media Foundation ist. Wie jede andere Medienquelle stellt die ASF-Medienquelle einen Präsentationsdeskriptor bereit, der in erster Linie das ASF-Headerobjekt beschreibt. Darüber hinaus stellt die ASF-Medienquelle Streamdeskriptoren bereit, die jeden Stream im Medieninhalt darstellen. Weitere Informationen finden Sie unter [ASF-Dateistruktur.](asf-file-structure.md)

-   [Erstellen der ASF-Medienquelle](#creating-the-asf-media-source)
-   [Konfigurations-Einstellungen für die ASF-Medienquelle](#configuration-settings-for-the-asf-media-source)
-   [ASF-Medienquellobjektmodell](#asf-media-source-object-model)
-   [ASF-Medienquelldienste](#asf-media-source-services)
    -   [Zeitcodeübersetzung](#timecode-translation)
-   [Zugehörige Themen](#related-topics)

## <a name="creating-the-asf-media-source"></a>Erstellen der ASF-Medienquelle

Um die ASF-Medienquelle zu erstellen, muss die Anwendung den [Quell-Resolver](source-resolver.md)verwenden. Um die ASF-Medienquelle zu erstellen, muss die Anwendung die Quelle angeben, für die der Quell resolver die ASF-Medienquelle erstellt. Die Quellinformationen müssen entweder durch Angeben der URL der Quelldatei oder des Bytestreams bereitgestellt werden, der die Medien enthält. Wenn die Anwendung sich entscheidet, die ASF-Medienquelle durch Angabe der URL zu erstellen, muss sie entweder [**"SFCSourceResolver::CreateObjectFromURL"**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) für den synchronen Vorgang oder **"SFCSourceResolver::Begin..." aufrufen. EndCreateObjectFromURL** für asynchrone Vorgänge. Der Prozess zum Erstellen der Medienquelle aus einem Bytestream ist ähnlich. Die Anwendung muss entweder [**EINEN DERSOURCEResolver::CreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream) für einen synchronen Vorgang oder **EINEN SOURCEResolver::Begin... aufrufen. EndCreateObjectFromBytestream** für asynchrone Vorgänge. Diese Aufrufe müssen MF \_ RESOLUTION \_ MEDIASOURCE im *dwFlags-Parameter* angeben. Weitere Informationen zur Verwendung dieses Flags finden Sie unter Verwenden des Quelllösers.

Wenn die Anwendung eine URL für eine lokale Datei angibt, kann die URL-Zeichenfolge den Pfad der Mediendatei enthalten oder dem Schema "file: " vorangestellt werden. Die Dateinamenerweiterung muss ".asf", ".wm", L".wma" oder ".wmv" sein. Für eine ASF-Datei im Netzwerk erstellt der Quell resolver die [Netzwerkquelle](network-source-features.md), die die ASF-Medienquelle verwendet.

Während des Objekterstellungsprozesses sucht der Quell resolver die Liste der Schemahandler und der Bytestreamhandler in der Systemregistrierung und lädt den nächstgelegenen übereinstimmenden Handler, der den Medieninhalt analysieren und darunter auch das Medienquellobjekt erstellen kann. Unabhängig von der Methode zum Erstellen der Medienquelle (URL und Bytestream) erstellt der Quell resolver einen Bytestream und liest den Inhalt der Quellmedien in den Bytestream. Weitere Informationen finden Sie unter [Schemahandler und Byte-Stream Handler.](scheme-handlers-and-byte-stream-handlers.md)

Ein Codebeispiel zum Erstellen einer Medienquelle finden Sie unter [Verwenden des Quell resolvers.](using-the-source-resolver.md)

## <a name="configuration-settings-for-the-asf-media-source"></a>Konfigurations-Einstellungen für die ASF-Medienquelle

Der Quell resolver fragt die Funktionen des zugrunde liegenden Bytestreams ab und bestimmt, welche Vorgänge für die neu erstellte Medienquelle zulässig sind. Eine dieser Funktionen ist die Suche. Wenn ein Suchvorgang zulässig ist, kann die Anwendung den Suchmodus angeben, den die Medienquelle verwendet, während sie zu einem bestimmten Punkt in der Präsentation sucht.

Eine Anwendung kann den Suchmodus für die Medienquelle während der Objekterstellung festlegen. Nachdem die ASF-Medienquelle mit dem angegebenen Suchmodus erstellt wurde, kann sie nicht in der Medienquelle geändert oder während einer Präsentation dynamisch geändert werden. Sucheinstellungen werden als Eigenschaften im Aufruf der Anwendung an die relevanten Quell resolver-Methoden angegeben, die zum Erstellen der Medienquelle verwendet werden. Diese Eigenschaften werden in einem Eigenschaftenspeicher festgelegt und an den *pProps-Parameter* übergeben. Wenn diese Eigenschaften nicht übergeben werden, funktioniert die Medienquelle mit den Standardeinstellungen. Weitere Informationen zum Festlegen dieser Eigenschaften finden Sie unter [Konfigurieren einer Medienquelle.](configuring-a-media-source.md)

Wenn suchen zulässig ist, unterstützt die ASF-Medienquelle die folgenden Suchmodi:

-   Genaue Suche: In diesem Modus basiert die ASF-Medienquelle auf dem ASF-Indexobjekt der ASF-Datei. Wenn die Datei nicht über das Indexobjekt verfügt, ist die genaue Suche deaktiviert, und einer der anderen Modi wird abhängig von den von der Anwendung angegebenen Eigenschaften verwendet, die für die Medienquelle festgelegt sind.
-   Ungefähre Suche: Dieser Modus wird von der Anwendung angefordert, indem [**MFPKEY \_ ASFMediaSource \_ ApproxSeek**](mfpkey-asfmediasource-approxseek-property.md) im Eigenschaftenspeicher an die relevanten Quell resolver-Methoden übergeben wird. Die ungefähre Suche wird jedoch nur verwendet, wenn der Bytestream keine zeitbasierte Suche unterstützt. In diesem Modus bestimmt die Medienquelle eine Startzeit, die relativ näher an der Suchzeit liegt. Wenn die ASF-Datei ein ASF-Indexobjekt enthält, wird sie zum Berechnen der Startzeit verwendet. Die ungefähre Suche ist weniger genau, aber schneller als die genaue Suche, da die Zeit, die zum Rendern der ersten Stichprobe zur vordefinierten Startzeit erforderlich ist, schneller ist.
-   Iterative Suche: Um diesen Modus festzulegen, muss die Anwendung die [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex-Eigenschaft](mfpkey-asfmediasource-iterativeseekifnoindex.md) festlegen. Iterative Suche ist ein Algorithmus, um eine Position in einer ASF-Datei zu finden, die kein ASF-Indexobjekt enthält. In diesem Modus bestimmt die Medienquelle eine grobe Schätzung des Suchpunkts, indem der Bytestreamoffset gelesen wird. Es verwendet eine Reihe von Näherungswerten, die auf der durchschnittlichen Bitrate basieren, um sich der Suchzeit des Ziels schrittweise anzunähern. (Der Algorithmus ähnelt einer binären Suche.) Die iterative Suche kann länger dauern als die Suche mithilfe des Indexobjekts, sodass sie standardmäßig deaktiviert ist. Wenn Sie diese Eigenschaft festlegen, verwenden Sie die folgenden Eigenschaften, um die Suchparameter festzulegen: [MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ Max \_ Count](mfpkey-asfmediasource-iterativeseek-max-count.md)[MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ Tolerance In \_ \_ MilliSecond](mfpkey-asfmediasource-iterativeseek-tolerance-in-millisecond.md). Diese Eigenschaften legen die maximale Anzahl von Iterationen bzw. die Toleranz fest. Der Algorithmus hält an, wenn er die maximale Anzahl von Iterationen erreicht, oder wenn er ein Paket findet, dessen Abstand von der Suchzeit innerhalb der angegebenen Toleranz liegt.

Kurz gesagt hat die Anwendung die Möglichkeit, eine ungefähre oder iterative Suche auszuwählen, wenn die ASF-Datei kein ASF-Indexobjekt enthält.

## <a name="asf-media-source-object-model"></a>ASF-Medienquellobjektmodell

Die ASF-Medienquelle implementiert die [**INTERFACESMediaSource-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) und macht die folgenden Schnittstellen verfügbar. Eine Anwendung kann einen Verweis auf diese Schnittstellen abrufen, indem **SIE DIE SOURCEMEDIASource::QueryInterface** für die ASF-Medienquelle aufrufen.



| Schnittstelle                                                | BESCHREIBUNG                                                                                                                                        |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WFMEDIASOURCE**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                 | Erforderlich für alle Medienquellen.                                                                                                                    |
| [**WFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) | Erforderlich für alle Medienquellen. Ermöglicht Anwendungen das Abrufen von Ereignissen aus der Medienquelle über die Mediensitzung.                                 |
| [**VERZRGETService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                   | Fragt die Medienquelle nach der angegebenen Dienstschnittstelle ab.                                                                                      |
| [**Ipropertystore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)               | Legt Eigenschaften für die Medienquelle fest und ruft sie ab. Jede Eigenschaft enthält einen beschreibenden Namen und einen Wert.                                               |
| [**VERINNUNGMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata)                       | Beschreibt die Metadaten für die ASF-Datei.                                                                                                           |
| [**PILLARMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider)       | Ruft eine Auflistung von Metadaten ab, entweder für eine gesamte Präsentation oder für einen Stream in der Präsentation.                                      |
| [**1000000000**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)                 | Fragt den Bereich der unterstützten Wiedergaberaten ab, einschließlich umgekehrter Wiedergabe.                                                                |
| [**THICKNESSRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)                 | Ruft die Wiedergaberate ab oder legt sie fest.                                                                                                                    |
| [**TRUSTTrustedInput**](/windows/desktop/api/mfidl/nn-mfidl-imftrustedinput)               | Ruft den ITA für jeden asf-Datenstrom ab, der in der Quelle enthalten ist.                                                                                  |
| [**IMFPMPClient**](/windows/desktop/api/mfidl/nn-mfidl-imfpmpclient)                     | Ermöglicht es einer Medienquelle, einen Zeiger auf die [**IMFPMPHost-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) zu empfangen, die zum Erstellen von Objekten im PMP-Prozess verwendet wird. |
| [**CODTIMECODETranslate**](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate)     | Konvertiert zeitcodes zwischen Society of Motion Picture und Tv Engineers (SMPTE) und Zeiteinheiten von 100 Nanosekunden.                              |



 

## <a name="asf-media-source-services"></a>ASF-Medienquelldienste

Die ASF-Medienquelle stellt verschiedene Dienste bereit, die für die ASF-Datei gelten. Um einen Zeiger auf einen bestimmten Dienst abzurufen, muss die Anwendung einen der folgenden Dienstbezeichner in ihrem Aufruf von [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice)verwenden. Weitere Informationen finden Sie unter [Dienstschnittstellen.](service-interfaces.md)



| Dienstbezeichner               | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MF \_ RATE \_ CONTROL \_ SERVICE       | Mithilfe dieses Bezeichners kann eine Anwendung einen Zeiger auf die Schnittstellen [**"THICKNESSRateSupport"**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) oder [**"POINTERRateControl"**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) abrufen. Mithilfe des von der Medienquelle implementierten Ratenunterstützungsobjekts kann die Anwendung überprüfen, ob eine bestimmte Rate von der zugrunde liegenden ASF-Mediendatei unterstützt wird, um auch die schnellste und langsamste Rate zu erzielen. Mithilfe des Rate Control-Objekts kann die Anwendung die Wiedergaberate abrufen und festlegen. Wenn die Anwendung eine bestimmte Rate für die Wiedergabe angibt, überprüft die ASF-Medienquelle zunächst, ob die angeforderte Rate innerhalb der Ratenbegrenzungen liegt (bestimmt durch schnelle und langsamste Raten), und legt dann die Rate fest. Dies überprüft nicht die Variablenbedingungen, da sich die Bitrate je nach Netzwerkbandbreite jederzeit ändern kann. Weitere Informationen hierzu unter [Ratensteuerung.](rate-control.md) |
| MF \_ METADATA \_ PROVIDER \_ SERVICE  | Mit diesem Bezeichner kann die Anwendung einen Zeiger auf die [**INTERFACESMetadataProvider-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) der ASF-Medienquelle abrufen. Diese Schnittstelle bietet Zugriff auf Informationen zur ASF-Datei, insbesondere zu den ASF-Headerobjekten und den Streams, die in den Medieninhalten enthalten sind. Headerinformationen werden über Darstellungsdeskriptorattribute verfügbar gemacht, und Streaminformationen werden über Streamdeskriptorattribute bereitgestellt. Weitere Informationen zu diesen Attributen finden Sie unter [Media Foundation Attribute für ASF-Headerobjekte.](media-foundation-attributes-for-asf-header-objects.md) Neben Informationen, die über Attribute verfügbar gemacht werden, gibt es auch beschreibende Metadaten, die als Eigenschaften festgelegt werden.                                                                                                 |
| \_ \_ MF-EIGENSCHAFTENHANDLERDIENST \_   | Mit diesem Bezeichner kann die Anwendung einen Zeiger auf die [**IPropertyStore-Schnittstelle**](/windows/win32/api/propsys/nn-propsys-ipropertystore) der ASF-Medienquelle abrufen. Der Eigenschaftenspeicher enthält alle Metadaten, die sich auf die ASF-Datei beziehen. Dieser Bezeichner ist neu in Windows 7 und ersetzt MF \_ METADATA PROVIDER SERVICE zum Abrufen von \_ \_ Metadateneigenschaften.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| MFNETSOURCE \_ STATISTICS \_ SERVICE | Weitere Informationen finden Sie unter Abrufen von Netzwerkstatistiken in der [Clientprotokollierung.](client-logging.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| MF \_ TIMECODE \_ SERVICE            | Mithilfe dieses Bezeichners kann die Anwendung einen Zeiger auf die [**POINTERTimecodeTranslate-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate) der Medienquelle abrufen. Diese Implementierung kann verwendet werden, um Zeitcodeübersetzungen durchzuführen, z. B. das Konvertieren von SMPTE-Zeitcode in Einheiten von 100 Nano sekunden und zurück.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

### <a name="timecode-translation"></a>Zeitcodeübersetzung

Die ASF-Medienquelle bietet einen Zeitcodeübersetzungsdienst, mit dem Ihre Anwendung SMPTE-Zeitcode in die nächste Präsentationszeit (in einer Einheit von 100 Nanosekunden) konvertieren kann. Umgekehrt kann die Anwendung auch den Zeitcode für eine angeforderte Präsentationszeit abrufen. Der Dienst ist über die [**INTERFACESTimecodeTranslate-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate) verfügbar, die von der ASF-Medienquelle implementiert wird. Die Methodenaufrufe für diesen Schnittstellenzeiger sind asynchron und können von Ihrem Hauptanwendungsthread ausgeführt werden, ohne die Benutzeroberfläche Ihrer Anwendung zu blockieren.

In den folgenden Schritten wird das Verfahren für die Zeitcodeübersetzung zusammengefasst:

1.  Rufen Sie durch Aufrufen von [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) und Angeben des MF TIMECODE SERVICE-Bezeichners einen Zeiger auf die [**SCHNITTSTELLE "POINTERTimecodeTranslate"**](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate) der ASF-Medienquelle ab. **\_ \_**
2.  Rufen Sie [**DIE Klammer AUFTIMECODETranslate::BeginConvertTimecodeToHNS**](/windows/desktop/api/mfidl/nf-mfidl-imftimecodetranslate-beginconverttimecodetohns) oder [**DENTIMECODETranslate::BeginConvertHNSToTimecode**](/windows/desktop/api/mfidl/nf-mfidl-imftimecodetranslate-beginconverthnstotimecode) auf, und geben Sie die zu übersetzende Zeit an. Für **BeginConvertTimecodeToHNS** muss der Zeitcode als [**PROPVARIANT-Variable**](/windows/win32/api/propidl/ns-propidl-propvariant) mit **VT \_ I8-Datentyp** angegeben werden. Die **BeginConvertHNSToTimecode-Methode** erfordert die Zeit in Einheiten von 100 Nanosekunden als [**MFTIME-Typ.**](mftime.md)
3.  Schließen Sie den asynchronen Vorgang ab, indem Sie [**DIE Klammern UNDTIMECODETranslate::EndConvertTimecodeToHNS**](/windows/desktop/api/mfidl/nf-mfidl-imftimecodetranslate-endconverttimecodetohns) oder **DENTIMECODETranslate::EndConvertTimecodeToHNS** entsprechend aufrufen.

Während der Erstellung der Medienquelle erstellt der Quell resolver einen Bytestream für die Datei, aus der die Medienquelle den ASF-Inhalt liest. Damit die Zeitkonvertierungen erfolgreich sind, muss der der ASF-Datei zugeordnete Bytestream suchfunktionen aufweisen. Andernfalls ruft die Anwendung den \_ MF E \_ BYTESTREAM \_ NOT \_ SEEKABLE-Fehler aus dem **Begin...-Aufruf** ab. Eine weitere Anforderung für Zeitkonvertierungen ist, dass die ASF-Datei, die durch die ASF-Medienquelle dargestellt wird, ÜBER ASF-Indexobjekte verfügen muss. Die Präsentationszeiten und die Zeitcodes werden aus den ASF-Indexobjekten extrahiert, die alle Indizes und die entsprechenden Suchpunkte für die ASF-Datei verwalten. Für die Zeit-zu-Zeit-Codeübersetzung der Präsentation muss die ASF-Datei ein Simple Index-Objekt enthalten. Für die Zeitübersetzung von Code zur Präsentationszeit muss die ASF-Datei über ein Indexobjekt verfügen. Die Konvertierungsvorgänge basieren auf dem zugrunde liegenden *Indexer* (WMContainer-Komponente), um das Indexobjekt zu analysieren und zu lesen, das der ASF-Datei zugeordnet ist. Wenn die Datei kein Indexobjekt enthält, empfängt die Anwendung asynchron den \_ MF E \_ NO \_ INDEX-Fehlercode.

Um die von der Anwendung angeforderte Zeit zu übersetzen, listet die Medienquelle die Datenströme in der Datei auf und sucht den Stream, der das entsprechende ASF-Indexobjekt enthält. Wenn ein solcher Stream gefunden wird, analysiert die Medienquelle die ASF-Pakete des Streams, bis der richtige Zeitcode erreicht ist. Nachdem das richtige Beispiel gefunden wurde, ruft es die entsprechende Präsentationszeit oder den Zeitcode aus dem Beispiel ab und gibt sie an den Aufrufer zurück.

### <a name="script-command-support"></a>Skriptbefehlsunterstützung

Wenn Sie eine ASF-Topologie erstellen, die einen Skriptstream enthält, wird der Topologie ein Skriptstreamknoten hinzugefügt. Dieser Knoten sendet ZUM richtigen Zeitpunkt NODESSamples. Das vom Skriptquellknoten bereitgestellte DANNSAMPLE speichert die Daten in dem DEM Beispiel zugeordneten NODESMediaBuffer. Sie können CopyToBuffer für das Beispiel aufrufen, um einen BUFFERMediaBuffer abzurufen, und dann Lock für den Puffer aufrufen, um die Daten abzurufen. 

Skriptstreamnutzlasten werden als Typzeichenfolge in den Puffer gepackt, gefolgt von NULL, gefolgt von der Befehlszeichenfolge, gefolgt von NULL. Zeichenfolgen sind Unicode im ASF-Format.

Eine Nutzlast könnte beispielsweise wie folgt aussehen (wobei \0 ein NULL-Zeichen angibt):

*URL\0http://contoso.com\0*

*Text\0Dies ist eine Beschriftung\0*



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASF-Komponenten auf Pipelineebene](pipeline-layer-asf-components.md)
</dt> <dt>

[ASF-Unterstützung in Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 

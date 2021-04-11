---
description: In diesem Thema wird beschrieben, wie eine Media Foundation Transformation (MFT) geschrieben wird, die als Proxy für einen Hardware Encoder, Decoder oder einen Port (Digital Signal Processor, DSP) fungiert.
ms.assetid: 9922d403-5d0d-433f-ad9f-c86142ac0f46
title: Hardware-MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac5ce05b4fdad6040b51f66f543c1737fc3918d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214966"
---
# <a name="hardware-mfts"></a>Hardware-MFTs

> [!Note]  
> Dieses Thema gilt für Windows 7 oder höher.

 

In diesem Thema wird beschrieben, wie eine Media Foundation Transformation (MFT) geschrieben wird, die als Proxy für einen Hardware Encoder, Decoder oder einen Port (Digital Signal Processor, DSP) fungiert.

> [!IMPORTANT]
> Wenn ein Hardware Codec den AVStream-Multimedia-Klassen Treiber verwendet, ist kein benutzerdefiniertes MFT erforderlich. Media Foundation stellt zu diesem Zweck einen AVStream-Proxy bereit. Die Informationen in diesem Thema gelten nur für Sonderfälle, in denen der Hardware Codec AVStream nicht verwendet. Weitere Informationen finden Sie [unter Unterstützung für Hardware Codec in AVStream](https://msdn.microsoft.com/library/dd568169.aspx).

 

Dieses Thema enthält folgende Abschnitte:

-   [Introduction (Einführung)](#introduction)
-   [Hardware-MFT-Attribute](#hardware-mft-attributes)
-   [Hardware Hand Shake Sequenz](#hardware-handshake-sequence)
-   [Datenverarbeitung](#data-processing)
-   [Paarweise Decoder/Encoder](#paired-decoderencoder)
-   [Zugehörige Themen](#related-topics)

## <a name="introduction"></a>Einführung

Jeder Hardware-Codec, der nicht auf AVStream basiert, muss eine eigene MFT bereitstellen, die als Proxy für den Treiber fungiert. Ein Hardwarecodec kann mehrere unterschiedliche funktionale Blöcke enthalten:

-   Encoder
-   Decoder
-   Frame Skalierung/Formatkonvertierung

Jede dieser Funktionen sollte von einem separaten MFT verwaltet werden. Eine Hardware-MFT sollte nie als "Transcoder" für mehrere Zwecke fungieren. Fügen Sie Codierungs Funktionen stattdessen in einem MFT-Codierer ein. Wenn die Hardware Frame Skalierung und Formatkonvertierungen bietet, platzieren Sie diese Funktionen in einem separaten Videoprozessor, der in der Kategorie **\_ \_ Video \_ Prozessor Kategorie der MFT-Kategorie** registriert ist. Wenn die Hardware keine Frame Skalierung oder Formatkonvertierung unterstützt, stellt Media Foundation einen Software-Videoprozessor bereit.

Für Hardware-MFTs gelten die folgenden allgemeinen Anforderungen:

-   Hardware-MFTs müssen das neue asynchrone Verarbeitungsmodell verwenden, wie in [asynchroner MFTs](asynchronous-mfts.md)beschrieben.
-   Hardware-MFTs müssen dynamische Formatänderungen unterstützen, wie in [dynamische Formatänderungen](basic-mft-processing-model.md)beschrieben.

## <a name="hardware-mft-attributes"></a>Hardware-MFT-Attribute

Eine Hardware-MFT muss folgende Methoden im Zusammenhang mit Attributen implementieren:

-   [**Imftransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes): gibt einen Attribut Speicher für globale MFT-Attribute zurück.
-   [**IMF Transform:: getinputstreamattributs**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes): gibt einen Attribut Speicher für einen Eingabestream zurück.
-   [**IMF Transform:: getoutputstreamattributs**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes): gibt einen Attribut Speicher für einen Ausgabestream zurück.

Wenn der MFT erstmalig erstellt wird, muss er die folgenden Attribute für seinen eigenen globalen Attribut Speicher festlegen (d. h. den von [**GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)zurückgegebenen Attribut Speicher):



| Attribut                                                                                    | BESCHREIBUNG                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MF- \_ Transformation \_ Async](mf-transform-async.md)                                               | Muss auf " **true**" festgelegt werden. Gibt an, dass die MFT asynchrone Verarbeitung ausführt.                                                                                                      |
| [MFT-Aufzählungs \_ \_ Hardware-URL- \_ \_ Attribut](mft-enum-hardware-url-attribute.md)                   | Enthält den symbolischen Link für das Hardware Gerät.<br/> Das topologielader verwendet dieses Attribut, um zu testen, ob ein MFT ein Hardware Gerät darstellt.<br/> |
| [**MFT- \_ Unterstützung für \_ dynamisches \_ Format \_ ändern**](mft-support-dynamic-format-change-attribute.md) | Muss auf " **true**" festgelegt werden. Gibt an, dass der MFT dynamische Formatänderungen unterstützt.                                                                                                       |



 

## <a name="hardware-handshake-sequence"></a>Hardware Hand Shake Sequenz

Wenn zwei MFTs dasselbe physische Gerät darstellen, können Sie Daten innerhalb der Hardware austauschen – beispielsweise über einen Hardwarebus. Es ist nicht erforderlich, die Daten in den Systemspeicher und dann zurück auf das Gerät zu kopieren.

In der folgenden Abbildung stellen die MFTs mit der Bezeichnung "A" und "B" funktionale Blöcke innerhalb derselben Hardware dar. Beispielsweise kann in einem Transcodierungs Szenario "a" einen Hardware Decoder und "B" einen Hardware Encoder darstellen. Der Datenfluss zwischen "A" und "B" erfolgt innerhalb der Hardware. Die MFT-Bezeichnung "C" ist eine Software-MFT. Der Datenfluss von "B" zu "C" verwendet den System Arbeitsspeicher.

![Diagramm, das Felder mit der Bezeichnung a bis c und einen Hardwarecodec anzeigt: a zeigt auf b und den Codec, der Codec zeigt auf b und b auf c](images/proxy-mft.png)

Zum Herstellen einer Hardware Verbindung müssen die beiden Hardware-MFTs einen privaten Kommunikationskanal verwenden. Diese Verbindung wird während der Format Aushandlung hergestellt, bevor die Medientypen festgelegt werden, und vor dem ersten Aufrufen von [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput). Der Verbindungsprozess funktioniert wie folgt:

1.  Das topologielader überprüft beide MFTs auf das vorhanden sein des [MFT \_ Enum- \_ Hardware-URL- \_ \_ Attribut](mft-enum-hardware-url-attribute.md) Attributs. Beachten Sie, dass der Wert dieses Attributs nicht untersucht wird.
2.  Wenn das [MFT- \_ Enum- \_ Hardware-URL- \_ \_ Attribut](mft-enum-hardware-url-attribute.md) in beiden MFTs vorhanden ist, führt das topologielader Folgendes aus:
    1.  Das topologielader ruft [**imftransform:: getoutputstreamattributs**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) für den upstreammft (A) auf. Diese Methode gibt einen [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Zeiger zurück. Lassen Sie diesen Zeiger als " *pupstream*" bezeichnen.
    2.  Das topologielader ruft [**imftransform:: getinputstreamattributs für die downstreammft**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) (B) auf. Dieser Befehl gibt auch einen [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Zeiger zurück. Lassen Sie diesen Zeiger als " *pdownstream*" bezeichnet.
    3.  Das topologielader legt das Attribut Attribut des [verbundenen MFT- \_ \_ Streams \_](mft-connected-stream-attribute.md) auf *pdownstream* fest, indem [**imfattributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)aufgerufen wird. Der Wert des-Attributs ist der *pupstream* -Zeiger.
    4.  Der topologielader legt die mit dem [ \_ HW- \_ \_ \_ streamattribut verbundene MFT](mft-connected-to-hw-stream.md) für *pdownstream* und *pupstream* auf **true** fest.
3.  An diesem Punkt hat das downstreammft einen Zeiger auf den Attribut Speicher der Upstream-MFT, wie in der folgenden Abbildung dargestellt.

    ![Diagramm mit jedem MFTs, der auf seinen Stream zeigt, jeder Stream, der auf seinen Speicher zeigt, und der Eingabe Speicher mit einer gestrichelten Linie in den Ausgabe Speicher](images/proxy-mft2.png)

    > [!Note]  
    > Aus Gründen der Übersichtlichkeit zeigt dieses Diagramm die Datenströme und die Attribut Speicher als unterschiedliche Objekte an, dies ist für die Implementierung jedoch nicht erforderlich.

     

4.  Der Downstream-MFT verwendet den [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Zeiger, um einen privaten Kommunikationskanal mit der upstreammft einzurichten. Da der Kanal privat ist, wird der genaue Mechanismus durch die-Implementierung definiert. Beispielsweise könnte die MFT eine private com-Schnittstelle Abfragen.

In Schritt 4 muss das downstreammft überprüfen, ob die beiden MFTs dasselbe physische Gerät gemeinsam verwenden. Wenn dies nicht der Fall ist, müssen Sie auf den System Arbeitsspeicher für den Datentransport zurückgreifen. Dies ermöglicht die korrekte Funktionsweise des MFT mit Software-MFTs und anderen Hardware Geräten.

Wenn der Handshake erfolgreich ist und die beiden MFTs einen privaten Datenkanal gemeinsam verwenden, verwenden Sie nicht das standardmäßige Datenverarbeitungs Modell (im nächsten Abschnitt beschrieben) am Verbindungspunkt. Insbesondere das downstreammft sendet keine [metransformneedinput](metransformneedinput.md) -Ereignisse. Weitere Informationen finden Sie im nächsten Abschnitt in diesem Thema.

## <a name="data-processing"></a>Datenverarbeitung

Wenn eine Hardware-MFT den Systemspeicher für den Datentransport verwendet, funktioniert der Prozess wie folgt:

1.  Um weitere Eingaben anzufordern, sendet der MFT ein [metransformneedinput](metransformneedinput.md) -Ereignis.
2.  Das [metransformneedinput](metransformneedinput.md) -Ereignis bewirkt, dass die Pipeline [**imftransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)aufruft.
3.  Wenn der MFT Ausgabedaten enthält, sendet der MFT ein [metransformhaveoutput](metransformhaveoutput.md) -Ereignis.
4.  Das [metransformhaveoutput](metransformhaveoutput.md) -Ereignis bewirkt, dass die Pipeline [**imftransform::P rocess Output**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)aufruft.

Weitere Informationen finden Sie unter [asynchrone MFTs](asynchronous-mfts.md).

Wenn die MFT jedoch einen Hardware Kanal verwendet, sendet Sie diese Ereignisse nicht an den Hardware Verbindungspunkt, da die gesamte Datenübertragung intern innerhalb der Hardware erfolgt. Daher ruft die Pipeline nicht [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) oder [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) am Verbindungspunkt auf.

Sehen Sie sich beispielsweise das erste Diagramm in diesem Thema an. Bei dieser Konfiguration erfolgt die Datenverarbeitung wie folgt:

1.  "A" sendet [metransformneedinput](metransformneedinput.md) , um Daten anzufordern.
2.  Die Pipeline ruft [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) für "A" auf.
3.  "A" und "B" verarbeiten die Daten in der Hardware.
4.  Wenn die Verarbeitung fertig ist, sendet "B" ein [metransformhaveoutput](metransformhaveoutput.md) -Ereignis.
5.  Die Pipeline ruft [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) für "B" auf.

## <a name="paired-decoderencoder"></a>Paarweise Decoder/Encoder

Wenn sich ein Decoder und ein Encoder auf demselben Hardware Chip befinden, ist es möglicherweise besser, Sie bei der Transcodierung zusammen zu verwenden. Das heißt, wenn Sie eine auswählen, sollte die andere in der Transcodierung-Pipeline ausgewählt werden. Um sicherzustellen, dass übereinstimmende Hardware Codecs ausgewählt werden, sollten beide Codec-MFTs einen benutzerdefinierten Medientyp anbieten. So erstellen Sie einen benutzerdefinierten Medientyp:

-   Legen Sie ggf. das Attribut " [**MF- \_ \_ Haupt \_**](mf-mt-major-type-attribute.md) Attribut" auf **mfmediatype \_ -Audiodatei** oder **mfmediatype- \_ Video** fest.
-   Legen Sie das Attribut " [**MF \_ MT \_ SubType**](mf-mt-subtype-attribute.md) " auf einen benutzerdefinierten GUID-Wert fest.

Andere Typattribute sind optional. Der Decoder gibt den benutzerdefinierten Typ aus seinem [**imftransform:: getoutputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype)zurück, und der Encoder gibt den benutzerdefinierten Typ aus der [**imftransform:: getinputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) -Methode zurück. In beiden Fällen muss der benutzerdefinierte Typ der erste Eintrag in der Liste (*dwtypeindex* = 0) sein.

Zum Arbeiten mit Software Codecs sollte der Codec auch mindestens ein Standardformat (z. b. NV12 for Video) zurückgeben. Standard Formate sollten nach dem benutzerdefinierten Typ (*dwtypeindex* > 0) angezeigt werden. Wenn die beiden Codecs immer paarweise gekoppelt werden müssen und nicht mit Software Codecs interagieren können, sollten die MFTs nur das benutzerdefinierte Format zurückgeben und keine Standardformate zurückgeben.

> [!Note]  
> Wenn ein Decoder keine Standardformate zurückgibt, kann er nicht für die Wiedergabe mit dem [erweiterten Videorenderer](enhanced-video-renderer.md)verwendet werden. In diesem Fall sollte Sie als ein nur-transcode-Decoder registriert werden. Siehe [nur-transcode-Decoders](implementing-a-codec-mft.md).

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schreiben eines benutzerdefinierten MFT](writing-a-custom-mft.md)
</dt> <dt>

[Implementieren eines Codec-MFT](implementing-a-codec-mft.md)
</dt> <dt>

[Media Foundation Transformationen](media-foundation-transforms.md)
</dt> </dl>

 

 





---
description: In diesem Thema wird beschrieben, wie Sie eine Media Foundation Transform (MFT) schreiben, die als Proxy für einen Hardwareencoder, Decoder oder digital signal processor (DSP) fungiert.
ms.assetid: 9922d403-5d0d-433f-ad9f-c86142ac0f46
title: Hardware-MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 532fef959e2c2b5946d5a27ad98106a2e25cc77f8426c0a871e821c7298a69f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119724932"
---
# <a name="hardware-mfts"></a>Hardware-MFTs

> [!Note]  
> Dieses Thema gilt für Windows 7 oder höher.

 

In diesem Thema wird beschrieben, wie Sie eine Media Foundation Transform (MFT) schreiben, die als Proxy für einen Hardwareencoder, Decoder oder digital signal processor (DSP) fungiert.

> [!IMPORTANT]
> Wenn ein Hardwarecodec den AVStream-Multimediaklassentreiber verwendet, ist kein benutzerdefinierter MFT erforderlich. Media Foundation stellt zu diesem Zweck einen AVStream-Proxy zur Verfügung. Die Informationen in diesem Thema gelten nur für den Sonderfall, in dem der Hardwarecodec AVStream nicht verwendet. Weitere Informationen finden Sie unter [HardwareCodec-Unterstützung in AVStream.](https://msdn.microsoft.com/library/dd568169.aspx)

 

Dieses Thema enthält folgende Abschnitte:

-   [Introduction (Einführung)](#introduction)
-   [Hardware-MFT-Attribute](#hardware-mft-attributes)
-   [Hardwarehandshakesequenz](#hardware-handshake-sequence)
-   [Datenverarbeitung](#data-processing)
-   [Gekoppelter Decoder/Encoder](#paired-decoderencoder)
-   [Zugehörige Themen](#related-topics)

## <a name="introduction"></a>Einführung

Jeder Hardwarecodec, der nicht auf AVStream basiert, muss einen eigenen MFT bereitstellen, um als Proxy für den Treiber zu fungieren. Ein Hardwarecodec kann mehrere verschiedene Funktionsblöcke enthalten:

-   Encoder
-   Decoder
-   Frameskalierung/Formatkonvertierung

Jede dieser Funktionen sollte von einem separaten MFT verwaltet werden. Ein Hardware-MFT sollte nie als mehrzweckigen "Transcoder" fungieren. Legen Sie stattdessen Codierungsfunktionen in einen Encoder MFT und Decodierungsfunktionen in einen Decoder-MFT ab. Wenn die Hardware Frameskalierung und Formatkonvertierungen bietet, platzieren Sie diese Funktionen in einem separaten Videoprozessor, der in der **Kategorie MFT \_ CATEGORY VIDEO \_ PROCESSOR \_ registriert** ist. Wenn die Hardware keine Frameskalierung oder Formatkonvertierung unterstützt, stellt Media Foundation einen Softwarevideoprozessor zur Verfügung.

Hardware-MFTs haben die folgenden allgemeinen Anforderungen:

-   Hardware-MFTs müssen das neue asynchrone Verarbeitungsmodell verwenden, wie unter [Asynchrone MFTs beschrieben.](asynchronous-mfts.md)
-   Hardware-MFTs müssen dynamische Formatänderungen unterstützen, wie unter [Dynamische Formatänderungen beschrieben.](basic-mft-processing-model.md)

## <a name="hardware-mft-attributes"></a>Hardware-MFT-Attribute

Ein Hardware-MFT muss die folgenden Methoden im Zusammenhang mit Attributen implementieren:

-   [**FALSETransform::GetAttributes:**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)Gibt einen Attributspeicher für globale MFT-Attribute zurück.
-   [**FALSETransform::GetInputStreamAttributes:**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes)Gibt einen Attributspeicher für einen Eingabestream zurück.
-   [**FALSETransform::GetOutputStreamAttributes:**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes)Gibt einen Attributspeicher für einen Ausgabestream zurück.

Wenn der MFT zum ersten Mal erstellt wird, muss er die folgenden Attribute für seinen eigenen globalen Attributspeicher (d. h. den von GetAttributes zurückgegebenen [**Attributspeicher) festlegen:**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)



| attribute                                                                                    | Beschreibung                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MF \_ TRANSFORM \_ ASYNC](mf-transform-async.md)                                               | Muss auf TRUE festgelegt **werden.** Gibt an, dass MFT eine asynchrone Verarbeitung ausführt.                                                                                                      |
| [\_ \_ \_ MFT-ENUM-HARDWARE-URL-Attribut \_](mft-enum-hardware-url-attribute.md)                   | Enthält die symbolische Verknüpfung für das Hardwaregerät.<br/> Das Topologielader verwendet das Vorhandensein dieses Attributs, um zu testen, ob ein MFT ein Hardwaregerät darstellt.<br/> |
| [**MFT-UNTERSTÜTZUNG \_ \_ FÜR DYNAMISCHE \_ \_ FORMATÄNDERUNG**](mft-support-dynamic-format-change-attribute.md) | Muss auf TRUE festgelegt **werden.** Gibt an, dass MFT dynamische Formatänderungen unterstützt.                                                                                                       |



 

## <a name="hardware-handshake-sequence"></a>Hardwarehandshakesequenz

Wenn zwei MFTs dasselbe physische Gerät darstellen, können sie Daten innerhalb der Hardware austauschen, z. B. über einen Hardwarebus. Es ist nicht notwendig, die Daten in den Systemspeicher und dann zurück auf das Gerät zu kopieren.

Im folgenden Diagramm stellen die MFTs mit den Bezeichnungen "A" und "B" Funktionsblöcke innerhalb derselben Hardware dar. In einem Transcodierungsszenario kann "A" beispielsweise einen Hardwaredecoder und "B" einen Hardwareencoder darstellen. Der Datenfluss zwischen "A" und "B" erfolgt innerhalb der Hardware. MFT mit der Bezeichnung "C" ist eine Software-MFT. Der Datenfluss von "B" zu "C" verwendet Systemspeicher.

![Diagramm mit Feldern mit der Bezeichnung "a" bis "c" und einem Hardwarecodec: ein Punkt auf b und der Codec, der Codec zeigt auf b und b auf c.](images/proxy-mft.png)

Um eine Hardwareverbindung herzustellen, müssen die beiden Hardware-MFTs einen privaten Kommunikationskanal verwenden. Diese Verbindung wird während der Formataushandlung vor dem Festlegen der Medientypen und vor dem ersten Aufruf von [**ProcessInput hergestellt.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) Der Verbindungsprozess funktioniert wie folgt:

1.  Das Topologielader überprüft beide MFTs auf das Vorhandensein des [Attributs \_ MFT-ENUM-HARDWARE-URL-Attribut. \_ \_ \_ ](mft-enum-hardware-url-attribute.md) Beachten Sie, dass der Wert dieses Attributs nicht untersucht wird.
2.  Wenn [das \_ MFT-ENUM-HARDWARE-URL-Attribut \_ \_ \_ ](mft-enum-hardware-url-attribute.md) auf beiden MFTs vorhanden ist, führt das Topologielader folgende Schritte aus:
    1.  Das Topologielader ruft auf dem Upstream-MFT (A) [**DIE ATTRIBUTETransform::GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) auf. Diese Methode gibt einen [**ATTRIBUTEAttributes-Zeiger**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) zurück. Lassen Sie diesen Zeiger als *pUpstream bezeichnet werden.*
    2.  Das Topologielader ruft AUF dem Downstream-MFT (B) [**DIE ATTRIBUTETransform::GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) auf. Dieser Aufruf gibt auch einen [**ATTRIBUTEAttributes-Zeiger**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) zurück. Lassen Sie diesen Zeiger als *pDownstream bezeichnet werden.*
    3.  Das Topologielader legt das [MFT \_ CONNECTED STREAM \_ \_ ATTRIBUTE-Attribut](mft-connected-stream-attribute.md) auf *pDownstream fest,* indem [**ESATTRIBUTEs::SetUnknown aufruft.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown) Der Wert des Attributs ist der *pUpstream-Zeiger.*
    4.  Das Topologielader legt das [MFT \_ CONNECTED TO \_ \_ HW \_ STREAM-Attribut](mft-connected-to-hw-stream.md) sowohl für *pDownstream* als auch *für pUpstream* auf **TRUE** fest.
3.  An diesem Punkt verfügt der Downstream-MFT über einen Zeiger auf den Attributspeicher des Upstream-MFT, wie im folgenden Diagramm dargestellt.

    ![Diagramm mit jedem Mfts,der auf seinen Stream zeigt, jeder Stream zeigt auf seinen Speicher und der Eingabespeicher mit einer gestrichelten Linie zum Ausgabespeicher](images/proxy-mft2.png)

    > [!Note]  
    > Aus Gründen der Übersichtlichkeit zeigt dieses Diagramm die Datenströme und die Attributspeicher als unterschiedliche Objekte an, dies ist jedoch für die Implementierung nicht erforderlich.

     

4.  Der Downstream-MFT verwendet den [**ZEIGER AUF ATTRIBUTEattribute,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) um einen privaten Kommunikationskanal mit dem Upstream-MFT zu erstellen. Da der Kanal privat ist, wird der genaue Mechanismus von der Implementierung definiert. Beispielsweise kann MFT eine private COM-Schnittstelle abfragen.

In Schritt 4 muss der nachgeschaltete MFT überprüfen, ob sich die beiden MFTs dasselbe physische Gerät teilen. Wenn dies nicht der Fall ist, müssen sie auf die Verwendung des Systemspeichers für den Datentransport zurückfallen. Dadurch kann MFT ordnungsgemäß mit Software-MFTs und anderen Hardwaregeräten arbeiten.

Wenn der Handshake erfolgreich ist und die beiden MFTs einen privaten Datenkanal gemeinsam nutzen, verwenden sie nicht das Standarddatenverarbeitungsmodell (im nächsten Abschnitt beschrieben) am Verbindungspunkt. Insbesondere sendet der Downstream-MFT keine [METransformNeedInput-Ereignisse.](metransformneedinput.md) Weitere Informationen finden Sie im nächsten Abschnitt dieses Themas.

## <a name="data-processing"></a>Datenverarbeitung

Wenn ein Hardware-MFT Systemspeicher für den Datentransport verwendet, funktioniert der Prozess wie folgt:

1.  Um weitere Eingaben an fordern zu können, sendet MFT ein [METransformNeedInput-Ereignis.](metransformneedinput.md)
2.  Das [METransformNeedInput-Ereignis](metransformneedinput.md) bewirkt, dass die Pipeline [**DENKtransform::P rocessInput aufruft.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)
3.  Wenn MFT Ausgabedaten enthält, sendet MFT ein [METransformHaveOutput-Ereignis.](metransformhaveoutput.md)
4.  Das [METransformHaveOutput-Ereignis](metransformhaveoutput.md) bewirkt, dass die Pipeline [**DENKtransform::P rocessOutput aufruft.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)

Weitere Informationen finden Sie unter [Asynchrone MFTs.](asynchronous-mfts.md)

Wenn der MFT jedoch einen Hardwarekanal verwendet, sendet er diese Ereignisse nicht an den Hardwareverbindungspunkt, da alle Datenübertragungen intern innerhalb der Hardware erfolgt. Daher ruft die Pipeline am Verbindungspunkt [**weder ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) noch [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) auf.

Betrachten Sie beispielsweise das erste Diagramm in diesem Thema. Bei dieser Konfiguration würde die Datenverarbeitung wie folgt erfolgen:

1.  "A" sendet [METransformNeedInput zum](metransformneedinput.md) Anfordern von Daten.
2.  Die Pipeline ruft [**ProcessInput auf**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) "A" auf.
3.  "A" und "B" verarbeiten die Daten auf Hardware.
4.  Wenn die Verarbeitung abgeschlossen ist, sendet "B" ein [METransformHaveOutput-Ereignis.](metransformhaveoutput.md)
5.  Die Pipeline ruft [**ProcessOutput auf**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) "B" auf.

## <a name="paired-decoderencoder"></a>Gekoppelter Decoder/Encoder

Wenn sich ein Decoder und ein Encoder auf demselben Hardwarechip befinden, ist es möglicherweise vorzuziehen, sie bei der Transcodierung zusammen zu verwenden. Das heißt, die Auswahl einer option sollte dazu führen, dass die andere in der Transcodierungspipeline ausgewählt wird. Um sicherzustellen, dass übereinstimmende Hardwarecodecs ausgewählt werden, sollten beide Codec-MFTs einen benutzerdefinierten Medientyp bieten. So erstellen Sie einen benutzerdefinierten Medientyp:

-   Legen Sie das [**MF \_ MT MAJOR \_ \_ TYPE-Attribut**](mf-mt-major-type-attribute.md) je nach Bedarf auf **MFMediaType \_ Audio** oder **MFMediaType \_ Video** fest.
-   Legen Sie das [**MF \_ MT \_ SUBTYPE-Attribut**](mf-mt-subtype-attribute.md) auf einen benutzerdefinierten GUID-Wert fest.

Andere Typattribute sind optional. Der Decoder gibt den benutzerdefinierten Typ aus seinem [**TYPSTRANSFORM::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype)zurück, und der Encoder gibt den benutzerdefinierten Typ aus seiner [**ENTRANSTRANSFORM::GetInputAvailableType-Methode**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) zurück. In beiden Fällen muss der benutzerdefinierte Typ der erste Eintrag in der Liste sein (*dwTypeIndex* = 0).

Für die Arbeit mit Softwarecodecs sollte der Codec auch mindestens ein Standardformat zurückgeben, z. B. NV12 für Videos. Standardformate sollten nach dem benutzerdefinierten Typ *(dwTypeIndex* > 0) angezeigt werden. Wenn die beiden Codecs immer gekoppelt sein müssen und nicht mit Softwarecodecs zusammenarbeiten können, sollten die MFTs nur das benutzerdefinierte Format und keine Standardformate zurückgeben.

> [!Note]  
> Wenn ein Decoder keine Standardformate zurückgibt, kann er nicht für die Wiedergabe mit dem [Erweiterten Videorenderer](enhanced-video-renderer.md)verwendet werden. In diesem Fall sollte es als nur transcodierten Decoder registriert werden. Weitere Informationen finden Sie unter [Nur-Transcode-Decoder.](implementing-a-codec-mft.md)

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schreiben eines benutzerdefinierten MFT](writing-a-custom-mft.md)
</dt> <dt>

[Implementieren eines Codec-MFT](implementing-a-codec-mft.md)
</dt> <dt>

[Media Foundation Transformationen](media-foundation-transforms.md)
</dt> </dl>

 

 





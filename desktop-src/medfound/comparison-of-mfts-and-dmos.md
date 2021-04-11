---
description: Media Foundation Transformationen (MFTs) sind eine Weiterentwicklung des Transformations Modells, das zuerst mit DirectX Media Objects (DMOs) eingeführt wurde.
ms.assetid: 4e8c3ec9-6ffa-4858-a4ea-8ef8ccaf9253
title: Vergleich von MFTs und DMOs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e76e128ece1609f25e053486dbb6bcf4578161c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041561"
---
# <a name="comparison-of-mfts-and-dmos"></a>Vergleich von MFTs und DMOs

Media Foundation Transformationen (MFTs) sind eine Weiterentwicklung des Transformations Modells, das zuerst mit DirectX Media Objects (DMOs) eingeführt wurde. In diesem Thema werden die Hauptmethoden zusammengefasst, mit denen sich MFTs von dmos unterscheiden. Lesen Sie dieses Thema, wenn Sie bereits mit den DMO-Schnittstellen vertraut sind oder wenn Sie ein vorhandenes DMO in eine MFT konvertieren möchten.

Dieses Thema enthält folgende Abschnitte:

-   [Anzahl der Streams](#number-of-streams)
-   [Aushandlung formatieren](#format-negotiation)
-   [Streaming](#streaming)
    -   [Zuweisen von Ressourcen](#allocating-resources)
    -   [Verarbeiten von Daten](#processing-data)
    -   [Lak](#flushing)
    -   [Datenstrom Diskontinuitäten](#stream-discontinuities)
-   [Verschiedene Unterschiede](#miscellaneous-differences)
-   [Flags](#flags)
    -   [ProcessInput-Flags](#processinput-flags)
    -   [ProcessOutput-Flags](#processoutput-flags)
    -   [Getinputstatus-Flags](#getinputstatus-flags)
    -   [Getoutputstatus-Flags](#getoutputstatus-flags)
    -   [Getinputstreaminfo-Flags](#getinputstreaminfo-flags)
    -   [Getoutputstreaminfo-Flags](#getoutputstreaminfo-flags)
    -   [Setinputtype/setoutputtype-Flags](#setinputtypesetoutputtype-flags)
-   [Fehlercodes](#error-codes)
-   [Erstellen von Hybriden DMO-/MFT-Objekten](#creating-hybrid-dmomft-objects)
-   [Zugehörige Themen](#related-topics)

## <a name="number-of-streams"></a>Anzahl der Streams

Ein DMO verfügt über eine festgelegte Anzahl von Streams, während eine MFT eine dynamische Anzahl von Streams unterstützen kann. Der Client kann Eingabedaten Ströme hinzufügen, und der MFT kann während der Verarbeitung neue Ausgabedaten Ströme hinzufügen. MFTs sind jedoch nicht erforderlich, um dynamische Streams zu unterstützen. Eine MFT kann eine festgelegte Anzahl von Datenströmen aufweisen, genau wie ein DMO.

Die folgenden Methoden werden verwendet, um dynamische Streams auf einem MFT zu unterstützen:

-   [**IMF Transform:: addinputstreams**](/windows/win32/api/mftransform/nf-mftransform-imftransform-addinputstreams)
-   [**IMF Transform::D eleteinputstream**](/windows/win32/api/mftransform/nf-mftransform-imftransform-deleteinputstream)
-   [**IMF Transform:: getstreamids**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getstreamids)
-   [**IMF Transform:: getstreamlimits**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getstreamlimits)

Außerdem definiert die [**IMF Transform::P rocessoutput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processoutput) -Methode das Verhalten zum Hinzufügen oder Entfernen von Ausgabestreams.

Da DMOS über fixierte Streams verfügen, werden die Datenströme in einem DMO mithilfe NULL basierter Indexwerte identifiziert. MFTs hingegen verwenden Datenstrom Bezeichner, die nicht notwendigerweise den Indexwerten entsprechen. Dies liegt daran, dass sich die Anzahl der Streams in einer MFT möglicherweise ändert. Beispielsweise könnte Stream 0 entfernt werden, sodass Stream 1 als erster Stream belassen wird. Ein MFT mit einer festgelegten Anzahl von Streams sollte jedoch dieselbe Konvention wie DMOS beobachten und Indexwerte für Datenstrom Bezeichner verwenden.

## <a name="format-negotiation"></a>Aushandlung formatieren

Bei MFTs wird die [**imfmediatype**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediatype) -Schnittstelle verwendet, um Medientypen zu beschreiben. Andernfalls funktioniert die Format Aushandlung mit MFTs mit denselben Grundprinzipien wie bei DMOS. In der folgenden Tabelle sind die formataushandlungs Methoden für DMOS und die entsprechenden Methoden für MFTs aufgeführt.



| DMO-Methode                                                                        | MFT-Methode                                                                          |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**Imediaobject:: getinputcurrenttype**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputcurrenttype)   | [**IMF Transform:: getinputcurrenttype**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputcurrenttype)       |
| [**Imediaobject:: getinputmaxlatency**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputmaxlatency)     | [**IMF Transform:: getinputstreaminfo**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo)         |
| [**Imediaobject:: getinputsizeinfo**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputsizeinfo)         | [**IMF Transform:: getinputstreaminfo**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo)         |
| [**Imediaobject:: getinputtype**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype)                 | [**Imftransform:: getinputavailabletype**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputavailabletype)   |
| [**Imediaobject:: getoutputcurrenttype**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputcurrenttype) | [**IMF Transform:: getoutputcurrenttype**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getoutputcurrenttype)     |
| [**Imediaobject:: getoutputsizeinfo**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputsizeinfo)       | [**IMF Transform:: getoutputstreaminfo**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo)       |
| [**Imediaobject:: getoutputtype**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype)               | [**Imftransform:: getoutputavailabletype**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) |



 

## <a name="streaming"></a>Streaming

Wie bei DMOS verarbeiten die MFTs Daten durch Aufrufe von [**ProcessInput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processinput) -und [**ProcessOutput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processoutput) -Methoden. Im folgenden finden Sie die wichtigsten Unterschiede zwischen DMO-und MFT-Prozessen beim Streamen von Daten.

### <a name="allocating-resources"></a>Zuweisen von Ressourcen

MFTs verfügen nicht über die Methoden [**imediaobject:: depingestreamingresources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources) und [**imediaobject:: freestreamingresources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-freestreamingresources) , die mit DMOS verwendet werden. Um die Zuordnung und Freigabe von Ressourcen effizient zu verarbeiten, kann eine MFT auf die folgenden Meldungen in der [**imftransform::P rocess Message**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) -Methode Antworten:

-   [**MFT- \_ Nachrichten \_ Benachrichtigung zum Starten des \_ \_ Streamings**](mft-message-notify-begin-streaming.md)
-   [**\_Nachrichten \_ \_ Anfang \_ für \_ MFT-Nachricht Benachrichtigen**](mft-message-notify-start-of-stream.md)

Außerdem kann der Client den Anfang und das Ende eines Streams durch Aufrufen von [**ProcessMessage**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) mit den folgenden Meldungen signalisieren:

-   [**\_ \_ \_ Ende \_ des Daten \_ Stroms für MFT-Nachricht Benachrichtigen**](mft-message-notify-end-of-stream.md)
-   [**MFT- \_ Nachrichten Nachrichten \_ Ende- \_ \_ Streaming**](mft-message-notify-end-streaming.md)

Diese beiden Nachrichten haben keine genaue DMO-Entsprechung.

### <a name="processing-data"></a>Verarbeiten von Daten

MFTs verwenden Medien Beispiele zum Speichern von Eingabe-und Ausgabedaten. Medien Beispiele machen die [**IMF Sample**](/windows/win32/api/mfobjects/nn-mfobjects-imfsample) -Schnittstelle verfügbar und enthalten die folgenden Daten:

-   Zeitstempel und Dauer.
-   Attribute, die pro Stichproben Informationen enthalten. Eine Liste der Attribute finden Sie unter [Sample Attribute](sample-attributes.md).
-   NULL oder mehr Medien Puffer. Jeder Medien Puffer macht die [**imfmediabuffer**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediabuffer) -Schnittstelle verfügbar.

Die [**imfmediabuffer**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediabuffer) -Schnittstelle ähnelt der DMO **imediabuffer** -Schnittstelle. Um auf den zugrunde liegenden Speicherpuffer zuzugreifen, nennen Sie [**imfmediabuffer:: Lock**](/windows/win32/api/mfobjects/nf-mfobjects-imfmediabuffer-lock). Diese Methode entspricht in etwa [**imediabuffer:: getbufferandlength**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediabuffer-getbufferandlength) für DMOS.

Für nicht komprimierte Videodaten unterstützt ein Medien Puffer möglicherweise auch die [**IMF2DBuffer**](/windows/win32/api/mfobjects/nn-mfobjects-imf2dbuffer) -Schnittstelle. Ein MFT, das unkomprimierte Videos verarbeitet (entweder als Eingabe oder Ausgabe), sollte darauf vorbereitet sein, die **IMF2DBuffer** -Schnittstelle zu verwenden, wenn der Puffer Sie verfügbar macht. Weitere Informationen finden Sie unter [nicht komprimierte Video Puffer](uncompressed-video-buffers.md).

Media Foundation stellt einige Standard Implementierungen von [**imfmediabuffer**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediabuffer)bereit, sodass es im Allgemeinen nicht erforderlich ist, eine eigene Implementierung zu schreiben. Um einen DMO-Puffer aus einem Media Foundation Puffer zu erstellen, rufen Sie [**mfkreatelegacymediabufferonmfmediabuffer**](/windows/win32/api/mfapi/nf-mfapi-mfcreatelegacymediabufferonmfmediabuffer)auf.

### <a name="flushing"></a>Lak

MFTs verfügen über keine [**Flush**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-flush) -Methode. Um einen MFT zu leeren, wenden Sie [**imftransform::P rocess Message**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) mit der [**MFT- \_ Nachrichten \_ Befehls \_**](mft-message-command-flush.md) Leerungs Meldung an.

### <a name="stream-discontinuities"></a>Datenstrom Diskontinuitäten

MFTs haben keine [**discontinuity**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-discontinuity) -Methode. Um eine Diskontinuität in einem Stream zu signalisieren, legen Sie das Attribut [**\_ Diskontinuität von mfsampleextension**](mfsampleextension-discontinuity-attribute.md) für das Eingabe Beispiel fest.

## <a name="miscellaneous-differences"></a>Verschiedene Unterschiede

Im folgenden finden Sie einige zusätzliche geringfügige Unterschiede zwischen MFTs und DMOS.

-   Es gibt keine MFT-Entsprechungen für die folgenden DMO-Methoden:
    -   [**Imediaobject:: Lock**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-lock)
    -   [**Imediaobject:: setinputmaxlatency**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputmaxlatency)
-   MFTs sind nicht erforderlich, um Aggregationen zu unterstützen.
-   MFTs unterstützen einen Vorgang mit *dem Namen "*". Der Zweck der Ableitung besteht darin, alle Daten zu verarbeiten, die im MF verbleiben, ohne weitere Eingabedaten für die MFT (z. b. am Ende des Streams) bereitzustellen. Um einen MFT zu entleeren, wenden Sie [**imftransform::P rocess Message**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) mit der [**MFT- \_ Nachrichten \_ Befehls \_**](mft-message-command-drain.md) Ausgleichs Meldung an. Weitere Informationen finden Sie unter [Grundlegendes MFT-Verarbeitungsmodell](basic-mft-processing-model.md).
-   MFTs können über Attribute verfügen, einschließlich pro-Stream-Attribute. Verwenden Sie die folgenden Methoden, um die Attribute von einem MFT zu erhalten:

    -   [**IMF Transform:: GetAttributes**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getattributes)
    -   [**IMF Transform:: getinputstreamattribute**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes)
    -   [**IMF Transform:: getoutputstreamattribute**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes)

-   Mit MFTs können Ereignisse verarbeitet werden. Um ein Ereignis an einen MFT zu senden, wird [**imftransform::P rocesabvent**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processevent)aufgerufen. Ein MFT kann ein Ereignis über die [**ProcessOutput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processoutput) -Methode an den Client senden. Weitere Informationen finden Sie unter [Grundlegendes MFT-Verarbeitungsmodell](basic-mft-processing-model.md).

## <a name="flags"></a>Flags

In den folgenden Tabellen sind die verschiedenen DMO-Flags und Ihre mft-Entsprechungen aufgeführt. Jedes Mal, wenn ein DMO-Flag direkt einem MFT-Flag zugeordnet ist, haben beide Flags denselben numerischen Wert. Einige DMO-Flags haben jedoch keine exakten MFT-Entsprechungen und umgekehrt.

### <a name="processinput-flags"></a>ProcessInput-Flags

DMOS: [**\_ DMO- \_ Eingabe \_ Daten \_ Puffer \_ Flags**](/previous-versions/windows/embedded/aa451599(v=msdn.10)) -Enumeration.

MFTs: keine äquivalente Enumeration.



| DMO-Flag                                  | MFT-Flag                                                                                                                                      |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| **DMO- \_ Eingabe \_ Daten- \_ bufferf- \_ Synchronisierungs Punkt**  | Kein entsprechendes Flag. Legen Sie stattdessen das [**MF SampleExtension \_ -cleanpointattribut**](mfsampleextension-cleanpoint-attribute.md) für das Beispiel fest. |
| **DMO- \_ Eingabe \_ Daten \_ Puffer \_ Zeit**       | Kein entsprechendes Flag. Nennen Sie stattdessen [**imfsample:: setsampletime**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-setsampletime) für das Beispiel.                                  |
| **DMO- \_ Eingabe \_ Daten \_ bufferf \_ timelength** | Kein entsprechendes Flag. Aufrufen Sie stattdessen [**imfsample:: setsampleduration**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-setsampleduration) für das Beispiel.                          |



 

### <a name="processoutput-flags"></a>ProcessOutput-Flags

DMOS: [**\_ DMO \_ - \_ prozessausgabeflags \_**](/previous-versions/windows/desktop/api/Mediaobj/ne-mediaobj-_dmo_process_output_flags) -Enumeration.

MFTs: Enumeration der [**\_ \_ \_ Ausgabe \_ Flags für den MFT-Prozess**](/windows/win32/api/mftransform/ne-mftransform-_mft_process_output_flags) .



| DMO-Flag                                            | MFT-Flag                                            |
|-----------------------------------------------------|-----------------------------------------------------|
| **DMO- \_ Prozess \_ Ausgabe verwerfen, \_ \_ Wenn \_ kein \_ Puffer** | **Ausgabe der MFT- \_ Prozess \_ Ausgabe \_ verwerfen, \_ Wenn \_ kein \_ Puffer** |



 

DMOS: [**\_ DMO- \_ Ausgabe \_ Daten \_ Puffer \_ Flags**](/previous-versions/windows/desktop/api/Mediaobj/ne-mediaobj-_dmo_output_data_buffer_flags) -Enumeration.


MFTs: Enumeration der [**\_ MFT- \_ Ausgabe \_ Daten \_ Puffer \_ Flags**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_data_buffer_flags) .



| DMO-Flag                                   | MFT-Flag                                                                                                                                            |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| **DMO- \_ Ausgabe \_ Daten- \_ bufferf- \_ Synchronisierungs Punkt**  | Kein entsprechendes Flag. Überprüfen Sie stattdessen das [**MF Sample Extension- \_ cleanpointattribut**](mfsampleextension-cleanpoint-attribute.md) für das Beispiel. |
| **DMO- \_ Ausgabe \_ Daten \_ Puffer \_ Zeit**       | Kein entsprechendes Flag. Nennen Sie stattdessen [**imfsample:: getsampletime**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-getsampletime) für das Beispiel.                                        |
| **DMO- \_ Ausgabe \_ Daten \_ bufferf \_ timelength** | Kein entsprechendes Flag. Aufrufen Sie stattdessen [**imfsample:: getsampleduration**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-getsampleduration) für das Beispiel.                                |
| **DMO- \_ Ausgabe \_ Daten- \_ bufferf \_ unvollständig** | **der MFT- \_ Ausgabe \_ Daten \_ Puffer ist \_ unvollständig.**                                                                                                           |
| Kein entsprechendes Flag.                        | **Änderung des MFT- \_ Ausgabe \_ Daten \_ Puffer \_ Formats \_**                                                                                                       |
| Kein entsprechendes Flag.                        | **Datenstrom Ende des MFT- \_ Ausgabe \_ Daten \_ Puffers \_ \_**                                                                                                          |
| Kein entsprechendes Flag.                        | **MFT- \_ Ausgabe \_ Daten \_ Puffer \_ keine \_ Stichprobe**                                                                                                           |



 

### <a name="getinputstatus-flags"></a>Getinputstatus-Flags

DMOS: **\_ DMO \_ - \_ eingabestatusflags \_** -Enumeration.

MFTs: [**\_ MFT \_ - \_ eingabestatusflags \_**](/windows/win32/api/mftransform/ne-mftransform-_mft_input_status_flags) -Enumeration.



| DMO-Flag                              | MFT-Flag                             |
|---------------------------------------|--------------------------------------|
| **DMO- \_ Eingabe \_ Status " \_ \_ Daten akzeptieren"** | **MFT \_ - \_ Eingabe \_ Status \_ Daten akzeptieren** |



 

### <a name="getoutputstatus-flags"></a>Getoutputstatus-Flags

DMOS: keine äquivalente Enumeration.

MFTs: Enumeration der [**\_ \_ \_ \_ Statusflags für die MFT-Ausgabe**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_status_flags) .



| DMO-Flag            | MFT-Flag                               |
|---------------------|----------------------------------------|
| Kein entsprechendes Flag. | **Beispiel für den MFT- \_ Ausgabe \_ Status ist \_ \_ bereit** |



 

### <a name="getinputstreaminfo-flags"></a>Getinputstreaminfo-Flags

DMOS: [**\_ DMO \_ - \_ Eingabestream- \_ \_ infoFlags**](/previous-versions/windows/embedded/aa451600(v=msdn.10)) -Enumeration.

MFTs: [**\_ MFT \_ - \_ Eingabestream- \_ \_ infoFlags**](/windows/win32/api/mftransform/ne-mftransform-_mft_input_stream_info_flags) -Enumeration.



| DMO-Flag                                             | MFT-Flag                                            |
|------------------------------------------------------|-----------------------------------------------------|
| **DMO- \_ Eingabe streamf-vollständige \_ \_ \_ Beispiele**              | **vollständige Beispiele für MFT- \_ Eingabedaten \_ Strom \_ \_**              |
| **DMO \_ input \_ streamf \_ Single \_ Sample \_ per \_ buffer** | **Beispiel für MFT- \_ Eingabedaten \_ Strom \_ \_ \_ pro \_ Puffer** |
| **DMO- \_ Eingabe, \_ festes streamf- \_ \_ Stichproben \_ Größe**         | **\_ \_ \_ fixierte \_ Stichproben \_ Größe des MFT-Eingabedaten Stroms**         |
| **DMO- \_ Eingabe- \_ streamf \_ enthält \_ Puffer**              | **MFT \_ - \_ Eingabestream \_ enthält \_ Puffer**              |
| Kein entsprechendes Flag.                                  | **der MFT- \_ Eingabedaten \_ Strom \_ ist \_ nicht \_ adressieren.**           |
| Kein entsprechendes Flag.                                  | **Wechsel zum MFT- \_ Eingabedaten \_ Strom \_**                   |
| Kein entsprechendes Flag.                                  | **MFT- \_ Eingabedaten \_ Strom \_ optional**                    |



 

### <a name="getoutputstreaminfo-flags"></a>Getoutputstreaminfo-Flags

DMOS: [**\_ DMO \_ - \_ Ausgabestream- \_ \_ infoFlags**](/previous-versions/ms806053(v=msdn.10)) -Enumeration.

MFTs: [**\_ MFT \_ - \_ Ausgabestream- \_ \_ infoFlags**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_stream_info_flags) -Enumeration.



| DMO-Flag                                              | MFT-Flag                                             |
|-------------------------------------------------------|------------------------------------------------------|
| **DMO- \_ Ausgabe \_ streamf \_ ganze \_ Beispiele**              | **\_ \_ \_ ganze \_ Beispiele für den MFT-Ausgabedatenstrom**              |
| **DMO- \_ Ausgabe \_ streamf \_ Single \_ Sample \_ per \_ buffer** | **Beispiel für den MFT- \_ Ausgabedaten \_ Strom \_ \_ \_ pro \_ Puffer** |
| **DMO- \_ Ausgabe, \_ Fixed- \_ \_ Stichproben \_ Größe**         | **Fixed- \_ \_ \_ \_ Stichproben \_ Größe des MFT-Ausgabedaten Stroms**         |
| **DMO- \_ Ausgabe \_ streamf \_ verwerfen**                 | **Verwerfen des MFT- \_ Ausgabestreams \_ \_**                 |
| **DMO- \_ Ausgabe- \_ streamf \_ optional**                    | **MFT \_ - \_ Ausgabestream \_ optional**                    |
| Kein entsprechendes Flag.                                   | **MFT \_ - \_ Ausgabestream \_ enthält \_ Beispiele**           |
| Kein entsprechendes Flag.                                   | **der MFT- \_ \_ Ausgabestream \_ kann \_ \_ Beispiele enthalten.**       |
| Kein entsprechendes Flag.                                   | **verzögerter MFT- \_ \_ \_ \_ Ausgabestream**                  |
| Kein entsprechendes Flag.                                   | **Wechsel zum MFT- \_ Ausgabedaten \_ Strom \_**                   |



 

### <a name="setinputtypesetoutputtype-flags"></a>Setinputtype/setoutputtype-Flags

DMOS: [**\_ DMO \_ - \_ Typ \_ Flags**](/previous-versions/windows/desktop/api/Mediaobj/ne-mediaobj-_dmo_set_type_flags) -Enumeration.

MFTs: [**\_ MFT \_ - \_ Typ \_ Flags**](/windows/win32/api/mftransform/ne-mftransform-_mft_set_type_flags) -Enumeration.



| DMO-Flag                        | MFT-Flag                                                                             |
|---------------------------------|--------------------------------------------------------------------------------------|
| **DMO- \_ Satz \_ nur typef- \_ Test \_** | **MFT \_ - \_ Typ \_ nur Test festlegen \_**                                                       |
| **DMO \_ Set \_ typef \_ Clear**      | Kein entsprechendes Flag. Legen Sie stattdessen den Medientyp auf **null** fest, um den Medientyp zu löschen. |



 

## <a name="error-codes"></a>Fehlercodes

In der folgenden Tabelle wird gezeigt, wie Sie MFT-Fehlercodes DMO-Fehlercodes zuordnen. Ein hybrides MFT/DMO-Objekt sollte die DMO-Fehlercodes von [**imediaobject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) -Methoden und die MFT-Fehlercodes von [**imftransform**](/windows/win32/api/mftransform/nn-mftransform-imftransform) -Methoden zurückgeben. Die DMO-Fehlercodes werden in der Header Datei "mediaerr. h" definiert. Die MFT-Fehlercodes werden in der Header Datei "mferror. h" definiert.



| DMO-Fehlercode                  | MFT-Fehlercode                       |
|---------------------------------|--------------------------------------|
| **DMO \_ E \_ invalidtype**         | **MF \_ E \_ invalidtype**               |
| **DMO \_ E \_ invalidstreamindex**  | **MF \_ E \_ invalidstreamnumber**       |
| **DMO \_ E \_ notannahme**        | **MF \_ E \_ notannahme**              |
| **DMO \_ E \_ keine \_ weiteren \_ Elemente**     | **MF \_ E \_ keine \_ weiteren \_ Typen**           |
| **der DMO \_ E- \_ Typ wurde \_ nicht \_ akzeptiert.** | **MF \_ E \_ invalidmediatype**          |
| **DMO \_ E- \_ Typ \_ nicht \_ festgelegt**      | **MF \_ E \_ - \_ Transformationstyp \_ nicht \_ festgelegt** |



 

## <a name="creating-hybrid-dmomft-objects"></a>Erstellen von Hybriden DMO-/MFT-Objekten

Die [**IMF Transform**](/windows/win32/api/mftransform/nn-mftransform-imftransform) -Schnittstelle basiert auf [**imediaobject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject), das die primäre Schnittstelle für DirectX Media Objects (DMOs) ist. Es ist möglich, Objekte zu erstellen, die beide Schnittstellen verfügbar machen. Dies kann jedoch zu Namenskonflikten führen, da die Schnittstellen einige Methoden aufweisen, die denselben Namen aufweisen. Sie können dieses Problem auf zwei Arten beheben:

Lösung 1: Fügen Sie die folgende Zeile am Anfang jeder cpp-Datei ein, die MFT-Funktionen enthält:

``` syntax
#define MFT_UNIQUE_METHOD_NAMES
```

Dadurch wird die Deklaration der [**imftransform**](/windows/win32/api/mftransform/nn-mftransform-imftransform) -Schnittstelle geändert, sodass den meisten Methodennamen "MFT" vorangestellt wird. Folglich wird [**IMF Transform::P rocessinput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processinput) zu **IMF Transform:: mftprocessinput**, während [**imediaobject::P rocessinput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) den ursprünglichen Namen beibehält. Diese Technik ist besonders nützlich, wenn Sie ein vorhandenes DMO in einen Hybriden DMO/MFT-Wert umstellen. Sie können die neuen MFT-Methoden hinzufügen, ohne die DMO-Methoden zu ändern.

Lösung 2: Verwenden Sie die C++-Syntax, um Namen zu unterscheiden, die von mehr als einer Schnittstelle geerbt werden. Deklarieren Sie z. b. die MFT-Version von [**ProcessInput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processinput) wie folgt:

``` syntax
CMyHybridObject::IMFTransform::ProcessInput(...)
```

Deklarieren Sie die DMO-Version von [**ProcessInput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) wie folgt:

``` syntax
CMyHybridObject::IMediaObject::ProcessInput(...)
```

Wenn Sie einen internen Aufrufvorgang für eine Methode innerhalb des Objekts durchführen, können Sie diese Syntax verwenden. Dadurch wird jedoch der virtuelle Status der Methode überschrieben. Eine bessere Möglichkeit, Aufrufe innerhalb des-Objekts durchführen zu können, ist die folgende:

``` syntax
hr = ((IMediaObject*)this)->ProcessInput(...)
```

Wenn Sie auf diese Weise eine andere Klasse von **cmyhybridobject** ableiten und die cmyhybridobject:: imediaobject::P rocessinput-Methode außer Kraft setzen, wird die korrekte virtuelle Methode aufgerufen. Die DMO-Schnittstellen sind in der DirectShow SDK-Dokumentation dokumentiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation Transformationen](media-foundation-transforms.md)
</dt> </dl>

 

 

---
description: Media Foundation Transformationen (MFTs) sind eine Weiterentwicklung des Transformationsmodells, das erstmals mit DirectX Media Objects (DMOs) eingeführt wurde.
ms.assetid: 4e8c3ec9-6ffa-4858-a4ea-8ef8ccaf9253
title: Vergleich von MFTs und DMOs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e145effed095fb22f6bfeb07cbee23ab3d30836a404f36a2bad4b9fbeb1dd81a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958980"
---
# <a name="comparison-of-mfts-and-dmos"></a>Vergleich von MFTs und DMOs

Media Foundation Transformationen (MFTs) sind eine Weiterentwicklung des Transformationsmodells, das erstmals mit DirectX Media Objects (DMOs) eingeführt wurde. In diesem Thema werden die wichtigsten Unterschiede zwischen MFTs und DMOs zusammengefasst. Lesen Sie dieses Thema, wenn Sie bereits mit den DMO-Schnittstellen vertraut sind oder wenn Sie eine vorhandene DMO in einen MFT konvertieren möchten.

Dieses Thema enthält folgende Abschnitte:

-   [Anzahl der Streams](#number-of-streams)
-   [Formataushandlung](#format-negotiation)
-   [Streaming](#streaming)
    -   [Zuordnen von Ressourcen](#allocating-resources)
    -   [Verarbeiten von Daten](#processing-data)
    -   [Spülung](#flushing)
    -   [Stream-Diskontinuitäten](#stream-discontinuities)
-   [Verschiedene Unterschiede](#miscellaneous-differences)
-   [Flags](#flags)
    -   [ProcessInput-Flags](#processinput-flags)
    -   [ProcessOutput-Flags](#processoutput-flags)
    -   [GetInputStatus-Flags](#getinputstatus-flags)
    -   [GetOutputStatus-Flags](#getoutputstatus-flags)
    -   [GetInputStreamInfo-Flags](#getinputstreaminfo-flags)
    -   [GetOutputStreamInfo-Flags](#getoutputstreaminfo-flags)
    -   [SetInputType/SetOutputType-Flags](#setinputtypesetoutputtype-flags)
-   [Fehlercodes](#error-codes)
-   [Erstellen von Hybrid-DMO/MFT-Objekten](#creating-hybrid-dmomft-objects)
-   [Zugehörige Themen](#related-topics)

## <a name="number-of-streams"></a>Anzahl der Streams

Ein DMO verfügt über eine feste Anzahl von Streams, während ein MFT eine dynamische Anzahl von Streams unterstützen kann. Der Client kann Eingabestreams hinzufügen, und der MFT kann während der Verarbeitung neue Ausgabestreams hinzufügen. MFTs sind jedoch nicht erforderlich, um dynamische Streams zu unterstützen. Ein MFT kann eine feste Anzahl von Streams aufweisen, genau wie ein DMO.

Die folgenden Methoden werden verwendet, um dynamische Streams auf einem MFT zu unterstützen:

-   [**WFTransform::AddInputStreams**](/windows/win32/api/mftransform/nf-mftransform-imftransform-addinputstreams)
-   [**TRIESTransform::D eleteInputStream**](/windows/win32/api/mftransform/nf-mftransform-imftransform-deleteinputstream)
-   [**WFTransform::GetStreamIDs**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getstreamids)
-   [**ÜBERTRANSFORM::GetStreamLimits**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getstreamlimits)

Darüber hinaus definiert die [**ROCESSOutput-Methode :P DAS**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processoutput) Verhalten zum Hinzufügen oder Entfernen von Ausgabestreams.

Da DMOs über feste Streams verfügen, werden die Streams auf einem DMO mit nullbasierten Indexwerten identifiziert. MFTs verwenden dagegen Streambezeichner, die nicht notwendigerweise Indexwerten entsprechen. Dies liegt daran, dass sich die Anzahl der Datenströme in einem MFT ändern kann. Beispielsweise kann Stream 0 entfernt werden, wobei Stream 1 als erster Stream verbleibt. Ein MFT mit einer festen Anzahl von Streams sollte jedoch die gleiche Konvention wie DMOs einhalten und Indexwerte für Streambezeichner verwenden.

## <a name="format-negotiation"></a>Formataushandlung

MFTs verwenden die [**SCHNITTSTELLE "MFMediaType",**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediatype) um Medientypen zu beschreiben. Andernfalls funktioniert die Formataushandlung mit MFTs nach denselben Grundprinzipien wie bei DMOs. In der folgenden Tabelle sind die Formataushandlungsmethoden für DMOs und die entsprechenden Methoden für MFTs aufgeführt.



| DMO-Methode                                                                        | MFT-Methode                                                                          |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**IMediaObject::GetInputCurrentType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputcurrenttype)   | [**ARCHETRANSFORM::GetInputCurrentType**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputcurrenttype)       |
| [**IMediaObject::GetInputMaxLatency**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputmaxlatency)     | [**ÜBERTRANSFORM::GetInputStreamInfo**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo)         |
| [**IMediaObject::GetInputSizeInfo**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputsizeinfo)         | [**ÜBERTRANSFORM::GetInputStreamInfo**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo)         |
| [**IMediaObject::GetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype)                 | [**ARCHETRANSFORM::GetInputAvailableType**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputavailabletype)   |
| [**IMediaObject::GetOutputCurrentType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputcurrenttype) | [**ARCHETRANSFORM::GetOutputCurrentType**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getoutputcurrenttype)     |
| [**IMediaObject::GetOutputSizeInfo**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputsizeinfo)       | [**WFTransform::GetOutputStreamInfo**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo)       |
| [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype)               | [**WFTransform::GetOutputAvailableType**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) |



 

## <a name="streaming"></a>Streaming

Wie DMOs verarbeiten MFTs Daten durch Aufrufe der [**ProcessInput-**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processinput) und [**ProcessOutput-Methoden.**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processoutput) Hier sind die hauptunterschiede zwischen DMO und MFT-Prozessen beim Streamen von Daten.

### <a name="allocating-resources"></a>Zuordnen von Ressourcen

MFTs verfügen nicht über die Methoden [**IMediaObject::AllocateStreamingResources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources) und [**IMediaObject::FreeStreamingResources,**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-freestreamingresources) die mit DMOs verwendet werden. Um die Zuordnung und Freigabe von Ressourcen effizient zu verarbeiten, kann ein MFT auf die folgenden Nachrichten in der [**ROCTRANSFORM::P rocessMessage-Methode**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) reagieren:

-   [**MFT \_ MESSAGE \_ NOTIFY \_ BEGIN \_ STREAMING**](mft-message-notify-begin-streaming.md)
-   [**MFT \_ MESSAGE NOTIFY START OF STREAM (MFT-NACHRICHT: \_ \_ BENACHRICHTIGUNG ZUM START DES \_ \_ STREAMS)**](mft-message-notify-start-of-stream.md)

Darüber hinaus kann der Client den Anfang und das Ende eines Streams signalisieren, indem [**er ProcessMessage**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) mit den folgenden Nachrichten aufruft:

-   [**MFT \_ MESSAGE \_ NOTIFY \_ END \_ OF \_ STREAM**](mft-message-notify-end-of-stream.md)
-   [**MFT \_ MESSAGE \_ NOTIFY \_ END \_ STREAMING**](mft-message-notify-end-streaming.md)

Diese beiden Nachrichten haben keine genaue DMO Entsprechung.

### <a name="processing-data"></a>Verarbeiten von Daten

MFTs verwenden Medienbeispiele, um Eingabe- und Ausgabedaten zu speichern. Medienbeispiele machen die [**INTERFACESSample-Schnittstelle**](/windows/win32/api/mfobjects/nn-mfobjects-imfsample) verfügbar und enthalten die folgenden Daten:

-   Zeitstempel und Dauer.
-   Attribute, die Pro-Beispiel-Informationen enthalten. Eine Liste der Attribute finden Sie unter [Beispielattribute.](sample-attributes.md)
-   0 (null) oder mehr Medienpuffer. Jeder Medienpuffer macht die [**INTERFACESMediaBuffer-Schnittstelle**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediabuffer) verfügbar.

Die [**INTERFACESMediaBuffer-Schnittstelle**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediabuffer) ähnelt der DMO **IMediaBuffer-Schnittstelle.** Um auf den zugrunde liegenden Speicherpuffer zuzugreifen, rufen Sie [**DENMEDIABUFFER::Lock**](/windows/win32/api/mfobjects/nf-mfobjects-imfmediabuffer-lock)auf. Diese Methode entspricht in etwa [**IMediaBuffer::GetBufferAndLength**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediabuffer-getbufferandlength) für DMOs.

Bei nicht komprimierten Videodaten unterstützt ein Medienpuffer möglicherweise auch die [**SCHNITTSTELLE "2DBuffer".**](/windows/win32/api/mfobjects/nn-mfobjects-imf2dbuffer) Ein MFT, der unkomprimierte Videos verarbeitet (entweder als Eingabe oder Als Ausgabe), sollte darauf vorbereitet sein, die **INTERFACES2DBuffer-Schnittstelle** zu verwenden, wenn sie vom Puffer verfügbar gemacht wird. Weitere Informationen finden Sie unter [Unkomprimierte Videopuffer.](uncompressed-video-buffers.md)

Media Foundation bietet einige Standardimplementierungen von [**BUFFERMediaBuffer,**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediabuffer)sodass es im Allgemeinen nicht erforderlich ist, eine eigene Implementierung zu schreiben. Um einen DMO Puffer aus einem Media Foundation Puffer zu erstellen, rufen Sie [**MFCreateLegacyMediaBufferOnMFMediaBuffer auf.**](/windows/win32/api/mfapi/nf-mfapi-mfcreatelegacymediabufferonmfmediabuffer)

### <a name="flushing"></a>Spülung

MFTs verfügen nicht über eine [**Flush-Methode.**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-flush) Um einen MFT zu leeren, rufen Sie [**ÜBERTRANSFORM::P rocessMessage**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) mit der [**MELDUNG MFT \_ MESSAGE COMMAND \_ \_ FLUSH**](mft-message-command-flush.md) auf.

### <a name="stream-discontinuities"></a>Stream-Diskontinuitäten

MFTs verfügen nicht über eine [**Discontinuity-Methode.**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-discontinuity) Um eine Diskontinuität in einem Stream zu signalisieren, legen Sie das [**MFSampleExtension \_ Discontinuity-Attribut**](mfsampleextension-discontinuity-attribute.md) für das Eingabebeispiel fest.

## <a name="miscellaneous-differences"></a>Verschiedene Unterschiede

Im Folgenden finden Sie einige weitere kleinere Unterschiede zwischen MFTs und DMOs.

-   Es gibt keine MFT-Entsprechungen für die folgenden DMO Methoden:
    -   [**IMediaObject::Lock**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-lock)
    -   [**IMediaObject::SetInputMaxLatency**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputmaxlatency)
-   MFTs sind nicht erforderlich, um die Aggregation zu unterstützen.
-   MFTs unterstützen einen Vorgang namens *Draining*. Der Zweck der Entleerung besteht darin, alle Daten zu verarbeiten, die im MF verbleiben, ohne dem MFT weitere Eingabedaten bereitzustellen (z. B. am Ende des Streams). Um einen MFT zu entladen, rufen Sie [**ÜBERTRANSFORM::P rocessMessage**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) mit der [**Meldung MFT \_ MESSAGE COMMAND \_ \_ DRAIN**](mft-message-command-drain.md) auf. Weitere Informationen finden Sie unter [Grundlegendes MFT-Verarbeitungsmodell.](basic-mft-processing-model.md)
-   MFTs können Attribute aufweisen, einschließlich streambasierter Attribute. Verwenden Sie die folgenden Methoden, um die Attribute aus einem MFT abzurufen:

    -   [**ÜBERTRANSFORM::GetAttributes**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getattributes)
    -   [**WFTransform::GetInputStreamAttributes**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes)
    -   [**WFTransform::GetOutputStreamAttributes**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes)

-   MFTs können Ereignisse verarbeiten. Um ein Ereignis an einen MFT zu senden, rufen Sie [**ÜBERTRANSFORM::P rocessEvent**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processevent)auf. Ein MFT kann über die [**ProcessOutput-Methode**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processoutput) ein Ereignis an den Client senden. Weitere Informationen finden Sie unter [Grundlegendes MFT-Verarbeitungsmodell.](basic-mft-processing-model.md)

## <a name="flags"></a>Flags

In den folgenden Tabellen sind die verschiedenen DMO-Flags und ihre MFT-Entsprechungen aufgeführt. Wenn ein DMO Flag direkt einem MFT-Flag zugeordnet wird, haben beide Flags den gleichen numerischen Wert. Einige DMO-Flags verfügen jedoch nicht über genaue MFT-Entsprechungen und umgekehrt.

### <a name="processinput-flags"></a>ProcessInput-Flags

DMOs: [**\_ DMO INPUT DATA \_ BUFFER \_ \_ \_ FLAGS-Enumeration.**](/previous-versions/windows/embedded/aa451599(v=msdn.10))

MFTs: Keine entsprechende Enumeration.



| DMO-Flag                                  | MFT-Flag                                                                                                                                      |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| **\_DMO INPUT \_ DATA \_ BUFFERF \_ SYNCPOINT**  | Kein entsprechendes Flag. Legen Sie stattdessen das [**\_ CleanPoint-Attribut MFSampleExtension**](mfsampleextension-cleanpoint-attribute.md) für das Beispiel fest. |
| **\_DMO PUFFERF-ZEIT FÜR \_ EINGABEDATEN \_ \_**       | Kein entsprechendes Flag. Rufen Sie stattdessen IM Beispiel [**DIE DATEI "SAMPLESSample::SetSampleTime"**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-setsampletime) auf.                                  |
| **\_DMO \_ \_ EINGABEDATENPUFFERF \_ TIMELENGTH** | Kein entsprechendes Flag. Rufen Sie stattdessen IM Beispiel [**DIE DATEI "WENDSAMPLE::SetSampleDuration"**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-setsampleduration) auf.                          |



 

### <a name="processoutput-flags"></a>ProcessOutput-Flags

DMOs: [**\_ DMO \_ PROCESS \_ OUTPUT \_ FLAGS-Enumeration.**](/previous-versions/windows/desktop/api/Mediaobj/ne-mediaobj-_dmo_process_output_flags)

MFTs: [**\_ MFT \_ PROCESS OUTPUT \_ \_ FLAGS-Enumeration.**](/windows/win32/api/mftransform/ne-mftransform-_mft_process_output_flags)



| DMO-Flag                                            | MFT-Flag                                            |
|-----------------------------------------------------|-----------------------------------------------------|
| **\_DMO VERWERFEN DER \_ VERARBEITUNGSAUSGABE, \_ \_ WENN KEIN PUFFER VORHANDEN \_ IST \_** | **AUSGABE \_ DES MFT-PROZESSES \_ \_ \_ VERWORFEN, WENN \_ KEIN PUFFER VORHANDEN IST \_** |



 

DMOs: [**\_ DMO OUTPUT DATA \_ BUFFER \_ \_ \_ FLAGS-Enumeration.**](/previous-versions/windows/desktop/api/Mediaobj/ne-mediaobj-_dmo_output_data_buffer_flags)


MFTs: [**\_ MFT \_ OUTPUT DATA BUFFER \_ \_ \_ FLAGS-Enumeration.**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_data_buffer_flags)



| DMO-Flag                                   | MFT-Flag                                                                                                                                            |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_DMO OUTPUT \_ DATA \_ BUFFERF \_ SYNCPOINT**  | Kein entsprechendes Flag. Suchen Sie stattdessen im Beispiel nach dem [**\_ CleanPoint-Attribut MFSampleExtension.**](mfsampleextension-cleanpoint-attribute.md) |
| **\_DMO PUFFERF-ZEIT FÜR \_ AUSGABEDATEN \_ \_**       | Kein entsprechendes Flag. Rufen Sie stattdessen IM Beispiel [**DIE DATEI "WFSAMPLE::GetSampleTime"**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-getsampletime) auf.                                        |
| **\_DMO \_ \_ AUSGABEDATENPUFFERF \_ TIMELENGTH** | Kein entsprechendes Flag. Rufen Sie stattdessen IM Beispiel [**DEN AUFRUF VONSAMPLE::GetSampleDuration**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-getsampleduration) auf.                                |
| **\_DMO \_ \_ AUSGABEDATENPUFFERF \_ UNVOLLSTÄNDIG** | **\_ \_ \_ MFT-AUSGABEDATENPUFFER \_ UNVOLLSTÄNDIG**                                                                                                           |
| Kein entsprechendes Flag.                        | **ÄNDERUNG DES \_ MFT-AUSGABEDATENPUFFERFORMATS \_ \_ \_ \_**                                                                                                       |
| Kein entsprechendes Flag.                        | **ENDE \_ DES MFT-AUSGABEDATENPUFFERSTREAMS \_ \_ \_ \_**                                                                                                          |
| Kein entsprechendes Flag.                        | **\_MFT-AUSGABEDATENPUFFER \_ \_ KEINE \_ \_ STICHPROBE**                                                                                                           |



 

### <a name="getinputstatus-flags"></a>GetInputStatus-Flags

DMOs: **\_ DMO \_ \_ \_ EINGABESTATUS-FLAGS-Enumeration.**

MFTs: [**\_ MFT \_ INPUT STATUS \_ \_ FLAGS-Enumeration.**](/windows/win32/api/mftransform/ne-mftransform-_mft_input_status_flags)



| DMO-Flag                              | MFT-Flag                             |
|---------------------------------------|--------------------------------------|
| **\_DMO \_EINGABESTATUSF: \_ DATEN AKZEPTIEREN \_** | **\_MFT-EINGABESTATUS \_ \_ AKZEPTIEREN VON \_ DATEN** |



 

### <a name="getoutputstatus-flags"></a>GetOutputStatus-Flags

DMOs: Keine entsprechende Enumeration.

MFTs: [**\_ MFT \_ OUTPUT STATUS \_ \_ FLAGS-Enumeration.**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_status_flags)



| DMO-Flag            | MFT-Flag                               |
|---------------------|----------------------------------------|
| Kein entsprechendes Flag. | **\_MFT-AUSGABESTATUSBEISPIEL \_ \_ \_ BEREIT** |



 

### <a name="getinputstreaminfo-flags"></a>GetInputStreamInfo-Flags

DMOs: [**\_ DMO \_ INPUT \_ STREAM INFO \_ \_ FLAGS-Enumeration.**](/previous-versions/windows/embedded/aa451600(v=msdn.10))

MFTs: [**\_ MFT \_ INPUT STREAM INFO \_ \_ \_ FLAGS-Enumeration.**](/windows/win32/api/mftransform/ne-mftransform-_mft_input_stream_info_flags)



| DMO-Flag                                             | MFT-Flag                                            |
|------------------------------------------------------|-----------------------------------------------------|
| **\_DMO EINGABE VON \_ STREAMF \_ GANZE \_ BEISPIELE**              | **\_ \_ MFT-EINGABESTREAM \_ – GANZE \_ BEISPIELE**              |
| **\_DMO EINGABE \_ EINES \_ STREAMF-EINZELBEISPIELS \_ \_ PRO \_ PUFFER** | **EINZELNES \_ \_ MFT-EINGABESTREAMBEISPIEL PRO \_ \_ \_ \_ PUFFER** |
| **\_DMO \_EINGABESTREAMF \_ – FESTE \_ \_ STICHPROBENGRÖßE**         | **\_MFT INPUT \_ STREAM FIXED SAMPLE SIZE \_ (FESTE STICHPROBENGRÖßE FÜR MFT-EINGABESTREAM) \_ \_**         |
| **\_DMO \_EINGABESTREAMF \_ ENTHÄLT \_ PUFFER**              | **\_MFT-EINGABESTREAM \_ \_ ENTHÄLT \_ PUFFER**              |
| Kein entsprechendes Flag.                                  | **MFT \_ INPUT STREAM DOES NOT ADDREF (MFT-EINGABESTREAM \_ FÜGT NICHT \_ \_ \_ HINZUREF)**           |
| Kein entsprechendes Flag.                                  | **MFT \_ INPUT \_ STREAM \_ REMOVABLE**                   |
| Kein entsprechendes Flag.                                  | **MFT \_ INPUT \_ STREAM \_ OPTIONAL**                    |



 

### <a name="getoutputstreaminfo-flags"></a>GetOutputStreamInfo-Flags

DMOs: [**\_ DMO OUTPUT STREAM \_ INFO \_ \_ \_ FLAGS-Enumeration.**](/previous-versions/ms806053(v=msdn.10))

MFTs: [**\_ MFT \_ OUTPUT STREAM INFO \_ \_ \_ FLAGS-Enumeration.**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_stream_info_flags)



| DMO-Flag                                              | MFT-Flag                                             |
|-------------------------------------------------------|------------------------------------------------------|
| **\_DMO AUSGEBEN \_ \_ VON STREAMF-BEISPIELEN (GANZE \_ BEISPIELE)**              | **\_ \_ MFT-AUSGABESTREAM \_ – GANZE \_ BEISPIELE**              |
| **\_DMO AUSGABE \_ EINES \_ STREAMF-EINZELBEISPIELS \_ \_ PRO \_ PUFFER** | **EINZELNES \_ \_ MFT-AUSGABESTREAMBEISPIEL PRO \_ \_ \_ \_ PUFFER** |
| **\_DMO \_AUSGABESTREAMF \_ – FESTE \_ \_ STICHPROBENGRÖßE**         | **FESTE \_ \_ \_ \_ \_ BEISPIELGRÖßE FÜR MFT-AUSGABESTREAM**         |
| **\_DMO AUSGABE \_ STREAMF \_ VERWERF VERWERFBAR**                 | **\_MFT-AUSGABESTREAM \_ \_ VERWERFBAR**                 |
| **\_DMO OUTPUT \_ STREAMF \_ OPTIONAL**                    | **\_MFT-AUSGABESTREAM \_ \_ OPTIONAL**                    |
| Kein entsprechendes Flag.                                   | **\_MFT-AUSGABESTREAM \_ \_ STELLT BEISPIELE \_ BEREIT.**           |
| Kein entsprechendes Flag.                                   | **\_MFT-AUSGABESTREAM \_ \_ KANN \_ BEISPIELE BEREITSTELLEN \_**       |
| Kein entsprechendes Flag.                                   | **MFT \_ OUTPUT \_ STREAM \_ LAZY \_ READ**                  |
| Kein entsprechendes Flag.                                   | **\_MFT-AUSGABESTREAM \_ \_ WECHSELBAR**                   |



 

### <a name="setinputtypesetoutputtype-flags"></a>SetInputType/SetOutputType-Flags

DMOs: [**\_ DMO SET TYPE \_ \_ \_ FLAGS-Enumeration.**](/previous-versions/windows/desktop/api/Mediaobj/ne-mediaobj-_dmo_set_type_flags)

MFTs: [**\_ MFT \_ SET TYPE \_ \_ FLAGS-Enumeration.**](/windows/win32/api/mftransform/ne-mftransform-_mft_set_type_flags)



| DMO-Flag                        | MFT-Flag                                                                             |
|---------------------------------|--------------------------------------------------------------------------------------|
| **\_DMO SET \_ TYPEF \_ TEST \_ ONLY** | **NUR MFT \_ SET \_ TYPE \_ TEST \_**                                                       |
| **\_DMO SET \_ TYPEF \_ CLEAR**      | Kein entsprechendes Flag. Legen Sie stattdessen den Medientyp auf **NULL** fest, um den Medientyp zu löschen. |



 

## <a name="error-codes"></a>Fehlercodes

Die folgende Tabelle zeigt, wie sie MFT-Fehlercodes DMO Fehlercodes zuordnen. Ein Hybrid-MFT-/DMO-Objekt sollte die DMO Fehlercodes von [**IMediaObject-Methoden**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) und die MFT-Fehlercodes von [**DEN METHODEN DERTRANSFORM-Methode**](/windows/win32/api/mftransform/nn-mftransform-imftransform) zurückgeben. Die DMO Fehlercodes werden in der Headerdatei MediaErr.h definiert. Die MFT-Fehlercodes werden in der Headerdatei mferror.h definiert.



| DMO Fehlercode                  | MFT-Fehlercode                       |
|---------------------------------|--------------------------------------|
| **\_DMO E \_ INVALIDTYPE**         | **MF \_ E \_ INVALIDTYPE**               |
| **\_DMO E \_ INVALIDSTREAMINDEX**  | **MF \_ E \_ INVALIDSTREAMNUMBER**       |
| **\_DMO E \_ NICHT AKZEPTIERT**        | **MF \_ E \_ NOTACCEPTING**              |
| **\_DMO E \_ NO \_ MORE \_ ITEMS**     | **MF \_ E \_ NO \_ MORE \_ TYPES**           |
| **\_DMO \_E-TYP \_ NICHT \_ AKZEPTIERT** | **MF \_ E \_ INVALIDMEDIATYPE**          |
| **\_DMO E \_ TYPE \_ NOT \_ SET**      | **MF \_ E \_ TRANSFORM \_ TYPE \_ NOT \_ SET** |



 

## <a name="creating-hybrid-dmomft-objects"></a>Erstellen von Hybrid-DMO/MFT-Objekten

Die [**INTERFACESTransform-Schnittstelle**](/windows/win32/api/mftransform/nn-mftransform-imftransform) basiert lose auf [**IMediaObject,**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)der primären Schnittstelle für DirectX Media Objects (DMOs). Es ist möglich, Objekte zu erstellen, die beide Schnittstellen verfügbar machen. Dies kann jedoch zu Namenskonflikten führen, da die Schnittstellen über einige Methoden verfügen, die den gleichen Namen aufweisen. Sie können dieses Problem auf zwei Arten lösen:

Lösung 1: Fügen Sie die folgende Zeile am Anfang einer CPP-Datei ein, die MFT-Funktionen enthält:

``` syntax
#define MFT_UNIQUE_METHOD_NAMES
```

Dadurch wird die Deklaration der [**INTERFACESTransform-Schnittstelle**](/windows/win32/api/mftransform/nn-mftransform-imftransform) so geändert, dass den meisten Methodennamen das Präfix "MFT" vorangestellt wird. Daher wird [**VONTRANSFORM::P rocessInput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processinput) zu **EINERTRANSFORM::MFTProcessInput,** während [**IMediaObject::P rocessInput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) seinen ursprünglichen Namen beibehält. Diese Technik ist besonders nützlich, wenn Sie eine vorhandene DMO in eine Hybrid-DMO/MFT konvertieren. Sie können die neuen MFT-Methoden hinzufügen, ohne die DMO Methoden zu ändern.

Lösung 2: Verwenden Sie die C++-Syntax, um Namen zu unterscheiden, die von mehreren Schnittstellen geerbt werden. Deklarieren Sie beispielsweise die MFT-Version von [**ProcessInput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processinput) wie folgt:

``` syntax
CMyHybridObject::IMFTransform::ProcessInput(...)
```

Deklarieren Sie die DMO Version von [**ProcessInput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) wie folgt:

``` syntax
CMyHybridObject::IMediaObject::ProcessInput(...)
```

Wenn Sie eine Methode innerhalb des -Objekts intern aufrufen, können Sie diese Syntax verwenden. Dadurch wird jedoch der virtuelle Status der Methode überschrieben. Eine bessere Möglichkeit zum Ausführen von Aufrufen innerhalb des -Objekts ist folgende:

``` syntax
hr = ((IMediaObject*)this)->ProcessInput(...)
```

Auf diese Weise wird die richtige virtuelle Methode aufgerufen, wenn Sie eine andere Klasse von **CMyHybridObject** ableiten und die CMyHybridObject::IMediaObject::P rocessInput-Methode überschreiben. Die DMO Schnittstellen sind in der DirectShow SDK-Dokumentation dokumentiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation Transformationen](media-foundation-transforms.md)
</dt> </dl>

 

 

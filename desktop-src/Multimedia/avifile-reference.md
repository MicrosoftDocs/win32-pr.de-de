---
title: AVIFile-Referenz
description: AVIFile-Referenz
ms.assetid: 73532d83-89c2-4911-8558-ce110e9f0f95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19b4bbda5374f5b1418c166aae5efcc06168b522b2cae0f3b6d2c8fe3c069c36
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808320"
---
# <a name="avifile-reference"></a>AVIFile-Referenz

In diesem Abschnitt werden die Funktionen, Strukturen und Makros für Anwendungen beschrieben, die die AVIFile-Dienste verwenden. Diese Elemente sind wie folgt gruppiert:

## <a name="avifile-library-operations"></a>AVIFile-Bibliotheksvorgänge

-   [**AVIFileInit**](/windows/desktop/api/Vfw/nf-vfw-avifileinit)
-   [**AVIFileExit**](/windows/desktop/api/Vfw/nf-vfw-avifileexit)

## <a name="opening-and-closing-avi-files"></a>Öffnen und Schließen von AVI-Dateien

-   [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen)
-   [**AVIFileAddRef**](/windows/desktop/api/Vfw/nf-vfw-avifileaddref)
-   [**AVIFileRelease**](/windows/desktop/api/Vfw/nf-vfw-avifilerelease)
-   [**GetOpenFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa)

## <a name="reading-from-a-file"></a>Lesen aus einer Datei

-   [**AVIFileInfo**](/windows/desktop/api/Vfw/nf-vfw-avifileinfo)
-   [**AVIFILEINFO**](/windows/desktop/api/Vfw/ns-vfw-avifileinfoa)
-   [**AVIFileReadData**](/windows/desktop/api/Vfw/nf-vfw-avifilereaddata)

## <a name="writing-to-a-file"></a>Schreiben in eine Datei

-   [**AVIFileWriteData**](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata)

## <a name="using-the-clipboard"></a>Verwenden der Zwischenablage

-   [**AVIPutFileOnClipboard**](/windows/desktop/api/Vfw/nf-vfw-aviputfileonclipboard)
-   [**AVIGetFromClipboard**](/windows/desktop/api/Vfw/nf-vfw-avigetfromclipboard)
-   [**AVIClearClipboard**](/windows/desktop/api/Vfw/nf-vfw-aviclearclipboard)

## <a name="opening-and-closing-streams"></a>Öffnende und schließende Streams

-   [**AVIFileGetStream**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream)
-   [**AVIStreamOpenFromFile**](/windows/desktop/api/Vfw/nf-vfw-avistreamopenfromfilea)
-   [**AVIStreamAddRef**](/windows/desktop/api/Vfw/nf-vfw-avistreamaddref)
-   [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease)

## <a name="reading-stream-information"></a>Lesen von Streaminformationen

-   [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa)
-   [**AVIStreamReadData**](/windows/desktop/api/Vfw/nf-vfw-avistreamreaddata)
-   [**AVIStreamDataSize**](/windows/desktop/api/Vfw/nf-vfw-avistreamdatasize)
-   [**AVIStreamReadFormat**](/windows/desktop/api/Vfw/nf-vfw-avistreamreadformat)
-   [**AVIStreamFormatSize**](/windows/desktop/api/Vfw/nf-vfw-avistreamformatsize)
-   [**AVIStreamRead**](/windows/desktop/api/Vfw/nf-vfw-avistreamread)
-   [**AVIStreamSampleSize**](/windows/desktop/api/Vfw/nf-vfw-avistreamsamplesize)
-   [**AVIStreamBeginStreaming**](/windows/desktop/api/Vfw/nf-vfw-avistreambeginstreaming)
-   [**AVIStreamEndStreaming**](/windows/desktop/api/Vfw/nf-vfw-avistreamendstreaming)

## <a name="decompressing-video-data-in-a-stream"></a>Dekomprimieren von Videodaten in einem Stream

-   [**AVIStreamGetFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeopen)
-   [**AVIStreamGetFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframe)
-   [**AVIStreamGetFrameClose**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeclose)

## <a name="creating-a-file-from-existing-streams"></a>Erstellen einer Datei aus einem vorhandenen Streams

-   [**AVISave**](/windows/desktop/api/Vfw/nf-vfw-avisavea)
-   [**AVISaveV**](/windows/desktop/api/Vfw/nf-vfw-avisaveva)
-   [**AVISaveOptions**](/windows/desktop/api/Vfw/nf-vfw-avisaveoptions)
-   [**GetSaveFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getsavefilenamepreviewa)
-   [**AVIMakeFileFromStreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams)

## <a name="writing-individual-streams"></a>Schreiben einzelner Streams

-   [**AVIFileCreateStream**](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream)
-   [**AVIStreamSetFormat**](/windows/desktop/api/Vfw/nf-vfw-avistreamsetformat)
-   [**AVIStreamWrite**](/windows/desktop/api/Vfw/nf-vfw-avistreamwrite)
-   [**AVIFileWriteData**](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata)
-   [**AVIStreamWriteData**](/windows/desktop/api/Vfw/nf-vfw-avistreamwritedata)
-   [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease)

## <a name="finding-the-starting-position-in-a-stream"></a>Suchen der Anfangsposition in einem Stream

-   [**AVIStreamStart**](/windows/desktop/api/Vfw/nf-vfw-avistreamstart)
-   [**AVIStreamStartTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamstarttime)
-   [**AVIStreamLength**](/windows/desktop/api/Vfw/nf-vfw-avistreamlength)
-   [**AVIStreamLengthTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamlengthtime)
-   [**AVIStreamFindSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamfindsample)
-   [**AVIStreamEnd**](/windows/desktop/api/Vfw/nf-vfw-avistreamend)
-   [**AVIStreamEndTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamendtime)

## <a name="finding-sample-and-key-frames"></a>Suchen von Beispiel- und Keyframes

-   [**AVIStreamFindSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamfindsample)
-   [**AVIStreamIsKeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamiskeyframe)
-   [**AVIStreamStreamStreamrestKeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestkeyframe)
-   [**AVIStreamStreamStreamRestKeyFrameTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestkeyframetime)
-   [**AVIStreamStreamStreamrestSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestsample)
-   [**AVIStreamStreamStreamRestSampleTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestsampletime)
-   [**AVIStreamNextKeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextkeyframe)
-   [**AVIStreamNextKeyFrameTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextkeyframetime)
-   [**AVIStreamNextSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextsample)
-   [**AVIStreamNextSampleTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextsampletime)
-   [**AVIStreamPrevKeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevkeyframe)
-   [**AVIStreamPrevKeyFrameTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevkeyframetime)
-   [**AVIStreamPrevSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevsample)
-   [**AVIStreamPrevSampleTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevsampletime)
-   [**AVIStreamSampleToSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamsampletosample)

## <a name="switching-between-samples-and-time"></a>Wechseln zwischen Beispielen und Zeit

-   [**AVIStreamSampleToTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamsampletotime)
-   [**AVIStreamTimeToSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamtimetosample)

## <a name="creating-temporary-streams"></a>Erstellen von temporären Streams

-   [**AVIStreamCreate**](/windows/desktop/api/Vfw/nf-vfw-avistreamcreate)
-   [**AVIMakeCompressedStream**](/windows/desktop/api/Vfw/nf-vfw-avimakecompressedstream)
-   [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease)

## <a name="editing-avi-streams"></a>Bearbeiten von AVI-Streams

-   [**CreateEditableStream**](/windows/desktop/api/Vfw/nf-vfw-createeditablestream)
-   [**EditStreamCut**](/windows/desktop/api/Vfw/nf-vfw-editstreamcut)
-   [**EditStreamCopy**](/windows/desktop/api/Vfw/nf-vfw-editstreamcopy)
-   [**EditStreamPaste**](/windows/desktop/api/Vfw/nf-vfw-editstreampaste)
-   [**EditStreamClone**](/windows/desktop/api/Vfw/nf-vfw-editstreamclone)
-   [**EditStreamSetInfo**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetinfoa)
-   [**EditStreamSetName**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetnamea)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[AVIFile-Funktionen und -Makros](avifile-functions-and-macros.md)
</dt> </dl>

 

 





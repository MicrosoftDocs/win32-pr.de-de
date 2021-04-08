---
title: Avifile-Referenz
description: Avifile-Referenz
ms.assetid: 73532d83-89c2-4911-8558-ce110e9f0f95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0291d0ac5864a9b370e79a98fa061770d05bca03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037515"
---
# <a name="avifile-reference"></a>Avifile-Referenz

In diesem Abschnitt werden die Funktionen, Strukturen und Makros für Anwendungen beschrieben, die die avifile-Dienste verwenden. Diese Elemente werden wie folgt gruppiert:

## <a name="avifile-library-operations"></a>Vorgänge der avifile-Bibliothek

-   [**Avifileingeit**](/windows/desktop/api/Vfw/nf-vfw-avifileinit)
-   [**Avifileexit**](/windows/desktop/api/Vfw/nf-vfw-avifileexit)

## <a name="opening-and-closing-avi-files"></a>Öffnen und Schließen von AVI-Dateien

-   [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen)
-   [**Avifileadressf**](/windows/desktop/api/Vfw/nf-vfw-avifileaddref)
-   [**Avifilerelease**](/windows/desktop/api/Vfw/nf-vfw-avifilerelease)
-   [**Getopendatamepreview**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa)

## <a name="reading-from-a-file"></a>Lesen aus einer Datei

-   [**Avifileingefo**](/windows/desktop/api/Vfw/nf-vfw-avifileinfo)
-   [**Avifileingefo**](/windows/desktop/api/Vfw/ns-vfw-avifileinfoa)
-   [**Avifilereaddata**](/windows/desktop/api/Vfw/nf-vfw-avifilereaddata)

## <a name="writing-to-a-file"></a>Schreiben in eine Datei

-   [**Avifileschreitedata**](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata)

## <a name="using-the-clipboard"></a>Verwenden der Zwischenablage

-   [**Aviputfleonclipboard**](/windows/desktop/api/Vfw/nf-vfw-aviputfileonclipboard)
-   [**Avigetfromclipboard**](/windows/desktop/api/Vfw/nf-vfw-avigetfromclipboard)
-   [**Aviclearclipboard**](/windows/desktop/api/Vfw/nf-vfw-aviclearclipboard)

## <a name="opening-and-closing-streams"></a>Öffnen und Schließen von Streams

-   [**AVIFileGetStream**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream)
-   [**Avistreamopenfromfile**](/windows/desktop/api/Vfw/nf-vfw-avistreamopenfromfilea)
-   [**Avistreamadressf**](/windows/desktop/api/Vfw/nf-vfw-avistreamaddref)
-   [**Avistreamrelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease)

## <a name="reading-stream-information"></a>Lesen von streaminformationen

-   [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa)
-   [**Avistreamlesdata**](/windows/desktop/api/Vfw/nf-vfw-avistreamreaddata)
-   [**Avistreamdatasize**](/windows/desktop/api/Vfw/nf-vfw-avistreamdatasize)
-   [**Avistreamlesformat**](/windows/desktop/api/Vfw/nf-vfw-avistreamreadformat)
-   [**Avistreamformatsize**](/windows/desktop/api/Vfw/nf-vfw-avistreamformatsize)
-   [**Avistreamread**](/windows/desktop/api/Vfw/nf-vfw-avistreamread)
-   [**Avistreamsamplesize**](/windows/desktop/api/Vfw/nf-vfw-avistreamsamplesize)
-   [**Avistreambeginstreaming**](/windows/desktop/api/Vfw/nf-vfw-avistreambeginstreaming)
-   [**Avistreamendstreaming**](/windows/desktop/api/Vfw/nf-vfw-avistreamendstreaming)

## <a name="decompressing-video-data-in-a-stream"></a>Dekomprimieren von Video Daten in einem Stream

-   [**AVIStreamGetFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeopen)
-   [**AVIStreamGetFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframe)
-   [**Avistreamgetframeclose**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeclose)

## <a name="creating-a-file-from-existing-streams"></a>Erstellen einer Datei aus vorhandenen Streams

-   [**Avisave**](/windows/desktop/api/Vfw/nf-vfw-avisavea)
-   [**Avisavev**](/windows/desktop/api/Vfw/nf-vfw-avisaveva)
-   [**Avisaveoptions**](/windows/desktop/api/Vfw/nf-vfw-avisaveoptions)
-   [**Getsavefile Name Preview**](/windows/desktop/api/Vfw/nf-vfw-getsavefilenamepreviewa)
-   [**Avimakefilefromstreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams)

## <a name="writing-individual-streams"></a>Schreiben einzelner Streams

-   [**Avifilekreatestream**](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream)
-   [**Avistreamsetformat**](/windows/desktop/api/Vfw/nf-vfw-avistreamsetformat)
-   [**AVIStreamWrite**](/windows/desktop/api/Vfw/nf-vfw-avistreamwrite)
-   [**Avifileschreitedata**](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata)
-   [**Avistreamschreitedata**](/windows/desktop/api/Vfw/nf-vfw-avistreamwritedata)
-   [**Avistreamrelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease)

## <a name="finding-the-starting-position-in-a-stream"></a>Ermitteln der Anfangs Position in einem Stream

-   [**AVIStreamStart**](/windows/desktop/api/Vfw/nf-vfw-avistreamstart)
-   [**Avistreamstarttime**](/windows/desktop/api/Vfw/nf-vfw-avistreamstarttime)
-   [**Avistreamlength**](/windows/desktop/api/Vfw/nf-vfw-avistreamlength)
-   [**Avistreamverlängert-Zeit**](/windows/desktop/api/Vfw/nf-vfw-avistreamlengthtime)
-   [**Avistreamfindsample**](/windows/desktop/api/Vfw/nf-vfw-avistreamfindsample)
-   [**Avistreamend**](/windows/desktop/api/Vfw/nf-vfw-avistreamend)
-   [**Avistreamendzeit**](/windows/desktop/api/Vfw/nf-vfw-avistreamendtime)

## <a name="finding-sample-and-key-frames"></a>Suchen von Beispiel-und Keyframes

-   [**Avistreamfindsample**](/windows/desktop/api/Vfw/nf-vfw-avistreamfindsample)
-   [**Avistreamiskeyframe**](/windows/desktop/api/Vfw/nf-vfw-avistreamiskeyframe)
-   [**Avistreamnearestkeyframe**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestkeyframe)
-   [**Avistreamnearestkeyframetime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestkeyframetime)
-   [**Avistreamnearestsample**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestsample)
-   [**Avistreamnearestsampletime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestsampletime)
-   [**Avistreamnextkeyframe**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextkeyframe)
-   [**Avistreamnextkeyframetime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextkeyframetime)
-   [**Avistreamnextsample**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextsample)
-   [**Avistreamnextsampletime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextsampletime)
-   [**Avistreamprevkeyframe**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevkeyframe)
-   [**Avistreamprevkeyframetime**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevkeyframetime)
-   [**Avistreamprevsample**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevsample)
-   [**Avistreamprevsampletime**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevsampletime)
-   [**Avistreamsampleprosample**](/windows/desktop/api/Vfw/nf-vfw-avistreamsampletosample)

## <a name="switching-between-samples-and-time"></a>Wechseln zwischen Beispielen und Zeit

-   [**Avistreamsamplecomtime**](/windows/desktop/api/Vfw/nf-vfw-avistreamsampletotime)
-   [**Avistreamtimeto Sample**](/windows/desktop/api/Vfw/nf-vfw-avistreamtimetosample)

## <a name="creating-temporary-streams"></a>Erstellen temporärer Streams

-   [**Avistreamcreate**](/windows/desktop/api/Vfw/nf-vfw-avistreamcreate)
-   [**Avimakecompressedstream**](/windows/desktop/api/Vfw/nf-vfw-avimakecompressedstream)
-   [**Avistreamrelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease)

## <a name="editing-avi-streams"></a>Bearbeiten von AVI-Streams

-   [**"Kreateeditablestream"**](/windows/desktop/api/Vfw/nf-vfw-createeditablestream)
-   [**Editstreamcut**](/windows/desktop/api/Vfw/nf-vfw-editstreamcut)
-   [**Editstreamcopy**](/windows/desktop/api/Vfw/nf-vfw-editstreamcopy)
-   [**Editstreampaste**](/windows/desktop/api/Vfw/nf-vfw-editstreampaste)
-   [**Editstreamclone**](/windows/desktop/api/Vfw/nf-vfw-editstreamclone)
-   [**Editstreamabtinfo**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetinfoa)
-   [**Editstreamsetname**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetnamea)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Avifile-Funktionen und-Makros](avifile-functions-and-macros.md)
</dt> </dl>

 

 





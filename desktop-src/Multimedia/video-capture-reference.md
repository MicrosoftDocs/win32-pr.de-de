---
title: Videoaufnahmereferenz
description: Videoaufnahmereferenz
ms.assetid: 5356c575-2a59-4459-b4eb-76967deb6877
keywords:
- Video for Windows (VFW), Videoaufnahmereferenz
- VFW (Video for Windows),Video capture reference
- AVICap, Referenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 166bdcf06e700023a197334b0e63f612398485affe21dc9ffbc6e7ac0800926a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119804310"
---
# <a name="video-capture-reference"></a>Videoaufnahmereferenz

In diesem Abschnitt werden die Funktionen, Strukturen, Meldungen und Makros beschrieben, die der WINDOWCap-Fensterklasse zugeordnet sind. Diese Elemente sind wie folgt gruppiert.

## <a name="basic-capture-operations"></a>Grundlegende Erfassungsvorgänge

-   [**capCreateCaptureWindow**](/windows/desktop/api/Vfw/nf-vfw-capcreatecapturewindowa)
-   [**WM \_ CAP \_ ABORT**](wm-cap-abort.md)
-   [**WM \_ CAP \_ DRIVER \_ CONNECT**](wm-cap-driver-connect.md)
-   [**\_ \_ WM-CAP-SEQUENZ**](wm-cap-sequence.md)
-   [**WM \_ CAP \_ STOP**](wm-cap-stop.md)

## <a name="capture-windows"></a>Erfassungs Windows

-   [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus)
-   [**capGetDriverDescription**](/windows/desktop/api/Vfw/nf-vfw-capgetdriverdescriptiona)
-   [**WM \_ CAP \_ DRIVER \_ CONNECT**](wm-cap-driver-connect.md)
-   [**WM \_ CAP \_ DRIVER \_ DISCONNECT**](wm-cap-driver-disconnect.md)
-   [**WM \_ CAP \_ GET \_ STATUS**](wm-cap-get-status.md)

## <a name="capture-drivers"></a>Erfassen von Treibern

-   [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps)
-   [**WM \_ CAP \_ DRIVER \_ GET \_ CAPS**](wm-cap-driver-get-caps.md)
-   [**WM \_ CAP \_ DRIVER \_ GET \_ NAME**](wm-cap-driver-get-name.md)
-   [**WM \_ CAP \_ DRIVER \_ GET \_ VERSION**](wm-cap-driver-get-version.md)
-   [**WM \_ CAP \_ GET \_ AUDIOFORMAT**](wm-cap-get-audioformat.md)
-   [**WM \_ CAP \_ GET \_ VIDEOFORMAT**](wm-cap-get-videoformat.md)
-   [**WM \_ CAP \_ SET \_ AUDIOFORMAT**](wm-cap-set-audioformat.md)
-   [**WM \_ CAP \_ SET \_ VIDEOFORMAT**](wm-cap-set-videoformat.md)

## <a name="capture-driver-preview-and-overlay-modes"></a>Vorschau- und Überlagerungsmodi des Erfassungstreibers

-   [**WM \_ CAP \_ SET \_ OVERLAY**](wm-cap-set-overlay.md)
-   [**WM \_ CAP \_ SET \_ PREVIEW**](wm-cap-set-preview.md)
-   [**WM \_ CAP \_ SET \_ PREVIEWRATE**](wm-cap-set-previewrate.md)
-   [**WM \_ CAP \_ SET \_ SCALE**](wm-cap-set-scale.md)
-   [**WM \_ CAP \_ SET \_ SCROLL**](wm-cap-set-scroll.md)

## <a name="capture-driver-video-dialog-boxes"></a>Dialogfelder zum Erfassen von Treibervideos

-   [**WM \_ CAP \_ DLG \_ VIDEOCOMPRESSION**](wm-cap-dlg-videocompression.md)
-   [**WM \_ CAP \_ DLG \_ VIDEODISPLAY**](wm-cap-dlg-videodisplay.md)
-   [**WM \_ CAP \_ DLG \_ VIDEOFORMAT**](wm-cap-dlg-videoformat.md)
-   [**WM \_ CAP \_ DLG \_ VIDEOSOURCE**](wm-cap-dlg-videosource.md)

## <a name="audio-format"></a>Audioformat

-   [**WM \_ CAP \_ GET \_ AUDIOFORMAT**](wm-cap-get-audioformat.md)
-   [**WM \_ CAP \_ SET \_ AUDIOFORMAT**](wm-cap-set-audioformat.md)

## <a name="video-capture-settings"></a>Video capture Einstellungen

-   [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms)
-   [**WM \_ CAP \_ GET \_ SEQUENCE \_ SETUP**](wm-cap-get-sequence-setup.md)
-   [**WM \_ CAP \_ SET \_ SEQUENCE \_ SETUP**](wm-cap-set-sequence-setup.md)

## <a name="capture-file-and-buffers"></a>Erfassen von Dateien und Puffern

-   [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms)
-   [**WM \_ CAP \_ FILE \_ ALLOCATE**](wm-cap-file-allocate.md)
-   [**WM \_ CAP \_ FILE \_ GET \_ CAPTURE \_ FILE**](wm-cap-file-get-capture-file.md)
-   [**WM \_ CAP \_ FILE \_ SAVEAS**](wm-cap-file-saveas.md)
-   [**WM \_ CAP \_ FILE \_ SET \_ CAPTURE \_ FILE**](wm-cap-file-set-capture-file.md)

## <a name="directly-using-capture-data"></a>Direktes Verwenden von Erfassungsdaten

-   [**WM \_ CAP \_ SEQUENCE \_ NOFILE**](wm-cap-sequence-nofile.md)

## <a name="capture-from-mci-device"></a>Erfassen über ein MCI-Gerät

-   [**WM \_ CAP \_ SET \_ MCI \_ DEVICE**](wm-cap-set-mci-device.md)

## <a name="manual-frame-capture"></a>Manuelle Frameerfassung

-   [**WM \_ CAP \_ SINGLE \_ FRAME**](wm-cap-single-frame.md)
-   [**WM \_ CAP \_ SINGLE \_ FRAME \_ CLOSE**](wm-cap-single-frame-close.md)
-   [**WM \_ CAP \_ SINGLE \_ FRAME \_ OPEN**](wm-cap-single-frame-open.md)

## <a name="still-image-capture"></a>Still-Image Capture

-   [**WM \_ CAP \_ EDIT \_ COPY**](wm-cap-edit-copy.md)
-   [**WM \_ CAP \_ FILE \_ SAVEDIB**](wm-cap-file-savedib.md)
-   [**WM \_ CAP \_ GRAB \_ FRAME**](wm-cap-grab-frame.md)
-   [**WM \_ CAP \_ GRAB \_ FRAME \_ NOSTOP**](wm-cap-grab-frame-nostop.md)

## <a name="advanced-capture-options"></a>Erweiterte Erfassungsoptionen

-   [**WM \_ CAP \_ FILE \_ SET \_ INFOCHUNK**](wm-cap-file-set-infochunk.md)
-   [**WM \_ CAP \_ GET \_ USER \_ DATA**](wm-cap-get-user-data.md)
-   [**WM \_ CAP \_ \_ SET-BENUTZERDATEN \_**](wm-cap-set-user-data.md)

## <a name="working-with-palettes"></a>Arbeiten mit Paletten

-   [**WM \_ CAP \_ EDIT \_ COPY**](wm-cap-edit-copy.md)
-   [**WM \_ CAP \_ PAL \_ AUTOCREATE**](wm-cap-pal-autocreate.md)
-   [**WM \_ CAP \_ PAL \_ MANUALCREATE**](wm-cap-pal-manualcreate.md)
-   [**WM \_ CAP \_ PAL \_ OPEN**](wm-cap-pal-open.md)
-   [**WM \_ CAP \_ PAL \_ PASTE**](wm-cap-pal-paste.md)
-   [**WM \_ CAP \_ PAL \_ SAVE**](wm-cap-pal-save.md)

## <a name="yielding-to-other-applications"></a>Yielding to Other Applications

-   [**WM \_ CAP \_ GET \_ SEQUENCE \_ SETUP**](wm-cap-get-sequence-setup.md)
-   [**WM \_ CAP \_ SET \_ CALLBACK \_ YIELD**](wm-cap-set-callback-yield.md)
-   [**WM \_ CAP \_ SET \_ SEQUENCE \_ SETUP**](wm-cap-set-sequence-setup.md)

## <a name="avicap-callback-functions"></a>AVICap-Rückruffunktionen

-   [**capControlCallback**](/windows/desktop/api/Vfw/nc-vfw-capcontrolcallback)
-   [**capErrorCallback**](/windows/desktop/api/Vfw/nc-vfw-caperrorcallbacka)
-   [**capStatusCallback**](/windows/desktop/api/Vfw/nc-vfw-capstatuscallbacka)
-   [**capVideoStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback)
-   [**capWaveStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capwavecallback)
-   [**capYieldCallback**](/windows/desktop/api/Vfw/nc-vfw-capyieldcallback)
-   [**WM \_ CAP \_ SET \_ CALLBACK \_ CAPCONTROL**](wm-cap-set-callback-capcontrol.md)
-   [**WM \_ CAP SET CALLBACK ERROR (WM-CAP \_ \_ SET-RÜCKRUFFEHLER) \_**](wm-cap-set-callback-error.md)
-   [**WM \_ CAP \_ SET \_ CALLBACK \_ FRAME**](wm-cap-set-callback-frame.md)
-   [**WM \_ CAP \_ SET \_ CALLBACK \_ STATUS**](wm-cap-set-callback-status.md)
-   [**WM \_ CAP \_ SET \_ CALLBACK \_ VIDEOSTREAM**](wm-cap-set-callback-videostream.md)
-   [**WM \_ CAP \_ SET \_ CALLBACK \_ WAVESTREAM**](wm-cap-set-callback-wavestream.md)
-   [**WM \_ CAP \_ SET \_ CALLBACK \_ YIELD**](wm-cap-set-callback-yield.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Videoaufnahme](video-capture.md)
</dt> </dl>

 

 





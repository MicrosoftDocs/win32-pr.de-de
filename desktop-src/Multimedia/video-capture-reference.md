---
title: Video Aufzeichnungs Referenz
description: Video Aufzeichnungs Referenz
ms.assetid: 5356c575-2a59-4459-b4eb-76967deb6877
keywords:
- Video für Windows (Vfw), Video Aufzeichnungs Referenz
- VFW (Video für Windows), Video Aufzeichnungs Referenz
- Avicap, Referenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cef19834e244f6070a1d8bb3383dcac017e4d161
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036560"
---
# <a name="video-capture-reference"></a>Video Aufzeichnungs Referenz

In diesem Abschnitt werden die Funktionen, Strukturen, Meldungen und Makros beschrieben, die der avicap-Fenster Klasse zugeordnet sind. Diese Elemente werden wie folgt gruppiert.

## <a name="basic-capture-operations"></a>Grundlegende Erfassungs Vorgänge

-   [**capkreatecapturewindow**](/windows/desktop/api/Vfw/nf-vfw-capcreatecapturewindowa)
-   [**Abbruch der WM- \_ Obergrenze \_**](wm-cap-abort.md)
-   [**WM- \_ Cap- \_ Treiber \_ Verbindung**](wm-cap-driver-connect.md)
-   [**WM- \_ Cap- \_ Sequenz**](wm-cap-sequence.md)
-   [**WM- \_ Cap- \_ Ende**](wm-cap-stop.md)

## <a name="capture-windows"></a>Erfassungsfenster

-   [**Capstatus**](/windows/win32/api/vfw/ns-vfw-capstatus)
-   [**capgetdriverdescription**](/windows/desktop/api/Vfw/nf-vfw-capgetdriverdescriptiona)
-   [**WM- \_ Cap- \_ Treiber \_ Verbindung**](wm-cap-driver-connect.md)
-   [**WM- \_ Cap- \_ Treiber Verbindung \_ trennen**](wm-cap-driver-disconnect.md)
-   [**WM- \_ Cap- \_ \_ Status Get**](wm-cap-get-status.md)

## <a name="capture-drivers"></a>Erfassungs Treiber

-   [**Capdrivercaps**](/windows/win32/api/vfw/ns-vfw-capdrivercaps)
-   [**WM- \_ Cap- \_ Treiber \_ get \_ Caps**](wm-cap-driver-get-caps.md)
-   [**WM- \_ Cap- \_ Treiber get- \_ \_ Name**](wm-cap-driver-get-name.md)
-   [**WM- \_ Cap- \_ Treiber get- \_ \_ Version**](wm-cap-driver-get-version.md)
-   [**WM- \_ Cap \_ get \_ Audioformat**](wm-cap-get-audioformat.md)
-   [**WM- \_ Cap \_ get \_ Videoformat**](wm-cap-get-videoformat.md)
-   [**WM- \_ Cap- \_ Set \_ Audioformat**](wm-cap-set-audioformat.md)
-   [**WM- \_ Cap- \_ Set- \_ Videoformat**](wm-cap-set-videoformat.md)

## <a name="capture-driver-preview-and-overlay-modes"></a>Erfassungs Modus für Erfassungs Treiber

-   [**Überlagerung der WM- \_ Obergrenze \_ \_**](wm-cap-set-overlay.md)
-   [**WM- \_ Cap- \_ \_ Vorschau festlegen**](wm-cap-set-preview.md)
-   [**\_previewrate der WM-Obergrenze \_ \_**](wm-cap-set-previewrate.md)
-   [**WM- \_ Cap- \_ Set- \_ Skala**](wm-cap-set-scale.md)
-   [**Bild Lauf der WM- \_ Obergrenze \_ \_**](wm-cap-set-scroll.md)

## <a name="capture-driver-video-dialog-boxes"></a>Dialog Felder für das Erfassen von Treibern

-   [**WM \_ Cap \_ DLG- \_ Video Komprimierung**](wm-cap-dlg-videocompression.md)
-   [**WM- \_ Cap- \_ DLG- \_ Videodisplay**](wm-cap-dlg-videodisplay.md)
-   [**WM \_ Cap \_ DLG- \_ Videoformat**](wm-cap-dlg-videoformat.md)
-   [**WM \_ Cap \_ DLG- \_ videosource**](wm-cap-dlg-videosource.md)

## <a name="audio-format"></a>Audioformat

-   [**WM- \_ Cap \_ get \_ Audioformat**](wm-cap-get-audioformat.md)
-   [**WM- \_ Cap- \_ Set \_ Audioformat**](wm-cap-set-audioformat.md)

## <a name="video-capture-settings"></a>Video Erfassungs Einstellungen

-   [**Captureparms**](/windows/win32/api/vfw/ns-vfw-captureparms)
-   [**WM- \_ Cap- \_ \_ Setup Get Sequence \_ Setup**](wm-cap-get-sequence-setup.md)
-   [**Setup für die WM- \_ Cap- \_ Einrichtung \_ \_**](wm-cap-set-sequence-setup.md)

## <a name="capture-file-and-buffers"></a>Erfassungs Datei und Puffer

-   [**Captureparms**](/windows/win32/api/vfw/ns-vfw-captureparms)
-   [**WM- \_ Cap- \_ Datei \_ zuordnen**](wm-cap-file-allocate.md)
-   [**WM- \_ Cap- \_ Datei get- \_ \_ Erfassungs \_ Datei**](wm-cap-file-get-capture-file.md)
-   [**WM- \_ Cap- \_ Datei ( \_ SaveAs)**](wm-cap-file-saveas.md)
-   [**\_ \_ Datei Satz- \_ \_ Erfassungs \_ Datei für WM-Cap**](wm-cap-file-set-capture-file.md)

## <a name="directly-using-capture-data"></a>Direkte Verwendung von Erfassungsdaten

-   [**WM- \_ Abdeckungs \_ Sequenz- \_ NoFile**](wm-cap-sequence-nofile.md)

## <a name="capture-from-mci-device"></a>Erfassung vom MCI-Gerät

-   [**WM- \_ Cap- \_ festgelegte \_ MCI- \_ Gerät**](wm-cap-set-mci-device.md)

## <a name="manual-frame-capture"></a>Manuelle Frame Erfassung

-   [**WM- \_ Cap- \_ Einzel \_ Rahmen**](wm-cap-single-frame.md)
-   [**WM- \_ Cap- \_ Einzel \_ Rahmen \_ Schließen**](wm-cap-single-frame-close.md)
-   [**WM- \_ Cap- \_ Einzel \_ Rahmen \_ geöffnet**](wm-cap-single-frame-open.md)

## <a name="still-image-capture"></a>Still-Image Erfassung

-   [**\_ \_ Bearbeitungs \_ Kopie der WM-Abdeckung**](wm-cap-edit-copy.md)
-   [**WM- \_ Cap- \_ Datei ( \_ savedib)**](wm-cap-file-savedib.md)
-   [**WM- \_ Abdeckungs \_ \_ Rahmen**](wm-cap-grab-frame.md)
-   [**WM- \_ Obergrenze für Abdeckungs \_ \_ Rahmen \_ nostopps**](wm-cap-grab-frame-nostop.md)

## <a name="advanced-capture-options"></a>Erweiterte Aufzeichnungs Optionen

-   [**WM- \_ Cap- \_ Datei \_ Satz \_ Infoblock**](wm-cap-file-set-infochunk.md)
-   [**WM- \_ Cap- \_ \_ Benutzer \_ Daten erhalten**](wm-cap-get-user-data.md)
-   [**WM- \_ Cap- \_ \_ Benutzer \_ Daten festlegen**](wm-cap-set-user-data.md)

## <a name="working-with-palettes"></a>Arbeiten mit Paletten

-   [**\_ \_ Bearbeitungs \_ Kopie der WM-Abdeckung**](wm-cap-edit-copy.md)
-   [**WM \_ Cap \_ PAL \_ AutoCreate**](wm-cap-pal-autocreate.md)
-   [**WM \_ Cap \_ PAL \_ manualcreate**](wm-cap-pal-manualcreate.md)
-   [**WM- \_ Cap- \_ PAL \_ geöffnet**](wm-cap-pal-open.md)
-   [**WM- \_ Cap- \_ PAL \_ Einfügen**](wm-cap-pal-paste.md)
-   [**WM- \_ Cap- \_ PAL \_ Speichern**](wm-cap-pal-save.md)

## <a name="yielding-to-other-applications"></a>Bereitzustellen an andere Anwendungen

-   [**WM- \_ Cap- \_ \_ Setup Get Sequence \_ Setup**](wm-cap-get-sequence-setup.md)
-   [**\_ \_ \_ Rückruf \_ Rendite für WM-Cap-Satz**](wm-cap-set-callback-yield.md)
-   [**Setup für die WM- \_ Cap- \_ Einrichtung \_ \_**](wm-cap-set-sequence-setup.md)

## <a name="avicap-callback-functions"></a>Avicap-Rückruf Funktionen

-   [**capcontrolcallback**](/windows/desktop/api/Vfw/nc-vfw-capcontrolcallback)
-   [**caperrorcallback**](/windows/desktop/api/Vfw/nc-vfw-caperrorcallbacka)
-   [**capstatus-Rückruf**](/windows/desktop/api/Vfw/nc-vfw-capstatuscallbacka)
-   [**capvideostreamcallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback)
-   [**capwavestreamcallback**](/windows/desktop/api/Vfw/nc-vfw-capwavecallback)
-   [**capyieldcallback**](/windows/desktop/api/Vfw/nc-vfw-capyieldcallback)
-   [**WM- \_ Cap- \_ Satz Rückruf ( \_ \_ capcontrol)**](wm-cap-set-callback-capcontrol.md)
-   [**Rückruf Fehler bei WM-Abdeckung \_ \_ festgelegt \_ \_**](wm-cap-set-callback-error.md)
-   [**\_ \_ \_ Rückruf \_ Rahmen für WM-Cap-Satz**](wm-cap-set-callback-frame.md)
-   [**Rückruf Status der WM- \_ Obergrenze \_ festlegen \_ \_**](wm-cap-set-callback-status.md)
-   [**WM- \_ Abdeckungs \_ Satz \_ Rückruf \_ Videostream**](wm-cap-set-callback-videostream.md)
-   [**WM- \_ Cap- \_ Satz \_ Rückruf \_ WaveStream**](wm-cap-set-callback-wavestream.md)
-   [**\_ \_ \_ Rückruf \_ Rendite für WM-Cap-Satz**](wm-cap-set-callback-yield.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Video Erfassung](video-capture.md)
</dt> </dl>

 

 





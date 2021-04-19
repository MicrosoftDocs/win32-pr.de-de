---
title: Arbeiten mit Paletten
description: Arbeiten mit Paletten
ms.assetid: 0ad0d78b-4c2c-499c-ad5e-8324b59e89fc
keywords:
- WM_CAP_PAL_PASTE Meldung
- cappalettepaste-Makro
- WM_CAP_PAL_OPEN Meldung
- cappaletteopen-Makro
- WM_CAP_PAL_AUTOCREATE Meldung
- cappaletteauto-Makro
- WM_CAP_PAL_MANUALCREATE Meldung
- cappalettemanual-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f09cbbe3ffc8ea21d1ecf8545f036f5ba6dfb927
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341837"
---
# <a name="working-with-palettes"></a>Arbeiten mit Paletten

Wenn das Video Erfassungs Format eine Palette erfordert, verwendet das Erfassungsfenster zunächst die vom Erfassungs Treiber bereitgestellte Palette. Diese Palette kann aus Graustufen Werten für die schwarze und weiße Reproduktion oder eine breite Auswahl von Farbwerten bestehen. Sie können eine vorhandene Palette abrufen, um die Standardpalette zu ersetzen, indem Sie die " [**WM \_ Cap \_ PAL \_ Paste**](wm-cap-pal-paste.md) "-oder " [**WM \_ Cap \_ PAL \_ Open**](wm-cap-pal-open.md) "-Nachricht (oder das-Makro [**cappalettepaste**](/windows/desktop/api/Vfw/nf-vfw-cappalettepaste) oder [**cappaletteopen**](/windows/desktop/api/Vfw/nf-vfw-cappaletteopen) ) verwenden. Alternativ können Sie eine benutzerdefinierte Palette erstellen, um die Standardpalette zu ersetzen, indem Sie die " [**WM \_ Cap \_ PAL \_ AutoCreate**](wm-cap-pal-autocreate.md) "-oder " [**WM \_ Cap \_ PAL \_ manualcreate**](wm-cap-pal-manualcreate.md) "-Nachricht (oder das-Makro [**cappaletteauto**](/windows/desktop/api/Vfw/nf-vfw-cappaletteauto) oder [**cappalettemanual**](/windows/desktop/api/Vfw/nf-vfw-cappalettemanual) ) verwenden. Nachdem Sie die Standardpalette ersetzt haben, verwenden Sie das Erfassungsfenster und den Treiber, bis Sie eine andere Palette erstellen oder öffnen.

Die \_ Meldung WM Cap \_ PAL \_ AutoCreate oder WM \_ Cap \_ PAL \_ manualcreate erstellt basierend auf der aktuellen Videoeingabe eine optimierte Palette. Diese benutzerdefinierte Palette gibt einer Videosequenz die beste Farb Treue, da Sie auf Farben basiert, die in der Sequenz vorhanden sind. Das Erfassungsfenster erstellt ein dreidimensionales Histogramm der Farben, die es erstellt. Dadurch wird die Anzahl der Farben reduziert, indem der absolute Fehler zwischen benachbarten Farben untersucht und die Werte mit dem kleinsten Fehlerwert konsolidiert werden.

Beim Senden \_ von WM Cap \_ PAL \_ AutoCreate müssen Sie die Anzahl der Frames für das Beispiel avicap angeben und die Größe der Farbpalette angeben. Wenn Sie die Anzahl der Frames angeben, schließen Sie genügend Frames ein, um sicherzustellen, dass alle Farben in der Sequenz Stichproben sind.

Sie können den aktuellen Frame mithilfe von WM \_ Cap \_ PAL \_ manualcreate testen. Wenn Sie diese Meldung mit mehreren manuell ausgewählten Frames verwenden, können Sie eine Palette erstellen, die die Farben enthält, die in der Palette angezeigt werden sollen.

Eine Palette kann bis zu 256 Farben enthalten. Wenn Sie Paletten zusammenführen oder die Videosequenz gleichzeitig mit anderen Videos oder Bildern angezeigt werden soll, sollten Sie eine kleinere Farbauswahl verwenden, damit Farben aus den einzelnen Bild-oder Videoclips nebeneinander vorhanden sein können.

Sie speichern eine neue Palette mithilfe der " [**WM \_ Cap \_ PAL \_ Save**](wm-cap-pal-save.md) "-Nachricht (oder dem " [**cappalettesave**](/windows/desktop/api/Vfw/nf-vfw-cappalettesave) "-Makro) und rufen Sie später mithilfe der " [**WM \_ Cap \_ PAL \_ Open**](wm-cap-pal-open.md) "-Meldung ab. Sie können eine Palette für die Nachbearbeitung der Palette oder für die Verwendung in einer anderen Anwendung speichern.

Sie können eine Palette aus der Zwischenablage in das Aufzeichnungs Fenster einfügen, indem Sie die " [**WM \_ Cap \_ PAL- \_ Einfüge**](wm-cap-pal-paste.md) Nachricht" verwenden. Das Erfassungsfenster übergibt die Palette an den Erfassungs Treiber. Andere Anwendungen können Paletten in die Zwischenablage kopieren. Sie können auch eine Palette in die Zwischenablage kopieren, indem Sie die Meldung zum [**\_ \_ Bearbeiten \_ der WM**](wm-cap-edit-copy.md) -Abdeckung (oder das [**capeditcopy**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy) -Makro) verwenden. In dieser Meldung wird der Video Frame Puffer einschließlich der Palette in die Zwischenablage kopiert.

 

 





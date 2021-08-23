---
title: Arbeiten mit Paletten
description: Arbeiten mit Paletten
ms.assetid: 0ad0d78b-4c2c-499c-ad5e-8324b59e89fc
keywords:
- WM_CAP_PAL_PASTE-Nachricht
- capPalettePaste-Makro
- WM_CAP_PAL_OPEN-Nachricht
- capPaletteOpen-Makro
- WM_CAP_PAL_AUTOCREATE-Nachricht
- capPaletteAuto-Makro
- WM_CAP_PAL_MANUALCREATE-Nachricht
- capPaletteManual-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51f9399520b5a3cefc046959c0d59d7abe9d0f1b6ab19662f750720afd16447
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119686710"
---
# <a name="working-with-palettes"></a>Arbeiten mit Paletten

Wenn für das Videoaufnahmeformat zunächst eine Palette erforderlich ist, verwendet das Erfassungsfenster die vom Erfassungstreiber bereitgestellte Palette. Diese Palette kann aus grauen Werten für die Schwarz-Weiß-Reproduktion oder einer breiten Auswahl von Farbwerten bestehen. Sie können eine vorhandene Palette abrufen, um die Standardpalette zu ersetzen, indem Sie die [**WM \_ CAP PAL \_ \_ PASTE-**](wm-cap-pal-paste.md) oder [**WM CAP PAL \_ \_ \_ OPEN-Meldung**](wm-cap-pal-open.md) (oder das [**Makro capPalettePaste**](/windows/desktop/api/Vfw/nf-vfw-cappalettepaste) oder [**capPaletteOpen)**](/windows/desktop/api/Vfw/nf-vfw-cappaletteopen) verwenden. Alternativ können Sie eine benutzerdefinierte Palette erstellen, um die Standardpalette zu ersetzen, indem Sie die [**MELDUNG WM CAP PAL \_ \_ \_ AUTOCREATE**](wm-cap-pal-autocreate.md) oder [**WM CAP PAL \_ \_ \_ MANUALCREATE**](wm-cap-pal-manualcreate.md) (oder das [**Makro capPaletteAuto**](/windows/desktop/api/Vfw/nf-vfw-cappaletteauto) oder [**capPaletteManual)**](/windows/desktop/api/Vfw/nf-vfw-cappalettemanual) verwenden. Nachdem Sie die Standardpalette ersetzt haben, verwenden das Erfassungsfenster und der Treiber die Ersetzungspalette, bis Sie eine andere Palette erstellen oder öffnen.

Die MELDUNG WM \_ CAP \_ PAL \_ AUTOCREATE oder WM \_ CAP PAL \_ \_ MANUALCREATE erstellt basierend auf der aktuellen Videoeingabe eine optimierte Palette. Diese benutzerdefinierte Palette bietet einer Videosequenz die beste Farbgenauigkeit, da sie auf Farben basiert, die in der Sequenz vorhanden sind. Das Erfassungsfenster erstellt ein dreidimensionales Histogramm der Farben, die es abzeichen. Sie reduziert die Anzahl der Farben, indem der absolute Fehler zwischen angrenzenden Farben untersucht und mit dem kleinsten Fehlerwert konsolidiert wird.

Beim Senden von WM CAP PAL AUTOCREATE müssen Sie die Anzahl der Frames für DIE STICHPROBEN-Kapsel und die Größe der \_ \_ \_ Farbpalette angeben. Wenn Sie die Anzahl der Frames angeben, schließen Sie genügend Frames ein, um sicherzustellen, dass alle Farben in der Sequenz entnommen werden.

Sie können den aktuellen Frame mithilfe von WM \_ CAP \_ PAL \_ MANUALCREATE als Beispiel verwenden. Wenn Sie diese Meldung mit mehreren manuell ausgewählten Frames verwenden, können Sie eine Palette erstellen, die die Farben enthält, die in der Palette angezeigt werden sollen.

Eine Palette kann bis zu 256 Farben enthalten. Wenn Sie Paletten zusammenführen oder die Videosequenz gleichzeitig mit anderen Videos oder Bildern angezeigt werden soll, sollten Sie eine kleinere Farbauswahl verwenden, damit Farben aus jedem Bild oder Videoclip gleichzeitig verwendet werden können.

Sie speichern eine neue Palette mithilfe der [**WM \_ CAP PAL \_ \_ SAVE-Meldung**](wm-cap-pal-save.md) (oder des [**Makros capPaletteSave)**](/windows/desktop/api/Vfw/nf-vfw-cappalettesave) und rufen sie später mithilfe der [**WM CAP PAL \_ \_ \_ OPEN-Meldung**](wm-cap-pal-open.md) ab. Sie können eine Palette für die Nachbearbeitung der Palette oder für die Verwendung in einer anderen Anwendung speichern.

Sie können eine Palette aus der Zwischenablage in das Erfassungsfenster einfügen, indem Sie die [**WM \_ CAP PAL \_ \_ PASTE-Meldung**](wm-cap-pal-paste.md) verwenden. Das Erfassungsfenster übergibt die Palette an den Erfassungstreiber. Andere Anwendungen können Paletten in die Zwischenablage kopieren. Sie können eine Palette auch in die Zwischenablage kopieren, indem Sie die [**WM \_ CAP EDIT \_ \_ COPY-Meldung**](wm-cap-edit-copy.md) (oder das [**Makro capEditCopy)**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy) verwenden. Diese Meldung kopiert den Videoframepuffer einschließlich der Palette in die Zwischenablage.

 

 





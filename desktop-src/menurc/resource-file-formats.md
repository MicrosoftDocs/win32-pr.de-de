---
title: Ressourcendateiformate
description: In diesem Abschnitt wird das Format der binären Ressourcendatei beschrieben, die der Ressourcencompiler basierend auf dem Inhalt der Ressourcendefinitionsdatei erstellt.
ms.assetid: a0b17555-f50a-4d58-b2bc-760843dd67eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16bfc85190993992b7bf87001f3d807b777ed2fe27b4d66cba0b7f7c948d8cfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117869791"
---
# <a name="resource-file-formats"></a>Ressourcendateiformate

In diesem Abschnitt wird das Format der binären Ressourcendatei beschrieben, die der Ressourcencompiler basierend auf dem Inhalt der Ressourcendefinitionsdatei erstellt. Diese Datei hat in der Regel die Erweiterung .res. Der Linker neu erstellt die RES-Datei in eine Ressourcenobjektdatei und verknüpft sie dann mit der ausführbaren Datei einer Anwendung.

Eine binäre Ressourcendatei besteht aus einer Reihe verketteter Ressourceneinträge. Jeder Eintrag besteht aus einem Ressourcenheader und den Daten für diese Ressource. Ein Ressourcenheader ist in der Datei **DWORD** ausgerichtet und besteht aus folgendem Code:

-   Ein **DWORD,** das die Größe des Ressourcenheaders enthält
-   Ein **DWORD,** das die Größe der Ressourcendaten enthält
-   Der Ressourcentyp
-   Der Ressourcenname
-   Zusätzliche Ressourceninformationen

Die [**RESOURCEHEADER-Struktur**](resourceheader.md) beschreibt das Format dieses Headers. Die Daten für die Ressource folgen dem Ressourcenheader und sind für jeden Ressourcentyp spezifisch. Einige Ressourcen verwenden auch eine ressourcenspezifische Gruppenheaderstruktur, um Informationen zu einer Gruppe von Ressourcen zur Verfügung zu stellen.

## <a name="accelerator-table-resources"></a>Zugriffstastentabellenressourcen

Eine Zugriffstastentabelle ist ein Ressourceneintrag in einer Ressourcendatei. Sie verfügt nicht über einen Gruppenheader. Eine [**ACCELTABLEENTRY-Struktur**](acceltableentry.md) beschreibt jeden Eintrag in der Zugriffstastentabelle. Mehrere Zugriffstastentabellen sind zulässig.

## <a name="cursor-and-icon-resources"></a>Cursor- und Symbolressourcen

Das System behandelt jedes Symbol und jeden Cursor als einzelne Datei. Diese werden jedoch in RES-Dateien und ausführbaren Dateien als Gruppe von Symbolressourcen oder als Gruppe von Cursorressourcen gespeichert. Die Dateiformate von Symbol- und Cursorressourcen sind ähnlich. In der RES-Datei folgt ein Ressourcengruppenheader allen einzelnen Symbol- oder Cursorgruppenkomponenten.

Das Format der einzelnen Symbolkomponenten ähnelt dem Format der ICO-Datei. Jedes Symbolbild wird in einer [**BITMAPINFO-Struktur**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) gespeichert, gefolgt von den farblich geräteunabhängigen Bitmapbits (DIB) der **XOR-Maske** des Symbols. Die monofarbigen DIB-Bits der  AND-Maske des Symbols folgen den DIB-Farbbits.

Das Format jeder Cursorkomponente ähnelt dem Format der CUR-Datei. Jedes Cursorbild wird in einer [**BITMAPINFO-Struktur**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) gespeichert, gefolgt von den monofarbigen DIB-Bits der **XOR-Maske** des Cursors und dann von den monotonen DIB-Bits der **AND-Maske** des Cursors. Beachten Sie, dass es einen Unterschied in den Bitmaps der beiden Ressourcen gibt: Im Gegensatz zu Symbolen weisen Cursor-XOR-Masken keine Farb-DIB-Bits auf. Obwohl die Bitmaps der Cursormasken monofarbig sind und keine DIB-Header oder Farbtabellen haben, befinden sich die Bits in Bezug auf Ausrichtung und Richtung weiterhin im DIB-Format. Ein weiterer signifikanter Unterschied zwischen Cursorn und Symbolen ist, dass Cursor einen Hotspot haben und Symbole dies nicht tun.

Der Gruppenheader für Symbol- und Cursorressourcen besteht aus einer [**NEWHEADER-Struktur**](newheader.md) sowie einer oder mehreren [**RESDIR-Strukturen.**](resdir.md) Es gibt eine **RESDIR-Struktur** für jedes Symbol oder jeden Cursor. Der Gruppenheader enthält die Informationen, die eine Anwendung benötigt, um das richtige Symbol oder den richtigen Cursor für die Anzeige auszuwählen. Sowohl der Gruppenkopf als auch die Daten, die für jedes Symbol oder jeden Cursor in der Gruppe wiederholt werden, haben eine feste Länge. Dadurch kann die Anwendung nach dem Zufallsprinzip auf die Informationen zugreifen.

## <a name="dialog-box-resources"></a>Dialogfeldressourcen

Ein Dialogfeld ist auch ein Ressourceneintrag in der Ressourcendatei. Sie besteht aus einer [**DLGTEMPLATE-Dialogfeldheaderstruktur**](/windows/desktop/api/winuser/ns-winuser-dlgtemplate) sowie einer [**DLGITEMTEMPLATE-Struktur**](/windows/desktop/api/winuser/ns-winuser-dlgitemtemplate) für jedes Steuerelement im Dialogfeld. Die [**DLGTEMPLATEEX-**](/windows/desktop/dlgbox/dlgtemplateex) und [**DLGITEMTEMPLATEEX-Strukturen**](/windows/desktop/dlgbox/dlgitemtemplateex) beschreiben das Format erweiterter Dialogfeldressourcen.

## <a name="font-resources"></a>Schriftarten Ressourcen

Schriftarten werden in der Ressourcendatei als Gruppe von Ressourcen gespeichert. Einzelne Schriftarten machen eine Schriftartgruppe aus. Eine FONT Statement-Ressourcendefinitions-Anweisung in der . [](./font-statement.md) Die RC-Datei definiert jede Schriftart. Jede einzelne Schriftart in der Ressource besteht aus dem vollständigen Inhalt der zugehörigen FNT-Datei. Eine [**FONTGROUPHDR-Struktur**](fontgrouphdr.md) folgt allen einzelnen Schriftartkomponenten in der RES-Datei.

Schriftartressourcen werden den Ressourcen einer bestimmten Anwendung nicht hinzugefügt. Stattdessen werden sie normalerweise ausführbaren Dateien mit der Erweiterung .fon hinzugefügt. Bei diesen Dateien handelt es sich in der Regel nicht um Anwendungen, sondern um ressourcenbasierte DLLs.

## <a name="menu-resources"></a>Menüressourcen

Eine *Menüressource* besteht aus einer [**MENUHEADER-Struktur,**](menuheader.md) gefolgt von einer oder mehreren [**NORMALMENUITEM-**](normalmenuitem.md) oder [**POPUPMENUITEM-Strukturen,**](popupmenuitem.md) eine für jedes Menüelement in der Menüvorlage. Die [**MENUEX \_ TEMPLATE \_ HEADER-**](menuex-template-header.md) und [**MENUEX TEMPLATE \_ \_ ITEM-Strukturen**](menuex-template-item.md) beschreiben das Format erweiterter Menüressourcen.

## <a name="message-table-resources"></a>Nachrichtentabellenressourcen

Eine *Meldungstabelle* ist eine Ressource, die formatierten Text für die Anzeige als Fehlermeldung oder in einem Meldungsfeld enthält. Die Hauptstruktur in einer Nachrichtentabellenressource ist die [**MESSAGE \_ RESOURCE \_ DATA-Struktur.**](/windows/desktop/api/Winnt/ns-winnt-message_resource_data)

## <a name="version-resources"></a>Versionsressourcen

Die Hauptstruktur in einer Versionsressource ist die [**VS \_ FIXEDFILEINFO-Struktur.**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) Weitere Strukturen sind die [**VarFileInfo-Struktur**](varfileinfo.md) zum Speichern von Sprachinformationsdaten und [**StringFileInfo**](stringfileinfo.md) für benutzerdefinierte Zeichenfolgeninformationen. Alle Zeichenfolgen in einer Versionsressource haben das Unicode-Format. Jeder Informationsblock wird an einer **DWORD-Grenze** ausgerichtet.

 

 
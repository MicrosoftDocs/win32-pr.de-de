---
title: Ressourcen Dateiformate
description: In diesem Abschnitt wird das Format der binären Ressourcen Datei beschrieben, die vom Ressourcen Compiler basierend auf dem Inhalt der Ressourcen Definitionsdatei erstellt wird.
ms.assetid: a0b17555-f50a-4d58-b2bc-760843dd67eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b90c789cd1684c1f5ca31af0e2d60a31052ca03f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858243"
---
# <a name="resource-file-formats"></a>Ressourcen Dateiformate

In diesem Abschnitt wird das Format der binären Ressourcen Datei beschrieben, die vom Ressourcen Compiler basierend auf dem Inhalt der Ressourcen Definitionsdatei erstellt wird. Diese Datei weist in der Regel die Erweiterung ". res" auf. Der Linker formatiert die res-Datei in eine Ressourcen Objektdatei und verknüpft Sie dann mit der ausführbaren Datei einer Anwendung.

Eine binäre Ressourcen Datei besteht aus einer Reihe von verketteten Ressourcen Einträgen. Jeder Eintrag besteht aus einem Ressourcen Header und den Daten für diese Ressource. Ein Ressourcen Header ist in der Datei **DWORD**-ausgerichtet und besteht aus folgendem:

-   Ein **DWORD** , das die Größe des Ressourcen Headers enthält.
-   Ein **DWORD** , das die Größe der Ressourcen Daten enthält.
-   Der Ressourcentyp
-   Der Ressourcen Name
-   Zusätzliche Ressourcen Informationen

Die [**resourceheader**](resourceheader.md) -Struktur beschreibt das Format dieses Headers. Die Daten für die Ressource folgen dem Ressourcen Header und sind für jeden Ressourcentyp spezifisch. Einige Ressourcen verwenden auch eine Ressourcen spezifische Gruppen Header Struktur, um Informationen über eine Gruppe von Ressourcen bereitzustellen.

## <a name="accelerator-table-resources"></a>Zugriffstasten Tabellen-Ressourcen

Eine Zugriffstasten Tabelle ist ein Ressourcen Eintrag in einer Ressourcen Datei. Er verfügt über keinen Gruppenkopf. Eine [**acceltableentry**](acceltableentry.md) -Struktur beschreibt jeden Eintrag in der Zugriffstasten Tabelle. Mehrere Zugriffstasten Tabellen sind zulässig.

## <a name="cursor-and-icon-resources"></a>Cursor-und Symbol Ressourcen

Das System behandelt die einzelnen Symbole und Cursor als einzelne Datei. Diese werden jedoch in. res-Dateien und ausführbaren Dateien als Gruppe von Symbol Ressourcen oder einer Gruppe von Cursor Ressourcen gespeichert. Die Dateiformate von Symbol-und Cursor Ressourcen sind ähnlich. In der. res-Datei folgt eine Ressourcengruppen Kopfzeile allen einzelnen Symbol-oder Cursor Gruppen Komponenten.

Das Format jeder Symbol Komponente ähnelt dem Format der ICO-Datei. Jedes Symbolbild wird in einer [**BitmapInfo**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) -Struktur gefolgt von der Farbe geräteunabhängige Bitmap (DIB)-Bits der **Xor** -Maske des Symbols gespeichert. Die monochrome DIB-Bits des Symbols **und** der Maske folgen den farbdib-Bits.

Das Format jeder Cursor Komponente ähnelt dem Format der CUR-Datei. Jedes Cursor Bild wird in einer [**BitmapInfo**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) -Struktur gespeichert, gefolgt von den monochrome DIB-Bits der **Xor** -Maske des Cursors und dann von den monochrome DIB-Bits der Cursor- **und** -Maske. Beachten Sie, dass es einen Unterschied in den Bitmaps der beiden Ressourcen gibt: im Unterschied zu Symbolen haben Cursor-XOR-Masken keine farbdib-Bits. Obwohl die Bitmaps der Cursor Masken monochrome sind und keine DIB-Header oder Farbtabellen aufweisen, sind die Bits in Bezug auf Ausrichtung und Richtung immer noch im DIB-Format. Ein weiterer bedeutender Unterschied zwischen Cursorn und Symbolen besteht darin, dass Cursor über einen Hotspot verfügen und Symbole nicht.

Die Gruppen Kopfzeile für die Symbol-und die Cursor-Ressource besteht aus einer [**nwheader**](newheader.md) -Struktur und einer oder mehreren [**resdir**](resdir.md) -Strukturen. Es gibt eine **resdir** -Struktur für jedes Symbol oder jeden Cursor. Die Gruppen Kopfzeile enthält die Informationen, die eine Anwendung benötigt, um das richtige Symbol oder den anzuzeigenden Cursor auszuwählen. Sowohl die Gruppen Kopfzeile als auch die Daten, die für jedes Symbol oder jeder Cursor in der Gruppe wiederholt werden, haben eine festgelegte Länge. Dadurch kann die Anwendung nach dem Zufallsprinzip auf die Informationen zugreifen.

## <a name="dialog-box-resources"></a>Dialog Feld Ressourcen

Ein Dialogfeld ist auch ein Ressourcen Eintrag in der Ressourcen Datei. Sie besteht aus einer [**DLGTEMPLATE**](/windows/desktop/api/winuser/ns-winuser-dlgtemplate) -Dialogfeld-Header Struktur und einer [**DLGITEMTEMPLATE**](/windows/desktop/api/winuser/ns-winuser-dlgitemtemplate) -Struktur für jedes Steuerelement im Dialogfeld. Die Strukturen [**dlgtemplateex**](/windows/desktop/dlgbox/dlgtemplateex) und [**dlgitemtemplateex**](/windows/desktop/dlgbox/dlgitemtemplateex) beschreiben das Format erweiterter Dialogfeld Ressourcen.

## <a name="font-resources"></a>Schriftarten Ressourcen

Schriftarten werden in der Ressourcen Datei als Gruppe von Ressourcen gespeichert. Einzelne Schriftarten bilden eine Schriftart Gruppe. Eine [Schriftart Anweisung](./font-statement.md) Ressourcen Definitions Anweisung in. In der RC-Datei wird jede Schriftart definiert. Jede einzelne Schriftart in der Ressource besteht aus dem gesamten Inhalt der zugehörigen. file-Datei. Eine [**fontgrouphdr**](fontgrouphdr.md) -Struktur folgt allen einzelnen Schriftart Komponenten in der RES-Datei.

Den Ressourcen einer bestimmten Anwendung werden keine Schriftart Ressourcen hinzugefügt. Stattdessen werden Sie normalerweise ausführbaren Dateien hinzugefügt, die über die Erweiterung ". FON" verfügen. Diese Dateien sind in der Regel reine Ressourcen-DLLs anstelle von Anwendungen.

## <a name="menu-resources"></a>Menü Ressourcen

Eine *Menü Ressource* besteht aus einer [**menuheader**](menuheader.md) -Struktur, gefolgt von einer oder mehreren [**normmenuitem**](normalmenuitem.md) -oder [**popupmenuitem**](popupmenuitem.md) -Strukturen, eine für jedes Menü Element in der Menüvorlage. Der [**menuex- \_ Vorlagen \_ Header**](menuex-template-header.md) und die [**menuex- \_ Vorlagen \_ Element**](menuex-template-item.md) Strukturen beschreiben das Format erweiterter Menü Ressourcen.

## <a name="message-table-resources"></a>Nachrichten Tabellen Ressourcen

Eine *Nachrichten Tabelle* ist eine Ressource, die formatierten Text enthält, der als Fehlermeldung oder in einem Meldungs Feld angezeigt werden soll. Die Hauptstruktur in einer Nachrichten Tabellen Ressource ist die [**\_ \_ Datenstruktur der Nachrichten Ressource**](/windows/desktop/api/Winnt/ns-winnt-message_resource_data) .

## <a name="version-resources"></a>Versions Ressourcen

Die Hauptstruktur in einer Versions Ressource ist die [**vs \_ fixedfileingefo**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) -Struktur. Zu den zusätzlichen Strukturen gehören die [**varfileinfo**](varfileinfo.md) -Struktur zum Speichern von sprach Informationsdaten und [**stringfileinfo**](stringfileinfo.md) für benutzerdefinierte Zeichen folgen Informationen. Alle Zeichen folgen in einer Versions Ressource sind im Unicode-Format. Jeder Informationsblock wird an einer **DWORD** -Grenze ausgerichtet.

 

 
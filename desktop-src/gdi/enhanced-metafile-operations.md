---
description: 'Sie können das Handle für eine erweiterte Metadatei verwenden, um die folgenden Aufgaben auszuführen:'
ms.assetid: 8f887c38-6cfa-4918-aa44-dd5fb837b40b
title: Erweiterte metadateivorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18ba9e2ac2f14c4436c039a66cc3211b471c0461
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130780"
---
# <a name="enhanced-metafile-operations"></a>Erweiterte metadateivorgänge

Sie können das Handle für eine erweiterte Metadatei verwenden, um die folgenden Aufgaben auszuführen:

-   Zeigt das in einer erweiterten Metadatei gespeicherte Bild an.
-   Erstellen Sie Kopien einer erweiterten Metadatei.
-   Bearbeiten Sie eine erweiterte Metadatendatei.
-   Rufen Sie die optionale Beschreibung ab, die in einer erweiterten Metadatei gespeichert ist.
-   Rufen Sie eine Kopie eines Enhanced-Metafile-Headers ab.
-   Rufen Sie eine binäre Version einer erweiterten Metadatei ab.
-   Listet die Farben in der optionalen Palette auf.

Diese Aufgaben werden in den Abschnitten im weiteren Verlauf dieses Themas erläutert.

## <a name="display-the-picture-stored-in-an-enhanced-metafile"></a>Anzeigen des in einer erweiterten Metadatei gespeicherten Bilds

Mithilfe der Funktion [**playenhmetafile**](/windows/desktop/api/Wingdi/nf-wingdi-playenhmetafile) können Sie das Bild anzeigen, das in einer erweiterten Metadatei gespeichert ist. Übergeben Sie der Funktion ein Handle an die erweiterte Metadatendatei, ohne dass Sie sich mit dem Format der erweiterten metadateieinträge beschäftigen müssen. Manchmal ist es jedoch wünschenswert, die Datensätze in der erweiterten Metadatei aufzuzählen, um nach einer bestimmten GDI-Funktion zu suchen und die Parameter der Funktion in irgendeiner Weise zu ändern. Zu diesem Zweck können Sie " [**enumenhmetafile**](/windows/desktop/api/Wingdi/nf-wingdi-enumenhmetafile) " verwenden und eine Rückruffunktion " [**enhmetafileproc**](/windows/win32/api/wingdi/nc-wingdi-enhmfenumproc)" bereitstellen, um die erweiterten Metadatei-Datensätze zu verarbeiten. Um die Parameter für einen erweiterten Metadateidatensatz zu ändern, müssen Sie das Format der Parameter im Datensatz kennen.

## <a name="create-copies-of-an-enhanced-metafile"></a>Erstellen von Kopien einer erweiterten Metadatei

Einige Anwendungen erstellen temporäre Sicherungskopien (oder Duplikate) einer Datei, bevor Sie dem Benutzer die Möglichkeit geben, das Original zu ändern. Eine Anwendung kann eine Sicherungskopie einer erweiterten Metadatei erstellen, indem Sie die [**copyenhmetafile**](/windows/desktop/api/Wingdi/nf-wingdi-copyenhmetafilea) -Funktion aufrufen und ein Handle bereitstellt, das die erweiterte Metadatei identifiziert, und einen Zeiger auf den Namen der neuen Datei bereitstellt.

Rufen Sie zum Erstellen einer Speicher basierten Metadatei mit erweitertem Format die [**SetEnhMetaFileBits**](/windows/desktop/api/Wingdi/nf-wingdi-setenhmetafilebits) -Funktion auf.

## <a name="edit-an-enhanced-metafile"></a>Bearbeiten einer erweiterten Metadatei

Die meisten Zeichnungs-, Illustrations-und computergestützten Entwurfs Anwendungen (CAD) erfordern eine Methode zum Bearbeiten eines Bilds, das in einer erweiterten Metadatei gespeichert ist. Obwohl das Bearbeiten einer erweiterten Metadatei eine komplexe Aufgabe ist, können Sie die [**enumenhmetafile**](/windows/desktop/api/Wingdi/nf-wingdi-enumenhmetafile) -Funktion in Kombination mit anderen Funktionen verwenden, um diese Funktion in der Anwendung bereitzustellen. Mit der **enumenhmetafile** -Funktion und der zugehörigen Rückruffunktion " [**enhmetafileproc**](/windows/win32/api/wingdi/nc-wingdi-enhmfenumproc)" kann die Anwendung einzelne Datensätze in einer erweiterten Metadatei verarbeiten.

## <a name="retrieve-the-optional-description-stored-in-an-enhanced-metafile"></a>Abrufen der optionalen Beschreibung, die in einer erweiterten Metadatei gespeichert ist

Einige Anwendungen zeigen die Textbeschreibung einer erweiterten Metadatei mit dem entsprechenden Dateinamen im Dialogfeld **Öffnen** an. Sie können bestimmen, ob diese Zeichenfolge in einer erweiterten Metadatei vorhanden ist, indem Sie den Metadatei-Header mit der [**getenhmetafileheader**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafileheader) -Funktion abrufen und einen seiner Member untersuchen. Wenn die Zeichenfolge vorhanden ist, ruft die Anwendung Sie durch Aufrufen der [**getenhmetafiledescription**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafiledescriptiona) -Funktion ab.

## <a name="retrieve-a-binary-version-of-an-enhanced-metafile"></a>Abrufen einer binären Version einer erweiterten Metadatei

Sie können den Inhalt einer Metadatei abrufen, indem Sie die [**GetEnhMetaFileBits**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafilebits) -Funktion aufrufen. bevor Sie den Inhalt abrufen, müssen Sie jedoch die Größe der Datei angeben. Um die Größe zu erhalten, können Sie die [**getenhmetafileheader**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafileheader) -Funktion verwenden und den entsprechenden Member überprüfen.

## <a name="enumerate-the-colors-in-the-optional-palette"></a>Auflisten der Farben in der optionalen Palette

Um konsistente Farben zu erreichen, wenn ein Bild auf verschiedenen Ausgabegeräten angezeigt wird, können Sie die [**CreatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-createpalette) -Funktion aufzurufen und eine logische Palette in einer erweiterten Metadatei speichern. Eine Anwendung, die das in der erweiterten Metadatei gespeicherte Bild anzeigt, ruft diese Palette ab und ruft die [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) -Funktion vor dem Anzeigen des Bilds auf. Um zu ermitteln, ob eine Palette in einer erweiterten Metadatei gespeichert ist, rufen Sie den Metadatei-Header ab, und überprüfen Sie den entsprechenden Member. Wenn eine Palette vorhanden ist, können Sie die [**getenhmetafilepaletteentries**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafilepaletteentries) -Funktion aufrufen, um die logische Palette abzurufen.

 

 

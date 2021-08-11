---
description: 'Sie können das Handle für eine erweiterte Metadatei verwenden, um die folgenden Aufgaben auszuführen:'
ms.assetid: 8f887c38-6cfa-4918-aa44-dd5fb837b40b
title: Erweiterte Metadateivorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5daf08ef5d8d48b81aea4daa5d2696ececec3fce44b1303c9ff7ccd692151a7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118250284"
---
# <a name="enhanced-metafile-operations"></a>Erweiterte Metadateivorgänge

Sie können das Handle für eine erweiterte Metadatei verwenden, um die folgenden Aufgaben auszuführen:

-   Zeigt das in einer erweiterten Metadatei gespeicherte Bild an.
-   Erstellen Sie Kopien einer erweiterten Metadatei.
-   Bearbeiten Sie eine erweiterte Metadatei.
-   Rufen Sie die optionale Beschreibung ab, die in einer erweiterten Metadatei gespeichert ist.
-   Rufen Sie eine Kopie eines Enhanced-Metafile-Headers ab.
-   Ruft eine Binärversion einer erweiterten Metadatei ab.
-   Enumerieren Sie die Farben in der optionalen Palette.

Diese Aufgaben werden in den Abschnitten im restlichen Teil dieses Themas erläutert.

## <a name="display-the-picture-stored-in-an-enhanced-metafile"></a>Anzeigen des in einer erweiterten Metadatei gespeicherten Bilds

Sie können das in einer erweiterten Metadatei gespeicherte Bild mithilfe der [**PlayEnhMetaFile-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-playenhmetafile) anzeigen. Übergeben Sie der Funktion ein Handle an die erweiterte Metadatei, ohne sich mit dem Format der erweiterten Metadateidatensätze zu kümmern. Es ist jedoch manchmal wünschenswert, die Datensätze in der erweiterten Metadatei aufzählen, um nach einer bestimmten GDI-Funktion zu suchen und die Parameter der Funktion in irgendeiner Weise zu ändern. Hierzu können Sie [**EnumEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-enumenhmetafile) verwenden und die Rückruffunktion [**EnhMetaFileProc**](/windows/win32/api/wingdi/nc-wingdi-enhmfenumproc)bereitstellen, um die erweiterten Metadateidatensätze zu verarbeiten. Um die Parameter für einen erweiterten Metadateidatensatz zu ändern, müssen Sie das Format der Parameter innerhalb des Datensatzes kennen.

## <a name="create-copies-of-an-enhanced-metafile"></a>Erstellen von Kopien einer erweiterten Metadatei

Einige Anwendungen erstellen temporäre Sicherungskopien (oder duplizierte) Kopien einer Datei, bevor der Benutzer das Ändern des Originals ermöglicht. Eine Anwendung kann eine Sicherungskopie einer erweiterten Metadatei erstellen, indem sie die [**CopyEnhMetaFile-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-copyenhmetafilea) aufruft, ein Handle zur Identifizierung der erweiterten Metadatei und einen Zeiger auf den Namen der neuen Datei an die Hand gibt.

Um eine speicherbasierte Metadatei im erweiterten Format zu erstellen, rufen Sie die [**SetEnhMetaFileBits-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-setenhmetafilebits) auf.

## <a name="edit-an-enhanced-metafile"></a>Bearbeiten einer erweiterten Metadatei

Die meisten Cad-Anwendungen (Drawing, Illustration und Computer-Aided Design) erfordern eine Möglichkeit zum Bearbeiten eines Bilds, das in einer erweiterten Metadatei gespeichert ist. Obwohl das Bearbeiten einer erweiterten Metadatei eine komplexe Aufgabe ist, können Sie die [**EnumEnhMetaFile-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-enumenhmetafile) in Kombination mit anderen Funktionen verwenden, um diese Funktion in Ihrer Anwendung zur Verfügung zu stellen. Mit **der EnumEnhMetaFile-Funktion** und der zugehörigen Rückruffunktion [**EnhMetaFileProc**](/windows/win32/api/wingdi/nc-wingdi-enhmfenumproc)kann die Anwendung einzelne Datensätze in einer erweiterten Metadatei verarbeiten.

## <a name="retrieve-the-optional-description-stored-in-an-enhanced-metafile"></a>Abrufen der optionalen Beschreibung, die in einer erweiterten Metadatei gespeichert ist

Einige Anwendungen zeigen die Textbeschreibung einer erweiterten Metadatei mit dem entsprechenden Dateinamen im **Dialogfeld** Öffnen an. Sie können bestimmen, ob diese Zeichenfolge in einer erweiterten Metadatei vorhanden ist, indem Sie den Metadateiheader mit der [**GetEnhMetaFileHeader-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafileheader) abrufen und einen seiner Member untersuchen. Wenn die Zeichenfolge vorhanden ist, ruft die Anwendung sie ab, indem sie die [**GetEnhMetaFileDescription-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafiledescriptiona) aufruft.

## <a name="retrieve-a-binary-version-of-an-enhanced-metafile"></a>Abrufen einer Binärversion einer erweiterten Metadatei

Sie können den Inhalt einer Metadatei abrufen, indem Sie die [**GetEnhMetaFileBits-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafilebits) aufrufen. Vor dem Abrufen des Inhalts müssen Sie jedoch die Größe der Datei angeben. Um die Größe zu erhalten, können Sie die [**GetEnhMetaFileHeader-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafileheader) verwenden und den entsprechenden Member untersuchen.

## <a name="enumerate-the-colors-in-the-optional-palette"></a>Aufzählen der Farben in der optionalen Palette

Um konsistente Farben zu erzielen, wenn ein Bild auf verschiedenen Ausgabegeräten angezeigt wird, können Sie die [**CreatePalette-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-createpalette) aufrufen und eine logische Palette in einer erweiterten Metadatei speichern. Eine Anwendung, die das in der erweiterten Metadatei gespeicherte Bild anzeigt, ruft diese Palette ab und ruft die [**Funktion RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) auf, bevor das Bild angezeigt wird. Um zu bestimmen, ob eine Palette in einer erweiterten Metadatei gespeichert ist, rufen Sie den Metadateiheader ab und untersuchen den entsprechenden Member. Wenn eine Palette vorhanden ist, können Sie die [**GetEnhMetaFilePaletteEntries-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafilepaletteentries) aufrufen, um die logische Palette abzurufen.

 

 

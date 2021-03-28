---
description: Sie erstellen eine erweiterte Metadatei mithilfe der Funktion "-Funktion", die die entsprechenden Argumente bereitstellt.
ms.assetid: b012e50e-a7f5-4687-9833-38dacc113d77
title: Erweiterte metadateierstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 080c350e41e895c5d4bf834a6f407cca5907743d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754416"
---
# <a name="enhanced-metafile-creation"></a>Erweiterte metadateierstellung

Sie erstellen eine erweiterte Metadatei mithilfe der [**Funktion "**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) -Funktion", die die entsprechenden Argumente bereitstellt. Das System verwendet diese Argumente, um Bild Dimensionen beizubehalten, zu bestimmen, ob die Metadatendatei auf einem Datenträger oder im Arbeitsspeicher gespeichert werden soll usw.

Um Bild Dimensionen über Ausgabegeräte hinweg beizubehalten, erfordert die Auflösung des Referenz Geräts in der [**Datei**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) "". Dieses *Referenzgerät* ist das Gerät, auf dem das Bild zum ersten Mal angezeigt wird, und der *Referenz-DC* ist der *Gerätekontext* , der dem Referenzgerät zugeordnet ist. Wenn Sie die **CreateEnhMetaFile** -Funktion aufrufen, müssen Sie ein Handle bereitstellen, das diesen DC identifiziert. Sie können dieses Handle abrufen, indem Sie die [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) -oder [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) -Funktion aufrufen. Sie können auch **null** als Handle angeben, um das aktuelle Anzeigegerät für das Referenzgerät zu verwenden.

In den meisten Anwendungen werden Bilder permanent gespeichert und daher eine erweiterte Metadatei erstellt, die auf einem Datenträger gespeichert ist. Es gibt jedoch einige Instanzen, wenn dies nicht erforderlich ist. Beispielsweise könnte eine Textverarbeitungsanwendung, die Diagramm Zeichnungsfunktionen bereitstellt, ein benutzerdefiniertes Diagramm im Arbeitsspeicher als erweiterte Metadatendatei speichern und dann die erweiterten metadateibits aus dem Arbeitsspeicher in die Dokument Datei des Benutzers kopieren. Eine Anwendung, die eine auf einem Datenträger dauerhaft gespeicherte Metadatei erfordert, muss beim Aufrufen von "" die [**Datei "**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea)" den Dateinamen angeben. Wenn Sie keinen Dateinamen angeben, behandelt das System die Metadatendatei automatisch als temporäre Datei und speichert Sie im Arbeitsspeicher.

Sie können eine optionale Textbeschreibung zu einer Metadatei hinzufügen, die Informationen über das Bild und den Autor enthält. In einer Anwendung können diese Zeichen folgen im Dialogfeld Datei öffnen angezeigt werden, um dem Benutzerinformationen über metadateninhalte bereitzustellen, die bei der Auswahl der entsprechenden Datei helfen. Wenn eine Anwendung die Textbeschreibung enthält, muss Sie einen Zeiger auf die Zeichenfolge bereitstellen, wenn Sie "" "" " [**".**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea)

Wenn " [**deateenhmetafile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) " erfolgreich ist, wird ein Handle zurückgegeben, das einen speziellen Metadatei-Gerätekontext identifiziert. Ein Metadatei-Gerätekontext ist insofern eindeutig, als er einer Datei und nicht einem Ausgabegerät zugeordnet ist. Wenn das System eine GDI-Funktion verarbeitet, die ein Handle für einen Metadatei-Gerätekontext empfangen hat, konvertiert Sie die GDI-Funktion in einen erweiterten Metadateidatensatz und fügt den Datensatz an das Ende der erweiterten Metadatei an.

Nachdem ein Bild abgeschlossen und der letzte Datensatz an die erweiterte Metadatendatei angehängt wurde, kann die Anwendung die Datei durch Aufrufen der [**CloseEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-closeenhmetafile) -Funktion schließen. Diese Funktion schließt und löscht den speziellen Metadatei-Gerätekontext und gibt ein Handle zurück, das die erweiterte Metadatei identifiziert.

Zum Löschen einer Datei mit erweitertem Format oder eines metadateihandles mit erweitertem Format müssen Sie die [**DeleteEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-deleteenhmetafile) -Funktion aufrufen.

 

 




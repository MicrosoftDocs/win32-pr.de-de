---
description: Sie erstellen eine erweiterte Metadatei, indem Sie die CreateEnhMetaFile-Funktion verwenden und die entsprechenden Argumente angeben.
ms.assetid: b012e50e-a7f5-4687-9833-38dacc113d77
title: Erweiterte Metadateierstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c89a4a05a18ecce4bc1b1fe3689e4f7a8dc64c833db4eac937da4f9a290dd3ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831990"
---
# <a name="enhanced-metafile-creation"></a>Erweiterte Metadateierstellung

Sie erstellen eine erweiterte Metadatei, indem Sie die [**CreateEnhMetaFile-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) verwenden und die entsprechenden Argumente angeben. Das System verwendet diese Argumente, um Bilddimensionen zu verwalten, zu bestimmen, ob die Metadatei auf einem Datenträger oder im Arbeitsspeicher gespeichert werden soll, und so weiter.

Zum Verwalten von Bildabmessungen über Ausgabegeräte hinweg erfordert [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) die Auflösung des Referenzgeräts. Dieses *Referenzgerät* ist das Gerät, auf dem das Bild zum ersten Mal angezeigt wurde, und der *Referenz-DC* ist der Gerätekontext, *der* dem Referenzgerät zugeordnet ist. Beim Aufrufen der **CreateEnhMetaFile-Funktion** müssen Sie ein Handle angeben, das diesen DC identifiziert. Sie können dieses Handle durch Aufrufen der [**GetDC- oder**](/windows/desktop/api/Winuser/nf-winuser-getdc) [**CreateDC-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) erhalten. Sie können auch NULL als **Handle** angeben, um das aktuelle Anzeigegerät für das Referenzgerät zu verwenden.

Die meisten Anwendungen speichern Bilder dauerhaft und erstellen daher eine erweiterte Metadatei, die auf einem Datenträger gespeichert ist. Es gibt jedoch einige Fälle, in denen dies nicht erforderlich ist. Beispielsweise könnte eine Anwendung für die Wortverarbeitung, die Diagrammzeichnungsfunktionen bietet, ein benutzerdefiniertes Diagramm im Arbeitsspeicher als erweiterte Metadatei speichern und dann die erweiterten Metadateibits aus dem Arbeitsspeicher in die Dokumentdatei des Benutzers kopieren. Eine Anwendung, die eine Metadatei erfordert, die dauerhaft auf einem Datenträger gespeichert ist, muss den Dateinamen angeben, wenn [**sie CreateEnhMetaFile aufruft.**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) Wenn Sie keinen Dateinamen angeben, behandelt das System die Metadatei automatisch als temporäre Datei und speichert sie im Arbeitsspeicher.

Sie können einer Metadatei, die Informationen über das Bild und den Autor enthält, eine optionale Textbeschreibung hinzufügen. Eine Anwendung kann diese Zeichenfolgen im Dialogfeld Datei öffnen anzeigen, um dem Benutzer Informationen zu Metadateiinhalten zur Verfügung zu stellen, die bei der Auswahl der entsprechenden Datei helfen. Wenn eine Anwendung die Textbeschreibung enthält, muss sie beim Aufrufen von [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea)einen Zeiger auf die Zeichenfolge angeben.

Wenn [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) erfolgreich ist, wird ein Handle zurückgegeben, das einen speziellen Metadatei-Gerätekontext identifiziert. Ein Metadatei-Gerätekontext ist eindeutig, da er einer Datei und nicht einem Ausgabegerät zugeordnet ist. Wenn das System eine GDI-Funktion verarbeitet, die ein Handle in einen Metadatei-Gerätekontext empfangen hat, konvertiert es die GDI-Funktion in einen erweiterten Metadateidatensatz und fügt den Datensatz an das Ende der erweiterten Metadatei an.

Nachdem ein Bild abgeschlossen und der letzte Datensatz an die erweiterte Metadatei angefügt wurde, kann die Anwendung die Datei schließen, indem sie die [**CloseEnhMetaFile-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-closeenhmetafile) aufruft. Diese Funktion schließt und löscht den speziellen Metadatei-Gerätekontext und gibt ein Handle zurück, das die erweiterte Metadatei identifiziert.

Um eine Metadatei im erweiterten Format oder ein Metadateihand handle im erweiterten Format zu löschen, rufen Sie die [**DeleteEnhMetaFile-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-deleteenhmetafile) auf.

 

 




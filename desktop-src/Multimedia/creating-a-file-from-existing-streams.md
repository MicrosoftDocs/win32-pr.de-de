---
title: Erstellen einer Datei aus vorhandenen Streams
description: Erstellen einer Datei aus vorhandenen Streams
ms.assetid: 5149a766-7809-42b7-8e5c-b67b847b9218
keywords:
- Avisave-Funktion
- Avisavev-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bc422d2170ccd49b8a9746666db7ebbcd7dff14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947637"
---
# <a name="creating-a-file-from-existing-streams"></a>Erstellen einer Datei aus vorhandenen Streams

Eine Möglichkeit, eine Datei zu erstellen, die Datenströme enthält, besteht darin, vorhandene Streams in einer neuen Datei zu kombinieren. Die Streams, die Daten für die neue Datei bereitstellen, können sich im Arbeitsspeicher oder in einer oder mehreren Dateien befinden.

Mithilfe der [**avisave**](/windows/desktop/api/Vfw/nf-vfw-avisavea) -Funktion können Sie eine Datei aus mehreren Datenströmen erstellen. Diese Funktion erstellt eine Datei und schreibt die Datenströme, die in der aufrufenden Sequenz angegeben sind, in die Datei. Die Aufruf Sequenz für **avisave** verwendet eine Variable Anzahl von Argumenten, die Schnittstellen für die Streams enthalten, die in der neuen Datei kombiniert werden.

Mithilfe der [**avisavev**](/windows/desktop/api/Vfw/nf-vfw-avisaveva) -Funktion können Sie auch Datenströme in einer neuen Datei kombinieren. Diese Funktion bietet die gleiche Funktionalität wie **avisave**, aber wenn Sie **avisavev** verwenden, gibt Ihre Anwendung die Datenströme als Array und nicht als Variable Anzahl von Argumenten an.

Sie können ein Dialogfeld erstellen, in dem der Benutzer mithilfe der [**avisaveoptions**](/windows/desktop/api/Vfw/nf-vfw-avisaveoptions) -Funktion Komprimierungs Einstellungen für die neue Datei auswählen kann. Das Dialogfeld zeigt die aktuellen Komprimierungs Einstellungen an und ermöglicht dem Benutzer, Sie zu bearbeiten. Änderungen an der Komprimierungs Einstellung werden in einer [**avicompressoptions**](/windows/desktop/api/Vfw/ns-vfw-avicompressoptions) -Struktur gespeichert.

Sie können auch eine Rückruffunktion mit [**avisave**](/windows/desktop/api/Vfw/nf-vfw-avisavea) und [**avisavev**](/windows/desktop/api/Vfw/nf-vfw-avisaveva) einschließen, die Ihre Anwendung verwenden kann, um den Fortschritt beim Schreiben der Datei anzuzeigen und ggf. den Benutzer den Speichervorgang abzubrechen. Sie können die Adresse der Rückruffunktion in die Aufruf Sequenz von **avisave** oder **avisavev** einschließen.

Mithilfe der Funktion [**getsavefileamepreview**](/windows/desktop/api/Vfw/nf-vfw-getsavefilenamepreviewa) können Sie den Benutzer einen Dateinamen für die neue Datei auswählen lassen. Diese Funktion zeigt das Dialogfeld Speichern unter an, in dem der Benutzer eine Vorschau für den ersten Datenstrom (normalerweise den Videostream) einer AVI-Datei anzeigen kann.

Mithilfe der [**avimakefilefromstreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) -Funktion können Sie einen Datei Schnittstellen Zeiger (und eine virtuelle Datei) für eine Gruppe von Datenströmen erstellen. Andere avifile-Funktionen können den Datei Schnittstellen Zeiger verwenden, der von dieser Funktion zurückgegeben wird, um auf die Datenströme in der virtuellen Datei zuzugreifen. Nachdem Sie die virtuelle Datei fertig verwendet haben, löschen Sie den Datei Schnittstellen Zeiger mithilfe der [**avifilerelease**](/windows/desktop/api/Vfw/nf-vfw-avifilerelease) -Funktion.

> [!Note]  
> Vermeiden Sie es, eine AVI-Datei mehrmals zu komprimieren, um die Abbild-und audiobeeinträchtigung zu minimieren. Kombinieren Sie unkomprimierte Video Teile in Ihrem Bearbeitungssystem, und komprimieren Sie dann das endgültige Produkt. Weitere Informationen zu Komprimierungs Optionen finden Sie unter [Video Compression Manager](video-compression-manager.md).

 

 

 





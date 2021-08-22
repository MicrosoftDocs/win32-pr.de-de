---
title: Erstellen einer Datei aus vorhandenen Streams
description: Erstellen einer Datei aus vorhandenen Streams
ms.assetid: 5149a766-7809-42b7-8e5c-b67b847b9218
keywords:
- AVISave-Funktion
- AVISaveV-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a15a6ad3770f93bc2fb77dcb79975e1e9aa1fc8da7319e34c140baf488a69554
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498010"
---
# <a name="creating-a-file-from-existing-streams"></a>Erstellen einer Datei aus vorhandenen Streams

Eine Möglichkeit zum Erstellen einer Datei, die Datenströme enthält, besteht darin, vorhandene Datenströme in einer neuen Datei zu kombinieren. Die Datenströme, die Daten für die neue Datei bereitstellen, können sich im Arbeitsspeicher oder in einer oder mehreren Dateien befinden.

Sie können eine Datei aus mehreren Streams erstellen, indem Sie die [**AVISave-Funktion**](/windows/desktop/api/Vfw/nf-vfw-avisavea) verwenden. Diese Funktion erstellt eine Datei und schreibt die in der aufrufenden Sequenz angegebenen Datenströme in die Datei. Die aufrufende Sequenz für **AVISave** verwendet eine variable Anzahl von Argumenten, die Schnittstellen für die in der neuen Datei kombinierten Streams enthalten.

Sie können Datenströme auch mithilfe der [**AVISaveV-Funktion**](/windows/desktop/api/Vfw/nf-vfw-avisaveva) in einer neuen Datei kombinieren. Diese Funktion bietet die gleiche Funktionalität wie **AVISave,** aber wenn Sie **AVISaveV** verwenden, gibt Ihre Anwendung die Datenströme als Array und nicht als variable Anzahl von Argumenten an.

Sie können ein Dialogfeld erstellen, in dem der Benutzer komprimierungseinstellungen für die neue Datei mithilfe der [**AVISaveOptions-Funktion**](/windows/desktop/api/Vfw/nf-vfw-avisaveoptions) auswählen kann. Im Dialogfeld werden die aktuellen Komprimierungseinstellungen angezeigt, und der Benutzer kann sie bearbeiten. Änderungen der Komprimierungseinstellung werden in einer [**AVICOMPRESSOPTIONS-Struktur**](/windows/desktop/api/Vfw/ns-vfw-avicompressoptions) gespeichert.

Sie können auch eine Rückruffunktion mit [**AVISave**](/windows/desktop/api/Vfw/nf-vfw-avisavea) und [**AVISaveV**](/windows/desktop/api/Vfw/nf-vfw-avisaveva) einschließen, die Ihre Anwendung verwenden kann, um den Fortschritt beim Schreiben der Datei anzuzeigen und den Benutzer bei Bedarf den Speichervorgang abbrechen zu lassen. Sie können die Adresse der Rückruffunktion in die aufrufende Sequenz von **AVISave** oder **AVISaveV** einschließen.

Sie können dem Benutzer mithilfe der Funktion [**GetSaveFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getsavefilenamepreviewa) einen Dateinamen für die neue Datei auswählen lassen. Diese Funktion zeigt das Dialogfeld Speichern unter an, in dem der Benutzer eine Vorschau des ersten Streams (normalerweise des Videodatenstroms) einer AVI-Datei anzeigen kann.

Sie können einen Dateischnittstellenzeiger (und eine virtuelle Datei) für eine Gruppe von Streams erstellen, indem Sie die [**AVIMakeFileFromStreams-Funktion**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) verwenden. Andere AVIFile-Funktionen können den von dieser Funktion zurückgegebenen Dateischnittstellenzeiger verwenden, um auf die Streams in der virtuellen Datei zuzugreifen. Nachdem Sie die virtuelle Datei verwendet haben, löschen Sie den Dateischnittstellenzeiger mithilfe der [**FUNKTION AVIFileRelease.**](/windows/desktop/api/Vfw/nf-vfw-avifilerelease)

> [!Note]  
> Um die Bild- und Audiobeeinträchtigung zu minimieren, vermeiden Sie die mehrfache Komprimierung einer AVI-Datei. Kombinieren Sie unkomprimierte Videoteile in Ihrem Bearbeitungssystem, und komprimieren Sie dann das endgültige Produkt. Informationen zu Komprimierungsoptionen finden Sie unter [Videokomprimierungs-Manager.](video-compression-manager.md)

 

 

 





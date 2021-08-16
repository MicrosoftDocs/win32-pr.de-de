---
description: In diesem Thema wird die Verwendung der Dateitypüberprüfung beschrieben, die im Windows 7 SDK bereitgestellt wird.
ms.assetid: 96FCA74B-DEB2-49D1-B670-EBD8BE0783F1
title: Verwenden der Dateitypüberprüfung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65af06de30d4fca2a9f5209d20e200153c061248576e7e94c8342cf9ae60e4f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118223372"
---
# <a name="how-to-use-the-file-type-verifier"></a>Verwenden der Dateitypüberprüfung

In diesem Thema wird beschrieben, wie die Dateitypüberprüfung verwendet wird, die im [Windows 7 SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)bereitgestellt wird. Wenn Ihr Programm Dateitypen erstellt, mit denen Benutzer über die Windows Shell interagieren sollen (die normalerweise im bekannten Ordner eines Benutzers wie **Eigene Dokumente** gespeichert sind), ist es sehr wichtig, Ihre Anwendung zu testen und zu überprüfen, ob die dateien, die sie erstellt, ordnungsgemäß registriert sind und eine hochwertige Benutzererfahrung beim Durchsuchen und Durchsuchen von Dateien bieten. Dies ist besonders wichtig, wenn Sie erwarten, dass Benutzer Ihre Anwendungen auf Windows 7 ausführen, die für viele der Shellfeatures auf hochwertigen Dateityphandlern basiert.

Führen Sie die folgenden Schritte aus, um Ihren Dateityp mithilfe der Dateitypüberprüfung zu überprüfen.

## <a name="instructions"></a>Anweisungen

### <a name="step-1"></a>Schritt 1:

Installieren Sie die Anwendung in Ihrer Testumgebung, und kopieren Sie die Dateitypüberprüfung in diese Umgebung. Die Dateitypüberprüfung ist im [Windows 7 SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)verfügbar.

### <a name="step-2"></a>Schritt 2:

Verwenden Sie Ihre Anwendung, um eine Datei zu erstellen, die getestet werden soll.

### <a name="step-3"></a>Schritt 3:

Starten Sie die Dateitypüberprüfung.

### <a name="step-4"></a>Schritt 4:

Wählen Sie die Kategorie für Ihren Dateityp aus, wie im folgenden Screenshot gezeigt.

![Screenshot: Drag & Drop-Funktion](images/file-assoc/filetypeverifier1.png)

Die Kategorieauswahl bestimmt den Satz von Tests, die vom Tool ausgeführt werden. Wenn Ihr Typ unter mehrere Kategorien fallen kann (z. B. kann eine TIF-Datei je nach Inhalt ein Bild oder ein Dokument sein), führen Sie das Tool mit jeder entsprechenden Kategorie erneut aus.

### <a name="step-5"></a>Schritt 5:

Suchen Sie mit Windows Explorer nach einer datei, die getestet werden soll, und ziehen Sie sie mit der Maus auf das Ziel in Dateitypüberprüfung, wie im folgenden Screenshot gezeigt.

![Screenshot der Drag & Drop-Funktion](images/file-assoc/filetypeverifier2.png)

### <a name="step-6"></a>Schritt 6:

Warten Sie, bis das Tool "Dateitypüberprüfung" eine Reihe von Tests durchläuft. Der Fortschritt der Tests wird auf der Statusleiste angezeigt, wie im folgenden Screenshot gezeigt.

![Screenshot: Statusanzeige](images/file-assoc/filetypeverifier3.png)

### <a name="step-7"></a>Schritt 7:

Überprüfen Sie die Ergebniszusammenfassung ihrer Dokumentdateityptests, wie im folgenden Screenshot gezeigt.

![Screenshot der Ergebniszusammenfassung](images/file-assoc/filetypeverifier4.png)

### <a name="step-8"></a>Schritt 8:

Klicken Sie auf der Zusammenfassungsseite auf eines der Ergebnisse, um das ausführliche Protokoll anzuzeigen. Ein Beispielprotokoll für einen Vorschauhandler wird im folgenden Screenshot gezeigt.

![Screenshot des Vorschauhandlerprotokolls](images/file-assoc/filetypeverifier5.png)

### <a name="step-9"></a>Schritt 9:

Um eine Kopie der Protokolldatei zu speichern, klicken Sie unten in der Protokollanzeige auf **Protokolldatei speichern,** und wählen Sie einen geeigneten Speicherort für die Speicherung auf Ihrem Computer aus.

### <a name="step-10"></a>Schritt 10:

Wenn Fehler gemeldet werden, nehmen Sie die entsprechenden Änderungen in Ihrer Anwendung vor, und führen Sie das Tool erneut aus, um zu überprüfen, ob die Fehler nicht mehr in den Tests angezeigt werden. Wenn Warnungen gemeldet werden, werten Sie sie aus, entscheiden Sie, ob sie für Ihren bestimmten Dateityp relevant sind, und nehmen Sie bei Bedarf die entsprechenden Änderungen an Ihrer Anwendung vor.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows 7 SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)
</dt> </dl>

 

 




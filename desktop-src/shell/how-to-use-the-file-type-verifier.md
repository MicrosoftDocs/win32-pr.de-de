---
description: In diesem Thema wird beschrieben, wie Sie den Dateityp Verifier verwenden, der im Windows 7 SDK bereitgestellt wird.
ms.assetid: 96FCA74B-DEB2-49D1-B670-EBD8BE0783F1
title: Verwenden des Dateityp-verifizierers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f083897499f972f945867a0c02318df192e734d9
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/28/2021
ms.locfileid: "104218891"
---
# <a name="how-to-use-the-file-type-verifier"></a>Verwenden des Dateityp-verifizierers

In diesem Thema wird beschrieben, wie Sie den Dateityp Verifier verwenden, der im [Windows 7 SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)bereitgestellt wird. Wenn das Programmdatei Typen erstellt, mit denen Benutzer von der Windows-Shell aus interagieren (in der Regel im bekannten Ordner eines Benutzers, z. b. " **eigene** Dateien"), ist es sehr wichtig, die Anwendung zu testen und zu überprüfen, ob die erstellten Dateien ordnungsgemäß registriert sind und eine hochwertige Benutzer Darstellung beim Durchsuchen und Durchsuchen von Dateien bieten. Dies ist besonders wichtig, wenn Sie erwarten, dass Benutzer ihre Anwendungen unter Windows 7 ausführen, was für viele Shellfeatures hochwertige Dateityp Handler ist.

Führen Sie die folgenden Schritte aus, um den Dateityp mit dem Dateityp Verifier zu überprüfen.

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Schritt 1:

Installieren Sie die Anwendung in der Testumgebung, und kopieren Sie die Dateityp Überprüfung in diese Umgebung. Der Dateityp Verifier ist im [Windows 7 SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)verfügbar.

### <a name="step-2"></a>Schritt 2:

Verwenden Sie Ihre Anwendung, um eine zu testende Datei zu erstellen.

### <a name="step-3"></a>Schritt 3:

Starten Sie den Dateityp Verifier.

### <a name="step-4"></a>Schritt 4:

Wählen Sie die Kategorie für den Dateityp aus, wie im folgenden Screenshot gezeigt.

![Screenshot, der die Drag & amp; Drop-Funktion anzeigt.](images/file-assoc/filetypeverifier1.png)

Die Kategorieauswahl bestimmt den Satz von Tests, die vom Tool ausgeführt werden. Wenn Ihr Typ unter mehr als eine Kategorie fallen könnte (z. b. kann eine TIF-Datei je nach Inhalt ein Bild oder ein Dokument sein), führen Sie das Tool erneut mit jeder entsprechenden Kategorie aus.

### <a name="step-5"></a>Schritt 5:

Suchen Sie mithilfe von Windows-Explorer eine zu testende Datei, und ziehen Sie Sie mit der Maus auf das Ziel im Dateityp Verifier, wie im folgenden Screenshot gezeigt.

![Screenshot der Drag & Drop-Funktion](images/file-assoc/filetypeverifier2.png)

### <a name="step-6"></a>Schritt 6:

Warten Sie, bis das Dateityp-Verifier-Tool eine Reihe von Tests durchläuft. Der Fortschritt der Tests wird von der Statusanzeige wie im folgenden Screenshot dargestellt.

![Screenshot der Statusanzeige](images/file-assoc/filetypeverifier3.png)

### <a name="step-7"></a>Schritt 7:

Überprüfen Sie die Ergebnis Zusammenfassung Ihrer Dokument Dateityp Tests, wie im folgenden Screenshot gezeigt.

![Screenshot der Ergebnis Zusammenfassung](images/file-assoc/filetypeverifier4.png)

### <a name="step-8"></a>Schritt 8:

Klicken Sie auf die Ergebnisse auf der Zusammenfassungs Seite, um das ausführliche Protokoll anzuzeigen. Ein Beispiel Protokoll für einen Vorschau Handler wird im folgenden Screenshot gezeigt.

![Screenshot des Vorschau handlerprotokolls](images/file-assoc/filetypeverifier5.png)

### <a name="step-9"></a>Schritt 9:

Wenn Sie eine Kopie der Protokolldatei speichern möchten, klicken Sie am unteren Rand der Protokoll Anzeige auf **Protokolldatei speichern** , und wählen Sie einen geeigneten Speicherort für die Speicherung auf dem Computer aus.

### <a name="step-10"></a>Schritt 10:

Wenn Fehler gemeldet werden, nehmen Sie die entsprechenden Änderungen in der Anwendung vor, und führen Sie das Tool erneut aus, um zu überprüfen, ob die Fehler nicht mehr in den Tests angezeigt werden. Wenn Warnungen gemeldet werden, sollten Sie diese auswerten und entscheiden, ob Sie für Ihren speziellen Dateityp relevant sind, und die entsprechenden Änderungen an der Anwendung vornehmen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows 7 SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)
</dt> </dl>

 

 




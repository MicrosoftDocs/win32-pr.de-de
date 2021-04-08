---
description: Die Windows-Kenn Wortfilter-dll, Passfilt.dll, wird im Sicherheitskontext des lokalen System Kontos ausgeführt und hilft Ihnen, Domänen Kennwörter oder lokale Konto Kennwörter zu filtern.
ms.assetid: 12a6fe6d-5b37-4fcf-bd04-0a22d84ba323
title: Installieren und Registrieren einer Kenn Wort Filter-dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cd911c1a527384e48a2ae4567f6d85862e184cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865444"
---
# <a name="installing-and-registering-a-password-filter-dll"></a>Installieren und Registrieren einer Kenn Wort Filter-dll

Mit dem Windows-Kenn Wortfilter können Sie Domänen Kennwörter oder lokale Konto Kennwörter filtern. Wenn Sie den Kenn Wortfilter für Domänen Konten verwenden möchten, installieren und registrieren Sie die dll auf den einzelnen Domänen Controllern in der Domäne.

Führen Sie die folgenden Schritte aus, um den Kenn Wortfilter zu installieren. Sie können diese Schritte manuell ausführen, oder Sie können ein Installationsprogramm schreiben, um diese Schritte auszuführen. Sie müssen ein Administrator sein oder zur Administrator Gruppe gehören, um diese Schritte ausführen zu können.

**So installieren und registrieren Sie eine Windows-Kenn Wortfilter-dll**

1.  Kopieren Sie die dll in das Windows-Installationsverzeichnis auf dem Domänen Controller oder auf dem lokalen Computer. Bei Standard Installationen ist Windows System32 der Standard \\ Ordner \\ . Stellen Sie sicher, dass Sie eine 32-Bit-Kenn Wortfilter-dll für 32-Bit-Computer und eine 64-Bit-Kenn Wortfilter-dll für 64-Bit-Computer erstellen und diese dann an den entsprechenden Speicherort kopieren.
2.  Aktualisieren Sie den folgenden System Registrierungsschlüssel, um den Kenn Wortfilter zu registrieren:

    ```
    HKEY_LOCAL_MACHINE
       SYSTEM
          CurrentControlSet
             Control
                Lsa
    ```

    Wenn der Unterschlüssel für **Benachrichtigungs Pakete** vorhanden ist, fügen Sie den vorhandenen Wertdaten den Namen der dll hinzu. Überschreiben Sie die vorhandenen Werte nicht, und schließen Sie die DLL-Erweiterung nicht ein.

    Wenn der Unterschlüssel für **Benachrichtigungs Pakete** nicht vorhanden ist, fügen Sie ihn hinzu, und geben Sie dann den Namen der DLL für die Wertdaten an. Schließen Sie die DLL-Erweiterung nicht ein.

    Mit dem Unterschlüssel **Benachrichtigungs Pakete** können mehrere Pakete hinzugefügt werden.

3.  Suchen Sie die Einstellung für die Kenn Wort Komplexität.

    Klicken Sie in der Systemsteuerung auf **Leistung und Wartung**, klicken Sie auf **Verwaltungs Tools**, doppelklicken Sie auf **lokale Sicherheitsrichtlinie**, doppelklicken Sie auf **Konto Richtlinien**, und doppelklicken Sie dann auf Kenn **Wort Richtlinie**.

4.  Um sowohl den standardmäßigen Windows-Kenn Wortfilter als auch den benutzerdefinierten Kenn Wortfilter zu erzwingen, stellen Sie sicher, dass die Richtlinien Einstellung Kenn **Wörter müssen Komplexitäts Anforderungen entsprechen** Deaktivieren Sie andernfalls die Richtlinien Einstellung Kenn **Wörter müssen Komplexitäts Anforderungen entsprechen** .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Überlegungen zur Kenn Wort Filter Programmierung](password-filter-programming-considerations.md)
</dt> <dt>

[Starke Kenn Wort Erzwingung und Passfilt.dll](strong-password-enforcement-and-passfilt-dll.md)
</dt> <dt>

[Kenn Wort Filter Funktionen](management-functions.md)
</dt> </dl>

 

 




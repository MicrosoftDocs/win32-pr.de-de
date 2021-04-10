---
description: Um dem Ordner Komponenten einer COM+-Anwendung Komponenten hinzuzufügen, können Sie entweder den com+-Komponenteninstallations-Assistenten verwenden oder DLL-Dateien ziehen, die die Komponenten aus dem Windows-Explorer enthalten, und Sie in der Anwendung ablegen.
ms.assetid: 3cb0c24d-cd52-42ac-8b07-d8774698b90c
title: Installieren neuer Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 434bdb59c0a0e9c786bb3460a0cb1cbb6a1f50dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041468"
---
# <a name="installing-new-components"></a>Installieren neuer Komponenten

Um dem Ordner **Komponenten** einer COM+-Anwendung Komponenten hinzuzufügen, können Sie entweder den com+-Komponenteninstallations-Assistenten verwenden oder DLL-Dateien ziehen, die die Komponenten aus dem Windows-Explorer enthalten, und Sie in der Anwendung ablegen.

Wenn Sie den com+-Komponenteninstallations-Assistenten verwenden, können Sie entweder eine neue-Komponente installieren, die die Komponente auf dem Computer registriert, oder bereits registrierte Komponenten importieren. Komponenten können leeren Anwendungen oder vorhandenen Anwendungen hinzugefügt werden.

**So fügen Sie einer COM+-Anwendung eine Komponente hinzu**

1.  Wählen Sie in der Konsolen Struktur des Verwaltungs Programms Komponenten Dienste den Computer aus, auf dem die COM+-Anwendung gehostet wird.

2.  Öffnen Sie den Ordner **com+-Anwendungen** für diesen Computer, und wählen Sie die Anwendung aus, in der Sie die Komponenten installieren möchten.

3.  Öffnen Sie den Anwendungsordner, und wählen Sie **Komponenten** aus.

4.  Zeigen Sie im Menü **Aktion** auf **neu**, und klicken Sie dann auf **Komponente**. Sie können auch mit der rechten Maustaste auf den Ordner **Komponenten** , zeigen Sie auf **neu**, und klicken Sie dann auf **Komponente**.

5.  Klicken Sie auf der **Willkommens** Seite des COM+-Anwendungsinstallations-Assistenten auf **weiter**, und klicken Sie dann im Dialogfeld **Komponente importieren oder installieren** auf **neue Komponenten installieren** .

6.  Klicken Sie im Dialogfeld **neue Komponenten installieren** auf **Hinzufügen** , um die Komponente zu suchen, die Sie hinzufügen möchten.

7.  Geben Sie im Dialogfeld **zu installierenden Dateien auswählen** den Dateinamen der zu installierenden Komponente ein, oder wählen Sie einen Dateinamen aus der angezeigten Liste aus. Klicken Sie auf **Öffnen**.

    Nachdem Sie die Dateien hinzugefügt haben, werden im Dialogfeld **neue Komponenten installieren** die Dateien angezeigt, die Sie hinzugefügt haben, und die zugehörigen Komponenten. Wenn Sie das Kontrollkästchen **Details** aktivieren, werden weitere Informationen zum Inhalt der Datei und zu den gefundenen Komponenten angezeigt.

    > [!Note]  
    > Nicht konfigurierte COM-Komponenten müssen eine Typbibliothek aufweisen. Wenn com+ die Typbibliothek der Komponente nicht finden kann, wird die Komponente nicht in der Liste angezeigt. Sie können eine Datei auch aus der Liste **zu installierendes Dateien entfernen,** indem Sie Sie auswählen und auf **Entfernen** klicken.

     

8.  Klicken Sie auf **weiter** und dann auf **Fertig** stellen, um die Komponente zu installieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kopieren von Komponenten](copying-components.md)
</dt> <dt>

[Eine neue COM+-Anwendung wird erstellt.](creating-a-new-com--application.md)
</dt> <dt>

[Eine COM+-Anwendung wird gelöscht.](deleting-a-com--application.md)
</dt> <dt>

[Importieren von Komponenten](importing-components.md)
</dt> <dt>

[Verschieben von Komponenten](moving-components.md)
</dt> <dt>

[Entfernen einer Komponente aus einer COM+-Anwendung](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 




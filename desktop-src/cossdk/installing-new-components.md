---
description: Zum Hinzufügen von Komponenten zum Ordner Komponenten einer COM+-Anwendung können Sie entweder den Installations-Assistenten für COM+-Komponenten verwenden oder .dll-Dateien, die die Komponenten enthalten, aus dem Windows-Explorer ziehen und in der Anwendung ablegen.
ms.assetid: 3cb0c24d-cd52-42ac-8b07-d8774698b90c
title: Installieren neuer Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af51bf28ce93e2d68dd1a07609c48c506911310781e8c5a0573017d43e022353
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118813590"
---
# <a name="installing-new-components"></a>Installieren neuer Komponenten

Zum Hinzufügen von  Komponenten zum Ordner Komponenten einer COM+-Anwendung können Sie entweder den Installations-Assistenten für COM+-Komponenten verwenden oder .dll-Dateien, die die Komponenten enthalten, aus dem Windows-Explorer ziehen und in der Anwendung ablegen.

Wenn Sie den Installations-Assistenten für COM+-Komponenten verwenden, können Sie entweder eine neue Komponente installieren, die die Komponente auf dem Computer registriert, oder Bereits registrierte Komponenten importieren. Komponenten können leeren Anwendungen oder vorhandenen Anwendungen hinzugefügt werden.

**So fügen Sie einer COM+-Anwendung eine Komponente hinzu**

1.  Wählen Sie in der Konsolenstruktur des Komponentendienste-Verwaltungstools den Computer aus, der die COM+-Anwendung hosten soll.

2.  Öffnen Sie **den Ordner COM+-Anwendungen** für diesen Computer, und wählen Sie die Anwendung aus, in der Sie die Komponenten installieren möchten.

3.  Öffnen Sie den Anwendungsordner, und wählen Sie **Komponenten aus.**

4.  Zeigen Sie **im Menü** Aktion auf **Neu,** und klicken Sie dann auf **Komponente**. Sie können auch mit der rechten Maustaste auf den **Ordner Komponenten** klicken, auf **Neu zeigen** und dann auf **Komponente klicken.**

5.  Klicken Sie auf **der** Willkommensseite des Assistenten zum Installieren  von COM+-Anwendungen auf Weiter, und klicken Sie dann im Dialogfeld Komponente importieren oder installieren auf **Neue Komponenten installieren.**

6.  Klicken Sie im Dialogfeld Neue  **Komponenten** installieren auf Hinzufügen, um nach der Komponente zu suchen, die Sie hinzufügen möchten.

7.  Geben Sie **im Dialogfeld Zu** installierende Dateien auswählen den Dateinamen der zu installierenden Komponente ein, oder wählen Sie einen Dateinamen aus der angezeigten Liste aus. Klicken Sie auf **Öffnen**.

    Nachdem Sie die Dateien hinzugefügt haben, werden im **Dialogfeld Neue** Komponenten installieren die hinzugefügten Dateien und die zugehörigen Komponenten angezeigt. Wenn Sie das **Kontrollkästchen Details** aktivieren, werden weitere Informationen zum Dateiinhalt und den gefundenen Komponenten angezeigt.

    > [!Note]  
    > Nicht konfigurierte COM-Komponenten müssen über eine Typbibliothek verfügen. Wenn COM+ die Typbibliothek Ihrer Komponente nicht finden kann, wird die Komponente nicht in der Liste angezeigt. Sie können eine Datei  auch aus der Liste Zu installierende Dateien entfernen, indem Sie sie auswählen und auf **Entfernen klicken.**

     

8.  Klicken **Sie auf Weiter** und dann auf Fertig **stellen,** um die Komponente zu installieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kopieren von Komponenten](copying-components.md)
</dt> <dt>

[Erstellen einer neuen COM+-Anwendung](creating-a-new-com--application.md)
</dt> <dt>

[Löschen einer COM+-Anwendung](deleting-a-com--application.md)
</dt> <dt>

[Importieren von Komponenten](importing-components.md)
</dt> <dt>

[Verschieben von Komponenten](moving-components.md)
</dt> <dt>

[Entfernen einer Komponente aus einer COM+-Anwendung](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 




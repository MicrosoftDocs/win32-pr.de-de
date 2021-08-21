---
description: Wenn vorhandene Anwendungen veraltet sind oder nicht mehr verwendet werden, müssen Sie sie möglicherweise entfernen.
ms.assetid: 5cce94c9-8eff-40b9-946d-a57749da073d
title: Löschen einer COM+-Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8332cd59ecde4115daa43ea97bc87d4354338e3ea94073317bfa293102deb78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047508"
---
# <a name="deleting-a-com-application"></a>Löschen einer COM+-Anwendung

Wenn vorhandene Anwendungen veraltet sind oder nicht mehr verwendet werden, müssen Sie sie möglicherweise entfernen.

**So löschen Sie eine COM+-Anwendung**

1.  Wählen Sie in der Konsolenstruktur des Component Services-Verwaltungstools den Computer aus, für den Sie eine Anwendung löschen möchten.

2.  Öffnen Sie den Ordner **COM+-Anwendungen** für den angegebenen Computer, um alle Anwendungen anzuzeigen.

3.  Wählen Sie die Anwendung aus, die Sie entfernen möchten.

4.  Wenn Sie eine Serveranwendung ausgewählt haben, fahren Sie die Anwendung herunter. Sie können eine Anwendung herunterfahren, indem Sie sie im Verwaltungstool Komponentendienste auswählen, mit der rechten Maustaste klicken und dann auf **Herunterfahren** klicken. Wenn Sie eine Bibliotheksanwendung ausgewählt haben, stellen Sie sicher, dass alle Prozesse, die diese Bibliotheksanwendung derzeit verwenden, heruntergefahren werden.

5.  Klicken Sie im Menü **Aktion** auf **Löschen**. Sie können auch mit der rechten Maustaste auf den Anwendungsnamen klicken und dann auf **Löschen** klicken. Sie können eine Anwendung auch löschen, indem Sie sie im Verwaltungstool Komponentendienste auswählen und die **Löschtaste** drücken. Alternativ können Sie die Anwendung auswählen, mit der rechten Maustaste klicken und dann auf **Löschen** klicken.

6.  Klicken Sie auf **Ja,** wenn Sie aufgefordert werden, Ihre Aktion zu bestätigen.

Wenn eine Serveranwendung oder ein Anwendungsproxy auf einem Computer mithilfe Windows Installers installiert wurde (wie unter "Installieren von COM+-Anwendungen" im Handbuch zur Verwaltung von Komponentendiensten beschrieben), können Sie sie außerdem über das Hilfsprogramm Software im Microsoft Windows Systemsteuerung löschen. Alternativ können Sie eine installierte Serveranwendung oder einen Anwendungsproxy löschen, indem Sie die Befehlszeilensyntax Windows Installer verwenden:

**msiexec -x** *\_ Anwendungsname .msi**

Diese Methoden sind besonders nützlich zum Löschen von COM+-Anwendungen auf Clientcomputern, auf denen das Verwaltungstool Komponentendienste nicht ausgeführt wird.

Beim Löschen der Anwendung werden auch alle in der Anwendung enthaltenen Komponenten gelöscht. Wenn diese Komponenten von zusätzlichen Ressourcen (Datenbankverbindungen, Daten- oder Textdateien, virtuelle IIS-Stammkonfiguration usw.) abhängen, müssen diese Ressourcen über andere Mechanismen als das Verwaltungstool Komponentendienste entfernt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kopieren von Komponenten](copying-components.md)
</dt> <dt>

[Erstellen einer neuen COM+-Anwendung](creating-a-new-com--application.md)
</dt> <dt>

[Importieren von Komponenten](importing-components.md)
</dt> <dt>

[Installieren neuer Komponenten](installing-new-components.md)
</dt> <dt>

[Verschieben von Komponenten](moving-components.md)
</dt> <dt>

[Entfernen einer Komponente aus einer COM+-Anwendung](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 




---
description: Wenn vorhandene Anwendungen veraltet sind oder nicht mehr verwendet werden, müssen Sie Sie möglicherweise entfernen.
ms.assetid: 5cce94c9-8eff-40b9-946d-a57749da073d
title: Eine COM+-Anwendung wird gelöscht.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da685e5a7ae7590fcc247caa765d49dc34d076e9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393130"
---
# <a name="deleting-a-com-application"></a>Eine COM+-Anwendung wird gelöscht.

Wenn vorhandene Anwendungen veraltet sind oder nicht mehr verwendet werden, müssen Sie Sie möglicherweise entfernen.

**So löschen Sie eine COM+-Anwendung**

1.  Wählen Sie in der Konsolen Struktur des Verwaltungs Programms Komponenten Dienste den Computer aus, für den Sie eine Anwendung löschen möchten.

2.  Öffnen Sie den **com+-Anwendungs** Ordner für den angegebenen Computer, um alle Anwendungen anzuzeigen.

3.  Wählen Sie die Anwendung aus, die Sie entfernen möchten.

4.  Wenn Sie eine Serveranwendung ausgewählt haben, fahren Sie die Anwendung herunter. Sie können eine Anwendung Herunterfahren, indem Sie Sie im Verwaltungs Programmkomponenten Dienste auswählen, mit der rechten Maustaste klicken und dann auf **herunter** fahren klicken. Wenn Sie eine Bibliotheks Anwendung ausgewählt haben, stellen Sie sicher, dass alle derzeit diese Bibliotheks Anwendung verwendeten Prozesse heruntergefahren werden.

5.  Klicken Sie im Menü **Aktion** auf **Löschen**. Sie können auch mit der rechten Maustaste auf den Anwendungsnamen klicken und dann auf **Löschen** klicken. Sie können eine Anwendung auch löschen, indem Sie Sie im Verwaltungs Programmkomponenten Dienste auswählen und die ENTF-Taste drücken, oder Sie können die Anwendung auswählen, **mit der rechten** Maustaste klicken und dann auf **Löschen** klicken.

6.  Klicken Sie auf **Ja** , wenn Sie zur Bestätigung Ihrer Aktion aufgefordert werden.

Außerdem können Sie, wenn eine Serveranwendung oder ein Anwendungs Proxy mithilfe von Windows Installer auf einem Computer installiert wurde (wie unter "Installieren von com+-Anwendungen" beschrieben), das Hilfsprogramm "Software" in der Microsoft Windows-Systemsteuerung löschen. Oder Sie können eine installierte Serveranwendung oder einen Anwendungs Proxy mithilfe der Windows Installer Befehlszeilen Syntax löschen:

**msiexec-x** *Anwendungs \_ Name * * *. msi**

Diese Methoden sind besonders nützlich zum Löschen von com+-Anwendungen auf Client Computern, auf denen das Verwaltungs Programmkomponenten Dienste nicht ausgeführt wird.

Wenn Sie die Anwendung löschen, werden auch alle in der Anwendung enthaltenen Komponenten gelöscht. Wenn diese Komponenten von zusätzlichen Ressourcen (Datenbankverbindungen, Daten-oder Textdateien, IIS Virtual root Configuration usw.) abhängen, müssen diese Ressourcen über andere Mechanismen als das Verwaltungs Programmkomponenten Dienste entfernt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kopieren von Komponenten](copying-components.md)
</dt> <dt>

[Eine neue COM+-Anwendung wird erstellt.](creating-a-new-com--application.md)
</dt> <dt>

[Importieren von Komponenten](importing-components.md)
</dt> <dt>

[Installieren neuer Komponenten](installing-new-components.md)
</dt> <dt>

[Verschieben von Komponenten](moving-components.md)
</dt> <dt>

[Entfernen einer Komponente aus einer COM+-Anwendung](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 




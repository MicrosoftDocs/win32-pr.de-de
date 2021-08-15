---
description: Da Sie in vielen Fällen nur einen Teil der Komponentenfunktionen in der Microsoft Visual Basic-Umgebung debuggen können, müssen Sie Komponenten debuggen, die mit Visual Basic erstellt wurden, nachdem sie kompiliert wurden. Da die Visual Basic-Umgebung dies nicht aktiviert, müssen Sie stattdessen die Microsoft Visual C++-Umgebung verwenden.
ms.assetid: a58c5884-3c2d-4699-8b19-277003912dfd
title: Debuggen von kompilierten Visual Basic Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eac784808602d3554e4610e70a8d8a22ef2ca1594062599ec6acd43db68b98a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128782"
---
# <a name="debugging-compiled-visual-basic-components"></a>Debuggen von kompilierten Visual Basic Komponenten

Da Sie in vielen Fällen nur einen Teil der Funktionalität Ihrer Komponente in der Microsoft Visual Basic-Umgebung debuggen können, müssen Sie Komponenten debuggen, die mit Visual Basic erstellt wurden, nachdem sie kompiliert wurden. Da die Visual Basic-Umgebung dies nicht aktiviert, müssen Sie stattdessen die Microsoft Visual C++-Umgebung verwenden.

**So debuggen Sie eine Visual Basic Komponente in der Visual C++-Umgebung**

1.  Öffnen Sie in Visual Basic 6.0 das Visual Basic Projekt, das Sie debuggen möchten.

2.  Klicken Sie im Menü **Datei** auf **Make YourProject.dll**.

3.  Klicken Sie im Dialogfeld **Make Project (Project** erstellen) auf **Optionen**.

4.  Klicken Sie im Dialogfeld **Project Eigenschaften** auf der Registerkarte **Kompilieren** auf **In nativen Code kompilieren** und **keine Optimierung,** und aktivieren Sie das Kontrollkästchen **Symbolische Debuginformationen erstellen.**

5.  Klicken Sie auf **OK** und dann erneut auf **OK,** um das Projekt zu kompilieren.

6.  Verschieben Sie die kompilierte DLL an den Speicherort, an dem COM+-Anwendungen normalerweise installiert sind.

    > [!Note]  
    > Wenn Sie die DLL nicht verschieben, erhalten Sie möglicherweise eine Fehlermeldung, die Sie darüber informiert, dass symbolische Debuginformationen für die DLL nicht gefunden werden konnten. Wenn Sie Probleme haben, den Debugger an Haltepunkten in ihrer Komponente anzuhalten, vergewissern Sie sich, dass sich die DLL im Standardpaketverzeichnis befindet, löschen Sie die Komponente aus ihrem Paket, und fügen Sie die Komponente erneut hinzu.

     

7.  Starten Sie Visual C++.

8.  Klicken Sie im Menü **Datei** auf **Arbeitsbereich öffnen.**

9.  Legen Sie im Dialogfeld **Arbeitsbereich öffnen** die Option Dateien **vom Typ** auf Alle **Dateien( . \* \* )** fest, wählen Sie Ihre kompilierte Komponente aus, und klicken Sie auf **Öffnen.**

10. Klicken Sie im Menü **Datei** auf **Öffnen** (nicht **Arbeitsbereich öffnen),** und öffnen Sie das Visual Basic Modul (.bas), das Formular (FRM) oder die Klasse (CLS), die Sie debuggen möchten.

11. Klicken Sie im **Menü Project** auf **Einstellungen**.

12. Wählen Sie im Dialogfeld **Project Einstellungen** auf der Registerkarte **Debuggen** im Feld **Kategorie** die Option **Allgemein** aus.

13. Geben Sie im Feld **Ausführbare Datei für Debugsitzung** den vollqualifizierten Pfad für Dllhost.exe ein, gefolgt von einem Argument, das die Prozess-ID der COM+-Anwendung angibt, die die Komponente enthält. Sie finden die Prozess-ID auf der Registerkarte **Allgemein** des Dialogfelds **Eigenschaften** der COM+-Anwendung. Es folgt ein Beispiel: C: \\ Winnt \\ System32 \\Dllhost.exe /ProcessID:{ <processID> }.

14. Klicken Sie auf **OK**.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM+ Visual Basic Debugunterstützung im Vergleich zu MTS](com--visual-basic-debugging-support-contrasted-with-mts.md)
</dt> <dt>

[Debuggen in der Visual Basic-IDE](debugging-in-the-visual-basic-ide.md)
</dt> </dl>

 

 




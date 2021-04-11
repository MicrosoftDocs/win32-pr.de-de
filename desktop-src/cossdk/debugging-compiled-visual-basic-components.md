---
description: Wenn Sie in vielen Fällen nur einen Teil der Komponenten Funktionen in der Microsoft Visual Basic Umgebung debuggen können, gibt es Situationen, in denen Sie Komponenten debuggen müssen, die mit Visual Basic erstellt wurden, nachdem Sie kompiliert wurden. Da dies in der Visual Basic Umgebung nicht möglich ist, müssen Sie stattdessen die Microsoft Visual C++ Umgebung verwenden.
ms.assetid: a58c5884-3c2d-4699-8b19-277003912dfd
title: Debuggen kompilierter Visual Basic Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07b32a39f0f1c50e1da4c9534b40658838361225
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126710"
---
# <a name="debugging-compiled-visual-basic-components"></a>Debuggen kompilierter Visual Basic Komponenten

Wenn Sie in vielen Fällen nur einen Teil der Funktionalität Ihrer Komponente innerhalb der Microsoft Visual Basic Umgebung debuggen können, gibt es Situationen, in denen Sie Komponenten debuggen müssen, die mit Visual Basic erstellt wurden, nachdem Sie kompiliert wurden. Da dies in der Visual Basic Umgebung nicht möglich ist, müssen Sie stattdessen die Microsoft Visual C++ Umgebung verwenden.

**So debuggen Sie eine Visual Basic Komponente in der Visual C++-Umgebung**

1.  Öffnen Sie in Visual Basic 6,0 das Visual Basic Projekt, das Sie debuggen möchten.

2.  Klicken Sie im Menü **Datei** auf **YourProject.dllerstellen**.

3.  Klicken Sie im Dialogfeld **Projekt erstellen** auf **Optionen**.

4.  Klicken Sie im Dialogfeld **Projekteigenschaften** auf der Registerkarte **Kompilieren** auf **in systemeigenen Code kompilieren** und dann auf **keine Optimierung** , und aktivieren Sie das Kontrollkästchen **symbolische Debuginformationen erstellen** .

5.  Klicken Sie auf **OK**, und klicken Sie dann erneut auf **OK** , um das Projekt zu kompilieren.

6.  Verschieben Sie die kompilierte DLL an den Speicherort, an dem com+-Anwendungen normalerweise installiert sind.

    > [!Note]  
    > Wenn Sie die dll nicht verschieben, erhalten Sie möglicherweise eine Fehlermeldung, die Sie darüber informiert, dass keine symbolischen Debuginformationen für die dll gefunden werden konnten. Wenn Sie Probleme haben, den Debugger an Haltepunkten in der Komponente anzuhalten, vergewissern Sie sich, dass sich die dll im Standardpaket Verzeichnis befindet, löschen Sie die Komponente aus dem zugehörigen Paket, und fügen Sie die Komponente erneut hinzu.

     

7.  Starten Sie Visual C++.

8.  Klicken Sie im Menü **Datei** auf **Arbeitsbereich öffnen**.

9.  Legen Sie im Dialogfeld **Arbeitsbereich öffnen** den **Dateityp** auf **alle Dateien ( \* . \* )** fest, wählen Sie die kompilierte Komponente aus, und klicken Sie auf **Öffnen**.

10. Klicken Sie im Menü **Datei** auf **Öffnen** (nicht **Arbeitsbereich öffnen**), und öffnen Sie das Visual Basic Modul (Bas), das Formular (. frm) oder die Klasse (. CLS), das Sie debuggen möchten.

11. Klicken Sie im Menü **Projekt** auf **Einstellungen**.

12. Wählen Sie im Dialogfeld **Projekteinstellungen** auf der Registerkarte **Debuggen** die Option **Allgemein** im Feld **Kategorie** aus.

13. Geben Sie im Feld **ausführbare Datei für Debugsitzung** den voll qualifizierten Pfad für Dllhost.exe ein, gefolgt von einem Argument, das die Prozess-ID der com+-Anwendung angibt, die die Komponente enthält. Die Prozess-ID finden Sie auf der Registerkarte **Allgemein** im Dialogfeld **Eigenschaften** der com+-Anwendung. Im folgenden finden Sie ein Beispiel: C: \\ Winnt \\ system32 \\Dllhost.exe/ProcessID: { <processID> }.

14. Klicken Sie auf **OK**.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Com+-Visual Basic Debugunterstützung im Vergleich zu MTS](com--visual-basic-debugging-support-contrasted-with-mts.md)
</dt> <dt>

[Debuggen in der Visual Basic IDE](debugging-in-the-visual-basic-ide.md)
</dt> </dl>

 

 




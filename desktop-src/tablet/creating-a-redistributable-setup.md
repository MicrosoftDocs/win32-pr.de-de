---
description: Um eine ink-fähige Anwendung an Computer zu verteilen, auf denen weder Windows Vista noch Windows XP Tablet PC Edition 2005 ausgeführt wird (d. h. Computer mit Windows XP, Windows Server 2003 oder Windows 2000), müssen Sie die erforderlichen Mergemodule in Das Setup ein schließen.
ms.assetid: 97515703-0bf4-4230-ae35-181b48b70c40
title: Erstellen eines redistributable-Setups
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80bdd63a00f1f4245ea83173e1a7e609094fe30e5357f5e1ebf3d6da63182cde
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119936870"
---
# <a name="creating-a-redistributable-setup"></a>Erstellen eines redistributable-Setups

Um eine ink-fähige Anwendung an Computer zu verteilen, auf denen weder Windows Vista noch Windows XP Tablet PC Edition 2005 ausgeführt wird (d. h. Computer mit Windows XP, Windows Server 2003 oder Windows 2000), müssen Sie die erforderlichen Mergemodule in Das Setup ein schließen.

Das Mergemodul Mstpcrt.msm enthält alle Dateien, Ressourcen, Registrierungseinträge und Setuplogik, die erforderlich sind, damit der Windows-Installer die freigegebenen Dateien installiert, die andere Plattformen zum Ausführen nicht verwalteter Anwendungen benötigen, die für den Tablet PC entwickelt wurden. Mstpcrt.msm wird von Windows Installer-Dateien (.msi) verwendet. Für Anwendungen, die das [**InkDivider-Objekt**](inkdivider-class.md) verwenden, müssen Sie auch InkDiv.msm neu verteilen. Für Anwendungen, die verwaltete Komponenten verwenden, müssen Sie auch die Mergemoduldateien für diese verwalteten Komponenten enthalten.

In der folgenden Tabelle werden die Mergemoduldateien beschrieben, die im Windows XP Tablet PC Edition Software Development Kit (SDK) enthalten sind.



| Redistributable Merge-Modul | BESCHREIBUNG                                                                                                                    | Dateien                                                       |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| InkDiv.msm<br/>        | Installiert die nicht verwaltete Version des [**InkDivider-Objekts.**](inkdivider-class.md)<br/>                                | InkDiv.dll<br/>                                       |
| Mstpcrt.msm<br/>       | Installiert die nicht verwalteten Komponenten der Tablet PC Platform Version 1.0.<br/>                                            | Gdiplus.dll, InkEd.dll, Tpcps.dll, Wisptis.exe<br/>   |
| Msvcp60.msm<br/>       | Installiert Komponenten der Microsoft Visual C++ Runtime.<br/>                                                            | Msvcp60.dll<br/>                                      |
| Msvcrt.msm<br/>        | Installiert Komponenten der Microsoft Visual C-Runtime.<br/>                                                              | Msvcrt.dll<br/>                                       |
| Tpcman17.msm<br/>      | Installiert die verwalteten Komponenten der Tablet PC Platform Runtime. Erfordert, dass die Datei mstpcrt.msm installiert ist.<br/> | Microsoft.Ink.dll, Microsoft.Ink.resources.dll<br/>   |
| iaCOM.msm<br/>         | Installiert die Automation-Komponenten der InkAnalysis-API.<br/>                                                          | IACom.dll<br/>                                        |
| iacore.msm<br/>        | Installiert die Basisklassenkomponenten der InkAnalysis-API.<br/>                                                          | IACore.dll<br/> IALoader.dll<br/>               |
| IAWinFrm.msm<br/>      | Installiert die Komponenten der verwalteten Bibliothek der InkAnalysis-API.<br/>                                                     | Microsoft.Ink.Analysis.dll<br/>                       |
| IAWinFX.msm<br/>       | Installiert die Windows Presentation Foundation der InkAnalysis-API.<br/>                                     | IAWinFX.dll<br/>                                      |
| journal.msm<br/>       | Installiert die Komponenten des Journallesers.<br/>                                                                             | Journal.dll<br/> Microsoft.ink.journal.dll<br/> |
| rtscom.msm<br/>        | Installiert die Automation-Komponenten des StylusInput-Namespace.<br/>                                                    | Rtscom.dll<br/>                                       |



 

> [!Note]  
> Um die Funktionen der Microsoft .NET Framework verwenden zu können, die in Mergemodulen für verwaltete Komponenten enthalten sind, müssen Sie Service Pack 2 des Frameworks auf dem Zielcomputer installiert haben.

 

## <a name="reduced-feature-set"></a>Reduzierter Funktionssatz

Ink-fähige Anwendungen behandeln Mausereignisse als Stiftbewegungen, um die Arbeit mit einem Tablettstift zu simulieren. Benutzer können Ink-, Ink- und Ink-Dokumente hinzufügen und speichern. Erkennungen und Gesten sind jedoch nur für Benutzer verfügbar, die Windows XP Tablet PC Edition ausführen.

Mstpcrt.msm enthält Windows Journal- oder Tablet PC-Eingabebereich nicht.

Das [**PenInputPanel-Objekt**](peninputpanel-class.md) funktioniert nicht auf Betriebssystemen außer Windows XP Tablet PC Edition.

## <a name="deployment"></a>Bereitstellung

> [!Note]  
> Wenn Ihre Anwendung verwalteten Code verwendet, müssen Sie auch das Framework bereitstellen. Das Framework muss installiert sein, bevor ihre verwalteten Assemblys für Den Tablet PC installiert werden.

 

So schließen Sie Mstpcrt.msm in ein Microsoft Visual Studio .NET-Setupprojekt ein:

1.  Wählen Sie im Projektmappen-Explorer Setupprojekt aus.
2.  Klicken Sie Project Menü auf **Hinzufügen** und dann auf **Modul zusammenführen.**
    > [!Note]  
    > Sie können das  Dialogfeld Module hinzufügen auch erreichen, indem Sie im Projektmappen-Explorer mit der rechten Maustaste auf den Projektnamen des Installationsprogramms klicken, auf Hinzufügen klicken und dann **Modul zusammenführen auswählen.**

     

3.  Navigieren Sie **im Dialogfeld Module** hinzufügen zu , und wählen Sie **Mstpcrt.msm aus.**
4.  Klicken Sie auf **Öffnen**.

Mstpcrt.msm wird Ihrem Setupprojekt hinzugefügt und im Fenster Projektmappen-Explorer angezeigt.

Windows Das Installationsprogramm fügt die im Mergemodul enthaltenen Dateien dem Ordner Programme hinzu. Um diese Dateien verwenden zu können, müssen Endbenutzer mit einem Konto angemeldet sein, das Zugriff auf den Ordner Programme hat.

> [!Note]  
> Sie müssen der [Installationssequenz Aktionen selfRegModules Action](../msi/selfregmodules-action.md) und [SelfUnregModules Action](../msi/selfunregmodules-action.md) hinzufügen. Die [Aktionen MsiPublishAssemblies Action](../msi/msipublishassemblies-action.md) und [MsiUnpublishAssemblies Action](/windows/desktop/Msi/msiunpublishassemblies-action) erhalten ihre Reihenfolge in der Installationssequenz von diesen Aktionen.

 

 


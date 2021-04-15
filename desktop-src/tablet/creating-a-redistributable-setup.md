---
description: Zum Verteilen einer frei Hand fähigen Anwendung auf Computer, auf denen entweder Windows Vista oder Windows XP Tablet PC Edition 2005 (d. h. Computer mit Windows XP, Windows Server 2003 oder Windows 2000) nicht ausgeführt wird, müssen Sie die erforderlichen Mergemodule in das Setup einschließen.
ms.assetid: 97515703-0bf4-4230-ae35-181b48b70c40
title: Erstellen eines verteilbaren Setups
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1ad9b9ec8b10032d4a2bb44cca52e5c2f4178b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524384"
---
# <a name="creating-a-redistributable-setup"></a>Erstellen eines verteilbaren Setups

Zum Verteilen einer frei Hand fähigen Anwendung auf Computer, auf denen entweder Windows Vista oder Windows XP Tablet PC Edition 2005 (d. h. Computer mit Windows XP, Windows Server 2003 oder Windows 2000) nicht ausgeführt wird, müssen Sie die erforderlichen Mergemodule in das Setup einschließen.

Das Mergemodul mstpcrt. msm enthält alle Dateien, Ressourcen, Registrierungseinträge und Setup Logik, die erforderlich sind, um zu Windows Installer, die freigegebenen Dateien zu installieren, die andere Plattformen benötigen, um nicht verwaltete Anwendungen auszuführen, die für den Tablet PC entwickelt wurden. Mstpcrt. msm wird von Windows Installer Dateien (. msi) genutzt. Für Anwendungen, die das [**InkDivider**](inkdivider-class.md) -Objekt verwenden, müssen Sie auch inkdiv. msm neu verteilen. Für Anwendungen, die verwaltete Komponenten verwenden, müssen Sie auch die Mergemoduldateien für diese verwalteten Komponenten einschließen.

In der folgenden Tabelle werden die Mergemoduldateien beschrieben, die im Lieferumfang des Windows XP Tablet PC Edition SDK (Software Development Kit) enthalten sind.



| Verteilbares Mergemodul | BESCHREIBUNG                                                                                                                    | Dateien                                                       |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| Inkdiv. msm<br/>        | Installiert die nicht verwaltete Version des [**InkDivider**](inkdivider-class.md) -Objekts.<br/>                                | InkDiv.dll<br/>                                       |
| Mstpcrt. msm<br/>       | Installiert die nicht verwalteten Komponenten der Tablet PC Platform-Version 1,0.<br/>                                            | Gdiplus.dll, InkEd.dll Tpcps.dll, Wisptis.exe<br/>   |
| Msvcp60. msm<br/>       | Installiert Komponenten der Microsoft Visual C++ Laufzeit.<br/>                                                            | Msvcp60.dll<br/>                                      |
| Msvcrt. msm<br/>        | Installiert Komponenten der Microsoft Visual C-Laufzeit.<br/>                                                              | Msvcrt.dll<br/>                                       |
| Tpcman17. msm<br/>      | Installiert die verwalteten Komponenten der Tablet PC Platform-Laufzeit. Erfordert, dass die Datei mstpcrt. msm installiert ist.<br/> | Microsoft.Ink.dll Microsoft.Ink.resources.dll<br/>   |
| iacom. msm<br/>         | Installiert die Automatisierungskomponenten der InkAnalysis-API.<br/>                                                          | IACom.dll<br/>                                        |
| IACore. msm<br/>        | Installiert die Basisklassen Komponenten der InkAnalysis-API.<br/>                                                          | IACore.dll<br/> IALoader.dll<br/>               |
| Iawinfrm. msm<br/>      | Installiert die verwalteten Bibliotheks Komponenten der InkAnalysis-API.<br/>                                                     | Microsoft.Ink.Analysis.dll<br/>                       |
| IAWinFX. msm<br/>       | Installiert die Windows Presentation Foundation Komponenten der InkAnalysis-API.<br/>                                     | IAWinFX.dll<br/>                                      |
| Journal. msm<br/>       | Installiert die Journal Leser-Komponenten.<br/>                                                                             | Journal.dll<br/> Microsoft.ink.journal.dll<br/> |
| rzcom. msm<br/>        | Installiert die Automatisierungskomponenten des StylusInput-Namespace.<br/>                                                    | Rtscom.dll<br/>                                       |



 

> [!Note]  
> Um die Funktionalität des Microsoft .NET Frameworks zu verwenden, das in Mergemodulen für verwaltete Komponenten enthalten ist, muss Service Pack 2 des Frameworks auf dem Bereitstellungs Zielcomputer installiert sein.

 

## <a name="reduced-feature-set"></a>Reduzierte Funktionsgruppe

Frei Hand aktivierte Anwendungen behandeln Mausereignisse als Stift Bewegungen, um die Arbeit mit einem Tablettstift zu simulieren. Benutzer können frei Hand Eingaben hinzufügen, frei Hand Eingaben löschen und frei Hand Dokumente speichern. Für andere Benutzer als Windows XP Tablet PC Edition sind jedoch keine Erkennung und Gesten verfügbar.

Mstpcrt. msm umfasst keinen Windows Journal-oder Tablet PC-Eingabebereich.

Das Objekt " [**pinputpanel**](peninputpanel-class.md) " funktioniert nicht auf Betriebssystemen außer Windows XP Tablet PC Edition.

## <a name="deployment"></a>Bereitstellung

> [!Note]  
> Wenn in Ihrer Anwendung verwalteter Code verwendet wird, müssen Sie auch das-Framework bereitstellen. Das Framework muss installiert werden, bevor die von Tablet PC verwalteten Assemblys installiert werden.

 

So fügen Sie "mstpcrt. msm" in ein Microsoft Visual Studio .NET-Setup-Projekt ein:

1.  Wählen Sie in der Projektmappen-Explorer das Setup-Projekt aus.
2.  Klicken Sie im Menü Projekt auf **Hinzufügen**, und klicken Sie dann auf **Modul zusammenführen**.
    > [!Note]  
    > Sie können auch das Dialogfeld **Module hinzufügen** aufrufen, indem Sie im Projektmappen-Explorer mit der rechten Maustaste auf den Namen des Installations Projekts klicken, auf **Hinzufügen** klicken und dann **Modul zusammenführen** auswählen.

     

3.  Navigieren Sie im Dialogfeld **Module hinzufügen** zu, und wählen Sie **mstpcrt. msm** aus.
4.  Klicken Sie auf **Öffnen**.

Mstpcrt. msm wird dem Setup-Projekt hinzugefügt und im Fenster Projektmappen-Explorer angezeigt.

Windows Installer fügt dem Ordner "Programme" die Dateien hinzu, die im Mergemodul enthalten sind. Um diese Dateien verwenden zu können, müssen Endbenutzer mit einem Konto angemeldet sein, das Zugriff auf den Ordner "Programme" hat.

> [!Note]  
> Sie müssen der Installations Sequenz [SelfRegModules Action](../msi/selfregmodules-action.md) -und [selfunregmodules-Aktions](../msi/selfunregmodules-action.md) Aktionen hinzufügen. Die Aktionen [msipublishassemblys](../msi/msipublishassemblies-action.md) und [msiunpublishassemblys](/windows/desktop/Msi/msiunpublishassemblies-action) erhalten ihre Reihenfolge in der Installations Sequenz dieser Aktionen.

 

 


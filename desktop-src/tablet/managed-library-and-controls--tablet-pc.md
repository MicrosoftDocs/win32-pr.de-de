---
description: Zum Erstellen von Tablet PC-Anwendungen in C \# und Visual Basic .NET muss Ihr Projekt in Microsoft Visual Studio .net einen Verweis auf die von Tablet PC verwalteten Bibliotheksassemblys enthalten. Dies ermöglicht den Zugriff auf das verwaltete Objektmodell und die Steuerelemente.
ms.assetid: d9c491c9-d341-4189-9a41-45c4d78322fa
title: Verwaltete Bibliothek und Steuerelemente (Tablet PC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7299a1df0cc1b64d650ec748eb2de01ad4b776f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366117"
---
# <a name="managed-library-and-controls-tablet-pc"></a>Verwaltete Bibliothek und Steuerelemente (Tablet PC)

Zum Erstellen von Tablet PC-Anwendungen in C \# und Visual Basic .NET muss Ihr Projekt in Microsoft Visual Studio .net einen Verweis auf die von Tablet PC verwalteten Bibliotheksassemblys enthalten. Dies ermöglicht den Zugriff auf das verwaltete Objektmodell und die Steuerelemente.

## <a name="microsoft-visual-c-and-visual-basicnet"></a>Microsoft Visual C \# und Visual Basic.net

In Windows Vista werden die von Tablet PC verwalteten Bibliotheksassemblys standardmäßig in zwei Verzeichnissen installiert:

-   <systemdrive>: \\ Programmdateien \\ Allgemeine Dateien \\ Microsoft Shared \\ Ink Directory
-   <systemdrive>: \\ Programme \\ Microsoft sdert \\ Windows \\ v 6.0 \\ bin

So fügen Sie einen Verweis auf die von Tablet PC Platform verwalteten Bibliotheken in Microsoft Visual Studio .net hinzu:

1.  Öffnen Sie das Visual Studio .net-Projekt.
2.  Klicken Sie im Menü **Projekt** auf **Verweis hinzufügen**.
3.  Wählen Sie auf der Registerkarte **.net** im Dialogfeld **Verweis hinzufügen** in der Liste Komponenten die Option **Microsoft Tablet PC-API** aus.
4.  Klicken Sie auf **auswählen**, und klicken Sie dann auf **OK**.

So fügen Sie einen Verweis auf die APIs für die frei Hand Analyse in Visual Studio .net hinzu:

1.  Öffnen Sie das Microsoft Visual Studio .net-Projekt.
2.  Klicken Sie im Menü **Projekt** auf **Verweis hinzufügen**.
3.  Wählen Sie auf der Registerkarte **.net** im Dialogfeld **Verweis hinzufügen** in der Liste Komponenten die Option **Microsoft Tablet PC Ink Analysis verwaltete Bibliothek** aus.
4.  Klicken Sie auf **auswählen**, und klicken Sie dann auf **OK**.

> [!Note]  
> Wenn Sie Anwendungen kompilieren, die Microsoft. Ink in Visual Studio 2005 verwenden, müssen Sie **Project**, Select **Properties**, **Build** und Set Platform Target = x86 auswählen. Diese Option ist in Microsoft Visual Studio Express Produkte nicht verfügbar.

 

 

 




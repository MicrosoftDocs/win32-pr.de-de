---
description: Um Tablet PC-Anwendungen in C und Visual Basic .NET zu erstellen, muss Ihr Projekt in Microsoft Visual Studio .NET einen Verweis auf die Assemblys der verwalteten \# Tablet PC-Bibliothek enthalten. Dies ermöglicht den Zugriff auf das verwaltete Objektmodell und die Steuerelemente.
ms.assetid: d9c491c9-d341-4189-9a41-45c4d78322fa
title: Verwaltete Bibliothek und Steuerelemente (Tablet PC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81b4096ba54d3cd882b3ee50469d94792b4a46ce
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884278"
---
# <a name="managed-library-and-controls-tablet-pc"></a>Verwaltete Bibliothek und Steuerelemente (Tablet PC)

Um Tablet PC-Anwendungen in C und Visual Basic .NET zu erstellen, muss Ihr Projekt in Microsoft Visual Studio .NET einen Verweis auf die Assemblys der verwalteten \# Tablet PC-Bibliothek enthalten. Dies ermöglicht den Zugriff auf das verwaltete Objektmodell und die Steuerelemente.

## <a name="microsoft-visual-c-and-visual-basicnet"></a>Microsoft Visual C \# und Visual Basic.NET

In Windows Vista werden die Assemblys der verwalteten Tablet PC-Bibliothek standardmäßig in zwei Verzeichnissen installiert:

-   &lt;&gt;systemdrive: Programme Common Files Microsoft Shared \\ \\ \\ \\ Ink directory
-   &lt;&gt;systemdrive: \\ Programme Microsoft \\ SDKs Windows \\ \\ v6.0 \\ Bin

So fügen Sie einen Verweis auf die verwalteten Bibliotheken der Tablet PC-Plattform in Microsoft Visual Studio .NET hinzu:

1.  Öffnen Sie Visual Studio .NET-Projekt.
2.  Klicken Sie im Menü **Projekt** auf **Verweis hinzufügen** .
3.  Wählen Sie **auf der Registerkarte .NET** im **Dialogfeld Verweis** hinzufügen in der Komponentenliste Microsoft Tablet PC **API aus.**
4.  Klicken **Sie auf** Auswählen und dann auf **OK.**

So fügen Sie einen Verweis auf die Ink-Analyse-APIs in Visual Studio .NET hinzu:

1.  Öffnen Sie Microsoft Visual Studio .NET-Projekt.
2.  Klicken Sie im Menü **Projekt** auf **Verweis hinzufügen** .
3.  Wählen Sie auf der  **Registerkarte .NET** im Dialogfeld Verweis hinzufügen in der Komponentenliste Microsoft Tablet PC **Ink Analysis Managed Library aus.**
4.  Klicken **Sie auf** Auswählen und dann auf **OK.**

> [!Note]  
> Beim Kompilieren von Anwendungen, die Microsoft.Ink in Visual Studio 2005 verwenden, müssen Sie **Project** auswählen, Eigenschaften **auswählen,** **Erstellen** auswählen und Plattformziel=x86 festlegen. Diese Option ist in den Microsoft Visual Studio Express nicht verfügbar.

 

 

 




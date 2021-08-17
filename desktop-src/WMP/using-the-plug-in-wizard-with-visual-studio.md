---
title: Verwenden des Plug-In-Assistenten mit Visual Studio
description: Verwenden des Plug-In-Assistenten mit Visual Studio
ms.assetid: 5d5521b7-5cbc-4259-92b1-a7250853fa2e
keywords:
- Windows Media Player Plug-Ins,Visual Studio
- Plug-Ins, Visual Studio
- Erstellen von Plug-Ins, Visual Studio
- Windows Media Player Plug-In-Assistent, Visual Studio
- Visual Studio,Windows Media Player-Plug-In-Assistent
- Plug-In-Assistent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1534d084d2c57d3546427db59274d1bd135bc66e8bf396906ff7776cae9a370f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134333"
---
# <a name="using-the-plug-in-wizard-with-visual-studio"></a>Verwenden des Plug-In-Assistenten mit Visual Studio

Nachdem Sie die erforderlichen Komponenten installiert haben, können Sie schnell ein Plug-In erstellen, das als Ausgangspunkt dient. Die folgenden Schritte führen Sie weiter.

1.  Starten Sie Microsoft Visual Studio.
2.  Zeigen Sie **im Menü** Datei auf **Neu,** und klicken Sie dann **Project**.
3.  Wählen **Project Typen** die Option Visual C++ Projekte **aus.**
4.  Wählen **Sie unter** Vorlagen die Windows Media Player **Plug-In-Assistenten aus.**
5.  Geben Sie einen Namen für das Projekt ein.
6.  Geben Sie einen Speicherort für Ihr Projekt ein. Dies ist der Ordner, in den Ihre Projektdateien kopiert werden.
7.  Klicken Sie **auf OK,** um den Assistenten zu starten.
8.  Wählen Sie den Typ des Plug-Ins aus, das Sie erstellen möchten.
9.  Schließen Sie alle verbleibenden Dialogfelder im Assistenten ab.
10. Verwenden Sie Visual Studio Entwicklungsumgebung, um Ihr Projekt zu erstellen.
    > [!Note]  
    > In Windows Vista und höher wird das Projekt nur erfolgreich erstellt, wenn Sie Visual Studio mit einem vollständigen Administratorzugriffstoken ausführen. Klicken Sie mit der rechten Maustaste auf Visual Studio Symbol, und klicken Sie **auf Als Administrator ausführen.**

     

Bevor Sie versuchen, das Projekt zu erstellen, müssen Sie Ihre Entwicklungsumgebung so konfigurieren, dass sie auf die Ordner include und lib verweisen, in denen Sie das Windows INSTALLIERT haben. Ihr Compiler und Linker benötigen Zugriff auf einige der Dateien in diesen Ordnern.

Wenn Sie das Visual Studio Registration-Hilfsprogramm aus dem Windows SDK ausführen, wurde Ihre Entwicklungsumgebung wahrscheinlich bereits so konfiguriert, dass sie auf die Ordner Windows SDK Include und Lib verweisen kann. Andernfalls müssen Sie Ihre Entwicklungsumgebung manuell konfigurieren.

Um die Visual Studio manuell zu konfigurieren, verwenden Sie die folgenden Schritte.

1.  Klicken Sie im Menü **Extras** auf **Optionen**.
2.  Klicken **Sie auf Projekte und Projektlösungen**, und klicken Sie dann VC++ Verzeichnisse **.**
3.  Klicken **Sie unter Verzeichnisse für anzeigen** auf Dateien **oder** **Bibliotheksdateien enthalten.**
4.  Fügen Sie die Verzeichnisse für die erforderlichen Dateien hinzu.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen eines Plug-Ins](building-a-plug-in.md)
</dt> </dl>

 

 





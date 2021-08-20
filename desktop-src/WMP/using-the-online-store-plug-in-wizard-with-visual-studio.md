---
title: Verwenden des Online-Store-Plug-In-Assistenten mit Visual Studio
description: Verwenden des Online-Store-Plug-In-Assistenten mit Visual Studio
ms.assetid: 0bf670cd-897d-4cd6-ae95-ae16b2dacc96
keywords:
- Windows Media Player Onlineshops, Plug-Ins
- Onlineshops, Plug-Ins
- Geben Sie 1 Onlineshops und Plug-Ins ein.
- Windows Media Player Onlineshops, Plug-In-Assistent
- Onlineshops, Plug-In-Assistent
- Typ 1 Onlineshops, Plug-In-Assistent
- Windows Media Player Onlineshops,Visual Studio
- Onlineshops,Visual Studio
- Geben Sie 1 Onlineshops ein, Visual Studio
- Plug-Ins, Windows Media Player Onlineshops
- Plug-Ins, Onlineshops
- Plug-Ins, Geben Sie 1 Onlineshop ein.
- Plug-Ins, Visual Studio
- Plug-Ins, Plug-In-Assistent
- Windows Media Player Plug-Ins, Geben Sie 1 Onlineshops ein.
- Windows Media Player Plug-Ins, Onlineshops
- Windows Media Player-Plug-Ins, Windows Media Player Onlineshops
- Windows Media Player-Plug-Ins, Visual Studio
- Windows Media Player Plug-Ins, Plug-In-Assistent
- Assistent für Visual Studio,Windows Media Player Onlineshops
- Plug-In-Assistent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd53a1b83f817e4cfcc7dede80361f56f46ea41da8730f4396330c12af05c73a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118830681"
---
# <a name="using-the-online-store-plug-in-wizard-with-visual-studio"></a>Verwenden des Online-Store-Plug-In-Assistenten mit Visual Studio

Nachdem Sie die erforderlichen Komponenten installiert haben, können Sie schnell ein Plug-In erstellen, das als Ausgangspunkt dient. Die folgenden Schritte führen Sie durch:

1.  Starten Sie Microsoft Visual Studio.
2.  Zeigen Sie im Menü **Datei** auf **Neu,** und klicken Sie dann auf **Project**.
3.  Klicken Sie **in Project Typen** auf Visual C++ **Projekte**.
4.  Klicken Sie unter **Vorlagen** auf **Windows Media Player Onlineshop-Assistent**.
5.  Geben Sie einen Namen für das Projekt ein.
6.  Geben Sie einen Speicherort für Ihr Projekt ein. Dies ist der Ordner, in den Ihre Projektdateien kopiert werden.
7.  Klicken Sie auf **OK,** um den Assistenten zu starten.
8.  Wählen Sie **Typ 1 (Deep Integration)** aus, und klicken Sie auf **Weiter.**
9.  Geben Sie einen Anzeigenamen und einen Inhaltsverteiler ein. Klicken Sie auf **Fertig stellen**.
10. Verwenden Sie die Visual Studio Entwicklungsumgebung, um Ihr Projekt zu erstellen.
    > [!Note]  
    > In Windows Vista und höher wird das Projekt nur erfolgreich erstellt, wenn Sie Visual Studio mit einem vollständigen Administratorzugriffstoken ausführen. Klicken Sie mit der rechten Maustaste auf den Visual Studio Namen oder Symbol, und klicken Sie auf **Als Administrator ausführen.**

     

Bevor Sie versuchen, das Projekt zu erstellen, müssen Sie Ihre Entwicklungsumgebung so konfigurieren, dass sie auf die Ordner include und lib verweist, in denen Sie das Windows SDK installiert haben. Ihr Compiler und Linker benötigen Zugriff auf einige der Dateien in diesen Ordnern.

Wenn Sie das Visual Studio Registration-Hilfsprogramm ausgeführt haben, das im Windows SDK enthalten ist, wurde Ihre Entwicklungsumgebung wahrscheinlich bereits so konfiguriert, dass sie auf die Ordner Windows SDK Include und Lib verweist. Andernfalls müssen Sie Ihre Entwicklungsumgebung manuell konfigurieren.

Um Visual Studio manuell zu konfigurieren, verwenden Sie die folgenden Schritte.

1.  Klicken Sie im Menü **Extras** auf Optionen.
2.  Klicken Sie auf **Projekte und Projektmappen** und dann auf **VC++ Verzeichnisse.**
3.  Klicken Sie unter **Verzeichnisse für anzeigen** auf Dateien oder **Bibliotheksdateien** **einschließen.**
4.  Fügen Sie die Verzeichnisse für die erforderlichen Dateien hinzu.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen des Plug-Ins für einen Typ 1 Online Store](building-the-plug-in-for-a-type-1-online-store.md)
</dt> </dl>

 

 





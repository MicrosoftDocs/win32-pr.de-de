---
title: Verwenden des Plug-in-Assistenten in Visual Studio
description: Verwenden des Plug-in-Assistenten in Visual Studio
ms.assetid: 5d5521b7-5cbc-4259-92b1-a7250853fa2e
keywords:
- Windows Media Player-Plug-ins, Visual Studio
- Plug-ins, Visual Studio
- Entwickeln von Plug-ins, Visual Studio
- Windows Media Player-Plug-in-Assistent, Visual Studio
- Visual Studio, Windows Media Player-Plug-in-Assistent
- Plug-in-Assistent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c7f7db9bdc2a99a42f60c2faf38605e50e7dd3e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310396"
---
# <a name="using-the-plug-in-wizard-with-visual-studio"></a>Verwenden des Plug-in-Assistenten in Visual Studio

Nachdem Sie die erforderlichen Komponenten installiert haben, können Sie schnell ein Plug-in erstellen, das als Ausgangspunkt fungiert. Die folgenden Schritte führen Sie durch.

1.  Starten Sie Microsoft Visual Studio.
2.  Zeigen Sie im Menü **Datei** auf **neu** , und klicken Sie dann auf **Projekt**.
3.  Wählen Sie unter **Projekttypen** die Option **Visual C++ Projekte** aus.
4.  Wählen Sie unter **Vorlagen** die Option **Windows Media Player-Plug-in-Assistent** aus.
5.  Geben Sie einen Namen für das Projekt ein.
6.  Geben Sie einen Speicherort für das Projekt ein. Dies ist der Ordner, in den die Projektdateien kopiert werden.
7.  Klicken Sie auf **OK** , um den Assistenten zu starten.
8.  Wählen Sie den Typ des Plug-ins aus, das Sie erstellen möchten.
9.  Vervollständigen Sie alle verbleibenden Dialogfelder im Assistenten.
10. Verwenden Sie die Visual Studio-Entwicklungsumgebung, um Ihr Projekt zu erstellen.
    > [!Note]  
    > In Windows Vista und höher wird das Projekt nicht erfolgreich erstellt, es sei denn, Sie führen Visual Studio mit einem vollen Administrator Zugriffs Token aus. Klicken Sie mit der rechten Maustaste auf den Namen oder das Symbol von Visual Studio, und klicken Sie auf **als Administrator ausführen**

     

Bevor Sie versuchen, das Projekt zu erstellen, stellen Sie sicher, dass Sie Ihre Entwicklungsumgebung so konfigurieren, dass Sie auf die Ordner include und lib verweist, in denen Sie die Windows SDK installiert haben. Der Compiler und Linker benötigen Zugriff auf einige der Dateien in diesen Ordnern.

Wenn Sie das Visual Studio-Registrierungs Dienstprogramm ausgeführt haben, das in der Windows SDK enthalten ist, wurde die Entwicklungsumgebung wahrscheinlich bereits so konfiguriert, dass Sie auf die Ordner Windows SDK include und lib verweist. Andernfalls müssen Sie Ihre Entwicklungsumgebung manuell konfigurieren.

Führen Sie die folgenden Schritte aus, um Visual Studio manuell zu konfigurieren.

1.  Klicken Sie im Menü **Extras** auf **Optionen**.
2.  Klicken Sie auf **Projekte und Projekt** Mappen und dann auf **VC + +-Verzeichnisse**.
3.  Klicken Sie unter **Verzeichnisse anzeigen für** auf Dateien oder **Bibliotheksdateien** **einschließen** .
4.  Fügen Sie die Verzeichnisse für die erforderlichen Dateien hinzu.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufbauen eines Plug-ins](building-a-plug-in.md)
</dt> </dl>

 

 





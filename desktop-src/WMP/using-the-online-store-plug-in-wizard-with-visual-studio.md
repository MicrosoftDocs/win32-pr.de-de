---
title: Verwenden des Online Store-Plug-in-Assistenten mit Visual Studio
description: Verwenden des Online Store-Plug-in-Assistenten mit Visual Studio
ms.assetid: 0bf670cd-897d-4cd6-ae95-ae16b2dacc96
keywords:
- Windows Media Player Online Stores, Plug-ins
- Online Stores, Plug-ins
- Typ 1 Online Stores, Plug-ins
- Windows Media Player Online Stores, Plug-in-Assistent
- Online Stores, Plug-in-Assistent
- Typ 1 Online Stores, Plug-in-Assistent
- Windows Media Player Online Stores, Visual Studio
- Online Stores, Visual Studio
- Typ 1 Online Stores, Visual Studio
- Plug-ins, Windows Media Player Online Stores
- Plug-ins, Online Stores
- Plug-ins, Typ 1 Online Stores
- Plug-ins, Visual Studio
- Plug-ins, Plug-in-Assistent
- Windows Media Player-Plug-ins, geben Sie 1 Online Stores ein.
- Windows Media Player-Plug-ins, Online Stores
- Windows Media Player-Plug-ins, Windows Media Player Online Stores
- Windows Media Player-Plug-ins, Visual Studio
- Windows Media Player-Plug-ins, Plug-in-Assistent
- Visual Studio, Windows Media Player Online Stores-Assistent
- Plug-in-Assistent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0c9aadbb9cef4b44cb421bf8a4737cc408c5220
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337557"
---
# <a name="using-the-online-store-plug-in-wizard-with-visual-studio"></a>Verwenden des Online Store-Plug-in-Assistenten mit Visual Studio

Nachdem Sie die erforderlichen Komponenten installiert haben, können Sie schnell ein Plug-in erstellen, das als Ausgangspunkt fungiert. Die folgenden Schritte führen Sie durch:

1.  Starten Sie Microsoft Visual Studio.
2.  Zeigen Sie im Menü **Datei** auf **neu** , und klicken Sie dann auf **Projekt**.
3.  Klicken Sie unter **Projekttypen** auf **Visual C++ Projekte**.
4.  Klicken Sie unter **Vorlagen** auf **Windows Media Player Online Stores Wizard**.
5.  Geben Sie einen Namen für das Projekt ein.
6.  Geben Sie einen Speicherort für das Projekt ein. Dies ist der Ordner, in den die Projektdateien kopiert werden.
7.  Klicken Sie auf **OK** , um den Assistenten zu starten.
8.  Wählen Sie **Typ 1 (Deep Integration)** aus, und klicken Sie auf **weiter**.
9.  Geben Sie einen anzeigen Amen und einen Inhalts Verteiler ein. Klicken Sie auf **Fertig stellen**.
10. Verwenden Sie die Visual Studio-Entwicklungsumgebung, um Ihr Projekt zu erstellen.
    > [!Note]  
    > In Windows Vista und höher wird das Projekt nicht erfolgreich erstellt, es sei denn, Sie führen Visual Studio mit einem vollen Administrator Zugriffs Token aus. Klicken Sie mit der rechten Maustaste auf den Namen oder das Symbol von Visual Studio, und klicken Sie auf **als Administrator ausführen**

     

Bevor Sie versuchen, das Projekt zu erstellen, stellen Sie sicher, dass Sie Ihre Entwicklungsumgebung so konfigurieren, dass Sie auf die Ordner include und lib verweist, in denen Sie die Windows SDK installiert haben. Der Compiler und Linker benötigen Zugriff auf einige der Dateien in diesen Ordnern.

Wenn Sie das Visual Studio-Registrierungs Dienstprogramm ausgeführt haben, das in der Windows SDK enthalten ist, wurde die Entwicklungsumgebung wahrscheinlich bereits so konfiguriert, dass Sie auf die Ordner Windows SDK include und lib verweist. Andernfalls müssen Sie Ihre Entwicklungsumgebung manuell konfigurieren.

Führen Sie die folgenden Schritte aus, um Visual Studio manuell zu konfigurieren.

1.  Klicken Sie **im Menü Extras** auf Optionen.
2.  Klicken Sie auf **Projekte und Projekt** Mappen und dann auf **VC + +-Verzeichnisse**.
3.  Klicken Sie unter **Verzeichnisse anzeigen für** auf Dateien oder **Bibliotheksdateien** **einschließen** .
4.  Fügen Sie die Verzeichnisse für die erforderlichen Dateien hinzu.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwickeln des Plug-Ins für einen Typ-1-Online Shop](building-the-plug-in-for-a-type-1-online-store.md)
</dt> </dl>

 

 





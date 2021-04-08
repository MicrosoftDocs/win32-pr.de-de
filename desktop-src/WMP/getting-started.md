---
title: Einführung in das Windows Media Player SDK
description: Einführung in das Windows Media Player SDK
ms.assetid: 47c333dc-dad3-4430-a053-016d2c931f74
keywords:
- Windows Media Player Mobile, Plug-ins
- Windows Media Player Mobile, Benutzerschnittstellen-Plug-ins
- Mobile Windows Media Player-Plug-ins
- Plug-ins, Benutzeroberfläche
- Plug-ins, Windows Media Player Mobile
- Plug-Ins für Benutzeroberflächen, Windows Media Player Mobile
- UI-Plug-ins, Windows Media Player Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a962c1f815f820a0b2e8125872baf9d02e301dc
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739304"
---
# <a name="getting-started-with-the-windows-media-player-sdk"></a>Einführung in das Windows Media Player SDK

Zum Erstellen des Plug-Ins müssen Sie zuerst Microsoft Embedded Visual C++ 4,0 und Visual Studio 2003 installieren. Sie müssen auch das Pocket PC 2003 SDK oder das Smartphone 2003 SDK installieren, bei dem es sich um separate Downloads handelt. Zum Kompilieren und Ausführen des Projekts muss ein Pocket PC-oder Smartphone-Gerät mit dem Betriebssystem Windows Mobile 2003 Second Edition mit dem Entwicklungs Computer synchronisiert werden, indem Microsoft ActiveSync® 3.7.1 oder höher verwendet wird.

Da Benutzeroberflächen-Plug-Ins auf Windows Mobile-Geräten das gleiche Plug-in-Modell wie die Desktop Versionen verwenden, können Sie den Windows Media Player-Plug-in-Assistenten als Ausgangspunkt verwenden, um ein Plug-in für die Benutzeroberfläche zu erstellen, das mit Windows Media Player 10 Mobile verwendet werden kann.

Gehen Sie folgendermaßen vor, um den UI-Plug-in-Code zu erstellen:

1.  Öffnen Sie Visual Studio 2003, und starten Sie ein neues Projekt in Visual C++.
2.  Wählen Sie im Bereich **Vorlagen** die Option **Windows Media Player-Plug-in-Assistent** aus.
3.  Benennen Sie Ihr Projekt mit networkplugin, und klicken Sie auf **OK**.
4.  Wählen Sie **UI-Plug-in** , und klicken Sie auf **weiter**.
5.  Wählen Sie **Hintergrund** , und klicken Sie auf **weiter**.
6.  Klicken Sie auf **Weiter**, um den Assistenten zu beenden. Wenn Sie Ereignisse mit dem Plug-in überwachen möchten, müssen Sie vor dem Abschließen des Assistenten Ereignisse **lauschen** aktivieren. lesen Sie die Dokumentation für die **iwmpevents** -Schnittstelle, um herauszufinden, welche Ereignisse unter Windows Media Player 10 Mobile unterstützt werden.

Nachdem Sie den UI-Plug-in-Code erstellt haben, müssen Sie in Embedded Visual C++ 4,0 ein leeres Windows CE DLL-Projekt erstellen. Kopieren Sie dann die vom Assistenten generierten Quelldateien in dieses neue Projekt, damit Sie mit dem ARM4-Compiler kompiliert werden.

So erstellen Sie ein leeres Projekt

1.  Starten Sie ein neues Projekt in eingebettetem Visual C++, und wählen Sie dann im **Projekt** Bereich **WCE-Dynamic-Link Bibliothek** aus.
2.  Benennen Sie Ihr Projekt, und klicken Sie auf **OK**.
3.  Stellen Sie sicher, dass **ein leeres Windows CE DLL-Projekt** ausgewählt ist, und klicken Sie dann auf **Fertig** stellen.
4.  Klicken Sie auf das Menü Element **Projekt** .
5.  Wählen Sie **zu Projekt hinzufügen** aus, und klicken Sie dann auf **Dateien**.
6.  Wählen Sie die mit dem Plug-in-Assistenten erstellten C++-Dateien aus, und klicken Sie dann auf **OK**.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen eines Benutzeroberflächen-Plug-Ins für Windows Media Player 10 Mobile**](creating-a-user-interface-plug-in-for-windows-media-player-10-mobile.md)
</dt> <dt>

[**Iwmpevents-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents)
</dt> </dl>

 

 





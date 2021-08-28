---
title: Erste Schritte mit dem Windows Media Player SDK
description: Erste Schritte mit dem Windows Media Player SDK
ms.assetid: 47c333dc-dad3-4430-a053-016d2c931f74
keywords:
- Windows Media Player Mobil, Plug-Ins
- Windows Media Player Mobile Plug-Ins für die Benutzeroberfläche
- Windows Media Player Mobile Plug-Ins
- Plug-Ins, Benutzeroberfläche
- Plug-Ins, Windows Media Player Mobile
- Benutzeroberflächen-Plug-Ins, Windows Media Player Mobile
- Ui-Plug-Ins, Windows Media Player Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7c18157511364b4846b79b8f9a4e617ba7fe87a9f37535d5eaf112546dba28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117934570"
---
# <a name="getting-started-with-the-windows-media-player-sdk"></a>Erste Schritte mit dem Windows Media Player SDK

Zum Erstellen Ihres Plug-Ins müssen Sie zunächst Microsoft eMbedded Visual C++ 4.0 und Visual Studio 2003 installieren. Sie müssen auch das Pocket PC 2003 SDK oder das Smartphone 2003 SDK installieren, bei dem es sich um separate Downloads handelt. Zum Kompilieren und Ausführen des Projekts muss ein Pocket PC- oder Smartphonegerät, auf dem das Betriebssystem Windows Mobile 2003 Second Edition ausgeführt wird, mithilfe von Microsoft ActiveSync® 3.7.1 oder höher mit dem Entwicklungscomputer synchronisiert werden.

Da Benutzeroberflächen-Plug-Ins auf Windows Mobile-Geräten das gleiche Plug-In-Modell wie die Desktopversionen verwenden, können Sie den Windows Media Player-Plug-In-Assistenten als Ausgangspunkt für die Erstellung eines Ui-Plug-Ins im Hintergrund verwenden, das mit Windows Media Player 10 Mobile funktioniert.

Gehen Sie wie folgt vor, um Ui-Plug-In-Code zu erstellen:

1.  Öffnen Sie Visual Studio 2003, und starten Sie ein neues Projekt in Visual C++.
2.  Wählen Sie **Windows Media Player Plug-In-Assistenten** im Bereich **Vorlagen** aus.
3.  Nennen Sie Ihr Projekt NetworkPlugin, und klicken Sie auf **OK.**
4.  Wählen Sie **UI-Plug-In** aus, und klicken Sie auf **Weiter.**
5.  Wählen Sie **Hintergrund** aus, und klicken Sie auf **Weiter.**
6.  Klicken Sie auf **Weiter**, um den Assistenten zu beenden. Wenn Sie Ereignisse mit Ihrem Plug-In überwachen möchten, müssen Sie vor Abschluss des Assistenten auf **Ereignisse lauschen** überprüfen. Lesen Sie die Dokumentation für die **IWMPEvents-Schnittstelle,** um herauszufinden, welche Ereignisse auf Windows Media Player 10 Mobile unterstützt werden.

Nachdem Sie ihren Ui-Plug-In-Code erstellt haben, müssen Sie ein leeres Windows CE DLL-Projekt in eMbedded Visual C++ 4.0 erstellen. Kopieren Sie dann die vom Assistenten generierten Quelldateien in das neue Projekt, damit sie mit dem ARM4-Compiler kompiliert werden.

So erstellen Sie ein leeres Projekt

1.  Starten Sie ein neues Projekt in eMbedded Visual C++, und wählen Sie im Bereich **Projekte** die Option **WCE Dynamic-Link Library** aus.
2.  Nennen Sie Ihr Projekt, und klicken Sie auf **OK.**
3.  Stellen Sie sicher, dass **Ein leeres Windows CE DLL-Projekt** ausgewählt ist, und klicken Sie dann auf **Fertig stellen.**
4.  Klicken Sie auf das **Menüelement Project.**
5.  Wählen Sie **Hinzufügen aus, um Project**, und klicken Sie dann auf **Dateien.**
6.  Wählen Sie die C++-Dateien aus, die Sie mit dem Plug-In-Assistenten erstellt haben, und klicken Sie dann auf **OK.**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen eines Benutzeroberfläche-Plug-Ins für Windows Media Player 10 Mobile**](creating-a-user-interface-plug-in-for-windows-media-player-10-mobile.md)
</dt> <dt>

[**IWMPEvents-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents)
</dt> </dl>

 

 





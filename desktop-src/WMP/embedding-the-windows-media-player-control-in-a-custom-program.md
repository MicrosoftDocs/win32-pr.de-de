---
title: Einbetten des Windows Media Player-Steuer Elements in ein benutzerdefiniertes Programm
description: Einbetten des Windows Media Player-Steuer Elements in ein benutzerdefiniertes Programm
ms.assetid: 2a5f0cd7-e3fa-4d4f-9203-bcb13362c9ab
keywords:
- Windows Media Player, Einbetten des ActiveX-Steuer Elements
- Windows Media Player Objektmodell, Einbetten des ActiveX-Steuer Elements
- Objektmodell, Einbetten des ActiveX-Steuer Elements
- Windows Media Player ActiveX-Steuerelement, einbetten
- ActiveX-Steuerelement, einbetten
- Windows Media Player Mobile ActiveX-Steuerelement, einbetten
- Windows Media Player Mobile, Einbetten des ActiveX-Steuer Elements
- einbetten, benutzerdefinierte Programme
- benutzerdefiniertes programmieren
- einbetten, Visual Basic basierte Programme
- Visual Basic basierte Programm Einbettung
- einbetten, Manuelles Verwenden von com-Methoden
- manuelle Einbettung mithilfe von com-Methoden
- einbetten, C++-Programme
- C++-Programm Einbettung
- einbetten, Visual Studio-Programme
- Visual Studio, Programm Einbettung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 441678e4b8db51040e18d9d31d2af78db134f74b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036738"
---
# <a name="embedding-the-windows-media-player-control-in-a-custom-program"></a>Einbetten des Windows Media Player-Steuer Elements in ein benutzerdefiniertes Programm

Da das Windows Media Player ActiveX-Steuerelement auf der com-Technologie (Microsoft Component Object Model) basiert, können Sie es in Programme einbetten, die mit vielen verschiedenen Programmiersprachen geschrieben wurden. Das Windows Media Player-Steuerelement stellt eine einfache Möglichkeit dar, einem beliebigen Programm ausgereifte Funktionen für digitale Medien hinzuzufügen.

In Microsoft Visual Basic können Sie das Steuerelement der Toolbox für Steuerelemente hinzufügen, es auf einem Formular platzieren und die Steuerelement Eigenschaften im Eigenschaften Fenster anpassen. Wenn Sie eine benutzerdefinierte Benutzeroberfläche erstellen möchten, können Sie Befehls Schaltflächen im Formular platzieren und Code hinzufügen, der das Windows Media Player-Steuerelement verwaltet. Das Einbetten des Steuer Elements in ein Visual Basic basiertes Programm ähnelt dem Einbetten in ein Office-Dokument und dem Programmieren mit VBA.

Alternativ können Sie das Steuerelement manuell mithilfe von com-Methoden einbetten, um das Steuerelement zu instanziieren und auf die COM-Schnittstellen zuzugreifen, die in der [Objektmodell Referenz für C++](object-model-reference-for-c.md)

Wenn Sie das Windows Media Player-Steuerelement in ein C++-Programm einbetten, haben Sie die Möglichkeit, COM-Schnittstellen zu implementieren, mit denen das Steuerelement im Remote Modus ausgeführt werden kann. Dies bedeutet, dass das eingebettete Steuerelement dieselbe Wiedergabe-Engine wie der vollständige Modus des Players nutzt und dass Benutzer zwischen dem vollständigen und dem angedockten Zustand hin-und herwechseln können, ohne die Wiedergabe digitaler Medien zu unterbrechen. Sie können auch steuern, was in den verschiedenen Bereichen des vollmodusplayers angezeigt wird, wenn die Benutzer in den nicht angedockten Zustand wechseln.

Mit C++ Einbettungen haben Sie auch die Möglichkeit, eine Skin-Definitionsdatei auf das eingebettete Player-Steuerelement anzuwenden. Dies ist eine einfache Möglichkeit zum Erstellen von einfachem Benutzeroberflächen Code, den Sie separat von Ihrem Hauptprogramm Code verwalten können.

Microsoft Visual Studio unterstützt das Einbetten von ActiveX-Steuerelementen, einschließlich des Windows Media Player Steuer Elements Wenn Sie sich dafür entscheiden, erstellt Visual Studio eine neue Alternative Interoperabilitäts-Assembly (Interop), um die Interoperabilität zwischen dem .NET Framework und dem Windows Media Player-Steuerelement zu verwalten. Visual Studio verwendet das .NET Framework tlbimp.exe Tool, um die Interop-Assembly zu erstellen. Dies bedeutet, dass die Signaturen, die bei Verwendung der IntelliSense-Funktion in Visual Studio angezeigt werden, Semantik verwenden, die von der aktuellen Version von Tlbimp bestimmt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Einbetten des Windows Media Player-Steuer Elements**](embedding-the-windows-media-player-control.md)
</dt> <dt>

[**Verwenden des Windows Media Player-Steuer Elements in einem C++-Programm**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> <dt>

[**Verwenden des Windows Media Player-Steuer Elements in einer .NET Framework-Lösung**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> <dt>

[**Verwenden des Windows Media Player-Steuer Elements mit Visual Basic**](using-the-windows-media-player-control-with-visual-basic.md)
</dt> </dl>

 

 





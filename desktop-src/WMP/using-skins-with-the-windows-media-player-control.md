---
title: Verwenden von Skins mit dem Windows Media Player-Steuerelement
description: Verwenden von Skins mit dem Windows Media Player-Steuerelement
ms.assetid: 0381e0e4-c686-4ab4-b947-b883b6f4e06e
keywords:
- Windows Media Player, Einbetten des ActiveX-Steuer Elements
- Windows Media Player Objektmodell, Einbetten des ActiveX-Steuer Elements
- Objektmodell, Einbetten des ActiveX-Steuer Elements
- Windows Media Player Mobile, Einbetten des ActiveX-Steuer Elements
- Windows Media Player ActiveX-Steuerelement, einbetten
- Windows Media Player Mobile ActiveX-Steuerelement, einbetten
- ActiveX-Steuerelement, einbetten
- Windows Media Player, C++
- Windows Media Player-Objektmodell, C++
- Objektmodell, C++
- Windows Media Player Mobile, C++
- Windows Media Player ActiveX-Steuerelement, C++
- Windows Media Player Mobile ActiveX-Steuerelement, C++
- ActiveX-Steuerelement, C++
- C++-Programm Einbettung
- einbetten, C++-Programme
- Windows Media Player ActiveX-Steuerelement, Skins
- Windows Media Player Mobile ActiveX-Steuerelement, Skins
- ActiveX-Steuerelement, Skins
- Skins, Einbettungs Steuerelement für ActiveX
- Windows Media Player Skins, Einbetten des ActiveX-Steuer Elements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3714a8be9e471541d008fcb76a4b0398dba2162b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206796"
---
# <a name="using-skins-with-the-windows-media-player-control"></a>Verwenden von Skins mit dem Windows Media Player-Steuerelement

Wenn Sie das Windows Media Player-Steuerelement in ein C++-Programm einbinden, können Sie die Player-Benutzeroberfläche (User Interface, UI) anpassen, indem Sie eine Skin-Definitionsdatei darauf anwenden. Eine Skin-Definitionsdatei ist ein XML-basiertes Dokument, das das Layout der standardmäßigen und anpassbaren UI-Komponenten und aller zugehörigen Grafiken angibt. Mithilfe von Microsoft JScript können Sie das Verhalten dieser Komponenten angeben und das Windows Media Player-Steuerelement ohne den Aufwand der C++-und com-Syntax bearbeiten.

Skins bieten eine einfache Möglichkeit, den Code Ihrer Benutzeroberfläche und den Code des Hauptprogramms voneinander getrennt zu halten, damit Sie unabhängig voneinander verwaltet und entwickelt werden können. Sie können auch die ursprünglich für die Verwendung durch den eigenständigen Player im Skin-Modus vorgesehenen Skins wieder verwenden. Skin-Code, den Sie speziell für C++-Programme entwerfen, kann über ein Skript fähiges Objekt, das von Ihrem Programm bereitgestellt werden kann, mit ihren Programmen interagieren.

Um den Skin-Modus für das Windows Media Player-Steuerelement zu aktivieren, muss das Programm die **iwmpremotemediaservices** -Schnittstelle implementieren. Obwohl Sie Skins mit dem-Steuerelement verwenden und das-Steuerelement gleichzeitig Remote verwenden können, können Sie diese Schnittstelle verwenden, um beide Funktionen zu aktivieren, ohne die andere zu aktivieren. Um Remoting zu deaktivieren, übergeben Sie einfach den Wert "local" als out-Parameter der **getservicetype** -Methode, und geben Sie ein HRESULT von E \_ notimpl von der **getapplicationname** -Methode zurück.

Um das Windows Media Player-Steuerelement in den Skin-Modus zu wechseln, wenden Sie die Methode **iwmpplayer::p UT \_ uiMode** an, und übergeben Sie dabei den Wert "Custom". Geben Sie den Pfad und den Dateinamen der zu verwendenden Skin-Definitionsdatei an, indem Sie Sie von der **iwmpremotemediaservices:: getcustomuimode** -Methode zurückgeben.

Wenn Sie ein Skript fähiges Objekt für die Kommunikation zwischen Ihrer Skin und Ihrem Programm bereitstellen möchten, übergeben Sie einen Namen und einen Zeiger an einen **IDispatch** -Zeiger als zwei out-Parameter der **iwmpremotemediaservices:: getscriptableobject** -Methode. Die Skin kann dann Aufrufe an das Skript fähige Objekt durchführen, indem der angegebene Name verwendet wird, als ob es sich um ein globales Attribut handelt, das dem globalen Attribut des **Players** ähnelt.

Ein Skin, das auf ein Remotes Windows-Media Player Steuerelement angewendet wird, kann mit einem anderen globalen Attribut namens **playerapplication** auf das **playerapplication** -Objekt zugreifen. Da Skins nicht auf die **Player. playerapplication** -Eigenschaft zugreifen kann, müssen Sie dieses globale Attribut verwenden, wenn Sie möchten, dass der Skin-Code Andocken und Andocken verwaltet.

## <a name="samples"></a>Beispiele

Das Windows Media Player SDK-Setup Paket installiert ein Beispiel, das das Anwenden einer Skin auf das Windows Media Player-Steuerelement veranschaulicht. Weitere Informationen finden Sie im remoteskin-Beispiel.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Beispiele**](samples.md)
</dt> <dt>

[**Verwenden des Windows Media Player-Steuer Elements in einem C++-Programm**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 





---
title: Verwenden des Windows Media Player-Steuerelements mit Microsoft Visual Studio
description: Verwenden des Windows Media Player-Steuerelements mit Microsoft Visual Studio
ms.assetid: e007876e-f215-4976-8a70-018fedc0e67d
keywords:
- Windows Media Player,einbetten ActiveX Steuerelement
- Windows Media Player-Objektmodell, Einbetten ActiveX Steuerelement
- Objektmodell,Einbetten ActiveX Steuerelement
- Windows Media Player Mobil,einbetten ActiveX Steuerelement
- Windows Media Player ActiveX,Einbetten
- Windows Media Player Mobile ActiveX-Steuerelement,Einbetten
- ActiveX,Einbetten
- Windows Media Player,.NET Framework
- Windows Media Player Objektmodell,.NET Framework
- Objektmodell,.NET Framework
- Windows Media Player Mobile,.NET Framework
- Windows Media Player ActiveX,.NET Framework
- Windows Media Player Mobile ActiveX-Steuerelement,.NET Framework
- ActiveX,.NET Framework
- Windows Media Player ActiveX,Visual Studio
- Windows Media Player Mobile ActiveX-Steuerelement,Visual Studio
- ActiveX,Visual Studio
- .NET Framework,Visual Studio-Einbettung des Programms
- Einbetten, Visual Studio Programme
- Visual Studio,Programm-Einbettung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73bb9597b8ad5baadbd51625c68a1d7fb7ebc1791c2d6e8015fb79ba2cab3be6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118830449"
---
# <a name="using-the-windows-media-player-control-with-microsoft-visual-studio"></a>Verwenden des Windows Media Player-Steuerelements mit Microsoft Visual Studio

Sie können das Windows Media Player 9-Serie oder höher ActiveX einer .NET Framework-Anwendung über die Toolbox in Visual Studio.

## <a name="adding-the-windows-media-player-control"></a>Hinzufügen des Windows Media Player-Steuerelements

Stellen Sie vor dem Erstellen eines neuen Projekts sicher, dass die neueste Version von Windows Media Player und das Windows Media Player SDK auf Ihrem Computer installiert ist.

Starten Visual Studio, und erstellen Sie dann ein neues Projekt.

Öffnen Visual Studio Die Toolbox.

Wenn Windows Media Player im Komponentenbereich der  Toolbox nicht angezeigt wird, gehen Sie wie folgt vor:

1.  Klicken Sie mit der rechten Maustaste innerhalb der Toolbox, und wählen Sie **elemente auswählen aus.** Dadurch wird das **Dialogfeld Toolbox anpassen** geöffnet.
2.  Wählen Sie **auf der Registerkarte COM-Komponenten** die Windows Media Player.

    Wenn Windows Media Player nicht in der Liste angezeigt wird, klicken Sie auf Durchsuchen, und öffnen Sie dann Wmp.dll, das sich im Windows \\ System32-Ordner befinden sollte.

3.  Klicken Sie auf **OK**. Das Windows Media Player-Steuerelement wird auf der aktuellen Registerkarte Toolbox platziert.

Sie können jetzt Windows Media Player Toolbox auswählen und einem Formular hinzufügen.

Visual Studio dem Windows Media Player-Steuerelement einen Standardnamen wie "axWindowsMediaPlayer1" zu. Möglicherweise möchten Sie den Namen in einen leichter zu merkenden Namen ändern, z. B. "Player".

Wenn Sie das Windows Media Player-Steuerelement aus der Toolbox hinzufügen, werden auch Verweise auf zwei Bibliotheken hinzugefügt, die von Visual Studio, AxWMPLib und WMPLib, erstellt wurden. Sie finden sie im Projektmappen-Explorer unter **Verweise**.

Um die Verwendung der Objekte im Player-Namespace zu vereinfachen, sollten Sie den -Namespace wie folgt in die using- oder imports-Direktiven Ihrer Dateien hinzufügen:


```Csharp
using WMPLib;
```




```VB
imports WMPLib

```



Die -Direktive stellt sicher, dass Sie auf **Player-Objekte** verweisen können, ohne ihre Namen vollständig zu qualifizieren.

> [!Note]  
> Das Windows Media Player-Steuerelement ist ein **AxWindowsMediaPlayer-Objekt** aus dem **AxWMPLib-Namespace.** Die **AxWindowsMediaPlayer-Klasse** verwendet jedoch Datentypen, Schnittstellen und andere Elemente aus dem **WMPLib-Namespace.**

 

## <a name="configuring-visibility-of-the-control"></a>Konfigurieren der Sichtbarkeit des Steuerelements

Wenn Sie das Steuerelement Windows Media Player einem Formular hinzufügen, wird es angezeigt. Wenn Sie das sichtbare Bild des Players in Ihrer Anwendung nicht verwenden möchten, blenden Sie den Standardplayer aus, indem Sie eine der folgenden Eigenschaften festlegen:



| Eigenschaft        | Wert                                                 |
|-----------------|-------------------------------------------------------|
| **uiMode**      | "unsichtbar" (siehe [Player.uiMode](player-uimode.md).) |
| **Visible**     | „FALSE“                                               |
| **Size.Width**  | 0                                                     |
| **Size.Height** | 0                                                     |



 

Sie können diese Eigenschaften entweder im  Code oder im Eigenschaftenfenster festlegen, wenn das Windows Media Player-Steuerelement im Formular-Designer ausgewählt ist.

## <a name="object-model-compatibility-of-the-control"></a>Objektmodellkompatibilität des Steuerelements

Das Objektmodell für das Windows Media Player-Steuerelement ist im Prinzip dasselbe in der .NET Framework wie in nicht verwaltetem Code und Skript. Es gibt jedoch Unterschiede in der Art und Weise, wie Elemente verfügbar gemacht werden:

-   Die meisten Objekte werden unter dem Namen ihrer zugrunde liegenden COM-Schnittstelle verfügbar gemacht. Beispielsweise wird das **Playlist-Objekt** als **IWMPPlaylist verfügbar gemacht.**
-   Einige Schnittstellen verfügen über spätere Versionen. BEISPIELSWEISE wurde **IWMPMedia zusätzliche** Funktionalität in **IWMPMedia2** und **IWMPMedia3 erteilt.** Wenn Sie ein Objekt als **IWMPMedia** deklarieren, haben Sie in der Regel Zugriff auf die Funktionalität aller Versionen der Schnittstelle. IntelliSense® erkennt jedoch die Methoden oder Eigenschaften der Schnittstellen der späteren Version nicht, und der Visual Basic.NET-Editor korrigiert die Groß-//Ausgabe nicht automatisch. Um den vollen Nutzen von IntelliSense und anderen Features von Visual Studio zu erhalten, deklarieren Sie das -Objekt mithilfe der neuesten Version der -Schnittstelle, z. B. **IWMPMedia3**.
-   Es gibt keine indizierten Eigenschaften (C#) oder Standardeigenschaften (Visual Basic .NET). Um beispielsweise ein **Playlist.item** abzurufen, müssen Sie die **IWMPlaylist.get Item-Accessormethode \_** in C# aufrufen oder die **IWMPlayist.Item-Eigenschaft** in Visual Basic .NET abrufen.
-   Aufgrund eines Namenskonflikts zwischen der Windows Media Player **Controls-Eigenschaft** und der **Controls-Eigenschaft,** die von jedem Steuerelement verfügbar gemacht wird, wird die Player-Version dieser Eigenschaft im Kontext des **steuerelements als CtlControls** ActiveX bezeichnet. (Dies ist jedoch nicht der Fall, wenn Sie den Player programmgesteuert und nicht als ActiveX erstellen.)

Verwenden Sie den Objektbrowser in Visual Studio, um die richtigen API-Namen für Methoden und Objekte in den **Namespaces AxWMPLib** und **WMPLib** zu finden.

## <a name="distributing-your-application"></a>Verteilen Ihrer Anwendung

Wenn Sie Ihre Anwendung verteilen, stellen Sie sicher, dass Sie AxInterop.WMPLib.dll und Interop.WMPLib.dll im Anwendungsordner installieren. Sie müssen auch sicherstellen, dass die erforderliche Windows Media Player auf dem Computer des Benutzers installiert ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmgesteuertes Erstellen Windows Media Player-Steuerelements**](creating-the-windows-media-player-control-programmatically.md)
</dt> <dt>

[**Einbetten des Windows Media Player-Steuerelements in eine C#-Projektmappe**](embedding-the-windows-media-player-control-in-a-c--solution.md)
</dt> <dt>

[**Einbetten des Windows Media Player-Steuerelements in eine Visual Basic .NET-Projektmappe**](embedding-the-windows-media-player-control-in-a-visual-basic--net-solution.md)
</dt> </dl>

 

 





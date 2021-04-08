---
title: Verwenden des Windows Media Player-Steuer Elements mit Microsoft Visual Studio
description: Verwenden des Windows Media Player-Steuer Elements mit Microsoft Visual Studio
ms.assetid: e007876e-f215-4976-8a70-018fedc0e67d
keywords:
- Windows Media Player, Einbetten des ActiveX-Steuer Elements
- Windows Media Player Objektmodell, Einbetten des ActiveX-Steuer Elements
- Objektmodell, Einbetten des ActiveX-Steuer Elements
- Windows Media Player Mobile, Einbetten des ActiveX-Steuer Elements
- Windows Media Player ActiveX-Steuerelement, einbetten
- Windows Media Player Mobile ActiveX-Steuerelement, einbetten
- ActiveX-Steuerelement, einbetten
- Windows Media Player,. NET-Framework
- Windows Media Player-Objektmodell,. NET-Framework
- Objektmodell,. NET-Framework
- Windows Media Player Mobile,. NET-Framework
- Windows Media Player ActiveX-Steuerelement,. NET-Framework
- Windows Media Player Mobile ActiveX-Steuerelement,. NET-Framework
- ActiveX-Steuerelement,. NET-Framework
- Windows Media Player ActiveX-Steuerelement, Visual Studio
- Windows Media Player Mobile ActiveX-Steuerelement, Visual Studio
- ActiveX-Steuerelement, Visual Studio
- .NET Framework, Visual Studio-Programm Einbettung
- einbetten, Visual Studio-Programme
- Visual Studio, Programm Einbettung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b01fecd6acdfd5ccc9a7d823740ef3915bf9c6
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/21/2019
ms.locfileid: "104037665"
---
# <a name="using-the-windows-media-player-control-with-microsoft-visual-studio"></a>Verwenden des Windows Media Player-Steuer Elements mit Microsoft Visual Studio

Mithilfe der Toolbox in Visual Studio können Sie das Windows Media Player 9-oder spätere ActiveX-Steuerelement zu einer .NET Framework Anwendung hinzufügen.

## <a name="adding-the-windows-media-player-control"></a>Hinzufügen des Windows Media Player-Steuer Elements

Stellen Sie vor dem Erstellen eines neuen Projekts sicher, dass die neueste Version von Windows Media Player und Windows Media Player SDK auf Ihrem Computer installiert ist.

Starten Sie Visual Studio, und erstellen Sie dann ein neues Projekt.

Öffnen Sie in Visual Studio die Toolbox.

Wenn Windows Media Player nicht im **Komponenten** Teil der Toolbox angezeigt wird, gehen Sie wie folgt vor:

1.  Klicken Sie mit der rechten Maustaste in die Toolbox, und wählen Sie dann **Elemente auswählen** aus. Dadurch wird das Dialogfeld **Toolbox anpassen** geöffnet.
2.  Wählen Sie auf der Registerkarte **com-Komponenten** die Option Windows Media Player aus.

    Wenn Windows Media Player nicht in der Liste angezeigt wird, klicken Sie auf **Durchsuchen**, und öffnen Sie dann Wmp.dll, das sich im Ordner Windows System32 befinden sollte \\ .

3.  Klicken Sie auf **OK**. Das Windows Media Player-Steuerelement wird auf der aktuellen Toolbox Registerkarte platziert.

Nun können Sie Windows Media Player in der Toolbox auswählen und einem Formular hinzufügen.

Visual Studio erteilt dem Windows Media Player-Steuerelement einen Standardnamen, z. b. "axWindowsMediaPlayer1". Möglicherweise möchten Sie den Namen in etwas leicht zu merken, z. b. "Player", ändern.

Durch das Hinzufügen des Windows Media Player-Steuer Elements aus der Toolbox werden auch Verweise auf zwei von Visual Studio, AxWMPLib und WMPLib erstellte Bibliotheken hinzugefügt. Sie finden Sie im Projektmappen-Explorer unter " **Verweise**".

Wenn Sie die Verwendung der Objekte im Player-Namespace vereinfachen möchten, sollten Sie den-Namespace in die using-oder Imports-Direktiven Ihrer Dateien wie folgt einschließen:


```Csharp
using WMPLib;
```




```VB
imports WMPLib

```



Die-Direktive stellt sicher, dass Sie auf **Player** Objekte verweisen können, ohne ihre Namen vollständig zu qualifizieren.

> [!Note]  
> Das Windows Media Player-Steuerelement ist ein **AxWindowsMediaPlayer** -Objekt aus dem **AxWMPLib** -Namespace. Die Klasse **AxWindowsMediaPlayer** verwendet jedoch Datentypen, Schnittstellen und andere Elemente aus dem **WMPLib** -Namespace.

 

## <a name="configuring-visibility-of-the-control"></a>Konfigurieren der Sichtbarkeit des Steuer Elements

Wenn Sie das Windows Media Player-Steuerelement zum ersten Mal einem Formular hinzufügen, wird es angezeigt. Wenn Sie das sichtbare Bild des Players nicht in Ihrer Anwendung verwenden möchten, blenden Sie den Standard Player aus, indem Sie eine der folgenden Eigenschaften festlegen:



| Eigenschaft        | Wert                                                 |
|-----------------|-------------------------------------------------------|
| **uiMode**      | "unsichtbar" (siehe [Player. uiMode](player-uimode.md).) |
| **Visible**     | „FALSE“                                               |
| **Size. Width**  | 0                                                     |
| **Size. Height** | 0                                                     |



 

Sie können diese Eigenschaften entweder im Code oder im Fenster **Eigenschaften** festlegen, wenn das Windows-Media Player Steuerelement im Formular-Designer ausgewählt wird.

## <a name="object-model-compatibility-of-the-control"></a>Objektmodell Kompatibilität des Steuer Elements

Das Objektmodell für das Windows Media Player-Steuerelement ist im .NET Framework identisch wie in nicht verwaltetem Code und Skript. Es gibt jedoch Unterschiede in der Art, wie Elemente verfügbar gemacht werden:

-   Die meisten Objekte werden unter dem Namen Ihrer zugrunde liegenden COM-Schnittstelle verfügbar gemacht. Beispielsweise wird das **Wiedergabe** Listen Objekt als **iwmpwiedergabe** verfügbar gemacht.
-   Einige Schnittstellen verfügen über spätere Versionen. Beispielsweise wurde **iwmpmedia** zusätzliche Funktionalität in **IWMPMedia2** und **IWMPMedia3** erhalten. Wenn Sie ein Objekt als **iwmpmedia** deklarieren, haben Sie in der Regel Zugriff auf die Funktionalität aller Versionen der-Schnittstelle. Der IntelliSense-® erkennt die Methoden oder Eigenschaften der Schnittstellen der neueren Version jedoch nicht, und der Visual Basic .net-Editor korrigiert nicht automatisch die Groß-/Kleinschreibung. Um den vollständigen Vorteil von IntelliSense und anderen Features von Visual Studio zu erhalten, deklarieren Sie das-Objekt, indem Sie die neueste Version der-Schnittstelle verwenden, z. b. **IWMPMedia3**.
-   Es sind keine indizierten Eigenschaften (c#) oder Standardeigenschaften (Visual Basic .net) vorhanden. Wenn Sie z **. b. ein Wiedergabelisten Element** abrufen möchten, müssen Sie in c# die **iwmwiedergabe. get \_ Item** -Accessor-Methode aufrufen oder die **iwmplayist. Item** -Eigenschaft in Visual Basic .net abrufen.
-   Aufgrund eines Namens Konflikts zwischen der Windows Media Player **Controls** -Eigenschaft und der Steuerelement Eigenschaft **, die von** jedem Steuerelement verfügbar gemacht wird, wird die Spieler Version dieser Eigenschaft im Kontext des ActiveX-Steuer Elements als **ctlcontrols** bezeichnet. (Dies ist jedoch nicht der Fall, wenn Sie den Player Programm gesteuert anstelle von als ActiveX-Steuerelement erstellen.)

Verwenden Sie die Objektkatalog in Visual Studio, um die richtigen API-Namen für Methoden und Objekte in den Namespaces " **AxWMPLib** " und " **WMPLib** " zu finden.

## <a name="distributing-your-application"></a>Verteilen Ihrer Anwendung

Wenn Sie Ihre Anwendung verteilen, achten Sie darauf, dass Sie AxInterop.WMPLib.dll und Interop.WMPLib.dll im Anwendungsordner installieren. Außerdem müssen Sie sicherstellen, dass die erforderliche Windows Media Player-Version auf dem Computer des Benutzers installiert ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programm gesteuertes Erstellen des Windows Media Player-Steuer Elements**](creating-the-windows-media-player-control-programmatically.md)
</dt> <dt>

[**Einbetten des Windows Media Player-Steuer Elements in eine c#-Lösung**](embedding-the-windows-media-player-control-in-a-c--solution.md)
</dt> <dt>

[**Einbetten des Windows Media Player-Steuer Elements in eine Visual Basic .net-Lösung**](embedding-the-windows-media-player-control-in-a-visual-basic--net-solution.md)
</dt> </dl>

 

 





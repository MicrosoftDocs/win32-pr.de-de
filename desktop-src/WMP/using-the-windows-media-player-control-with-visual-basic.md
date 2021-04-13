---
title: Verwenden des Windows Media Player-Steuer Elements mit Visual Basic
description: Verwenden des Windows Media Player-Steuer Elements mit Visual Basic
ms.assetid: 83e5440b-096b-42e1-9038-d779895d9519
keywords:
- Windows Media Player, Einbetten des ActiveX-Steuer Elements
- Windows Media Player Objektmodell, Einbetten des ActiveX-Steuer Elements
- Objektmodell, Einbetten des ActiveX-Steuer Elements
- Windows Media Player Mobile, Einbetten des ActiveX-Steuer Elements
- Windows Media Player ActiveX-Steuerelement, einbetten
- Windows Media Player Mobile ActiveX-Steuerelement, einbetten
- ActiveX-Steuerelement, einbetten
- Windows Media Player Visual Basic
- Windows Media Player-Objektmodell, Visual Basic
- Objektmodell, Visual Basic
- Windows Media Player Mobile, Visual Basic
- Windows Media Player ActiveX-Steuerelement, Visual Basic
- Windows Media Player Mobile ActiveX-Steuerelement, Visual Basic
- ActiveX-Steuerelement, Visual Basic
- Visual Basic basierte Programm Einbettung
- einbetten, Visual Basic basierte Programme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8f2ddd78fe5a254f5bf699fbd2557f1e8700c73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310459"
---
# <a name="using-the-windows-media-player-control-with-visual-basic"></a>Verwenden des Windows Media Player-Steuer Elements mit Visual Basic

In diesem Abschnitt wird beschrieben, wie Sie das ActiveX-Steuerelement Windows Media Player 9 oder höher in Anwendungen verwenden, die mit Microsoft Visual Basic 6,0 erstellt wurden.

## <a name="getting-started"></a>Erste Schritte

Wenn Sie der Toolbox das Windows Media Player-Steuerelement hinzufügen möchten, wählen Sie zunächst **Komponenten** aus dem Menü **Projekt** aus. Aktivieren Sie im Dialogfeld Komponenten das Kontrollkästchen neben "Windows Media Player". Vergewissern Sie sich am unteren Rand des Dialog Felds, dass die ausgewählte Datei wmp.dll ist. Nachdem Sie das Dialogfeld geschlossen haben, können Sie eine Instanz des Windows Media Player-Steuer Elements auf die übliche Weise auf dem Formular platzieren.

Sie können viele Steuerelement Eigenschaften mithilfe des Eigenschaftenfenster festlegen. Um einige Eigenschaften festzulegen, müssen Sie das Dialogfeld Eigenschaften von Windows Media Player verwenden, das Sie mit dem Element "(Custom)" in der Eigenschaftenfenster öffnen.

## <a name="object-references"></a>Objektverweise

Sie können bestimmte Player-Steuerelement Eigenschaften verwenden, um Verweise auf bestimmte Objekte zu erhalten. Beispielsweise gibt die **cdromcollection** -Eigenschaft einen Verweis auf ein **cdromcollection** -Objekt zurück. Sie müssen einen solchen Verweis auf eine Variable zuweisen, die Sie als entsprechende Schnittstelle deklariert haben. Im Fall der **cdromcollection** -Eigenschaft weisen Sie z. b. den Rückgabewert einer Variablen vom Typ " **iwmpcdromcollection**" zu.

Lesen Sie das Thema " [Schnittstellen](interfaces.md) " in der [Objektmodell Referenz für C++](object-model-reference-for-c.md) , um zu ermitteln, welche Objekte mehrere Schnittstellen implementieren. In diesen Fällen müssen Sie eine Objekt Variable als höchste nummerierte Schnittstelle deklarieren, die in diesem SDK dokumentiert ist, um Zugriff auf alle Eigenschaften und Methoden dieses Objekts zu haben. Sie sollten z. b. den Wert der Windows Media Player-Steuerelement Eigenschaft **currentMedia** einer Variablen zuweisen, die als **IWMPMedia3** deklariert ist, um sicherzustellen, dass Sie Zugriff auf die Methoden **getattributecountrytbytype** und **getItemInfoByType** haben.

> [!Note]  
> Das **windowsmediaplayer** -Objekt implementiert alle Eigenschaften und Methoden der Schnittstellen **iwmpcore**, **IWMPCore2**, **IWMPCore3**, **iwmpplayer**, **IWMPPlayer2**, **IWMPPlayer3** und **IWMPPlayer4** . Sie müssen keine separaten Variablen für eine dieser Schnittstellen deklarieren. Mit dem Namen, den Sie Ihrer **windowsmediaplayer** -Instanz zugewiesen haben, können Sie auf alle ihre Member zugreifen.

 

Im Visual Basic Objektkatalog werden viele Schnittstellen angezeigt, die für die private Verwendung durch das Windows Media Player-Steuerelement vorgesehen sind, einschließlich einiger, die Skin-Entwickler unterstützen. Sie sollten nur die Objekte, Eigenschaften, Methoden und Ereignisse verwenden, die in diesem SDK dokumentiert sind.

## <a name="additional-tips"></a>Weitere Tipps

-   Die Referenz Dokumentation zeigt die JScript-Syntax. In JScript werden Argumente, die an Methoden übergeben werden, immer in Klammern eingeschlossen. In Visual Basic 6,0 müssen Argumente, die an Methoden übergeben werden, die keinen Wert zurückgeben, nicht in Klammern eingeschlossen werden.
-   Einige Eigenschaften oder Methoden werden möglicherweise nicht im Code Vervollständigungs Feature der automatischen Liste im Visual Basic Code-Editor angezeigt. Sie können diese Member weiterhin verwenden, indem Sie Ihre Namen genau so eingeben, wie Sie in dieser Dokumentation angezeigt werden.
-   Verwalten der visuellen Darstellung des Steuer Elements mithilfe der **uiMode** -Eigenschaft. Dies kann auf zwei Arten erfolgen. Im Dialogfeld Eigenschaften von Windows-Media Player können Sie die Dropdown Liste **Modus auswählen** verwenden, oder Sie können den richtigen Wert in die Eigenschaftenfenster eingeben.

    Verwenden Sie insbesondere die **Visible** -Eigenschaft nicht, um das Steuerelement auszublenden. Weisen Sie stattdessen den Wert "unsichtbar" der **uiMode** -Eigenschaft zu.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Player-Steuerelement Handbuch**](player-control-guide.md)
</dt> </dl>

 

 





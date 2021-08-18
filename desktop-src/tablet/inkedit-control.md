---
description: Das InkEdit-Steuerelement bietet eine einfache Möglichkeit zum Erfassen, Erkennen und Anzeigen von Freihand.
ms.assetid: a1dfa254-cade-44c5-8fdd-74bb40849063
title: InkEdit-Steuerelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fa64c4452ba5d7f66cdc03a1148c02a12f3945f876d68ac240ff4473e8d50bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118451321"
---
# <a name="inkedit-control"></a>InkEdit-Steuerelement

Das [InkEdit-Steuerelement](inkedit-control-reference.md) bietet eine einfache Möglichkeit zum Erfassen, Erkennen und Anzeigen von Freihand.

Diese Implementierung des [InkEdit-Steuerelements](inkedit-control-reference.md) basiert auf dem [**RichEdit-Steuerelement.**](/windows/desktop/api/richole/nn-richole-iricheditole) Die verwaltete (.NET Framework) Implementierung von [InkEdit](/previous-versions/ms835842(v=msdn.10)) basiert auf dem [**RichTextBox-Steuerelement.**](/previous-versions/windows/)

Der Hauptzweck des [InkEdit-Steuerelements](inkedit-control-reference.md) besteht darin, Ink zu erfassen, zu erkennen und in Textform anzuzeigen. Darüber hinaus wird das Anzeigen von Ink als eingebettetes Objekt mit Textformatierungsfunktionen wie Fett und Unterstreichung unterstützt.

## <a name="gestures-and-correction"></a>Gesten und Korrekturen

[InkEdit](inkedit-control-reference.md) unterstützt die folgenden Gesten.



| Geste                                                                    | Gestenname              | Aktion               |
|----------------------------------------------------------------------------|---------------------------|----------------------|
| ![Geste nach links nach unten](images/d8b00c0a-f450-4f71-980f-3bca1b558e4c.gif)      | Links unten<br/>      | EINGABETASTE<br/>     |
| ![Geste von unten links nach links](images/b8cb23b5-b947-477d-922f-2ffb42756804.gif) | Unten links–lang<br/> | EINGABETASTE<br/>     |
| ![Nach oben nach rechts](images/02c34d24-c2d7-404f-b99a-742ba6de7f0c.gif)       | Nach oben rechts<br/>       | Registerkarte<br/>       |
| ![Nach oben nach rechts und lange Geste.](images/5e3522d3-2920-4a86-86ae-f29b01d93993.gif) | Up-right-long<br/>  | Registerkarte<br/>       |
| ![Rechte Geste](images/864cf4e1-2619-49cf-ac96-72994232e465.jpg)          | Right<br/>          | LeerZchn<br/>     |
| ![Linke Geste](images/ce60cc20-1769-428d-80de-7f47c86021fb.jpg)           | Links<br/>           | Rückschritt<br/> |



 

Gestenereignisse, die Sie behandeln können, enthalten Gesten-, Strich- und Cursorinformationen, mit denen Sie Text an [InkEdit](inkedit-control-reference.md) senden oder Daten in der Zwischenablage platzieren können.

[InkEdit](inkedit-control-reference.md) bietet auch eine Korrekturbenutzeroberfläche, mit der Benutzer Alternative anzeigen und auswählen, die Bildschirmtastatur sowie Zeichen-/Buchstaben-/Blockerkennungen verwenden können.

## <a name="other-details"></a>Weitere Details

[InkEdit](inkedit-control-reference.md) eignet sich gut in einem Formularszenario für einzeilige sowie mehrzeilige Texteingabe und -bearbeitung. Die primäre Verwendung von InkEdit ist das Abrufen von Texteingaben von einem Benutzer in Form von Handschrift. Standardmäßig wird die Ink-Eingabe erkannt, und Text wird an ihrer Stelle eingefügt. Die Standard-Benutzeroberfläche für InkEdit ähnelt der des [**RichTextBox-Steuerelements,**](/previous-versions/windows/) es sei denn, der Benutzer legt Ink fest. Sie können originale Ink anstelle von Text anzeigen. die Ink-Schriftart wird jedoch auf den aktuellen Eingabeschriftgrad des InkEdit-Steuerelements skaliert und inline mit anderem Text angezeigt.

> [!Note]  
> Aus Sicherheitsgründen müssen Sie Standardverfahren verwenden, um eine Datei zu öffnen oder zu schließen, die Eingabe/Ausgabe zu streamen und die [**RTF-**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selrtf) oder [**Text-Eigenschaft**](/windows/desktop/api/inked/nf-inked-iinkedit-get_seltext) festzulegen.

 

Das [InkEdit-Steuerelement](inkedit-control-reference.md) ist so festgelegt, dass ink als Text standardmäßig erkannt wird. Damit Benutzer Freihand als Freihand hinzufügen können, legen Sie die [**InkInsertMode-Eigenschaft**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkinsertmode) auf **InsertAsInk** fest.

Ausführliche Referenzinformationen zum [InkEdit-Steuerelement](inkedit-control-reference.md) finden Sie unter InkEdit.

> [!Note]  
> Wenn Sie das Win32 [InkEdit-Steuerelement](inkedit-control-reference.md) verwenden und es in einem Gruppenfeld platzieren, stellen Sie sicher, dass das Feld einen transparenten Stil hat. Andernfalls kann InkEdit keine Ink-Daten erfassen.

 

> [!Note]  
> Um sicherzustellen, dass Ink ordnungsgemäß angezeigt wird, rufen Sie die [**Refresh-Methode**](/windows/desktop/api/inked/nf-inked-iinkedit-refresh) des [InkEdit-Steuerelements](inkedit-control-reference.md) auf, wenn sie ein [**HScroll-**](/dotnet/api/system.windows.forms.richtextbox.hscroll?view=netcore-3.1) oder [**VScroll-Ereignis**](/dotnet/api/system.windows.forms.richtextbox.vscroll?view=netcore-3.1) empfängt.

 

In den folgenden Abschnitten wird die Verwendung des [InkEdit-Steuerelements](inkedit-control-reference.md) ausführlich beschrieben:

-   [Instanziieren von InkEdit](instantiating-inkedit.md)
-   [Wort- und Zeichenerkennung](word-vs--character-recognition.md)
-   [Anzeigen von "Ink" als "Ink"](displaying-ink-as-ink.md)
-   [Verwenden von InkEdit in früheren Versionen von Windows](using-inkedit-on-earlier-versions-of-windows.md)
-   [Verwenden eines Anwendungswörterbuchs mit InkEdit](using-an-application-dictionary-with-inkedit.md)

 


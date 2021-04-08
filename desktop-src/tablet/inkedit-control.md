---
description: Das InkEdit-Steuerelement bietet eine einfache Möglichkeit, frei Hand Eingaben zu erfassen, zu erkennen und anzuzeigen.
ms.assetid: a1dfa254-cade-44c5-8fdd-74bb40849063
title: InkEdit-Steuerelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf6d5441506ee791eefddba05b9b1f3ddb8a8ec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866139"
---
# <a name="inkedit-control"></a>InkEdit-Steuerelement

Das [InkEdit](inkedit-control-reference.md) -Steuerelement bietet eine einfache Möglichkeit, frei Hand Eingaben zu erfassen, zu erkennen und anzuzeigen.

Diese Implementierung des [InkEdit](inkedit-control-reference.md) -Steuer Elements basiert auf dem [**RichEdit**](/windows/desktop/api/richole/nn-richole-iricheditole) -Steuerelement. Die verwaltete (.NET Framework)-Implementierung von [InkEdit](/previous-versions/ms835842(v=msdn.10)) basiert auf dem [**RichTextBox**](/previous-versions/windows/) -Steuerelement.

Der Hauptzweck des [InkEdit](inkedit-control-reference.md) -Steuer Elements besteht darin, frei Hand Eingaben zu erfassen, zu erkennen und in Textform anzuzeigen. Außerdem wird die Anzeige von frei Hand Eingaben als eingebettetes Objekt mit Text Formatierungsfunktionen unterstützt, z. b. Fett und unterstrichen.

## <a name="gestures-and-correction"></a>Gesten und Korrektur

[InkEdit](inkedit-control-reference.md) unterstützt die folgenden Gesten.



| Geste                                                                    | Gesten Name              | Aktion               |
|----------------------------------------------------------------------------|---------------------------|----------------------|
| ![nach-links-Geste](images/d8b00c0a-f450-4f71-980f-3bca1b558e4c.gif)      | Nach unten links<br/>      | EINGABETASTE<br/>     |
| ![Bewegung nach unten links](images/b8cb23b5-b947-477d-922f-2ffb42756804.gif) | Nach unten links<br/> | EINGABETASTE<br/>     |
| ![Rechte Bewegung](images/02c34d24-c2d7-404f-b99a-742ba6de7f0c.gif)       | Rechts oben<br/>       | Registerkarte<br/>       |
| ![Bewegung nach oben rechts](images/5e3522d3-2920-4a86-86ae-f29b01d93993.gif) | Oben rechts<br/>  | Registerkarte<br/>       |
| ![Rechte Bewegung](images/864cf4e1-2619-49cf-ac96-72994232e465.jpg)          | Rechts<br/>          | LeerZchn<br/>     |
| ![linke Bewegung](images/ce60cc20-1769-428d-80de-7f47c86021fb.jpg)           | Links<br/>           | Rücktaste<br/> |



 

Gesten Ereignisse, die Sie behandeln können, enthalten Gesten-, Strich-und Cursor Informationen, die Sie zum Senden von Text an [InkEdit](inkedit-control-reference.md) oder zum Platzieren von Daten in der Zwischenablage verwenden können.

[InkEdit](inkedit-control-reference.md) bietet auch eine Korrektur Benutzeroberfläche, die es Benutzern ermöglicht, Alternativen anzuzeigen und aus Ihnen auszuwählen, die Bildschirmtastatur zu verwenden und Zeichen-/Schreib-/blockerkenzer zu verwenden.

## <a name="other-details"></a>Weitere Details

[InkEdit](inkedit-control-reference.md) ist so konzipiert, dass es in einem Formular Szenario für eine einzelne Zeile sowie für die mehrzeilige Texteingabe und-Bearbeitung funktioniert. Der primäre Verwendungszweck für InkEdit besteht darin, Texteingaben von einem Benutzer in Form von Handschrift zu erhalten. Standardmäßig wird die frei Hand Eingabe erkannt, und der Text wird an seiner Stelle eingefügt. Die Standardbenutzer Oberfläche für InkEdit ähnelt der des [**RichTextBox**](/previous-versions/windows/) -Steuer Elements, es sei denn, der Benutzer legt frei Hand Eingaben fest. Sie können ursprüngliches frei Hand Eingaben anstelle von Text anzeigen. die frei Hand Eingabe wird jedoch auf die aktuelle Eingabe Schriftgröße des InkEdit-Steuer Elements skaliert und Inline mit anderem Text angezeigt.

> [!Note]  
> Aus Sicherheitsgründen müssen Sie Standard Prozeduren verwenden, um eine Datei zu öffnen oder zu schließen, die Eingabe/Ausgabe zu streamen und die [**RTF**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selrtf) -oder [**Text**](/windows/desktop/api/inked/nf-inked-iinkedit-get_seltext) -Eigenschaft festzulegen.

 

Das [InkEdit](inkedit-control-reference.md) -Steuerelement ist so festgelegt, dass Freihand als Text standardmäßig erkannt wird. Legen Sie die [**InkInsertMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkinsertmode) -Eigenschaft auf **InsertAsInk** fest, damit Benutzer frei Hand Eingaben als frei Hand Eingaben hinzufügen können.

Ausführliche Referenzinformationen zum [InkEdit](inkedit-control-reference.md) -Steuerelement finden Sie unter InkEdit.

> [!Note]  
> Wenn Sie das Win32 [InkEdit](inkedit-control-reference.md) -Steuerelement verwenden und es in einem Gruppenfeld platzieren, stellen Sie sicher, dass das Feld einen transparenten Stil hat. Andernfalls kann InkEdit keine Freihand sammeln.

 

> [!Note]  
> Um sicherzustellen, dass frei Hand Eingaben ordnungsgemäß angezeigt werden, wenden Sie die Methode zum [**Aktualisieren**](/windows/desktop/api/inked/nf-inked-iinkedit-refresh) des [InkEdit](inkedit-control-reference.md) -Steuer Elements an, wenn es ein [**HScroll**](/dotnet/api/system.windows.forms.richtextbox.hscroll?view=netcore-3.1) [**-oder**](/dotnet/api/system.windows.forms.richtextbox.vscroll?view=netcore-3.1)

 

In den folgenden Abschnitten wird die Verwendung des [InkEdit](inkedit-control-reference.md) -Steuer Elements ausführlich erläutert:

-   [Instanziieren von InkEdit](instantiating-inkedit.md)
-   [Wort und Zeichenerkennung](word-vs--character-recognition.md)
-   [Anzeigen von frei Hand Eingaben](displaying-ink-as-ink.md)
-   [Verwenden von InkEdit unter früheren Versionen von Windows](using-inkedit-on-earlier-versions-of-windows.md)
-   [Verwenden eines Anwendungs Wörterbuchs mit InkEdit](using-an-application-dictionary-with-inkedit.md)

 


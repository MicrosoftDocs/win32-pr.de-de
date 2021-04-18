---
title: Einfaches Beispiel für die Skripterstellung auf einer Webseite
description: Einfaches Beispiel für die Skripterstellung auf einer Webseite
ms.assetid: c6d6954e-f684-4dc1-8b9c-c5fc3cab7421
keywords:
- Windows Media Player, Einbetten des ActiveX-Steuer Elements
- Windows Media Player Objektmodell, Einbetten des ActiveX-Steuer Elements
- Objektmodell, Einbetten des ActiveX-Steuer Elements
- Windows Media Player Mobile, Einbetten des ActiveX-Steuer Elements
- Windows Media Player ActiveX-Steuerelement, einbetten
- Windows Media Player Mobile ActiveX-Steuerelement, einbetten
- ActiveX-Steuerelement, einbetten
- Windows Media Player ActiveX-Steuerelement, Webseiten
- Windows Media Player Mobile ActiveX-Steuerelement, Webseiten
- ActiveX-Steuerelement, Webseiten
- Windows Media Player ActiveX-Steuerelement, Skript Beispiel
- Windows Media Player Mobile ActiveX-Steuerelement, Skript Beispiel
- ActiveX-Steuerelement, Skript Beispiel
- Einbettungen, Webseiten
- Einbetten von Webseiten, Skript Beispiel
- Skript Beispiel für die Einbettung von Webseiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9616bd4032a1b2d7e70916b545db30289995eb4
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/21/2019
ms.locfileid: "106337399"
---
# <a name="simple-example-of-scripting-in-a-web-page"></a>Einfaches Beispiel für die Skripterstellung auf einer Webseite

Sie können das Windows Media Player-Steuerelement problemlos in eine HTML-Datei einbetten, indem Sie jede Skriptsprache verwenden, die Ihr Browser erkennt Im folgenden einfachen Beispiel wird mithilfe von Microsoft JScript eine Seite erstellt, die eine Datei wieder gibt, wenn Sie auf eine Schaltfläche klicken und die Wiedergabe der Datei beenden, wenn Sie auf eine andere Schaltfläche klicken.

Sie können das Windows Media Player ActiveX-Steuerelement mithilfe der folgenden vier Schritte in eine Webseite einbetten:

1.  Erstellen Sie die Webseite.
2.  Fügen Sie das Objekttag hinzu.
3.  Fügen Sie eine Benutzeroberfläche hinzu. In diesem Fall zwei Schaltflächen.
4.  Fügen Sie einige Codezeilen hinzu, um zu antworten, wenn der Benutzer auf eine der Schaltflächen klickt, die Sie erstellt haben.

## <a name="creating-the-web-page"></a>Erstellen der Webseite

Der erste Schritt besteht darin, eine gültige HTML-Webseite zu erstellen. Der folgende Code ist mindestens erforderlich, um eine leere, aber gültige HTML-Seite zu erstellen:


```HTML
<HTML>
    <HEAD>
    </HEAD>
    <BODY>
    </BODY>
</HTML>

```



## <a name="adding-the-object-tag"></a>Hinzufügen des Objekttags

Nachdem Sie eine Webseite erstellt haben, müssen Sie ein Objekttag hinzufügen. Dadurch wird das ActiveX-Steuerelement für den Browser identifiziert, und alle anfänglichen Definitionen werden eingerichtet. Sie müssen das Objekttag im Text des Codes platzieren. Wenn Sie diese im Textkörper platzieren, wird die Standardbenutzer Oberfläche von Windows Media Player angezeigt. Wenn Sie eine eigene Benutzeroberfläche erstellen möchten, legen Sie die Attribute height und Width auf 0 (null) fest. Sie können auch den *Player* festlegen. **uiMode** -Eigenschaft auf "unsichtbar", wenn Sie das Steuerelement ausblenden möchten, aber trotzdem Platz für das Steuerelement auf der Seite reservieren. Der folgende Code wird empfohlen, wenn Sie eine benutzerdefinierte Benutzeroberfläche bereitstellen:


```HTML
<OBJECT ID="Player" height="0" width="0"
  CLASSID="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
</OBJECT>

```



Die folgenden objekttagattribute sind erforderlich:

id

Der Name, der von anderen Teilen des Codes verwendet wird, um das ActiveX-Steuerelement zu identifizieren und zu verwenden. Sie können einen beliebigen Namen auswählen, solange es sich um einen Namen handelt, der nicht bereits von HTML, HTML-Erweiterungen oder der verwendeten Skriptsprache verwendet wird. In diesem Beispiel wird der Name "Player" verwendet, Sie können ihn aber auch "myPlayer" oder etwas anderes nennen. Wählen Sie einfach einen Namen aus, der für diese Webseite eindeutig ist.

ClassID

Eine sehr große hexadezimal Zahl, die für das-Steuerelement eindeutig ist. Nur ein Steuerelement hat diese Zahl und ist das Windows Media Player ActiveX-Steuerelement. Um typografische Fehler zu vermeiden, können Sie diese Nummer aus der Dokumentation kopieren und einfügen. Versionen des Windows Media Player-Steuer Elements vor Version 7,0 verfügten über eine andere ClassID.

## <a name="adding-a-user-interface"></a>Hinzufügen einer Benutzeroberfläche

HTML ermöglicht eine große Zahl von Elementen der Benutzeroberfläche, sodass der Benutzer mit Ihrer Webseite interagieren kann, indem er auf Schlüssel und andere Benutzeraktionen klickt. Das Hinzufügen einiger Eingabe Schaltflächen ist die einfachste Möglichkeit, um eine schnelle Benutzeroberfläche bereitzustellen. Mit dem folgenden Code werden zwei Schaltflächen erstellt, die auf den Benutzer reagieren können. Wenn Sie auf eine Schaltfläche klicken, wird der Medienstrom abgespielt, und die andere Schaltfläche beendet ihn:


```HTML
<INPUT TYPE="BUTTON" NAME="BtnPlay" VALUE="Play" OnClick="StartMeUp()">
<INPUT TYPE="BUTTON" NAME="BtnStop" VALUE="Stop" OnClick="ShutMeDown()">

```



Der Name der Schaltfläche wird verwendet, um die Schaltfläche für den Code zu identifizieren. der Wert ist die Bezeichnung, die auf der Schaltfläche angezeigt wird, und das OnClick-Attribut gibt an, welcher Teil des Skriptcodes aufgerufen wird, wenn auf die Schaltfläche geklickt wird.

## <a name="adding-scripting-code"></a>Hinzufügen von Skript Code

Der Skriptcode fügt der Seite Interaktivität hinzu. Der Skriptcode kann auf Ereignisse, Aufruf Methoden und Änderungs Lauf Zeiteigenschaften reagieren. Erweiterte Skripts sind in einem skripttagsatz enthalten. Das Script-Tag teilt dem Browser mit, wo der Skriptcode ist, und identifiziert die Skriptsprache. Wenn Sie keine Sprache identifizieren, wird als Standardsprache Microsoft JScript verwendet.

Es ist empfehlenswert, das Skript in HTML-Kommentar Tags einzuschließen, sodass Browser, die keine Skripterstellung unterstützen, Ihren Code nicht als Text Rendering. Fügen Sie das Skript-Tag an eine beliebige Stelle innerhalb des Texts der HTML-Datei ein, und Betten Sie den Code aus, der in den öffnenden und schließenden Skript Tags

Im folgenden Beispiel für ein Microsoft JScript-Code wird das Windows Media Player-Steuerelement aufgerufen und eine entsprechende Aktion als Reaktion auf den entsprechenden Klick auf die Schaltfläche ausgeführt.


```HTML
<SCRIPT>
<!--

function StartMeUp ()
{
    Player.URL = "laure.wma";
}

function ShutMeDown ()
{
    Player.controls.stop();
}

-->
</SCRIPT>

```



Die Beispiel Funktion startmeup wird aufgerufen, wenn auf die Schaltfläche mit der markierten Wiedergabe Taste geklickt wird und die shutmedown-Funktion aufgerufen wird, wenn auf die Schaltfläche Beenden geklickt wird.

Der Code in startmeup verwendet die URL-Eigenschaft, um einen Pfad zu den Medien zu definieren. Die Medien werden sofort wiedergegeben.

Der shutmedown-Code ruft  die Methode "Beenden **" des Steuerelement Objekts auf** . Beachten Sie, dass das Steuerelement-Objekt über die **Controls** -Eigenschaft des **Player** **-Objekts aufgerufen** wird, das den ID-Wert "Player" hat.

Der folgende Code veranschaulicht das vollständige Beispiel.


```HTML
<HTML>
<HEAD>
</HEAD>
<BODY>
<OBJECT ID="Player" height="0" width="0"
  CLASSID="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
</OBJECT>
<INPUT TYPE="BUTTON" NAME="BtnPlay" VALUE="Play" OnClick="StartMeUp()">
<INPUT TYPE="BUTTON" NAME="BtnStop" VALUE="Stop" OnClick="ShutMeDown()">
<SCRIPT>
<!--

function StartMeUp ()
{
    Player.URL = "laure.wma";
}

function ShutMeDown ()
{
    Player.controls.stop();
}

-->
</SCRIPT>
</BODY>
</HTML>

```



Beachten Sie, dass Sie in der URL-Eigenschaft eine gültige URL für einen gültigen Dateinamen angeben müssen. In diesem Fall wird davon ausgegangen, dass sich die Datei "Laure. wma" im selben Verzeichnis wie die HTML-Datei befindet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden des Windows Media Player-Steuer Elements in einer Webseite**](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 





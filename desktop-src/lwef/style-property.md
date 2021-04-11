---
title: Style-Eigenschaft
description: Style-Eigenschaft
ms.assetid: f01d7d51-8a16-4265-b9b7-93b64f4984e3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 024d46dd7f7ce0e2fdc16b8b17f9074b1eef30c0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310076"
---
# <a name="style-property"></a>Style-Eigenschaft

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt den Ausgabe Stil der Wort Sprechblase des Zeichens zurück oder legt ihn fest.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent. ***Zeichen ("*** Merkmal-ID * * *"). Sprechblase. Stil* *  \[  =  *Stil*\]



| Teil    | BESCHREIBUNG                                                                                                                                                                                                                                                                       |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Stil* | Eine ganze Zahl, die den Ausgabe Stil der Sprechblase darstellt. Die Stil Einstellung ist ein Bitfeld mit Bits, die Folgendes aufweisen: Sprechblase-on (Bit 0), Größe-zu-Text (Bit 1), Automatisches Ausblenden (Bit 2), automatische Geschwindigkeit (Bit 3), Anzahl der Zeichen pro Zeile (Bits 16-23) und Anzahl der Zeilen (Bits 24-31). |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn das stylebit für die Sprechblase auf 1 festgelegt ist, wird die Word- [**Sprech**](https://www.bing.com/search?q=**Speak**) Blase angezeigt, wenn eine Sprech [**Methode oder**](think-method.md) eine-Methode verwendet wird, es sei denn, der Benutzer überschreibt diese Einstellung auf der Eigenschaften Seite des Microsoft-Agents Wenn der Wert auf 0 festgelegt ist, wird keine Sprechblase angezeigt.

Wenn das Bit-zu-Text-Format Bit auf 1 festgelegt ist, wird die Höhe der [**Sprech**](https://www.bing.com/search?q=**Speak**) Blase von der Word-Sprechblase automatisch auf die aktuelle Textgröße für die Sprech [**-oder die**](think-method.md) -Anweisung festgelegt. Wenn der Wert auf 0 festgelegt ist, basiert die Höhe der Sprechblase auf [**der Eigenschafts**](numberoflines-property.md) Einstellung für die-Eigenschaft. Wenn dieses Stilbit auf 1 festgelegt ist und Sie versuchen, die Eigenschaft " **numoflines** " festzulegen, löst der-Agent einen Fehler aus.

Wenn das Auto-Hide-Format Bit auf 1 festgelegt ist, wird die Wort Sprechblase automatisch ausgeblendet, wenn die gesprochene Ausgabe abgeschlossen ist. Wenn der Wert auf 0 festgelegt ist, bleibt die [**Sprech**](https://www.bing.com/search?q=**Speak**) Blase bis zum nächsten Sprech-oder ansichtenbefehl angezeigt, das Zeichen ist ausgeblendet, oder der Benutzer klickt oder zieht das Zeichen. [](think-method.md)

Wenn das Format des automatischen Geschwindigkeits Formats auf 1 festgelegt ist, wird die Ausgabe von der Word-Sprechblase basierend auf der aktuellen Ausgabe Rate, z. b. einem Wort, auf der Grundlage der aktuellen Ausgabe Rate. Wenn die Ausgabe die Größe der Sprechblase überschreitet, wird für den vorherigen Text automatisch ein Bildlauf durchgeführt. Wenn der Wert auf 0 festgelegt ist, wird der gesamte Text, der in einer [**sprechen**](https://www.bing.com/search?q=**Speak**) [**-oder-**](think-method.md) Anweisung enthalten ist, gleichzeitig

, Um nur den Wert der untersten vier Bits abzurufen, **und** den Wert, der von **Style** mit 255 zurückgegeben wird. , Um einen Bitwert festzulegen, **oder** den Wert, der mit dem Wert der Bits zurückgegeben wird, die Sie festlegen möchten. Um das Bit zu deaktivieren, **und** der Wert, der mit einem Komplement des Bits zurückgegeben wird:


```
   Const BalloonOn = 1

   ' Turn the word balloon off
   Genie.Balloon.Style = Genie.Balloon.Style And (Not BalloonOn)
   Genie.Speak "No balloon"

   ' Turn the word balloon on
   Genie.Balloon.Style = Genie.Balloon.Style Or BalloonOn
   Genie.Speak "Balloon"
```



Die **Style** -Eigenschaft gibt auch die Anzahl der Zeichen pro Zeile im unteren Byte des oberen Worts und die Anzahl der Zeilen im oberen Byte des oberen Worts zurück. Obwohl dies mithilfe der Eigenschaften " [**charsperline**](charsperline-property.md) " und " [**numoflines**](numberoflines-property.md)" leichter lesbar ist, können Sie mit der **Style** -Eigenschaft auch diese Werte festlegen.

Um z. b. die Anzahl der Zeilen zu ändern, löschen Sie Bits 24 bis 31 mit einem logischen **and-** Vorgang, bevor Sie den neuen Wert als Produkt des neuen Werts 2 ^ 24 festlegen, der dem vorhandenen Wert der **Style** -Eigenschaft hinzugefügt wird.


```
   ' Set the number of lines to 4
   Genie.Balloon.Style = (Genie.Balloon.Style <b>AND</b> &amp;H00FFFFFF) + (4*(2^24))
```



Um die Anzahl der Zeichen pro Zeile festzulegen, löschen Sie Bits 16 bis 23 mit einem logischen **and-** Vorgang, bevor Sie den neuen Wert als Produkt des neuen Werts 2 ^ 16 festlegen, der dem vorhandenen Wert der Style-Eigenschaft hinzugefügt wird.


```
   ' Set the number of characters per line to 16
   Genie.Balloon.Style = (Genie.Balloon.Style AND &amp;HFF00FFFF) + (16*(2^16))
```



Die **Style** -Eigenschaft kann auch dann festgelegt werden, wenn der Benutzer die Sprechblasen Anzeige mithilfe der Eigenschaften Seite des Microsoft-Agents deaktiviert hat. Allerdings müssen die Werte für die Anzahl der Zeilen zwischen 1 und 128 liegen, und die Anzahl der Zeichen pro Zeile muss zwischen 8 und 255 liegen. Wenn Sie einen ungültigen Wert für die **Style** -Eigenschaft angeben, wird vom-Agent ein Fehler ausgegeben.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.

Die Standardwerte für diese stilbits basieren auf Ihren Einstellungen, wenn das Zeichen mit dem Microsoft-Agent-Zeichen-Editor kompiliert wird.

 

 





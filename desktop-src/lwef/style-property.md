---
title: Style-Eigenschaft
description: Style-Eigenschaft
ms.assetid: f01d7d51-8a16-4265-b9b7-93b64f4984e3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37196aead474c5364c7a94780686707b74bab0f4c4831381cf4c40e47e350e17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119715880"
---
# <a name="style-property"></a>Style-Eigenschaft

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt den Ausgabestil des Wortsprechblasens des Zeichens zurück oder legt dieses fest.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent.***Characters("**_CharacterID_*_"). Balloon.Style-Stil_ *  \[  =  \]



| Teil    | Beschreibung                                                                                                                                                                                                                                                                       |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Stil* | Eine ganze Zahl, die den Ausgabestil des Sprechblasens darstellt. Die Stileinstellung ist ein Bitfeld mit Bits, die den folgenden Entsprechen entsprechen: balloon-on (bit 0), size-to-text (bit 1), auto-hide (bit 2), auto-pace (bit 3), number of characters per lines (bits 16-23) and number of lines (bits 24-31). |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn das Sprechblasen-On-Stilbit auf 1 festgelegt ist, wird die Wortsprechblase angezeigt, wenn eine [**Speak-**](https://www.bing.com/search?q=**Speak**) oder [**Think-Methode**](think-method.md) verwendet wird, es sei denn, der Benutzer überschreibt diese Einstellung im Eigenschaftenblatt des Microsoft-Agents. Wenn diese Einstellung auf 0 festgelegt ist, wird keine Sprechblase angezeigt.

Wenn das Size-to-Text-Formatbit auf 1 festgelegt ist, wird die Höhe des Sprechblasens automatisch auf die aktuelle Größe des Texts für die [**Speak-**](https://www.bing.com/search?q=**Speak**) oder [**Think-Anweisung**](think-method.md) festgelegt. Wenn diese Einstellung auf 0 festgelegt ist, basiert die Höhe des Sprechblasens auf der [**NumberOfLines-Eigenschafteneinstellung.**](numberoflines-property.md) Wenn dieses Formatbit auf 1 festgelegt ist und Sie versuchen, die **NumberOfLines-Eigenschaft** festzulegen, löst der -Agent einen Fehler aus.

Wenn das Formatbit für das automatische Ausblenden auf 1 festgelegt ist, wird der Wortsprechblasen automatisch ausgeblendet, wenn die gesprochene Ausgabe abgeschlossen ist. Wenn die Sprechblase auf 0 festgelegt ist, bleibt die Sprechblase angezeigt, bis der nächste [**Speak-**](https://www.bing.com/search?q=**Speak**) oder [**Think-Aufruf,**](think-method.md) das Zeichen ausgeblendet ist oder der Benutzer auf das Zeichen klickt oder zieht.

Wenn das Stilbit für die automatische Geschwindigkeit auf 1 festgelegt ist, beschleunigt das Wort balloon die Ausgabe basierend auf der aktuellen Ausgaberate, z. B. ein Wort nach dem anderen. Wenn die Ausgabe die Größe des Sprechblasens überschreitet, wird automatisch ein Bildlauf für den vorherigen Text durchgeführt. Wenn diese Einstellung auf 0 festgelegt ist, wird der gesamte Text, der in einer [**Speak-**](https://www.bing.com/search?q=**Speak**) oder [**Think-Anweisung**](think-method.md) enthalten ist, gleichzeitig angezeigt.

Um nur den Wert der unteren vier Bits abzurufen, **und** den wert, der von **Style** mit 255 zurückgegeben wird. So legen Sie einen Bitwert fest, **oder** den Wert, der mit dem Wert der bits zurückgegeben wird, die Sie festlegen möchten. Um ein Bit zu deaktivieren, **und** der Wert, der mit dem Komplement des Bits zurückgegeben wird:


```
   Const BalloonOn = 1

   ' Turn the word balloon off
   Genie.Balloon.Style = Genie.Balloon.Style And (Not BalloonOn)
   Genie.Speak "No balloon"

   ' Turn the word balloon on
   Genie.Balloon.Style = Genie.Balloon.Style Or BalloonOn
   Genie.Speak "Balloon"
```



Die **Style-Eigenschaft** gibt auch die Anzahl der Zeichen pro Zeile im unteren Byte des oberen Worts und die Anzahl der Zeilen im oberen Byte des oberen Worts zurück. Dies kann zwar mithilfe der Eigenschaften [**CharsPerLine**](charsperline-property.md) und [**NumberOfLines**](numberoflines-property.md)einfacher gelesen werden, aber mit der **Style-Eigenschaft** können Sie diese Werte auch festlegen.

Um beispielsweise die Anzahl der Zeilen zu ändern, löschen Sie die  Bits 24 bis 31 mit einem logischen AND-Vorgang, bevor Sie den neuen Wert als Produkt des neuen Werts mal 2^24 festlegen, der dem vorhandenen Wert der **Style-Eigenschaft** hinzugefügt wird.


```
   ' Set the number of lines to 4
   Genie.Balloon.Style = (Genie.Balloon.Style <b>AND</b> &amp;H00FFFFFF) + (4*(2^24))
```



Um die Anzahl der Zeichen pro Zeile festzulegen, löschen Sie die  Bits 16 bis 23 mit einem logischen AND-Vorgang, bevor Sie den neuen Wert als Produkt des neuen Werts mal 2^16 festlegen, der dem vorhandenen Wert der Style-Eigenschaft hinzugefügt wird.


```
   ' Set the number of characters per line to 16
   Genie.Balloon.Style = (Genie.Balloon.Style AND &amp;HFF00FFFF) + (16*(2^16))
```



Die **Style-Eigenschaft** kann auch dann festgelegt werden, wenn der Benutzer die Sprechblasenanzeige mithilfe des Eigenschaftenblatts des Microsoft-Agents deaktiviert hat. Die Werte für die Zeilenanzahl müssen jedoch zwischen 1 und 128 und die Zahlenzeichen pro Zeile zwischen 8 und 255 betragen. Wenn Sie einen ungültigen Wert für die **Style-Eigenschaft** angeben, wird vom -Agent ein Fehler ausgelöst.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch Ihre Clientanwendung. Die Einstellung wirkt sich nicht auf andere Clients des Zeichens oder anderer Zeichen Ihrer Clientanwendung aus.

Die Standardwerte für diese Stilbits basieren auf ihren Einstellungen, wenn das Zeichen mit dem Microsoft-Agent-Zeichen-Editor kompiliert wird.

 

 





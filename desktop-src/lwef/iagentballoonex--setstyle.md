---
title: Iagentballoonex-SetStyle
description: Iagentballoonex-SetStyle
ms.assetid: 5be569b7-8a2d-437b-b5db-401af343bc78
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d942cc8adaf454a7c5f1cd299581f917560c00a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339241"
---
# <a name="iagentballoonexsetstyle"></a>Iagentballoonex:: SetStyle

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT SetStyle(
   long lStyle,  // style settings
);
```

Ruft die Stileinstellungen der Wort Sprechblase des Zeichens ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="lStyle"></span><span id="lstyle"></span><span id="LSTYLE"></span>*lstyle*
</dt> <dd>

Stileinstellungen für die Word-Sprechblase, bei der es sich um eine Kombination aus einem der folgenden Werte handeln kann:



| Wert                                                                            | BESCHREIBUNG                                                 |
|----------------------------------------------------------------------------------|-------------------------------------------------------------|
| **Ganzzahl ohne Vorzeichen Short** -Sprechblasen **\_ Stil \_ : ballonon = 0x00000001;**<br/>  | Die Sprechblase wird für die Ausgabe unterstützt.                        |
| der **Ganzzahl ohne Vorzeichen Short** -Sprechblasen **\_ Stil \_ size-Text = 0x0000002;**<br/> | Die Höhe der Sprechblase ist so groß, dass Sie der Textausgabe entspricht. |
| **Ganzzahl ohne Vorzeichen Short** -Sprechblasen **\_ Stil \_ automatisch ausblenden = 0x00000004;**<br/>  | Die Sprechblase wird automatisch ausgeblendet.                        |
| automatische **unsignierte kurze** Sprechblasen Format- **\_ \_ autopace = 0x00000008;**<br/>  | Die Textausgabe erfolgt basierend auf der Ausgabe Rate.          |



 

</dd> </dl>

Wenn das Feld **für** das Blasen Format festgelegt ist, wird die Word- [**Sprech**](speak-method.md) Blase angezeigt, wenn die Sprech [**Methode oder die**](think-method.md) -Methode verwendet wird, es sei denn, der Benutzer überschreibt die Anzeige auf der Eigenschaften Seite des Microsoft-Agents. Wenn nicht festgelegt, wird keine Sprechblase angezeigt.

Wenn das **sizetetext** -Stilbit festgelegt ist, wird die Höhe der Sprechblase von der Word-Sprechblase automatisch auf die aktuelle Textgröße festgelegt, die in der [**Sprech**](speak-method.md) [**Methode oder**](think-method.md) der-Methode angegeben ist. Wenn nicht festgelegt, basiert die Höhe der Sprechblase auf der Eigenschaft Anzahl der Zeilen der Sprechblase. Dieses Stilbit ist auf 1 festgelegt, und ein Versuch, [**iagentballoonex:: setnumlines**](iagentballoonex--setnumlines.md) zu verwenden, führt zu einem Fehler.

Wenn das **Autohide** -Stilbit festgelegt ist, wird die Wort Sprechblase nach einem kurzen Timeout automatisch ausgeblendet. Wenn Sie nicht festgelegt ist, wird die [**Sprech**](speak-method.md) Blase bis zu einem neuen Sprech-oder ansichtenbefehl angezeigt, das Zeichen ist ausgeblendet, oder der Benutzer [**klickt oder zieht**](think-method.md) das Zeichen.

Wenn das **autopace** -Stilbit festgelegt ist, wird die Ausgabe von der Word-Sprechblase basierend auf der aktuellen Ausgabe Rate, z. b. einem Wort, auf der Grundlage der aktuellen Ausgabe Rate Wenn die Ausgabe die Größe der Sprechblase überschreitet, wird für den vorherigen Text automatisch ein Bildlauf durchgeführt. Wenn nicht festgelegt, wird der gesamte Text, der in einer " [**sprechen**](speak-method.md) "-oder " [**Think**](think-method.md) "-Anweisung enthalten

Die Style-Eigenschaft der Sprechblase kann auch dann festgelegt werden, wenn der Benutzer die Anzeige der Sprechblase mithilfe der Eigenschaften Seite des Microsoft-Agents deaktiviert hat.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.

Die Standardwerte für diese stilbits basieren auf Ihren Einstellungen, wenn das Zeichen mit dem Microsoft-Agent-Zeichen-Editor kompiliert wird.

## <a name="see-also"></a>Weitere Informationen

[**Iagentballoonex:: GetStyle**](iagentballoonex--getstyle.md)


 

 






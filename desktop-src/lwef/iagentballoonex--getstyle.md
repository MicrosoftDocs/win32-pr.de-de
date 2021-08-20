---
title: IAgentBalloonEx GetStyle
description: IAgentBalloonEx GetStyle
ms.assetid: 7c6a7260-073b-4535-b8e7-a8cae9aae9ef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a9acc8ab86b824339a8d97d4e25a4f7c9a2105d741ff1b10570f2cb3d8bf715
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117693251"
---
# <a name="iagentballoonexgetstyle"></a>IAgentBalloonEx::GetStyle

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT GetStyle(
   long * plStyle,  // address of style settings
);
```

Ruft die Stileinstellungen des Wortsprechblasens des Zeichens ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="plStyle"></span><span id="plstyle"></span><span id="PLSTYLE"></span>*plStyle*
</dt> <dd>

Stileinstellungen für den Wortsprechblasen, die eine Kombination aus einem der folgenden Werte sein können:



| Wert                                                                           | Beschreibung                                                 |
|---------------------------------------------------------------------------------|-------------------------------------------------------------|
| **const unsigned short** **\_ \_ BALLOONON = 0x00000001;**<br/> | Die Sprechblase wird für die Ausgabe unterstützt.                        |
| **const unsigned short** **BALLOON STYLE \_ \_ SIZETOTEXT = 0x0000002;**           | Die Höhe des Sprechblasens wird so angepasst, dass die Textausgabe berücksichtigt wird. |
| **const unsigned short** **BALLOON STYLE \_ \_ AUTOHIDE = 0x00000004;**            | Die Sprechblase wird automatisch ausgeblendet.                        |
| **const unsigned short** **BALLOON STYLE \_ \_ AUTOPACE = 0x00000008;**            | Die Geschwindigkeit der Textausgabe basiert auf der Ausgaberate.          |



 

</dd> </dl>

Wenn das **BalloonOn-Stilbit** festgelegt ist, wird die Wortsprechblase angezeigt, wenn die [**Speak-**](speak-method.md) oder [**Think-Methode**](think-method.md) verwendet wird, es sei denn, der Benutzer überschreibt seine Anzeige über das Eigenschaftenblatt des Microsoft-Agents. Wenn kein Sprechblasen festgelegt ist, wird keine Sprechblase angezeigt.

Wenn das **SizeToText-Formatbit** festgelegt ist, wird die Höhe des Sprechblasens automatisch auf die aktuelle Größe des Texts festgelegt, der in der [**Speak-**](speak-method.md) oder [**Think-Methode**](think-method.md) angegeben ist. Wenn diese Einstellung nicht festgelegt ist, basiert die Höhe des Sprechblasens auf der Eigenschafteneinstellung Anzahl der Zeilen des Sprechblases. Dieses Formatbit ist auf 1 festgelegt, und der Versuch, [**IAgentBalloonEx::SetNumLines**](iagentballoonex--setnumlines.md) zu verwenden, führt zu einem Fehler.

Wenn das **AutoHide-Stilbit** festgelegt ist, wird der Wortsprechblasen nach einem kurzen Time out automatisch ausgeblendet. Wenn die Sprechblase nicht festgelegt ist, wird die Sprechblase angezeigt, bis ein neuer [**Speak-**](speak-method.md) oder [**Think-Aufruf**](think-method.md) erfolgt, das Zeichen ausgeblendet ist oder der Benutzer auf das Zeichen klickt oder es zieht.

Wenn das **AutoPace-Formatbit** festgelegt ist, nimmt das Wort balloon die Geschwindigkeit der Ausgabe basierend auf der aktuellen Ausgaberate ein, z. B. ein Wort nach dem anderen. Wenn die Ausgabe die Größe des Sprechblasens überschreitet, wird automatisch ein Bildlauf für den vorherigen Text durchgeführt. Wenn nicht festgelegt, wird der gesamte Text, der in einer [**Speak-**](speak-method.md) oder [**Think-Anweisung**](think-method.md) enthalten ist, gleichzeitig angezeigt.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch Ihre Clientanwendung. Die Einstellung wirkt sich nicht auf andere Clients des Zeichens oder anderer Zeichen Ihrer Clientanwendung aus.

Die Standardwerte für diese Stilbits basieren auf den Einstellungen, wenn das Zeichen über den Microsoft-Agent-Zeichen-Editor kompiliert wird.

## <a name="see-also"></a>Weitere Informationen

[**IAgentBalloonEx::SetStyle**](iagentballoonex--setstyle.md)


 

 






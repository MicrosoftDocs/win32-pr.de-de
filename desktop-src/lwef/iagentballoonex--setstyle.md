---
title: IAgentBalloonEx SetStyle
description: IAgentBalloonEx SetStyle
ms.assetid: 5be569b7-8a2d-437b-b5db-401af343bc78
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3961bf5f32aad10c662d9dc2943f32b60fad485621b5adce32e2036e6d2d4275
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118478540"
---
# <a name="iagentballoonexsetstyle"></a>IAgentBalloonEx::SetStyle

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT SetStyle(
   long lStyle,  // style settings
);
```

Ruft die Stileinstellungen des Wortsprechblasens des Zeichens ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="lStyle"></span><span id="lstyle"></span><span id="LSTYLE"></span>*lStyle*
</dt> <dd>

Stileinstellungen für den Wortsprechblasen, die eine Kombination aus einem der folgenden Werte sein können:



| Wert                                                                            | BESCHREIBUNG                                                 |
|----------------------------------------------------------------------------------|-------------------------------------------------------------|
| **const unsigned short** **BALLOON STYLE \_ \_ BALLOONON = 0x00000001;**<br/>  | Die Sprechblase wird für die Ausgabe unterstützt.                        |
| **const unsigned short** **BALLOON STYLE \_ \_ SIZETOTEXT = 0x0000002;**<br/> | Die Höhe des Sprechblasens wird so angepasst, dass die Textausgabe berücksichtigt wird. |
| **const unsigned short** **BALLOON STYLE \_ \_ AUTOHIDE = 0x00000004;**<br/>  | Die Sprechblase wird automatisch ausgeblendet.                        |
| **const unsigned short** **BALLOON STYLE \_ \_ AUTOPACE = 0x00000008;**<br/>  | Die Geschwindigkeit der Textausgabe basiert auf der Ausgaberate.          |



 

</dd> </dl>

Wenn das **BalloonOn-Stilbit** festgelegt ist, wird die Wortsprechblase angezeigt, wenn die [**Speak-**](speak-method.md) oder [**Think-Methode**](think-method.md) verwendet wird, es sei denn, der Benutzer überschreibt seine Anzeige im Eigenschaftenblatt des Microsoft-Agents. Wenn kein Sprechblasen festgelegt ist, wird keine Sprechblase angezeigt.

Wenn das **SizeToText-Formatbit** festgelegt ist, wird die Höhe des Sprechblasens automatisch auf die aktuelle Größe des Texts festgelegt, der in der [**Speak-**](speak-method.md) oder [**Think-Methode**](think-method.md) angegeben ist. Wenn diese Einstellung nicht festgelegt ist, basiert die Höhe des Sprechblasens auf der Eigenschafteneinstellung Anzahl der Zeilen des Sprechblases. Dieses Formatbit ist auf 1 festgelegt, und der Versuch, [**IAgentBalloonEx::SetNumLines**](iagentballoonex--setnumlines.md) zu verwenden, führt zu einem Fehler.

Wenn das **AutoHide-Stilbit** festgelegt ist, wird die Wortsprechblase nach einem kurzen Timeout automatisch ausgeblendet. Wenn die Sprechblase nicht festgelegt ist, wird die Sprechblase angezeigt, bis ein neuer [**Speak-**](speak-method.md) oder [**Think-Aufruf**](think-method.md) erfolgt, das Zeichen ausgeblendet ist oder der Benutzer auf das Zeichen klickt oder es zieht.

Wenn das **AutoPace-Formatbit** festgelegt ist, nimmt das Wort balloon die Geschwindigkeit der Ausgabe basierend auf der aktuellen Ausgaberate ein, z. B. ein Wort nach dem anderen. Wenn die Ausgabe die Größe des Sprechblasens überschreitet, wird automatisch ein Bildlauf für den vorherigen Text durchgeführt. Wenn nicht festgelegt, wird der gesamte Text, der in einer [**Speak-**](speak-method.md) oder [**Think-Anweisung**](think-method.md) enthalten ist, gleichzeitig angezeigt.

Die Style-Eigenschaft des Balloons kann auch dann festgelegt werden, wenn der Benutzer die Anzeige des Balloons mithilfe des Eigenschaftenblatts des Microsoft-Agents deaktiviert hat.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch Ihre Clientanwendung. Die Einstellung wirkt sich nicht auf andere Clients des Zeichens oder anderer Zeichen Ihrer Clientanwendung aus.

Die Standardwerte für diese Stilbits basieren auf ihren Einstellungen, wenn das Zeichen mit dem Microsoft-Agent-Zeichen-Editor kompiliert wird.

## <a name="see-also"></a>Weitere Informationen

[**IAgentBalloonEx::GetStyle**](iagentballoonex--getstyle.md)


 

 






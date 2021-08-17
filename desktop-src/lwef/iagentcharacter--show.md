---
title: IAgentCharacter Show
description: IAgentCharacter Show
ms.assetid: 5f13dcef-3777-41eb-827f-6162bad71a2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcefb523bd2e9f477991bf6fa8352382f75b6bc76d93aab2e7f5c9e8cc1358dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117693002"
---
# <a name="iagentcharactershow"></a>IAgentCharacter::Show

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

``` syntax
HRESULT Show(
   long bFast,      // play Showing state animation flag
   long * pdwReqID  // address of request ID
);
```

Zeigt ein Zeichen an.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war. Wenn die Funktion zurückgegeben wird, *enthält pdwReqID* die ID der Anforderung.

<dl> <dt>

<span id="bFast"></span><span id="bfast"></span><span id="BFAST"></span>*Frühstück*
</dt> <dd>

Anzeige des Zustandsanimationsflags. Wenn dieser Parameter true **ist,** wird die **Animation Zum** Anzeigen des Zustands wiedergibt, nachdem das Zeichen sichtbar gemacht wurde. False **gibt an,** dass die Animation nicht abspielt.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Adresse einer Variablen, die die [**Anforderungs-ID**](/windows/desktop/lwef/iagentcharacter--show) anzeigen empfängt.

</dd> </dl>

Vermeiden Sie es, *den bFast-Parameter* auf **True** zu setzen, ohne vorher eine Animation wiedergibt. Andernfalls wird der Zeichenrahmen zwar angezeigt, es muss jedoch kein Bild angezeigt werden. Beachten Sie insbesondere Folgendes: Wenn Sie [**MoveTo**](iagentcharacter--moveto.md) aufrufen, wenn das Zeichen nicht sichtbar ist, wird keine Animation wieder verwendet. Wenn Sie daher die **Show-Methode aufrufen,** bei der *bFast* auf **True** festgelegt ist, wird kein Bild angezeigt. Wenn Sie ausblenden [](/windows/desktop/lwef/iagentcharacter--hide)aufrufen und  dann mit *bFast* auf **True** festlegen, wird kein Bild angezeigt.

Wenn Sie das HTTP-Protokoll für den Zugriff auf Zeichen- und  Animationsdaten verwenden, verwenden Sie die [**Prepare-Methode,**](/windows/desktop/lwef/iagentcharacter--prepare) um die Verfügbarkeit der Anzeigezustandsanimation sicherzustellen, bevor Sie diese Methode aufrufen.

## <a name="see-also"></a>Weitere Informationen

[**IAgentCharacter::Hide**](iagentcharacter--hide.md)


 

 
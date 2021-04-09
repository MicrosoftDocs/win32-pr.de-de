---
title: Iagentballoon getFont-Unterstreichung
description: Iagentballoon getFont-Unterstreichung
ms.assetid: 19886e94-8095-4650-bd88-34ea9d96ddaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5acf35453209679dc96c85b3017fbe76b19d53b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037549"
---
# <a name="iagentballoongetfontunderline"></a>Iagentballoon:: getFont-Unterstreichung

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetFontUnderline(
   long * pbFontUnderline  // address of variable for underline setting
);                         // for font displayed in word balloon 
```

Gibt an, ob die in einer Word-Sprechblase verwendete Schriftart den Stil für die Unterstreichung hat.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbFontUnderline"></span><span id="pbfontunderline"></span><span id="PBFONTUNDERLINE"></span>*pbfont-Unterstreichung*
</dt> <dd>

Die Adresse eines Werts, der **true** empfängt, wenn der Stil der Schrift Unterstreichung festgelegt ist, andernfalls **false** .

</dd> </dl>

Der Schriftart Stil, der in einer Wort Sprechblase verwendet wird, wird im Microsoft-Agent-Zeichen-Editor definiert. Sie kann nicht von einer Anwendung geändert werden. Der Benutzer kann jedoch die Schriftart Einstellungen für alle Zeichen überschreiben, indem er das Eigenschaften Blatt Microsoft-Agent verwendet.

 

 





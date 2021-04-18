---
title: Iagentballoon setfontcharset
description: Iagentballoon setfontcharset
ms.assetid: ce1b152d-c8af-47ec-9e6b-5768dbcf3566
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6202aa144d13c3c7435be03721a3f8fd4878b93
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340652"
---
# <a name="iagentballoonsetfontcharset"></a>Iagentballoon:: setfontcharset

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT SetFontCharSet(
   short sFontCharSet  // character set displayed in word balloon
); 
```

Legt den Zeichensatz der Schriftart fest, die in der Word-Sprechblase angezeigt wird.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="sFontCharSet"></span><span id="sfontcharset"></span><span id="SFONTCHARSET"></span>*sfontcharset*
</dt> <dd>

Der Zeichensatz der Schriftart. Im folgenden finden Sie einige allgemeine Einstellungen für Value:



|     |                                                                                        |
|-----|----------------------------------------------------------------------------------------|
| 0   | Standard mäßige Windows-Zeichen (ANSI).                                                    |
| 1   | Standardzeichensatz.                                                                 |
| 2   | Der Symbol Zeichensatz.                                                              |
| 128 | Doppelbyte-Zeichensatz (DBCS), der für die japanische Version von Windows eindeutig ist.            |
| 129 | Doppelbyte-Zeichensatz (DBCS), der für die koreanische Version von Windows eindeutig ist.              |
| 134 | Doppelbyte-Zeichensatz (DBCS), der für die vereinfachte chinesische Version von Windows eindeutig ist.  |
| 136 | Doppelbyte-Zeichensatz (DBCS), der für die traditionelle chinesische Version von Windows eindeutig ist. |
| 255 | Erweiterte Zeichen, die normalerweise von MS-DOS-Anwendungen angezeigt werden                          |



 

</dd> </dl>

Weitere Zeichensatz Werte finden Sie in der Platform SDK-Dokumentation.

Der Standardzeichensatz, der in der Wort Sprechblase eines Zeichens verwendet wird, wird im Microsoft-Agent-Zeichen-Editor definiert. Sie können es mit [**iagentballoon:: setfontcharset**](https://www.bing.com/search?q=**IAgentBalloon::SetFontCharSet**)ändern. Der Benutzer kann jedoch die Zeichensatz Einstellung für alle Zeichen überschreiben, indem er das Eigenschaften Blatt Microsoft-Agent verwendet. Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.

## <a name="see-also"></a>Weitere Informationen

[**Iagentballoon:: getfontcharset**](iagentballoon--getfontcharset.md)


 

 





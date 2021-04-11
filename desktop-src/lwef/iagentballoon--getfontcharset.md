---
title: Iagentballoon getfontcharset
description: Iagentballoon getfontcharset
ms.assetid: 1ab5767a-31e3-449c-b242-f20b11336ca0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54f544df6c09fb00d346015b610751dd23738820
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206932"
---
# <a name="iagentballoongetfontcharset"></a>Iagentballoon:: getfontcharset

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetFontCharSet(
   short * psFontCharSet  // character set displayed in word balloon
); 
```

Gibt den Zeichensatz der Schriftart an, die in einer Wort Sprechblase angezeigt wird.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="psFontCharSet"></span><span id="psfontcharset"></span><span id="PSFONTCHARSET"></span>*psfontcharset*
</dt> <dd>

Die Adresse eines Werts, der den Zeichensatz der Schriftart empfängt. Im folgenden finden Sie einige allgemeine Einstellungen für Value:



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

Der Standardzeichensatz, der in der Wort Sprechblase eines Zeichens verwendet wird, wird im Microsoft-Agent-Zeichen-Editor definiert. Sie können es mit [**iagentballoon:: setfontcharset**](iagentballoon--setfontcharset.md)ändern. Der Benutzer kann jedoch die Zeichensatz Einstellung für alle Zeichen überschreiben, indem er das Eigenschaften Blatt Microsoft-Agent verwendet.

## <a name="see-also"></a>Weitere Informationen

[**Iagentballoon:: setfontcharset**](iagentballoon--setfontcharset.md)


 

 





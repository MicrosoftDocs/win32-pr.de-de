---
title: IAgentBalloon SetFontCharSet
description: IAgentBalloon SetFontCharSet
ms.assetid: ce1b152d-c8af-47ec-9e6b-5768dbcf3566
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18cc462895ff9f19f7e722660608a268af13446f
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120205"
---
# <a name="iagentballoonsetfontcharset"></a>IAgentBalloon::SetFontCharSet

\[Microsoft Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT SetFontCharSet(
   short sFontCharSet  // character set displayed in word balloon
); 
```

Legt den Zeichensatz der Schriftart fest, die im Wort balloon angezeigt wird.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="sFontCharSet"></span><span id="sfontcharset"></span><span id="SFONTCHARSET"></span>*sFontCharSet*
</dt> <dd>

Der Zeichensatz der Schriftart. Im Folgenden finden Sie einige allgemeine Einstellungen für value:



| Wert    | Zeichensatz                                                                                       |
|-----|----------------------------------------------------------------------------------------|
| 0   | Standard-Windows-Zeichen (ANSI).                                                    |
| 1   | Standardzeichensatz.                                                                 |
| 2   | Der Symbolzeichensatz.                                                              |
| 128 | Doppel-Byte-Zeichensatz (DBCS), der für die japanische Version von Windows eindeutig ist.            |
| 129 | Doppel-Byte-Zeichensatz (DBCS), der für die koreanische Version von Windows eindeutig ist.              |
| 134 | Doppel-Byte-Zeichensatz (Double-Byte Character Set, DBCS), der für die vereinfachte chinesische Version von Windows eindeutig ist.  |
| 136 | Doppel-Byte-Zeichensatz (DBCS), der für die traditionelle chinesische Version von Windows eindeutig ist. |
| 255 | Erweiterte Zeichen werden in der Regel von MS-DOS-Anwendungen angezeigt.                          |



 

</dd> </dl>

Weitere Zeichensatzwerte finden Sie in der Dokumentation zum Platform SDK.

Der Standardzeichensatz, der in der Wortsprechblase eines Zeichens verwendet wird, wird im Microsoft Agent-Zeichen-Editor definiert. Sie können es mit [**IAgentBalloon::SetFontCharSet ändern.**](https://www.bing.com/search?q=**IAgentBalloon::SetFontCharSet**) Der Benutzer kann jedoch die Zeichensatzeinstellung für alle Zeichen mithilfe des Microsoft Agent-Eigenschaftenblatts überschreiben. Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch Ihre Clientanwendung. Die Einstellung wirkt sich nicht auf andere Clients des Zeichens oder anderer Zeichen Ihrer Clientanwendung aus.

## <a name="see-also"></a>Weitere Informationen

[**IAgentBalloon::GetFontCharSet**](iagentballoon--getfontcharset.md)


 

 





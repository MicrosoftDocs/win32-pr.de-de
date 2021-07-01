---
title: IAgentBalloon GetFontCharSet
description: IAgentBalloon GetFontCharSet
ms.assetid: 1ab5767a-31e3-449c-b242-f20b11336ca0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f809fbd83e44259c96184c9f364a85151ec9ddde
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120405"
---
# <a name="iagentballoongetfontcharset"></a>IAgentBalloon::GetFontCharSet

\[Microsoft Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT GetFontCharSet(
   short * psFontCharSet  // character set displayed in word balloon
); 
```

Gibt den Zeichensatz der Schriftart an, die in einer Wortsprechblase angezeigt wird.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="psFontCharSet"></span><span id="psfontcharset"></span><span id="PSFONTCHARSET"></span>*psFontCharSet*
</dt> <dd>

Die Adresse eines Werts, der den Zeichensatz der Schriftart empfängt. Im Folgenden finden Sie einige allgemeine Einstellungen für value:



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

Der Standardzeichensatz, der in der Wortsprechblase eines Zeichens verwendet wird, wird im Microsoft Agent-Zeichen-Editor definiert. Sie können es mithilfe von [**IAgentBalloon::SetFontCharSet ändern.**](iagentballoon--setfontcharset.md) Der Benutzer kann jedoch die Zeichensatzeinstellung für alle Zeichen mithilfe des Microsoft Agent-Eigenschaftenblatts überschreiben.

## <a name="see-also"></a>Weitere Informationen

[**IAgentBalloon::SetFontCharSet**](iagentballoon--setfontcharset.md)


 

 





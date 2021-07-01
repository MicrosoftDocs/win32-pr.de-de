---
title: IAgentCharacterEx GetLanguageID
description: IAgentCharacterEx GetLanguageID
ms.assetid: 4e4e5342-edf9-480b-a9c3-e2626fd89e76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d847bf392709b2433b045a357a703173e2de454
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120646"
---
# <a name="iagentcharacterexgetlanguageid"></a>IAgentCharacterEx::GetLanguageID

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT GetLanguageID(
   long * plangID  // address of language ID setting
);
```

Ruft den Sprach-ID-Satz für das Zeichen ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="plangID"></span><span id="plangid"></span><span id="PLANGID"></span>*plangID*
</dt> <dd>

Adresse einer Variablen, die die Sprach-ID-Einstellung für das Zeichen empfängt.

</dd> </dl>

Eine long-Ganzzahl, die die Sprach-ID für das Zeichen angibt. Die Sprach-ID (LANGID) für ein Zeichen ist ein von Windows definierter 16-Bit-Wert, der aus einer primären Sprach-ID und einer sekundären Sprach-ID besteht. Die folgenden Beispiele sind Werte für einige Sprachen. Informationen zum Ermitteln der Werte in anderen Sprachen finden Sie in der Dokumentation zum Plattform-SDK.



| Sprache              | id     | Sprache              | id     |
|-----------------------|--------|-----------------------|--------|
| Arabisch (Saudi)        | 0x0401 | Italienisch               | 0x0410 |
| Baskisch                | 0x042d | Japanisch              | 0x0411 |
| Chinesisch (vereinfacht)  | 0x0804 | Koreanisch                | 0x0412 |
| Chinesisch (traditionell) | 0x0404 | Norwegisch             | 0x0414 |
| Kroatisch              | 0x041A | Polnisch                | 0x0415 |
| Tschechisch                 | 0x0405 | Portugiesisch (Portugal) | 0x0816 |
| Dänisch                | 0x0406 | Portugiesisch (Brasilien)   | 0x0416 |
| Niederländisch                 | 0x0413 | Rumänisch              | 0x0418 |
| Englisch (Großbritannien)     | 0x0809 | Russisch               | 0x0419 |
| Englisch (USA)          | 0x0409 | Slowakisch             | 0x041B |
| Finnisch               | 0x040B | Slowenisch             | 0x0424 |
| Französisch                | 0x040C | Spanisch               | 0x0C0A |
| Deutsch                | 0x0407 | Schwedisch               | 0x041D |
| Griechisch                 | 0x0408 | Thai                  | 0x041E |
| Hebräisch                | 0x040D | Türkisch               | 0x041F |
| Ungarisch             | 0x040E |                       |        |



 

Wenn Sie diese Sprach-ID für das Zeichen nicht festlegen, ist die Sprach-ID des Zeichens die aktuelle Systemsprach-ID.

Diese Einstellung bestimmt auch die Sprache für die TTS-Ausgabe, den Text der Sprachsprechblasen, die Befehle im Popupmenü des Zeichens und die Spracherkennungs-Engine. Verwenden Sie [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md) oder [**IAgentCharacterEx::GetTTSModeID,**](iagentcharacterex--getttsmodeid.md)um zu ermitteln, ob eine kompatible Spracherkennungs-Engine für die Sprache des Zeichens verfügbar ist.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch Ihre Clientanwendung. Die Einstellung wirkt sich nicht auf andere Clients des Zeichens oder anderer Zeichen Ihrer Clientanwendung aus.

> [!Note]  
> Wenn die Sprach-ID auf eine Sprache festgelegt ist, die bidirektionalen Text unterstützt (z. B. Arabisch oder Hebräisch), aber auf dem System, auf dem Ihre Anwendung ausgeführt wird, keine bidirektionale Unterstützung installiert ist, wird Text im Wortsprechblasen in logischer statt in der Anzeigereihenfolge angezeigt.

 

## <a name="see-also"></a>Weitere Informationen

[**IAgentCharacterEx:SetLanguageID**](iagentcharacterex--setlanguageid.md), [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md)


 

 





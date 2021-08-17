---
title: IAgentCharacterEx GetLanguageID
description: IAgentCharacterEx GetLanguageID
ms.assetid: 4e4e5342-edf9-480b-a9c3-e2626fd89e76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb0eeee052111ef0acbb843f4362ca0bfd3b40ab7d154ef0c46c43f6c2d0e0f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105548"
---
# <a name="iagentcharacterexgetlanguageid"></a>IAgentCharacterEx::GetLanguageID

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

``` syntax
HRESULT GetLanguageID(
   long * plangID  // address of language ID setting
);
```

Ruft die Sprach-ID ab, die für das Zeichen festgelegt ist.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="plangID"></span><span id="plangid"></span><span id="PLANGID"></span>*plangID*
</dt> <dd>

Adresse einer Variablen, die die Sprach-ID-Einstellung für das Zeichen empfängt.

</dd> </dl>

Eine lange ganze Zahl, die die Sprach-ID für das Zeichen angibt. Die Sprach-ID (LANGID) für ein Zeichen ist ein von Windows definierter 16-Bit-Wert, der aus einer primären Und einer sekundären Sprach-ID besteht. Die folgenden Beispiele sind Werte für einige Sprachen. Informationen zum Ermitteln der Werte für andere Sprachen finden Sie in der Dokumentation zum Plattform-SDK.



| Sprache              | ID     | Sprache              | ID     |
|-----------------------|--------|-----------------------|--------|
| Arabisch (Arabisch)        | 0x0401 | Italienisch               | 0x0410 |
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
| Griechisch                 | 0x0408 | Thailändisch                  | 0x041E |
| Hebräisch                | 0x040D | Türkisch               | 0x041F |
| Ungarisch             | 0x040E |                       |        |



 

Wenn Sie diese Sprach-ID nicht für das Zeichen festlegen, ist die Sprach-ID des Zeichens die aktuelle Systemsprach-ID.

Diese Einstellung bestimmt auch die Sprache für die TTS-Ausgabe, den Text der Wortsprechblasen, die Befehle im Popupmenü des Zeichens und die Spracherkennungs-Engine. Verwenden Sie [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md) oder [**IAgentCharacterEx::GetTTSModeID,**](iagentcharacterex--getttsmodeid.md)um zu ermitteln, ob eine kompatible Spracherkennungs-Engine für die Sprache des Zeichens verfügbar ist.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch Ihre Clientanwendung. Die Einstellung wirkt sich nicht auf andere Clients des Zeichens oder anderer Zeichen Ihrer Clientanwendung aus.

> [!Note]  
> Wenn die Sprach-ID auf eine Sprache festgelegt ist, die bidirektionalen Text unterstützt (z. B. Arabisch oder Hebräisch), aber das System, auf dem Ihre Anwendung ausgeführt wird, keine bidirektionale Unterstützung installiert ist, wird Text im Wortsprechblasen in logischer statt in der Anzeigefolge angezeigt.

 

## <a name="see-also"></a>Weitere Informationen

[**IAgentCharacterEx:SetLanguageID**](iagentcharacterex--setlanguageid.md), [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md)


 

 





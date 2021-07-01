---
title: IAgentCharacterEx SetLanguageID
description: IAgentCharacterEx SetLanguageID
ms.assetid: 064f4c3c-1871-4372-9796-5b53f05c6d9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 036e1d41878adaae878a5961b45d190971d790af
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119005"
---
# <a name="iagentcharacterexsetlanguageid"></a>IAgentCharacterEx::SetLanguageID

\[Microsoft Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT SetLanguageID(
   long langID  // language ID setting of character
); 
```

Legt die Sprach-ID fest, die für das Zeichen festgelegt ist.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*Langid*
</dt> <dd>

Die Sprach-ID-Einstellung für das Zeichen.

</dd> </dl>

Eine lange ganze Zahl, die die Sprach-ID für das Zeichen angibt. Die Sprach-ID (LANGID) für ein Zeichen ist ein von Windows definierter 16-Bit-Wert, der aus einer primären Sprach-ID und einer sekundären Sprach-ID besteht. Sie können die folgenden Werte für die angegebenen Sprachen verwenden. Weitere Informationen finden Sie in der Platform SDK-Dokumentation.



| Sprache              | id     |  Sprache             | id     |
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
| Griechisch                 | 0x0408 | Thai                  | 0x041E |
| Hebräisch                | 0x040D | Türkisch               | 0x041F |
| Ungarisch             | 0x040E |                       |        |



 

Wenn Sie die Sprach-ID für das Zeichen nicht festlegen, ist ihre Sprach-ID die aktuelle Systemsprach-ID, wenn die entsprechende -Agent-Sprach-DLL installiert ist. Andernfalls ist die Sprache des Zeichens Englisch (USA).

Diese Eigenschaft bestimmt auch die Sprache für den Text der Wortsprechblasen, die Befehle im Popupmenü des Zeichens und die Spracherkennungs-Engine. Außerdem wird die Standardsprache für die TTS-Ausgabe bestimmt. Verwenden Sie [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md) oder [**IAgentCharacterEx::GetTTSModeID,**](iagentcharacterex--getttsmodeid.md)um zu ermitteln, ob eine kompatible Sprach-Engine für die Sprache des Zeichens verfügbar ist.

Wenn Sie versuchen, die Sprach-ID für ein Zeichen und die Agent-Sprachressourcen, die Codepage oder eine Anzeigeschriftart für die Sprach-ID nicht verfügbar zu machen, gibt der -Agent einen Fehler zurück, und die Sprach-ID des Zeichens bleibt bei seiner letzten Einstellung. Das Festlegen dieser Eigenschaft gibt keinen Fehler zurück, wenn keine übereinstimmenden Sprach-Engines für die Sprache sind.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch Ihre Clientanwendung. Die Einstellung wirkt sich nicht auf andere Clients des Zeichens oder anderer Zeichen Ihrer Clientanwendung aus.

> [!Note]  
> Wenn Sie die Sprach-ID des Zeichens auf eine Sprache festlegen, die bidirektionalen Text unterstützt (z. B. Arabisch oder Hebräisch), aber das System, auf dem Ihre Anwendung ausgeführt wird, keine bidirektionale Unterstützung installiert ist, wird Text im Wortsprechblasen in logischer statt in der Anzeigerichtung angezeigt.

 

## <a name="see-also"></a>Weitere Informationen

[**IAgentCharacterEx:GetLanguageID**](iagentcharacterex--getlanguageid.md), [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md)


 

 





---
title: Iagentcharakteriex getlanguageid
description: Iagentcharakteriex getlanguageid
ms.assetid: 4e4e5342-edf9-480b-a9c3-e2626fd89e76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9679538f93d779acc6272dccada824585c4449f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037319"
---
# <a name="iagentcharacterexgetlanguageid"></a>Iagentcharakteriex:: getlanguageid

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetLanguageID(
   long * plangID  // address of language ID setting
);
```

Ruft die Sprachen-ID ab, die für das Zeichen festgelegt ist.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="plangID"></span><span id="plangid"></span><span id="PLANGID"></span>*plangid*
</dt> <dd>

Adresse einer Variablen, die die Sprach-ID-Einstellung für das Zeichen empfängt.

</dd> </dl>

Eine lange ganze Zahl, die die Sprach-ID für das Zeichen angibt. Die Sprach-ID (langid) für ein Zeichen ist ein 16-Bit-Wert, der von Windows definiert wird und aus einer primär Sprachen-ID und einer sekundären Sprach-ID besteht. Die folgenden Beispiele sind Werte für einige Sprachen. Informationen zum Bestimmen der Werte anderer Sprachen finden Sie in der Platform SDK-Dokumentation.



|                       |        |                       |        |
|-----------------------|--------|-----------------------|--------|
| Arabisch (Saudi)        | 0x0401 | Italienisch               | 0x0410 |
| Baskisch                | 0x042d | Japanisch              | 0x0411 |
| Chinesisch (vereinfacht)  | 0x0804 | Koreanisch                | 0x0412 |
| Chinesisch (traditionell) | 0x0404 | Norwegisch             | 0x0414 |
| Kroatisch              | 0x041a | Polnisch                | 0x0415 |
| Tschechisch                 | 0x0405 | Portugiesisch (Portugal) | 0x0816 |
| Dänisch                | 0x0406 | Portugiesisch (Brasilien)   | 0x0416 |
| Niederländisch                 | 0x0413 | Rumänisch              | 0x0418 |
| Englisch (Großbritannien)     | 0x0809 | Russisch               | 0x0419 |
| Englisch (USA)          | 0x0409 | Slowakisch             | 0x041b |
| Finnisch               | 0x040b | Slowenisch             | 0x0424 |
| Französisch                | 0x040c | Spanisch               | 0x0C0A |
| Deutsch                | 0x0407 | Schwedisch               | 0x041d |
| Griechisch                 | 0x0408 | Thailändisch                  | 0x041E |
| Hebräisch                | 0x040d | Türkisch               | 0x041f |
| Ungarisch             | 0x040e |                       |        |



 

Wenn Sie diese Sprach-ID nicht für das Zeichen festlegen, wird die Sprach-ID des Zeichens als aktuelle Systemsprachen-ID verwendet.

Diese Einstellung bestimmt auch die Sprache für die TTS-Ausgabe, den Word-Sprechblasen Text, die Befehle im Popupmenü des Zeichens und die Spracherkennungs-Engine. Verwenden Sie [**iagentcharakteriex:: getsrmodeid**](iagentcharacterex--getsrmodeid.md) oder [**iagentcharakteriex:: getttsmodeid**](iagentcharacterex--getttsmodeid.md), um zu bestimmen, ob eine kompatible sprach Erkennungs-Engine für die Sprache des Zeichens verfügbar ist.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.

> [!Note]  
> Wenn die Sprach-ID auf eine Sprache festgelegt ist, die bidirektionalen Text (z. b. Arabisch oder Hebräisch) unterstützt, aber das System, auf dem Ihre Anwendung ausgeführt wird, nicht über eine bidirektionale Unterstützung verfügt, wird Text in der Wort Sprechblase in logischer und nicht in

 

## <a name="see-also"></a>Weitere Informationen

[**Iagentcharakteriex: setlanguageid**](iagentcharacterex--setlanguageid.md), [**iagentcharakteriex:: gezrmodeid**](iagentcharacterex--getsrmodeid.md), [**iagentcharakteriex:: getttmodeid**](iagentcharacterex--getttsmodeid.md)


 

 





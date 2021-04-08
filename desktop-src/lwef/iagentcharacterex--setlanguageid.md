---
title: Iagentcharakteriex setlanguageid
description: Iagentcharakteriex setlanguageid
ms.assetid: 064f4c3c-1871-4372-9796-5b53f05c6d9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ec8a396c174fd251b1cc7ac8d7e9696c9b9f2d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708879"
---
# <a name="iagentcharacterexsetlanguageid"></a>Iagentcharakteriex:: setlanguageid

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT SetLanguageID(
   long langID  // language ID setting of character
); 
```

Legt die für das Zeichen festgelegte Sprach-ID fest.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*
</dt> <dd>

Die Sprach-ID-Einstellung für das Zeichen.

</dd> </dl>

Eine lange ganze Zahl, die die Sprach-ID für das Zeichen angibt. Die Sprach-ID (langid) für ein Zeichen ist ein 16-Bit-Wert, der von Windows definiert wird und aus einer primär Sprachen-ID und einer sekundären Sprach-ID besteht. Die folgenden Werte können für die angegebenen Sprachen verwendet werden. Weitere Informationen finden Sie in der Platform SDK-Dokumentation.



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



 

Wenn Sie die Sprach-ID für das Zeichen nicht festlegen, wird die Sprach-ID der aktuellen Systemsprachen-ID angezeigt, wenn die entsprechende dll der Agent-Sprache installiert ist. Andernfalls ist die Sprache des Zeichens Englisch (USA).

Diese Eigenschaft bestimmt auch die Sprache für den Word-Sprechblasen Text, die Befehle im Popupmenü des Zeichens und die Spracherkennungs-Engine. Außerdem wird die Standardsprache für die TTS-Ausgabe bestimmt. Wenn Sie feststellen möchten, ob eine kompatible Sprach-Engine für die Sprache des Zeichens verfügbar ist, verwenden Sie [**iagentcharakteriex:: gezrmodeid**](iagentcharacterex--getsrmodeid.md) oder [**iagentcharakteriex:: getttmodeid**](iagentcharacterex--getttsmodeid.md).

Wenn Sie versuchen, die Sprach-ID für ein Zeichen und die Agent-Sprachressourcen festzulegen, ist die Codepage oder eine Anzeige Schriftart für die Sprach-ID nicht verfügbar. der-Agent gibt einen Fehler zurück, und die Sprach-ID des Zeichens bleibt bei der letzten Einstellung. Das Festlegen dieser Eigenschaft gibt keinen Fehler zurück, wenn keine übereinstimmenden Sprach-Engines für die Sprache vorhanden sind.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.

> [!Note]  
> Wenn Sie die Sprach-ID des Zeichens auf eine Sprache festlegen, die bidirektionalen Text (z. b. Arabisch oder Hebräisch) unterstützt, aber das System, auf dem Ihre Anwendung ausgeführt wird, nicht über eine bidirektionale Unterstützung verfügt, wird Text in der Wort Sprechblase anstelle der Anzeigereihenfolge

 

## <a name="see-also"></a>Weitere Informationen

[**Iagentcharakteriex: getlanguageid**](iagentcharacterex--getlanguageid.md), [**iagentcharakteriex:: gezrmodeid**](iagentcharacterex--getsrmodeid.md), [**iagentcharakteriex:: getttmodeid**](iagentcharacterex--getttsmodeid.md)


 

 





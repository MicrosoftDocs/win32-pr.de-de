---
description: Ein Doppel-Byte-Zeichensatz (Double-Byte Character Set, DBCS), auch als &\# 0034;erweiterter 8-Bit-Zeichensatz&0034; bezeichnet, ist ein erweiterter \# Single-Byte-Zeichensatz (Single-Byte Character Set, SBCS), der als Codepage implementiert wird.
ms.assetid: df049d22-02e2-48b2-8b74-52f71c00c549
title: Doppel-Byte-Zeichensätze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dbef827b91c5ed2468b06f759883c0ba0b874e74038871227aabe0f65f1a046
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147663"
---
# <a name="double-byte-character-sets"></a>Doppel-Byte-Zeichensätze

Ein Doppel-Byte-Zeichensatz (Double-Byte Character Set, DBCS), auch als "erweiterter 8-Bit-Zeichensatz" bezeichnet, ist ein erweiterter [Single-Byte-Zeichensatz (Single-Byte Character Set,](single-byte-character-sets.md) SBCS), der als Codepage implementiert wird. DBCSs wurden ursprünglich entwickelt, um den SBCS-Entwurf auf Sprachen wie Japanisch und Chinesisch zu erweitern. Einige Zeichen in einem DBCS, einschließlich der Ziffern und Buchstaben, die zum Schreiben von Englisch verwendet werden, verfügen über Einzel-Byte-Codewerte. Andere Zeichen, z. B. chinesische Ideogramme oder japanische Kanji, verfügen über Doppel-Byte-Codewerte. Ein DBCS kann entweder einer Windows Codepage oder einer OEM-Codepage entsprechen. Eine DBCS-Codepage kann auch eine nicht native Codepage enthalten, z. B. eine EBCDIC-Codepage. Definitionen dieser Codepages finden Sie unter [CodePages](code-pages.md).

> [!Note]  
> Neue Windows sollten [Unicode](unicode.md) verwenden, um inkonsistente Codepages zu vermeiden und die Lokalisierung zu erleichtern. Einige ältere Protokolle erfordern jedoch möglicherweise die Verwendung von DBCS-Codepages. Jede DBCS-Codepage unterstützt unterschiedliche Zeichen, aber keine Seite unterstützt die gesamte Breite der von Unicode bereitgestellten Zeichen. Jede DBCS-Codepage unterstützt eine andere Teilmenge, die unterschiedlich codiert ist. Daten, die von einer DBCS-Codepage in eine andere konvertiert werden, unterliegen einer Beschädigung, da derselbe Datenwert auf verschiedenen Codepages ein anderes Zeichen codieren kann. Daten, die von Unicode in DBCS konvertiert werden, können datenverlusten, da eine bestimmte Codepage möglicherweise nicht jedes Zeichen darstellen kann, das in diesen bestimmten Unicode-Daten verwendet wird.

 

Um eine DBCS-Zeichenfolge zu interpretieren, muss eine Anwendung am Anfang der Zeichenfolge beginnen und vorwärts suchen. Sie verfolgt nach, wenn ein Lead-Byte in der Zeichenfolge vor sich geht, und behandelt das nächste Byte als den nachdenkenden Teil desselben Zeichens. Wenn die Anwendung die Zeichenfolge einfach nach und nach durchsucht und auf ein Byte trifft, das der Codewert zu sein scheint, der einen zurücken Schrägstrich ("") darstellt, kann dieses Byte einfach das Nach-Byte eines \\ Zwei-Byte-Zeichens sein. Die Anwendung kann nicht einfach ein Byte sichern, um zu sehen, ob das vorherige Byte ein Lead-Byte ist, da dieser Bytewert möglicherweise sowohl als Lead-Byte als auch als Nach-Byte verwendet werden kann. Daher hat die Anwendung im Wesentlichen das gleiche Problem wie mit dem möglichen zurücken Schrägstrich. Anders ausgedrückt: Suchvorgänge in Teilzeichenfolgen sind bei DBCS wesentlich komplizierter als bei SBCSs oder Unicode. Entsprechend müssen Anwendungen, die dbcs unterstützen, anstelle der [**StrStr-Funktion**](https://msdn.microsoft.com/library/z9da80kz(v=VS.71).aspx) spezielle Funktionen wie [ \_ mbsstr](/cpp/c-runtime-library/reference/strstr-wcsstr-mbsstr-mbsstr-l)verwenden.

Ihre Anwendungen verwenden DBCS Windows Codepages mit den "A"-Versionen Windows Funktionen. Weitere Informationen [finden Sie unter Konventionen für Funktionsprototypen](conventions-for-function-prototypes.md) [und Codepages.](code-pages.md) Um eine DBCS-Codepage zu identifizieren, kann eine Anwendung die [**GetCPInfo-**](/windows/desktop/api/Winnls/nf-winnls-getcpinfo) oder [**GetCPInfoEx-Funktion**](/windows/desktop/api/Winnls/nf-winnls-getcpinfoexa) verwenden. Eine Anwendung kann die [**IsDBCSLeadByte-Funktion**](/windows/desktop/api/Winnls/nf-winnls-isdbcsleadbyte) verwenden, um zu bestimmen, ob ein angegebener Wert als Leadbyte eines 2-Byte-Zeichens verwendet werden kann. Darüber hinaus kann eine Anwendung die [**Funktionen MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) und [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) verwenden, um Unicode- und DBCS-Zeichenfolgen zu zuordnen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zeichensätze](character-sets.md)
</dt> <dt>

[Einzel-Byte-Zeichensätze](single-byte-character-sets.md)
</dt> </dl>

 

 

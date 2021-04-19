---
description: Ein Doppelbyte-Zeichensatz (Double-Byte Character Set, DBCS), der auch als &\# 0034, erweiterter 8-Bit-Zeichensatz&\# 0034; bezeichnet wird, ist ein erweiterter Single-Byte-Zeichensatz (SBCS), der als Codepage implementiert ist.
ms.assetid: df049d22-02e2-48b2-8b74-52f71c00c549
title: Doppelbyte-Zeichensätze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 431b762b19f5531644e4bbaace548f34245c9d5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366139"
---
# <a name="double-byte-character-sets"></a>Doppelbyte-Zeichensätze

Ein Doppelbyte-Zeichensatz (DBCS), der auch als "Erweiterter 8-Bit-Zeichensatz" bezeichnet wird, ist ein erweiterter [Single-Byte-Zeichensatz](single-byte-character-sets.md) (SBCS), der als Codepage implementiert ist. Dbcss wurde ursprünglich entwickelt, um den SBCS-Entwurf so zu erweitern, dass er Sprachen wie Japanisch und Chinesisch behandelt. Einige Zeichen in einem DBCS, einschließlich der Ziffern und Buchstaben, die zum Schreiben von Englisch verwendet werden, verfügen über Einzel Byte-Codewerte. Andere Zeichen, wie z. b. chinesische Ideogramme oder japanische Kanji, haben Doppelbyte-Codewerte. Ein DBCS kann entweder einer Windows-Codepage oder einer OEM-Codepage entsprechen. Eine DBCS-Codepage kann auch eine nicht systemeigene Codepage einschließen, z. b. eine EBCDIC-Codepage. Definitionen dieser Codepages finden Sie unter [Codepages](code-pages.md).

> [!Note]  
> Neue Windows-Anwendungen sollten [Unicode](unicode.md) verwenden, um die Inkonsistenzen von unterschiedlichen Codepages und eine einfache Lokalisierung zu vermeiden. Einige Legacy Protokolle erfordern jedoch möglicherweise die Verwendung von DBCS-Codepages. Jede DBCS-Codepage unterstützt verschiedene Zeichen, aber keine Seite unterstützt die vollständige Breite der Zeichen, die von Unicode bereitgestellt werden. Jede DBCS-Codepage unterstützt eine andere Teilmenge, unterschiedlich codiert. Daten, die von einer DBCS-Codepage in eine andere konvertiert werden, unterliegen Beschädigungen, da der gleiche Datenwert auf unterschiedlichen Codepages ein anderes Zeichen codieren kann. Daten, die von Unicode in DBCS konvertiert werden, unterliegen Datenverlusten, da eine bestimmte Codepage möglicherweise nicht jedes Zeichen darstellen kann, das in den einzelnen Unicode-Daten verwendet wird.

 

Um eine DBCS-Zeichenfolge zu interpretieren, muss eine Anwendung am Anfang der Zeichenfolge beginnen und die Überprüfung fortzusetzen. Es wird nachverfolgt, wenn ein führendes Byte in der Zeichenfolge gefunden wird, und das nächste Byte wird als nachfolgende Teil desselben Zeichens behandelt. Wenn die Anwendung die Zeichenfolge einfach nacheinander scannt und auf ein Byte stößt, das als Codewert angezeigt wird, der einen umgekehrten Schrägstrich (" \\ ") darstellt, ist dieses Byte möglicherweise einfach das nachfolgende Byte eines 2-Byte-Zeichens. Die Anwendung kann nicht einfach ein Byte sichern, um festzustellen, ob das vorangehende Byte ein führendes Byte ist, da dieser Bytewert möglicherweise als führendes Byte und als nachfolgendes Byte verwendet werden kann. Folglich hat die Anwendung im Grunde das gleiche Problem wie mit dem möglichen umgekehrten Schrägstrich. Anders ausgedrückt: die Suche nach Teil Zeichenfolgen ist mit einem DBCS weitaus komplizierter als mit SBCSs oder Unicode. Dementsprechend müssen Anwendungen, die ein DBCS unterstützen, anstelle der " [**strestr**](https://msdn.microsoft.com/library/z9da80kz(v=VS.71).aspx) "-Funktion spezielle Funktionen, wie z. b. [ \_ mbsstr](/cpp/c-runtime-library/reference/strstr-wcsstr-mbsstr-mbsstr-l), verwenden.

Ihre Anwendungen verwenden DBCS-Windows-Codepages mit den "A"-Versionen von Windows Functions. Weitere Informationen finden Sie unter [Konventionen für Funktionsprototypen](conventions-for-function-prototypes.md) und [Codepages](code-pages.md). Um eine DBCS-Codepage zu identifizieren, kann eine Anwendung die [**GetCPInfo**](/windows/desktop/api/Winnls/nf-winnls-getcpinfo) -Funktion oder die [**getcpinfoex**](/windows/desktop/api/Winnls/nf-winnls-getcpinfoexa) -Funktion verwenden. Eine Anwendung kann die [**isdbcsleadbyte**](/windows/desktop/api/Winnls/nf-winnls-isdbcsleadbyte) -Funktion verwenden, um zu bestimmen, ob ein bestimmter Wert als führendes Byte eines 2-Byte-Zeichens verwendet werden kann. Außerdem kann eine Anwendung die Funktionen [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) und [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) zum Zuordnen zwischen Unicode-und DBCS-Zeichen folgen verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zeichensätze](character-sets.md)
</dt> <dt>

[Einzel Byte-Zeichensätze](single-byte-character-sets.md)
</dt> </dl>

 

 

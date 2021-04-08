---
description: Bei einem Einzel Byte-Zeichensatz (SBCS) handelt es sich um eine Zuordnung von 256 einzelnen Zeichen zu ihren identifizierenden Codewerten, die als Codepage implementiert werden.
ms.assetid: 53f74132-91aa-4257-846a-f6e1f2f9ae0b
title: Einzel Byte-Zeichensätze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5618b191b83e33333dce2a290d8c9a7181233df4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960841"
---
# <a name="single-byte-character-sets"></a>Einzel Byte-Zeichensätze

Bei einem Einzel Byte-Zeichensatz (SBCS) handelt es sich um eine Zuordnung von 256 einzelnen Zeichen zu ihren identifizierenden Codewerten, die als Codepage implementiert werden. SBCS können entweder einer Windows-Codepage oder einer OEM-Codepage entsprechen. Eine SBCS-Codepage kann auch eine nicht systemeigene Codepage einschließen, z. b. eine EBCDIC-Codepage. Definitionen dieser Codepages finden Sie unter [Codepages](code-pages.md).

> [!Note]  
> Neue Windows-Anwendungen sollten [Unicode](unicode.md) verwenden, um die Inkonsistenzen von unterschiedlichen Codepages und eine einfache Lokalisierung zu vermeiden. Einige Legacy Protokolle erfordern jedoch die Verwendung eines SBCS. Jede SBCS-Codepage unterstützt unterschiedliche Zeichen, aber keine Seite unterstützt die vollständige Breite von Zeichen, die von Unicode bereitgestellt werden. Jede SBCS-Codepage unterstützt eine andere Teilmenge, unterschiedlich codiert. Daten, die von einer SBCS-Codepage in eine andere konvertiert werden, unterliegen Beschädigungen, da der gleiche Datenwert auf unterschiedlichen Codepages ein anderes Zeichen codieren kann. Daten, die von Unicode in SBCS konvertiert werden, unterliegen Datenverlusten, da eine bestimmte Codepage nicht jedes Zeichen darstellen kann, das in den einzelnen Unicode-Daten verwendet wird.

 

Ihre Anwendungen verwenden SBCS-Windows-Codepage mit den "A"-Versionen von Windows Functions. Weitere Informationen finden Sie unter [Konventionen für Funktionsprototypen](conventions-for-function-prototypes.md) und [Codepages](code-pages.md). Um eine SBCS-Codepage zu identifizieren, kann eine Anwendung die [**GetCPInfo**](/windows/desktop/api/Winnls/nf-winnls-getcpinfo) -Funktion oder die [**getcpinfoex**](/windows/desktop/api/Winnls/nf-winnls-getcpinfoexa) -Funktion verwenden. Außerdem kann eine Anwendung die Funktionen [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) und [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) zum Zuordnen zwischen Unicode-und SBCS-Zeichen folgen verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zeichensätze](character-sets.md)
</dt> <dt>

[Doppelbyte-Zeichensätze](double-byte-character-sets.md)
</dt> </dl>

 

 




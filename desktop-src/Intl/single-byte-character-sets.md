---
description: Ein Einzel byte-Zeichensatz (Single-Byte Character Set, SBCS) ist eine Zuordnung von 256 einzelnen Zeichen zu ihren identifizierenden Codewerten, die als Codepage implementiert werden.
ms.assetid: 53f74132-91aa-4257-846a-f6e1f2f9ae0b
title: Einzel byte-Zeichensätze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22bb0150dfaf2e3b8e8251530fd5e90e7b1ede3b3597d344e5efb192fa96ed36
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130230"
---
# <a name="single-byte-character-sets"></a>Einzel byte-Zeichensätze

Ein Einzel byte-Zeichensatz (Single-Byte Character Set, SBCS) ist eine Zuordnung von 256 einzelnen Zeichen zu ihren identifizierenden Codewerten, die als Codepage implementiert werden. Ein SBCS kann entweder einer Windows Codepage oder einer OEM-Codepage entsprechen. Eine SBCS-Codepage kann auch eine nicht native Codepage enthalten, z. B. eine EBCDIC-Codepage. Definitionen dieser Codepages finden Sie unter [Codepages](code-pages.md).

> [!Note]  
> Neue Windows Anwendungen sollten [Unicode](unicode.md) verwenden, um die Inkonsistenzen verschiedener Codepages zu vermeiden und die Lokalisierung zu vereinfachen. Einige Legacyprotokolle erfordern jedoch die Verwendung eines SBCS. Jede SBCS-Codepage unterstützt unterschiedliche Zeichen, aber keine Seite unterstützt die gesamte Breite von Zeichen, die von Unicode bereitgestellt werden. Jede SBCS-Codepage unterstützt eine andere Teilmenge, die unterschiedlich codiert ist. Daten, die von einer SBCS-Codepage in eine andere konvertiert werden, sind beschädigt, da derselbe Datenwert auf verschiedenen Codepages ein anderes Zeichen codieren kann. Daten, die aus Unicode in SBCS konvertiert werden, unterliegen Datenverlusten, da eine bestimmte Codepage möglicherweise nicht jedes Zeichen darstellen kann, das in diesen bestimmten Unicode-Daten verwendet wird.

 

Ihre Anwendungen verwenden SBCS Windows Codepages mit den "A"-Versionen von Windows Funktionen. Weitere Informationen finden Sie unter [Konventionen für Funktionsprototypen](conventions-for-function-prototypes.md) und [Codepages.](code-pages.md) Um eine SBCS-Codepage zu identifizieren, kann eine Anwendung die [**Funktion GetCPInfo**](/windows/desktop/api/Winnls/nf-winnls-getcpinfo) oder [**GetCPInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcpinfoexa) verwenden. Darüber hinaus kann eine Anwendung die Funktionen [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) und [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) verwenden, um unicode- und SBCS-Zeichenfolgen zuzuordnen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zeichensätze](character-sets.md)
</dt> <dt>

[Doppel-Byte-Zeichensätze](double-byte-character-sets.md)
</dt> </dl>

 

 




---
description: Ein Sprachbezeichner ist eine internationale Numerische Standardabkürzung für die Sprache in einem Land oder einer geografischen Region.
ms.assetid: 076e2a43-256a-4646-a5c8-1d48ab08ce1a
title: Sprachen-IDs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6245101099b5df5c192af60a977ede88412f95cca8afda9270b7aba6e1c41ad2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120106980"
---
# <a name="language-identifiers"></a>Sprachen-IDs

Ein Sprachbezeichner ist eine internationale Numerische Standardabkürzung für [die Sprache](locales-and-languages.md) in einem Land oder einer geografischen Region. Jede Sprache verfügt über einen eindeutigen Sprachbezeichner (LangID-Datentyp), einen 16-Bit-Wert, der aus einem Bezeichner der primären Sprache und einem Untersprachbezeichner besteht. Weitere Informationen zu Sprachbezeichnern finden Sie unter [Sprachbezeichnerkonst konstanten und Zeichenfolgen](language-identifier-constants-and-strings.md).

Ein Sprachbezeichner wird mithilfe des [**MAKELANGID-Makros**](/windows/desktop/api/Winnt/nf-winnt-makelangid) erstellt. Die folgende Abbildung zeigt das Format der Bits in einem Sprachbezeichner.

``` syntax
+-------------------------+-------------------------+
|     SubLanguage ID      |   Primary Language ID   |
+-------------------------+-------------------------+
15                    10  9                         0   bit
```

Im Folgenden finden Sie vordefinierte Sprachbezeichner:

-   LANG \_ SYSTEM \_ DEFAULT. Die Standardsprache des Betriebssystems.
-   LANG \_ USER \_ DEFAULT. Sprache des aktuellen Benutzers.

Ihre Anwendung kann die aktuellen Sprachbezeichner mithilfe der mehrsprachige Benutzeroberfläche [abrufen.](multilingual-user-interface.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Lokal und Sprachen](locales-and-languages.md)
</dt> <dt>

[Sprachbezeichnerkonstatoren und Zeichenfolgen](language-identifier-constants-and-strings.md)
</dt> <dt>

[Multilingual User Interface](multilingual-user-interface.md)
</dt> <dt>

[**MAKELANGID**](/windows/desktop/api/Winnt/nf-winnt-makelangid)
</dt> </dl>

 

 




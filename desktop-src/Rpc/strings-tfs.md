---
title: Zeichenfolgen (RPC)
description: Drei Zeichenfolgentypen und Remoteprozeduraufruf (RPC).
ms.assetid: 186cabeb-ea3f-4213-ba71-53afe91e6e14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b15467ed5a1425443cbc5a53cf35aba71725c5db68c542c292af38eb0d238cfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924836"
---
# <a name="strings-rpc"></a>Zeichenfolgen (RPC)

Es gibt drei Zeichenfolgentypen, die durch die folgenden endenden Unterzeichenfolgen im Formatzeichen bezeichnet werden.



| type                  | TEILZEICHENFOLGE |
|-----------------------|-----------|
| Zeichenfolge      | Cstring   |
| Breitzeichenzeichenfolge | WSTRING   |
| Zeichenfolgen-orientierte Struktur | SSTRING   |



 

### <a name="nonconformant-strings"></a>Nicht konforme Zeichenfolgen

Ein Beispiel für eine nicht konforme Zeichenfolge ist eine **\[ Zeichenfolge \]** in einem Array fester Größe.

``` syntax
FC_CSTRING | FC _WSTRING 
FC_PAD 
string_size<2>
```

### <a name="conformant-strings"></a>Konforme Zeichenfolgen

``` syntax
FC_C_CSTRING | FC_C_WSTRING
FC_PAD 
```

– oder –

``` syntax
FC_C_CSTRING | FC_C_WSTRING 
FC_STRING_SIZED 
conformance_description<> 
```

Das erste Format beschreibt allgemeine Zeichenfolgen, z. B. ein **\[ \] Zeichenfolgen-Char-Argument.** \* Eine konforme Zeichenfolge mit angepasster Größe hat die zweite Beschreibung.

Die Konformitätsbeschreibung ist<> Korrelationsdeskriptor und hat 4 oder 6 Bytes, je nachdem, ob \_ [**/robust**](/windows/desktop/Midl/-robust) verwendet wird.

### <a name="structure-strings"></a>Strukturzeichenfolgen

Im Folgenden finden Sie eine nicht konforme Zeichenfolgen-konforme Struktur:

``` syntax
FC_SSTRING 
element_size<1> 
number_of_elements<2>
```

Konforme Zeichenfolgen-konforme Struktur:

``` syntax
FC_C_SSTRING 
element_size<1>
```

–oder –

``` syntax
FC_C_SSTRING 
elements_size<1> 
FC_STRING_SIZED FC_PAD 
conformance_description<>
```

Letztere Beschreibung ist für eine Zeichenfolgenstruktur mit Zeichenfolgengröße.

 

 
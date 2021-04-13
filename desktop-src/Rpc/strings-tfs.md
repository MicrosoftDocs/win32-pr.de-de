---
title: Zeichen folgen (RPC)
description: Drei Zeichen folgen Typen und Remote Prozedur Aufruf (RPC).
ms.assetid: 186cabeb-ea3f-4213-ba71-53afe91e6e14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 207e20b1c343ded17b5d62db2321bee380463f20
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316059"
---
# <a name="strings-rpc"></a>Zeichen folgen (RPC)

Es gibt drei Zeichen folgen Typen, die durch die folgenden enden untergeordneten Zeichen folgen im Formatzeichen angegeben werden.



| type                  | TEILZEICHENFOLGE |
|-----------------------|-----------|
| Zeichenfolge      | CSTRING   |
| Breit Zeichen-Zeichenfolge | WSTRING   |
| Zeichen folgen fähige Struktur | SString   |



 

### <a name="nonconformant-strings"></a>Nicht konforme Zeichen folgen

Ein Beispiel für eine nicht konforme Zeichenfolge ist eine **\[ Zeichen \]** Folge in einem Array mit fester Größe.

``` syntax
FC_CSTRING | FC _WSTRING 
FC_PAD 
string_size<2>
```

### <a name="conformant-strings"></a>Konforme Zeichen folgen

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

Das erste Format beschreibt gängige Zeichen folgen, wie z. b. ein **\[ String \]** char- \* Argument. Eine konforme Zeichenfolge mit der Größenanpassung hat die letztgenannte Beschreibung.

Die Übereinstimmungs \_ Beschreibung<> ist ein Korrelations Deskriptor, der abhängig davon, ob [**/robust**](/windows/desktop/Midl/-robust) verwendet wird, 4 oder 6 Bytes hat.

### <a name="structure-strings"></a>Struktur Zeichenfolgen

Im folgenden finden Sie eine nicht konforme Zeichen folgen fähige Struktur:

``` syntax
FC_SSTRING 
element_size<1> 
number_of_elements<2>
```

Konforme Zeichen folgen fähige Struktur:

``` syntax
FC_C_SSTRING 
element_size<1>
```

noch

``` syntax
FC_C_SSTRING 
elements_size<1> 
FC_STRING_SIZED FC_PAD 
conformance_description<>
```

Die letztgenannte Beschreibung ist für eine Struktur mit einer Größen Zeichenfolge zulässig.

 

 
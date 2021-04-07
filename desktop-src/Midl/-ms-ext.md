---
title: /ms_ext Schalter
description: Ab der mittleren l-Version 3,0 sind die vom MS ext-Schalter aktivierten Funktionen \_ nun der Standardmodus für den Mittelwert Compiler.
ms.assetid: 175894c9-fa7e-4907-966d-e9df5a8e2745
keywords:
- /ms_ext-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /ms_ext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbccf1205c9a937b78b08c46f31bc09aa3b75c70
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038846"
---
# <a name="ms_ext-switch"></a>/MS \_ ext-Schalter

Ab der mittleren l-Version 3,0 sind die vom **MS \_ ext** -Schalter aktivierten Funktionen nun der Standardmodus für den Mittelwert Compiler.

``` syntax
midl /ms_ext
```

## <a name="switch-options"></a>Optionen wechseln

Dieser Switch hat keine Parameter.

## <a name="remarks"></a>Bemerkungen

Wenn Sie den Schalter verwenden, wird kein Compilerfehler generiert, sodass Sie keine Verweise auf **/MS \_ ext** oder [**/c \_ ext**](-c-ext.md) aus einem vorhandenen Makefile entfernen müssen.

Die folgenden Microsoft-Erweiterungen für OSF-DCE sind nun standardmäßig verfügbar:

-   Schnittstellendefinitionen für OLE-Objekte. Weitere Informationen zu den für OLE-Schnittstellen generierten Dateien finden Sie unter für [eine COM-Schnittstelle generierte Dateien](files-generated-for-a-com-interface.md) .
-   Ein [**\[ Rückruf \]**](callback.md) Attribut, das eine statische Rückruffunktion auf dem Client angibt.
-   [**cpp- \_ Zitat**](cpp-quote.md)(*\_ Zeichenfolge* in Anführungszeichen) und [**\# pragma-Mittell- \_ Echo**](pragma.md)
-   [**WCHAR \_ t**](wchar-t.md) -breit Zeichen Typen,-Konstanten und-Zeichen folgen
-   [**enumerationsinitialisierung**](enum.md) (Sparse-Enumeratoren)
-   Ausdrücke als Größen-und diskriminatorspezifiker
-   [Behandeln von Erweiterungen](/windows/desktop/Rpc/microsoft-rpc-binding-handle-extensions)
-   [Vererbung von Attributtypen](/windows/desktop/Rpc/pointer-attribute-type-inheritance)
-   [Mehrere Schnittstellen](/windows/desktop/Rpc/registering-interfaces)
-   Definitionen außerhalb des Schnittstellen Blocks
-   Sie können [direktionale Attribute](/windows/desktop/Rpc/directional-parameter-attributes) \[ [**in**](in.md), [**out**](out-idl.md) weglassen.\]

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine Syntax der Mittell-Befehlszeile](general-midl-command-line-syntax.md)
</dt> <dt>

[Vererbung von Attributtypen](/windows/desktop/Rpc/pointer-attribute-type-inheritance)
</dt> <dt>

[**/APP- \_ Konfiguration**](-app-config.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> </dl>

 

 
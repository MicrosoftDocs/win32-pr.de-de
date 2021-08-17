---
title: /ms_ext Schalter
description: Ab MIDL Version 3.0 sind die durch den ms ext-Schalter aktivierten Features jetzt der \_ Standardmodus für den MIDL-Compiler.
ms.assetid: 175894c9-fa7e-4907-966d-e9df5a8e2745
keywords:
- /ms_ext MIDL-Switch
topic_type:
- apiref
api_name:
- /ms_ext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73bee998e96d26c0f5bb2a1e0f28446433681a7175ff181556ad7976c58af356
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118644559"
---
# <a name="ms_ext-switch"></a>/ms \_ ext-Schalter

Ab MIDL Version 3.0 sind die durch den **ms \_ ext-Schalter** aktivierten Features jetzt der Standardmodus für den MIDL-Compiler.

``` syntax
midl /ms_ext
```

## <a name="switch-options"></a>Switch-Optionen

Dieser Schalter verfügt über keine Parameter.

## <a name="remarks"></a>Hinweise

Wenn Sie den Schalter verwenden, wird kein Compilerfehler generiert, sodass Sie keine Verweise auf **/ms \_ ext** oder [**/c \_ ext**](-c-ext.md) aus einem vorhandenen Makefile entfernen müssen.

Die folgenden Microsoft-Erweiterungen für OSF DCE sind jetzt standardmäßig verfügbar:

-   Schnittstellendefinitionen für OLE-Objekte. Weitere Informationen zu den für OLE-Schnittstellen generierten Dateien finden Sie unter [Für eine COM-Schnittstelle generierte Dateien.](files-generated-for-a-com-interface.md)
-   Ein [**\[ \] Rückrufattribut,**](callback.md) das eine statische Rückruffunktion auf dem Client an gibt
-   [**cpp \_ quote**](cpp-quote.md)(*quoted \_ string*) und [**\# pragma midl \_ echo**](pragma.md)
-   [**wchar \_ t-Breitzeichentypen,**](wchar-t.md) Konstanten und Zeichenfolgen
-   [**enum-Initialisierung**](enum.md) (Sparse-Enumeratoren)
-   Ausdrücke als Größen- und Diskriminatorspezifizierer
-   [Behandeln von Erweiterungen](/windows/desktop/Rpc/microsoft-rpc-binding-handle-extensions)
-   [Vererbung von Zeigerattributtypen](/windows/desktop/Rpc/pointer-attribute-type-inheritance)
-   [Mehrere Schnittstellen](/windows/desktop/Rpc/registering-interfaces)
-   Definitionen außerhalb des Schnittstellenblocks
-   Sie können [direktionale Attribute](/windows/desktop/Rpc/directional-parameter-attributes) \[ [**in**](in.md)auslassen. [](out-idl.md)\]

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Allgemeine MIDL-Befehlszeilensyntax](general-midl-command-line-syntax.md)
</dt> <dt>

[Vererbung von Zeigerattributtypen](/windows/desktop/Rpc/pointer-attribute-type-inheritance)
</dt> <dt>

[**/app \_ config**](-app-config.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> </dl>

 

 
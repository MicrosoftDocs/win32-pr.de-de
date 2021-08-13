---
title: /ms_ext Switch
description: Ab MIDL Version 3.0 sind die durch den ms ext-Switch aktivierten Funktionen \_ jetzt der Standardmodus für den MIDL-Compiler.
ms.assetid: 175894c9-fa7e-4907-966d-e9df5a8e2745
keywords:
- /ms_ext Switch MIDL
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
# <a name="ms_ext-switch"></a>Schalter "/ms \_ ext"

Ab MIDL Version 3.0 sind die durch den ms **\_ ext-Switch** aktivierten Funktionen jetzt der Standardmodus für den MIDL-Compiler.

``` syntax
midl /ms_ext
```

## <a name="switch-options"></a>Optionen wechseln

Dieser Schalter verfügt über keine Parameter.

## <a name="remarks"></a>Hinweise

Wenn Sie den Schalter verwenden, wird kein Compilerfehler generiert, sodass Sie verweise auf **/ms \_ ext** oder [**/c \_ ext**](-c-ext.md) nicht aus einem vorhandenen Makefile entfernen müssen.

Die folgenden Microsoft-Erweiterungen für OSF DCE sind jetzt standardmäßig verfügbar:

-   Schnittstellendefinitionen für OLE-Objekte. Weitere Informationen zu den für OLE-Schnittstellen generierten Dateien finden Sie unter [Für eine COM-Schnittstelle generierte Dateien.](files-generated-for-a-com-interface.md)
-   Ein [**\[ \] Rückrufattribut,**](callback.md) das eine statische Rückruffunktion auf dem Client angibt
-   [**\_ CPP-Anführungszeichen**](cpp-quote.md)*\_ (Zeichenfolge in Anführungszeichen)* und [**\# Pragma midl \_ echo**](pragma.md)
-   [**wchar \_ t**](wchar-t.md) Breitzeichentypen, Konstanten und Zeichenfolgen
-   [**Enumerationsinitialisierung**](enum.md) (Sparseenumeratoren)
-   Ausdrücke als Größen- und Diskriminatorspezifizierer
-   [Behandeln von Erweiterungen](/windows/desktop/Rpc/microsoft-rpc-binding-handle-extensions)
-   [Zeigerattributtypvererbung](/windows/desktop/Rpc/pointer-attribute-type-inheritance)
-   [Mehrere Schnittstellen](/windows/desktop/Rpc/registering-interfaces)
-   Definitionen außerhalb des Schnittstellenblocks
-   Sie können [richtungsale Attribute](/windows/desktop/Rpc/directional-parameter-attributes) \[ [**in**](in.md)auslassen. [](out-idl.md)\]

## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[Allgemeine MIDL-Befehlszeilensyntax](general-midl-command-line-syntax.md)
</dt> <dt>

[Zeigerattributtypvererbung](/windows/desktop/Rpc/pointer-attribute-type-inheritance)
</dt> <dt>

[**\_/app-Konfiguration**](-app-config.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> </dl>

 

 
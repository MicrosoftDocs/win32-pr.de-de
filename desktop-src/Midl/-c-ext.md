---
title: /c_ext Schalter
description: Dieser Schalter ist in Version 3,0 des Mittelwert Compilers veraltet. Wenn Sie jedoch den \_ Schalter c EXT verwenden, wird kein Compilerfehler generiert, sodass Sie keine Verweise auf/MS \_ ext oder/c \_ ext aus einem vorhandenen Makefile entfernen müssen.
ms.assetid: 3d4072ba-5563-4014-a4ed-2e3aa26bb00a
keywords:
- /c_ext-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /c_ext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8b3f179c2ce56b8e8ab6802b2d4bf5dd96c458e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106338425"
---
# <a name="c_ext-switch"></a>/c \_ ext-Schalter

Dieser Schalter ist in Version 3,0 des Mittelwert Compilers veraltet. Wenn Sie jedoch den Schalter **c \_ ext** verwenden, wird kein Compilerfehler generiert, sodass Sie keine Verweise auf [**/MS \_ ext**](-ms-ext.md) oder **/c \_ ext** aus einem vorhandenen Makefile entfernen müssen.

``` syntax
midl /c_ext
```

## <a name="switch-options"></a>Optionen wechseln

Dieser Switch hat keine Parameter.

## <a name="remarks"></a>Bemerkungen

Die folgenden Funktionen sind jetzt standardmäßig verfügbar:

-   Viele vorhandene Header Dateien definieren Typen mit Qualifizierern, z. b. " **weit** " und " **StdCall"**, die nicht Teil der DCE-IDL sind. Diese Compiler (und der mittlerer l-Compiler im DCE-Kompatibilitätsmodus) generieren Fehler, wenn Sie versuchen, diese Qualifizierer zu verarbeiten. Der-Mittell-Compiler ermöglicht das Kompilieren von IDL-Dateien, die diese Qualifizierer enthalten. Die Typqualifizierer beeinflussen nicht die Art und Weise, wie die Daten im Netzwerk übertragen werden.
-   Sie können direktionale Attribute wie z. b. [**\[ in \]**](in.md) oder [**\[ out \]**](out-idl.md)weglassen.

Die folgenden C-Spracherweiterungen werden im Standardmodus unterstützt:

-   Bitfelder in Strukturen und Unions
-   Kommentare, die mit zwei Schrägstrichen beginnen (//)
-   Externe Deklarationen
-   Prozeduren mit Ellipsen in der Parameterliste (...)
-   Auf 32-Bit-Plattformen ist [**int**](int.md) ein nativer 32-Bit-Basistyp. auf 16-Bit-Plattformen wird **int** erkannt, ist aber kein Remote barer Typ.
-   Typ [**" \* void**](void.md) ", der in Remote Vorgängen nicht verwendet wird
-   Typqualifizierer – einschließlich des Formulars mit dem ANSI-konforme Präfix – enthalten zwei Unterstriche: **cdecl**, **\_ \_ cdecl**, [**const**](const.md), **\_ \_ const**, **Export**, **\_ \_ Export**, **weit**, **\_ \_ weit**, **loadds**, **\_ \_ loadds**, **near**, **\_ \_ near**, **Pascal**, **\_ \_ Pascal**, **StdCall,** **\_ \_ StdCall,** **volatile** und **\_ \_ volatile**.

Weitere Informationen zu Deklarations Qualifizierern finden Sie in der Microsoft C/C++-Dokumentation.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**/APP- \_ Konfiguration**](-app-config.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[Allgemeine Syntax der Mittell-Befehlszeile](general-midl-command-line-syntax.md)
</dt> </dl>

 

 





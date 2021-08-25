---
title: /U-Schalter
description: Der Schalter /U entfernt alle vorherigen Definitionen eines Namens, indem der Name an den C-Präprozessor übergeben wird, als ob durch eine \undefine-Direktive.
ms.assetid: 3c253fb3-9448-4b55-bfd5-852e6feec280
keywords:
- /U switch MIDL
topic_type:
- apiref
api_name:
- /U
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9eab33e5aff861c1afecaafa52e04964ef286c5835e0a6992a3d369210f8927
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895770"
---
# <a name="u-switch"></a>/U-Schalter

Der **Schalter /U** entfernt alle vorherigen Definitionen eines Namens, indem der Name an den C-Präprozessor übergeben wird, als ob er durch eine **\# Undefine-Direktive wäre.**

``` syntax
midl /U name
```

## <a name="switch-options"></a>Switch-Optionen

<dl> <dt>

*name* 
</dt> <dd>

Gibt einen definierten Namen an, der wie durch eine Undefine-Direktive an den **\# C-Präprozessor übergeben werden** soll. Der Name ist vom C-Präprozessor vordefiniert oder zuvor vom Benutzer definiert.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Mehrere **/U-Direktiven** können in einer Befehlszeile verwendet werden. Leerzeichen zwischen dem **Schalter /U** und dem nicht definierten Namen sind optional.

Wenn der Schalter [**/cpp \_ cmd**](-cpp-cmd.md) vorhanden und der Schalter [**/cpp \_ opt**](-cpp-opt.md) nicht vorhanden ist, verkettet der MIDL-Compiler die vom /cpp cmd-Schalter angegebene Zeichenfolge mit den \_ Optionen [**/I,**](-i.md) [**/D**](-d.md)und **/U** und verwendet diese verkettete Zeichenfolge, um den C-Präprozessor für jede IDL- und ACF-Quelldatei auf aufruft. Der MIDL-Compilerschalter **/U** wird ignoriert, wenn der MIDL-Compilerschalter **/no \_ cpp** oder **/cpp \_ opt** angegeben wird.

## <a name="examples"></a>Beispiele

**midl /UUNICODE filename.idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine MIDL-Befehlszeilensyntax](general-midl-command-line-syntax.md)
</dt> <dt>

[**/cpp \_ cmd**](-cpp-cmd.md)
</dt> <dt>

[**/cpp \_ opt**](-cpp-opt.md)
</dt> <dt>

[**/D**](-d.md)
</dt> <dt>

[**/I**](-i.md)
</dt> <dt>

[**/no \_ cpp**](-no-cpp-nocpp.md)
</dt> </dl>

 

 





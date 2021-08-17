---
title: /D-Schalter
description: Der Schalter /D definiert einen Namen und einen optionalen Wert, die an den C-Präprozessor übergeben werden sollen, als ob durch eine \define-Direktive. In einer Befehlszeile können mehrere /D-Direktiven verwendet werden.
ms.assetid: 65642bf6-8e25-400b-8b1c-43513ab6b313
keywords:
- /D switch MIDL
topic_type:
- apiref
api_name:
- /D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa8bc01a978949ec0f0cc4ff78289a1cb442046966f1cea954c6b65cc232f563
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118385777"
---
# <a name="d-switch"></a>/D-Schalter

Der **Schalter /D** definiert einen Namen und einen optionalen Wert, der wie durch eine define-Direktive an den C-Präprozessor **\# übergeben werden** soll. In einer Befehlszeile können mehrere **/D-Direktiven** verwendet werden.

``` syntax
midl /Dname[=definition]
```

## <a name="switch-options"></a>Switch-Optionen

<dl> <dt>

*name* 
</dt> <dd>

Gibt einen definierten Namen an, der an den C-Präprozessor übergeben wird, wenn der [**Schalter /cpp \_ cmd**](-cpp-cmd.md) vorhanden und der [**Schalter /cpp \_ opt**](-cpp-opt.md) nicht vorhanden ist.

</dd> <dt>

*Definition* 
</dt> <dd>

Gibt einen Wert an, der dem definierten Namen zugeordnet ist.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Leerraum zwischen dem **Schalter /D** und dem definierten Namen ist optional.

Wenn der Schalter [**/cpp \_ cmd**](-cpp-cmd.md) vorhanden und der Schalter [**/cpp \_ opt**](-cpp-opt.md) nicht vorhanden ist, verkettet der MIDL-Compiler die vom **/cpp \_ cmd-Schalter** angegebene Zeichenfolge mit den [**Optionen /I,**](-i.md) **/D** und [**/U**](-u.md) und verwendet diese verkettete Zeichenfolge, um den C-Präprozessor für jede IDL- und ACF-Quelldatei auf aufruft.

Der MIDL-Compilerschalter **/D** wird ignoriert, wenn der MIDL-Compilerschalter [/no \_ cpp](-no-cpp-nocpp.md) oder [**/cpp \_ opt**](-cpp-opt.md) angegeben wird.

## <a name="examples"></a>Beispiele

**midl -DUNICODE filename.idl**

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**/cpp \_ cmd**](-cpp-cmd.md)
</dt> <dt>

[**/cpp \_ opt**](-cpp-opt.md)
</dt> <dt>

[**/I**](-i.md)
</dt> <dt>

[Allgemeine MIDL-Befehlszeilensyntax](general-midl-command-line-syntax.md)
</dt> <dt>

[**/no \_ cpp**](-no-cpp-nocpp.md)
</dt> <dt>

[**/U**](-u.md)
</dt> </dl>

 

 





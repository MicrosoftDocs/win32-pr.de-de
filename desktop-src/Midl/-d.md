---
title: /D-Schalter
description: Der Schalter/D definiert einen Namen und einen optionalen Wert, der an den C-Präprozessor als If by a \ define-Direktive übermittelt werden soll. Mehrere/D-Direktiven können in einer Befehlszeile verwendet werden.
ms.assetid: 65642bf6-8e25-400b-8b1c-43513ab6b313
keywords:
- /D-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d51cdcbecb5386acb1a97d933be8b25f68720ee
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104100971"
---
# <a name="d-switch"></a>/D-Schalter

Der Schalter **/D** definiert einen Namen und einen optionalen Wert, der an den C-Präprozessor wie bei einer **\# define** -Direktive übermittelt werden soll. Mehrere **/D** -Direktiven können in einer Befehlszeile verwendet werden.

``` syntax
midl /Dname[=definition]
```

## <a name="switch-options"></a>Optionen wechseln

<dl> <dt>

*name* 
</dt> <dd>

Gibt einen definierten Namen an, der an den C-Präprozessor übergeben wird, wenn der [**/cpp- \_ cmd**](-cpp-cmd.md) -Schalter vorhanden ist, und der [**/cpp- \_ opt**](-cpp-opt.md) -Switch ist nicht vorhanden.

</dd> <dt>

*Definition* 
</dt> <dd>

Gibt einen Wert an, der mit dem definierten Namen verknüpft ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Leerraum zwischen dem **/D** -Switch und dem definierten Namen ist optional.

Wenn der [**/cpp \_ -cmd**](-cpp-cmd.md) -Schalter vorhanden und der [**/cpp- \_ opt**](-cpp-opt.md) -Switch nicht ist, verkettet der Mittell-Compiler die durch den **/cpp \_ cmd** -Schalter angegebene Zeichenfolge mit den Optionen [**/I**](-i.md), **/D** und [**/U**](-u.md) und verwendet diese verketteten Zeichenfolge, um den C-Präprozessor für jede IDL-und ACF-Quelldatei aufzurufen.

Der Mittell-Compilerschalter **/D** wird ignoriert, wenn der Mittelwert-Compilerschalter [/No \_ cpp](-no-cpp-nocpp.md) oder [**/cpp \_ opt**](-cpp-opt.md) angegeben wird.

## <a name="examples"></a>Beispiele

**Dateiname-dunicode-Dateiname. idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**/cpp- \_ cmd**](-cpp-cmd.md)
</dt> <dt>

[**/cpp \_ Opt**](-cpp-opt.md)
</dt> <dt>

[**/I**](-i.md)
</dt> <dt>

[Allgemeine Syntax der Mittell-Befehlszeile](general-midl-command-line-syntax.md)
</dt> <dt>

[**/No \_ cpp**](-no-cpp-nocpp.md)
</dt> <dt>

[**/U**](-u.md)
</dt> </dl>

 

 





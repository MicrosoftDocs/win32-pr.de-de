---
title: /U-Schalter
description: Der/U-Schalter entfernt alle vorherigen Definitionen eines Namens, indem er den Namen an den C-Präprozessor übergibt, wie bei einer \ Präprozessordefinitionen aufheben-Direktive.
ms.assetid: 3c253fb3-9448-4b55-bfd5-852e6feec280
keywords:
- /U-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /U
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6d018d47dd5cbcc8192dee490965bd06c56d0e3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104100926"
---
# <a name="u-switch"></a>/U-Schalter

Der **/U** -Schalter entfernt alle vorherigen Definitionen eines Namens, indem er den Namen an den C-Präprozessor übergibt, wie bei einer **\# Präprozessordefinitionen aufheben** -Direktive.

``` syntax
midl /U name
```

## <a name="switch-options"></a>Optionen wechseln

<dl> <dt>

*name* 
</dt> <dd>

Gibt einen definierten Namen an, der an den C-Präprozessor als if durch eine **\# Präprozessordefinitionen aufheben** -Direktive übermittelt werden soll. Der Name wird vom C-Präprozessor oder zuvor vom Benutzer definiert.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Mehrere **/U** -Direktiven können in einer Befehlszeile verwendet werden. Leerraum zwischen dem Schalter **/U** und dem nicht definierten Namen ist optional.

Wenn der [**/cpp- \_ cmd**](-cpp-cmd.md) -Schalter vorhanden und [**der/cpp- \_ opt**](-cpp-opt.md) -Switch nicht ist, verkettet der Mittell-Compiler die durch den/cpp cmd-Schalter angegebene Zeichenfolge \_ mit den Optionen [**/I**](-i.md), [**/D**](-d.md)und **/U** und verwendet diese verketteten Zeichenfolge, um den C-Präprozessor für jede IDL-und ACF-Quelldatei aufzurufen. Der Mittell-Compilerschalter **/U** wird ignoriert, wenn der Mittelwert-Compilerschalter **/No \_ cpp** oder **/cpp \_ opt** angegeben wird.

## <a name="examples"></a>Beispiele

**Mittel l/UUNICODE Dateiname. idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine Syntax der Mittell-Befehlszeile](general-midl-command-line-syntax.md)
</dt> <dt>

[**/cpp- \_ cmd**](-cpp-cmd.md)
</dt> <dt>

[**/cpp \_ Opt**](-cpp-opt.md)
</dt> <dt>

[**/D**](-d.md)
</dt> <dt>

[**/I**](-i.md)
</dt> <dt>

[**/No \_ cpp**](-no-cpp-nocpp.md)
</dt> </dl>

 

 





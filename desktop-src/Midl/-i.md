---
title: /I-Schalter
description: Der Schalter/I gibt Verzeichnisse an, die nach importierten IDL-Dateien, enthaltenen Header Dateien und ACF-Dateien durchsucht werden sollen.
ms.assetid: cdb0a1c2-ff99-4060-be72-a54dd20dbf93
keywords:
- /I-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /I
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49ee48ad1e66caf5ed8facbf09ebf2c517c8c895
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104038084"
---
# <a name="i-switch"></a>/I-Schalter

Der Schalter **/I** gibt Verzeichnisse an, die nach importierten IDL-Dateien, enthaltenen Header Dateien und ACF-Dateien durchsucht werden sollen.

``` syntax
midl /I include_path
```

## <a name="switch-options"></a>Optionen wechseln

<dl> <dt>

*\_Includepfad* 
</dt> <dd>

Gibt mindestens ein Verzeichnis an, das Import-, include-und ACF-Dateien enthält. Leerraum zwischen dem **/I** -Switch und dem *include- \_ Pfad* ist optional. Trennen Sie mehrere Verzeichnisse durch ein Semikolon (;).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Mehrere Verzeichnisse können mit jedem **/I** -Schalter angezeigt werden, und es können mehr als ein **/I** -Schalter mit jedem mittleren Compileraufruf angezeigt werden. Verzeichnisse werden in der Reihenfolge durchsucht, in der Sie angegeben sind.

Die **/I** -switcheinstellung wird auch vom Mittelwert-Compiler an den c-Präprozessor des c-Compilers übermittelt. Wenn der [**/cpp \_ -cmd**](-cpp-cmd.md) -Schalter vorhanden und der [**/cpp- \_ opt**](-cpp-opt.md) -Switch nicht ist, verkettet der Mittell-Compiler die durch den **/cpp \_ cmd** -Schalter angegebene Zeichenfolge mit den Optionen **/I**, [**/D**](-d.md)und [**/U**](-u.md) und verwendet diese verketteten Zeichenfolge, um den C-Präprozessor für jede IDL-und ACF-Quelldatei aufzurufen. Der Mittell-Compilerschalter **/I** wird nicht an den Präprozessor übergeben, wenn der Mittelwert-Compilerschalter **/No \_ cpp** oder **/cpp \_ opt** angegeben wird.

In Microsoft-Betriebssystemumgebungen (64-Bit-Windows, 32-Bit-Windows, 16-Bit-Windows und MS-DOS) werden Verzeichnisse in der folgenden Reihenfolge durchsucht:

1.  Aktuelles Verzeichnis
2.  Durch den **/I** -Schalter angegebene Verzeichnisse (in der Reihenfolge, in der Sie dem Switch folgen)
3.  Von der include-Umgebungsvariable angegebene Verzeichnisse

Wenn Verzeichnisse mit dem Schalter **/I** angegeben werden, weist der [**/No \_ DEF \_ Idir**](-no-def-idir.md) -Schalter den Mittelwert Compiler an, das aktuelle Verzeichnis zu ignorieren, die von der INCLUDE-Umgebungsvariablen angegebenen Verzeichnisse zu ignorieren und nur die angegebenen Verzeichnisse zu durchsuchen.

Wenn keine Verzeichnisse mit dem **/I** -Schalter angegeben werden, weist der [**/No \_ DEF \_ Idir**](-no-def-idir.md) -Schalter den Mittelwert Compiler an, nur das aktuelle Verzeichnis zu durchsuchen.

## <a name="examples"></a>Beispiele

**Mittel l/I c: \\ include; c: \\ include \\ h/I \\ include2 filename. idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine Syntax der Mittell-Befehlszeile](general-midl-command-line-syntax.md)
</dt> <dt>

[**/acf**](-acf.md)
</dt> <dt>

[**/cpp- \_ cmd**](-cpp-cmd.md)
</dt> <dt>

[**/cpp \_ Opt**](-cpp-opt.md)
</dt> <dt>

[**/No \_ DEF \_ Idir**](-no-def-idir.md)
</dt> </dl>

 

 





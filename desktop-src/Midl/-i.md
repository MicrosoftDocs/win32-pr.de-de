---
title: /I-Schalter
description: Der Schalter /I gibt Verzeichnisse an, die nach importierten IDL-Dateien, eingeschlossenen Headerdateien und ACF-Dateien durchsucht werden sollen.
ms.assetid: cdb0a1c2-ff99-4060-be72-a54dd20dbf93
keywords:
- /I switch MIDL
topic_type:
- apiref
api_name:
- /I
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40fa167ea2ef95074d201ff460eb8eece79e43442a35985921c97455f086b46d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117992337"
---
# <a name="i-switch"></a>/I-Schalter

Der Schalter **/I** gibt Verzeichnisse an, die nach importierten IDL-Dateien, eingeschlossenen Headerdateien und ACF-Dateien durchsucht werden sollen.

``` syntax
midl /I include_path
```

## <a name="switch-options"></a>Optionen wechseln

<dl> <dt>

*\_Includepfad* 
</dt> <dd>

Gibt ein oder mehrere Verzeichnisse an, die Import-, Include- und ACF-Dateien enthalten. Leerzeichen zwischen dem **Schalter "/I"** und dem *\_ Includepfad* sind optional. Trennen Sie mehrere Verzeichnisse durch ein Semikolonzeichen (;).

</dd> </dl>

## <a name="remarks"></a>Hinweise

Mit jedem **/I-Switch** können mehrere Verzeichnisse angezeigt werden, und bei jedem MIDL-Compileraufruf können mehrere **/I-Schalter** angezeigt werden. Verzeichnisse werden in der Reihenfolge durchsucht, in der sie angegeben sind.

Die Schaltereinstellung **/I** wird auch vom MIDL-Compiler an den C-Präprozessor des C-Compilers übergeben. Wenn der [**Schalter /cpp \_ cmd**](-cpp-cmd.md) vorhanden ist und der [**Schalter /cpp \_ opt**](-cpp-opt.md) nicht ist, verkettet der MIDL-Compiler die vom **Schalter /cpp \_ cmd** angegebene Zeichenfolge mit den Optionen **/I,** [**/D**](-d.md)und [**/U**](-u.md) und verwendet diese verkettete Zeichenfolge, um den C-Präprozessor für jede IDL- und ACF-Quelldatei aufzurufen. Der MIDL-Compilerschalter **/I** wird nicht an den Präprozessor übergeben, wenn der MIDL-Compilerschalter **/no \_ cpp** oder **/cpp \_ opt** angegeben wird.

In Microsoft-Betriebssystemumgebungen (64-Bit-Windows, 32-Bit-Windows, 16-Bit-Windows und MS-DOS) werden Verzeichnisse in der folgenden Reihenfolge durchsucht:

1.  Aktuelles Verzeichnis
2.  Vom **Schalter /I** angegebene Verzeichnisse (in der Reihenfolge, in der sie dem Schalter folgen)
3.  Von der INCLUDE-Umgebungsvariablen angegebene Verzeichnisse

Wenn Verzeichnisse mit dem Schalter **/I** angegeben werden, weist der Schalter [**/no \_ def \_ idir**](-no-def-idir.md) den MIDL-Compiler an, das aktuelle Verzeichnis zu ignorieren, die von der INCLUDE-Umgebungsvariablen angegebenen Verzeichnisse zu ignorieren und nur die angegebenen Verzeichnisse zu durchsuchen.

Wenn mit dem Schalter **/I** keine Verzeichnisse angegeben werden, weist der Schalter [**/no \_ def \_ idir**](-no-def-idir.md) den MIDL-Compiler an, nur das aktuelle Verzeichnis zu durchsuchen.

## <a name="examples"></a>Beispiele

**midl /I c: \\ include;c: \\ include \\ h /I \\ include2 filename.idl**

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Allgemeine MIDL-Befehlszeilensyntax](general-midl-command-line-syntax.md)
</dt> <dt>

[**/acf**](-acf.md)
</dt> <dt>

[**/cpp \_ cmd**](-cpp-cmd.md)
</dt> <dt>

[**/cpp \_ opt**](-cpp-opt.md)
</dt> <dt>

[**/no \_ def \_ idir**](-no-def-idir.md)
</dt> </dl>

 

 





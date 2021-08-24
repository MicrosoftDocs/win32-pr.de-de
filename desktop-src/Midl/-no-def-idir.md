---
title: /no_def_idir Schalter
description: Wenn Verzeichnisse mit dem Schalter /I angegeben werden, weist der Schalter /no def idir den MIDL-Compiler an, nur verzeichnisse zu durchsuchen, die mit dem \_ \_ Schalter /I angegeben sind.
ms.assetid: 9a396de4-332d-4832-8e8b-291690cd3a10
keywords:
- /no_def_idir MIDL-Switch
topic_type:
- apiref
api_name:
- /no_def_idir
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c93d61bff28ad0aa4306047755c88419d0b925431f9b3ea476ec957dcd62b98
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811300"
---
# <a name="no_def_idir-switch"></a>/no \_ def \_ idir switch

Wenn Verzeichnisse mit dem Schalter [**/I**](-i.md) angegeben werden, weist der Schalter **/no \_ def \_ idir** den MIDL-Compiler an, nur die verzeichnisse zu durchsuchen, die mit dem **/I-Schalter** angegeben sind, und ignoriert dabei das aktuelle Verzeichnis sowie die von der INCLUDE-Umgebungsvariablen angegebenen Verzeichnisse.

``` syntax
midl /no_def_idir
```

## <a name="switch-options"></a>Switch-Optionen

Dieser Schalter verfügt über keine Parameter.

## <a name="remarks"></a>Hinweise

Wenn mit dem Schalter [**/I**](-i.md) keine Verzeichnisse angegeben werden, weist der **Schalter /no \_ def \_ idir** den MIDL-Compiler an, nur das aktuelle Verzeichnis zu durchsuchen.

## <a name="examples"></a>Beispiele

``` syntax
; search only the current directory 
midl /no_def_idir filename.idl  

; search only the specified directories 
midl /no_def_idir /I c:\c700\include filename.idl 
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Allgemeine MIDL-Befehlszeilensyntax](general-midl-command-line-syntax.md)
</dt> <dt>

[**/acf**](-acf.md)
</dt> <dt>

[**/I**](-i.md)
</dt> </dl>

 

 





---
title: /no_def_idir Schalter
description: Wenn Verzeichnisse mit dem/I-Schalter angegeben werden, weist der/No \_ DEF \_ Idir-Schalter den Mittelwert-Compiler an, nur Verzeichnisse zu durchsuchen, die mit dem/I-Schalter angegeben wurden.
ms.assetid: 9a396de4-332d-4832-8e8b-291690cd3a10
keywords:
- /no_def_idir-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /no_def_idir
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62ed845c73c36fbbfe4ea7dea952ee4541b043a7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857584"
---
# <a name="no_def_idir-switch"></a>/No \_ DEF ( \_ Idir-Schalter)

Wenn Verzeichnisse mit dem [**/I**](-i.md) -Schalter angegeben werden, weist der **/No \_ DEF \_ Idir** -Schalter den Mittelwert-Compiler an, nur die Verzeichnisse zu durchsuchen, die mit dem **/I** -Schalter angegeben werden, wobei das aktuelle Verzeichnis sowie die von der INCLUDE-Umgebungsvariablen angegebenen Verzeichnisse ignoriert werden.

``` syntax
midl /no_def_idir
```

## <a name="switch-options"></a>Optionen wechseln

Dieser Switch hat keine Parameter.

## <a name="remarks"></a>Bemerkungen

Wenn keine Verzeichnisse mit dem [**/I**](-i.md) -Schalter angegeben werden, weist der **/No \_ DEF \_ Idir** -Schalter den Mittelwert Compiler an, nur das aktuelle Verzeichnis zu durchsuchen.

## <a name="examples"></a>Beispiele

``` syntax
; search only the current directory 
midl /no_def_idir filename.idl  

; search only the specified directories 
midl /no_def_idir /I c:\c700\include filename.idl 
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Allgemeine Syntax der Mittell-Befehlszeile](general-midl-command-line-syntax.md)
</dt> <dt>

[**/acf**](-acf.md)
</dt> <dt>

[**/I**](-i.md)
</dt> </dl>

 

 





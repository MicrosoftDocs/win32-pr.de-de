---
title: Attribut ohne Vorzeichen
description: Das Schlüsselwort unsigned gibt an, dass das wichtigste Bit einer ganzzahligen Variablen ein Datenbit anstelle eines Vorzeichenbits darstellt.
ms.assetid: bfcc6bec-895e-45e1-b162-b79651662aa6
keywords:
- MIDL-Attribut ohne Vorzeichen
topic_type:
- apiref
api_name:
- unsigned
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 383a8fc0379ca81abb9ad0a88edab8750661bdfa429e32e7e91d193aa0fd2938
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146173"
---
# <a name="unsigned-attribute"></a>Attribut ohne Vorzeichen

Das Schlüsselwort **unsigned** gibt an, dass das wichtigste Bit einer ganzzahligen Variablen ein Datenbit anstelle eines Vorzeichenbits darstellt.

``` syntax
[[ unsigned ]] type-qualifier [[ int ]]identifier-name;
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*type-qualifier* 
</dt> <dd>

Kann ein beliebiges vom [**Typ char**](char-idl.md), [**wchar \_ t**](wchar-t.md), [**long**](long.md), [**int**](int.md), [**short**](short.md)und [**small**](small.md)sein.

</dd> <dt>

*Bezeichnername* 
</dt> <dd>

Gibt einen gültigen MIDL-Bezeichner an. Gültige MIDL-Bezeichner bestehen aus bis zu 31 alphanumerischen Zeichen und/oder Unterstrichen und müssen mit einem Alphabet- oder Unterstrich beginnen.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Dieses Schlüsselwort ist optional und kann mit jedem der Zeichen- und Ganzzahltypen [**char**](char-idl.md), [**wchar \_ t**](wchar-t.md), [**long**](long.md), [**short**](short.md)und [**small**](small.md)verwendet werden. Sie können optional das Schlüsselwort [**int**](int.md) nach den Typqualifizierern **long,** **short** und **small** einfügen.

Wenn Sie den MIDL-Compilerschalter [**/char**](-char.md)verwenden, können Zeichen- und Ganzzahltypen, die in der IDL-Datei ohne explizite Vorzeichenschlüsselwörter angezeigt werden, mit dem Schlüsselwort [**signed**](signed.md) oder **unsigned** in der generierten Headerdatei angezeigt werden. Um Verwirrung zu vermeiden, geben Sie das Vorzeichen der Ganzzahl- und Zeichentypen an.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[MIDL-Basistypen](midl-base-types.md)
</dt> <dt>

[**Char**](char-idl.md)
</dt> <dt>

[**/char**](-char.md)
</dt> <dt>

[IDL-Datei (Interface Definition)](interface-definition-idl-file.md)
</dt> <dt>

[**INT**](int.md)
</dt> <dt>

[**long**](long.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**Unterzeichnet**](signed.md)
</dt> <dt>

[**klein**](small.md)
</dt> <dt>

[**wchar \_ t**](wchar-t.md)
</dt> </dl>

 

 





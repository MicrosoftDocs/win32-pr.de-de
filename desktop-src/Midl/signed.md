---
title: signed-Attribut
description: Das Schlüsselwort signed gibt an, dass das wichtigste Bit einer ganzzahligen Variablen ein Vorzeichenbit und kein Datenbit darstellt.
ms.assetid: 6116089a-647e-485b-8f79-9c9267aa4810
keywords:
- SIGNED-Attribut MIDL
topic_type:
- apiref
api_name:
- signed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f3db15bc46d6d8ab3ec108c648d094ebf706d9286a8c4b0a823fa409e118e3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641334"
---
# <a name="signed-attribute"></a>signed-Attribut

Das **Schlüsselwort signed** gibt an, dass das wichtigste Bit einer ganzzahligen Variablen ein Vorzeichenbit und kein Datenbit darstellt.

``` syntax
[[ signed ]] type-qualifier [[ int ]]identifier-name;
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*type-qualifier* 
</dt> <dd>

Kann ein beliebiges [**von char,**](char-idl.md) [**wchar \_ t,**](wchar-t.md) [**long,**](long.md) [**short**](short.md)und [**small sein.**](small.md)

</dd> <dt>

*Bezeichnername* 
</dt> <dd>

Gibt einen gültigen MIDL-Bezeichner an. Gültige MIDL-Bezeichner bestehen aus bis zu 31 alphanumerischen und/oder Unterstrichen und müssen mit einem alphabetischen oder Unterstrich beginnen.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Dieses Schlüsselwort ist optional und kann mit jedem der Zeichen- und Ganzzahltypen [**char,**](char-idl.md) [**wchar \_ t,**](wchar-t.md) [**long,**](long.md) [**short**](short.md)und [**small verwendet werden.**](small.md) Optional können Sie das Schlüsselwort [**int nach**](int.md) den Typqualifizierern **long,** **short** und **small verwenden.**

Wenn Sie den MIDL-Compilerschalter [**char**](char-idl.md)verwenden, können Zeichen- und Ganzzahltypen, die in der IDL-Datei ohne explizite Vorzeichenschlüsselwörter angezeigt werden, mit den Schlüsselwörtern **signed** oder [**unsigned**](unsigned.md) in der generierten Headerdatei angezeigt werden. Um Verwirrung zu vermeiden, geben Sie das Vorzeichen der Ganzzahl- und Zeichentypen an.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[MIDL-Basistypen](midl-base-types.md)
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

[**klein**](small.md)
</dt> <dt>

[**Unsigned**](unsigned.md)
</dt> <dt>

[**wchar \_ t**](wchar-t.md)
</dt> </dl>

 

 




